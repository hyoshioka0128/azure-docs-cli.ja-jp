---
title: apt を使用して Linux に Azure CLI 2.0 をインストールする
description: apt パッケージ マネージャーで Azure CLI 2.0 をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/24/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: a0908c5b5bda7ec903b702eecb61eabbbedaf533
ms.sourcegitcommit: 64f2c628e83d687d0e172c01f13d71c8c39a8040
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2018
ms.locfileid: "38967845"
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="f9eef-103">apt での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="f9eef-103">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="f9eef-104">Ubuntu や Debian など、`apt` が付属するディストリビューションを実行している場合は、Azure CLI 用の利用可能な 64 ビット パッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="f9eef-104">If you are running a distribution that comes with `apt`, such as Ubuntu or Debian, there is a 64-bit package available for the Azure CLI.</span></span> <span data-ttu-id="f9eef-105">このパッケージは、以下でテストされています。</span><span class="sxs-lookup"><span data-stu-id="f9eef-105">This package has been tested with:</span></span>

* <span data-ttu-id="f9eef-106">Ubuntu trusty、xenial、artful、および bionic</span><span class="sxs-lookup"><span data-stu-id="f9eef-106">Ubuntu trusty, xenial, artful, and bionic</span></span>
* <span data-ttu-id="f9eef-107">Debian wheezy、jessie、および stretch</span><span class="sxs-lookup"><span data-stu-id="f9eef-107">Debian wheezy, jessie, and stretch</span></span>

## <a name="install"></a><span data-ttu-id="f9eef-108">Install</span><span class="sxs-lookup"><span data-stu-id="f9eef-108">Install</span></span>

1. <div id="install-step-1"/><span data-ttu-id="f9eef-109">ソース リストを変更します。</span><span class="sxs-lookup"><span data-stu-id="f9eef-109">Modify your sources list:</span></span>

    ```bash
    AZ_REPO=$(lsb_release -cs)
    echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
    ```

2. <div id="signingKey"/><span data-ttu-id="f9eef-110">Microsoft の署名キーを取得します。</span><span class="sxs-lookup"><span data-stu-id="f9eef-110">Get the Microsoft signing key:</span></span>

   ```bash
   curl -L https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
   ```

3. <span data-ttu-id="f9eef-111">CLI をインストールします。</span><span class="sxs-lookup"><span data-stu-id="f9eef-111">Install the CLI:</span></span>

   ```bash
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

   > [!WARNING]
   > <span data-ttu-id="f9eef-112">署名キーは 2018 年 5 月に更新され、置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="f9eef-112">The signing key was updated in May 2018, and has been replaced.</span></span> <span data-ttu-id="f9eef-113">署名キーのエラーが発生した場合は、[最新の署名キーを取得済み](#signingKey)であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f9eef-113">If you receive signing key errors, please ensure that you have [acquired the latest signing key](#signingKey).</span></span>

<span data-ttu-id="f9eef-114">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="f9eef-114">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="f9eef-115">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f9eef-115">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="f9eef-116">さまざまな認証方法の詳細については、「[Azure CLI 2.0 を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9eef-116">To learn more about different authentication methods, see [Sign in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="f9eef-117">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="f9eef-117">Troubleshooting</span></span>

<span data-ttu-id="f9eef-118">ここでは、`apt` でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="f9eef-118">Here are some common problems seen when installing with `apt`.</span></span> <span data-ttu-id="f9eef-119">問題がここに示されていない場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="f9eef-119">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="lsbrelease-fails-with-command-not-found"></a><span data-ttu-id="f9eef-120">"コマンドが見つかりません" が発生して lsb_release が失敗する</span><span class="sxs-lookup"><span data-stu-id="f9eef-120">lsb_release fails with "Command not found"</span></span>

<span data-ttu-id="f9eef-121">`lsb_release` コマンドの実行時に、次のようなエラーが出力されることがあります。</span><span class="sxs-lookup"><span data-stu-id="f9eef-121">When running the `lsb_release` command, you may see output similar to the following error:</span></span>

```output
-bash: lsb_release: command not found
```

<span data-ttu-id="f9eef-122">このエラーは、lsb_release がインストールされていないことが原因です。</span><span class="sxs-lookup"><span data-stu-id="f9eef-122">The error is due to lsb_release not being installed.</span></span> <span data-ttu-id="f9eef-123">これを解決するには、`lsb-release` パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="f9eef-123">You can resolve it by installing the `lsb-release` package.</span></span>

```bash
sudo apt-get install lsb-release
```

### <a name="lsbrelease-does-not-return-the-base-distribution-version"></a><span data-ttu-id="f9eef-124">lsb_release では、ベース ディストリビューション バージョンが返されません</span><span class="sxs-lookup"><span data-stu-id="f9eef-124">lsb_release does not return the base distribution version</span></span>

<span data-ttu-id="f9eef-125">Linux Mint など、Ubuntu や Debian から派生する一部のディストリビューションでは、正しいバージョン名が `lsb_release` から返されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="f9eef-125">Some Ubuntu- or Debian-derived distributions such as Linux Mint may not return the correct version name from `lsb_release`.</span></span> <span data-ttu-id="f9eef-126">この値は、インストール プロセスで、インストールするパッケージを特定するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="f9eef-126">This value is used in the install process to determine the package to install.</span></span> <span data-ttu-id="f9eef-127">ディストリビューションの派生元バージョンの名前がわかっている場合は、[インストール手順 1.](#install-step-1) で `AZ_REPO` 値を手動で設定できます。</span><span class="sxs-lookup"><span data-stu-id="f9eef-127">If you know the name of the version your distribution is derived from, you can set the `AZ_REPO` value manually in [install step 1](#install-step-1).</span></span> <span data-ttu-id="f9eef-128">それ以外の場合は、ご自身のディストリビューションについて、ベース ディストリビューション名を調べて、`AZ_REPO` を正しい値に設定する方法をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="f9eef-128">Otherwise, look up information for your distribution on how to determine the base distribution name and set `AZ_REPO` to the correct value.</span></span>

### <a name="apt-key-fails-with-no-dirmngr"></a><span data-ttu-id="f9eef-129">"No dirmngr" で apt-key が失敗する</span><span class="sxs-lookup"><span data-stu-id="f9eef-129">apt-key fails with "No dirmngr"</span></span>

<span data-ttu-id="f9eef-130">`apt-key` コマンドの実行時に、次のようなエラーが出力されることがあります。</span><span class="sxs-lookup"><span data-stu-id="f9eef-130">When running the `apt-key` command, you may see output similar to the following error:</span></span>

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

<span data-ttu-id="f9eef-131">このエラーは、`apt-key` に必要なコンポーネントがないためです。</span><span class="sxs-lookup"><span data-stu-id="f9eef-131">The error is due to a missing component required by `apt-key`.</span></span> <span data-ttu-id="f9eef-132">これを解決するには、`dirmngr` パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="f9eef-132">You can resolve it by installing the `dirmngr` package.</span></span>

```bash
sudo apt-get install dirmngr
```

### <a name="apt-key-hangs"></a><span data-ttu-id="f9eef-133">apt-key がハングする</span><span class="sxs-lookup"><span data-stu-id="f9eef-133">apt-key hangs</span></span>

<span data-ttu-id="f9eef-134">ファイアウォールの内側でポート 11371 への発信接続がブロックされている場合、`apt-key` コマンドが無期限にハングすることがあります。</span><span class="sxs-lookup"><span data-stu-id="f9eef-134">When behind a firewall blocking outgoing connections to port 11371, the `apt-key` command might hang indefinitely.</span></span> <span data-ttu-id="f9eef-135">発信接続用にファイアウォールで HTTP プロキシを使用する必要がある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f9eef-135">Your firewall may require the use of an HTTP proxy for outgoing connections:</span></span>

```bash
sudo apt-key adv --keyserver-options http-proxy=http://<USER>:<PASSWORD>@<PROXY-HOST>:<PROXY-PORT>/ --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
```

<span data-ttu-id="f9eef-136">プロキシがあるかどうかがわからない場合は、システム管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="f9eef-136">If you do not know if you have a proxy, contact your system administrator.</span></span> <span data-ttu-id="f9eef-137">プロキシでログインを必要としない場合は、ユーザー、パスワード、および `@` トークンを指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="f9eef-137">If your proxy does not require a login then leave out the user, password, and `@` token.</span></span>

## <a name="update"></a><span data-ttu-id="f9eef-138">アップデート</span><span class="sxs-lookup"><span data-stu-id="f9eef-138">Update</span></span>

<span data-ttu-id="f9eef-139">CLI パッケージを更新するには、`apt-get upgrade` を使用します。</span><span class="sxs-lookup"><span data-stu-id="f9eef-139">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!WARNING]
> <span data-ttu-id="f9eef-140">署名キーは 2018 年 5 月に更新され、置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="f9eef-140">The signing key was updated in May 2018, and has been replaced.</span></span> <span data-ttu-id="f9eef-141">署名キーのエラーが発生した場合は、[最新の署名キーを取得済み](#signingKey)であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f9eef-141">If you receive signing key errors, please ensure that you have [acquired the latest signing key](#signingKey).</span></span>
>
> [!NOTE]
> <span data-ttu-id="f9eef-142">このコマンドにより、システムにインストールされている、依存関係が変更されていないすべてのパッケージがアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="f9eef-142">This command upgrades all of the installed packages on your system that have not had a dependency change.</span></span>
> <span data-ttu-id="f9eef-143">CLI だけをアップグレードするには、`apt-get install` を使用します。</span><span class="sxs-lookup"><span data-stu-id="f9eef-143">To upgrade the CLI only, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a><span data-ttu-id="f9eef-144">アンインストール</span><span class="sxs-lookup"><span data-stu-id="f9eef-144">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="f9eef-145">`apt-get remove` を使用してアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="f9eef-145">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="f9eef-146">CLI を再インストールする予定がない場合は、Azure CLI リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="f9eef-146">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="f9eef-147">不要なパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="f9eef-147">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
