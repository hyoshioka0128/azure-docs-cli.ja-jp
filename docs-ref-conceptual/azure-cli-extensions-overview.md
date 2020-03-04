---
title: Azure CLI の拡張機能
description: Azure CLI での拡張機能の使用
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 09/07/2018
ms.topic: conceptual
ms.service: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 73488fc464ed052f22f071f6373fb6b8f682b778
ms.sourcegitcommit: 7caa6673f65e61deb8d6def6386e4eb9acdac923
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2020
ms.locfileid: "77779994"
---
# <a name="use-extensions-with-azure-cli"></a><span data-ttu-id="79a9c-103">Azure CLI で拡張機能を使用する</span><span class="sxs-lookup"><span data-stu-id="79a9c-103">Use extensions with Azure CLI</span></span> 

<span data-ttu-id="79a9c-104">Azure CLI には、拡張機能を読み込む機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="79a9c-104">The Azure CLI offers the capability to load extensions.</span></span> <span data-ttu-id="79a9c-105">拡張機能は Python の wheel 形式で、CLI には付属していませんが CLI コマンドとして実行できます。</span><span class="sxs-lookup"><span data-stu-id="79a9c-105">Extensions are Python wheels that aren't shipped as part of the CLI but run as CLI commands.</span></span>
<span data-ttu-id="79a9c-106">拡張機能を使用すると、独自の CLI インターフェイスを記述する機能と共に、リリース前の実験的なコマンドにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="79a9c-106">With extensions, you gain access to experimental and pre-release commands along with the ability to write your own CLI interfaces.</span></span> <span data-ttu-id="79a9c-107">この記事では、拡張機能の管理方法について説明し、その使用に関する一般的な質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="79a9c-107">This article covers how to manage extensions and answers common questions about their use.</span></span>

## <a name="find-extensions"></a><span data-ttu-id="79a9c-108">拡張機能の検索</span><span class="sxs-lookup"><span data-stu-id="79a9c-108">Find extensions</span></span>

<span data-ttu-id="79a9c-109">Microsoft によって提供および管理されている拡張機能を確認するには、[az extension list-available](/cli/azure/extension#az-extension-list-available) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="79a9c-109">To see the extensions provided and maintained by Microsoft, use the [az extension list-available](/cli/azure/extension#az-extension-list-available) command.</span></span>

```azurecli-interactive
az extension list-available --output table
```

<span data-ttu-id="79a9c-110">Microsoft では、ドキュメント サイトでも[拡張機能の一覧](azure-cli-extensions-list.md)をホストしています。</span><span class="sxs-lookup"><span data-stu-id="79a9c-110">We also host a [list of extensions](azure-cli-extensions-list.md) on the documentation site.</span></span>

## <a name="install-extensions"></a><span data-ttu-id="79a9c-111">拡張機能のインストール</span><span class="sxs-lookup"><span data-stu-id="79a9c-111">Install extensions</span></span>

<span data-ttu-id="79a9c-112">インストールする拡張機能を見つけたら、[az extension add](https://docs.microsoft.com/cli/azure/extension#az-extension-add) を使用して取得します。</span><span class="sxs-lookup"><span data-stu-id="79a9c-112">Once you have found an extension to install, use [az extension add](https://docs.microsoft.com/cli/azure/extension#az-extension-add) to get it.</span></span> <span data-ttu-id="79a9c-113">その拡張機能が `az extension list-available` に表示される場合は、名前によってインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="79a9c-113">If the extension is listed in `az extension list-available`, you can install the extension by name.</span></span>

```azurecli-interactive
az extension add --name <extension-name>
```

<span data-ttu-id="79a9c-114">拡張機能のソースが外部リソースであるか、その拡張機能への直接リンクがある場合は、ソース URL またはローカル パスを指定します。</span><span class="sxs-lookup"><span data-stu-id="79a9c-114">If the extension is from an external resource or you have a direct link to it, provide the source URL or local path.</span></span> <span data-ttu-id="79a9c-115">拡張機能は、コンパイルされた Python の wheel 形式ファイルである "_必要があります_"。</span><span class="sxs-lookup"><span data-stu-id="79a9c-115">The extension _must_ be a compiled Python wheel file.</span></span>

```azurecli-interactive
az extension add --source <URL-or-path>
```

<span data-ttu-id="79a9c-116">インストールされた拡張機能は、`$AZURE_EXTENSION_DIR` シェル変数の値で確認できます。</span><span class="sxs-lookup"><span data-stu-id="79a9c-116">Once an extension is installed, it's found under the value of the `$AZURE_EXTENSION_DIR` shell variable.</span></span> <span data-ttu-id="79a9c-117">この変数が設定されていない場合、既定では、この値は `$HOME/.azure/cliextensions` (Linux と macOS の場合) または `%USERPROFILE%\.azure\cliextensions` (Windows の場合) になります。</span><span class="sxs-lookup"><span data-stu-id="79a9c-117">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

## <a name="update-extensions"></a><span data-ttu-id="79a9c-118">拡張機能の更新</span><span class="sxs-lookup"><span data-stu-id="79a9c-118">Update extensions</span></span>

<span data-ttu-id="79a9c-119">拡張機能を名前でインストールした場合、[az extension update](https://docs.microsoft.com/cli/azure/extension#az-extension-update) を使用してその拡張機能を更新します。</span><span class="sxs-lookup"><span data-stu-id="79a9c-119">If an extension was installed by name, update it using [az extension update](https://docs.microsoft.com/cli/azure/extension#az-extension-update).</span></span>

```azurecli-interactive
az extension update --name <extension-name>
```

<span data-ttu-id="79a9c-120">それ以外の場合は、「[拡張機能のインストール](#install-extensions)」の説明に従って、ソースから拡張機能を更新できます。</span><span class="sxs-lookup"><span data-stu-id="79a9c-120">Otherwise, an extension can be updated from source by following the [Install extensions](#install-extensions) instructions.</span></span>

<span data-ttu-id="79a9c-121">CLI で拡張機能の名前を解決できない場合は、アンインストールしてから再インストールを試みてください。</span><span class="sxs-lookup"><span data-stu-id="79a9c-121">If an extension name can't be resolved by the CLI, uninstall it and attempt to reinstall.</span></span> <span data-ttu-id="79a9c-122">拡張機能が、基本 CLI の一部になっている可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="79a9c-122">The extension could also have become part of the base CLI.</span></span>
<span data-ttu-id="79a9c-123">「[Azure CLI のインストール](install-azure-cli.md)」の説明に従って CLI の更新を試み、拡張機能のコマンドが追加されているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="79a9c-123">Try updating the CLI as described in [Install the Azure CLI](install-azure-cli.md) and see if the extension's commands were added.</span></span>

## <a name="uninstall-extensions"></a><span data-ttu-id="79a9c-124">拡張機能のアンインストール</span><span class="sxs-lookup"><span data-stu-id="79a9c-124">Uninstall extensions</span></span>

<span data-ttu-id="79a9c-125">拡張機能が不要になった場合は、[az extension remove](https://docs.microsoft.com/cli/azure/extension#az-extension-remove) を使用して削除します。</span><span class="sxs-lookup"><span data-stu-id="79a9c-125">If you no longer need an extension, remove it with [az extension remove](https://docs.microsoft.com/cli/azure/extension#az-extension-remove).</span></span>

```azurecli-interactive
az extension remove --name <extension-name>
```

<span data-ttu-id="79a9c-126">また、手動で削除することもできます。それには、インストールした場所から拡張機能を削除します。</span><span class="sxs-lookup"><span data-stu-id="79a9c-126">You can also remove an extension manually by deleting it from the location where it was installed.</span></span> <span data-ttu-id="79a9c-127">`$AZURE_EXTENSION_DIR` シェル変数によって、モジュールがインストールされている場所が定義されています。</span><span class="sxs-lookup"><span data-stu-id="79a9c-127">The `$AZURE_EXTENSION_DIR` shell variable defines where modules are installed.</span></span>
<span data-ttu-id="79a9c-128">この変数が設定されていない場合、既定では、この値は `$HOME/.azure/cliextensions` (Linux と macOS の場合) または `%USERPROFILE%\.azure\cliextensions` (Windows の場合) になります。</span><span class="sxs-lookup"><span data-stu-id="79a9c-128">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

```bash
rm -rf $AZURE_EXTENSION_DIR/<extension-name>
```

## <a name="faq"></a><span data-ttu-id="79a9c-129">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="79a9c-129">FAQ</span></span>

<span data-ttu-id="79a9c-130">ここでは、CLI 拡張機能に関するその他の一般的な質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="79a9c-130">Here are some answers to other common questions about CLI extensions.</span></span>

### <a name="what-file-formats-are-allowed-for-installation"></a><span data-ttu-id="79a9c-131">インストールでは、どのファイル形式が許可されていますか。</span><span class="sxs-lookup"><span data-stu-id="79a9c-131">What file formats are allowed for installation?</span></span>

<span data-ttu-id="79a9c-132">現時点では、Python のコンパイルされた wheel 形式のみを拡張機能としてインストールできます。</span><span class="sxs-lookup"><span data-stu-id="79a9c-132">Currently, only compiled Python wheels can be installed as extensions.</span></span>

### <a name="can-extensions-replace-existing-commands"></a><span data-ttu-id="79a9c-133">拡張機能で既存のコマンドを置き換えることはできますか。</span><span class="sxs-lookup"><span data-stu-id="79a9c-133">Can extensions replace existing commands?</span></span>

<span data-ttu-id="79a9c-134">はい。</span><span class="sxs-lookup"><span data-stu-id="79a9c-134">Yes.</span></span> <span data-ttu-id="79a9c-135">拡張機能で既存のコマンドを置き換えることはできますが、置き換えられたコマンドを実行する前に、CLI によって警告が発せられます。</span><span class="sxs-lookup"><span data-stu-id="79a9c-135">Extensions may replace existing commands, but before running a command that has been replaced the CLI will issue a warning.</span></span>

### <a name="how-can-i-tell-if-an-extension-is-in-pre-release"></a><span data-ttu-id="79a9c-136">拡張機能がプレリリースかどうかをどのように確認できますか。</span><span class="sxs-lookup"><span data-stu-id="79a9c-136">How can I tell if an extension is in pre-release?</span></span>

<span data-ttu-id="79a9c-137">拡張機能がプレリリースに含まれているかどうかは、拡張機能のドキュメントとバージョン管理に示されています。</span><span class="sxs-lookup"><span data-stu-id="79a9c-137">An extension's documentation and versioning will show if it's in pre-release.</span></span> <span data-ttu-id="79a9c-138">Microsoft では、多くの場合、プレビューのコマンドを CLI 拡張機能としてリリースしますが、後でそのコマンドをメインの CLI 製品に追加します。</span><span class="sxs-lookup"><span data-stu-id="79a9c-138">Microsoft often releases preview commands as CLI extensions, with the option of moving them into the main CLI product later.</span></span> <span data-ttu-id="79a9c-139">コマンドが拡張機能から移動された場合は、古い拡張機能をアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="79a9c-139">When commands are moved out of extensions, the old extension should be uninstalled.</span></span> 

### <a name="can-extensions-depend-upon-each-other"></a><span data-ttu-id="79a9c-140">拡張機能は相互に依存できますか。</span><span class="sxs-lookup"><span data-stu-id="79a9c-140">Can extensions depend upon each other?</span></span>

<span data-ttu-id="79a9c-141">いいえ。</span><span class="sxs-lookup"><span data-stu-id="79a9c-141">No.</span></span> <span data-ttu-id="79a9c-142">CLI では読み込みの順序が保証されていないため、依存関係が満たされていないことがあります。</span><span class="sxs-lookup"><span data-stu-id="79a9c-142">Since the CLI doesn't guarantee a load order, dependencies might not be satisfied.</span></span> <span data-ttu-id="79a9c-143">拡張機能を削除しても、他の拡張機能には影響しません。</span><span class="sxs-lookup"><span data-stu-id="79a9c-143">Removing an extension won't affect any others.</span></span>

### <a name="are-extensions-updated-along-with-the-cli"></a><span data-ttu-id="79a9c-144">拡張機能は CLI と共に更新されますか。</span><span class="sxs-lookup"><span data-stu-id="79a9c-144">Are extensions updated along with the CLI?</span></span>

<span data-ttu-id="79a9c-145">いいえ。</span><span class="sxs-lookup"><span data-stu-id="79a9c-145">No.</span></span> <span data-ttu-id="79a9c-146">「[拡張機能の更新](#update-extensions)」で説明したように、拡張機能は個別に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="79a9c-146">Extensions must be updated separately, as described in [Update extensions](#update-extensions).</span></span>

### <a name="how-to-develop-our-own-extension"></a><span data-ttu-id="79a9c-147">独自の拡張機能を開発する方法</span><span class="sxs-lookup"><span data-stu-id="79a9c-147">How to develop our own extension?</span></span>
<span data-ttu-id="79a9c-148">詳細については、公式リポジトリを参照してください。</span><span class="sxs-lookup"><span data-stu-id="79a9c-148">Please refer to the official repository for more help.</span></span> [<span data-ttu-id="79a9c-149">Azure/azure-cli-extensions</span><span class="sxs-lookup"><span data-stu-id="79a9c-149">Azure/azure-cli-extensions</span></span>](https://github.com/Azure/azure-cli/tree/master/doc/extensions)
