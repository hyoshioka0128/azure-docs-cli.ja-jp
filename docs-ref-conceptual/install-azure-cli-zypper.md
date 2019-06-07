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
ms.openlocfilehash: f8a3bec4fffb731c6521fa7b8a2a90798ef191e6
ms.sourcegitcommit: 08043c47d3ccf23522b91e6bba3932e312c04c7f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2019
ms.locfileid: "66516232"
---
# <a name="install-azure-cli-with-zypper"></a><span data-ttu-id="73bf3-103">zypper での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="73bf3-103">Install Azure CLI with zypper</span></span>

<span data-ttu-id="73bf3-104">openSUSE や SLES など、`zypper` が付属するディストリビューションには、Azure CLI 用に利用できるパッケージが用意されています。</span><span class="sxs-lookup"><span data-stu-id="73bf3-104">For Linux distributions with `zypper`, such as openSUSE or SLES, there's a package available for the Azure CLI.</span></span> <span data-ttu-id="73bf3-105">このパッケージは、openSUSE 42.2 以降と SLES 12 SP 2 以降でテストされています。</span><span class="sxs-lookup"><span data-stu-id="73bf3-105">This package has been tested with openSUSE 42.2 and later, and SLES 12 SP 2 and later.</span></span>

[!INCLUDE [current-version](includes/current-version.md)]

[!INCLUDE [rpm-warning](includes/rpm-warning.md)]

## <a name="install"></a><span data-ttu-id="73bf3-106">Install</span><span class="sxs-lookup"><span data-stu-id="73bf3-106">Install</span></span>

1. <span data-ttu-id="73bf3-107">`curl` をインストールします。</span><span class="sxs-lookup"><span data-stu-id="73bf3-107">Install `curl`:</span></span>

   ```bash
   sudo zypper install -y curl
   ```

2. <span data-ttu-id="73bf3-108">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="73bf3-108">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. <span data-ttu-id="73bf3-109">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="73bf3-109">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo zypper addrepo --name 'Azure CLI' --check https://packages.microsoft.com/yumrepos/azure-cli azure-cli
   ```

4. <span data-ttu-id="73bf3-110">`zypper` パッケージのインデックスを更新し、インストールを行います。</span><span class="sxs-lookup"><span data-stu-id="73bf3-110">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper install --from azure-cli -y azure-cli
   ```

<span data-ttu-id="73bf3-111">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="73bf3-111">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="73bf3-112">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="73bf3-112">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="73bf3-113">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73bf3-113">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="73bf3-114">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="73bf3-114">Troubleshooting</span></span>

<span data-ttu-id="73bf3-115">ここでは、`zypper` でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="73bf3-115">Here are some common problems seen when installing with `zypper`.</span></span> <span data-ttu-id="73bf3-116">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="73bf3-116">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="73bf3-117">プロキシによる接続のブロック</span><span class="sxs-lookup"><span data-stu-id="73bf3-117">Proxy blocks connection</span></span>

[!INCLUDE[configure-proxy](includes/configure-proxy.md)]

<span data-ttu-id="73bf3-118">常にこのプロキシを使用するように `zypper` (`yast2` 経由) を明示的に構成することが必要な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="73bf3-118">You may also want to explicitly configure `zypper` (via `yast2`) to use this proxy at all times.</span></span> <span data-ttu-id="73bf3-119">このためには、`yast2 proxy` コマンドをスーパーユーザーとして実行し、フォームに提示された情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="73bf3-119">To do so, run the `yast2 proxy` command as superuser, and fill in the information presented in the form.</span></span> <span data-ttu-id="73bf3-120">システムでウィンドウ マネージャーを使用できる場合、`YaST Control Center` で `Network Services > Proxy` ウィンドウを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="73bf3-120">If you have a window manager available on your system, you can also use the `Network Services > Proxy` pane in the `YaST Control Center`.</span></span>

<span data-ttu-id="73bf3-121">詳細な構成やその他の情報については、[OpenSUSE プロキシの構成に関するドキュメント](https://www.suse.com/documentation/slms1/book_slms/data/sec_wy_config_updates_proxy.html)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="73bf3-121">For advanced configuration or more information, see the [OpenSUSE Proxy configuration documentation](https://www.suse.com/documentation/slms1/book_slms/data/sec_wy_config_updates_proxy.html)</span></span>

<span data-ttu-id="73bf3-122">Microsoft 署名キーを取得し、リポジトリからパッケージを取得するには、お使いのプロキシで次のアドレスへの HTTPS 接続を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="73bf3-122">In order to get the Microsoft signing key and get the package from our repository, your proxy needs to allow HTTPS connections to the following addresses:</span></span>

* `https://packages.microsoft.com`
* `https://download.opensuse.org`

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]

## <a name="update"></a><span data-ttu-id="73bf3-123">アップデート</span><span class="sxs-lookup"><span data-stu-id="73bf3-123">Update</span></span>

<span data-ttu-id="73bf3-124">`zypper update` コマンドでパッケージを更新できます。</span><span class="sxs-lookup"><span data-stu-id="73bf3-124">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="73bf3-125">アンインストール</span><span class="sxs-lookup"><span data-stu-id="73bf3-125">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="73bf3-126">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="73bf3-126">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="73bf3-127">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="73bf3-127">If you don't plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo zypper removerepo azure-cli
   ```

3. <span data-ttu-id="73bf3-128">リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。</span><span class="sxs-lookup"><span data-stu-id="73bf3-128">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

   ```bash
   MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
   sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
   ```

## <a name="next-steps"></a><span data-ttu-id="73bf3-129">次の手順</span><span class="sxs-lookup"><span data-stu-id="73bf3-129">Next Steps</span></span>

<span data-ttu-id="73bf3-130">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="73bf3-130">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="73bf3-131">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="73bf3-131">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
