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
ms.openlocfilehash: a98a51e4dc3ac85d27e27ef9b9164a7f98431d31
ms.sourcegitcommit: ee64dc738cfe689a2a479e32a87bf420f96c31c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2020
ms.locfileid: "78953328"
---
# <a name="install-azure-cli-with-yum"></a><span data-ttu-id="9a518-103">yum での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="9a518-103">Install Azure CLI with yum</span></span>

<span data-ttu-id="9a518-104">RHEL、Fedora、CentOS など、`yum` が付属する Linux ディストリビューションには、Azure CLI 用のパッケージが用意されています。</span><span class="sxs-lookup"><span data-stu-id="9a518-104">For Linux distributions with `yum` such as RHEL, Fedora, or CentOS, there's a package for the Azure CLI.</span></span> <span data-ttu-id="9a518-105">このパッケージは、RHEL 7.7、RHEL 8、Fedora 24 以降、CentOS 7、および CentOS 8 でテストされています。</span><span class="sxs-lookup"><span data-stu-id="9a518-105">This package has been tested with RHEL 7.7, RHEL 8, Fedora 24 and higher, CentOS 7 and CentOS 8.</span></span>

[!INCLUDE [current-version](includes/current-version.md)]

[!INCLUDE [rpm-warning](includes/rpm-warning.md)]

## <a name="install"></a><span data-ttu-id="9a518-106">インストール</span><span class="sxs-lookup"><span data-stu-id="9a518-106">Install</span></span>

1. <span data-ttu-id="9a518-107">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="9a518-107">Import the Microsoft repository key.</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="9a518-108">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="9a518-108">Create local `azure-cli` repository information.</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]
   name=Azure CLI
   baseurl=https://packages.microsoft.com/yumrepos/azure-cli
   enabled=1
   gpgcheck=1
   gpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="9a518-109">`yum install` コマンドを使用してインストールします。</span><span class="sxs-lookup"><span data-stu-id="9a518-109">Install with the `yum install` command.</span></span>

   ```bash
   sudo yum install azure-cli
   ```

<span data-ttu-id="9a518-110">`az` コマンドで Azure CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a518-110">Run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="9a518-111">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a518-111">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="9a518-112">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a518-112">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="9a518-113">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="9a518-113">Troubleshooting</span></span>

<span data-ttu-id="9a518-114">ここでは、`yum` でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="9a518-114">Here are some common problems seen when installing with `yum`.</span></span> <span data-ttu-id="9a518-115">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="9a518-115">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="install-on-rhel-76-or-other-systems-without-python-3"></a><span data-ttu-id="9a518-116">Python 3 を含まない RHEL 7.6 またはその他のシステムにインストールする</span><span class="sxs-lookup"><span data-stu-id="9a518-116">Install on RHEL 7.6 or other systems without Python 3</span></span>

<span data-ttu-id="9a518-117">可能な場合は、`python3` パッケージの正式なサポートを含むバージョンにシステムをアップグレードしてください。</span><span class="sxs-lookup"><span data-stu-id="9a518-117">If you can, please upgrade your system to a version with official support for `python3` package.</span></span> <span data-ttu-id="9a518-118">それ以外の場合は、最初に `python3` パッケージをインストールする ([ソースからビルドする](https://github.com/linux-on-ibm-z/docs/wiki/Building-Python-3.6.x)か、[追加のリポジトリ](https://developers.redhat.com/blog/2018/08/13/install-python3-rhel/)を使用してインストールする) 必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a518-118">Otherwise, you need to first install a `python3` package, either [build from source](https://github.com/linux-on-ibm-z/docs/wiki/Building-Python-3.6.x) or install through some [additional repo](https://developers.redhat.com/blog/2018/08/13/install-python3-rhel/).</span></span> <span data-ttu-id="9a518-119">その後、パッケージをダウンロードして、依存関係なしでインストールできます。</span><span class="sxs-lookup"><span data-stu-id="9a518-119">Then you can download the package and install it without dependency.</span></span>
```bash
$ sudo yum install yum-utils
$ sudo yumdownloader azure-cli
$ sudo rpm -ivh --nodeps azure-cli-*.rpm
```

<span data-ttu-id="9a518-120">python3 を設定しても、CLI を実行しようするとエラー `python3: command not found` が依然として表示される場合は、パスにそれを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a518-120">If you have setup python3 but are still getting an error `python3: command not found` when trying to run the cli, you need to add it to your path.</span></span>
```bash
$ scl enable rh-python36 bash
```

### <a name="proxy-blocks-connection"></a><span data-ttu-id="9a518-121">プロキシによる接続のブロック</span><span class="sxs-lookup"><span data-stu-id="9a518-121">Proxy blocks connection</span></span>

[!INCLUDE[configure-proxy](includes/configure-proxy.md)]

<span data-ttu-id="9a518-122">常にこのプロキシを使用するように `yum` を明示的に構成することが必要な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="9a518-122">You may also want to explicitly configure `yum` to use this proxy at all times.</span></span> <span data-ttu-id="9a518-123">次の行が `[main]` の `/etc/yum.conf` セクションの下に表示されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9a518-123">Make sure that the following lines appear under the `[main]` section of `/etc/yum.conf`:</span></span>

```yum.conf
[main]
# ...
proxy=http://[proxy]:[port] # If your proxy requires https, change http->https
proxy_username=[username] # Only required for basic auth
proxy_password=[password] # Only required for basic auth
```

<span data-ttu-id="9a518-124">Microsoft 署名キーを取得し、リポジトリからパッケージを取得するには、お使いのプロキシで次のアドレスへの HTTPS 接続を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a518-124">In order to get the Microsoft signing key and get the package from our repository, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://packages.microsoft.com`

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]

## <a name="update"></a><span data-ttu-id="9a518-125">更新</span><span class="sxs-lookup"><span data-stu-id="9a518-125">Update</span></span>

<span data-ttu-id="9a518-126">`yum update` コマンドで Azure CLI を更新します。</span><span class="sxs-lookup"><span data-stu-id="9a518-126">Update the Azure CLI with the `yum update` command.</span></span>

```bash
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="9a518-127">アンインストール</span><span class="sxs-lookup"><span data-stu-id="9a518-127">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="9a518-128">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="9a518-128">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="9a518-129">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="9a518-129">If you don't plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="9a518-130">他の Microsoft パッケージを使用しない場合は、署名キーを削除します。</span><span class="sxs-lookup"><span data-stu-id="9a518-130">If you don't use any other Microsoft packages, remove the signing key.</span></span>

   ```bash
   MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
   sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
   ```

## <a name="next-steps"></a><span data-ttu-id="9a518-131">次の手順</span><span class="sxs-lookup"><span data-stu-id="9a518-131">Next Steps</span></span>

<span data-ttu-id="9a518-132">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="9a518-132">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="9a518-133">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="9a518-133">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
