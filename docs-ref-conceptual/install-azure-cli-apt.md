---
title: apt を使用して Linux に Azure CLI をインストールする
description: apt パッケージ マネージャーで Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 11/27/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 45e1e7468e5817d0138c9b87da83c5a5228e4965
ms.sourcegitcommit: 1987a39809f9865034b27130e56f30b2bd1eb72c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2019
ms.locfileid: "56421934"
---
# <a name="install-azure-cli-with-apt"></a><span data-ttu-id="96d4f-103">apt での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="96d4f-103">Install Azure CLI with apt</span></span>

<span data-ttu-id="96d4f-104">Ubuntu や Debian など、`apt` が付属するディストリビューションを実行している場合は、Azure CLI 用に 64 ビット パッケージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="96d4f-104">If you are running a distribution that comes with `apt`, such as Ubuntu or Debian, there's a 64-bit package available for the Azure CLI.</span></span> <span data-ttu-id="96d4f-105">このパッケージは、以下でテストされています。</span><span class="sxs-lookup"><span data-stu-id="96d4f-105">This package has been tested with:</span></span>

* <span data-ttu-id="96d4f-106">Ubuntu trusty、xenial、artful、および bionic</span><span class="sxs-lookup"><span data-stu-id="96d4f-106">Ubuntu trusty, xenial, artful, and bionic</span></span>
* <span data-ttu-id="96d4f-107">Debian wheezy、jessie、および stretch</span><span class="sxs-lookup"><span data-stu-id="96d4f-107">Debian wheezy, jessie, and stretch</span></span>

[!INCLUDE [current-version](includes/current-version.md)]

> [!NOTE]
>
> <span data-ttu-id="96d4f-108">Azure CLI の `.deb` パッケージによって独自の Python インタープリターがインストールされ、システム上の Python は使用されないため、ローカルの Python バージョンには明示的な要件はありません。</span><span class="sxs-lookup"><span data-stu-id="96d4f-108">The `.deb` package for Azure CLI installs its own Python interpreter, and does not use the system Python, so there is no explicit requirement for a local Python version.</span></span>

## <a name="install"></a><span data-ttu-id="96d4f-109">Install</span><span class="sxs-lookup"><span data-stu-id="96d4f-109">Install</span></span>

1. <span data-ttu-id="96d4f-110">前提条件となるパッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="96d4f-110">Install prerequisite packages:</span></span>

    ```bash
    sudo apt-get install apt-transport-https lsb-release software-properties-common dirmngr -y
    ```

2. <div id="set-release"/><span data-ttu-id="96d4f-111">ソース リストを変更します。</span><span class="sxs-lookup"><span data-stu-id="96d4f-111">Modify your sources list:</span></span>

    ```bash
    AZ_REPO=$(lsb_release -cs)
    echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
    ```

3. <div id="signingKey"/><span data-ttu-id="96d4f-112">Microsoft の署名キーを取得します。</span><span class="sxs-lookup"><span data-stu-id="96d4f-112">Get the Microsoft signing key:</span></span>

   ```bash
   sudo apt-key --keyring /etc/apt/trusted.gpg.d/Microsoft.gpg adv \
        --keyserver packages.microsoft.com \
        --recv-keys BC528686B50D79E339D3721CEB3E94ADBE1229CF
   ```

4. <span data-ttu-id="96d4f-113">CLI をインストールします。</span><span class="sxs-lookup"><span data-stu-id="96d4f-113">Install the CLI:</span></span>

   ```bash
   sudo apt-get update
   sudo apt-get install azure-cli
   ```

   > [!WARNING]
   > <span data-ttu-id="96d4f-114">署名キーは 2018 年 5 月に更新され、置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="96d4f-114">The signing key was updated in May 2018, and has been replaced.</span></span> <span data-ttu-id="96d4f-115">署名のエラーが発生した場合は、[最新の署名キー](#signingKey)を使用していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="96d4f-115">If you receive signing errors, make sure you have [the latest signing key](#signingKey).</span></span>

<span data-ttu-id="96d4f-116">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="96d4f-116">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="96d4f-117">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="96d4f-117">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="96d4f-118">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96d4f-118">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="96d4f-119">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="96d4f-119">Troubleshooting</span></span>

<span data-ttu-id="96d4f-120">ここでは、`apt` でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="96d4f-120">Here are some common problems seen when installing with `apt`.</span></span> <span data-ttu-id="96d4f-121">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="96d4f-121">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="lsbrelease-does-not-return-the-correct-base-distribution-version"></a><span data-ttu-id="96d4f-122">lsb_release がベース ディストリビューション バージョンを返さない</span><span class="sxs-lookup"><span data-stu-id="96d4f-122">lsb_release does not return the correct base distribution version</span></span>

<span data-ttu-id="96d4f-123">Linux Mint など、Ubuntu や Debian から派生する一部のディストリビューションでは、正しいバージョン名が `lsb_release` から返されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="96d4f-123">Some Ubuntu- or Debian-derived distributions such as Linux Mint may not return the correct version name from `lsb_release`.</span></span> <span data-ttu-id="96d4f-124">この値は、インストール プロセスで、インストールするパッケージを特定するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="96d4f-124">This value is used in the install process to determine the package to install.</span></span> <span data-ttu-id="96d4f-125">ディストリビューションの派生元バージョンの名前がわかっている場合は、[インストール手順 2.](#set-release) で `AZ_REPO` 値を手動で設定できます。</span><span class="sxs-lookup"><span data-stu-id="96d4f-125">If you know the name of the version your distribution is derived from, you can set the `AZ_REPO` value manually in [install step 2](#set-release).</span></span> <span data-ttu-id="96d4f-126">それ以外の場合は、ご自身のディストリビューションについて、ベース ディストリビューション名を調べて、`AZ_REPO` を正しい値に設定する方法をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="96d4f-126">Otherwise, look up information for your distribution on how to determine the base distribution name and set `AZ_REPO` to the correct value.</span></span>

### <a name="no-package-for-your-distribution"></a><span data-ttu-id="96d4f-127">ご使用のディストリビューションのパッケージがない</span><span class="sxs-lookup"><span data-stu-id="96d4f-127">No package for your distribution</span></span>

<span data-ttu-id="96d4f-128">Ubuntu ディストリビューションがリリースされてから、そのディストリビューション用の Azure CLI パッケージが利用可能になるまではしばらくかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="96d4f-128">Sometimes it may be a while after an Ubuntu distribution is released before there's an Azure CLI package made available for it.</span></span> <span data-ttu-id="96d4f-129">Azure CLI は、以降のバージョンの依存関係に関して弾力性を持つように、また可能な限り以降のバージョンに依存しないように設計されています。</span><span class="sxs-lookup"><span data-stu-id="96d4f-129">The Azure CLI designed to be resilient with regards to future versions of dependencies and rely on as few of them as possible.</span></span> <span data-ttu-id="96d4f-130">ベース ディストリビューションに使用できるパッケージがない場合は、以前のディストリビューション用のパッケージをお試しください。</span><span class="sxs-lookup"><span data-stu-id="96d4f-130">If there's no package available for your base distribution, try a package for an earlier distribution.</span></span>

<span data-ttu-id="96d4f-131">これを行うには、[インストール手順 1.](#install-step-1) で、`AZ_REPO` の値を手動で設定します。</span><span class="sxs-lookup"><span data-stu-id="96d4f-131">To do this, set the value of `AZ_REPO` manually in [install step 1](#install-step-1).</span></span> <span data-ttu-id="96d4f-132">Ubuntu ディストリビューションには `bionic` リポジトリーを使用し、Debian ディストリビューションには `stretch` を使用します。</span><span class="sxs-lookup"><span data-stu-id="96d4f-132">For Ubuntu distributions use the `bionic` repository, and for Debian distributions use `stretch`.</span></span> <span data-ttu-id="96d4f-133">Ubuntu Trusty および Debian Wheezy より前にリリースされたディストリビューションはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="96d4f-133">Distributions released before Ubuntu Trusty and Debian Wheezy are not supported.</span></span>

### <a name="apt-key-fails-with-no-dirmngr"></a><span data-ttu-id="96d4f-134">"No dirmngr" で apt-key が失敗する</span><span class="sxs-lookup"><span data-stu-id="96d4f-134">apt-key fails with "No dirmngr"</span></span>

<span data-ttu-id="96d4f-135">`apt-key` コマンドの実行時に、次のようなエラーが出力されることがあります。</span><span class="sxs-lookup"><span data-stu-id="96d4f-135">When running the `apt-key` command, you may see output similar to the following error:</span></span>

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

<span data-ttu-id="96d4f-136">このエラーは、`apt-key` に必要なコンポーネントがないためです。</span><span class="sxs-lookup"><span data-stu-id="96d4f-136">The error is due to a missing component required by `apt-key`.</span></span> <span data-ttu-id="96d4f-137">これを解決するには、`dirmngr` パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="96d4f-137">You can resolve it by installing the `dirmngr` package.</span></span>

```bash
sudo apt-get install dirmngr
```

<span data-ttu-id="96d4f-138">Windows Subsystem for Linux (WSL) の場合は、このエラーは Windows 10 1809 よりも前のバージョンの Windows にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="96d4f-138">If you are on Windows Subsystem for Linux (WSL), this error also appears on versions of Windows prior to Windows 10 1809.</span></span> <span data-ttu-id="96d4f-139">問題を解決するには、Windows のバージョンを更新します。</span><span class="sxs-lookup"><span data-stu-id="96d4f-139">To resolve the issue, update your version of Windows.</span></span>

### <a name="apt-key-hangs"></a><span data-ttu-id="96d4f-140">apt-key がハングする</span><span class="sxs-lookup"><span data-stu-id="96d4f-140">apt-key hangs</span></span>

<span data-ttu-id="96d4f-141">ファイアウォールの内側でポート 11371 への発信接続がブロックされている場合、`apt-key` コマンドが無期限にハングすることがあります。</span><span class="sxs-lookup"><span data-stu-id="96d4f-141">When behind a firewall blocking outgoing connections to port 11371, the `apt-key` command might hang indefinitely.</span></span>
<span data-ttu-id="96d4f-142">ご使用のファイアウォールでは、発信接続用に HTTP プロキシが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="96d4f-142">Your firewall may require an HTTP proxy for outgoing connections:</span></span>

```bash
sudo apt-key --keyring /etc/apt/trusted.gpg.d/Microsoft.gpg adv \
    --keyserver-options http-proxy=http://<USER>:<PASSWORD>@<PROXY-HOST>:<PROXY-PORT>/ \
    --keyserver packages.microsoft.com \
    --recv-keys BC528686B50D79E339D3721CEB3E94ADBE1229CF
```

<span data-ttu-id="96d4f-143">プロキシがあるかどうかを確認するには、システム管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="96d4f-143">To determine if you have a proxy, contact your system administrator.</span></span> <span data-ttu-id="96d4f-144">プロキシでログインが不要な場合は、ユーザーとパスワードの情報を指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="96d4f-144">If your proxy does not require a login, then leave out the user and password information.</span></span>

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]

## <a name="update"></a><span data-ttu-id="96d4f-145">アップデート</span><span class="sxs-lookup"><span data-stu-id="96d4f-145">Update</span></span>

<span data-ttu-id="96d4f-146">CLI パッケージを更新するには、`apt-get upgrade` を使用します。</span><span class="sxs-lookup"><span data-stu-id="96d4f-146">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!WARNING]
> <span data-ttu-id="96d4f-147">署名キーは 2018 年 5 月に更新され、置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="96d4f-147">The signing key was updated in May 2018, and has been replaced.</span></span> <span data-ttu-id="96d4f-148">署名のエラーが発生した場合は、[最新の署名キー](#signingKey)を使用していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="96d4f-148">If you receive signing errors, make sure you have [the latest signing key](#signingKey).</span></span>
>
> [!NOTE]
> <span data-ttu-id="96d4f-149">このコマンドにより、システムにインストールされている、依存関係が変更されていないすべてのパッケージがアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="96d4f-149">This command upgrades all of the installed packages on your system that have not had a dependency change.</span></span>
> <span data-ttu-id="96d4f-150">CLI だけをアップグレードするには、`apt-get install` を使用します。</span><span class="sxs-lookup"><span data-stu-id="96d4f-150">To upgrade the CLI only, use `apt-get install`.</span></span>
> 
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a><span data-ttu-id="96d4f-151">アンインストール</span><span class="sxs-lookup"><span data-stu-id="96d4f-151">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="96d4f-152">`apt-get remove` を使用してアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="96d4f-152">Uninstall with `apt-get remove`:</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="96d4f-153">CLI を再インストールする予定がない場合は、Azure CLI リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="96d4f-153">If you don't plan to reinstall the CLI, remove the Azure CLI repository information:</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="96d4f-154">署名キーを削除します。</span><span class="sxs-lookup"><span data-stu-id="96d4f-154">Remove the signing key:</span></span>

    ```bash
    sudo rm /etc/apt/trusted.gpg.d/Microsoft.gpg
    ```

4. <span data-ttu-id="96d4f-155">不要なパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="96d4f-155">Remove any unneeded packages:</span></span>

   ```bash
   sudo apt autoremove
   ```

## <a name="next-steps"></a><span data-ttu-id="96d4f-156">次の手順</span><span class="sxs-lookup"><span data-stu-id="96d4f-156">Next Steps</span></span>

<span data-ttu-id="96d4f-157">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="96d4f-157">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="96d4f-158">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="96d4f-158">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
