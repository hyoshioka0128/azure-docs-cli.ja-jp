---
title: macOS での Azure CLI のインストール
description: macOS で Azure CLI 2.0 をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 01/29/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: e8190ba91006bd6d83eb0ef90b492ee7df4dda4c
ms.sourcegitcommit: 308f9eb433a05b814999ac404f63d181169fffeb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2018
ms.locfileid: "37439909"
---
# <a name="install-azure-cli-20-on-macos"></a><span data-ttu-id="1a84b-103">macOS での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="1a84b-103">Install Azure CLI 2.0 on macOS</span></span>

<span data-ttu-id="1a84b-104">macOS プラットフォームの場合は、[Homebrew パッケージ マネージャー](http://brew.sh)で Azure CLI をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="1a84b-104">For the macOS platform, you can install the Azure CLI with [homebrew package manager](http://brew.sh).</span></span> <span data-ttu-id="1a84b-105">Homebrew を使用すると、CLI のインストールを最新の状態に保つことが容易になります。</span><span class="sxs-lookup"><span data-stu-id="1a84b-105">Homebrew makes it easy to keep your installation of the CLI update to date.</span></span> <span data-ttu-id="1a84b-106">CLI パッケージは、macOS バージョン 10.9 以降でテストされています。</span><span class="sxs-lookup"><span data-stu-id="1a84b-106">The CLI package has been tested on macOS versions 10.9 and later.</span></span>

## <a name="install"></a><span data-ttu-id="1a84b-107">Install</span><span class="sxs-lookup"><span data-stu-id="1a84b-107">Install</span></span>

<span data-ttu-id="1a84b-108">CLI インストールを管理する方法としては、Homebrew を使用するのが最も簡単です。</span><span class="sxs-lookup"><span data-stu-id="1a84b-108">Homebrew is the easiest way to manage your CLI install.</span></span> <span data-ttu-id="1a84b-109">これには、便利なインストール、更新、およびアンインストール手段が用意されています。</span><span class="sxs-lookup"><span data-stu-id="1a84b-109">It provides convenient ways to install, update, and uninstall.</span></span>
<span data-ttu-id="1a84b-110">システムで使用できる Homebrew がない場合は、[Homebrew をインストール](https://docs.brew.sh/Installation.html)してから操作を続行します。</span><span class="sxs-lookup"><span data-stu-id="1a84b-110">If you don't have homebrew available on your system, [install homebrew](https://docs.brew.sh/Installation.html) before continuing.</span></span>

<span data-ttu-id="1a84b-111">CLI をインストールするには、brew リポジトリ情報を更新し、`install` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1a84b-111">You can install the CLI by updating your brew repository information, and then running the `install` command:</span></span>

```bash
brew update && brew install azure-cli
```

<span data-ttu-id="1a84b-112">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="1a84b-112">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="1a84b-113">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="1a84b-113">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="1a84b-114">さまざまなログイン方法の詳細については、「[Azure CLI 2.0 を使用してログインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1a84b-114">To learn more about different login methods, see [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="1a84b-115">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="1a84b-115">Troubleshooting</span></span>

<span data-ttu-id="1a84b-116">Homebrew を使用した CLI のインストール時に問題が発生した場合、一般的なエラーを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="1a84b-116">If you encounter a problem when installing the CLI through Homebrew, here are some common errors.</span></span> <span data-ttu-id="1a84b-117">問題がここに示されていない場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="1a84b-117">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="unable-to-find-python-or-installed-packages"></a><span data-ttu-id="1a84b-118">Python またはインストールされているパッケージが見つかりません</span><span class="sxs-lookup"><span data-stu-id="1a84b-118">Unable to find Python or installed packages</span></span>

<span data-ttu-id="1a84b-119">インストール時に Python またはインストールされているパッケージが見つからない場合、マイナー バージョンの不一致があるか、Homebrew のインストール中に別の問題が発生した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1a84b-119">If your install is unable to find Python or installed packages, there may be a minor version mismatch or other issue that occurred during homebrew installation.</span></span> <span data-ttu-id="1a84b-120">CLI では Python 仮想環境を使用しないため、適切な Python バージョンを見つけることができる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a84b-120">Since the CLI does not use a Python virtual environment, it relies on being able to find correct Python version.</span></span> <span data-ttu-id="1a84b-121">Python インストールを再リンクすることで、これらの問題を解決できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1a84b-121">You may be able to fix these issues by relinking your Python installation.</span></span>

```bash
brew link --overwrite python3
```

### <a name="cli-version-1x-is-installed"></a><span data-ttu-id="1a84b-122">CLI バージョン 1.x がインストールされている</span><span class="sxs-lookup"><span data-stu-id="1a84b-122">CLI version 1.x is installed</span></span>

<span data-ttu-id="1a84b-123">古いバージョンがインストールされている場合は、Homebrew の古いキャッシュが原因と考えられます。</span><span class="sxs-lookup"><span data-stu-id="1a84b-123">If an out-of-date version was installed, it could be due to a stale homebrew cache.</span></span> <span data-ttu-id="1a84b-124">[更新](#Update)の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="1a84b-124">Follow the [update](#Update) instructions.</span></span>

## <a name="update"></a><span data-ttu-id="1a84b-125">アップデート</span><span class="sxs-lookup"><span data-stu-id="1a84b-125">Update</span></span>

<span data-ttu-id="1a84b-126">CLI は、バグの修正、機能強化、新機能、およびプレビュー機能で定期的に更新されています。</span><span class="sxs-lookup"><span data-stu-id="1a84b-126">The CLI is regularly updated with bug fixes, improvements, new features, and preview functionality.</span></span> <span data-ttu-id="1a84b-127">新しいリリースは約 2 週間ごとに入手できます。</span><span class="sxs-lookup"><span data-stu-id="1a84b-127">A new release is available roughly every two weeks.</span></span> <span data-ttu-id="1a84b-128">ローカル リポジトリ情報を更新してから、`azure-cli` パッケージをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="1a84b-128">Update your local repository information and then upgrade the `azure-cli` package.</span></span>

```bash
brew update && brew upgrade azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="1a84b-129">アンインストール</span><span class="sxs-lookup"><span data-stu-id="1a84b-129">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="1a84b-130">Homebrew を使用して、`azure-cli` パッケージをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="1a84b-130">Use homebrew to uninstall the `azure-cli` package.</span></span>

```bash
brew uninstall azure-cli
```
