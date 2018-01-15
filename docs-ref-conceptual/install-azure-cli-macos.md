---
title: "macOS での Azure CLI のインストール"
description: "macOS で Azure CLI 2.0 をインストールする方法"
keywords: "Azure CLI,Azure CLI のインストール,azure macos, azure インストール macos"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 10/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e615d2b3ab3b1307e982cb1d4d456633440afdf6
ms.sourcegitcommit: 3eef136ae752eb90c67af604d4ddd298d70b1c9d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/06/2018
---
# <a name="install-azure-cli-20-on-macos"></a><span data-ttu-id="f76cc-104">macOS での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="f76cc-104">Install Azure CLI 2.0 on macOS</span></span>

<span data-ttu-id="f76cc-105">macOS プラットフォームについては、[Homebrew パッケージ マネージャー](http://brew.sh)または手動のいずれかで、Azure CLI をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="f76cc-105">For the macOS platform, you can install the Azure CLI either through the [homebrew package manager](http://brew.sh) or manually.</span></span> <span data-ttu-id="f76cc-106">Homebrew を使用したインストール方法をお勧めします。こちらの方がインストール、更新プログラムの取得、およびアンインストール (必要な場合) が容易です。</span><span class="sxs-lookup"><span data-stu-id="f76cc-106">The preferred installation method is through homebrew, so that it's easier to install, get updates, and uninstall if you need to.</span></span>

## <a name="use-homebrew-to-install"></a><span data-ttu-id="f76cc-107">Homebrew を使用したインストール</span><span class="sxs-lookup"><span data-stu-id="f76cc-107">Use homebrew to install</span></span>

<span data-ttu-id="f76cc-108">CLI インストールを管理する方法としては、Homebrew を使用するのが最も簡単です。</span><span class="sxs-lookup"><span data-stu-id="f76cc-108">Homebrew is the easiest way to manage your CLI install.</span></span> <span data-ttu-id="f76cc-109">これには、便利なインストール、更新、およびアンインストール手段が用意されています。</span><span class="sxs-lookup"><span data-stu-id="f76cc-109">It provides convenient ways to install, update, and uninstall.</span></span> <span data-ttu-id="f76cc-110">これは、`apt` や`yum` などの他のパッケージ マネージャーと似ています。</span><span class="sxs-lookup"><span data-stu-id="f76cc-110">It's similar to other package managers such as `apt` or `yum`.</span></span>
<span data-ttu-id="f76cc-111">システムで使用できる Homebrew がない場合は、[Homebrew をインストール](https://docs.brew.sh/Installation.html)してから操作を続行します。</span><span class="sxs-lookup"><span data-stu-id="f76cc-111">If you don't have homebrew available on your system, [install homebrew](https://docs.brew.sh/Installation.html) before continuing.</span></span>

### <a name="install-with-homebrew"></a><span data-ttu-id="f76cc-112">Homebrew でのインストール</span><span class="sxs-lookup"><span data-stu-id="f76cc-112">Install with homebrew</span></span>

<span data-ttu-id="f76cc-113">CLI をインストールするには、brew リポジトリ情報を更新し、`install` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f76cc-113">You can install the CLI by updating your brew repository information, and then running the `install` command:</span></span>

```bash
brew update && brew install azure-cli
```

<span data-ttu-id="f76cc-114">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="f76cc-114">You can then run the Azure CLI with the `az` command.</span></span>

### <a name="update-with-homebrew"></a><span data-ttu-id="f76cc-115">Homebrew での更新</span><span class="sxs-lookup"><span data-stu-id="f76cc-115">Update with homebrew</span></span>

<span data-ttu-id="f76cc-116">CLI は、バグの修正、機能強化、新機能、およびプレビュー機能で定期的に更新されています。</span><span class="sxs-lookup"><span data-stu-id="f76cc-116">The CLI is regularly updated with bug fixes, improvements, new features, and preview functionality.</span></span> <span data-ttu-id="f76cc-117">新しいリリースは約 2 週間ごとに入手できます。</span><span class="sxs-lookup"><span data-stu-id="f76cc-117">A new release is available roughly every two weeks.</span></span> <span data-ttu-id="f76cc-118">ローカル リポジトリ情報を更新してから、CLI パッケージを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f76cc-118">You will need to update your local repository information, and then update the CLI package.</span></span>

```bash
brew update && brew upgrade azure-cli
```

### <a name="troubleshooting"></a><span data-ttu-id="f76cc-119">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="f76cc-119">Troubleshooting</span></span>

<span data-ttu-id="f76cc-120">Homebrew での CLI のインストールまたは更新時に問題が発生しましたか。</span><span class="sxs-lookup"><span data-stu-id="f76cc-120">Did you encounter a problem when installing or updating the CLI with homebrew?</span></span> <span data-ttu-id="f76cc-121">ここでは、発生する可能性のある一般的なエラーをいくつか取り上げ、そのエラーを診断および解決する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f76cc-121">Here are some common errors that might occur, and ways to diagnose and resolve them.</span></span>

#### <a name="unable-to-find-python-or-installed-packages"></a><span data-ttu-id="f76cc-122">Python またはインストールされているパッケージが見つかりません</span><span class="sxs-lookup"><span data-stu-id="f76cc-122">Unable to find Python or installed packages</span></span>

<span data-ttu-id="f76cc-123">インストール時に Python またはインストールされているパッケージが見つからない場合、マイナー バージョンの不一致があるか、Homebrew のインストール中に別の問題が発生した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f76cc-123">If your install is unable to find Python or installed packages, there may be a minor version mismatch or other issue which occurred during homebrew installation.</span></span> <span data-ttu-id="f76cc-124">CLI は Virtualenv を使用しないため、Homebrew によってインストールされた正しいバージョンの Python を検索できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f76cc-124">Since the CLI does not use a virtualenv, it relies on being able to find correct versions of Python installed by homebrew.</span></span> <span data-ttu-id="f76cc-125">この問題を修正するには、Python インストールを再リンクします。</span><span class="sxs-lookup"><span data-stu-id="f76cc-125">You may be able to fix these issues by re-linking your Python installation:</span></span>

```bash
brew link --overwrite python3
```

#### <a name="the-cli-version-is-out-of-date"></a><span data-ttu-id="f76cc-126">CLI バージョンが古すぎます</span><span class="sxs-lookup"><span data-stu-id="f76cc-126">The CLI version is out of date</span></span>

<span data-ttu-id="f76cc-127">インストールされている CLI バージョンが古くなっていると思われる場合は、`brew update` コマンドを実行し、その後に `brew upgrade azure-cli` を実行します。</span><span class="sxs-lookup"><span data-stu-id="f76cc-127">If you think that your installed CLI version might be out of date, you will need to run a `brew update` command, followed by `brew upgrade azure-cli`.</span></span> <span data-ttu-id="f76cc-128">これで CLI が更新されない場合は、Homebrew パッケージのロールアウトが、一般公開リリースよりも時間がかかっている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f76cc-128">If this does not update the CLI, be aware that homebrew packages may roll out more slowly than general releases.</span></span> <span data-ttu-id="f76cc-129">最新の CLI インストールが必要な場合は、[手動でインストール](#manage-the-cli-manually)してください。</span><span class="sxs-lookup"><span data-stu-id="f76cc-129">If you require bleeding-edge installs of the CLI, then you should [install manually](#manage-the-cli-manually).</span></span>

### <a name="uninstall-with-homebrew"></a><span data-ttu-id="f76cc-130">Homebrew でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="f76cc-130">Uninstall with homebrew</span></span>

<span data-ttu-id="f76cc-131">Azure CLI が不要であると判断した場合は、アンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="f76cc-131">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="f76cc-132">アンインストールする前に、`az feedback` コマンドを使用して、アンインストールの理由と、CLI エクスペリエンスの改善方法について、ご意見をお聞かせください。</span><span class="sxs-lookup"><span data-stu-id="f76cc-132">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="f76cc-133">Microsoft では、できる限り Azure CLI のバグをなくし、使いやすいものにしたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="f76cc-133">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="f76cc-134">また、[GitHub に問題を提出](https://github.com/Azure/azure-cli/issues)していただくこともできます。</span><span class="sxs-lookup"><span data-stu-id="f76cc-134">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

<span data-ttu-id="f76cc-135">Homebrew でインストールした場合は、アンインストールにも、それを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f76cc-135">If you installed with homebrew, you should also use it to uninstall.</span></span>

```bash
brew uninstall azure-cli
```

## <a name="install-the-cli-manually"></a><span data-ttu-id="f76cc-136">CLI の手動インストール</span><span class="sxs-lookup"><span data-stu-id="f76cc-136">Install the CLI manually</span></span>

<span data-ttu-id="f76cc-137">CLI インストールの管理に Homebrew を使用できない、または使用したくない場合は、手動でインストールできます。</span><span class="sxs-lookup"><span data-stu-id="f76cc-137">If you can't or don't want to rely on homebrew to manage the CLI install for you, then you can manually install.</span></span>

<span data-ttu-id="f76cc-138">[手動による Linux インストール手順](install-azure-cli-linux.md)に従って、macOS に手動でインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="f76cc-138">Follow the [manual Linux installation instructions](install-azure-cli-linux.md) to install manually on macOS.</span></span> <span data-ttu-id="f76cc-139">macOS 10.9 バージョン以降には、必要な依存関係がすべて含まれています。</span><span class="sxs-lookup"><span data-stu-id="f76cc-139">macOS versions 10.9 and later should include all of the required dependencies.</span></span>
