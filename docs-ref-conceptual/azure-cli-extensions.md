---
title: "Azure CLI 2.0 の拡張機能"
description: "Azure CLI 2.0 での拡張機能の使用"
keywords: "Azure CLI, 拡張機能"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 02/13/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 548c06c64cc98598a2bd24bcc5959e59bffb4930
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2018
---
# <a name="using-extensions-with-the-azure-cli-20"></a><span data-ttu-id="bb834-104">Azure CLI 2.0 での拡張機能の使用</span><span class="sxs-lookup"><span data-stu-id="bb834-104">Using extensions with the Azure CLI 2.0</span></span>

<span data-ttu-id="bb834-105">拡張機能は、Azure CLI 自体に付属していない独立したモジュールです。この拡張機能により、新しいコマンドで機能が追加されます。</span><span class="sxs-lookup"><span data-stu-id="bb834-105">Extensions are individual modules not shipped with the Azure CLI itself that add functionality through new commands.</span></span> <span data-ttu-id="bb834-106">これは試験段階またはリリース前のサービス、Microsoft の特別なツール、またはご自身で作成したカスタム機能である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bb834-106">These might be experimental or pre-release offerings, specialized tools from Microsoft, or custom features you write yourself.</span></span> <span data-ttu-id="bb834-107">拡張機能により、ご自身のニーズに合わせてある程度柔軟に CLI を変更できます。コア機能セットの一部として見なされない多数の追加パッケージを出荷する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="bb834-107">Extensions allow for a degree of flexibility with the CLI that let you modify it to your own needs, without having to ship a lot of additional packages that aren't considered part of the core feature set.</span></span>

<span data-ttu-id="bb834-108">この記事は、CLI 用の拡張機能をインストール、更新、および削除する方法を理解するうえで役立ちます。</span><span class="sxs-lookup"><span data-stu-id="bb834-108">This article helps you understand how to install, update, and remove extensions for the CLI.</span></span> <span data-ttu-id="bb834-109">また、拡張機能の動作に関する一般的な質問にも回答します。</span><span class="sxs-lookup"><span data-stu-id="bb834-109">It should also answer common questions about extension behavior.</span></span>

## <a name="finding-extensions"></a><span data-ttu-id="bb834-110">拡張機能の検索</span><span class="sxs-lookup"><span data-stu-id="bb834-110">Finding extensions</span></span>

<span data-ttu-id="bb834-111">使用できる拡張機能を確認するには、[az extension list-available](/cli/azure/extension?view=azure-cli-latest#az_extension_list_available) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="bb834-111">In order to know what extensions are available, you can use [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az_extension_list_available).</span></span> <span data-ttu-id="bb834-112">このコマンドにより、Microsoft が提供およびサポートする使用可能な公式拡張機能の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bb834-112">This command lists the available, official extensions which are provided and supported by Microsoft.</span></span>

## <a name="installing-extensions"></a><span data-ttu-id="bb834-113">拡張機能のインストール</span><span class="sxs-lookup"><span data-stu-id="bb834-113">Installing extensions</span></span>

<span data-ttu-id="bb834-114">インストールする拡張機能を見つけたら、[az extension add](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az_extension_add) を使用して取得します。</span><span class="sxs-lookup"><span data-stu-id="bb834-114">Once you have found an extension to install, use [az extension add](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az_extension_add) to get it.</span></span> <span data-ttu-id="bb834-115">その拡張機能が `az extension list-available` に表示される場合は、名前によってインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="bb834-115">If the extension is listed in `az extension list-available`, you can install the extension by name.</span></span>

```azurecli
az extension add --name <extension-name>
```

<span data-ttu-id="bb834-116">拡張機能のソースが外部リソースであるか、その拡張機能への直接リンクがある場合は、ソース URL またはローカル パスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="bb834-116">If the extension is from an external resource or you have a direct link to it, you can provide the source URL or local path.</span></span> <span data-ttu-id="bb834-117">これは、コンパイルされた Python の wheel 形式ファイルである "_必要があります_"。</span><span class="sxs-lookup"><span data-stu-id="bb834-117">This _must_ be a compiled Python wheel file.</span></span>

```azurecli
az extension add --source <URL-or-path>
```

<span data-ttu-id="bb834-118">インストールされた拡張機能は、`$AZURE_EXTENSION_DIR` シェル変数の値で確認できます。</span><span class="sxs-lookup"><span data-stu-id="bb834-118">Once an extension is installed, it can be found under the value of the `$AZURE_EXTENSION_DIR` shell variable.</span></span> <span data-ttu-id="bb834-119">この変数が設定されていない場合、既定では、この値は `$HOME/.azure/cliextensions` (Linux と macOS の場合) または `%USERPROFILE%\.azure\cliextensions` (Windows の場合) になります。</span><span class="sxs-lookup"><span data-stu-id="bb834-119">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

## <a name="updating-extensions"></a><span data-ttu-id="bb834-120">拡張機能の更新</span><span class="sxs-lookup"><span data-stu-id="bb834-120">Updating extensions</span></span>

<span data-ttu-id="bb834-121">拡張機能は名前によってのみ、[az extension update](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az_extension_update) を使用して更新できます。</span><span class="sxs-lookup"><span data-stu-id="bb834-121">Extensions can only be updated by name, using [az extension update](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az_extension_update).</span></span>

```azurecli
az extension update --name <extension-name>
```

<span data-ttu-id="bb834-122">何らかの理由により、拡張機能の名前を CLI で解決できない場合は、拡張機能を再インストールして更新します。</span><span class="sxs-lookup"><span data-stu-id="bb834-122">If an extension name cannot be resolved by the CLI for whatever reason, reinstall the extension to update it.</span></span> <span data-ttu-id="bb834-123">拡張機能がプレビューから移行し、CLI の組み込みコマンドになった可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="bb834-123">There is also the possibility that the extension was moved out of preview and became a built-in command for the CLI.</span></span> <span data-ttu-id="bb834-124">その場合は、CLI を更新し、拡張機能をアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="bb834-124">In that case, update the CLI and uninstall the extension.</span></span>

## <a name="uninstalling-extensions"></a><span data-ttu-id="bb834-125">拡張機能のアンインストール</span><span class="sxs-lookup"><span data-stu-id="bb834-125">Uninstalling extensions</span></span>

<span data-ttu-id="bb834-126">不要になった拡張機能は、[az extension remove](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az_extension_remove) を使用して削除できます。</span><span class="sxs-lookup"><span data-stu-id="bb834-126">If you no longer need an extension, it can be removed with [az extension remove](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az_extension_remove).</span></span>

```azurecli
az extension remove --name <extension-name>
```

<span data-ttu-id="bb834-127">また、手動で削除することもできます。それには、インストールした場所から拡張機能を削除します。</span><span class="sxs-lookup"><span data-stu-id="bb834-127">You can also remove an extension manually by deleting it from the location where it was installed.</span></span> <span data-ttu-id="bb834-128">これは、`$AZURE_EXTENSION_DIR` シェル変数の値になります。</span><span class="sxs-lookup"><span data-stu-id="bb834-128">This will be the value of the `$AZURE_EXTENSION_DIR` shell variable.</span></span> <span data-ttu-id="bb834-129">この変数が設定されていない場合、既定では、この値は `$HOME/.azure/cliextensions` (Linux と macOS の場合) または `%USERPROFILE%\.azure\cliextensions` (Windows の場合) になります。</span><span class="sxs-lookup"><span data-stu-id="bb834-129">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

```bash
rm -rf $AZURE_EXTENSION_DIR/<extension-name>
```

<span data-ttu-id="bb834-130">`az extension remove` を使用してアンインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bb834-130">It is recommended that you uninstall using `az extension remove`.</span></span>

## <a name="faq"></a><span data-ttu-id="bb834-131">FAQ</span><span class="sxs-lookup"><span data-stu-id="bb834-131">FAQ</span></span>

<span data-ttu-id="bb834-132">ここでは、CLI 拡張機能に関するその他の一般的な質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="bb834-132">Here are some answers to other common questions about CLI extensions.</span></span>

### <a name="what-file-formats-are-allowed-for-installation"></a><span data-ttu-id="bb834-133">インストールでは、どのファイル形式が許可されていますか。</span><span class="sxs-lookup"><span data-stu-id="bb834-133">What file formats are allowed for installation?</span></span>

<span data-ttu-id="bb834-134">現時点では、Python のコンパイルされた wheel 形式のみを拡張機能としてインストールできます。</span><span class="sxs-lookup"><span data-stu-id="bb834-134">Currently, only compiled Python wheels can be installed as extensions.</span></span>

### <a name="can-extensions-replace-existing-commands"></a><span data-ttu-id="bb834-135">拡張機能で既存のコマンドを置き換えることはできますか。</span><span class="sxs-lookup"><span data-stu-id="bb834-135">Can extensions replace existing commands?</span></span>

<span data-ttu-id="bb834-136">はい。</span><span class="sxs-lookup"><span data-stu-id="bb834-136">Yes.</span></span> <span data-ttu-id="bb834-137">拡張機能で既存のコマンドを置き換えることはできますが、置き換えられたコマンドを実行する前に、CLI によって警告が発せられます。</span><span class="sxs-lookup"><span data-stu-id="bb834-137">Extensions may replace existing commands, but before running a command that has been replaced the CLI will issue a warning.</span></span>

### <a name="how-can-i-tell-if-an-extension-is-in-pre-release"></a><span data-ttu-id="bb834-138">拡張機能がプレリリースかどうかをどのように確認できますか。</span><span class="sxs-lookup"><span data-stu-id="bb834-138">How can I tell if an extension is in pre-release?</span></span>

<span data-ttu-id="bb834-139">拡張機能がプレリリースかどうかは、それ自体のドキュメントとバージョン管理に示されています。</span><span class="sxs-lookup"><span data-stu-id="bb834-139">An extension should indicate through its own documentation and versioning if it is in pre-release.</span></span> <span data-ttu-id="bb834-140">また、Microsoft では、通常、CLI のプレビュー コマンドを拡張機能としてリリースし、製品がプレビュー段階を脱した時点で、その拡張機能をメインの CLI インターフェイスに移行させる予定です。</span><span class="sxs-lookup"><span data-stu-id="bb834-140">It is also common for Microsoft to release preview commands for the CLI as extensions, with plans to move them into the main CLI interface once the product is out of preview.</span></span>

### <a name="can-extensions-depend-upon-each-other"></a><span data-ttu-id="bb834-141">拡張機能は相互に依存できますか。</span><span class="sxs-lookup"><span data-stu-id="bb834-141">Can extensions depend upon each other?</span></span>

<span data-ttu-id="bb834-142">
いいえ。</span><span class="sxs-lookup"><span data-stu-id="bb834-142">No.</span></span> <span data-ttu-id="bb834-143">拡張機能は、相互に依存しない独立したパッケージである必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb834-143">Extensions must be individual packages which do not rely on one another.</span></span> <span data-ttu-id="bb834-144">これは、CLI では拡張機能が読み込まれるタイミングが不明であるため、依存関係が満たされる保証がないからです。</span><span class="sxs-lookup"><span data-stu-id="bb834-144">This is because the CLI gives no guarantee about when extensions are loaded, so dependencies could not be guaranteed to be satisfied.</span></span> <span data-ttu-id="bb834-145">拡張機能をインストールした場合、その拡張機能のみがインストールされます。また、他の拡張機能を削除しても、その拡張機能は動作し続けます。</span><span class="sxs-lookup"><span data-stu-id="bb834-145">Installing an extension installs that extension only, and it should continue to work even if you remove other extensions.</span></span>

### <a name="are-extensions-updated-along-with-the-cli"></a><span data-ttu-id="bb834-146">拡張機能は CLI と共に更新されますか。</span><span class="sxs-lookup"><span data-stu-id="bb834-146">Are extensions updated along with the CLI?</span></span>

<span data-ttu-id="bb834-147">
いいえ。</span><span class="sxs-lookup"><span data-stu-id="bb834-147">No.</span></span> <span data-ttu-id="bb834-148">「[拡張機能の更新](#updating-extensions)」で説明したように、拡張機能は個別に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb834-148">Extensions must be updated separately, as described in the [Updating extensions](#updating-extensions) section.</span></span>
