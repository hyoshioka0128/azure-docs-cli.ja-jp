---
title: zypper を使用して Linux に Azure CLI 2.0 をインストールする
description: zypper で Azure CLI 2.0 をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 01/29/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: a862cca17adb1bfa0201af250819158081c29813
ms.sourcegitcommit: 5c80e96e96f9608c92a94fa4a9c4afb25099f3fc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/13/2018
ms.locfileid: "35512973"
---
# <a name="install-azure-cli-20-with-zypper"></a><span data-ttu-id="14cac-103">zypper での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="14cac-103">Install Azure CLI 2.0 with zypper</span></span>

<span data-ttu-id="14cac-104">openSUSE や SLES など、`zypper` が付属するディストリビューションを実行している場合は、Azure CLI 用の利用可能なパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="14cac-104">If you are running a distribution that comes with `zypper`, such as openSUSE or SLES, there is a package available for the Azure CLI.</span></span> <span data-ttu-id="14cac-105">このパッケージは、openSUSE 42.2 と SLES 12 SP 2 でテストされています。</span><span class="sxs-lookup"><span data-stu-id="14cac-105">This package has been tested with openSUSE 42.2 and SLES 12 SP 2.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="14cac-106">Install</span><span class="sxs-lookup"><span data-stu-id="14cac-106">Install</span></span>

1. <span data-ttu-id="14cac-107">`curl` をインストールします。</span><span class="sxs-lookup"><span data-stu-id="14cac-107">Install `curl`:</span></span>

   ```bash
   sudo zypper install -y curl
   ```

2. <span data-ttu-id="14cac-108">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="14cac-108">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. <span data-ttu-id="14cac-109">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="14cac-109">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo zypper addrepo --name 'Azure CLI' --check https://packages.microsoft.com/yumrepos/azure-cli azure-cli
   ```

4. <span data-ttu-id="14cac-110">`zypper` パッケージのインデックスを更新し、インストールを行います。</span><span class="sxs-lookup"><span data-stu-id="14cac-110">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper install --from azure-cli -y azure-cli
   ```

<span data-ttu-id="14cac-111">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="14cac-111">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="14cac-112">ログインするには、`az login` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="14cac-112">To log in, run the `az login` command.</span></span>

```azurecli
az login
```

<span data-ttu-id="14cac-113">さまざまなログイン方法の詳細については、「[Azure CLI 2.0 を使用してログインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="14cac-113">To learn more about different login methods, see [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="update"></a><span data-ttu-id="14cac-114">アップデート</span><span class="sxs-lookup"><span data-stu-id="14cac-114">Update</span></span>

<span data-ttu-id="14cac-115">`zypper update` コマンドでパッケージを更新できます。</span><span class="sxs-lookup"><span data-stu-id="14cac-115">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="14cac-116">アンインストール</span><span class="sxs-lookup"><span data-stu-id="14cac-116">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="14cac-117">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="14cac-117">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="14cac-118">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="14cac-118">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

  ```bash
  sudo zypper removerepo azure-cli
  ```

3. <span data-ttu-id="14cac-119">リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。</span><span class="sxs-lookup"><span data-stu-id="14cac-119">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

