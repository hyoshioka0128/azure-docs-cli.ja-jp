---
title: macOS での Azure CLI のインストール
description: macOS で Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 11/05/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: a79e5445654a9f339321db18b54e558aa598e19b
ms.sourcegitcommit: 0d6b08048b5b35bf0bb3d7b91ff567adbaab2a8b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "51222261"
---
# <a name="install-azure-cli-on-macos"></a><span data-ttu-id="ca0c5-103">macOS での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="ca0c5-103">Install Azure CLI on macOS</span></span>

<span data-ttu-id="ca0c5-104">macOS プラットフォームの場合は、[Homebrew パッケージ マネージャー](https://brew.sh)で Azure CLI をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-104">For the macOS platform, you can install the Azure CLI with [homebrew package manager](https://brew.sh).</span></span> <span data-ttu-id="ca0c5-105">Homebrew を使用すると、CLI のインストールを最新の状態に保つことが容易になります。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-105">Homebrew makes it easy to keep your installation of the CLI update to date.</span></span> <span data-ttu-id="ca0c5-106">CLI パッケージは、macOS バージョン 10.9 以降でテストされています。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-106">The CLI package has been tested on macOS versions 10.9 and later.</span></span>

## <a name="install"></a><span data-ttu-id="ca0c5-107">Install</span><span class="sxs-lookup"><span data-stu-id="ca0c5-107">Install</span></span>

<span data-ttu-id="ca0c5-108">CLI インストールを管理する方法としては、Homebrew を使用するのが最も簡単です。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-108">Homebrew is the easiest way to manage your CLI install.</span></span> <span data-ttu-id="ca0c5-109">これには、便利なインストール、更新、およびアンインストール手段が用意されています。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-109">It provides convenient ways to install, update, and uninstall.</span></span>
<span data-ttu-id="ca0c5-110">システムで使用できる Homebrew がない場合は、[Homebrew をインストール](https://docs.brew.sh/Installation.html)してから操作を続行します。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-110">If you don't have homebrew available on your system, [install homebrew](https://docs.brew.sh/Installation.html) before continuing.</span></span>

<span data-ttu-id="ca0c5-111">CLI をインストールするには、brew リポジトリ情報を更新し、`install` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-111">You can install the CLI by updating your brew repository information, and then running the `install` command:</span></span>

```bash
brew update && brew install azure-cli
```

<span data-ttu-id="ca0c5-112">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-112">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="ca0c5-113">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-113">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="ca0c5-114">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-114">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ca0c5-115">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="ca0c5-115">Troubleshooting</span></span>

<span data-ttu-id="ca0c5-116">Homebrew を使用した CLI のインストール時に問題が発生した場合、一般的なエラーを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-116">If you encounter a problem when installing the CLI through Homebrew, here are some common errors.</span></span> <span data-ttu-id="ca0c5-117">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-117">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="unable-to-find-python-or-installed-packages"></a><span data-ttu-id="ca0c5-118">Python またはインストールされているパッケージが見つかりません</span><span class="sxs-lookup"><span data-stu-id="ca0c5-118">Unable to find Python or installed packages</span></span>

<span data-ttu-id="ca0c5-119">Homebrew のインストール中に、マイナー バージョンの不一致またはその他の問題が発生した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-119">There may be a minor version mismatch or other issue during homebrew installation.</span></span> <span data-ttu-id="ca0c5-120">CLI では Python 仮想環境を使用しないため、インストールされている Python バージョンを見つけることができる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-120">The CLI doesn't use a Python virtual environment, so it relies on finding the installed Python version.</span></span> <span data-ttu-id="ca0c5-121">考えられる修正案は、Homebrew から `python3` の依存関係をインストールして再リンクすることです。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-121">A possible fix is to install and relink the `python3` dependency from Homebrew.</span></span>

```bash
brew update && brew install python3 && brew upgrade python3
brew link --overwrite python3
```

### <a name="cli-version-1x-is-installed"></a><span data-ttu-id="ca0c5-122">CLI バージョン 1.x がインストールされている</span><span class="sxs-lookup"><span data-stu-id="ca0c5-122">CLI version 1.x is installed</span></span>

<span data-ttu-id="ca0c5-123">古いバージョンがインストールされている場合は、Homebrew の古いキャッシュが原因と考えられます。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-123">If an out-of-date version was installed, it could be because of a stale homebrew cache.</span></span> <span data-ttu-id="ca0c5-124">[更新](#Update)の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-124">Follow the [update](#Update) instructions.</span></span>

## <a name="update"></a><span data-ttu-id="ca0c5-125">アップデート</span><span class="sxs-lookup"><span data-stu-id="ca0c5-125">Update</span></span>

<span data-ttu-id="ca0c5-126">CLI は、バグの修正、機能強化、新機能、およびプレビュー機能で定期的に更新されています。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-126">The CLI is regularly updated with bug fixes, improvements, new features, and preview functionality.</span></span> <span data-ttu-id="ca0c5-127">新しいリリースは約 2 週間ごとに入手できます。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-127">A new release is available roughly every two weeks.</span></span> <span data-ttu-id="ca0c5-128">ローカル リポジトリ情報を更新してから、`azure-cli` パッケージをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-128">Update your local repository information and then upgrade the `azure-cli` package.</span></span>

```bash
brew update && brew upgrade azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="ca0c5-129">アンインストール</span><span class="sxs-lookup"><span data-stu-id="ca0c5-129">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="ca0c5-130">Homebrew を使用して、`azure-cli` パッケージをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-130">Use homebrew to uninstall the `azure-cli` package.</span></span>

```bash
brew uninstall azure-cli
```

## <a name="other-installation-methods"></a><span data-ttu-id="ca0c5-131">その他のインストール方法</span><span class="sxs-lookup"><span data-stu-id="ca0c5-131">Other installation methods</span></span>

<span data-ttu-id="ca0c5-132">Homebrew を使用して環境に Azure CLI をインストールできない場合は、Linux の手動手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-132">If you can't use homebrew to install the Azure CLI in your environment, it's possible to use the manual instructions for Linux.</span></span> <span data-ttu-id="ca0c5-133">正式には、このプロセスは macOS との互換性が維持されていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-133">Note that this process is not officially maintained to be compatible with macOS.</span></span> <span data-ttu-id="ca0c5-134">Homebrew などのパッケージ マネージャーを使用することを常にお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-134">Using a package manager such as Homebrew is always recommended.</span></span> <span data-ttu-id="ca0c5-135">他の選択肢を利用できない場合のみ、手動によるインストール方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-135">Only use the manual installation method if you have no other option available.</span></span>

<span data-ttu-id="ca0c5-136">手動インストールの手順については、「[Linux での Azure CLI の手動インストール](install-azure-cli-linux.md)」参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-136">For the manual installation instructions, see [Install Azure CLI on Linux manually](install-azure-cli-linux.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="ca0c5-137">次の手順</span><span class="sxs-lookup"><span data-stu-id="ca0c5-137">Next Steps</span></span>

<span data-ttu-id="ca0c5-138">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="ca0c5-138">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="ca0c5-139">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="ca0c5-139">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
