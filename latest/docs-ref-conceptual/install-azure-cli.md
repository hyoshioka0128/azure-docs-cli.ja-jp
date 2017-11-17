---
title: "Azure CLI 2.0 のインストール"
description: "Azure CLI 2.0 のインストールに関するリファレンス ドキュメント"
keywords: "Azure CLI, Azure CLI のインストール, Azure Python CLI, Azure CLI のリファレンス"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 11/01/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 2b56382355cad5313a604ed1f493a2bcbebf3e27
ms.sourcegitcommit: e9b4c6dd9093980b69ca47f93f44ac54d0e5b68a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="9ece0-104">Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="9ece0-105">今すぐ Azure CLI の新しいバージョンをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="9ece0-106">Azure のリソース管理を目的とした優れたネイティブ コマンド ライン エクスペリエンスを実現するために強化して更新しました。</span><span class="sxs-lookup"><span data-stu-id="9ece0-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="9ece0-107">macOS、Linux、および Windows で使用できます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="9ece0-108">最新リリースについては、[リリース ノート](release-notes-azure-cli.md)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="9ece0-109">Azure CLI の以前のバージョンが必要な場合は、[Azure CLI 1.0 をインストールする](/azure/cli-install-nodejs)方法に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-109">If you need the previous version of the Azure CLI, here's how to [install Azure CLI 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="a-namemacosinstall-on-macos"></a><span data-ttu-id="9ece0-110"><a name="macOS"/>macOS へのインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-110"><a name="macOS"/>Install on macOS</span></span>

<span data-ttu-id="9ece0-111">macOS では、[Homebrew](https://brew.sh/) または手動でインストールを行えます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-111">On macOS, you are able to install either with [Homebrew](https://brew.sh/) or manually.</span></span>

### <a name="install-with-homebrew"></a><span data-ttu-id="9ece0-112">Homebrew でインストールする</span><span class="sxs-lookup"><span data-stu-id="9ece0-112">Install with Homebrew</span></span>

1. <span data-ttu-id="9ece0-113">まだお持ちでない場合は、[Homebrew のインストール手順](https://docs.brew.sh/Installation.html)に従って Homebrew をインストールします。</span><span class="sxs-lookup"><span data-stu-id="9ece0-113">If you don't have it already, install Homebrew by following the [Homebrew installation instructions](https://docs.brew.sh/Installation.html).</span></span>

2. <span data-ttu-id="9ece0-114">以前に手動で CLI をインストール済みの場合は、[手動によるアンインストール](#UninstallManually)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9ece0-114">If you have previously installed the CLI manually, follow the [manual uninstall](#UninstallManually) instructions.</span></span>

3. <span data-ttu-id="9ece0-115">ローカルの Homebrew リポジトリを更新します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-115">Update your local Homebrew repositories.</span></span>

   ```bash
   brew update
   ```

4. <span data-ttu-id="9ece0-116">`azure-cli` パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="9ece0-116">Install the `azure-cli` package.</span></span>

  ```bash
  brew install azure-cli
  ```

> [!NOTE]
> <span data-ttu-id="9ece0-117">以前 Homebrew で Azure CLI 1.0 をインストールしている場合、パッケージをインストールをするのではなく、通常の Homebrew アップグレード プロセスで CLI 2.0 を取得できます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-117">If you previously installed the Azure CLI 1.0 with Homebrew, instead of installing the package you can get CLI 2.0 through the regular Homebrew upgrade process.</span></span>
>
> ```bash
> brew upgrade
> ```

### <a name="install-manually"></a><span data-ttu-id="9ece0-118">手動でインストールする</span><span class="sxs-lookup"><span data-stu-id="9ece0-118">Install manually</span></span>

1. <span data-ttu-id="9ece0-119">`curl` で Azure CLI 2.0 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="9ece0-119">Install Azure CLI 2.0 with `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="9ece0-120">場合によっては、変更を有効にするために、シェルを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ece0-120">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="9ece0-121">コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-121">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-windows"></a><span data-ttu-id="9ece0-122">Windows へのインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-122">Install on Windows</span></span>

### <a name="install-with-msi-for-the-windows-command-line"></a><span data-ttu-id="9ece0-123">Windows コマンド ライン用に MSI でインストールを行う</span><span class="sxs-lookup"><span data-stu-id="9ece0-123">Install with MSI for the Windows command-line</span></span> 

<span data-ttu-id="9ece0-124">Windows に CLI をインストールして、Windows コマンド ラインで使用するには、[Azure CLI インストーラー (MSI)](https://aka.ms/InstallAzureCliWindows) をダウンロードして実行します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-124">To install the CLI on Windows and use it in the Windows command-line, download and run the [Azure CLI Installer (MSI)](https://aka.ms/InstallAzureCliWindows).</span></span>

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="9ece0-125">Bash on Ubuntu on Windows 用に apt-get でインストールを行う</span><span class="sxs-lookup"><span data-stu-id="9ece0-125">Install with apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="9ece0-126">Bash on Windows をインストールしていない場合は、[インストールします](https://msdn.microsoft.com/commandline/wsl/install_guide)。</span><span class="sxs-lookup"><span data-stu-id="9ece0-126">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="9ece0-127">Bash シェルを開きます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-127">Open the Bash shell.</span></span>

3. <span data-ttu-id="9ece0-128">ソース リストを変更します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-128">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="9ece0-129">次の sudo コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-129">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  <span data-ttu-id="9ece0-130">コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-130">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-apt-package-manager"></a><span data-ttu-id="9ece0-131">apt パッケージ マネージャーでのインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-131">Install with apt package manager</span></span> 

<span data-ttu-id="9ece0-132">Ubuntu、Debian など、`apt` パッケージ マネージャーを使用するディストリビューションでは、`apt-get` を使用して Azure CLI 2.0 をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-132">For distributions using the `apt` package manager such as Ubuntu or Debian, you can install Azure CLI 2.0 via `apt-get`.</span></span>

> [!NOTE]
> <span data-ttu-id="9ece0-133">CLI を使用するには、Python 2.7.x または Python 3.x が必要です。</span><span class="sxs-lookup"><span data-stu-id="9ece0-133">You must have Python 2.7.x or Python 3.x in order to use the CLI.</span></span> <span data-ttu-id="9ece0-134">ディストリビューションにいずれのパッケージもない場合は、[Python をインストール](https://www.python.org/downloads/)してください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-134">If your distribution does not have a package for either, [install Python](https://www.python.org/downloads/).</span></span>

1. <span data-ttu-id="9ece0-135">ソース リストを変更します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-135">Modify your sources list:</span></span>
 
   - <span data-ttu-id="9ece0-136">32 ビット システム</span><span class="sxs-lookup"><span data-stu-id="9ece0-136">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="9ece0-137">64 ビット システム</span><span class="sxs-lookup"><span data-stu-id="9ece0-137">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="9ece0-138">次の sudo コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-138">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  <span data-ttu-id="9ece0-139">コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-139">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-yum-package-manager"></a><span data-ttu-id="9ece0-140">yum パッケージ マネージャーでのインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-140">Install with yum package manager</span></span>

<span data-ttu-id="9ece0-141">Red Hat Enterprise Linux (RHEL)、Fedora、CentOS など、`yum` パッケージ マネージャーを使用するディストリビューションでは、`yum` を使用して Azure CLI 2.0 をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-141">For distributions which use the `yum` package manager such as Red Hat Enterprise Linux (RHEL), Fedora, or CentOS, you can install Azure CLI 2.0 via `yum`.</span></span>

> [!NOTE]
> <span data-ttu-id="9ece0-142">CLI を使用するには、Python 2.7.x または Python 3.x が必要です。</span><span class="sxs-lookup"><span data-stu-id="9ece0-142">You must have Python 2.7.x or Python 3.x in order to use the CLI.</span></span> <span data-ttu-id="9ece0-143">ディストリビューションにいずれのパッケージもない場合は、[Python をインストール](https://www.python.org/downloads/)してください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-143">If your distribution does not have a package for either, [install Python](https://www.python.org/downloads/).</span></span>

1. <span data-ttu-id="9ece0-144">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="9ece0-144">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="9ece0-145">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-145">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="9ece0-146">`yum` パッケージのインデックスを更新し、インストールを行います。</span><span class="sxs-lookup"><span data-stu-id="9ece0-146">Update the `yum` package index and install:</span></span>

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

4. <span data-ttu-id="9ece0-147">コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-147">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-zypper-package-manager"></a><span data-ttu-id="9ece0-148">zypper パッケージ マネージャーでのインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-148">Install with zypper package manager</span></span>

<span data-ttu-id="9ece0-149">OpenSUSE、SLE など、`zypper` パッケージ マネージャーを使用するディストリビューションでは、`zypper` を使用して Azure CLI 2.0 をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-149">For distributions which use the `zypper` package manager such as OpenSUSE or SLE, you can install Azure CLI 2.0 via `zypper`.</span></span>

> [!NOTE]
> <span data-ttu-id="9ece0-150">CLI を使用するには、Python 2.7.x または Python 3.x が必要です。</span><span class="sxs-lookup"><span data-stu-id="9ece0-150">You must have Python 2.7.x or Python 3.x in order to use the CLI.</span></span> <span data-ttu-id="9ece0-151">ディストリビューションにいずれのパッケージもない場合は、[Python をインストール](https://www.python.org/downloads/)してください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-151">If your distribution does not have a package for either, [install Python](https://www.python.org/downloads/).</span></span>

1. <span data-ttu-id="9ece0-152">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="9ece0-152">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="9ece0-153">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-153">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="9ece0-154">`zypper` パッケージのインデックスを更新し、インストールを行います。</span><span class="sxs-lookup"><span data-stu-id="9ece0-154">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install azure-cli
   ```

4. <span data-ttu-id="9ece0-155">コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-155">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-docker"></a><span data-ttu-id="9ece0-156">Docker によるインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-156">Install with Docker</span></span>

<span data-ttu-id="9ece0-157">Microsoft では、Azure CLI 2.0 が事前構成されている Docker イメージを保持しています。</span><span class="sxs-lookup"><span data-stu-id="9ece0-157">We maintain a Docker image preconfigured with the Azure CLI 2.0.</span></span>

<span data-ttu-id="9ece0-158">`docker run` を使用して、CLI をインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-158">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run -it azuresdk/azure-cli-python:<version>
   ```

<span data-ttu-id="9ece0-159">利用可能なバージョンについては、[Docker のタグ](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-159">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

<span data-ttu-id="9ece0-160">CLI は、`/usr/local/bin` の `az` コマンドとしてイメージにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-160">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="9ece0-161">ユーザー環境から SSH キーを取得する場合は、`-v ${HOME}:/root` を使用して、$HOME を `/root` としてマウントできます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-161">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -it -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-a-package-manager"></a><span data-ttu-id="9ece0-162"><a name="Linux"/>パッケージ マネージャーなしでの Linux へのインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-162"><a name="Linux"/>Install on Linux without a package manager</span></span>

<span data-ttu-id="9ece0-163">可能であれば、CLI はパッケージ マネージャーを使ってインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9ece0-163">It is recommended that you install the CLI with a package manager if you are able to.</span></span> <span data-ttu-id="9ece0-164">Microsoft のリポジトリを追加しない場合、または指定されたパッケージがないディストリビューションで操作している場合は、手動で CLI をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-164">If you do not want to add Microsoft's repositories, or are working with a distribution which does not have a provided package, you can manually install the CLI.</span></span>

1. <span data-ttu-id="9ece0-165">Linux ディストリビューションに応じて、前提条件をインストールします。</span><span class="sxs-lookup"><span data-stu-id="9ece0-165">Install the prerequisites based on your Linux distribution.</span></span>

   ```
   Platform              | Prerequisites
   ----------------------|---------------------------------------------
   Ubuntu 15.10 or 16.04 | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev build-essential
   Ubuntu 12.04 or 14.04 | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev
   Debian 8              | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev build-essential
   Debian 7              | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev
   CentOS 7.1 or 7.2     | sudo yum check-update; sudo yum install -y gcc python libffi-devel python-devel openssl-devel
   RedHat 7.2            | sudo yum check-update; sudo yum install -y gcc python libffi-devel python-devel openssl-devel
   SUSE OpenSUSE 13.2    | sudo zypper refresh && sudo zypper --non-interactive install curl gcc python python-xml libffi-devel python-devel openssl-devel
   ```

<span data-ttu-id="9ece0-166">ディストリビューションが上の一覧に記載されていない場合は、[Python 2.7 以降](https://www.python.org/downloads/)、[libffi](https://sourceware.org/libffi/)、[OpenSSL](https://www.openssl.org/source/) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ece0-166">If your distribution is not listed above, you will need to install [Python 2.7 or later](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), and [OpenSSL](https://www.openssl.org/source/).</span></span>

2. <span data-ttu-id="9ece0-167">`curl` で CLI をインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-167">Install the CLI with  `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="9ece0-168">場合によっては、変更を有効にするために、シェルを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ece0-168">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="9ece0-169">コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-169">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="9ece0-170">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="9ece0-170">Troubleshooting</span></span>

<span data-ttu-id="9ece0-171">CLI のインストール中に問題が発生した場合は、このセクションを見て、該当するケースの説明があるかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-171">If you encounter an issue during CLI install, check this section to see if your particular case is covered.</span></span> <span data-ttu-id="9ece0-172">問題がここで説明されていない場合は、[GitHub に問題を提出](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-172">If your issue is not here, please [file a Github issue](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="9ece0-173">curl の "Object Moved" エラー</span><span class="sxs-lookup"><span data-stu-id="9ece0-173">curl "Object Moved" error</span></span>

<span data-ttu-id="9ece0-174">`curl` で `-L` パラメーターに関連するエラーが発生した場合や、"Object Moved" というテキストが含まれているエラー メッセージが表示された場合は、次のように、`aka.ms` リダイレクトの代わりに完全な URL を使用してみてください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-174">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a><span data-ttu-id="9ece0-175">`az` コマンドが見つからない</span><span class="sxs-lookup"><span data-stu-id="9ece0-175">`az` command not found</span></span>

<span data-ttu-id="9ece0-176">シェルのコマンド ハッシュのキャッシュをクリアすることが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9ece0-176">You may need to clear your shell's command hash cache.</span></span> <span data-ttu-id="9ece0-177">実行</span><span class="sxs-lookup"><span data-stu-id="9ece0-177">Run</span></span>

```bash
hash -r
```

<span data-ttu-id="9ece0-178">問題が解決されているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-178">and see if the problem is resolved.</span></span> <span data-ttu-id="9ece0-179">コマンドが、`$PATH` にない可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="9ece0-179">The command may also not be in your `$PATH`.</span></span> <span data-ttu-id="9ece0-180">`<install path>/bin` が `$PATH` に 表示されることを確認し、必要に応じてシェルを再起動してください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-180">Make sure that `<install path>/bin` appears in your `$PATH`, and restart your shell if necessary.</span></span>

## <a name="uninstall-cli-1x-versions"></a><span data-ttu-id="9ece0-181">CLI 1.x バージョンのアンインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-181">Uninstall CLI 1.x versions</span></span>

<span data-ttu-id="9ece0-182">システム上で以前の CLI 1.x バージョンが使用可能な場合は、使用されたインストールの種類に基づいてアンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-182">If you have an earlier CLI 1.x version available on your system, you can uninstall it based upon the type of install used.</span></span>

### <a name="uninstall-with-npm"></a><span data-ttu-id="9ece0-183">npm でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-183">Uninstall with npm</span></span>

<span data-ttu-id="9ece0-184">古い CLI を `npm uninstall` で削除します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-184">Remove the older CLI with `npm uninstall`.</span></span>

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="uninstall-with-distributable"></a><span data-ttu-id="9ece0-185">再頒布可能パッケージでのアンインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-185">Uninstall with distributable</span></span>

<span data-ttu-id="9ece0-186">[Azure CLI インストーラー (MSI)](http://aka.ms/webpi-azure-cli) または [macOS パッケージ](http://aka.ms/mac-azure-cli)を通じてインストールした場合は、同じツールを使用してインストールを削除してください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-186">If you installed via the [Azure CLI Installer (MSI)](http://aka.ms/webpi-azure-cli) or a [macOS package](http://aka.ms/mac-azure-cli), use the same tool to remove your install.</span></span>

### <a name="uninstall-with-docker"></a><span data-ttu-id="9ece0-187">Docker でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-187">Uninstall with Docker</span></span>

<span data-ttu-id="9ece0-188">以前の CLI バージョンを使用するために Docker イメージをインストールした場合は、そのイメージと、関連するすべてのコンテナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-188">If you installed a Docker image to use the earlier CLI version, remove that image and any associated containers.</span></span> <span data-ttu-id="9ece0-189">その後、インストール手順の説明に従って新しい Docker イメージをインストールしてから、コンテナーを再作成できます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-189">You can then re-create the containers after installing the new Docker image as described in the install instructions.</span></span>

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a><span data-ttu-id="9ece0-190">CLI の更新</span><span class="sxs-lookup"><span data-stu-id="9ece0-190">Update the CLI</span></span>

<span data-ttu-id="9ece0-191">Azure CLI を更新するには、それをインストールしたのと同じ方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-191">To update the Azure CLI, use the same method that you used to install it.</span></span>

### <a name="update-with-homebrew"></a><span data-ttu-id="9ece0-192">Homebrew での更新</span><span class="sxs-lookup"><span data-stu-id="9ece0-192">Update with Homebrew</span></span>

1. <span data-ttu-id="9ece0-193">以前に手動でインストール済みの場合は、「[Homebrew でインストールする](#macOS)」の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9ece0-193">If you previously installed manually, follow the [install with Homebrew](#macOS) instructions.</span></span>

2. <span data-ttu-id="9ece0-194">ローカルの Homebrew リポジトリ情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-194">Update your local Homebrew repository information.</span></span>

   ```bash
   brew update
   ```

3. <span data-ttu-id="9ece0-195">インストール済みパッケージをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="9ece0-195">Upgrade your installed packages.</span></span>

   ```bash
   brew upgrade
   ```

### <a name="update-with-msi"></a><span data-ttu-id="9ece0-196">MSI での更新</span><span class="sxs-lookup"><span data-stu-id="9ece0-196">Update with MSI</span></span>

<span data-ttu-id="9ece0-197">もう一度 [Azure CLI インストーラー (MSI)](https://aka.ms/InstallAzureCliWindows) を実行します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-197">Run the [Azure CLI Installer (MSI)](https://aka.ms/InstallAzureCliWindows) again.</span></span>

### <a name="update-with-apt"></a><span data-ttu-id="9ece0-198">apt での更新</span><span class="sxs-lookup"><span data-stu-id="9ece0-198">Update with apt</span></span>

<span data-ttu-id="9ece0-199">CLI パッケージを更新するには、`apt-get upgrade` を使用します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-199">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="9ece0-200">これにより、依存関係が変更されていない、システム上のすべてのインストール済みパッケージがアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-200">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="9ece0-201">CLI のみをアップグレードするには、`apt-get install` を使用します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-201">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-yum"></a><span data-ttu-id="9ece0-202">yum での更新</span><span class="sxs-lookup"><span data-stu-id="9ece0-202">Update with yum</span></span>

<span data-ttu-id="9ece0-203">`yum update` コマンドで Azure CLI を更新します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-203">Update the Azure CLI with the `yum update` command.</span></span>

```bash
yum check-update
sudo yum update azure-cli
```

### <a name="update-with-zypper"></a><span data-ttu-id="9ece0-204">zypper での更新</span><span class="sxs-lookup"><span data-stu-id="9ece0-204">Update with zypper</span></span>

<span data-ttu-id="9ece0-205">`zypper update` コマンドでパッケージを更新できます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-205">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

### <a name="update-with-docker"></a><span data-ttu-id="9ece0-206">Docker での更新</span><span class="sxs-lookup"><span data-stu-id="9ece0-206">Update with Docker</span></span>

1. <span data-ttu-id="9ece0-207">`docker pull` でローカル イメージを更新します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-207">Update your local image with `docker pull`.</span></span>

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. <span data-ttu-id="9ece0-208">現時点で CLI イメージを使用しているコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-208">Get the containers currently using the CLI image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> <span data-ttu-id="9ece0-209">イメージの特定のバージョンをインストールした場合は、イメージ名の末尾に `:<version>` を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ece0-209">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

3. <span data-ttu-id="9ece0-210">コンテナーを停止し、もう一度作成します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-210">Halt and recreate the containers.</span></span>

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a><span data-ttu-id="9ece0-211">手動での更新</span><span class="sxs-lookup"><span data-stu-id="9ece0-211">Update manually</span></span>

<span data-ttu-id="9ece0-212">更新するには、[macOS](#macOS) または [Linux](#Linux) の手動でのインストール手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-212">Follow the manual installation instructions for [macOS](#macOS) or [Linux](#Linux) to update.</span></span>

## <a name="uninstall"></a><span data-ttu-id="9ece0-213">アンインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-213">Uninstall</span></span>

<span data-ttu-id="9ece0-214">CLI が不要であると判断した場合は、アンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-214">If you decide to uninstall the CLI, we're sorry to see you go.</span></span> <span data-ttu-id="9ece0-215">CLI をインストールしたときと同じ方法を使用して、アンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ece0-215">You should uninstall using the same method that you used to install the CLI.</span></span>

### <a name="uninstall-with-homebrew"></a><span data-ttu-id="9ece0-216">Homebrew でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-216">Uninstall with Homebrew</span></span>

<span data-ttu-id="9ece0-217">`azure-cli` パッケージをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="9ece0-217">Uninstall the `azure-cli` package.</span></span>

   ```bash
   brew uninstall azure-cli
   ```

### <a name="uninstall-with-msi"></a><span data-ttu-id="9ece0-218">MSI でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-218">Uninstall with MSI</span></span>

<span data-ttu-id="9ece0-219">[MSI](https://aka.ms/InstallAzureCliWindows) をもう一度実行して、アンインストールを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-219">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="uninstall-with-apt"></a><span data-ttu-id="9ece0-220">apt でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-220">Uninstall with apt</span></span>

<span data-ttu-id="9ece0-221">次のように、`apt-get remove` を通じてアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="9ece0-221">Uninstall via `apt-get remove`:</span></span>

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-yum"></a><span data-ttu-id="9ece0-222">yum でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-222">Uninstall with yum</span></span>

1. <span data-ttu-id="9ece0-223">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-223">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="9ece0-224">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-224">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="9ece0-225">リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-225">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

### <a name="uninstall-with-zypper"></a><span data-ttu-id="9ece0-226">zypper でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-226">Uninstall with zypper</span></span>

1. <span data-ttu-id="9ece0-227">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-227">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="9ece0-228">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-228">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

  ```bash
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. <span data-ttu-id="9ece0-229">リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-229">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

### <a name="uninstall-with-docker"></a><span data-ttu-id="9ece0-230">Docker でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-230">Uninstall with Docker</span></span>

<span data-ttu-id="9ece0-231">Docker イメージをインストールした場合は、それを実行しているすべてのコンテナーを削除してから、ローカル イメージを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ece0-231">If you installed a docker image, you will need to remove any containers running it, and then delete the local image.</span></span>

1. <span data-ttu-id="9ece0-232">azure-cli イメージを実行しているコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-232">Get the containers which are running the azure-cli image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

2. <span data-ttu-id="9ece0-233">CLI イメージがあるすべてのコンテナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-233">Delete any containers with the CLI image.</span></span>

   ```bash
   docker rm 34a868beb2ab
   ```

3. <span data-ttu-id="9ece0-234">ローカルにインストールされた CLI イメージを削除します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-234">Remove the locally installed CLI image.</span></span>

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

> [!NOTE]
> <span data-ttu-id="9ece0-235">イメージの特定のバージョンをインストールした場合は、イメージ名の末尾に `:<version>` を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ece0-235">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

###<a name="a-nameuninstallmanuallyuninstall-manually"></a><span data-ttu-id="9ece0-236"><a name="UninstallManually"/>手動でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="9ece0-236"><a name="UninstallManually"/>Uninstall manually</span></span>

<span data-ttu-id="9ece0-237">https://aka.ms/InstallAzureCli のスクリプトを使用して CLI をインストールした場合は、次の手順でアンインストールできます。</span><span class="sxs-lookup"><span data-stu-id="9ece0-237">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="9ece0-238">インストールされたファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-238">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="9ece0-239">`<install location>/.bash_profile` から `<install location>/lib/azure-cli/az.completion` という行を削除します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-239">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

3. <span data-ttu-id="9ece0-240">シェルでコマンド キャッシュを使用する場合は、それを再度読み込んでください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-240">If your shell uses a command cache, reload it.</span></span>

   ```bash
   hash -r
   ```

> [!Note]
> <span data-ttu-id="9ece0-241">既定のインストール場所は `/Users/<username>` です。</span><span class="sxs-lookup"><span data-stu-id="9ece0-241">The default install location is `/Users/<username>`.</span></span>

## <a name="report-cli-issues-and-feedback"></a><span data-ttu-id="9ece0-242">CLI の問題とフィードバックの報告</span><span class="sxs-lookup"><span data-stu-id="9ece0-242">Report CLI issues and feedback</span></span>

<span data-ttu-id="9ece0-243">ツールにバグを発見した場合は、GitHub リポジトリの [[Issues]\(問題\)](https://github.com/Azure/azure-cli/issues) セクションで問題を報告してください。</span><span class="sxs-lookup"><span data-stu-id="9ece0-243">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repository.</span></span>
<span data-ttu-id="9ece0-244">コマンド ラインからフィードバックを送るには、`az feedback` コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="9ece0-244">To provide feedback from the command line, use the `az feedback` command.</span></span>
