---
title: Linux での Azure CLI 2.0 の手動インストール
description: Linux で Azure CLI 2.0 を手動インストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 01/29/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 7e73ae8bbbba80bf48c6f01fc1c37a3c32c6eb31
ms.sourcegitcommit: 64f2c628e83d687d0e172c01f13d71c8c39a8040
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2018
ms.locfileid: "38967556"
---
# <a name="install-azure-cli-20-on-linux-manually"></a><span data-ttu-id="ccd65-103">Linux での Azure CLI 2.0 の手動インストール</span><span class="sxs-lookup"><span data-stu-id="ccd65-103">Install Azure CLI 2.0 on Linux manually</span></span>

<span data-ttu-id="ccd65-104">お使いのディストリビューションで使用できる Azure CLI 用パッケージがない場合は、インストール スクリプトを実行して、いつでも手動で CLI をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="ccd65-104">If you do not have a package for the Azure CLI available on your distribution, you can always install the CLI manually by running an installation script.</span></span>

> [!NOTE]
> <span data-ttu-id="ccd65-105">CLI 用パッケージ マネージャーを使用することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ccd65-105">It's strongly recommend that you use a package manager for the CLI.</span></span> <span data-ttu-id="ccd65-106">パッケージ マネージャーを使用すると、常に最新の更新プログラムを取得できるので、CLI コンポーネントの安定性が保証されます。</span><span class="sxs-lookup"><span data-stu-id="ccd65-106">A package manager makes sure you always get the latest updates, and guarantees the stability of CLI components.</span></span> <span data-ttu-id="ccd65-107">手動でインストールする前に、お使いのディストリビューション用のパッケージがあるかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ccd65-107">Check and see if there is a package for your distribution before installing manually.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ccd65-108">前提条件</span><span class="sxs-lookup"><span data-stu-id="ccd65-108">Prerequisites</span></span>

<span data-ttu-id="ccd65-109">CLI をインストールするには、システムで次のソフトウェアを使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ccd65-109">In order to install the CLI, you need the following software available on your system:</span></span>

* [<span data-ttu-id="ccd65-110">Python 2.7 または Python 3.x</span><span class="sxs-lookup"><span data-stu-id="ccd65-110">Python 2.7 or Python 3.x</span></span>](https://www.python.org/downloads/)
* [<span data-ttu-id="ccd65-111">libffi</span><span class="sxs-lookup"><span data-stu-id="ccd65-111">libffi</span></span>](https://sourceware.org/libffi/)
* [<span data-ttu-id="ccd65-112">OpenSSL 1.0.2</span><span class="sxs-lookup"><span data-stu-id="ccd65-112">OpenSSL 1.0.2</span></span>](https://www.openssl.org/source/)

## <a name="install-or-update"></a><span data-ttu-id="ccd65-113">インストールまたは更新</span><span class="sxs-lookup"><span data-stu-id="ccd65-113">Install or update</span></span>

<span data-ttu-id="ccd65-114">CLI をインストールするか更新するかに関わらず、完全インストールを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ccd65-114">Whether you are installing or updating the CLI, you need to perform a full installation.</span></span> <span data-ttu-id="ccd65-115">前提条件を準備できたら、`curl` を実行して CLI をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="ccd65-115">Once you have the prerequisites, you can install the CLI by running `curl`.</span></span>

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

<span data-ttu-id="ccd65-116">代わりに、スクリプトをダウンロードしてローカルで実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="ccd65-116">You can also download the script and run it locally instead.</span></span> <span data-ttu-id="ccd65-117">変更を有効にするために、シェルの再起動が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="ccd65-117">You may have to restart your shell in order for changes to take effect.</span></span>

<span data-ttu-id="ccd65-118">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="ccd65-118">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="ccd65-119">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ccd65-119">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="ccd65-120">さまざまな認証方法の詳細については、「[Azure CLI 2.0 を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ccd65-120">To learn more about different authentication methods, see [Sign in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ccd65-121">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="ccd65-121">Troubleshooting</span></span>

<span data-ttu-id="ccd65-122">ここでは、手動インストール中に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="ccd65-122">Here are some common problems seen during a manual installation.</span></span> <span data-ttu-id="ccd65-123">問題がここに示されていない場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="ccd65-123">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="ccd65-124">curl の "Object Moved" エラー</span><span class="sxs-lookup"><span data-stu-id="ccd65-124">curl "Object Moved" error</span></span>

<span data-ttu-id="ccd65-125">`curl` で `-L` パラメーターに関連するエラーが発生した場合や、"Object Moved" というテキストが含まれているエラー メッセージが表示された場合は、次のように、`aka.ms` リダイレクトの代わりに完全な URL を使用してみてください。</span><span class="sxs-lookup"><span data-stu-id="ccd65-125">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a><span data-ttu-id="ccd65-126">`az` コマンドが見つからない</span><span class="sxs-lookup"><span data-stu-id="ccd65-126">`az` command not found</span></span>

<span data-ttu-id="ccd65-127">インストール後に、`bash` または `zsh` でコマンドを実行できない場合は、シェルのコマンド ハッシュのキャッシュをクリアします。</span><span class="sxs-lookup"><span data-stu-id="ccd65-127">If you can't run the command after installation and using `bash` or `zsh`, clear your shell's command hash cache.</span></span> <span data-ttu-id="ccd65-128">ラン</span><span class="sxs-lookup"><span data-stu-id="ccd65-128">Run</span></span>

```bash
hash -r
```

<span data-ttu-id="ccd65-129">問題が解決されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="ccd65-129">and check if the problem is resolved.</span></span>

<span data-ttu-id="ccd65-130">インストール後にシェルを再起動しなかった場合にも、この問題が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="ccd65-130">The issue can also occur if you did not restart your shell after installation.</span></span> <span data-ttu-id="ccd65-131">`az` コマンドの場所が `$PATH` にあることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ccd65-131">Make sure that the location of the `az` command is in your `$PATH`.</span></span> <span data-ttu-id="ccd65-132">`az` コマンドの場所は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ccd65-132">The location of the `az` command is</span></span>

```bash
<install path>/bin
```

## <a name="uninstall"></a><span data-ttu-id="ccd65-133">アンインストール</span><span class="sxs-lookup"><span data-stu-id="ccd65-133">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="ccd65-134">CLI をアンインストールするには、インストール時に選択した場所からファイルを直接削除します。</span><span class="sxs-lookup"><span data-stu-id="ccd65-134">Uninstall the CLI by directly deleting the files from the location chosen at the time of installation.</span></span> <span data-ttu-id="ccd65-135">既定のインストール場所は `$HOME` です。</span><span class="sxs-lookup"><span data-stu-id="ccd65-135">The default install location is `$HOME`.</span></span>

1. <span data-ttu-id="ccd65-136">インストールされている CLI ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="ccd65-136">Remove the installed CLI files.</span></span>

  ```bash
  rm -r <install location>/lib/azure-cli
  rm <install location>/bin/az
  ```

2. <span data-ttu-id="ccd65-137">`$HOME/.bash_profile` ファイルを変更して、次の行を削除します。</span><span class="sxs-lookup"><span data-stu-id="ccd65-137">Modify your `$HOME/.bash_profile` file to remove the following line:</span></span>

  ```text
  <install location>/lib/azure-cli/az.completion
  ```

3. <span data-ttu-id="ccd65-138">`bash` または `zsh` を使用している場合は、シェルのコマンド キャッシュを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="ccd65-138">If using `bash` or `zsh`, reload your shell's command cache.</span></span>

  ```bash
  hash -r
  ```
