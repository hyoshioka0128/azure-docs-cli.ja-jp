---
title: Azure CLI 1.0 のインストール | Microsoft Docs
description: Mac、Linux、および Windows に Azure CLI 1.0 をインストールして Azure サービスの利用を開始する
editor: ''
manager: timlt
documentationcenter: ''
author: squillace
services: virtual-machines-linux,virtual-network,storage,azure-resource-manager
tags: azure-resource-manager,azure-service-management
ms.assetid: bdb776c8-7a76-4f3a-887c-236b4fffee10
ms.service: multiple
ms.workload: multiple
ms.tgt_pltfrm: command-line-interface
ms.devlang: na
ms.topic: article
ms.date: 03/20/2017
ms.author: rasquill
ms.openlocfilehash: 1c57e920c52f7f324c32fd457165bbafbda19b21
ms.sourcegitcommit: d9e5743a4321684c412c1740d26e7c1e258af5b2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/30/2018
---
# <a name="install-the-azure-cli-10"></a><span data-ttu-id="aa595-103">Azure CLI 1.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="aa595-103">Install the Azure CLI 1.0</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa595-104">このトピックでは、Azure CLI 1.0 のインストール方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="aa595-104">This topic describes how to install the Azure CLI 1.0.</span></span> <span data-ttu-id="aa595-105">この CLI は廃止されており、"従来の" リソースを使用した Azure サービス管理 (ASM) モデルのサポートにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="aa595-105">This CLI is deprecated and should only be used for support with the Azure Service Management (ASM) model with "classic" resources.</span></span>
> <span data-ttu-id="aa595-106">Azure Resource Manager のデプロイには、[Azure CLI 2.0](/cli/azure) を使用します。</span><span class="sxs-lookup"><span data-stu-id="aa595-106">For Azure Resource Manager deployments, use [Azure CLI 2.0](/cli/azure).</span></span>

<span data-ttu-id="aa595-107">Azure コマンド ライン インターフェイス (Azure CLI 1.0) を簡単にインストールして、コマンド ライン シェルからオープン ソースのコマンドを使って Microsoft Azure 上のリソースを作成したり管理したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="aa595-107">Quickly install the Azure Command-Line Interface (Azure CLI 1.0) to use a set of open-source shell-based commands for creating and managing resources in Microsoft Azure.</span></span> <span data-ttu-id="aa595-108">お使いのコンピューターにこれらのクロスプラットフォーム ツールをインストールするオプションは複数あります。</span><span class="sxs-lookup"><span data-stu-id="aa595-108">You have several options to install these cross-platform tools on your computer:</span></span>

* <span data-ttu-id="aa595-109">**npm パッケージ** - npm (JavaScript 用のパッケージ マネージャー) を実行して、Linux ディストリビューションまたは OS に最新の Azure CLI 1.0 パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="aa595-109">**npm package** - Run npm (the package manager for JavaScript) to install the latest Azure CLI 1.0 package on your Linux distribution or OS.</span></span> <span data-ttu-id="aa595-110">お使いのコンピューターに node.js と npm が必要です。</span><span class="sxs-lookup"><span data-stu-id="aa595-110">Requires node.js and npm on your computer.</span></span>
* <span data-ttu-id="aa595-111">**インストーラー** - Mac または Windows に簡単インストールするにはインストーラーをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="aa595-111">**Installer** - Download an installer for easy installation on Mac or Windows.</span></span>
* <span data-ttu-id="aa595-112">**Docker コンテナー** - すぐに実行できる Docker コンテナーで最新の CLI の使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="aa595-112">**Docker container** - Start using the latest CLI in a ready-to-run Docker container.</span></span> <span data-ttu-id="aa595-113">お使いのコンピューター上に Docker ホストが必要です。</span><span class="sxs-lookup"><span data-stu-id="aa595-113">Requires Docker host on your computer.</span></span>

<span data-ttu-id="aa595-114">その他のオプションと背景については、 [GitHub](https://github.com/azure/azure-xplat-cli)のプロジェクト リポジトリを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa595-114">For more options and background, see the project repository on [GitHub](https://github.com/azure/azure-xplat-cli).</span></span>

<span data-ttu-id="aa595-115">Azure CLI 1.0 をインストールした後、[Azure サブスクリプションに接続](/cli/azure/authenticate-azure-cli)し、コマンド ライン インターフェイス (Bash、ターミナル、コマンド プロンプトなど) から **azure** コマンドを実行して、Azure リソースを操作します。</span><span class="sxs-lookup"><span data-stu-id="aa595-115">Once the Azure CLI 1.0 is installed, [connect it with your Azure subscription](/cli/azure/authenticate-azure-cli) and run the **azure** commands from your command-line interface (Bash, Terminal, Command prompt, and so on) to work with your Azure resources.</span></span>

## <a name="option-1-install-an-npm-package"></a><span data-ttu-id="aa595-116">オプション 1: npm パッケージのインストール</span><span class="sxs-lookup"><span data-stu-id="aa595-116">Option 1: Install an npm package</span></span>
<span data-ttu-id="aa595-117">CLI を npm パッケージからインストールするには、[最新の Node.js と npm](https://nodejs.org/en/download/package-manager/) をダウンロードし、インストールしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="aa595-117">To install the CLI from an npm package, make sure you have downloaded and installed the [latest Node.js and npm](https://nodejs.org/en/download/package-manager/).</span></span> <span data-ttu-id="aa595-118">次に、**npm install** を実行して、azure-cli パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="aa595-118">Then, run **npm install** to install the azure-cli package:</span></span>

```bash
npm install -g azure-cli
```

<span data-ttu-id="aa595-119">Linux ディストリビューションの場合、**npm** コマンドを正常に実行するには、次のように **sudo** の使用が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="aa595-119">On Linux distributions, you might need to use **sudo** to successfully run the **npm** command, as follows:</span></span>

```bash
sudo npm install -g azure-cli
```

> [!NOTE]
> <span data-ttu-id="aa595-120">Node.js と npm を Linux ディストリビューションまたは OS にインストールまたは更新する必要がある場合は、最新の Node.js LTS バージョン (4.x) をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="aa595-120">If you need to install or update Node.js and npm on your Linux distribution or OS, we recommend that you install the most recent Node.js LTS version (4.x).</span></span> <span data-ttu-id="aa595-121">以前のバージョンを使用すると、インストール エラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="aa595-121">If you use an older version, you might get installation errors.</span></span>

<span data-ttu-id="aa595-122">必要に応じて、npm パッケージの最新の Linux [tar ファイルを][linux-installer]ローカルにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="aa595-122">If you prefer, download the latest Linux [tar file][linux-installer] for the npm package locally.</span></span> <span data-ttu-id="aa595-123">その後、ダウンロードした npm パッケージを次のようにインストールします (Linux ディストリビューションでは **sudo**を使用しなければならないことがあります)。</span><span class="sxs-lookup"><span data-stu-id="aa595-123">Then, install the downloaded npm package as follows (on Linux distributions you might need to use **sudo**):</span></span>

```bash
npm install -g <path to downloaded tar file>
```

## <a name="option-2-use-an-installer"></a><span data-ttu-id="aa595-124">オプション 2: インストーラーの使用</span><span class="sxs-lookup"><span data-stu-id="aa595-124">Option 2: Use an installer</span></span>
<span data-ttu-id="aa595-125">Mac または Windows コンピューターを使用する場合、次の CLI インストーラーをダウンロードに使用できます。</span><span class="sxs-lookup"><span data-stu-id="aa595-125">If you use a Mac or Windows computer, the following CLI installers are available for download:</span></span>

* <span data-ttu-id="aa595-126">[Mac OS X インストーラー][mac-installer]</span><span class="sxs-lookup"><span data-stu-id="aa595-126">[Mac OS X installer][mac-installer]</span></span>
* <span data-ttu-id="aa595-127">[Windows MSI][windows-installer]</span><span class="sxs-lookup"><span data-stu-id="aa595-127">[Windows MSI][windows-installer]</span></span>

> [!TIP]
> <span data-ttu-id="aa595-128">Windows では、 [Web プラットフォーム インストーラー](https://go.microsoft.com/?linkid=9828653) をダウンロードして CLI をインストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="aa595-128">On Windows, you can also download the [Web Platform Installer](https://go.microsoft.com/?linkid=9828653) to install the CLI.</span></span> <span data-ttu-id="aa595-129">このインストーラーを使用すると、CLI をインストールした後で、その他の Azure SDK とコマンド ライン ツールをインストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="aa595-129">This installer gives you the option to install additional Azure SDK and command-line tools after installing the CLI.</span></span>

## <a name="option-3-use-a-docker-container"></a><span data-ttu-id="aa595-130">オプション 3: Docker コンテナーの使用</span><span class="sxs-lookup"><span data-stu-id="aa595-130">Option 3: Use a Docker container</span></span>
<span data-ttu-id="aa595-131">お使いのコンピューターを [Docker](https://docs.docker.com/engine/understanding-docker/) ホストとして設定すると、Docker コンテナーで最新の Azure CLI 1.0 を実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="aa595-131">If you have set up your computer as a [Docker](https://docs.docker.com/engine/understanding-docker/) host, you can run the latest Azure CLI 1.0 in a Docker container.</span></span> <span data-ttu-id="aa595-132">次のコマンドを実行します (Linux ディストリビューションの場合、**sudo** の使用が必要になる場合があります)。</span><span class="sxs-lookup"><span data-stu-id="aa595-132">Run the following command (on Linux distributions you might need to use **sudo**):</span></span>

```bash
docker run -it microsoft/azure-cli
```

## <a name="run-azure-cli-10-commands"></a><span data-ttu-id="aa595-133">Azure CLI 1.0 コマンドの実行</span><span class="sxs-lookup"><span data-stu-id="aa595-133">Run Azure CLI 1.0 commands</span></span>
<span data-ttu-id="aa595-134">Azure CLI 1.0 をインストールした後、コマンド ライン ユーザー インターフェイス (Bash、ターミナル、コマンド プロンプトなど) から **azure** コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="aa595-134">After the Azure CLI 1.0 is installed, run the **azure** command from your command-line user interface (Bash, Terminal, Command prompt, and so on).</span></span> <span data-ttu-id="aa595-135">たとえば、ヘルプ コマンドを実行するには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="aa595-135">For example, to run the help command, type the following:</span></span>

```azurecli
azure help
```

> [!NOTE]
> <span data-ttu-id="aa595-136">一部の Linux ディストリビューションでは、`/usr/bin/env: ‘node’: No such file or directory` のようなエラーが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="aa595-136">On some Linux distributions, you may receive an error similar to `/usr/bin/env: ‘node’: No such file or directory`.</span></span> <span data-ttu-id="aa595-137">このエラーは、/usr/bin/nodejs に最近インストールされた Node.js が原因で発生します。</span><span class="sxs-lookup"><span data-stu-id="aa595-137">This error comes from recent installations of Node.js being installed at /usr/bin/nodejs.</span></span> <span data-ttu-id="aa595-138">このエラーを修正するには、次のコマンドを実行して /usr/bin/node へのシンボリック リンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="aa595-138">To fix it, create a symbolic link to /usr/bin/node by running this command:</span></span>

```bash
sudo ln -s /usr/bin/nodejs /usr/bin/node
```

<span data-ttu-id="aa595-139">インストールした Azure CLI 1.0 のバージョンを確認するには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="aa595-139">To see the version of the Azure CLI 1.0 you installed, type the following:</span></span>

```azurecli
azure --version
```

<span data-ttu-id="aa595-140">これで準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="aa595-140">Now you are ready!</span></span> <span data-ttu-id="aa595-141">すべての CLI コマンドにアクセスして独自のリソースを操作するには、 [Azure CLI から Azure サブスクリプションに接続](/cli/azure/authenticate-azure-cli)します。</span><span class="sxs-lookup"><span data-stu-id="aa595-141">To access all the CLI commands to work with your own resources, [connect to your Azure subscription from the Azure CLI](/cli/azure/authenticate-azure-cli).</span></span>

> [!NOTE]
> <span data-ttu-id="aa595-142">Azure CLI を初めて使用する場合、Microsoft が使用状況についての情報を収集することを許可するかどうかをたずねるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa595-142">When you first use Azure CLI, you see a message asking if you want to allow Microsoft to collect usage information.</span></span> <span data-ttu-id="aa595-143">参加は任意です。</span><span class="sxs-lookup"><span data-stu-id="aa595-143">Participation is voluntary.</span></span> <span data-ttu-id="aa595-144">参加した後でも、 `azure telemetry --disable`を実行するといつでも停止できます。</span><span class="sxs-lookup"><span data-stu-id="aa595-144">If you choose to participate, you can stop at any time by running `azure telemetry --disable`.</span></span> <span data-ttu-id="aa595-145">参加を有効にするには、任意のタイミングで `azure telemetry --enable`を実行します。</span><span class="sxs-lookup"><span data-stu-id="aa595-145">To enable participation at any time, run `azure telemetry --enable`.</span></span>

## <a name="update-the-cli"></a><span data-ttu-id="aa595-146">CLI の更新</span><span class="sxs-lookup"><span data-stu-id="aa595-146">Update the CLI</span></span>
<span data-ttu-id="aa595-147">マイクロソフトは、Azure CLI の更新バージョンを頻繁にリリースしています。</span><span class="sxs-lookup"><span data-stu-id="aa595-147">Microsoft frequently releases updated versions of the Azure CLI.</span></span> <span data-ttu-id="aa595-148">ご使用のオペレーティング システム用のインストーラーを使用するか、最新の Docker コンテナーを実行して、CLI を再インストールします。</span><span class="sxs-lookup"><span data-stu-id="aa595-148">Reinstall the CLI using the installer for your operating system, or run the latest Docker container.</span></span> <span data-ttu-id="aa595-149">または、最新の Node.js と npm がインストールされている場合は、次のコマンドを入力して更新します (Linux ディストリビューションでは、 **sudo**の使用が必要になる場合があります)。</span><span class="sxs-lookup"><span data-stu-id="aa595-149">Or, if you have the latest Node.js and npm installed, update by typing the following (on Linux distributions you might need to use **sudo**).</span></span>

```bash
npm update -g azure-cli
```

## <a name="enable-tab-completion"></a><span data-ttu-id="aa595-150">タブ補完の有効化</span><span class="sxs-lookup"><span data-stu-id="aa595-150">Enable tab completion</span></span>
<span data-ttu-id="aa595-151">Mac と Linux では、CLI コマンドのタブ補完がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="aa595-151">Tab completion of CLI commands is supported for Mac and Linux.</span></span>

<span data-ttu-id="aa595-152">zsh で有効化する場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="aa595-152">To enable it in zsh, run:</span></span>

```bash
echo '. <(azure --completion)' >> .zshrc
```

<span data-ttu-id="aa595-153">bash で有効化する場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="aa595-153">To enable it in bash, run:</span></span>

```bash
azure --completion >> ~/azure.completion.sh
echo 'source ~/azure.completion.sh' >> ~/.bash_profile
```


## <a name="next-steps"></a><span data-ttu-id="aa595-154">次の手順</span><span class="sxs-lookup"><span data-stu-id="aa595-154">Next steps</span></span>
* <span data-ttu-id="aa595-155">[CLI から Azure サブスクリプションへの接続](/cli/azure/authenticate-azure-cli) を行い、Azure リソースを作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="aa595-155">[Connect from the CLI to your Azure subscription](/cli/azure/authenticate-azure-cli) to create and manage Azure resources.</span></span>
* <span data-ttu-id="aa595-156">Azure CLI の詳細、ソース コードのダウンロード、問題のレポート、プロジェクトへの協力については、 [GitHub リポジトリの Azure CLI](https://github.com/azure/azure-xplat-cli)のページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa595-156">To learn more about the Azure CLI, download source code, report problems, or contribute to the project, visit the [GitHub repository for the Azure CLI](https://github.com/azure/azure-xplat-cli).</span></span>
* <span data-ttu-id="aa595-157">Azure CLI または Azure の使用に関してご不明な点がある場合は、 [Azure のフォーラム](https://social.msdn.microsoft.com/Forums/en-US/home?forum=azurescripting)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="aa595-157">If you have questions about using the Azure CLI, or Azure, visit the [Azure Forums](https://social.msdn.microsoft.com/Forums/en-US/home?forum=azurescripting).</span></span>


[mac-installer]: http://aka.ms/mac-azure-cli
[windows-installer]: http://aka.ms/webpi-azure-cli
[linux-installer]: http://aka.ms/linux-azure-cli
[cliasm]: /cli/azure/get-started-with-az-cli2
[cliarm]: ./virtual-machines/azure-cli-arm-commands.md
