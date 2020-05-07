---
title: apt を使用して Linux に Azure CLI をインストールする
description: apt パッケージ マネージャーで Azure CLI をインストールする方法
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 10/14/2019
ms.topic: conceptual
ms.service: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 302b98717ee422de9bd60a57b18d900bcf5fcaf9
ms.sourcegitcommit: ee64dc738cfe689a2a479e32a87bf420f96c31c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2020
ms.locfileid: "80417928"
---
# <a name="install-azure-cli-with-apt"></a><span data-ttu-id="45c89-103">apt での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="45c89-103">Install Azure CLI with apt</span></span>

<span data-ttu-id="45c89-104">Ubuntu や Debian など、`apt` が付属するディストリビューションを実行している場合は、Azure CLI 用に x86_64 パッケージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="45c89-104">If you are running a distribution that comes with `apt`, such as Ubuntu or Debian, there's an x86_64 package available for the Azure CLI.</span></span> <span data-ttu-id="45c89-105">このパッケージは、以下でテストされ、サポートされています。</span><span class="sxs-lookup"><span data-stu-id="45c89-105">This package has been tested with and is supported for:</span></span>

* <span data-ttu-id="45c89-106">Ubuntu trusty、xenial、artful、bionic、および disco</span><span class="sxs-lookup"><span data-stu-id="45c89-106">Ubuntu trusty, xenial, artful, bionic, and disco</span></span>
* <span data-ttu-id="45c89-107">Debian wheezy、jessie、stretch、および buster</span><span class="sxs-lookup"><span data-stu-id="45c89-107">Debian wheezy, jessie, stretch, and buster</span></span>

[!INCLUDE [current-version](includes/current-version.md)]

> [!NOTE]
>
> <span data-ttu-id="45c89-108">Azure CLI のパッケージによって独自の Python インタープリターがインストールされ、システム上の Python は使用されません。</span><span class="sxs-lookup"><span data-stu-id="45c89-108">The package for Azure CLI installs its own Python interpreter, and does not use the system Python.</span></span>

## <a name="install"></a><span data-ttu-id="45c89-109">インストール</span><span class="sxs-lookup"><span data-stu-id="45c89-109">Install</span></span>

<span data-ttu-id="45c89-110">`apt` をサポートするディストリビューションで Azure CLI をインストールするために、次の 2 つの方法が提供されています。ユーザーに代わってコマンドを実行してインストールするオールインワンのスクリプトと、ユーザーが段階的なプロセスを自分で実行できる手順です。</span><span class="sxs-lookup"><span data-stu-id="45c89-110">We offer two ways to install the Azure CLI with distributions that support `apt`: As an all-in-one script that runs the install commands for you, and instructions that you can run as a step-by-step process on your own.</span></span>

### <a name="install-with-one-command"></a><span data-ttu-id="45c89-111">1 つのコマンドでインストールする</span><span class="sxs-lookup"><span data-stu-id="45c89-111">Install with one command</span></span>

<span data-ttu-id="45c89-112">1 つの手順ですべてのインストール コマンドを実行するスクリプトを提供および保守しています。</span><span class="sxs-lookup"><span data-stu-id="45c89-112">We offer and maintain a script which runs all of the installation commands in one step.</span></span> <span data-ttu-id="45c89-113">`curl` を使用してコマンドを実行し、`bash` に直接パイプするか、ファイルにスクリプトをダウンロードして実行前に検査します。</span><span class="sxs-lookup"><span data-stu-id="45c89-113">Run it by using `curl` and pipe directly to `bash`, or download the script to a file and inspect it before running.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45c89-114">このスクリプトは、Ubuntu 16.04 以降および Debian 8 以降でのみ検証されています。</span><span class="sxs-lookup"><span data-stu-id="45c89-114">This script is only verified for Ubuntu 16.04+ and Debian 8+.</span></span> <span data-ttu-id="45c89-115">他のディストリビューションでは機能しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="45c89-115">It may not work on other distributions.</span></span>
> <span data-ttu-id="45c89-116">Linux Mint などの派生ディストリビューションを使用している場合は、手動のインストール手順に従い、必要なトラブルシューティングを実行します。</span><span class="sxs-lookup"><span data-stu-id="45c89-116">If you're using a derived distribution such as Linux Mint, follow the manual install instructions and perform any necessary troubleshooting.</span></span>

```bash
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
```

### <a name="manual-install-instructions"></a><span data-ttu-id="45c89-117">手動のインストール手順</span><span class="sxs-lookup"><span data-stu-id="45c89-117">Manual install instructions</span></span>

<span data-ttu-id="45c89-118">スーパーユーザーとしてスクリプトを実行しない場合またはオールインワン スクリプトが失敗する場合は、次の手順に従って Azure CLI をインストールします。</span><span class="sxs-lookup"><span data-stu-id="45c89-118">If you don't want to run a script as superuser or the all-in-one script fails, follow these steps to install the Azure CLI.</span></span>

1. <span data-ttu-id="45c89-119">インストール プロセスに必要なパッケージを取得します。</span><span class="sxs-lookup"><span data-stu-id="45c89-119">Get packages needed for the install process:</span></span>

    ```bash
    sudo apt-get update
    sudo apt-get install ca-certificates curl apt-transport-https lsb-release gnupg
    ```

2. <span data-ttu-id="45c89-120">Microsoft の署名キーをダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="45c89-120">Download and install the Microsoft signing key:</span></span>

    ```bash
    curl -sL https://packages.microsoft.com/keys/microsoft.asc |
        gpg --dearmor |
        sudo tee /etc/apt/trusted.gpg.d/microsoft.asc.gpg > /dev/null
    ```

3. <div id="set-release"/><span data-ttu-id="45c89-121">Azure CLI  ソフトウェア リポジトリを追加します。</span><span class="sxs-lookup"><span data-stu-id="45c89-121">Add the Azure CLI software repository:</span></span>

    ```bash
    AZ_REPO=$(lsb_release -cs)
    echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" |
        sudo tee /etc/apt/sources.list.d/azure-cli.list
    ```

4. <span data-ttu-id="45c89-122">リポジトリ情報を更新し、`azure-cli` パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="45c89-122">Update repository information and install the `azure-cli` package:</span></span>

    ```bash
    sudo apt-get update
    sudo apt-get install azure-cli
    ```

<span data-ttu-id="45c89-123">`az` コマンドで Azure CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="45c89-123">Run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="45c89-124">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="45c89-124">To sign in, use the [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="45c89-125">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45c89-125">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="45c89-126">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="45c89-126">Troubleshooting</span></span>

<span data-ttu-id="45c89-127">ここでは、`apt` でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="45c89-127">Here are some common problems seen when installing with `apt`.</span></span> <span data-ttu-id="45c89-128">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="45c89-128">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="lsb_release-does-not-return-the-correct-base-distribution-version"></a><span data-ttu-id="45c89-129">lsb_release がベース ディストリビューション バージョンを返さない</span><span class="sxs-lookup"><span data-stu-id="45c89-129">lsb_release does not return the correct base distribution version</span></span>

<span data-ttu-id="45c89-130">Linux Mint など、Ubuntu や Debian から派生する一部のディストリビューションでは、正しいバージョン名が `lsb_release` から返されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="45c89-130">Some Ubuntu- or Debian-derived distributions such as Linux Mint may not return the correct version name from `lsb_release`.</span></span> <span data-ttu-id="45c89-131">この値は、インストール プロセスで、インストールするパッケージを特定するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="45c89-131">This value is used in the install process to determine the package to install.</span></span> <span data-ttu-id="45c89-132">ディストリビューションの派生元である Ubuntu バージョンまたは Debian バージョンのコード名がわかっている場合は、[リポジトリを追加する](#set-release)ときに `AZ_REPO` 値を手動で設定できます。</span><span class="sxs-lookup"><span data-stu-id="45c89-132">If you know the code name of the Ubuntu or Debian version your distribution is derived from, you can set the `AZ_REPO` value manually when [adding the repository](#set-release).</span></span> <span data-ttu-id="45c89-133">それ以外の場合は、ご自身のディストリビューションについて、ベース ディストリビューションのコード名を調べて、`AZ_REPO` を正しい値に設定する方法をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="45c89-133">Otherwise, look up information for your distribution on how to determine the base distribution code name and set `AZ_REPO` to the correct value.</span></span>

### <a name="no-package-for-your-distribution"></a><span data-ttu-id="45c89-134">ご使用のディストリビューションのパッケージがない</span><span class="sxs-lookup"><span data-stu-id="45c89-134">No package for your distribution</span></span>

<span data-ttu-id="45c89-135">ディストリビューションがリリースされてから、そのディストリビューション用の Azure CLI パッケージが利用可能になるまではしばらくかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="45c89-135">Sometimes it may be a while after a distribution is released before there's an Azure CLI package available for it.</span></span> <span data-ttu-id="45c89-136">Azure CLI は、以降のバージョンの依存関係に関して弾力性を持つように、また可能な限り以降のバージョンに依存しないように設計されています。</span><span class="sxs-lookup"><span data-stu-id="45c89-136">The Azure CLI designed to be resilient with regards to future versions of dependencies and rely on as few of them as possible.</span></span> <span data-ttu-id="45c89-137">ベース ディストリビューションに使用できるパッケージがない場合は、以前のディストリビューション用のパッケージをお試しください。</span><span class="sxs-lookup"><span data-stu-id="45c89-137">If there's no package available for your base distribution, try a package for an earlier distribution.</span></span>

<span data-ttu-id="45c89-138">これを行うには、[リポジトリを追加する](#set-release)ときに `AZ_REPO` の値を手動で設定します。</span><span class="sxs-lookup"><span data-stu-id="45c89-138">To do this, set the value of `AZ_REPO` manually when [adding the repository](#set-release).</span></span> <span data-ttu-id="45c89-139">Ubuntu ディストリビューションには `bionic` リポジトリーを使用し、Debian ディストリビューションには `stretch` を使用します。</span><span class="sxs-lookup"><span data-stu-id="45c89-139">For Ubuntu distributions use the `bionic` repository, and for Debian distributions use `stretch`.</span></span> <span data-ttu-id="45c89-140">Ubuntu Trusty および Debian Wheezy より前にリリースされたディストリビューションはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="45c89-140">Distributions released before Ubuntu Trusty and Debian Wheezy are not supported.</span></span>

### <a name="elementary-os-eos-fails-to-install-the-azure-cli"></a><span data-ttu-id="45c89-141">elementary OS (EOS) で Azure CLI のインストールが失敗する</span><span class="sxs-lookup"><span data-stu-id="45c89-141">Elementary OS (EOS) fails to install the Azure CLI</span></span>

<span data-ttu-id="45c89-142">`lsb_release` によって `HERA` (EOS リリース名) が返されるため、EOS で Azure CLI のインストールが失敗します。</span><span class="sxs-lookup"><span data-stu-id="45c89-142">EOS fails to install the Azure cli because `lsb_release` returns `HERA`, which is the EOS release name.</span></span>  <span data-ttu-id="45c89-143">解決策は、ファイル `/etc/apt/sources.list.d/azure-cli.list` を修正して、`hera main` を `bionic main` に変更することです。</span><span class="sxs-lookup"><span data-stu-id="45c89-143">The solution is to fix the file `/etc/apt/sources.list.d/azure-cli.list` and change `hera main` to `bionic main`.</span></span>

<span data-ttu-id="45c89-144">元のファイルの内容:</span><span class="sxs-lookup"><span data-stu-id="45c89-144">Original file contents:</span></span>

```
deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ hera main
```

<span data-ttu-id="45c89-145">修正したファイルの内容</span><span class="sxs-lookup"><span data-stu-id="45c89-145">Modified file contents</span></span>

```
deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ bionic main
```

### <a name="proxy-blocks-connection"></a><span data-ttu-id="45c89-146">プロキシによる接続のブロック</span><span class="sxs-lookup"><span data-stu-id="45c89-146">Proxy blocks connection</span></span>

[!INCLUDE[configure-proxy](includes/configure-proxy.md)]

<span data-ttu-id="45c89-147">常にこのプロキシを使用するように `apt` を明示的に構成することが必要な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="45c89-147">You may also want to explicitly configure `apt` to use this proxy at all times.</span></span> <span data-ttu-id="45c89-148">次の行が `/etc/apt/apt.conf.d/` の `apt` 構成ファイルに表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="45c89-148">Make sure that the following lines appear in an `apt` configuration file in `/etc/apt/apt.conf.d/`.</span></span> <span data-ttu-id="45c89-149">既存のグローバル構成ファイル、既存のプロキシ構成ファイル、`40proxies`、または `99local` を使用することをお勧めしますが、システム管理の要件に従ってください。</span><span class="sxs-lookup"><span data-stu-id="45c89-149">We recommend using either your existing global configuration file, an existing proxy configuration file, `40proxies`, or `99local`, but follow your system administration requirements.</span></span>

```apt.conf
Acquire {
    http::proxy "http://[username]:[password]@[proxy]:[port]";
    https::proxy "https://[username]:[password]@[proxy]:[port]";
}
```

<span data-ttu-id="45c89-150">プロキシで基本認証を使用しない場合、プロキシ URL の `[username]:[password]@` ポーションを__削除__します。</span><span class="sxs-lookup"><span data-stu-id="45c89-150">If your proxy does not use basic auth, __remove__ the `[username]:[password]@` portion of the proxy URI.</span></span> <span data-ttu-id="45c89-151">プロキシ構成について詳しくは、Ubuntu の公式ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="45c89-151">If you require more information for proxy configuration, see the official Ubuntu documentation:</span></span>

* [<span data-ttu-id="45c89-152">apt.conf マニュアル ページ</span><span class="sxs-lookup"><span data-stu-id="45c89-152">apt.conf manpage</span></span>](http://manpages.ubuntu.com/manpages/bionic/en/man5/apt.conf.5.html)
* [<span data-ttu-id="45c89-153">Ubuntu wiki - apt-get ハウツー</span><span class="sxs-lookup"><span data-stu-id="45c89-153">Ubuntu wiki - apt-get howto</span></span>](https://help.ubuntu.com/community/AptGet/Howto#Setting_up_apt-get_to_use_a_http-proxy)

<span data-ttu-id="45c89-154">Microsoft 署名キーを取得し、リポジトリからパッケージを取得するには、お使いのプロキシで次のアドレスへの HTTPS 接続を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45c89-154">In order to get the Microsoft signing key and get the package from our repository, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://packages.microsoft.com`

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]

## <a name="update"></a><span data-ttu-id="45c89-155">更新</span><span class="sxs-lookup"><span data-stu-id="45c89-155">Update</span></span>

<span data-ttu-id="45c89-156">CLI パッケージを更新するには、`apt-get upgrade` を使用します。</span><span class="sxs-lookup"><span data-stu-id="45c89-156">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="45c89-157">このコマンドにより、システムにインストールされている、依存関係が変更されていないすべてのパッケージがアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="45c89-157">This command upgrades all of the installed packages on your system that have not had a dependency change.</span></span>
> <span data-ttu-id="45c89-158">CLI だけをアップグレードするには、`apt-get install` を使用します。</span><span class="sxs-lookup"><span data-stu-id="45c89-158">To upgrade the CLI only, use `apt-get install`.</span></span>
>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a><span data-ttu-id="45c89-159">アンインストール</span><span class="sxs-lookup"><span data-stu-id="45c89-159">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="45c89-160">`apt-get remove` を使用してアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="45c89-160">Uninstall with `apt-get remove`:</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="45c89-161">CLI を再インストールする予定がない場合は、Azure CLI リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="45c89-161">If you don't plan to reinstall the CLI, remove the Azure CLI repository information:</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="45c89-162">Microsoft の他のパッケージを使用しない場合は、署名キーを削除します。</span><span class="sxs-lookup"><span data-stu-id="45c89-162">If you use no other packages from Microsoft, remove the signing key:</span></span>

    ```bash
    sudo rm /etc/apt/trusted.gpg.d/microsoft.asc.gpg
    ```

4. <span data-ttu-id="45c89-163">不要なパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="45c89-163">Remove any unneeded packages:</span></span>

   ```bash
   sudo apt autoremove
   ```

## <a name="next-steps"></a><span data-ttu-id="45c89-164">次の手順</span><span class="sxs-lookup"><span data-stu-id="45c89-164">Next Steps</span></span>

<span data-ttu-id="45c89-165">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="45c89-165">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="45c89-166">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="45c89-166">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
