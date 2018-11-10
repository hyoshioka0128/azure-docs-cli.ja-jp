---
title: Azure クラシック CLI のインストール
description: Mac、Linux、および Windows に Azure クラシック CLI をインストールして Azure サービスの利用を開始する
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 06/11/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 78043f9c070626545030971dea2a8fd155ac76c2
ms.sourcegitcommit: 0d6b08048b5b35bf0bb3d7b91ff567adbaab2a8b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "51222465"
---
# <a name="install-the-azure-classic-cli"></a><span data-ttu-id="f4844-103">Azure クラシック CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="f4844-103">Install the Azure classic CLI</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4844-104">このトピックでは、Azure クラシック CLI のインストール方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f4844-104">This topic describes how to install the Azure classic CLI.</span></span> <span data-ttu-id="f4844-105">クラシック CLI は非推奨です。クラシック デプロイ モデルでのみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="f4844-105">The classic CLI is deprecated and should only be used with the classic deployment model.</span></span>
> <span data-ttu-id="f4844-106">その他すべてのデプロイについては、[Azure CLI](/cli/azure) を使用してください。</span><span class="sxs-lookup"><span data-stu-id="f4844-106">For all other deployments, use [the Azure CLI](/cli/azure).</span></span>

<span data-ttu-id="f4844-107">Azure クラシック CLI を簡単にインストールして、コマンド ライン シェルからオープン ソースのコマンドを使って Microsoft Azure 上のリソースを作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="f4844-107">Quickly install the Azure classic CLI to use a set of open-source shell-based commands for creating and managing resources in Microsoft Azure.</span></span> <span data-ttu-id="f4844-108">お使いのコンピューターにこれらのクロスプラットフォーム ツールをインストールするオプションは複数あります。</span><span class="sxs-lookup"><span data-stu-id="f4844-108">You have several options to install these cross-platform tools on your computer:</span></span>

* <span data-ttu-id="f4844-109">**npm パッケージ** - npm (JavaScript 用のパッケージ マネージャー) を実行して、Linux ディストリビューションまたは OS に Azure クラシック CLI パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="f4844-109">**npm package** - Run npm (the package manager for JavaScript) to install the Azure classic CLI package on your Linux distribution or OS.</span></span> <span data-ttu-id="f4844-110">node.js と npm が必要です。</span><span class="sxs-lookup"><span data-stu-id="f4844-110">Requires node.js and npm.</span></span>
* <span data-ttu-id="f4844-111">**インストーラー** - macOS または Windows に簡単インストールするにはインストーラーをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="f4844-111">**Installer** - Download an installer for easy installation on macOS or Windows.</span></span>
* <span data-ttu-id="f4844-112">**Docker コンテナー** - すぐに実行できる Docker コンテナーでクラシック CLI の使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="f4844-112">**Docker container** - Start using the classic CLI in a ready-to-run Docker container.</span></span> <span data-ttu-id="f4844-113">Docker ホストが必要です。</span><span class="sxs-lookup"><span data-stu-id="f4844-113">Requires a Docker host.</span></span>

<span data-ttu-id="f4844-114">その他のオプションと背景については、 [GitHub](https://github.com/azure/azure-xplat-cli)のプロジェクト リポジトリを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4844-114">For more options and background, see the project repository on [GitHub](https://github.com/azure/azure-xplat-cli).</span></span>

<span data-ttu-id="f4844-115">Azure クラシック CLI をインストールした後、`azure login` に接続し、お使いのコマンド ライン インターフェイス (Bash、ターミナル、コマンド プロンプトなど) から `azure` コマンドを実行して、Azure リソースを操作します。</span><span class="sxs-lookup"><span data-stu-id="f4844-115">Once the Azure classic CLI is installed, connect with `azure login` and run the `azure` commands from your command-line interface (Bash, Terminal, Command prompt, and so on) to work with your Azure resources.</span></span>

## <a name="option-1-install-an-npm-package"></a><span data-ttu-id="f4844-116">オプション 1: npm パッケージのインストール</span><span class="sxs-lookup"><span data-stu-id="f4844-116">Option 1: Install an npm package</span></span>

<span data-ttu-id="f4844-117">クラシック CLI を npm パッケージからインストールするには、[最新の Node.js と npm](https://nodejs.org/en/download/package-manager/) をダウンロードし、インストールしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f4844-117">To install the classic CLI from an npm package, make sure you have downloaded and installed the [latest Node.js and npm](https://nodejs.org/en/download/package-manager/).</span></span> <span data-ttu-id="f4844-118">次に、`npm install` を実行して、azure-cli パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="f4844-118">Then, run `npm install` to install the azure-cli package:</span></span>

```bash
npm install -g azure-cli
```

<span data-ttu-id="f4844-119">Linux ディストリビューションの場合、`npm` コマンドを正常に実行するには、次のように `sudo` の使用が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f4844-119">On Linux distributions, you might need to use `sudo` to successfully run the `npm` command, as follows:</span></span>

```bash
sudo npm install -g azure-cli
```

> [!NOTE]
> <span data-ttu-id="f4844-120">Node.js と npm をご自身の OS にインストールまたは更新する必要がある場合は、Node.js LTS バージョン 4.x 以降をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f4844-120">If you need to install or update Node.js and npm on your OS, we recommend that you install Node.js LTS version 4.x or later.</span></span> <span data-ttu-id="f4844-121">以前のバージョンを使用すると、インストール エラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="f4844-121">If you use an older version, you might get installation errors.</span></span>

<span data-ttu-id="f4844-122">必要に応じて、[GitHub リリース](https://github.com/Azure/azure-xplat-cli/releases)から tar ファイルをダウンロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f4844-122">If you prefer, you may also download a tar file from the [GitHub releases](https://github.com/Azure/azure-xplat-cli/releases).</span></span> <span data-ttu-id="f4844-123">その後、ダウンロードした npm パッケージを次のようにインストールします (Linux ディストリビューションでは `sudo` を使用しなければならないことがあります)。</span><span class="sxs-lookup"><span data-stu-id="f4844-123">Then, install the downloaded npm package as follows (on Linux distributions you might need to use `sudo`):</span></span>

```bash
npm install -g <path to downloaded tar file>
```

## <a name="option-2-use-an-installer"></a><span data-ttu-id="f4844-124">オプション 2: インストーラーの使用</span><span class="sxs-lookup"><span data-stu-id="f4844-124">Option 2: Use an installer</span></span>

<span data-ttu-id="f4844-125">Mac または Windows コンピューターを使用している場合は、[GitHub リリース](https://github.com/Azure/azure-xplat-cli/releases)から DMG および MSI インストーラーを入手できます。</span><span class="sxs-lookup"><span data-stu-id="f4844-125">If you use a Mac or Windows computer, DMG and MSI installers are available from [GitHub releases](https://github.com/Azure/azure-xplat-cli/releases).</span></span>

> [!TIP]
> <span data-ttu-id="f4844-126">Windows では、[Web Platform Installer](https://go.microsoft.com/?linkid=9828653) をダウンロードして、クラシック CLI をインストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f4844-126">On Windows, you can also download the [Web Platform Installer](https://go.microsoft.com/?linkid=9828653) to install the classic CLI.</span></span> <span data-ttu-id="f4844-127">このインストーラーを使用すると、その他の Azure SDK とコマンドライン ツールをインストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f4844-127">This installer gives you the option to install additional Azure SDK and command-line tools.</span></span>

## <a name="option-3-use-a-docker-container"></a><span data-ttu-id="f4844-128">オプション 3: Docker コンテナーの使用</span><span class="sxs-lookup"><span data-stu-id="f4844-128">Option 3: Use a Docker container</span></span>

<span data-ttu-id="f4844-129">お使いのコンピューターを [Docker](https://docs.docker.com/engine/understanding-docker/) ホストとして設定すると、Docker コンテナーで Azure クラシック CLI を実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="f4844-129">If you have set up your computer as a [Docker](https://docs.docker.com/engine/understanding-docker/) host, you can run the Azure classic CLI in a Docker container.</span></span> <span data-ttu-id="f4844-130">次のコマンドを実行します (Linux ディストリビューションの場合、`sudo` の使用が必要になる場合があります)。</span><span class="sxs-lookup"><span data-stu-id="f4844-130">Run the following command (on Linux distributions you might need to use `sudo`):</span></span>

```bash
docker run -it microsoft/azure-cli:0.10.17
```

## <a name="run-azure-classic-cli-commands"></a><span data-ttu-id="f4844-131">Azure クラシック CLI コマンドの実行</span><span class="sxs-lookup"><span data-stu-id="f4844-131">Run Azure classic CLI commands</span></span>

<span data-ttu-id="f4844-132">クラシック CLI をインストールした後、コマンド ライン ユーザー インターフェイス (Bash、ターミナル、コマンド プロンプトなど) から `azure` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f4844-132">After the classic CLI is installed, run the `azure` command from your command-line user interface (Bash, Terminal, Command prompt, and so on).</span></span> <span data-ttu-id="f4844-133">たとえば、ヘルプ コマンドを実行するには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="f4844-133">For example, to run the help command, type the following:</span></span>

```azurecli-interactive
azure help
```

> [!NOTE]
> <span data-ttu-id="f4844-134">一部の Linux ディストリビューションでは、`/usr/bin/env: ‘node’: No such file or directory` のようなエラーが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="f4844-134">On some Linux distributions, you may receive an error similar to `/usr/bin/env: ‘node’: No such file or directory`.</span></span> <span data-ttu-id="f4844-135">このエラーは、/usr/bin/nodejs に最近インストールされた Node.js が原因で発生します。</span><span class="sxs-lookup"><span data-stu-id="f4844-135">This error comes from recent installations of Node.js being installed at /usr/bin/nodejs.</span></span> <span data-ttu-id="f4844-136">このエラーを修正するには、次のコマンドを実行して /usr/bin/node へのシンボリック リンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="f4844-136">To fix it, create a symbolic link to /usr/bin/node by running this command:</span></span>

```bash
sudo ln -s /usr/bin/nodejs /usr/bin/node
```

<span data-ttu-id="f4844-137">インストールした Azure クラシック CLI のバージョンを確認するには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="f4844-137">To see the version of the Azure classic CLI installed, type the following:</span></span>

```azurecli-interactive
azure --version
```

> [!NOTE]
> <span data-ttu-id="f4844-138">Azure クラシック CLI を初めて使用する場合、Microsoft が使用状況についての情報を収集することを許可するかどうかをたずねるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4844-138">When you first use Azure classic CLI, you see a message asking if you want to allow Microsoft to collect usage information.</span></span> <span data-ttu-id="f4844-139">参加は任意です。</span><span class="sxs-lookup"><span data-stu-id="f4844-139">Participation is voluntary.</span></span> <span data-ttu-id="f4844-140">参加した後でも、 `azure telemetry --disable`を実行するといつでも停止できます。</span><span class="sxs-lookup"><span data-stu-id="f4844-140">If you choose to participate, you can stop at any time by running `azure telemetry --disable`.</span></span> <span data-ttu-id="f4844-141">参加を有効にするには、任意のタイミングで `azure telemetry --enable`を実行します。</span><span class="sxs-lookup"><span data-stu-id="f4844-141">To enable participation at any time, run `azure telemetry --enable`.</span></span>

## <a name="update-the-classic-cli"></a><span data-ttu-id="f4844-142">クラシック CLI の更新</span><span class="sxs-lookup"><span data-stu-id="f4844-142">Update the classic CLI</span></span>

<span data-ttu-id="f4844-143">Microsoft は、Azure クラシック CLI の更新バージョンをリリースする場合があります。</span><span class="sxs-lookup"><span data-stu-id="f4844-143">Microsoft may release updated versions of the Azure classic CLI.</span></span> <span data-ttu-id="f4844-144">ご利用のオペレーティング システム用のインストーラーを使用するか、最新の Docker コンテナーを実行して、クラシック CLI を再インストールします。</span><span class="sxs-lookup"><span data-stu-id="f4844-144">Reinstall the classic CLI using the installer for your operating system, or run the latest Docker container.</span></span> <span data-ttu-id="f4844-145">または、最新の Node.js と npm がインストールされている場合は、次のコマンドを入力して更新します (Linux ディストリビューションでは、`sudo` の使用が必要になる場合があります)。</span><span class="sxs-lookup"><span data-stu-id="f4844-145">Or, if you have the latest Node.js and npm installed, update by typing the following (on Linux distributions you might need to use `sudo`).</span></span>

```bash
npm update -g azure-cli
```

## <a name="enable-tab-completion"></a><span data-ttu-id="f4844-146">タブ補完の有効化</span><span class="sxs-lookup"><span data-stu-id="f4844-146">Enable tab completion</span></span>

<span data-ttu-id="f4844-147">Mac と Linux では、クラシック CLI コマンドのタブ補完がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f4844-147">Tab completion of classic CLI commands is supported for Mac and Linux.</span></span>

<span data-ttu-id="f4844-148">zsh で有効化する場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f4844-148">To enable it in zsh, run:</span></span>

```bash
echo '. <(azure --completion)' >> .zshrc
```

<span data-ttu-id="f4844-149">bash で有効化する場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f4844-149">To enable it in bash, run:</span></span>

```bash
azure --completion >> ~/azure.completion.sh
echo 'source ~/azure.completion.sh' >> ~/.bash_profile
```

## <a name="next-steps"></a><span data-ttu-id="f4844-150">次の手順</span><span class="sxs-lookup"><span data-stu-id="f4844-150">Next steps</span></span>

* <span data-ttu-id="f4844-151">Azure クラシック CLI の詳細、ソース コードのダウンロード、問題のレポート、プロジェクトへの協力については、[Azure クラシック CLI 用の GitHub リポジトリ](https://github.com/azure/azure-xplat-cli)のページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4844-151">To learn more about the Azure classic CLI, download source code, report problems, or contribute to the project, visit the [GitHub repository for the Azure classic CLI](https://github.com/azure/azure-xplat-cli).</span></span>
