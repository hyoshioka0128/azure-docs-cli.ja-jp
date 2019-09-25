---
title: yum を使用して Linux に Azure CLI をインストールする
description: yum で Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 270be4c41bdb3c913e41ef1b2bb0c7c0b393aa20
ms.sourcegitcommit: 5a29ce9c0a3d7b831f22b1a13b1ae2e239e5549f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/19/2019
ms.locfileid: "71144033"
---
# <a name="install-azure-cli-with-yum"></a><span data-ttu-id="09208-103">yum での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="09208-103">Install Azure CLI with yum</span></span>

<span data-ttu-id="09208-104">RHEL、Fedora、CentOS など、`yum` が付属する Linux ディストリビューションには、Azure CLI 用のパッケージが用意されています。</span><span class="sxs-lookup"><span data-stu-id="09208-104">For Linux distributions with  `yum` such as RHEL, Fedora, or CentOS, there's a package for the Azure CLI.</span></span> <span data-ttu-id="09208-105">このパッケージは、RHEL 7、Fedora 19 以降、CentOS 7 でテストされています。</span><span class="sxs-lookup"><span data-stu-id="09208-105">This package has been tested with RHEL 7, Fedora 19 and higher, and CentOS 7.</span></span>

[!INCLUDE [current-version](includes/current-version.md)]

[!INCLUDE [rpm-warning](includes/rpm-warning.md)]

## <a name="install"></a><span data-ttu-id="09208-106">Install</span><span class="sxs-lookup"><span data-stu-id="09208-106">Install</span></span>

1. <span data-ttu-id="09208-107">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="09208-107">Import the Microsoft repository key.</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="09208-108">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="09208-108">Create local `azure-cli` repository information.</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]
   name=Azure CLI
   baseurl=https://packages.microsoft.com/yumrepos/azure-cli
   enabled=1
   gpgcheck=1
   gpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="09208-109">`yum install` コマンドを使用してインストールします。</span><span class="sxs-lookup"><span data-stu-id="09208-109">Install with the `yum install` command.</span></span>

   ```bash
   sudo yum install azure-cli
   ```

<span data-ttu-id="09208-110">`az` コマンドで Azure CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="09208-110">Run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="09208-111">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="09208-111">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="09208-112">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09208-112">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="09208-113">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="09208-113">Troubleshooting</span></span>

<span data-ttu-id="09208-114">ここでは、`yum` でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="09208-114">Here are some common problems seen when installing with `yum`.</span></span> <span data-ttu-id="09208-115">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="09208-115">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="09208-116">プロキシによる接続のブロック</span><span class="sxs-lookup"><span data-stu-id="09208-116">Proxy blocks connection</span></span>

[!INCLUDE[configure-proxy](includes/configure-proxy.md)]

<span data-ttu-id="09208-117">常にこのプロキシを使用するように `yum` を明示的に構成することが必要な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="09208-117">You may also want to explicitly configure `yum` to use this proxy at all times.</span></span> <span data-ttu-id="09208-118">次の行が `/etc/yum.conf` の `[main]` セクションの下に表示されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="09208-118">Make sure that the following lines appear under the `[main]` section of `/etc/yum.conf`:</span></span>

```yum.conf
[main]
# ...
proxy=http://[proxy]:[port] # If your proxy requires https, change http->https
proxy_username=[username] # Only required for basic auth
proxy_password=[password] # Only required for basic auth
```

<span data-ttu-id="09208-119">Microsoft 署名キーを取得し、リポジトリからパッケージを取得するには、お使いのプロキシで次のアドレスへの HTTPS 接続を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09208-119">In order to get the Microsoft signing key and get the package from our repository, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://packages.microsoft.com`

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]

## <a name="update"></a><span data-ttu-id="09208-120">アップデート</span><span class="sxs-lookup"><span data-stu-id="09208-120">Update</span></span>

<span data-ttu-id="09208-121">`yum update` コマンドで Azure CLI を更新します。</span><span class="sxs-lookup"><span data-stu-id="09208-121">Update the Azure CLI with the `yum update` command.</span></span>

```bash
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="09208-122">アンインストール</span><span class="sxs-lookup"><span data-stu-id="09208-122">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="09208-123">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="09208-123">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="09208-124">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="09208-124">If you don't plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="09208-125">他の Microsoft パッケージを使用しない場合は、署名キーを削除します。</span><span class="sxs-lookup"><span data-stu-id="09208-125">If you don't use any other Microsoft packages, remove the signing key.</span></span>

   ```bash
   MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
   sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
   ```

## <a name="next-steps"></a><span data-ttu-id="09208-126">次の手順</span><span class="sxs-lookup"><span data-stu-id="09208-126">Next Steps</span></span>

<span data-ttu-id="09208-127">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="09208-127">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="09208-128">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="09208-128">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
