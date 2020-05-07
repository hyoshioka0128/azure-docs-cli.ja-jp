---
title: macOS での Azure CLI のインストール
description: macOS で Azure CLI をインストールする方法
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 11/05/2018
ms.topic: conceptual
ms.service: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 862ebf9144d7e81be6dda550eba108198f38d397
ms.sourcegitcommit: ee64dc738cfe689a2a479e32a87bf420f96c31c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2020
ms.locfileid: "77780096"
---
# <a name="install-azure-cli-on-macos"></a><span data-ttu-id="ff0c4-103">macOS での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="ff0c4-103">Install Azure CLI on macOS</span></span>

<span data-ttu-id="ff0c4-104">macOS プラットフォームの場合は、[Homebrew パッケージ マネージャー](https://brew.sh)で Azure CLI をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-104">For the macOS platform, you can install the Azure CLI with [homebrew package manager](https://brew.sh).</span></span> <span data-ttu-id="ff0c4-105">Homebrew を使用すると、CLI のインストールを最新の状態に保つことが容易になります。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-105">Homebrew makes it easy to keep your installation of the CLI update to date.</span></span> <span data-ttu-id="ff0c4-106">CLI パッケージは、macOS バージョン 10.9 以降でテストされています。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-106">The CLI package has been tested on macOS versions 10.9 and later.</span></span>

[!INCLUDE [current-version](includes/current-version.md)]

## <a name="install-with-homebrew"></a><span data-ttu-id="ff0c4-107">Homebrew でインストールする</span><span class="sxs-lookup"><span data-stu-id="ff0c4-107">Install with Homebrew</span></span>

<span data-ttu-id="ff0c4-108">CLI インストールを管理する方法としては、Homebrew を使用するのが最も簡単です。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-108">Homebrew is the easiest way to manage your CLI install.</span></span> <span data-ttu-id="ff0c4-109">これには、便利なインストール、更新、およびアンインストール手段が用意されています。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-109">It provides convenient ways to install, update, and uninstall.</span></span>
<span data-ttu-id="ff0c4-110">システムで使用できる Homebrew がない場合は、[Homebrew をインストール](https://docs.brew.sh/Installation.html)してから操作を続行します。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-110">If you don't have homebrew available on your system, [install homebrew](https://docs.brew.sh/Installation.html) before continuing.</span></span>

<span data-ttu-id="ff0c4-111">CLI をインストールするには、brew リポジトリ情報を更新し、`install` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-111">You can install the CLI by updating your brew repository information, and then running the `install` command:</span></span>

```bash
brew update && brew install azure-cli
```

> [!IMPORTANT]
>
> <span data-ttu-id="ff0c4-112">Azure CLI は Homebrew の `python3` パッケージに依存しているため、これをインストールします。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-112">The Azure CLI has a dependency on the Homebrew `python3` package, and will install it.</span></span>
> <span data-ttu-id="ff0c4-113">Azure CLI は、Homebrew で公開される `python3` の最新バージョンと互換性があることが保証されています。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-113">The Azure CLI is guaranteed to be compatible with the latest version of `python3` published on Homebrew.</span></span>

<span data-ttu-id="ff0c4-114">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-114">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="ff0c4-115">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-115">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="ff0c4-116">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-116">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ff0c4-117">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="ff0c4-117">Troubleshooting</span></span>

<span data-ttu-id="ff0c4-118">Homebrew を使用した CLI のインストール時に問題が発生した場合、一般的なエラーを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-118">If you encounter a problem when installing the CLI through Homebrew, here are some common errors.</span></span> <span data-ttu-id="ff0c4-119">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-119">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="completion-is-not-working"></a><span data-ttu-id="ff0c4-120">補完が機能していません</span><span class="sxs-lookup"><span data-stu-id="ff0c4-120">Completion is not working</span></span>

<span data-ttu-id="ff0c4-121">Azure CLI の Homebrew formula では、Homebrew によって管理される補完ディレクトリ (既定の場所は `az`) に `/usr/local/etc/bash_completion.d/` という名前の補完ファイルがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-121">The Homebrew formula of Azure CLI installs a completion file named `az` in the Homebrew-managed completions directory (default location is `/usr/local/etc/bash_completion.d/`).</span></span> <span data-ttu-id="ff0c4-122">補完を有効にするには、Homebrew の指示 ([ここ](https://docs.brew.sh/Shell-Completion)) に従ってしてください。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-122">To enable completion, please follow Homebrew's instructions [here](https://docs.brew.sh/Shell-Completion).</span></span>

### <a name="unable-to-find-python-or-installed-packages"></a><span data-ttu-id="ff0c4-123">Python またはインストールされているパッケージが見つかりません</span><span class="sxs-lookup"><span data-stu-id="ff0c4-123">Unable to find Python or installed packages</span></span>

<span data-ttu-id="ff0c4-124">Homebrew のインストール中に、マイナー バージョンの不一致またはその他の問題が発生した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-124">There may be a minor version mismatch or other issue during homebrew installation.</span></span> <span data-ttu-id="ff0c4-125">CLI では Python 仮想環境を使用しないため、インストールされている Python バージョンを見つけることができる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-125">The CLI doesn't use a Python virtual environment, so it relies on finding the installed Python version.</span></span> <span data-ttu-id="ff0c4-126">考えられる修正案は、Homebrew から `python3` の依存関係をインストールして再リンクすることです。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-126">A possible fix is to install and relink the `python3` dependency from Homebrew.</span></span>

```bash
brew update && brew install python3 && brew upgrade python3
brew link --overwrite python3
```

### <a name="cli-version-1x-is-installed"></a><span data-ttu-id="ff0c4-127">CLI バージョン 1.x がインストールされている</span><span class="sxs-lookup"><span data-stu-id="ff0c4-127">CLI version 1.x is installed</span></span>

<span data-ttu-id="ff0c4-128">古いバージョンがインストールされている場合は、Homebrew の古いキャッシュが原因と考えられます。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-128">If an out-of-date version was installed, it could be because of a stale homebrew cache.</span></span> <span data-ttu-id="ff0c4-129">[更新](#update)の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-129">Follow the [update](#update) instructions.</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="ff0c4-130">プロキシによる接続のブロック</span><span class="sxs-lookup"><span data-stu-id="ff0c4-130">Proxy blocks connection</span></span>

<span data-ttu-id="ff0c4-131">お使いのプロキシを使用するように適切に構成しない限り、Homebrew からリソースを取得することができない場合があります。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-131">You may be unable to get resources from Homebrew unless you have correctly configured it to use your proxy.</span></span> <span data-ttu-id="ff0c4-132">[Homebrew プロキシの構成手順](https://docs.brew.sh/Manpage#using-homebrew-behind-a-proxy)に従ってください。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-132">Follow the [Homebrew proxy configuration instructions](https://docs.brew.sh/Manpage#using-homebrew-behind-a-proxy).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff0c4-133">プロキシの内側にいる場合は、CLI によって Azure サービスに接続するように `HTTP_PROXY` と `HTTPS_PROXY` を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-133">If you are behind a proxy, `HTTP_PROXY` and `HTTPS_PROXY` must be set to connect to Azure services with the CLI.</span></span>
> <span data-ttu-id="ff0c4-134">基本認証を使用しない場合は、`.bashrc` ファイルでこれらの変数をエクスポートすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-134">If you are not using basic auth, it's recommended to export these variables in your `.bashrc` file.</span></span>
> <span data-ttu-id="ff0c4-135">常に、貴社のビジネスのセキュリティ ポリシーと、システム管理者の要件に従ってください。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-135">Always follow your business' security policies and the requirements of your system administrator.</span></span>

<span data-ttu-id="ff0c4-136">Homebrew からボトル リソースを取得するには、プロキシで次のアドレスへの HTTPS 接続を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-136">In order to get the bottle resources from Homebrew, your proxy needs to allow HTTPS connections to the following addresses:</span></span>

* `https://formulae.brew.sh`
* `https://homebrew.bintray.com`

## <a name="update"></a><span data-ttu-id="ff0c4-137">更新</span><span class="sxs-lookup"><span data-stu-id="ff0c4-137">Update</span></span>

<span data-ttu-id="ff0c4-138">CLI は、バグの修正、機能強化、新機能、およびプレビュー機能で定期的に更新されています。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-138">The CLI is regularly updated with bug fixes, improvements, new features, and preview functionality.</span></span> <span data-ttu-id="ff0c4-139">新しいリリースは約 2 週間ごとに入手できます。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-139">A new release is available roughly every two weeks.</span></span> <span data-ttu-id="ff0c4-140">ローカル リポジトリ情報を更新してから、`azure-cli` パッケージをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-140">Update your local repository information and then upgrade the `azure-cli` package.</span></span>

```bash
brew update && brew upgrade azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="ff0c4-141">アンインストール</span><span class="sxs-lookup"><span data-stu-id="ff0c4-141">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="ff0c4-142">Homebrew を使用して、`azure-cli` パッケージをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-142">Use homebrew to uninstall the `azure-cli` package.</span></span>

```bash
brew uninstall azure-cli
```

## <a name="other-installation-methods"></a><span data-ttu-id="ff0c4-143">その他のインストール方法</span><span class="sxs-lookup"><span data-stu-id="ff0c4-143">Other installation methods</span></span>

<span data-ttu-id="ff0c4-144">Homebrew を使用して環境に Azure CLI をインストールできない場合は、Linux の手動手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-144">If you can't use homebrew to install the Azure CLI in your environment, it's possible to use the manual instructions for Linux.</span></span> <span data-ttu-id="ff0c4-145">正式には、このプロセスは macOS との互換性が維持されていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-145">Note that this process is not officially maintained to be compatible with macOS.</span></span> <span data-ttu-id="ff0c4-146">Homebrew などのパッケージ マネージャーを使用することを常にお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-146">Using a package manager such as Homebrew is always recommended.</span></span> <span data-ttu-id="ff0c4-147">他の選択肢を利用できない場合のみ、手動によるインストール方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-147">Only use the manual installation method if you have no other option available.</span></span>

<span data-ttu-id="ff0c4-148">手動インストールの手順については、「[Linux での Azure CLI の手動インストール](install-azure-cli-linux.md)」参照してください。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-148">For the manual installation instructions, see [Install Azure CLI on Linux manually](install-azure-cli-linux.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="ff0c4-149">次の手順</span><span class="sxs-lookup"><span data-stu-id="ff0c4-149">Next Steps</span></span>

<span data-ttu-id="ff0c4-150">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="ff0c4-150">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="ff0c4-151">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="ff0c4-151">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
