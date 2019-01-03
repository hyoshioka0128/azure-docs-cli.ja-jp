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
ms.devlang: azurecli
ms.openlocfilehash: 4cdbeaffb00e87b590080c1d341ec9e7ee198410
ms.sourcegitcommit: f40bd067ece4e6ec13e259782ed8db3e33b61a75
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/18/2018
ms.locfileid: "53593525"
---
# <a name="install-azure-cli-with-zypper"></a><span data-ttu-id="7ee98-103">zypper での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="7ee98-103">Install Azure CLI with zypper</span></span>

<span data-ttu-id="7ee98-104">openSUSE や SLES など、`zypper` が付属するディストリビューションには、Azure CLI 用に利用できるパッケージが用意されています。</span><span class="sxs-lookup"><span data-stu-id="7ee98-104">For Linux distributions with `zypper`, such as openSUSE or SLES, there's a package available for the Azure CLI.</span></span> <span data-ttu-id="7ee98-105">このパッケージは、openSUSE 42.2 と SLES 12 SP 2 でテストされています。</span><span class="sxs-lookup"><span data-stu-id="7ee98-105">This package has been tested with openSUSE 42.2 and SLES 12 SP 2.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="7ee98-106">Install</span><span class="sxs-lookup"><span data-stu-id="7ee98-106">Install</span></span>

1. <span data-ttu-id="7ee98-107">`curl` をインストールします。</span><span class="sxs-lookup"><span data-stu-id="7ee98-107">Install `curl`:</span></span>

   ```bash
   sudo zypper install -y curl
   ```

2. <span data-ttu-id="7ee98-108">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="7ee98-108">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. <span data-ttu-id="7ee98-109">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="7ee98-109">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo zypper addrepo --name 'Azure CLI' --check https://packages.microsoft.com/yumrepos/azure-cli azure-cli
   ```

4. <span data-ttu-id="7ee98-110">`zypper` パッケージのインデックスを更新し、インストールを行います。</span><span class="sxs-lookup"><span data-stu-id="7ee98-110">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper install --from azure-cli -y azure-cli
   ```

<span data-ttu-id="7ee98-111">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="7ee98-111">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="7ee98-112">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="7ee98-112">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="7ee98-113">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7ee98-113">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="7ee98-114">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="7ee98-114">Troubleshooting</span></span>

<span data-ttu-id="7ee98-115">ここでは、`zypper` でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="7ee98-115">Here are some common problems seen when installing with `zypper`.</span></span> <span data-ttu-id="7ee98-116">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="7ee98-116">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]


## <a name="update"></a><span data-ttu-id="7ee98-117">アップデート</span><span class="sxs-lookup"><span data-stu-id="7ee98-117">Update</span></span>

<span data-ttu-id="7ee98-118">`zypper update` コマンドでパッケージを更新できます。</span><span class="sxs-lookup"><span data-stu-id="7ee98-118">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="7ee98-119">アンインストール</span><span class="sxs-lookup"><span data-stu-id="7ee98-119">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="7ee98-120">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="7ee98-120">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="7ee98-121">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="7ee98-121">If you don't plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo zypper removerepo azure-cli
   ```

3. <span data-ttu-id="7ee98-122">リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。</span><span class="sxs-lookup"><span data-stu-id="7ee98-122">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

   ```bash
   MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
   sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
   ```
   ## <a name="next-steps"></a><span data-ttu-id="7ee98-123">次の手順</span><span class="sxs-lookup"><span data-stu-id="7ee98-123">Next Steps</span></span>

<span data-ttu-id="7ee98-124">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="7ee98-124">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="7ee98-125">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="7ee98-125">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
