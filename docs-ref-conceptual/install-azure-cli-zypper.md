---
title: zypper を使用して Linux に Azure CLI 2.0 をインストールする
description: zypper で Azure CLI 2.0 をインストールする方法
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 01d293eff229ab8b0eb3a3ff4e23978ea9e00174
ms.sourcegitcommit: 0e9aafa07311526f43661c8bd3a7eba7cbc2caed
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2018
---
# <a name="install-azure-cli-20-with-zypper"></a><span data-ttu-id="7d74d-103">zypper での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="7d74d-103">Install Azure CLI 2.0 with zypper</span></span>

<span data-ttu-id="7d74d-104">openSUSE や SLES など、`zypper` が付属するディストリビューションを実行している場合は、Azure CLI 用の利用可能なパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="7d74d-104">If you are running a distribution that comes with `zypper`, such as openSUSE or SLES, there is a package available for the Azure CLI.</span></span> <span data-ttu-id="7d74d-105">このパッケージは、openSUSE 42.2 と SLES 12 SP 2 でテストされています。</span><span class="sxs-lookup"><span data-stu-id="7d74d-105">This package has been tested with openSUSE 42.2 and SLES 12 SP 2.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="7d74d-106">Install</span><span class="sxs-lookup"><span data-stu-id="7d74d-106">Install</span></span>

1. <span data-ttu-id="7d74d-107">`curl` をインストールします。</span><span class="sxs-lookup"><span data-stu-id="7d74d-107">Install `curl`:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install -y curl
   ```

2. <span data-ttu-id="7d74d-108">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="7d74d-108">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. <span data-ttu-id="7d74d-109">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="7d74d-109">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

4. <span data-ttu-id="7d74d-110">`zypper` パッケージのインデックスを更新し、インストールを行います。</span><span class="sxs-lookup"><span data-stu-id="7d74d-110">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install -y azure-cli
   ```

<span data-ttu-id="7d74d-111">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="7d74d-111">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="7d74d-112">ログインするには、`az login` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7d74d-112">To log in, run the `az login` command.</span></span>

```azurecli
az login
```

<span data-ttu-id="7d74d-113">さまざまなログイン方法の詳細については、「[Azure CLI 2.0 を使用してログインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7d74d-113">To learn more about different login methods, see [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="update"></a><span data-ttu-id="7d74d-114">プライマリの</span><span class="sxs-lookup"><span data-stu-id="7d74d-114">Update</span></span>

<span data-ttu-id="7d74d-115">`zypper update` コマンドでパッケージを更新できます。</span><span class="sxs-lookup"><span data-stu-id="7d74d-115">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="7d74d-116">アンインストール</span><span class="sxs-lookup"><span data-stu-id="7d74d-116">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="7d74d-117">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="7d74d-117">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="7d74d-118">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="7d74d-118">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

  ```bash
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. <span data-ttu-id="7d74d-119">リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。</span><span class="sxs-lookup"><span data-stu-id="7d74d-119">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

