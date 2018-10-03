---
title: zypper を使用して Linux に Azure CLI をインストールする
description: zypper で Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 201cce81046d5039a313b918ac48b2849352995c
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47177676"
---
# <a name="install-azure-cli-with-zypper"></a><span data-ttu-id="4c06a-103">zypper での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="4c06a-103">Install Azure CLI with zypper</span></span>

<span data-ttu-id="4c06a-104">openSUSE や SLES など、`zypper` が付属するディストリビューションには、Azure CLI 用に利用できるパッケージが用意されています。</span><span class="sxs-lookup"><span data-stu-id="4c06a-104">For Linux distributions with `zypper`, such as openSUSE or SLES, there's a package available for the Azure CLI.</span></span> <span data-ttu-id="4c06a-105">このパッケージは、openSUSE 42.2 と SLES 12 SP 2 でテストされています。</span><span class="sxs-lookup"><span data-stu-id="4c06a-105">This package has been tested with openSUSE 42.2 and SLES 12 SP 2.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="4c06a-106">Install</span><span class="sxs-lookup"><span data-stu-id="4c06a-106">Install</span></span>

1. <span data-ttu-id="4c06a-107">`curl` をインストールします。</span><span class="sxs-lookup"><span data-stu-id="4c06a-107">Install `curl`:</span></span>

   ```bash
   sudo zypper install -y curl
   ```

2. <span data-ttu-id="4c06a-108">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4c06a-108">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. <span data-ttu-id="4c06a-109">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="4c06a-109">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo zypper addrepo --name 'Azure CLI' --check https://packages.microsoft.com/yumrepos/azure-cli azure-cli
   ```

4. <span data-ttu-id="4c06a-110">`zypper` パッケージのインデックスを更新し、インストールを行います。</span><span class="sxs-lookup"><span data-stu-id="4c06a-110">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper install --from azure-cli -y azure-cli
   ```

<span data-ttu-id="4c06a-111">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="4c06a-111">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="4c06a-112">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="4c06a-112">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="4c06a-113">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c06a-113">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="update"></a><span data-ttu-id="4c06a-114">アップデート</span><span class="sxs-lookup"><span data-stu-id="4c06a-114">Update</span></span>

<span data-ttu-id="4c06a-115">`zypper update` コマンドでパッケージを更新できます。</span><span class="sxs-lookup"><span data-stu-id="4c06a-115">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="4c06a-116">アンインストール</span><span class="sxs-lookup"><span data-stu-id="4c06a-116">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="4c06a-117">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="4c06a-117">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="4c06a-118">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="4c06a-118">If you don't plan to reinstall the CLI, remove the repository information.</span></span>

  ```bash
  sudo zypper removerepo azure-cli
  ```

3. <span data-ttu-id="4c06a-119">リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。</span><span class="sxs-lookup"><span data-stu-id="4c06a-119">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```
## <a name="next-steps"></a><span data-ttu-id="4c06a-120">次の手順</span><span class="sxs-lookup"><span data-stu-id="4c06a-120">Next Steps</span></span>

<span data-ttu-id="4c06a-121">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="4c06a-121">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="4c06a-122">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="4c06a-122">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
