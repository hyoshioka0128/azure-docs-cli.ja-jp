---
title: "Azure CLI 2.0 のインストール"
description: "Azure CLI 2.0 のインストールに関するリファレンス ドキュメント"
keywords: "Azure CLI 2.0, Azure CLI 2.0 のリファレンス, Azure CLI 2.0 のインストール, Azure Python CLI, Azure CLI 2.0 のアンインストール, Azure CLI, Azure CLI のインストール, Azure CLI のリファレンス"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 08/17/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 00d5b555975007d7e57f04ce5d69f4f29e6d0219
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="372dd-104">Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="372dd-105">今すぐ Azure CLI の新しいバージョンをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="372dd-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="372dd-106">Azure のリソース管理を目的とした優れたネイティブ コマンド ライン エクスペリエンスを実現するために強化して更新しました。</span><span class="sxs-lookup"><span data-stu-id="372dd-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="372dd-107">macOS、Linux、および Windows で使用できます。</span><span class="sxs-lookup"><span data-stu-id="372dd-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="372dd-108">最新リリースについては、[リリース ノート](release-notes-azure-cli.md)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="372dd-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="372dd-109">Azure CLI の以前のバージョンが必要な場合は、[Azure CLI 1.0 をインストールする](/azure/cli-install-nodejs)方法に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="372dd-109">If you need the previous version of the Azure CLI, here's how to [install Azure CLI 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="a-namemacosinstall-on-macos"></a><span data-ttu-id="372dd-110"><a name="macOS"/>macOS へのインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-110"><a name="macOS"/>Install on macOS</span></span>

1. <span data-ttu-id="372dd-111">`curl` で Azure CLI 2.0 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="372dd-111">Install Azure CLI 2.0 with `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="372dd-112">場合によっては、変更を有効にするために、シェルを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="372dd-112">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="372dd-113">コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="372dd-113">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-windows"></a><span data-ttu-id="372dd-114">Windows へのインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-114">Install on Windows</span></span>

<span data-ttu-id="372dd-115">MSI を使用して Azure CLI 2.0 をインストールし、Windows コマンド ラインで使用するか、Bash on Ubuntu on Windows で `apt-get` を使用して、CLI をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="372dd-115">You can install Azure CLI 2.0 with the MSI and use it in the Windows command-line, or you can install the CLI with `apt-get` on Bash on Ubuntu on Windows.</span></span>

### <a name="install-with-msi-for-the-windows-command-line"></a><span data-ttu-id="372dd-116">Windows コマンド ライン用に MSI でインストールを行う</span><span class="sxs-lookup"><span data-stu-id="372dd-116">Install with MSI for the Windows command-line</span></span> 

<span data-ttu-id="372dd-117">Windows に CLI をインストールして、Windows コマンド ラインで使用するには、[MSI](https://aka.ms/InstallAzureCliWindows) をダウンロードして実行します。</span><span class="sxs-lookup"><span data-stu-id="372dd-117">To install the CLI on Windows and use it in the Windows command-line, download and run the [MSI](https://aka.ms/InstallAzureCliWindows).</span></span>

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="372dd-118">Bash on Ubuntu on Windows 用に apt-get でインストールを行う</span><span class="sxs-lookup"><span data-stu-id="372dd-118">Install with apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="372dd-119">Bash on Windows をインストールしていない場合は、[インストールします](https://msdn.microsoft.com/commandline/wsl/install_guide)。</span><span class="sxs-lookup"><span data-stu-id="372dd-119">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="372dd-120">Bash シェルを開きます。</span><span class="sxs-lookup"><span data-stu-id="372dd-120">Open the Bash shell.</span></span>

3. <span data-ttu-id="372dd-121">ソース リストを変更します。</span><span class="sxs-lookup"><span data-stu-id="372dd-121">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="372dd-122">次の sudo コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="372dd-122">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  <span data-ttu-id="372dd-123">コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="372dd-123">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-debianubuntu-with-apt-get"></a><span data-ttu-id="372dd-124">apt-get による Debian/Ubuntu へのインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-124">Install on Debian/Ubuntu with apt-get</span></span>

<span data-ttu-id="372dd-125">Debian/Ubuntu ベースのシステムでは、`apt-get` を使用して Azure CLI 2.0 をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="372dd-125">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="372dd-126">ソース リストを変更します。</span><span class="sxs-lookup"><span data-stu-id="372dd-126">Modify your sources list.</span></span>
 
   - <span data-ttu-id="372dd-127">32 ビット システム</span><span class="sxs-lookup"><span data-stu-id="372dd-127">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="372dd-128">64 ビット システム</span><span class="sxs-lookup"><span data-stu-id="372dd-128">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="372dd-129">次の sudo コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="372dd-129">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  <span data-ttu-id="372dd-130">コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="372dd-130">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-docker"></a><span data-ttu-id="372dd-131">Docker によるインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-131">Install with Docker</span></span>

<span data-ttu-id="372dd-132">Microsoft では、Azure CLI 2.0 が事前構成されている Docker イメージを保持しています。</span><span class="sxs-lookup"><span data-stu-id="372dd-132">We maintain a Docker image preconfigured with the Azure CLI 2.0.</span></span>

<span data-ttu-id="372dd-133">`docker run` を使用して、CLI をインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="372dd-133">Install the CLI using `docker run`.</span></span>

  ```bash
  docker run azuresdk/azure-cli-python:<version>
  ```

<span data-ttu-id="372dd-134">利用可能なバージョンについては、[Docker のタグ](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="372dd-134">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

<span data-ttu-id="372dd-135">CLI は、`/usr/local/bin` の `az` コマンドとしてイメージにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="372dd-135">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="372dd-136">ユーザー環境から SSH キーを取得する場合は、`-v ${HOME}:/root` を使用して、$HOME を `/root` としてマウントできます。</span><span class="sxs-lookup"><span data-stu-id="372dd-136">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-apt-get"></a><span data-ttu-id="372dd-137"><a name="Linux"/>apt-get なしでの Linux へのインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-137"><a name="Linux"/>Install on Linux without apt-get</span></span>

<span data-ttu-id="372dd-138">できれば、`apt-get` で CLI をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="372dd-138">It is recommended that you install the CLI with `apt-get` if you are able to.</span></span> <span data-ttu-id="372dd-139">`apt` パッケージ マネージャーを使用しないディストリビューションでは、インストールを手動で行えます。</span><span class="sxs-lookup"><span data-stu-id="372dd-139">For distributions which do not use the `apt` package manager, you can manually install.</span></span>

1. <span data-ttu-id="372dd-140">Linux ディストリビューションに応じて、前提条件をインストールします。</span><span class="sxs-lookup"><span data-stu-id="372dd-140">Install the prerequisites based on your Linux distribution.</span></span>

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

<span data-ttu-id="372dd-141">ディストリビューションが上の一覧に記載されていない場合は、[Python](https://www.python.org/downloads/)、[libffi](https://sourceware.org/libffi/)、および [OpenSSL](https://www.openssl.org/source/) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="372dd-141">If your distribution is not listed above, you will need to install [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), and [OpenSSL](https://www.openssl.org/source/).</span></span>

2. <span data-ttu-id="372dd-142">`curl` で CLI をインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="372dd-142">Install the CLI with  `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="372dd-143">場合によっては、変更を有効にするために、シェルを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="372dd-143">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="372dd-144">コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="372dd-144">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="372dd-145">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="372dd-145">Troubleshooting</span></span>

<span data-ttu-id="372dd-146">CLI のインストール中に問題が発生した場合は、このセクションを見て、該当するケースの説明があるかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="372dd-146">If you encounter an issue during CLI install, check this section to see if your particular case is covered.</span></span> <span data-ttu-id="372dd-147">問題がここで説明されていない場合は、[GitHub に問題を提出](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="372dd-147">If your issue is not here, please [file a Github issue](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="372dd-148">curl の "Object Moved" エラー</span><span class="sxs-lookup"><span data-stu-id="372dd-148">curl "Object Moved" error</span></span>

<span data-ttu-id="372dd-149">`curl` で `-L` パラメーターに関連するエラーが発生した場合や、"Object Moved" というテキストが含まれているエラー メッセージが表示された場合は、次のように、`aka.ms` リダイレクトの代わりに完全な URL を使用してみてください。</span><span class="sxs-lookup"><span data-stu-id="372dd-149">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="homebrew-on-macos-installing-older-version"></a><span data-ttu-id="372dd-150">macOS の Homebrew による古いバージョンのインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-150">Homebrew on macOS installing older version</span></span>

<span data-ttu-id="372dd-151">macOS で使用可能な Homebrew `azure-cli` Formula は、現在古くなっており、CLI の 1.x バージョンをインストールします。</span><span class="sxs-lookup"><span data-stu-id="372dd-151">The Homebrew `azure-cli` formula available for macOS is currently out of date, and will install a 1.x version of the CLI.</span></span> <span data-ttu-id="372dd-152">いつ更新されたかを調べるには、`brew info azure-cli` を確認してください。</span><span class="sxs-lookup"><span data-stu-id="372dd-152">You can see when it is updated by checking `brew info azure-cli`.</span></span>

<span data-ttu-id="372dd-153">更新されるまでは、[古いバージョンをアンインストール](#uninstall_brew)し、[macOS のインストール手順](#macOS)に従ってください。</span><span class="sxs-lookup"><span data-stu-id="372dd-153">Until then, [uninstall the older version](#uninstall_brew) and follow the [macOS install instructions](#macOS).</span></span>

## <a name="uninstall-cli-1x-versions"></a><span data-ttu-id="372dd-154">CLI 1.x バージョンのアンインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-154">Uninstall CLI 1.x versions</span></span>

<span data-ttu-id="372dd-155">システム上で以前の CLI 1.x バージョンが使用可能な場合は、使用されたインストールの種類に基づいてアンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="372dd-155">If you have an earlier CLI 1.x version available on your system, you can uninstall it based upon the type of install used.</span></span>

### <a name="uninstall-with-npm"></a><span data-ttu-id="372dd-156">npm でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-156">Uninstall with npm</span></span>

<span data-ttu-id="372dd-157">古い CLI を `npm uninstall` で削除します。</span><span class="sxs-lookup"><span data-stu-id="372dd-157">Remove the older CLI with `npm uninstall`.</span></span>

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="a-nameuninstallbrewuninstall-with-homebrew-on-macos"></a><span data-ttu-id="372dd-158"><a name="uninstall_brew"/>macOS の Homebrew でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-158"><a name="uninstall_brew"/>Uninstall with Homebrew on macOS</span></span>

<span data-ttu-id="372dd-159">古い CLI を `brew uninstall` で削除します。</span><span class="sxs-lookup"><span data-stu-id="372dd-159">Remove the older CLI with `brew uninstall`.</span></span>

```bash
brew uninstall azure-cli
```

### <a name="uninstall-with-distributable"></a><span data-ttu-id="372dd-160">再頒布可能パッケージでのアンインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-160">Uninstall with distributable</span></span>

<span data-ttu-id="372dd-161">[MSI](http://aka.ms/webpi-azure-cli) または [macOS パッケージ](http://aka.ms/mac-azure-cli)を通じてインストールした場合は、同じツールを使用してインストールを削除してください。</span><span class="sxs-lookup"><span data-stu-id="372dd-161">If you installed via [MSI](http://aka.ms/webpi-azure-cli) or a [macOS package](http://aka.ms/mac-azure-cli), use the same tool to remove your install.</span></span>

### <a name="uninstall-with-docker"></a><span data-ttu-id="372dd-162">Docker でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-162">Uninstall with Docker</span></span>

<span data-ttu-id="372dd-163">以前の CLI バージョンを使用するために Docker イメージをインストールした場合は、そのイメージと、関連するすべてのコンテナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="372dd-163">If you installed a Docker image to use the earlier CLI version, remove that image and any associated containers.</span></span> <span data-ttu-id="372dd-164">その後、インストール手順の説明に従って新しい Docker イメージをインストールしてから、コンテナーを再作成できます。</span><span class="sxs-lookup"><span data-stu-id="372dd-164">You can then re-create the containers after installing the new Docker image as described in the install instructions.</span></span>

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a><span data-ttu-id="372dd-165">CLI の更新</span><span class="sxs-lookup"><span data-stu-id="372dd-165">Update the CLI</span></span>

<span data-ttu-id="372dd-166">Azure CLI を更新するには、それをインストールしたのと同じ方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="372dd-166">To update the Azure CLI, use the same method that you used to install it.</span></span>

### <a name="update-with-msi"></a><span data-ttu-id="372dd-167">MSI での更新</span><span class="sxs-lookup"><span data-stu-id="372dd-167">Update with MSI</span></span>

<span data-ttu-id="372dd-168">[MSI](https://aka.ms/InstallAzureCliWindows) をもう一度実行します。</span><span class="sxs-lookup"><span data-stu-id="372dd-168">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again.</span></span>

### <a name="update-with-apt-get"></a><span data-ttu-id="372dd-169">apt-get での更新</span><span class="sxs-lookup"><span data-stu-id="372dd-169">Update with apt-get</span></span>

<span data-ttu-id="372dd-170">CLI パッケージを更新するには、`apt-get upgrade` を使用します。</span><span class="sxs-lookup"><span data-stu-id="372dd-170">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="372dd-171">これにより、依存関係が変更されていない、システム上のすべてのインストール済みパッケージがアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="372dd-171">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="372dd-172">CLI のみをアップグレードするには、`apt-get install` を使用します。</span><span class="sxs-lookup"><span data-stu-id="372dd-172">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-docker"></a><span data-ttu-id="372dd-173">Docker での更新</span><span class="sxs-lookup"><span data-stu-id="372dd-173">Update with Docker</span></span>

1. <span data-ttu-id="372dd-174">`docker pull` でローカル イメージを更新します。</span><span class="sxs-lookup"><span data-stu-id="372dd-174">Update your local image with `docker pull`.</span></span>

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. <span data-ttu-id="372dd-175">現時点で CLI イメージを使用しているコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="372dd-175">Get the containers currently using the CLI image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> <span data-ttu-id="372dd-176">イメージの特定のバージョンをインストールした場合は、イメージ名の末尾に `:<version>` を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="372dd-176">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

3. <span data-ttu-id="372dd-177">コンテナーを停止し、もう一度作成します。</span><span class="sxs-lookup"><span data-stu-id="372dd-177">Halt and recreate the containers.</span></span>

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a><span data-ttu-id="372dd-178">手動での更新</span><span class="sxs-lookup"><span data-stu-id="372dd-178">Update manually</span></span>

<span data-ttu-id="372dd-179">更新するには、[macOS](#macOS) または [Linux](#Linux) の手動でのインストール手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="372dd-179">Follow the manual installation instructions for [macOS](#macOS) or [Linux](#Linux) to update.</span></span>

## <a name="uninstall"></a><span data-ttu-id="372dd-180">アンインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-180">Uninstall</span></span>

<span data-ttu-id="372dd-181">CLI が不要であると判断した場合は、アンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="372dd-181">If you decide to uninstall the CLI, we're sorry to see you go.</span></span> <span data-ttu-id="372dd-182">CLI をインストールしたときと同じ方法を使用して、アンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="372dd-182">You should uninstall using the same method that you used to install the CLI.</span></span>

### <a name="uninstall-with-msi"></a><span data-ttu-id="372dd-183">MSI でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-183">Uninstall with MSI</span></span>

<span data-ttu-id="372dd-184">[MSI](https://aka.ms/InstallAzureCliWindows) をもう一度実行して、アンインストールを選択します。</span><span class="sxs-lookup"><span data-stu-id="372dd-184">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="uninstall-with-apt-get"></a><span data-ttu-id="372dd-185">apt-get でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-185">Uninstall with apt-get</span></span>

<span data-ttu-id="372dd-186">次のように、`apt-get remove` を通じてアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="372dd-186">Uninstall via `apt-get remove`:</span></span>

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-docker"></a><span data-ttu-id="372dd-187">Docker でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-187">Uninstall with Docker</span></span>

<span data-ttu-id="372dd-188">Docker イメージをインストールした場合は、それを実行しているすべてのコンテナーを削除してから、ローカル イメージを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="372dd-188">If you installed a docker image, you will need to remove any containers running it, and then delete the local image.</span></span>

1. <span data-ttu-id="372dd-189">azure-cli イメージを実行しているコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="372dd-189">Get the containers which are running the azure-cli image.</span></span>

  ```bash
  docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
  ```

  ```output
  CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
  34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
  ```

2. <span data-ttu-id="372dd-190">CLI イメージがあるすべてのコンテナーを削除します。</span><span class="sxs-lookup"><span data-stu-id="372dd-190">Delete any containers with the CLI image.</span></span>

  ```bash
  docker rm 34a868beb2ab
  ```

3. <span data-ttu-id="372dd-191">ローカルにインストールされた CLI イメージを削除します。</span><span class="sxs-lookup"><span data-stu-id="372dd-191">Remove the locally installed CLI image.</span></span>

  ```bash
  docker rmi azuresdk/azure-cli-python
  ```

> [!NOTE]
> <span data-ttu-id="372dd-192">イメージの特定のバージョンをインストールした場合は、イメージ名の末尾に `:<version>` を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="372dd-192">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

### <a name="uninstall-manually"></a><span data-ttu-id="372dd-193">手動でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="372dd-193">Uninstall manually</span></span>

<span data-ttu-id="372dd-194">https://aka.ms/InstallAzureCli のスクリプトを使用して CLI をインストールした場合は、次の手順でアンインストールできます。</span><span class="sxs-lookup"><span data-stu-id="372dd-194">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="372dd-195">インストールされたファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="372dd-195">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="372dd-196">`<install location>/.bash_profile` から `<install location>/lib/azure-cli/az.completion` という行を削除します。</span><span class="sxs-lookup"><span data-stu-id="372dd-196">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="372dd-197">既定のインストール場所は `/Users/<username>` です。</span><span class="sxs-lookup"><span data-stu-id="372dd-197">The default install location is `/Users/<username>`.</span></span>

## <a name="report-cli-issues-and-feedback"></a><span data-ttu-id="372dd-198">CLI の問題とフィードバックの報告</span><span class="sxs-lookup"><span data-stu-id="372dd-198">Report CLI issues and feedback</span></span>

<span data-ttu-id="372dd-199">ツールにバグを発見した場合は、GitHub リポジトリの [[Issues]\(問題\)](https://github.com/Azure/azure-cli/issues) セクションで問題を報告してください。</span><span class="sxs-lookup"><span data-stu-id="372dd-199">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repository.</span></span>
<span data-ttu-id="372dd-200">コマンド ラインからフィードバックを送るには、`az feedback` コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="372dd-200">To provide feedback from the command line, use the `az feedback` command.</span></span>
