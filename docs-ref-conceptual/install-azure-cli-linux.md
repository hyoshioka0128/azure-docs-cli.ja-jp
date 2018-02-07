---
title: "Linux での Azure CLI 2.0 の手動インストール"
description: "Linux で Azure CLI 2.0 を手動インストールする方法"
keywords: "Azure CLI,Azure CLI のインストール,azure linux, azure インストール linux"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: d8c88d111c50a3cbb6b643a14dcd2a9773699657
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2018
---
# <a name="install-azure-cli-20-on-linux-manually"></a><span data-ttu-id="52ffe-104">Linux での Azure CLI 2.0 の手動インストール</span><span class="sxs-lookup"><span data-stu-id="52ffe-104">Install Azure CLI 2.0 on Linux manually</span></span>

<span data-ttu-id="52ffe-105">お使いのディストリビューションで使用できる Azure CLI 用パッケージがない場合は、インストール スクリプトを実行して、いつでも手動で CLI をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="52ffe-105">If you do not have a package for the Azure CLI available on your distribution, you can always install the CLI manually by running an installation script.</span></span>

> [!NOTE]
> <span data-ttu-id="52ffe-106">CLI 用パッケージ マネージャーを使用することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="52ffe-106">It's strongly recommend that you use a package manager for the CLI.</span></span> <span data-ttu-id="52ffe-107">パッケージ マネージャーを使用すると、常に最新の更新プログラムを取得できるので、CLI コンポーネントの安定性が保証されます。</span><span class="sxs-lookup"><span data-stu-id="52ffe-107">A package manager makes sure you always get the latest updates, and guarantees the stability of CLI components.</span></span> <span data-ttu-id="52ffe-108">手動でインストールする前に、お使いのディストリビューション用のパッケージがあるかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="52ffe-108">Check and see if there is a package for your distribution before installing manually.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="52ffe-109">前提条件</span><span class="sxs-lookup"><span data-stu-id="52ffe-109">Prerequisites</span></span>

<span data-ttu-id="52ffe-110">CLI をインストールするには、システムで次のソフトウェアを使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="52ffe-110">In order to install the CLI, you need the following software available on your system:</span></span>

* [<span data-ttu-id="52ffe-111">Python 2.7 または Python 3.x</span><span class="sxs-lookup"><span data-stu-id="52ffe-111">Python 2.7 or Python 3.x</span></span>](https://www.python.org/downloads/)
* [<span data-ttu-id="52ffe-112">libffi</span><span class="sxs-lookup"><span data-stu-id="52ffe-112">libffi</span></span>](https://sourceware.org/libffi/)
* [<span data-ttu-id="52ffe-113">OpenSSL 1.0.2</span><span class="sxs-lookup"><span data-stu-id="52ffe-113">OpenSSL 1.0.2</span></span>](https://www.openssl.org/source/)

## <a name="install-or-update"></a><span data-ttu-id="52ffe-114">インストールまたは更新</span><span class="sxs-lookup"><span data-stu-id="52ffe-114">Install or update</span></span> 

<span data-ttu-id="52ffe-115">CLI をインストールするか更新するかに関わらず、完全インストールを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52ffe-115">Whether you are installing or updating the CLI, you need to perform a full installation.</span></span> <span data-ttu-id="52ffe-116">前提条件を準備できたら、`curl` を実行して CLI をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="52ffe-116">Once you have the prerequisites, you can install the CLI by running `curl`.</span></span>

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

<span data-ttu-id="52ffe-117">代わりに、スクリプトをダウンロードしてローカルで実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="52ffe-117">You can also download the script and run it locally instead.</span></span> <span data-ttu-id="52ffe-118">変更を有効にするために、シェルの再起動が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="52ffe-118">You may have to restart your shell in order for changes to take effect.</span></span> <span data-ttu-id="52ffe-119">インストール後、`az` コマンドを使用して CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="52ffe-119">After installation, run the CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="52ffe-120">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="52ffe-120">Troubleshooting</span></span>

<span data-ttu-id="52ffe-121">ここでは、手動インストール中に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="52ffe-121">Here are some common problems seen during a manual installation.</span></span> <span data-ttu-id="52ffe-122">問題がここに示されていない場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="52ffe-122">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>
### <a name="curl-object-moved-error"></a><span data-ttu-id="52ffe-123">curl の "Object Moved" エラー</span><span class="sxs-lookup"><span data-stu-id="52ffe-123">curl "Object Moved" error</span></span>

<span data-ttu-id="52ffe-124">`curl` で `-L` パラメーターに関連するエラーが発生した場合や、"Object Moved" というテキストが含まれているエラー メッセージが表示された場合は、次のように、`aka.ms` リダイレクトの代わりに完全な URL を使用してみてください。</span><span class="sxs-lookup"><span data-stu-id="52ffe-124">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a><span data-ttu-id="52ffe-125">`az` コマンドが見つからない</span><span class="sxs-lookup"><span data-stu-id="52ffe-125">`az` command not found</span></span>

<span data-ttu-id="52ffe-126">インストール後に、`bash` または `zsh` でコマンドを実行できない場合は、シェルのコマンド ハッシュのキャッシュをクリアします。</span><span class="sxs-lookup"><span data-stu-id="52ffe-126">If you can't run the command after installation and using `bash` or `zsh`, clear your shell's command hash cache.</span></span> <span data-ttu-id="52ffe-127">実行</span><span class="sxs-lookup"><span data-stu-id="52ffe-127">Run</span></span>

```bash
hash -r
```

<span data-ttu-id="52ffe-128">問題が解決されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="52ffe-128">and check if the problem is resolved.</span></span>

<span data-ttu-id="52ffe-129">インストール後にシェルを再起動しなかった場合にも、この問題が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="52ffe-129">The issue can also occur if you did not restart your shell after installation.</span></span> <span data-ttu-id="52ffe-130">`az` コマンドの場所が `$PATH` にあることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="52ffe-130">Make sure that the location of the `az` command is in your `$PATH`.</span></span> <span data-ttu-id="52ffe-131">`az` コマンドの場所は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="52ffe-131">The location of the `az` command is</span></span>

```bash
<install path>/bin
```

## <a name="uninstall"></a><span data-ttu-id="52ffe-132">アンインストール</span><span class="sxs-lookup"><span data-stu-id="52ffe-132">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="52ffe-133">CLI をアンインストールするには、インストール時に選択した場所からファイルを直接削除します。</span><span class="sxs-lookup"><span data-stu-id="52ffe-133">Uninstall the CLI by directly deleting the files from the location chosen at the time of installation.</span></span> <span data-ttu-id="52ffe-134">既定のインストール場所は `$HOME` です。</span><span class="sxs-lookup"><span data-stu-id="52ffe-134">The default install location is `$HOME`.</span></span>

1. <span data-ttu-id="52ffe-135">インストールされている CLI ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="52ffe-135">Remove the installed CLI files.</span></span>
  
  ```bash
  rm -r <install location>/lib/azure-cli
  rm <install location>/bin/az
  ```
2. <span data-ttu-id="52ffe-136">`$HOME/.bash_profile` ファイルを変更して、次の行を削除します。</span><span class="sxs-lookup"><span data-stu-id="52ffe-136">Modify your `$HOME/.bash_profile` file to remove the following line:</span></span>
  
  ```
  <install location>/lib/azure-cli/az.completion
  ```

3. <span data-ttu-id="52ffe-137">`bash` または `zsh` を使用している場合は、シェルのコマンド キャッシュを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="52ffe-137">If using `bash` or `zsh`, reload your shell's command cache.</span></span>
  
  ```bash
  hash -r
  ```
