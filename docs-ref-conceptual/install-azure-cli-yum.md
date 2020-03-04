---
title: yum を使用して Linux に Azure CLI をインストールする
description: yum で Azure CLI をインストールする方法
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 11/26/2019
ms.topic: conceptual
ms.service: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: ad773a58cf784c46a1c605e7e7eca58de8a4a722
ms.sourcegitcommit: 7caa6673f65e61deb8d6def6386e4eb9acdac923
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2020
ms.locfileid: "77780113"
---
# <a name="install-azure-cli-with-yum"></a><span data-ttu-id="6c537-103">yum での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="6c537-103">Install Azure CLI with yum</span></span>

<span data-ttu-id="6c537-104">RHEL、Fedora、CentOS など、`yum` が付属する Linux ディストリビューションには、Azure CLI 用のパッケージが用意されています。</span><span class="sxs-lookup"><span data-stu-id="6c537-104">For Linux distributions with `yum` such as RHEL, Fedora, or CentOS, there's a package for the Azure CLI.</span></span> <span data-ttu-id="6c537-105">このパッケージは、RHEL 7.7、RHEL 8、Fedora 24 以降、CentOS 7、および CentOS 8 でテストされています。</span><span class="sxs-lookup"><span data-stu-id="6c537-105">This package has been tested with RHEL 7.7, RHEL 8, Fedora 24 and higher, CentOS 7 and CentOS 8.</span></span>

[!INCLUDE [current-version](includes/current-version.md)]

[!INCLUDE [rpm-warning](includes/rpm-warning.md)]

## <a name="install"></a><span data-ttu-id="6c537-106">インストール</span><span class="sxs-lookup"><span data-stu-id="6c537-106">Install</span></span>

1. <span data-ttu-id="6c537-107">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="6c537-107">Import the Microsoft repository key.</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="6c537-108">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="6c537-108">Create local `azure-cli` repository information.</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]
   name=Azure CLI
   baseurl=https://packages.microsoft.com/yumrepos/azure-cli
   enabled=1
   gpgcheck=1
   gpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="6c537-109">`yum install` コマンドを使用してインストールします。</span><span class="sxs-lookup"><span data-stu-id="6c537-109">Install with the `yum install` command.</span></span>

   ```bash
   sudo yum install azure-cli
   ```

<span data-ttu-id="6c537-110">`az` コマンドで Azure CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="6c537-110">Run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="6c537-111">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6c537-111">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="6c537-112">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c537-112">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="6c537-113">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="6c537-113">Troubleshooting</span></span>

<span data-ttu-id="6c537-114">ここでは、`yum` でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="6c537-114">Here are some common problems seen when installing with `yum`.</span></span> <span data-ttu-id="6c537-115">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="6c537-115">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="install-on-rhel-76-or-other-systems-without-python-3"></a><span data-ttu-id="6c537-116">Python 3 を含まない RHEL 7.6 またはその他のシステムにインストールする</span><span class="sxs-lookup"><span data-stu-id="6c537-116">Install on RHEL 7.6 or other systems without Python 3</span></span>

<span data-ttu-id="6c537-117">可能な場合は、`python3` パッケージの正式なサポートを含むバージョンにシステムをアップグレードしてください。</span><span class="sxs-lookup"><span data-stu-id="6c537-117">If you can, please upgrade your system to a version with official support for `python3` package.</span></span> <span data-ttu-id="6c537-118">それ以外の場合は、最初に `python3` パッケージをインストールする ([ソースからビルドする](https://github.com/linux-on-ibm-z/docs/wiki/Building-Python-3.6.x)か、[追加のリポジトリ](https://developers.redhat.com/blog/2018/08/13/install-python3-rhel/)を使用してインストールする) 必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c537-118">Otherwise, you need to first install a `python3` package, either [build from source](https://github.com/linux-on-ibm-z/docs/wiki/Building-Python-3.6.x) or install through some [additional repo](https://developers.redhat.com/blog/2018/08/13/install-python3-rhel/).</span></span> <span data-ttu-id="6c537-119">その後、パッケージをダウンロードして、依存関係なしでインストールできます。</span><span class="sxs-lookup"><span data-stu-id="6c537-119">Then you can download the package and install it without dependency.</span></span>
```bash
$ sudo yum install yum-utils
$ sudo yumdownloader azure-cli
$ sudo rpm -ivh --nodeps azure-cli-*.rpm
```

### <a name="proxy-blocks-connection"></a><span data-ttu-id="6c537-120">プロキシによる接続のブロック</span><span class="sxs-lookup"><span data-stu-id="6c537-120">Proxy blocks connection</span></span>

[!INCLUDE[configure-proxy](includes/configure-proxy.md)]

<span data-ttu-id="6c537-121">常にこのプロキシを使用するように `yum` を明示的に構成することが必要な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="6c537-121">You may also want to explicitly configure `yum` to use this proxy at all times.</span></span> <span data-ttu-id="6c537-122">次の行が `/etc/yum.conf` の `[main]` セクションの下に表示されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6c537-122">Make sure that the following lines appear under the `[main]` section of `/etc/yum.conf`:</span></span>

```yum.conf
[main]
# ...
proxy=http://[proxy]:[port] # If your proxy requires https, change http->https
proxy_username=[username] # Only required for basic auth
proxy_password=[password] # Only required for basic auth
```

<span data-ttu-id="6c537-123">Microsoft 署名キーを取得し、リポジトリからパッケージを取得するには、お使いのプロキシで次のアドレスへの HTTPS 接続を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c537-123">In order to get the Microsoft signing key and get the package from our repository, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://packages.microsoft.com`

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]

## <a name="update"></a><span data-ttu-id="6c537-124">更新</span><span class="sxs-lookup"><span data-stu-id="6c537-124">Update</span></span>

<span data-ttu-id="6c537-125">`yum update` コマンドで Azure CLI を更新します。</span><span class="sxs-lookup"><span data-stu-id="6c537-125">Update the Azure CLI with the `yum update` command.</span></span>

```bash
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="6c537-126">アンインストール</span><span class="sxs-lookup"><span data-stu-id="6c537-126">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="6c537-127">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="6c537-127">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="6c537-128">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="6c537-128">If you don't plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="6c537-129">他の Microsoft パッケージを使用しない場合は、署名キーを削除します。</span><span class="sxs-lookup"><span data-stu-id="6c537-129">If you don't use any other Microsoft packages, remove the signing key.</span></span>

   ```bash
   MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
   sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
   ```

## <a name="next-steps"></a><span data-ttu-id="6c537-130">次の手順</span><span class="sxs-lookup"><span data-stu-id="6c537-130">Next Steps</span></span>

<span data-ttu-id="6c537-131">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="6c537-131">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="6c537-132">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="6c537-132">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
