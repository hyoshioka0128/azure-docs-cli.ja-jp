---
title: Linux での Azure CLI の手動インストール
description: Linux で Azure CLI を手動インストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 13edb9954678aca627529714aeee02062c720219
ms.sourcegitcommit: 08043c47d3ccf23522b91e6bba3932e312c04c7f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2019
ms.locfileid: "66516306"
---
# <a name="install-azure-cli-on-linux-manually"></a><span data-ttu-id="ad93a-103">Linux での Azure CLI の手動インストール</span><span class="sxs-lookup"><span data-stu-id="ad93a-103">Install Azure CLI on Linux manually</span></span>

<span data-ttu-id="ad93a-104">お使いのディストリビューションに対応した Azure CLI 用パッケージがない場合は、手動でスクリプトを実行して CLI をインストールします。</span><span class="sxs-lookup"><span data-stu-id="ad93a-104">If there's no package for the Azure CLI for you your distribution, install the CLI manually by running a script.</span></span>

[!INCLUDE [current-version](includes/current-version.md)]

> [!NOTE]
> <span data-ttu-id="ad93a-105">パッケージ マネージャーを使用して CLI をインストールすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ad93a-105">It's strongly recommend to install the CLI with a package manager.</span></span> <span data-ttu-id="ad93a-106">パッケージ マネージャーを使用すると、常に最新の更新プログラムを取得できるので、CLI コンポーネントの安定性が保証されます。</span><span class="sxs-lookup"><span data-stu-id="ad93a-106">A package manager makes sure you always get the latest updates, and guarantees the stability of CLI components.</span></span> <span data-ttu-id="ad93a-107">手動でインストールする前に、お使いのディストリビューション用のパッケージがあるかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ad93a-107">Check and see if there is a package for your distribution before installing manually.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ad93a-108">前提条件</span><span class="sxs-lookup"><span data-stu-id="ad93a-108">Prerequisites</span></span>

<span data-ttu-id="ad93a-109">CLI には、次のソフトウェアが必要です。</span><span class="sxs-lookup"><span data-stu-id="ad93a-109">The CLI requires the following software:</span></span>

* <span data-ttu-id="ad93a-110">[Python 3.6.x または 3.7.x](https://www.python.org/downloads/)。</span><span class="sxs-lookup"><span data-stu-id="ad93a-110">[Python 3.6.x or 3.7.x](https://www.python.org/downloads/).</span></span> 
* [<span data-ttu-id="ad93a-111">libffi</span><span class="sxs-lookup"><span data-stu-id="ad93a-111">libffi</span></span>](https://sourceware.org/libffi/)
* [<span data-ttu-id="ad93a-112">OpenSSL 1.0.2</span><span class="sxs-lookup"><span data-stu-id="ad93a-112">OpenSSL 1.0.2</span></span>](https://www.openssl.org/source/)

> [!IMPORTANT]
>
> <span data-ttu-id="ad93a-113">CLI は、Python 2.7.x とも互換性がありますが、Python 2.7.x は 2020 年 1 月 1 日に有効期間が終了します。</span><span class="sxs-lookup"><span data-stu-id="ad93a-113">The CLI is also compatible with Python 2.7.x, which is being end-of-lifed on January 1, 2020.</span></span> <span data-ttu-id="ad93a-114">このため、CLI を実行する場合は、Python 3 をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ad93a-114">For this reason we recommend that you install Python 3 to run the CLI.</span></span>

## <a name="install-or-update"></a><span data-ttu-id="ad93a-115">インストールまたは更新</span><span class="sxs-lookup"><span data-stu-id="ad93a-115">Install or update</span></span>

<span data-ttu-id="ad93a-116">CLI をインストールおよび更新するには、いずれの場合もインストール スクリプトを再実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad93a-116">Both installing and updating the CLI requires re-running the install script.</span></span> <span data-ttu-id="ad93a-117">`curl` を実行して CLI をインストールします。</span><span class="sxs-lookup"><span data-stu-id="ad93a-117">Install the CLI by running `curl`.</span></span>

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

<span data-ttu-id="ad93a-118">スクリプトをダウンロードして、ローカルで実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="ad93a-118">The script can also be downloaded and run locally.</span></span> <span data-ttu-id="ad93a-119">変更を有効にするために、シェルの再起動が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="ad93a-119">You may have to restart your shell in order for changes to take effect.</span></span>

<span data-ttu-id="ad93a-120">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="ad93a-120">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="ad93a-121">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ad93a-121">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="ad93a-122">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad93a-122">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ad93a-123">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="ad93a-123">Troubleshooting</span></span>

<span data-ttu-id="ad93a-124">ここでは、手動インストール中に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="ad93a-124">Here are some common problems seen during a manual installation.</span></span> <span data-ttu-id="ad93a-125">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="ad93a-125">If you experience a problem not covered here, [file an issue on GitHub](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="ad93a-126">curl の "Object Moved" エラー</span><span class="sxs-lookup"><span data-stu-id="ad93a-126">curl "Object Moved" error</span></span>

<span data-ttu-id="ad93a-127">`curl` で `-L` パラメーターに関連するエラーが発生した場合や、"Object Moved" というテキストが含まれているエラー メッセージが表示された場合は、次のように、`aka.ms` リダイレクトの代わりに完全な URL を使用してみてください。</span><span class="sxs-lookup"><span data-stu-id="ad93a-127">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a><span data-ttu-id="ad93a-128">`az` コマンドが見つからない</span><span class="sxs-lookup"><span data-stu-id="ad93a-128">`az` command not found</span></span>

<span data-ttu-id="ad93a-129">インストール後に、`bash` または `zsh` でコマンドを実行できない場合は、シェルのコマンド ハッシュのキャッシュをクリアします。</span><span class="sxs-lookup"><span data-stu-id="ad93a-129">If you can't run the command after installation and using `bash` or `zsh`, clear your shell's command hash cache.</span></span> <span data-ttu-id="ad93a-130">ラン</span><span class="sxs-lookup"><span data-stu-id="ad93a-130">Run</span></span>

```bash
hash -r
```

<span data-ttu-id="ad93a-131">問題が解決されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="ad93a-131">and check if the problem is resolved.</span></span>

<span data-ttu-id="ad93a-132">インストール後にシェルを再起動しなかった場合にも、この問題が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="ad93a-132">The issue can also occur if you didn't restart your shell after installation.</span></span> <span data-ttu-id="ad93a-133">`az` コマンドの場所が `$PATH` にあることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ad93a-133">Make sure that the location of the `az` command is in your `$PATH`.</span></span> <span data-ttu-id="ad93a-134">`az` コマンドの場所は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ad93a-134">The location of the `az` command is</span></span>

```bash
<install path>/bin
```

### <a name="proxy-blocks-connection"></a><span data-ttu-id="ad93a-135">プロキシによる接続のブロック</span><span class="sxs-lookup"><span data-stu-id="ad93a-135">Proxy blocks connection</span></span>

[!INCLUDE[configure-proxy](includes/configure-proxy.md)]

<span data-ttu-id="ad93a-136">インストール スクリプトを取得するには、プロキシで次のアドレスへの HTTPS 接続を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad93a-136">In order to get the installation scripts, your proxy needs to allow HTTPS connections to the following addresses:</span></span>

* `https://aka.ms/`
* `https://azurecliprod.blob.core.windows.net/`
* `https://pypi.python.org`
* <span data-ttu-id="ad93a-137">コア パッケージ用のディストリビューションのパッケージ マネージャー (ある場合) によって使用されるエンドポイント</span><span class="sxs-lookup"><span data-stu-id="ad93a-137">Endpoints used by your distribution's package manager (if any) for core packages</span></span>

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]

## <a name="uninstall"></a><span data-ttu-id="ad93a-138">アンインストール</span><span class="sxs-lookup"><span data-stu-id="ad93a-138">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="ad93a-139">CLI をアンインストールするには、インストール時に選択した場所からファイルを直接削除します。</span><span class="sxs-lookup"><span data-stu-id="ad93a-139">Uninstall the CLI by directly deleting the files from the location chosen at the time of installation.</span></span> <span data-ttu-id="ad93a-140">既定のインストール場所は `$HOME` です。</span><span class="sxs-lookup"><span data-stu-id="ad93a-140">The default install location is `$HOME`.</span></span>

1. <span data-ttu-id="ad93a-141">インストールされている CLI ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="ad93a-141">Remove the installed CLI files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="ad93a-142">`$HOME/.bash_profile` ファイルを変更して、次の行を削除します。</span><span class="sxs-lookup"><span data-stu-id="ad93a-142">Modify your `$HOME/.bash_profile` file to remove the following line:</span></span>

   ```text
   <install location>/lib/azure-cli/az.completion
   ```

3. <span data-ttu-id="ad93a-143">`bash` または `zsh` を使用している場合は、シェルのコマンド キャッシュを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="ad93a-143">If using `bash` or `zsh`, reload your shell's command cache.</span></span>

   ```bash
   hash -r
   ```

## <a name="next-steps"></a><span data-ttu-id="ad93a-144">次の手順</span><span class="sxs-lookup"><span data-stu-id="ad93a-144">Next Steps</span></span>

<span data-ttu-id="ad93a-145">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="ad93a-145">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="ad93a-146">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="ad93a-146">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
