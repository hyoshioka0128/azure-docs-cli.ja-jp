---
title: Azure CLI 2.0 の拡張機能
description: Azure CLI 2.0 での拡張機能の使用
keywords: Azure CLI, 拡張機能
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/16/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 1b983faef4c1678763b3483192e94a6c96e24f32
ms.sourcegitcommit: 80189ff103c91f8c47ab8ebf586df815fff5dd5d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/07/2018
ms.locfileid: "34479479"
---
# <a name="using-extensions-with-the-azure-cli-20"></a><span data-ttu-id="14535-104">Azure CLI 2.0 での拡張機能の使用</span><span class="sxs-lookup"><span data-stu-id="14535-104">Using extensions with the Azure CLI 2.0</span></span>

<span data-ttu-id="14535-105">拡張機能は、Azure CLI 自体に付属していない独立したモジュールです。この拡張機能により、新しいコマンドで機能が追加されます。</span><span class="sxs-lookup"><span data-stu-id="14535-105">Extensions are individual modules not shipped with the Azure CLI itself that add functionality through new commands.</span></span> <span data-ttu-id="14535-106">これは試験段階またはリリース前のサービス、Microsoft の特別なツール、またはご自身で作成したカスタム機能である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="14535-106">These might be experimental or pre-release offerings, specialized tools from Microsoft, or custom features you write yourself.</span></span> <span data-ttu-id="14535-107">拡張機能により、ご自身のニーズに合わせてある程度柔軟に CLI を変更できます。コア機能セットの一部として見なされない多数の追加パッケージを出荷する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="14535-107">Extensions allow for a degree of flexibility with the CLI that let you modify it to your own needs, without having to ship a lot of additional packages that aren't considered part of the core feature set.</span></span>

<span data-ttu-id="14535-108">この記事は、CLI 用の拡張機能をインストール、更新、および削除する方法を理解するうえで役立ちます。</span><span class="sxs-lookup"><span data-stu-id="14535-108">This article helps you understand how to install, update, and remove extensions for the CLI.</span></span> <span data-ttu-id="14535-109">また、拡張機能の動作に関する一般的な質問にも回答します。</span><span class="sxs-lookup"><span data-stu-id="14535-109">It also answers common questions about extension behavior.</span></span>

## <a name="find-extensions"></a><span data-ttu-id="14535-110">拡張機能の検索</span><span class="sxs-lookup"><span data-stu-id="14535-110">Find extensions</span></span>

<span data-ttu-id="14535-111">使用できる拡張機能を確認するには、[az extension list-available](/cli/azure/extension#az-extension-list-available) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="14535-111">In order to know what extensions are available, you can use [az extension list-available](/cli/azure/extension#az-extension-list-available).</span></span> <span data-ttu-id="14535-112">このコマンドにより、Microsoft によって提供および管理されている公式の拡張機能が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="14535-112">This command lists the official extensions provided and maintained by Microsoft.</span></span>

```azurecli-interactive
az extension list-available --output table
```

<span data-ttu-id="14535-113">Microsoft では、ドキュメント サイトで [Microsoft 拡張機能の一覧](azure-cli-extensions-list.md)もホストしています。</span><span class="sxs-lookup"><span data-stu-id="14535-113">We also host a [list of Microsoft extensions](azure-cli-extensions-list.md) on the documentation site.</span></span>

## <a name="install-extensions"></a><span data-ttu-id="14535-114">拡張機能のインストール</span><span class="sxs-lookup"><span data-stu-id="14535-114">Install extensions</span></span>

<span data-ttu-id="14535-115">インストールする拡張機能を見つけたら、[az extension add](https://docs.microsoft.com/cli/azure/extension#az-extension-add) を使用して取得します。</span><span class="sxs-lookup"><span data-stu-id="14535-115">Once you have found an extension to install, use [az extension add](https://docs.microsoft.com/cli/azure/extension#az-extension-add) to get it.</span></span> <span data-ttu-id="14535-116">その拡張機能が `az extension list-available` に表示される場合は、名前によってインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="14535-116">If the extension is listed in `az extension list-available`, you can install the extension by name.</span></span>

```azurecli-interactive
az extension add --name <extension-name>
```

<span data-ttu-id="14535-117">拡張機能のソースが外部リソースであるか、その拡張機能への直接リンクがある場合は、ソース URL またはローカル パスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="14535-117">If the extension is from an external resource or you have a direct link to it, you can provide the source URL or local path.</span></span> <span data-ttu-id="14535-118">これは、コンパイルされた Python の wheel 形式ファイルである "_必要があります_"。</span><span class="sxs-lookup"><span data-stu-id="14535-118">This _must_ be a compiled Python wheel file.</span></span>

```azurecli-interactive
az extension add --source <URL-or-path>
```

<span data-ttu-id="14535-119">インストールされた拡張機能は、`$AZURE_EXTENSION_DIR` シェル変数の値で確認できます。</span><span class="sxs-lookup"><span data-stu-id="14535-119">Once an extension is installed, it can be found under the value of the `$AZURE_EXTENSION_DIR` shell variable.</span></span> <span data-ttu-id="14535-120">この変数が設定されていない場合、既定では、この値は `$HOME/.azure/cliextensions` (Linux と macOS の場合) または `%USERPROFILE%\.azure\cliextensions` (Windows の場合) になります。</span><span class="sxs-lookup"><span data-stu-id="14535-120">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

## <a name="update-extensions"></a><span data-ttu-id="14535-121">拡張機能の更新</span><span class="sxs-lookup"><span data-stu-id="14535-121">Update extensions</span></span>

<span data-ttu-id="14535-122">拡張機能を名前でインストールした場合、[az extension update](https://docs.microsoft.com/cli/azure/extension#az-extension-update) を使用してその拡張機能を更新できます。</span><span class="sxs-lookup"><span data-stu-id="14535-122">If an extension was installed by name, it can be updated using [az extension update](https://docs.microsoft.com/cli/azure/extension#az-extension-update).</span></span>

```azurecli-interactive
az extension update --name <extension-name>
```

<span data-ttu-id="14535-123">それ以外の場合は、「[拡張機能のインストール](#install-extensions)」の説明に従って、ソースから拡張機能を更新できます。</span><span class="sxs-lookup"><span data-stu-id="14535-123">Otherwise, an extension can be updated from source by following the [Install extensions](#install-extensions) instructions.</span></span>

<span data-ttu-id="14535-124">CLI を使用して拡張機能の名前を解決できない場合は、アンインストールしてから再インストールを試みてください。</span><span class="sxs-lookup"><span data-stu-id="14535-124">If an extension name cannot be resolved by the CLI, uninstall it and attempt to reinstall.</span></span> <span data-ttu-id="14535-125">拡張機能がプレビューから移行し、CLI の組み込みコマンドになった可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="14535-125">There's also the possibility that the extension was moved out of preview and became a built-in command for the CLI.</span></span> <span data-ttu-id="14535-126">「[Azure CLI 2.0 のインストール](install-azure-cli.md)」の説明に従って CLI の更新を試み、拡張機能のコマンドが追加されているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="14535-126">Try updating the CLI as described in [Install the Azure CLI 2.0](install-azure-cli.md) and see if the extension's commands were added.</span></span> 

## <a name="uninstall-extensions"></a><span data-ttu-id="14535-127">拡張機能のアンインストール</span><span class="sxs-lookup"><span data-stu-id="14535-127">Uninstall extensions</span></span>

<span data-ttu-id="14535-128">不要になった拡張機能は、[az extension remove](https://docs.microsoft.com/cli/azure/extension#az-extension-remove) を使用して削除できます。</span><span class="sxs-lookup"><span data-stu-id="14535-128">If you no longer need an extension, it can be removed with [az extension remove](https://docs.microsoft.com/cli/azure/extension#az-extension-remove).</span></span>

```azurecli-interactive
az extension remove --name <extension-name>
```

<span data-ttu-id="14535-129">また、手動で削除することもできます。それには、インストールした場所から拡張機能を削除します。</span><span class="sxs-lookup"><span data-stu-id="14535-129">You can also remove an extension manually by deleting it from the location where it was installed.</span></span> <span data-ttu-id="14535-130">これは、`$AZURE_EXTENSION_DIR` シェル変数の値になります。</span><span class="sxs-lookup"><span data-stu-id="14535-130">This will be the value of the `$AZURE_EXTENSION_DIR` shell variable.</span></span> <span data-ttu-id="14535-131">この変数が設定されていない場合、既定では、この値は `$HOME/.azure/cliextensions` (Linux と macOS の場合) または `%USERPROFILE%\.azure\cliextensions` (Windows の場合) になります。</span><span class="sxs-lookup"><span data-stu-id="14535-131">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

```bash
rm -rf $AZURE_EXTENSION_DIR/<extension-name>
```

<span data-ttu-id="14535-132">`az extension remove` を使用してアンインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="14535-132">It is recommended that you uninstall using `az extension remove`.</span></span>

## <a name="faq"></a><span data-ttu-id="14535-133">FAQ</span><span class="sxs-lookup"><span data-stu-id="14535-133">FAQ</span></span>

<span data-ttu-id="14535-134">ここでは、CLI 拡張機能に関するその他の一般的な質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="14535-134">Here are some answers to other common questions about CLI extensions.</span></span>

### <a name="what-file-formats-are-allowed-for-installation"></a><span data-ttu-id="14535-135">インストールでは、どのファイル形式が許可されていますか。</span><span class="sxs-lookup"><span data-stu-id="14535-135">What file formats are allowed for installation?</span></span>

<span data-ttu-id="14535-136">現時点では、Python のコンパイルされた wheel 形式のみを拡張機能としてインストールできます。</span><span class="sxs-lookup"><span data-stu-id="14535-136">Currently, only compiled Python wheels can be installed as extensions.</span></span>

### <a name="can-extensions-replace-existing-commands"></a><span data-ttu-id="14535-137">拡張機能で既存のコマンドを置き換えることはできますか。</span><span class="sxs-lookup"><span data-stu-id="14535-137">Can extensions replace existing commands?</span></span>

<span data-ttu-id="14535-138">はい。</span><span class="sxs-lookup"><span data-stu-id="14535-138">Yes.</span></span> <span data-ttu-id="14535-139">拡張機能で既存のコマンドを置き換えることはできますが、置き換えられたコマンドを実行する前に、CLI によって警告が発せられます。</span><span class="sxs-lookup"><span data-stu-id="14535-139">Extensions may replace existing commands, but before running a command that has been replaced the CLI will issue a warning.</span></span>

### <a name="how-can-i-tell-if-an-extension-is-in-pre-release"></a><span data-ttu-id="14535-140">拡張機能がプレリリースかどうかをどのように確認できますか。</span><span class="sxs-lookup"><span data-stu-id="14535-140">How can I tell if an extension is in pre-release?</span></span>

<span data-ttu-id="14535-141">拡張機能がプレリリースかどうかは、それ自体のドキュメントとバージョン管理に示されています。</span><span class="sxs-lookup"><span data-stu-id="14535-141">An extension should indicate through its own documentation and versioning if it is in pre-release.</span></span> <span data-ttu-id="14535-142">また、Microsoft では、通常、CLI のプレビュー コマンドを拡張機能としてリリースし、製品がプレビュー段階を脱した時点で、その拡張機能をメインの CLI インターフェイスに移行させる予定です。</span><span class="sxs-lookup"><span data-stu-id="14535-142">It is also common for Microsoft to release preview commands for the CLI as extensions, with plans to move them into the main CLI interface once the product is out of preview.</span></span>

### <a name="can-extensions-depend-upon-each-other"></a><span data-ttu-id="14535-143">拡張機能は相互に依存できますか。</span><span class="sxs-lookup"><span data-stu-id="14535-143">Can extensions depend upon each other?</span></span>

<span data-ttu-id="14535-144">いいえ。</span><span class="sxs-lookup"><span data-stu-id="14535-144">No.</span></span> <span data-ttu-id="14535-145">拡張機能は、相互に依存しない独立したパッケージである必要があります。</span><span class="sxs-lookup"><span data-stu-id="14535-145">Extensions must be individual packages which do not rely on one another.</span></span> <span data-ttu-id="14535-146">これは、CLI では拡張機能が読み込まれるタイミングが不明であるため、依存関係が満たされる保証がないからです。</span><span class="sxs-lookup"><span data-stu-id="14535-146">This is because the CLI gives no guarantee about when extensions are loaded, so dependencies could not be guaranteed to be satisfied.</span></span> <span data-ttu-id="14535-147">拡張機能をインストールした場合、その拡張機能のみがインストールされます。また、他の拡張機能を削除しても、その拡張機能は動作し続けます。</span><span class="sxs-lookup"><span data-stu-id="14535-147">Installing an extension installs that extension only, and it should continue to work even if you remove other extensions.</span></span>

### <a name="are-extensions-updated-along-with-the-cli"></a><span data-ttu-id="14535-148">拡張機能は CLI と共に更新されますか。</span><span class="sxs-lookup"><span data-stu-id="14535-148">Are extensions updated along with the CLI?</span></span>

<span data-ttu-id="14535-149">いいえ。</span><span class="sxs-lookup"><span data-stu-id="14535-149">No.</span></span> <span data-ttu-id="14535-150">「[拡張機能の更新](#update-extensions)」で説明したように、拡張機能は個別に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="14535-150">Extensions must be updated separately, as described in [Update extensions](#update-extensions).</span></span>
