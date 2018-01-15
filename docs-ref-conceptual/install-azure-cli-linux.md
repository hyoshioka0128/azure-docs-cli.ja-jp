---
title: "Linux での Azure CLI 2.0 の手動インストール"
description: "Linux で Azure CLI 2.0 を手動インストールする方法"
keywords: "Azure CLI,Azure CLI のインストール,azure linux, azure インストール linux"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 11/01/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cf1405cae70762146f63bc6629edc0dd1d949fff
ms.sourcegitcommit: 3eef136ae752eb90c67af604d4ddd298d70b1c9d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/06/2018
---
# <a name="install-azure-cli-20-on-linux-manually"></a><span data-ttu-id="267d4-104">Linux での Azure CLI 2.0 の手動インストール</span><span class="sxs-lookup"><span data-stu-id="267d4-104">Install Azure CLI 2.0 on Linux manually</span></span>

<span data-ttu-id="267d4-105">ディストリビューションで使用できる Azure CLI 用パッケージがない場合は、インストール スクリプトを実行して、いつでも手動で CLI をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="267d4-105">If you do not have a package for the Azure CLI available on your distribution, you can always install the CLI manualy by running an installation script.</span></span> <span data-ttu-id="267d4-106">使用できるパッケージがある場合は、それを使用してインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="267d4-106">If you do have a package available, that is always the recommended installation method.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="267d4-107">前提条件</span><span class="sxs-lookup"><span data-stu-id="267d4-107">Prerequisites</span></span>

<span data-ttu-id="267d4-108">CLI をインストールするには、システムで次のソフトウェアを使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="267d4-108">In order to install the CLI, you will need the following software available on your system:</span></span>

* [<span data-ttu-id="267d4-109">Python 2.7 または Python 3.x</span><span class="sxs-lookup"><span data-stu-id="267d4-109">Python 2.7 or Python 3.x</span></span>](https://www.python.org/downloads/)
* [<span data-ttu-id="267d4-110">libffi</span><span class="sxs-lookup"><span data-stu-id="267d4-110">libffi</span></span>](https://sourceware.org/libffi/)
* [<span data-ttu-id="267d4-111">OpenSSL 1.0.2</span><span class="sxs-lookup"><span data-stu-id="267d4-111">OpenSSL 1.0.2</span></span>](https://www.openssl.org/source/)

## <a name="install-or-update-manually"></a><span data-ttu-id="267d4-112">手動でのインストールまたは更新</span><span class="sxs-lookup"><span data-stu-id="267d4-112">Install or update manually</span></span>

<span data-ttu-id="267d4-113">CLI をインストールするか更新するかにかかわらず、完全インストールを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="267d4-113">Whether you are installing or updating the CLI, you will need to perform a full installation.</span></span> <span data-ttu-id="267d4-114">前提条件を準備できたら、`curl` を実行して CLI をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="267d4-114">Once you have the prerequisites, you can install the CLI by running `curl`.</span></span>

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

<span data-ttu-id="267d4-115">必要がある場合、または `curl` がシステムにない場合は、代わりにスクリプトをダウンロードして、ローカルで実行できます。</span><span class="sxs-lookup"><span data-stu-id="267d4-115">If you would prefer, or do not have `curl` on your system, you can download the script and run it locally instead.</span></span> <span data-ttu-id="267d4-116">変更を有効にするために、シェルの再起動が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="267d4-116">You may have to restart your shell in order for changes to take effect.</span></span> <span data-ttu-id="267d4-117">インストール後、`az` コマンドを使用して CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="267d4-117">After installation, run the CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="267d4-118">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="267d4-118">Troubleshooting</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="267d4-119">curl の "Object Moved" エラー</span><span class="sxs-lookup"><span data-stu-id="267d4-119">curl "Object Moved" error</span></span>

<span data-ttu-id="267d4-120">`curl` で `-L` パラメーターに関連するエラーが発生した場合や、"Object Moved" というテキストが含まれているエラー メッセージが表示された場合は、次のように、`aka.ms` リダイレクトの代わりに完全な URL を使用してみてください。</span><span class="sxs-lookup"><span data-stu-id="267d4-120">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a><span data-ttu-id="267d4-121">`az` コマンドが見つからない</span><span class="sxs-lookup"><span data-stu-id="267d4-121">`az` command not found</span></span>

<span data-ttu-id="267d4-122">インストール後に、コマンドを実行できない場合は、シェルのコマンド ハッシュのキャッシュをクリアしなければならない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="267d4-122">After installation if you can't run the command, you may need to clear your shell's command hash cache.</span></span> <span data-ttu-id="267d4-123">実行</span><span class="sxs-lookup"><span data-stu-id="267d4-123">Run</span></span>

```bash
hash -r
```

<span data-ttu-id="267d4-124">問題が解決されているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="267d4-124">and see if the problem is resolved.</span></span>

<span data-ttu-id="267d4-125">これは、インストール後、シェルを再起動していない場合にも発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="267d4-125">This can also occur if you did not restart your shell after installation.</span></span> <span data-ttu-id="267d4-126">`az` コマンドの場所が `$PATH` にあることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="267d4-126">Make sure that the location of the `az` command is in your `$PATH`.</span></span>

<span data-ttu-id="267d4-127">インストール スクリプトを実行した場合、これは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="267d4-127">If you ran the installation script, this will be:</span></span>

```bash
<install path>/bin
```

## <a name="unstinall-manually"></a><span data-ttu-id="267d4-128">手動でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="267d4-128">Unstinall manually</span></span>

<span data-ttu-id="267d4-129">Azure CLI が不要であると判断した場合は、アンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="267d4-129">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="267d4-130">アンインストールする前に、`az feedback` コマンドを使用して、アンインストールの理由と、CLI エクスペリエンスの改善方法について、ご意見をお聞かせください。</span><span class="sxs-lookup"><span data-stu-id="267d4-130">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="267d4-131">Microsoft では、できる限り Azure CLI のバグをなくし、使いやすいものにしたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="267d4-131">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="267d4-132">また、[GitHub に問題を提出](https://github.com/Azure/azure-cli/issues)していただくこともできます。</span><span class="sxs-lookup"><span data-stu-id="267d4-132">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

<span data-ttu-id="267d4-133">CLI をアンインストールするには、インストール場所からファイルを直接削除します。</span><span class="sxs-lookup"><span data-stu-id="267d4-133">You can uninstall the CLI by directly deleting the files from the install location.</span></span> <span data-ttu-id="267d4-134">`https://aka.ms/InstallAzureCLI` スクリプト経由でインストールした場合、インストール時に選択した場所にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="267d4-134">Your install location should have been chosen at the time of install, if you installed via the `https://aka.ms/InstallAzureCLI` script.</span></span> <span data-ttu-id="267d4-135">既定のインストール場所は `$HOME` です。</span><span class="sxs-lookup"><span data-stu-id="267d4-135">The default installation location is `$HOME`.</span></span>

<span data-ttu-id="267d4-136">最初に、インストールされた CLI ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="267d4-136">First, remove the installed CLI files:</span></span>

```bash
rm -r <install location>/lib/azure-cli
rm <install location>/bin/az
```

<span data-ttu-id="267d4-137">次に、`$HOME/.bash_profile` ファイルを変更して、行を削除します。</span><span class="sxs-lookup"><span data-stu-id="267d4-137">Then modify your `$HOME/.bash_profile` file to remove the line:</span></span>

```
<install location>/lib/azure-cli/az.completion
```

<span data-ttu-id="267d4-138">最後に、シェルのコマンド キャッシュを再度読み込みます (使用している場合)。</span><span class="sxs-lookup"><span data-stu-id="267d4-138">And finally, reload your shell's command cache if it uses one.</span></span> <span data-ttu-id="267d4-139">`bash` および `zsh` ユーザーは、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="267d4-139">`bash` and `zsh` users will need to perform this step:</span></span>

```bash
hash -r
```
