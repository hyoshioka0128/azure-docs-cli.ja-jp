---
title: yum を使用して Linux に Azure CLI をインストールする
description: yum で Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 11/26/2019
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: a33b5850abc40e91a1ffbeacd49d56169f67d282
ms.sourcegitcommit: 443e14098d6643cdb2e178847d1c79b1b95146ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2019
ms.locfileid: "74543583"
---
# <a name="install-azure-cli-with-yum"></a><span data-ttu-id="9973a-103">yum での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="9973a-103">Install Azure CLI with yum</span></span>

<span data-ttu-id="9973a-104">RHEL、Fedora、CentOS など、`yum` が付属する Linux ディストリビューションには、Azure CLI 用のパッケージが用意されています。</span><span class="sxs-lookup"><span data-stu-id="9973a-104">For Linux distributions with `yum` such as RHEL, Fedora, or CentOS, there's a package for the Azure CLI.</span></span> <span data-ttu-id="9973a-105">このパッケージは、RHEL 7.7、RHEL 8、Fedora 24 以降、CentOS 7、および CentOS 8 でテストされています。</span><span class="sxs-lookup"><span data-stu-id="9973a-105">This package has been tested with RHEL 7.7, RHEL 8, Fedora 24 and higher, CentOS 7 and CentOS 8.</span></span>

[!INCLUDE [current-version](includes/current-version.md)]

[!INCLUDE [rpm-warning](includes/rpm-warning.md)]

## <a name="install"></a><span data-ttu-id="9973a-106">Install</span><span class="sxs-lookup"><span data-stu-id="9973a-106">Install</span></span>

1. <span data-ttu-id="9973a-107">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="9973a-107">Import the Microsoft repository key.</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="9973a-108">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="9973a-108">Create local `azure-cli` repository information.</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]
   name=Azure CLI
   baseurl=https://packages.microsoft.com/yumrepos/azure-cli
   enabled=1
   gpgcheck=1
   gpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="9973a-109">`yum install` コマンドを使用してインストールします。</span><span class="sxs-lookup"><span data-stu-id="9973a-109">Install with the `yum install` command.</span></span>

   ```bash
   sudo yum install azure-cli
   ```

<span data-ttu-id="9973a-110">`az` コマンドで Azure CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="9973a-110">Run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="9973a-111">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="9973a-111">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="9973a-112">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9973a-112">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="9973a-113">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="9973a-113">Troubleshooting</span></span>

<span data-ttu-id="9973a-114">ここでは、`yum` でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="9973a-114">Here are some common problems seen when installing with `yum`.</span></span> <span data-ttu-id="9973a-115">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="9973a-115">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="9973a-116">プロキシによる接続のブロック</span><span class="sxs-lookup"><span data-stu-id="9973a-116">Proxy blocks connection</span></span>

[!INCLUDE[configure-proxy](includes/configure-proxy.md)]

<span data-ttu-id="9973a-117">常にこのプロキシを使用するように `yum` を明示的に構成することが必要な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="9973a-117">You may also want to explicitly configure `yum` to use this proxy at all times.</span></span> <span data-ttu-id="9973a-118">次の行が `/etc/yum.conf` の `[main]` セクションの下に表示されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9973a-118">Make sure that the following lines appear under the `[main]` section of `/etc/yum.conf`:</span></span>

```yum.conf
[main]
# ...
proxy=http://[proxy]:[port] # If your proxy requires https, change http->https
proxy_username=[username] # Only required for basic auth
proxy_password=[password] # Only required for basic auth
```

<span data-ttu-id="9973a-119">Microsoft 署名キーを取得し、リポジトリからパッケージを取得するには、お使いのプロキシで次のアドレスへの HTTPS 接続を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9973a-119">In order to get the Microsoft signing key and get the package from our repository, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://packages.microsoft.com`

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]

### <a name="install-on-rhel-76-or-other-systems-without-python-3"></a><span data-ttu-id="9973a-120">Python 3 を含まない RHEL 7.6 またはその他のシステムにインストールする</span><span class="sxs-lookup"><span data-stu-id="9973a-120">Install on RHEL 7.6 or other systems without Python 3</span></span>

<span data-ttu-id="9973a-121">可能な場合は、`python3` パッケージの正式なサポートを含むバージョンにシステムをアップグレードしてください。</span><span class="sxs-lookup"><span data-stu-id="9973a-121">If you can, please upgrade your system to a verison with official support for `python3` package.</span></span> <span data-ttu-id="9973a-122">それ以外の場合は、最初に `python3` パッケージをインストールする ([ソースからビルドする](https://github.com/linux-on-ibm-z/docs/wiki/Building-Python-3.6.x)か、[追加のリポジトリ](https://developers.redhat.com/blog/2018/08/13/install-python3-rhel/)を使用してインストールする) 必要があります。</span><span class="sxs-lookup"><span data-stu-id="9973a-122">Otherwise, you need to first install a `python3` package, either [build from source](https://github.com/linux-on-ibm-z/docs/wiki/Building-Python-3.6.x) or install through some [additional repo](https://developers.redhat.com/blog/2018/08/13/install-python3-rhel/).</span></span> <span data-ttu-id="9973a-123">その後、[手動のインストール手順](install-azure-cli-linux.md)に従うことができます。</span><span class="sxs-lookup"><span data-stu-id="9973a-123">Then you can follow the [manual install instructions](install-azure-cli-linux.md).</span></span>

<span data-ttu-id="9973a-124">最も推奨されない選択は、Python 2 を引き続き使用し、[手動インストール](install-azure-cli-linux.md)手順に従うというものです。これは Python 2 が 2020 年 1 月 1 日に終了するためです。</span><span class="sxs-lookup"><span data-stu-id="9973a-124">The least recommended option is to still use Python 2 and follow the [manual install instructions](install-azure-cli-linux.md) since Python 2 is being end-of-lifed on January 1, 2020.</span></span> <span data-ttu-id="9973a-125">Azure CLI の今後のバージョンでは、Python 2.7 のサポートは削除されます。</span><span class="sxs-lookup"><span data-stu-id="9973a-125">A future version of Azure CLI will drop support for Python 2.7.</span></span>

## <a name="update"></a><span data-ttu-id="9973a-126">更新</span><span class="sxs-lookup"><span data-stu-id="9973a-126">Update</span></span>

<span data-ttu-id="9973a-127">`yum update` コマンドで Azure CLI を更新します。</span><span class="sxs-lookup"><span data-stu-id="9973a-127">Update the Azure CLI with the `yum update` command.</span></span>

```bash
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="9973a-128">アンインストール</span><span class="sxs-lookup"><span data-stu-id="9973a-128">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="9973a-129">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="9973a-129">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="9973a-130">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="9973a-130">If you don't plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="9973a-131">他の Microsoft パッケージを使用しない場合は、署名キーを削除します。</span><span class="sxs-lookup"><span data-stu-id="9973a-131">If you don't use any other Microsoft packages, remove the signing key.</span></span>

   ```bash
   MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
   sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
   ```

## <a name="next-steps"></a><span data-ttu-id="9973a-132">次の手順</span><span class="sxs-lookup"><span data-stu-id="9973a-132">Next Steps</span></span>

<span data-ttu-id="9973a-133">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="9973a-133">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="9973a-134">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="9973a-134">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
