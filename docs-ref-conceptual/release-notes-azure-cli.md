---
title: Azure CLI 2.0 リリース ノート
description: Azure CLI 2.0 の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 06/01/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 72e667d74ff8d55f26ecbf3b3c8845c9c03b56be
ms.sourcegitcommit: 5c80e96e96f9608c92a94fa4a9c4afb25099f3fc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/13/2018
ms.locfileid: "35512905"
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="b141f-103">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="b141f-103">Azure CLI 2.0 release notes</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="b141f-104">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b141f-104">June 13, 2018</span></span>

<span data-ttu-id="b141f-105">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="b141f-105">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="b141f-106">AKS</span><span class="sxs-lookup"><span data-stu-id="b141f-106">AKS</span></span>

* <span data-ttu-id="b141f-107">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-107">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="b141f-108">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-108">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span> 
* <span data-ttu-id="b141f-109">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-109">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="b141f-110">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-110">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="b141f-111">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-111">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-112">AppService</span><span class="sxs-lookup"><span data-stu-id="b141f-112">AppService</span></span>

* <span data-ttu-id="b141f-113">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-113">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="b141f-114">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="b141f-114">June 5, 2018</span></span>

<span data-ttu-id="b141f-115">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="b141f-115">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="b141f-116">対話</span><span class="sxs-lookup"><span data-stu-id="b141f-116">Interactive</span></span>

* <span data-ttu-id="b141f-117">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-117">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="b141f-118">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="b141f-118">June 5, 2018</span></span>

<span data-ttu-id="b141f-119">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="b141f-119">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="b141f-120">コア</span><span class="sxs-lookup"><span data-stu-id="b141f-120">Core</span></span>

* <span data-ttu-id="b141f-121">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-121">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="b141f-122">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="b141f-122">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="b141f-123">ACR</span><span class="sxs-lookup"><span data-stu-id="b141f-123">ACR</span></span>

* <span data-ttu-id="b141f-124">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-124">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="b141f-125">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-125">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="b141f-126">AKS</span><span class="sxs-lookup"><span data-stu-id="b141f-126">AKS</span></span>

* <span data-ttu-id="b141f-127">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-127">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="b141f-128">Batch</span><span class="sxs-lookup"><span data-stu-id="b141f-128">Batch</span></span>

* <span data-ttu-id="b141f-129">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-129">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="b141f-130">IoT</span><span class="sxs-lookup"><span data-stu-id="b141f-130">IOT</span></span>

* <span data-ttu-id="b141f-131">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-131">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="b141f-132">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-132">Network</span></span>

* <span data-ttu-id="b141f-133">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="b141f-133">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="b141f-134">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="b141f-134">Policy Insights</span></span>

* <span data-ttu-id="b141f-135">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b141f-135">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="b141f-136">ARM</span><span class="sxs-lookup"><span data-stu-id="b141f-136">ARM</span></span>

* <span data-ttu-id="b141f-137">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-137">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="b141f-138">SQL</span><span class="sxs-lookup"><span data-stu-id="b141f-138">SQL</span></span>

* <span data-ttu-id="b141f-139">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-139">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="b141f-140">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-140">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="b141f-141">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-141">Storage</span></span>

* <span data-ttu-id="b141f-142">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-142">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-143">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-143">VM</span></span>

* <span data-ttu-id="b141f-144">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-144">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="b141f-145">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-145">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="b141f-146">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-146">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="b141f-147">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="b141f-147">May 22, 2018</span></span>

<span data-ttu-id="b141f-148">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="b141f-148">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="b141f-149">コア</span><span class="sxs-lookup"><span data-stu-id="b141f-149">Core</span></span>

* <span data-ttu-id="b141f-150">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-150">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-151">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-151">ACS</span></span>

* <span data-ttu-id="b141f-152">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-152">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="b141f-153">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-153">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-154">AppService</span><span class="sxs-lookup"><span data-stu-id="b141f-154">AppService</span></span>

* <span data-ttu-id="b141f-155">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="b141f-155">Improved generic update commands</span></span>
* <span data-ttu-id="b141f-156">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-156">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="b141f-157">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b141f-157">Container</span></span>

* <span data-ttu-id="b141f-158">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-158">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="b141f-159">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-159">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="b141f-160">内線番号</span><span class="sxs-lookup"><span data-stu-id="b141f-160">Extension</span></span>

* <span data-ttu-id="b141f-161">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="b141f-161">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="b141f-162">対話</span><span class="sxs-lookup"><span data-stu-id="b141f-162">Interactive</span></span>

* <span data-ttu-id="b141f-163">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-163">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="b141f-164">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="b141f-164">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="b141f-165">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b141f-165">KeyVault</span></span>

* <span data-ttu-id="b141f-166">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-166">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="b141f-167">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-167">Network</span></span>

* <span data-ttu-id="b141f-168">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-168">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="b141f-169">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-169">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="b141f-170">SQL</span><span class="sxs-lookup"><span data-stu-id="b141f-170">SQL</span></span>

* <span data-ttu-id="b141f-171">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-171">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="b141f-172">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-172">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="b141f-173">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-173">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span> 
    * <span data-ttu-id="b141f-174">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-174">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="b141f-175">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-175">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="b141f-176">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="b141f-176">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="b141f-177">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="b141f-177">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="b141f-178">`edition`</span><span class="sxs-lookup"><span data-stu-id="b141f-178">`edition`.</span></span> <span data-ttu-id="b141f-179">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="b141f-179">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="b141f-180">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="b141f-180">`elasticPoolName`.</span></span> <span data-ttu-id="b141f-181">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="b141f-181">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="b141f-182">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-182">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="b141f-183">`edition`</span><span class="sxs-lookup"><span data-stu-id="b141f-183">`edition`.</span></span> <span data-ttu-id="b141f-184">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b141f-184">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="b141f-185">`dtu`</span><span class="sxs-lookup"><span data-stu-id="b141f-185">`dtu`.</span></span> <span data-ttu-id="b141f-186">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b141f-186">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="b141f-187">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="b141f-187">`databaseDtuMin`.</span></span> <span data-ttu-id="b141f-188">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b141f-188">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="b141f-189">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="b141f-189">`databaseDtuMax`.</span></span> <span data-ttu-id="b141f-190">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b141f-190">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="b141f-191">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-191">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="b141f-192">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-192">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-193">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-193">Storage</span></span>

* <span data-ttu-id="b141f-194">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-194">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="b141f-195">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-195">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-196">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-196">VM</span></span>

* <span data-ttu-id="b141f-197">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-197">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="b141f-198">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="b141f-198">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="b141f-199">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-199">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="b141f-200">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-200">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="b141f-201">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-201">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="b141f-202">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="b141f-202">May 7, 2018</span></span>

<span data-ttu-id="b141f-203">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="b141f-203">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="b141f-204">コア</span><span class="sxs-lookup"><span data-stu-id="b141f-204">Core</span></span>

* <span data-ttu-id="b141f-205">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-205">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="b141f-206">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-206">Added limited support for positional arguments</span></span>
* <span data-ttu-id="b141f-207">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-207">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="b141f-208">#5591</span><span class="sxs-lookup"><span data-stu-id="b141f-208">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="b141f-209">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-209">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="b141f-210">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="b141f-210">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="b141f-211">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-211">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="b141f-212">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-212">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="b141f-213">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-213">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="b141f-214">ACR</span><span class="sxs-lookup"><span data-stu-id="b141f-214">ACR</span></span>

* <span data-ttu-id="b141f-215">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-215">Added ACR Build commands</span></span>
* <span data-ttu-id="b141f-216">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-216">Improved resource not found error messages</span></span>
* <span data-ttu-id="b141f-217">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-217">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="b141f-218">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-218">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="b141f-219">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-219">Improved repository commands error messages</span></span>
* <span data-ttu-id="b141f-220">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="b141f-220">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-221">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-221">ACS</span></span>

* <span data-ttu-id="b141f-222">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-222">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="b141f-223">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-223">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="b141f-224">AMS</span><span class="sxs-lookup"><span data-stu-id="b141f-224">AMS</span></span>

* <span data-ttu-id="b141f-225">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="b141f-225">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-226">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-226">Appservice</span></span>

* <span data-ttu-id="b141f-227">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-227">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="b141f-228">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-228">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="b141f-229">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-229">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="b141f-230">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-230">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="b141f-231">Batch AI</span><span class="sxs-lookup"><span data-stu-id="b141f-231">Batch AI</span></span>

* <span data-ttu-id="b141f-232">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-232">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="b141f-233">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="b141f-233">Cognitive Services</span></span>

* <span data-ttu-id="b141f-234">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-234">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="b141f-235">消費</span><span class="sxs-lookup"><span data-stu-id="b141f-235">Consumption</span></span>

* <span data-ttu-id="b141f-236">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-236">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="b141f-237">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b141f-237">Container</span></span>

* <span data-ttu-id="b141f-238">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-238">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="b141f-239">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b141f-239">Cosmos DB</span></span>

* <span data-ttu-id="b141f-240">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="b141f-240">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="b141f-241">DMS</span><span class="sxs-lookup"><span data-stu-id="b141f-241">DMS</span></span>

* <span data-ttu-id="b141f-242">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-242">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="b141f-243">内線番号</span><span class="sxs-lookup"><span data-stu-id="b141f-243">Extension</span></span>

* <span data-ttu-id="b141f-244">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-244">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="b141f-245">対話</span><span class="sxs-lookup"><span data-stu-id="b141f-245">Interactive</span></span>

* <span data-ttu-id="b141f-246">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-246">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="b141f-247">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="b141f-247">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="b141f-248">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-248">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="b141f-249">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-249">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="b141f-250">ラボ</span><span class="sxs-lookup"><span data-stu-id="b141f-250">Lab</span></span>

* <span data-ttu-id="b141f-251">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-251">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="b141f-252">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-252">Network</span></span>

* <span data-ttu-id="b141f-253">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-253">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span> 
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="b141f-254">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b141f-254">Profile</span></span>

* <span data-ttu-id="b141f-255">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-255">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="b141f-256">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-256">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="b141f-257">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-257">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="b141f-258">Redis</span><span class="sxs-lookup"><span data-stu-id="b141f-258">Redis</span></span>

* <span data-ttu-id="b141f-259">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-259">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="b141f-260">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="b141f-260">Deprecated `redis list-all`.</span></span> <span data-ttu-id="b141f-261">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="b141f-261">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="b141f-262">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-262">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="b141f-263">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-263">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="b141f-264">役割</span><span class="sxs-lookup"><span data-stu-id="b141f-264">Role</span></span>

* <span data-ttu-id="b141f-265">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-265">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-266">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-266">Storage</span></span>

* <span data-ttu-id="b141f-267">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="b141f-267">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="b141f-268">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="b141f-268">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="b141f-269">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="b141f-269">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="b141f-270">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="b141f-270">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="b141f-271">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-271">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-272">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-272">VM</span></span>

* <span data-ttu-id="b141f-273">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-273">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="b141f-274">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-274">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="b141f-275">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="b141f-275">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="b141f-276">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-276">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="b141f-277">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-277">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="b141f-278">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-278">Added write accelerator support</span></span> 
* <span data-ttu-id="b141f-279">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-279">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="b141f-280">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-280">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="b141f-281">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-281">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="b141f-282">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="b141f-282">April 10, 2018</span></span>

<span data-ttu-id="b141f-283">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="b141f-283">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="b141f-284">ACR</span><span class="sxs-lookup"><span data-stu-id="b141f-284">ACR</span></span>

* <span data-ttu-id="b141f-285">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-285">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-286">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-286">ACS</span></span>

* <span data-ttu-id="b141f-287">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-287">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-288">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-288">Appservice</span></span>

* [重大な変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="b141f-290">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-290">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="b141f-291">BatchAI</span><span class="sxs-lookup"><span data-stu-id="b141f-291">BatchAI</span></span>

* <span data-ttu-id="b141f-292">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-292">Added support for 2018-03-01 API</span></span>

 - <span data-ttu-id="b141f-293">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="b141f-293">Job level mounting</span></span>
 - <span data-ttu-id="b141f-294">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="b141f-294">Environment variables with secret values</span></span>
 - <span data-ttu-id="b141f-295">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="b141f-295">Performance counters settings</span></span>
 - <span data-ttu-id="b141f-296">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="b141f-296">Reporting of job specific path segment</span></span>
 - <span data-ttu-id="b141f-297">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="b141f-297">Support for subfolders in list files api</span></span>
 - <span data-ttu-id="b141f-298">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="b141f-298">Usage and limits reporting</span></span>
 - <span data-ttu-id="b141f-299">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="b141f-299">Allow to specify caching type for NFS servers</span></span>
 - <span data-ttu-id="b141f-300">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="b141f-300">Support for custom images</span></span>
 - <span data-ttu-id="b141f-301">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-301">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="b141f-302">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-302">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="b141f-303">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="b141f-303">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="b141f-304">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="b141f-304">National clouds are supported</span></span>
* <span data-ttu-id="b141f-305">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-305">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="b141f-306">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-306">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="b141f-307">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-307">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="b141f-308">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-308">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="b141f-309">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="b141f-309">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="b141f-310">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="b141f-310">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="b141f-311">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-311">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="b141f-312">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-312">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="b141f-313">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="b141f-313">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="b141f-314">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-314">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="b141f-315">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="b141f-315">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="b141f-316">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="b141f-316">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="b141f-317">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-317">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="b141f-318">課金</span><span class="sxs-lookup"><span data-stu-id="b141f-318">Billing</span></span>

* <span data-ttu-id="b141f-319">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-319">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="b141f-320">消費</span><span class="sxs-lookup"><span data-stu-id="b141f-320">Consumption</span></span>

* <span data-ttu-id="b141f-321">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-321">Added `marketplace` commands</span></span>
* <span data-ttu-id="b141f-322">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-322">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="b141f-323">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-323">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="b141f-324">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-324">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="b141f-325">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-325">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="b141f-326">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-326">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="b141f-327">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b141f-327">Container</span></span>

* <span data-ttu-id="b141f-328">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-328">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="b141f-329">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-329">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="b141f-330">内線番号</span><span class="sxs-lookup"><span data-stu-id="b141f-330">Extension</span></span>

* <span data-ttu-id="b141f-331">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-331">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="b141f-332">対話</span><span class="sxs-lookup"><span data-stu-id="b141f-332">Interactive</span></span>

* <span data-ttu-id="b141f-333">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-333">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="b141f-334">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-334">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="b141f-335">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-335">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="b141f-336">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-336">Network</span></span>

* <span data-ttu-id="b141f-337">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-337">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="b141f-338">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-338">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="b141f-339">#4910</span><span class="sxs-lookup"><span data-stu-id="b141f-339">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="b141f-340">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-340">Added `ddos-protection` commands to create DDoS protection plans</span></span> 
* <span data-ttu-id="b141f-341">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="b141f-341">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="b141f-342">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-342">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="b141f-343">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-343">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="b141f-344">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-344">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="b141f-345">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b141f-345">Profile</span></span>

* <span data-ttu-id="b141f-346">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-346">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="b141f-347">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-347">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="b141f-348">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b141f-348">RDBMS</span></span>

* <span data-ttu-id="b141f-349">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-349">Added `georestore` command</span></span>
* <span data-ttu-id="b141f-350">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-350">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="b141f-351">リソース</span><span class="sxs-lookup"><span data-stu-id="b141f-351">Resource</span></span>

* <span data-ttu-id="b141f-352">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-352">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="b141f-353">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-353">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="b141f-354">SQL</span><span class="sxs-lookup"><span data-stu-id="b141f-354">SQL</span></span>

* <span data-ttu-id="b141f-355">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-355">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-356">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-356">Storage</span></span>

* <span data-ttu-id="b141f-357">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-357">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-358">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-358">VM</span></span>

* <span data-ttu-id="b141f-359">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-359">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="b141f-360">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-360">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [重大な変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="b141f-362">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-362">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="b141f-363">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-363">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="b141f-364">#5718</span><span class="sxs-lookup"><span data-stu-id="b141f-364">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="b141f-365">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-365">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="b141f-366">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="b141f-366">March 27, 2018</span></span>

<span data-ttu-id="b141f-367">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="b141f-367">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="b141f-368">コア</span><span class="sxs-lookup"><span data-stu-id="b141f-368">Core</span></span>

* <span data-ttu-id="b141f-369">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="b141f-369">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-370">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-370">ACS</span></span>

* <span data-ttu-id="b141f-371">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-371">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-372">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-372">Appservice</span></span>

* <span data-ttu-id="b141f-373">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-373">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="b141f-374">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-374">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="b141f-375">Backup
</span><span class="sxs-lookup"><span data-stu-id="b141f-375">Backup</span></span>

* <span data-ttu-id="b141f-376">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-376">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="b141f-377">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="b141f-377">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="b141f-378">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-378">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
  * `backup container show`
  * `backup item set-policy`
  * `backup item show`
  * `backup job show`
  * `backup job stop`
  * `backup job wait`
  * `backup policy delete`
  * `backup policy get-default-for-vm`
  * `backup policy list-associated-items`
  * `backup policy set`
  * `backup policy show`
  * `backup protection backup-now`
  * `backup protection disable`
  * `backup protection enable-for-vm`
  * `backup recoverypoint show`
  * `backup restore files mount-rp`
  * `backup restore files unmount-rp`
  * `backup restore restore-disks`
  * `backup vault delete`
  * `backup vault show`
* <span data-ttu-id="b141f-379">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-379">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="b141f-380">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b141f-380">Container</span></span>

* <span data-ttu-id="b141f-381">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-381">Added `container exec` command.</span></span> <span data-ttu-id="b141f-382">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="b141f-382">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="b141f-383">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="b141f-383">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="b141f-384">内線番号</span><span class="sxs-lookup"><span data-stu-id="b141f-384">Extension</span></span>

* <span data-ttu-id="b141f-385">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-385">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="b141f-386">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-386">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="b141f-387">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-387">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="b141f-388">対話</span><span class="sxs-lookup"><span data-stu-id="b141f-388">Interactive</span></span>

* <span data-ttu-id="b141f-389">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-389">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="b141f-390">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-390">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="b141f-391">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="b141f-391">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="b141f-392">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="b141f-392">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="b141f-393">ラボ</span><span class="sxs-lookup"><span data-stu-id="b141f-393">Lab</span></span>

* <span data-ttu-id="b141f-394">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-394">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="b141f-395">監視</span><span class="sxs-lookup"><span data-stu-id="b141f-395">Monitor</span></span>

* <span data-ttu-id="b141f-396">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="b141f-396">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="b141f-397">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました: `metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="b141f-397">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="b141f-398">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="b141f-398">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="b141f-399">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-399">Network</span></span>

* <span data-ttu-id="b141f-400">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-400">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="b141f-401">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b141f-401">Profile</span></span>

* <span data-ttu-id="b141f-402">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-402">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="b141f-403">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b141f-403">RDBMS</span></span>

* <span data-ttu-id="b141f-404">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-404">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="b141f-405">リソース</span><span class="sxs-lookup"><span data-stu-id="b141f-405">Resource</span></span>

* [重大な変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="b141f-407">役割</span><span class="sxs-lookup"><span data-stu-id="b141f-407">Role</span></span>

* <span data-ttu-id="b141f-408">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-408">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="b141f-409">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-409">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="b141f-410">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-410">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="b141f-411">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-411">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="b141f-412">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-412">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-413">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-413">Storage</span></span>

* <span data-ttu-id="b141f-414">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-414">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="b141f-415">[#4049](https://github.com/Azure/azure-cli/issues/4049) (追加 BLOB のアップロードで条件のパラメーターが無視される問題) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-415">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-416">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-416">VM</span></span>

* <span data-ttu-id="b141f-417">インスタンス数が 100 を超えるセットに対する今後の重大な変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-417">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="b141f-418">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-418">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="b141f-419">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-419">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="b141f-420">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-420">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="b141f-421">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b141f-421">March 13, 2018</span></span>

<span data-ttu-id="b141f-422">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="b141f-422">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="b141f-423">ACR</span><span class="sxs-lookup"><span data-stu-id="b141f-423">ACR</span></span>

* <span data-ttu-id="b141f-424">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-424">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="b141f-425">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-425">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="b141f-426">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-426">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-427">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-427">ACS</span></span>

* <span data-ttu-id="b141f-428">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-428">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="b141f-429">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-429">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="b141f-430">Advisor</span><span class="sxs-lookup"><span data-stu-id="b141f-430">Advisor</span></span>

* <span data-ttu-id="b141f-431">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-431">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="b141f-432">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-432">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="b141f-433">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-433">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span> 
* <span data-ttu-id="b141f-434">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-434">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="b141f-435">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-435">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-436">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-436">Appservice</span></span>

* <span data-ttu-id="b141f-437">を非推奨にしました `[webapp|functionapp] assign-identity`</span><span class="sxs-lookup"><span data-stu-id="b141f-437">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="b141f-438">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-438">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="b141f-439">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="b141f-439">Eventhubs</span></span>

* <span data-ttu-id="b141f-440">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b141f-440">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="b141f-441">内線番号</span><span class="sxs-lookup"><span data-stu-id="b141f-441">Extension</span></span>

* <span data-ttu-id="b141f-442">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-442">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="b141f-443">対話</span><span class="sxs-lookup"><span data-stu-id="b141f-443">Interactive</span></span>

* <span data-ttu-id="b141f-444">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました: 異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="b141f-444">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="b141f-445">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました: スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="b141f-445">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="b141f-446">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました: コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="b141f-446">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="b141f-447">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-447">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="b141f-448">監視</span><span class="sxs-lookup"><span data-stu-id="b141f-448">Monitor</span></span>

* <span data-ttu-id="b141f-449">コマンドを非推奨にしました `monitor autoscale-settings`</span><span class="sxs-lookup"><span data-stu-id="b141f-449">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="b141f-450">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-450">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="b141f-451">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-451">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="b141f-452">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-452">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="b141f-453">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-453">Network</span></span>

* <span data-ttu-id="b141f-454">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-454">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="b141f-455">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-455">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="b141f-456">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-456">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="b141f-457">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-457">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="b141f-458">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b141f-458">Profile</span></span>

* <span data-ttu-id="b141f-459">の `--msi` パラメーターを非推奨にしました `az login`</span><span class="sxs-lookup"><span data-stu-id="b141f-459">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="b141f-460">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-460">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="b141f-461">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b141f-461">RDBMS</span></span>

* <span data-ttu-id="b141f-462">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-462">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="b141f-463">Service Bus</span><span class="sxs-lookup"><span data-stu-id="b141f-463">Service Bus</span></span>

* <span data-ttu-id="b141f-464">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b141f-464">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-465">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-465">Storage</span></span>

* <span data-ttu-id="b141f-466">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-466">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="b141f-467">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました: Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="b141f-467">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-468">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-468">VM</span></span>

* <span data-ttu-id="b141f-469">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-469">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="b141f-470">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-470">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="b141f-471">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-471">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="b141f-472">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-472">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="b141f-473">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="b141f-473">February 27, 2018</span></span>

<span data-ttu-id="b141f-474">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="b141f-474">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="b141f-475">コア</span><span class="sxs-lookup"><span data-stu-id="b141f-475">Core</span></span>

* <span data-ttu-id="b141f-476">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正: Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="b141f-476">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="b141f-477">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-477">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="b141f-478">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-478">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-479">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-479">ACS</span></span>

* <span data-ttu-id="b141f-480">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-480">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="b141f-481">修正された問題: ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="b141f-481">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="b141f-482">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-482">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="b141f-483">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-483">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-484">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-484">Appservice</span></span>

* <span data-ttu-id="b141f-485">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="b141f-485">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="b141f-486">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="b141f-486">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="b141f-487">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="b141f-487">Cognitive Services</span></span>

* <span data-ttu-id="b141f-488">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="b141f-488">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="b141f-489">消費</span><span class="sxs-lookup"><span data-stu-id="b141f-489">Consumption</span></span>

* <span data-ttu-id="b141f-490">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-490">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="b141f-491">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="b141f-491">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="b141f-492">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b141f-492">Container</span></span>

* <span data-ttu-id="b141f-493">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-493">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="b141f-494">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-494">Network</span></span>

* <span data-ttu-id="b141f-495">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正: `network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="b141f-495">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="b141f-496">リソース</span><span class="sxs-lookup"><span data-stu-id="b141f-496">Resource</span></span>

* <span data-ttu-id="b141f-497">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-497">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="b141f-498">役割</span><span class="sxs-lookup"><span data-stu-id="b141f-498">Role</span></span>

* <span data-ttu-id="b141f-499">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-499">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="b141f-500">SQL</span><span class="sxs-lookup"><span data-stu-id="b141f-500">SQL</span></span>

* <span data-ttu-id="b141f-501">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-501">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-502">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-502">Storage</span></span>

* <span data-ttu-id="b141f-503">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-503">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-504">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-504">VM</span></span>

* <span data-ttu-id="b141f-505">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-505">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="b141f-506">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b141f-506">February 13, 2018</span></span>

<span data-ttu-id="b141f-507">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="b141f-507">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="b141f-508">コア</span><span class="sxs-lookup"><span data-stu-id="b141f-508">Core</span></span>

* <span data-ttu-id="b141f-509">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-509">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-510">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-510">ACS</span></span>

* <span data-ttu-id="b141f-511">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-511">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="b141f-512">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-512">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="b141f-513">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-513">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="b141f-514">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="b141f-514">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="b141f-515">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-515">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="b141f-516">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="b141f-516">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="b141f-517">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-517">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="b141f-518">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="b141f-518">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-519">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-519">Appservice</span></span>

* <span data-ttu-id="b141f-520">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-520">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="b141f-521">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-521">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="b141f-522">CDN</span><span class="sxs-lookup"><span data-stu-id="b141f-522">CDN</span></span>

* <span data-ttu-id="b141f-523">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-523">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="b141f-524">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b141f-524">Container</span></span>

* <span data-ttu-id="b141f-525">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-525">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="b141f-526">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-526">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b141f-527">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b141f-527">CosmosDB</span></span>

* <span data-ttu-id="b141f-528">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-528">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="b141f-529">内線番号</span><span class="sxs-lookup"><span data-stu-id="b141f-529">Extension</span></span>

* <span data-ttu-id="b141f-530">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-530">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="b141f-531">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-531">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="b141f-532">フィードバック</span><span class="sxs-lookup"><span data-stu-id="b141f-532">Feedback</span></span>

* <span data-ttu-id="b141f-533">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-533">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="b141f-534">対話</span><span class="sxs-lookup"><span data-stu-id="b141f-534">Interactive</span></span>

* <span data-ttu-id="b141f-535">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-535">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="b141f-536">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-536">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="b141f-537">IoT</span><span class="sxs-lookup"><span data-stu-id="b141f-537">IoT</span></span>

* <span data-ttu-id="b141f-538">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-538">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="b141f-539">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-539">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="b141f-540">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-540">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="b141f-541">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-541">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="b141f-542">監視</span><span class="sxs-lookup"><span data-stu-id="b141f-542">Monitor</span></span>

* <span data-ttu-id="b141f-543">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-543">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="b141f-544">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-544">Network</span></span>

* <span data-ttu-id="b141f-545">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-545">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="b141f-546">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b141f-546">Profile</span></span>

* <span data-ttu-id="b141f-547">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-547">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="b141f-548">リソース</span><span class="sxs-lookup"><span data-stu-id="b141f-548">Resource</span></span>

* <span data-ttu-id="b141f-549">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-549">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="b141f-550">役割</span><span class="sxs-lookup"><span data-stu-id="b141f-550">Role</span></span>

* <span data-ttu-id="b141f-551">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-551">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="b141f-552">SQL</span><span class="sxs-lookup"><span data-stu-id="b141f-552">SQL</span></span>

* <span data-ttu-id="b141f-553">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-553">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="b141f-554">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-554">Added `sql db rename`</span></span>
* <span data-ttu-id="b141f-555">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-555">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-556">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-556">Storage</span></span>

* <span data-ttu-id="b141f-557">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-557">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-558">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-558">VM</span></span>

* <span data-ttu-id="b141f-559">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-559">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="b141f-560">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-560">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="b141f-561">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="b141f-561">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="b141f-562">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="b141f-562">January 31, 2018</span></span>

<span data-ttu-id="b141f-563">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="b141f-563">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="b141f-564">コア</span><span class="sxs-lookup"><span data-stu-id="b141f-564">Core</span></span>

* <span data-ttu-id="b141f-565">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-565">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="b141f-566">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-566">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="b141f-567">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-567">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="b141f-568">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="b141f-568">Use `--verbose` to see</span></span>
* <span data-ttu-id="b141f-569">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="b141f-569">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-570">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-570">ACS</span></span>

* <span data-ttu-id="b141f-571">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="b141f-571">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="b141f-572">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="b141f-572">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-573">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-573">Appservice</span></span>

* <span data-ttu-id="b141f-574">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="b141f-574">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="b141f-575">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-575">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="b141f-576">CDN</span><span class="sxs-lookup"><span data-stu-id="b141f-576">CDN</span></span>

* <span data-ttu-id="b141f-577">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-577">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b141f-578">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b141f-578">CosmosDB</span></span>

* <span data-ttu-id="b141f-579">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-579">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="b141f-580">対話</span><span class="sxs-lookup"><span data-stu-id="b141f-580">Interactive</span></span>

* <span data-ttu-id="b141f-581">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-581">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="b141f-582">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-582">Network</span></span>

* <span data-ttu-id="b141f-583">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-583">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="b141f-584">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-584">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="b141f-585">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-585">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="b141f-586">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-586">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="b141f-587">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-587">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="b141f-588">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-588">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="b141f-589">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-589">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="b141f-590">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-590">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="b141f-591">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-591">Fixed issue where certain records were imported twice with `dns zone import`</span></span> 
* <span data-ttu-id="b141f-592">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="b141f-592">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="b141f-593">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b141f-593">Profile</span></span>

* <span data-ttu-id="b141f-594">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-594">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="b141f-595">リソース</span><span class="sxs-lookup"><span data-stu-id="b141f-595">Resource</span></span>

* <span data-ttu-id="b141f-596">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-596">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-597">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-597">Storage</span></span>

* <span data-ttu-id="b141f-598">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-598">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="b141f-599">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-599">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="b141f-600">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-600">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>  
* <span data-ttu-id="b141f-601">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-601">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="b141f-602">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-602">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-603">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-603">VM</span></span>

* <span data-ttu-id="b141f-604">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-604">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="b141f-605">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-605">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="b141f-606">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-606">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="b141f-607">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-607">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="b141f-608">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="b141f-608">January 17, 2018</span></span>

<span data-ttu-id="b141f-609">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="b141f-609">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="b141f-610">ACR</span><span class="sxs-lookup"><span data-stu-id="b141f-610">ACR</span></span>

* <span data-ttu-id="b141f-611">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-611">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="b141f-612">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-612">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-613">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-613">ACS</span></span>

* <span data-ttu-id="b141f-614">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-614">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="b141f-615">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-615">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-616">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-616">Appservice</span></span>

* <span data-ttu-id="b141f-617">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-617">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="b141f-618">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-618">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="b141f-619">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-619">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="b141f-620">Backup
</span><span class="sxs-lookup"><span data-stu-id="b141f-620">Backup</span></span>

* <span data-ttu-id="b141f-621">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-621">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="b141f-622">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-622">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="b141f-623">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-623">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="b141f-624">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-624">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="b141f-625">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-625">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="b141f-626">Batch</span><span class="sxs-lookup"><span data-stu-id="b141f-626">Batch</span></span>

* <span data-ttu-id="b141f-627">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-627">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="b141f-628">クラウド</span><span class="sxs-lookup"><span data-stu-id="b141f-628">Cloud</span></span>

* <span data-ttu-id="b141f-629">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-629">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="b141f-630">消費</span><span class="sxs-lookup"><span data-stu-id="b141f-630">Consumption</span></span>

* <span data-ttu-id="b141f-631">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-631">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="b141f-632">Event Grid</span><span class="sxs-lookup"><span data-stu-id="b141f-632">Event Grid</span></span>

* <span data-ttu-id="b141f-633">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="b141f-633">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="b141f-634">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="b141f-634">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="b141f-635">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-635">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="b141f-636">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b141f-636">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="b141f-637">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-637">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="b141f-638">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-638">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="b141f-639">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-639">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="b141f-640">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-640">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="b141f-641">対話</span><span class="sxs-lookup"><span data-stu-id="b141f-641">Interactive</span></span>

* <span data-ttu-id="b141f-642">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="b141f-642">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="b141f-643">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-643">Fixed errors on startup</span></span>
* <span data-ttu-id="b141f-644">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-644">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="b141f-645">IoT</span><span class="sxs-lookup"><span data-stu-id="b141f-645">IoT</span></span>

* <span data-ttu-id="b141f-646">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-646">Added support for device provisioning service</span></span>
* <span data-ttu-id="b141f-647">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-647">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="b141f-648">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-648">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="b141f-649">監視</span><span class="sxs-lookup"><span data-stu-id="b141f-649">Monitor</span></span>

* <span data-ttu-id="b141f-650">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-650">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="b141f-651">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="b141f-651">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="b141f-652">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-652">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="b141f-653">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-653">Network</span></span>

* <span data-ttu-id="b141f-654">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-654">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="b141f-655">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-655">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="b141f-656">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b141f-656">Profile</span></span>

* <span data-ttu-id="b141f-657">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-657">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="b141f-658">役割</span><span class="sxs-lookup"><span data-stu-id="b141f-658">Role</span></span>

* <span data-ttu-id="b141f-659">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-659">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="b141f-660">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b141f-660">Service Fabric</span></span>

* <span data-ttu-id="b141f-661">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-661">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="b141f-662">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-662">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-663">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-663">VM</span></span>

* <span data-ttu-id="b141f-664">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="b141f-664">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="b141f-665">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-665">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="b141f-666">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-666">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="b141f-667">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-667">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="b141f-668">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-668">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="b141f-669">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-669">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="b141f-670">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-670">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="b141f-671">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-671">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="b141f-672">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="b141f-672">December 19, 2017</span></span>

<span data-ttu-id="b141f-673">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="b141f-673">Version 2.0.23</span></span>

* <span data-ttu-id="b141f-674">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-674">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="b141f-675">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b141f-675">Container</span></span>

* <span data-ttu-id="b141f-676">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-676">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="b141f-677">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-677">Network</span></span>

* <span data-ttu-id="b141f-678">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-678">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="b141f-679">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-679">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-680">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-680">Storage</span></span>

* <span data-ttu-id="b141f-681">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-681">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-682">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-682">VM</span></span>

* <span data-ttu-id="b141f-683">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-683">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="b141f-684">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="b141f-684">December 5, 2017</span></span>

<span data-ttu-id="b141f-685">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="b141f-685">Version 2.0.22</span></span>

* <span data-ttu-id="b141f-686">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-686">Removed `az component` commands.</span></span> <span data-ttu-id="b141f-687">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b141f-687">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="b141f-688">コア</span><span class="sxs-lookup"><span data-stu-id="b141f-688">Core</span></span>
* <span data-ttu-id="b141f-689">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-689">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="b141f-690">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-690">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-691">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-691">ACS</span></span>

* <span data-ttu-id="b141f-692">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-692">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="b141f-693">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-693">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="b141f-694">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-694">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="b141f-695">Advisor</span><span class="sxs-lookup"><span data-stu-id="b141f-695">Advisor</span></span>

* <span data-ttu-id="b141f-696">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b141f-696">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-697">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-697">Appservice</span></span>

* <span data-ttu-id="b141f-698">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-698">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="b141f-699">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-699">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="b141f-700">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-700">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="b141f-701">消費</span><span class="sxs-lookup"><span data-stu-id="b141f-701">Consumption</span></span>

* <span data-ttu-id="b141f-702">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-702">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="b141f-703">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b141f-703">Container</span></span>

* <span data-ttu-id="b141f-704">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-704">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="b141f-705">監視</span><span class="sxs-lookup"><span data-stu-id="b141f-705">Monitor</span></span>

* <span data-ttu-id="b141f-706">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-706">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="b141f-707">リソース</span><span class="sxs-lookup"><span data-stu-id="b141f-707">Resource</span></span>

* <span data-ttu-id="b141f-708">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-708">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="b141f-709">役割</span><span class="sxs-lookup"><span data-stu-id="b141f-709">Role</span></span>

* <span data-ttu-id="b141f-710">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-710">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="b141f-711">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="b141f-711">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="b141f-712">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-712">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="b141f-713">SQL</span><span class="sxs-lookup"><span data-stu-id="b141f-713">SQL</span></span>

* <span data-ttu-id="b141f-714">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-714">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="b141f-715">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-715">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-716">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-716">VM</span></span>

* <span data-ttu-id="b141f-717">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-717">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="b141f-718">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="b141f-718">November 14, 2017</span></span>

<span data-ttu-id="b141f-719">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="b141f-719">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="b141f-720">ACR</span><span class="sxs-lookup"><span data-stu-id="b141f-720">ACR</span></span>

* <span data-ttu-id="b141f-721">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-721">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="b141f-722">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-722">ACS</span></span>

* <span data-ttu-id="b141f-723">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-723">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="b141f-724">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-724">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="b141f-725">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-725">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="b141f-726">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-726">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="b141f-727">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-727">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-728">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-728">Appservice</span></span>

* <span data-ttu-id="b141f-729">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-729">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="b141f-730">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-730">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="b141f-731">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-731">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="b141f-732">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-732">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="b141f-733">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-733">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="b141f-734">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="b141f-734">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="b141f-735">Batch</span><span class="sxs-lookup"><span data-stu-id="b141f-735">Batch</span></span>

* <span data-ttu-id="b141f-736">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-736">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="b141f-737">Batchai</span><span class="sxs-lookup"><span data-stu-id="b141f-737">Batchai</span></span>

* <span data-ttu-id="b141f-738">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-738">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="b141f-739">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-739">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="b141f-740">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-740">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="b141f-741">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-741">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="b141f-742">クラウド</span><span class="sxs-lookup"><span data-stu-id="b141f-742">Cloud</span></span>

* <span data-ttu-id="b141f-743">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-743">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="b141f-744">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b141f-744">Container</span></span>

* <span data-ttu-id="b141f-745">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-745">Added support to open multiple ports</span></span>
* <span data-ttu-id="b141f-746">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-746">Added container group restart policy</span></span>
* <span data-ttu-id="b141f-747">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-747">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="b141f-748">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="b141f-748">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="b141f-749">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b141f-749">Data Lake Analytics</span></span>

* <span data-ttu-id="b141f-750">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-750">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="b141f-751">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b141f-751">Data Lake Store</span></span>

* <span data-ttu-id="b141f-752">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-752">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="b141f-753">内線番号</span><span class="sxs-lookup"><span data-stu-id="b141f-753">Extension</span></span>

* <span data-ttu-id="b141f-754">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-754">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="b141f-755">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-755">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="b141f-756">IoT</span><span class="sxs-lookup"><span data-stu-id="b141f-756">IoT</span></span>

* <span data-ttu-id="b141f-757">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-757">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="b141f-758">監視</span><span class="sxs-lookup"><span data-stu-id="b141f-758">Monitor</span></span>

* <span data-ttu-id="b141f-759">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-759">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="b141f-760">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-760">Network</span></span>

* <span data-ttu-id="b141f-761">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-761">Added support for CAA DNS records</span></span>
* <span data-ttu-id="b141f-762">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-762">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="b141f-763">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-763">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="b141f-764">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-764">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="b141f-765">Reservations</span><span class="sxs-lookup"><span data-stu-id="b141f-765">Reservations</span></span>

* <span data-ttu-id="b141f-766">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b141f-766">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="b141f-767">リソース</span><span class="sxs-lookup"><span data-stu-id="b141f-767">Resource</span></span>

* <span data-ttu-id="b141f-768">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-768">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="b141f-769">SQL</span><span class="sxs-lookup"><span data-stu-id="b141f-769">SQL</span></span>

* <span data-ttu-id="b141f-770">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-770">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-771">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-771">Storage</span></span>

* <span data-ttu-id="b141f-772">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-772">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="b141f-773">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-773">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="b141f-774">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-774">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="b141f-775">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-775">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="b141f-776">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-776">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="b141f-777">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-777">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="b141f-778">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-778">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-779">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-779">VM</span></span>

* <span data-ttu-id="b141f-780">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-780">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="b141f-781">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-781">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="b141f-782">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-782">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="b141f-783">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-783">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="b141f-784">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-784">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="b141f-785">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="b141f-785">October 24, 2017</span></span>

<span data-ttu-id="b141f-786">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="b141f-786">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="b141f-787">コア</span><span class="sxs-lookup"><span data-stu-id="b141f-787">Core</span></span>

* <span data-ttu-id="b141f-788">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="b141f-788">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="b141f-789">ACR</span><span class="sxs-lookup"><span data-stu-id="b141f-789">ACR</span></span>

* <span data-ttu-id="b141f-790">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="b141f-790">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="b141f-791">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-791">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="b141f-792">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-792">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-793">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-793">ACS</span></span>

* <span data-ttu-id="b141f-794">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-794">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="b141f-795">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-795">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-796">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-796">Appservice</span></span>

* <span data-ttu-id="b141f-797">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-797">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="b141f-798">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b141f-798">Component</span></span>

* <span data-ttu-id="b141f-799">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-799">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="b141f-800">監視</span><span class="sxs-lookup"><span data-stu-id="b141f-800">Monitor</span></span>

* <span data-ttu-id="b141f-801">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-801">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="b141f-802">リソース</span><span class="sxs-lookup"><span data-stu-id="b141f-802">Resource</span></span>

* <span data-ttu-id="b141f-803">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-803">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="b141f-804">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-804">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-805">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-805">VM</span></span>

* <span data-ttu-id="b141f-806">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-806">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="b141f-807">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="b141f-807">October 9, 2017</span></span>

<span data-ttu-id="b141f-808">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="b141f-808">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="b141f-809">コア</span><span class="sxs-lookup"><span data-stu-id="b141f-809">Core</span></span>

* <span data-ttu-id="b141f-810">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-810">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-811">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-811">Appservice</span></span>

* <span data-ttu-id="b141f-812">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-812">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="b141f-813">Batch</span><span class="sxs-lookup"><span data-stu-id="b141f-813">Batch</span></span>

* <span data-ttu-id="b141f-814">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="b141f-814">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="b141f-815">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="b141f-815">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="b141f-816">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-816">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="b141f-817">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-817">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="b141f-818">Batchai</span><span class="sxs-lookup"><span data-stu-id="b141f-818">Batchai</span></span>

* <span data-ttu-id="b141f-819">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b141f-819">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="b141f-820">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b141f-820">Keyvault</span></span>

* <span data-ttu-id="b141f-821">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-821">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="b141f-822">(#4448)</span><span class="sxs-lookup"><span data-stu-id="b141f-822">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="b141f-823">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-823">Network</span></span>

* <span data-ttu-id="b141f-824">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-824">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="b141f-825">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="b141f-825">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="b141f-826">リソース</span><span class="sxs-lookup"><span data-stu-id="b141f-826">Resource</span></span>

* <span data-ttu-id="b141f-827">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-827">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="b141f-828">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-828">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="b141f-829">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-829">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="b141f-830">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-830">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="b141f-831">SQL</span><span class="sxs-lookup"><span data-stu-id="b141f-831">Sql</span></span>

* <span data-ttu-id="b141f-832">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-832">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="b141f-833">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="b141f-833">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="b141f-834">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="b141f-834">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-835">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-835">Storage</span></span>

* <span data-ttu-id="b141f-836">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-836">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-837">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-837">Vm</span></span>

* <span data-ttu-id="b141f-838">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-838">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="b141f-839">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-839">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="b141f-840">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-840">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="b141f-841">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-841">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="b141f-842">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-842">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="b141f-843">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="b141f-843">September 22, 2017</span></span>

<span data-ttu-id="b141f-844">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="b141f-844">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="b141f-845">リソース</span><span class="sxs-lookup"><span data-stu-id="b141f-845">Resource</span></span>

* <span data-ttu-id="b141f-846">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-846">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="b141f-847">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-847">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="b141f-848">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-848">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="b141f-849">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-849">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="b141f-850">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-850">Network</span></span>

* <span data-ttu-id="b141f-851">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-851">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="b141f-852">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-852">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="b141f-853">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-853">Added `asg` application security group commands</span></span>
* <span data-ttu-id="b141f-854">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-854">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="b141f-855">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-855">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="b141f-856">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-856">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="b141f-857">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-857">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-858">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-858">Storage</span></span>

* <span data-ttu-id="b141f-859">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-859">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="b141f-860">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="b141f-860">Eventgrid</span></span>

* <span data-ttu-id="b141f-861">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="b141f-861">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="b141f-862">SQL</span><span class="sxs-lookup"><span data-stu-id="b141f-862">SQL</span></span>

* <span data-ttu-id="b141f-863">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-863">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="b141f-864">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="b141f-864">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="b141f-865">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-865">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="b141f-866">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b141f-866">Keyvault</span></span>

* <span data-ttu-id="b141f-867">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-867">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-868">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-868">VM</span></span>

* <span data-ttu-id="b141f-869">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-869">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="b141f-870">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-870">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="b141f-871">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-871">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="b141f-872">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-872">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="b141f-873">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-873">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="b141f-874">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-874">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-875">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-875">ACS</span></span>

* <span data-ttu-id="b141f-876">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-876">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-877">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-877">Appservice</span></span>

* <span data-ttu-id="b141f-878">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-878">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="b141f-879">Backup
</span><span class="sxs-lookup"><span data-stu-id="b141f-879">Backup</span></span>

* <span data-ttu-id="b141f-880">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b141f-880">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="b141f-881">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="b141f-881">September 11, 2017</span></span>

<span data-ttu-id="b141f-882">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="b141f-882">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="b141f-883">コア</span><span class="sxs-lookup"><span data-stu-id="b141f-883">Core</span></span>

* <span data-ttu-id="b141f-884">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-884">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="b141f-885">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-885">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-886">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-886">Acs</span></span>

* <span data-ttu-id="b141f-887">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-887">Added `acs list-locations` command</span></span>
* <span data-ttu-id="b141f-888">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="b141f-888">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-889">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-889">Appservice</span></span>

* <span data-ttu-id="b141f-890">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-890">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="b141f-891">CDN</span><span class="sxs-lookup"><span data-stu-id="b141f-891">CDN</span></span>

* <span data-ttu-id="b141f-892">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-892">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="b141f-893">内線番号</span><span class="sxs-lookup"><span data-stu-id="b141f-893">Extension</span></span>

* <span data-ttu-id="b141f-894">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b141f-894">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="b141f-895">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b141f-895">Keyvault</span></span>

* <span data-ttu-id="b141f-896">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-896">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="b141f-897">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-897">Network</span></span>

* <span data-ttu-id="b141f-898">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-898">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="b141f-899">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-899">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="b141f-900">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-900">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="b141f-901">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-901">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="b141f-902">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-902">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="b141f-903">リソース</span><span class="sxs-lookup"><span data-stu-id="b141f-903">Resource</span></span>

* <span data-ttu-id="b141f-904">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="b141f-904">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="b141f-905">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="b141f-905">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="b141f-906">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="b141f-906">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="b141f-907">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="b141f-907">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="b141f-908">SQL</span><span class="sxs-lookup"><span data-stu-id="b141f-908">SQL</span></span>

* <span data-ttu-id="b141f-909">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-909">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-910">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-910">VM</span></span>

* <span data-ttu-id="b141f-911">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="b141f-911">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="b141f-912">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="b141f-912">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="b141f-913">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-913">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="b141f-914">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="b141f-914">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="b141f-915">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="b141f-915">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="b141f-916">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="b141f-916">August 31, 2017</span></span>

<span data-ttu-id="b141f-917">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="b141f-917">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="b141f-918">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b141f-918">Keyvault</span></span>

* <span data-ttu-id="b141f-919">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-919">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="b141f-920">SF</span><span class="sxs-lookup"><span data-stu-id="b141f-920">Sf</span></span>

* <span data-ttu-id="b141f-921">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="b141f-921">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-922">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-922">Storage</span></span>

* <span data-ttu-id="b141f-923">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-923">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="b141f-924">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="b141f-924">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="b141f-925">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="b141f-925">August 28, 2017</span></span>

<span data-ttu-id="b141f-926">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="b141f-926">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="b141f-927">CLI</span><span class="sxs-lookup"><span data-stu-id="b141f-927">CLI</span></span>

* <span data-ttu-id="b141f-928">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-928">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-929">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-929">ACS</span></span>

* <span data-ttu-id="b141f-930">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-930">Corrected preview regions</span></span>
* <span data-ttu-id="b141f-931">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-931">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="b141f-932">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="b141f-932">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-933">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-933">Appservice</span></span>

* <span data-ttu-id="b141f-934">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-934">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="b141f-935">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-935">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="b141f-936">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="b141f-936">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="b141f-937">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="b141f-937">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="b141f-938">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="b141f-938">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="b141f-939">IoT</span><span class="sxs-lookup"><span data-stu-id="b141f-939">IoT</span></span>

* <span data-ttu-id="b141f-940">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="b141f-940">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="b141f-941">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-941">Network</span></span>

* <span data-ttu-id="b141f-942">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-942">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="b141f-943">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-943">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="b141f-944">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-944">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="b141f-945">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-945">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="b141f-946">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-946">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="b141f-947">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b141f-947">Profile</span></span>

* <span data-ttu-id="b141f-948">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="b141f-948">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="b141f-949">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b141f-949">Service Fabric</span></span>

* <span data-ttu-id="b141f-950">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b141f-950">Preview release</span></span>
* <span data-ttu-id="b141f-951">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="b141f-951">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="b141f-952">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-952">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="b141f-953">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-953">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-954">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-954">Storage</span></span>

* <span data-ttu-id="b141f-955">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-955">Enabled setting blob tier</span></span>
* <span data-ttu-id="b141f-956">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-956">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="b141f-957">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-957">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="b141f-958">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-958">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="b141f-959">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-959">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="b141f-960">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="b141f-960">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-961">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-961">VM</span></span>

* <span data-ttu-id="b141f-962">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-962">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="b141f-963">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-963">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="b141f-964">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-964">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="b141f-965">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-965">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="b141f-966">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-966">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="b141f-967">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-967">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="b141f-968">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="b141f-968">August 15, 2017</span></span>

<span data-ttu-id="b141f-969">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="b141f-969">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-970">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-970">ACS</span></span>

* <span data-ttu-id="b141f-971">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-971">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-972">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-972">Appservice</span></span>

* <span data-ttu-id="b141f-973">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-973">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="b141f-974">Event Grid</span><span class="sxs-lookup"><span data-stu-id="b141f-974">Event Grid</span></span>

* <span data-ttu-id="b141f-975">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-975">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="b141f-976">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="b141f-976">August 11, 2017</span></span>

<span data-ttu-id="b141f-977">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="b141f-977">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-978">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-978">ACS</span></span>

* <span data-ttu-id="b141f-979">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-979">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="b141f-980">Batch</span><span class="sxs-lookup"><span data-stu-id="b141f-980">Batch</span></span>

* <span data-ttu-id="b141f-981">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="b141f-981">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="b141f-982">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-982">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="b141f-983">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-983">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="b141f-984">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-984">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="b141f-985">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-985">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="b141f-986">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-986">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="b141f-987">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b141f-987">Component</span></span>

* <span data-ttu-id="b141f-988">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-988">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="b141f-989">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b141f-989">Container</span></span>

* <span data-ttu-id="b141f-990">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-990">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="b141f-991">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b141f-991">Data Lake Store</span></span>

* <span data-ttu-id="b141f-992">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-992">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="b141f-993">Event Grid</span><span class="sxs-lookup"><span data-stu-id="b141f-993">Event Grid</span></span>

* <span data-ttu-id="b141f-994">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b141f-994">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="b141f-995">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-995">Network</span></span>

* <span data-ttu-id="b141f-996">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-996">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="b141f-997">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-997">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="b141f-998">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-998">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="b141f-999">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-999">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="b141f-1000">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b141f-1000">Profile</span></span>

* <span data-ttu-id="b141f-1001">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1001">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-1002">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-1002">Storage</span></span>

* <span data-ttu-id="b141f-1003">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="b141f-1003">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-1004">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-1004">VM</span></span>

* <span data-ttu-id="b141f-1005">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1005">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="b141f-1006">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1006">Exposed `list-skus` command</span></span>
* <span data-ttu-id="b141f-1007">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-1007">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="b141f-1008">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="b141f-1008">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="b141f-1009">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1009">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="b141f-1010">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="b141f-1010">July 28, 2017</span></span>

<span data-ttu-id="b141f-1011">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="b141f-1011">Version 2.0.12</span></span>

* <span data-ttu-id="b141f-1012">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1012">Added container commands</span></span>
* <span data-ttu-id="b141f-1013">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1013">Added billing and consumption modules</span></span>

```text
azure-cli (2.0.12)

acr (2.0.9)
acs (2.0.11)
appservice (0.1.11)
batch (3.0.3)
billing (0.1.3)
cdn (0.0.6)
cloud (2.0.7)
cognitiveservices (0.1.6)
command-modules-nspkg (2.0.1)
component (2.0.6)
configure (2.0.10)
consumption (0.1.3)
container (0.1.7)
core (2.0.12)
cosmosdb (0.1.11)
dla (0.0.10)
dls (0.0.11)
feedback (2.0.6)
find (0.2.6)
interactive (0.3.7)
iot (0.1.10)
keyvault (2.0.8)
lab (0.0.9)
monitor (0.0.8)
network (2.0.11)
nspkg (3.0.1)
profile (2.0.9)
rdbms (0.0.5)
redis (0.2.7)
resource (2.0.11)
role (2.0.9)
sf (1.0.5)
sql (2.0.8)
storage (2.0.11)
vm (2.0.11)
```

### <a name="core"></a><span data-ttu-id="b141f-1014">コア</span><span class="sxs-lookup"><span data-stu-id="b141f-1014">Core</span></span>

* <span data-ttu-id="b141f-1015">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="b141f-1015">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="b141f-1016">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1016">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="b141f-1017">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="b141f-1017">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="b141f-1018">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="b141f-1018">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="b141f-1019">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="b141f-1019">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="b141f-1020">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="b141f-1020">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="b141f-1021">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="b141f-1021">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="b141f-1022">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="b141f-1022">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="b141f-1023">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="b141f-1023">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="b141f-1024">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="b141f-1024">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="b141f-1025">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="b141f-1025">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="b141f-1026">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="b141f-1026">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="b141f-1027">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1027">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="b141f-1028">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1028">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="b141f-1029">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-1029">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="b141f-1030">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="b141f-1030">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="b141f-1031">ACR</span><span class="sxs-lookup"><span data-stu-id="b141f-1031">ACR</span></span>

* <span data-ttu-id="b141f-1032">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1032">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="b141f-1033">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-1033">Support SKU update for managed registries</span></span>
* <span data-ttu-id="b141f-1034">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1034">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="b141f-1035">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1035">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="b141f-1036">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1036">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="b141f-1037">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1037">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-1038">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-1038">ACS</span></span>

* <span data-ttu-id="b141f-1039">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-1039">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-1040">Appservice</span><span class="sxs-lookup"><span data-stu-id="b141f-1040">Appservice</span></span>

* <span data-ttu-id="b141f-1041">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1041">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="b141f-1042">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-1042">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="b141f-1043">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="b141f-1043">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="b141f-1044">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="b141f-1044">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="b141f-1045">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="b141f-1045">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="b141f-1046">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="b141f-1046">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="b141f-1047">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="b141f-1047">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="b141f-1048">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="b141f-1048">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="b141f-1049">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-1049">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="b141f-1050">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b141f-1050">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="b141f-1051">Batch</span><span class="sxs-lookup"><span data-stu-id="b141f-1051">Batch</span></span>

* <span data-ttu-id="b141f-1052">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="b141f-1052">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="b141f-1053">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1053">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="b141f-1054">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1054">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="b141f-1055">CDN</span><span class="sxs-lookup"><span data-stu-id="b141f-1055">CDN</span></span>

* <span data-ttu-id="b141f-1056">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1056">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="b141f-1057">クラウド</span><span class="sxs-lookup"><span data-stu-id="b141f-1057">Cloud</span></span>

* <span data-ttu-id="b141f-1058">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1058">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="b141f-1059">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="b141f-1059">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="b141f-1060">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-1060">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="b141f-1061">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1061">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="b141f-1062">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1062">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b141f-1063">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b141f-1063">CosmosDB</span></span>

* <span data-ttu-id="b141f-1064">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1064">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="b141f-1065">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1065">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="b141f-1066">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b141f-1066">Data Lake Analytics</span></span>

* <span data-ttu-id="b141f-1067">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1067">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="b141f-1068">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1068">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="b141f-1069">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1069">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="b141f-1070">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b141f-1070">Data Lake Store</span></span>

* <span data-ttu-id="b141f-1071">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1071">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="b141f-1072">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1072">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="b141f-1073">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-1073">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="b141f-1074">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="b141f-1074">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="b141f-1075">対話</span><span class="sxs-lookup"><span data-stu-id="b141f-1075">Interactive</span></span>

* <span data-ttu-id="b141f-1076">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1076">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="b141f-1077">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="b141f-1077">Increased test coverage</span></span>
* <span data-ttu-id="b141f-1078">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1078">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="b141f-1079">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="b141f-1079">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="b141f-1080">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="b141f-1080">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="b141f-1081">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="b141f-1081">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="b141f-1082">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="b141f-1082">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="b141f-1083">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1083">Added `--progress` flag</span></span>
* <span data-ttu-id="b141f-1084">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1084">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="b141f-1085">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="b141f-1085">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="b141f-1086">IoT</span><span class="sxs-lookup"><span data-stu-id="b141f-1086">IoT</span></span>

* <span data-ttu-id="b141f-1087">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-1087">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="b141f-1088">(#3934)</span><span class="sxs-lookup"><span data-stu-id="b141f-1088">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="b141f-1089">Key Vault</span><span class="sxs-lookup"><span data-stu-id="b141f-1089">Key vault</span></span>

* <span data-ttu-id="b141f-1090">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-1090">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="b141f-1091">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b141f-1091">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="b141f-1092">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b141f-1092">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="b141f-1093">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b141f-1093">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="b141f-1094">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b141f-1094">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="b141f-1095">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="b141f-1095">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="b141f-1096">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-1096">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="b141f-1097">(#3307)</span><span class="sxs-lookup"><span data-stu-id="b141f-1097">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="b141f-1098">ラボ</span><span class="sxs-lookup"><span data-stu-id="b141f-1098">Lab</span></span>

* <span data-ttu-id="b141f-1099">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1099">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="b141f-1100">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1100">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="b141f-1101">監視</span><span class="sxs-lookup"><span data-stu-id="b141f-1101">Monitor</span></span>

* <span data-ttu-id="b141f-1102">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="b141f-1102">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="b141f-1103">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1103">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="b141f-1104">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1104">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="b141f-1105">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1105">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="b141f-1106">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1106">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="b141f-1107">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="b141f-1107">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="b141f-1108">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1108">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="b141f-1109">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="b141f-1109">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="b141f-1110">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1110">`location` no longer required</span></span>
  * <span data-ttu-id="b141f-1111">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="b141f-1111">Add name and ID support for target</span></span>
  * <span data-ttu-id="b141f-1112">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="b141f-1112">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="b141f-1113">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-1113">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="b141f-1114">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1114">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="b141f-1115">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="b141f-1115">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="b141f-1116">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-1116">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="b141f-1117">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1117">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="b141f-1118">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-1118">Network</span></span>

* <span data-ttu-id="b141f-1119">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1119">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="b141f-1120">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1120">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="b141f-1121">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1121">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="b141f-1122">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1122">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="b141f-1123">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1123">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="b141f-1124">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1124">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="b141f-1125">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1125">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="b141f-1126">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1126">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="b141f-1127">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1127">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="b141f-1128">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1128">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="b141f-1129">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1129">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="b141f-1130">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1130">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="b141f-1131">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1131">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="b141f-1132">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1132">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="b141f-1133">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1133">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="b141f-1134">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1134">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="b141f-1135">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1135">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="b141f-1136">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1136">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="b141f-1137">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1137">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="b141f-1138">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1138">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="b141f-1139">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1139">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="b141f-1140">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1140">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="b141f-1141">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1141">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="b141f-1142">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b141f-1142">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="b141f-1143">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b141f-1143">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="b141f-1144">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b141f-1144">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="b141f-1145">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b141f-1145">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="b141f-1146">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b141f-1146">Profile</span></span>

* <span data-ttu-id="b141f-1147">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-1147">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="b141f-1148">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-1148">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="b141f-1149">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="b141f-1149">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="b141f-1150">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1150">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="b141f-1151">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-1151">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="b141f-1152">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b141f-1152">RDBMS</span></span>

* <span data-ttu-id="b141f-1153">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="b141f-1153">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="b141f-1154">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="b141f-1154">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="b141f-1155">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="b141f-1155">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="b141f-1156">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="b141f-1156">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="b141f-1157">リソース</span><span class="sxs-lookup"><span data-stu-id="b141f-1157">Resource</span></span>

* <span data-ttu-id="b141f-1158">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1158">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="b141f-1159">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1159">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="b141f-1160">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1160">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="b141f-1161">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-1161">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="b141f-1162">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="b141f-1162">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="b141f-1163">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1163">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="b141f-1164">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="b141f-1164">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="b141f-1165">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1165">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="b141f-1166">役割</span><span class="sxs-lookup"><span data-stu-id="b141f-1166">Role</span></span>

* <span data-ttu-id="b141f-1167">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-1167">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="b141f-1168">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="b141f-1168">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="b141f-1169">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="b141f-1169">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="b141f-1170">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="b141f-1170">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="b141f-1171">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1171">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="b141f-1172">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b141f-1172">Service Fabric</span></span>
* <span data-ttu-id="b141f-1173">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="b141f-1173">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="b141f-1174">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="b141f-1174">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="b141f-1175">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="b141f-1175">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="b141f-1176">SQL</span><span class="sxs-lookup"><span data-stu-id="b141f-1176">SQL</span></span>

* <span data-ttu-id="b141f-1177">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1177">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="b141f-1178">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1178">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="b141f-1179">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1179">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-1180">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-1180">Storage</span></span>

* <span data-ttu-id="b141f-1181">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="b141f-1181">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="b141f-1182">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-1182">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="b141f-1183">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="b141f-1183">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="b141f-1184">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="b141f-1184">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="b141f-1185">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="b141f-1185">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="b141f-1186">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="b141f-1186">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-1187">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-1187">VM</span></span>

* <span data-ttu-id="b141f-1188">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-1188">Support configuring nsg</span></span>
* <span data-ttu-id="b141f-1189">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1189">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="b141f-1190">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="b141f-1190">Support managed service identities</span></span>
* <span data-ttu-id="b141f-1191">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1191">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="b141f-1192">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="b141f-1192">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="b141f-1193">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="b141f-1193">May 10, 2017</span></span>

<span data-ttu-id="b141f-1194">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="b141f-1194">Version 2.0.6</span></span>

* <span data-ttu-id="b141f-1195">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1195">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="b141f-1196">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1196">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="b141f-1197">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1197">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="b141f-1198">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1198">Include Cognitive Services module</span></span>
* <span data-ttu-id="b141f-1199">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1199">Include Service Fabric module</span></span>
* <span data-ttu-id="b141f-1200">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="b141f-1200">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="b141f-1201">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1201">Add support for CDN commands</span></span>
* <span data-ttu-id="b141f-1202">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1202">Remove Container module</span></span>
* <span data-ttu-id="b141f-1203">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="b141f-1203">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="b141f-1204">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="b141f-1204">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

```text
azure-cli (2.0.6)

acr (2.0.4)
acs (2.0.6)
appservice (0.1.6)
batch (2.0.4)
cdn (0.0.2)
cloud (2.0.2)
cognitiveservices (0.1.2)
command-modules-nspkg (2.0.0)
component (2.0.4)
configure (2.0.6)
core (2.0.6)
cosmosdb (0.1.6)
dla (0.0.6)
dls (0.0.6)
feedback (2.0.2)
find (0.2.2)
interactive (0.3.1)
iot (0.1.5)
keyvault (2.0.4)
lab (0.0.4)
monitor (0.0.4)
network (2.0.6)
nspkg (3.0.0)
profile (2.0.4)
rdbms (0.0.1)
redis (0.2.3)
resource (2.0.6)
role (2.0.4)
sf (1.0.1)
sql (2.0.3)
storage (2.0.6)
vm (2.0.6)
```

### <a name="core"></a><span data-ttu-id="b141f-1205">コア</span><span class="sxs-lookup"><span data-stu-id="b141f-1205">Core</span></span>

* <span data-ttu-id="b141f-1206">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="b141f-1206">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="b141f-1207">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="b141f-1207">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="b141f-1208">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="b141f-1208">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="b141f-1209">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="b141f-1209">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="b141f-1210">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="b141f-1210">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="b141f-1211">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="b141f-1211">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="b141f-1212">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="b141f-1212">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="b141f-1213">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="b141f-1213">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="b141f-1214">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="b141f-1214">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="b141f-1215">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="b141f-1215">core: Improved performance</span></span>
* <span data-ttu-id="b141f-1216">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="b141f-1216">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="b141f-1217">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="b141f-1217">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-1218">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-1218">ACS</span></span>

* <span data-ttu-id="b141f-1219">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1219">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="b141f-1220">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1220">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="b141f-1221">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1221">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="b141f-1222">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="b141f-1222">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-1223">AppService</span><span class="sxs-lookup"><span data-stu-id="b141f-1223">AppService</span></span>

* <span data-ttu-id="b141f-1224">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1224">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="b141f-1225">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1225">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="b141f-1226">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="b141f-1226">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="b141f-1227">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1227">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="b141f-1228">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1228">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="b141f-1229">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="b141f-1229">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="b141f-1230">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="b141f-1230">support slot swap with preview</span></span>
* <span data-ttu-id="b141f-1231">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="b141f-1231">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="b141f-1232">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="b141f-1232">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b141f-1233">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b141f-1233">CosmosDB</span></span>

* <span data-ttu-id="b141f-1234">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1234">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="b141f-1235">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1235">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="b141f-1236">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1236">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="b141f-1237">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1237">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="b141f-1238">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b141f-1238">Data Lake Analytics</span></span>

* <span data-ttu-id="b141f-1239">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1239">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="b141f-1240">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="b141f-1240">Add support for new catalog item type: package.</span></span> <span data-ttu-id="b141f-1241">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="b141f-1241">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="b141f-1242">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="b141f-1242">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="b141f-1243">テーブル</span><span class="sxs-lookup"><span data-stu-id="b141f-1243">Table</span></span>
  * <span data-ttu-id="b141f-1244">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="b141f-1244">Table valued function</span></span>
  * <span data-ttu-id="b141f-1245">表示</span><span class="sxs-lookup"><span data-stu-id="b141f-1245">View</span></span>
  * <span data-ttu-id="b141f-1246">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="b141f-1246">Table Statistics.</span></span> <span data-ttu-id="b141f-1247">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="b141f-1247">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="b141f-1248">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b141f-1248">Data Lake Store</span></span>

* <span data-ttu-id="b141f-1249">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1249">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="b141f-1250">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="b141f-1250">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="b141f-1251">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="b141f-1251">missed help for access show.</span></span> <span data-ttu-id="b141f-1252">追加しました </span><span class="sxs-lookup"><span data-stu-id="b141f-1252">adding it.</span></span> <span data-ttu-id="b141f-1253">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="b141f-1253">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="b141f-1254">検索</span><span class="sxs-lookup"><span data-stu-id="b141f-1254">Find</span></span>

* <span data-ttu-id="b141f-1255">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="b141f-1255">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="b141f-1256">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b141f-1256">KeyVault</span></span>

* <span data-ttu-id="b141f-1257">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1257">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="b141f-1258">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1258">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="b141f-1259">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="b141f-1259">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="b141f-1260">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1260">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="b141f-1261">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="b141f-1261">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="b141f-1262">ラボ</span><span class="sxs-lookup"><span data-stu-id="b141f-1262">Lab</span></span>

* <span data-ttu-id="b141f-1263">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1263">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="b141f-1264">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1264">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="b141f-1265">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1265">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="b141f-1266">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1266">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="b141f-1267">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1267">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="b141f-1268">監視</span><span class="sxs-lookup"><span data-stu-id="b141f-1268">Monitor</span></span>

* <span data-ttu-id="b141f-1269">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="b141f-1269">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="b141f-1270">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="b141f-1270">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="b141f-1271">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-1271">Network</span></span>

* <span data-ttu-id="b141f-1272">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1272">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="b141f-1273">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1273">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="b141f-1274">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1274">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="b141f-1275">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1275">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="b141f-1276">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1276">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="b141f-1277">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1277">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="b141f-1278">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1278">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="b141f-1279">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1279">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="b141f-1280">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1280">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="b141f-1281">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1281">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="b141f-1282">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1282">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="b141f-1283">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1283">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="b141f-1284">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1284">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="b141f-1285">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1285">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="b141f-1286">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b141f-1286">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="b141f-1287">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1287">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="b141f-1288">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b141f-1288">Profile</span></span>

* <span data-ttu-id="b141f-1289">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="b141f-1289">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="b141f-1290">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="b141f-1290">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="b141f-1291">Redis</span><span class="sxs-lookup"><span data-stu-id="b141f-1291">Redis</span></span>

* <span data-ttu-id="b141f-1292">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1292">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="b141f-1293">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1293">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="b141f-1294">リソース</span><span class="sxs-lookup"><span data-stu-id="b141f-1294">Resource</span></span>

* <span data-ttu-id="b141f-1295">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="b141f-1295">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="b141f-1296">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="b141f-1296">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="b141f-1297">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="b141f-1297">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="b141f-1298">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="b141f-1298">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="b141f-1299">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="b141f-1299">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="b141f-1300">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="b141f-1300">Add docs for az lock update.</span></span> <span data-ttu-id="b141f-1301">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="b141f-1301">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="b141f-1302">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="b141f-1302">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="b141f-1303">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="b141f-1303">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="b141f-1304">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="b141f-1304">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="b141f-1305">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="b141f-1305">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="b141f-1306">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="b141f-1306">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="b141f-1307">役割</span><span class="sxs-lookup"><span data-stu-id="b141f-1307">Role</span></span>

* <span data-ttu-id="b141f-1308">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="b141f-1308">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="b141f-1309">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="b141f-1309">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="b141f-1310">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="b141f-1310">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="b141f-1311">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="b141f-1311">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="b141f-1312">SQL</span><span class="sxs-lookup"><span data-stu-id="b141f-1312">SQL</span></span>

* <span data-ttu-id="b141f-1313">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b141f-1313">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="b141f-1314">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="b141f-1314">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="b141f-1315">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-1315">Storage</span></span>

* <span data-ttu-id="b141f-1316">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="b141f-1316">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="b141f-1317">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1317">Add support for incremental blob copy</span></span>
* <span data-ttu-id="b141f-1318">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1318">Add support for large block blob upload</span></span>
* <span data-ttu-id="b141f-1319">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="b141f-1319">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-1320">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-1320">VM</span></span>

* <span data-ttu-id="b141f-1321">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="b141f-1321">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="b141f-1322">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="b141f-1322">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="b141f-1323">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="b141f-1323">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="b141f-1324">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="b141f-1324">az vm/vmss disk</span></span>
  3. <span data-ttu-id="b141f-1325">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="b141f-1325">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="b141f-1326">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="b141f-1326">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="b141f-1327">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="b141f-1327">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="b141f-1328">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="b141f-1328">April 3, 2017</span></span>

<span data-ttu-id="b141f-1329">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="b141f-1329">Version 2.0.2</span></span>

<span data-ttu-id="b141f-1330">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="b141f-1330">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

```text
azure-cli (2.0.2)

acr (2.0.0)
acs (2.0.2)
appservice (0.1.2)
batch (2.0.0)
cloud (2.0.0)
component (2.0.0)
configure (2.0.2)
container (0.1.2)
core (2.0.2)
documentdb (0.1.2)
feedback (2.0.0)
find (0.0.1b1)
iot (0.1.2)
keyvault (2.0.0)
lab (0.0.1)
monitor (0.0.1)
network (2.0.2)
nspkg (2.0.0)
profile (2.0.2)
redis (0.1.1b3)
resource (2.0.2)
role (2.0.1)
sql (2.0.0)
storage (2.0.2)
vm (2.0.2)
```

### <a name="core"></a><span data-ttu-id="b141f-1331">コア</span><span class="sxs-lookup"><span data-stu-id="b141f-1331">Core</span></span>

* <span data-ttu-id="b141f-1332">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="b141f-1332">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="b141f-1333">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="b141f-1333">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="b141f-1334">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="b141f-1334">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="b141f-1335">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="b141f-1335">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="b141f-1336">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="b141f-1336">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="b141f-1337">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="b141f-1337">Add prompting for missing template parameters.</span></span> <span data-ttu-id="b141f-1338">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="b141f-1338">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="b141f-1339">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="b141f-1339">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="b141f-1340">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="b141f-1340">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="b141f-1341">ACS</span><span class="sxs-lookup"><span data-stu-id="b141f-1341">ACS</span></span>

* <span data-ttu-id="b141f-1342">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="b141f-1342">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="b141f-1343">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="b141f-1343">Add support for ssh key password prompting.</span></span> <span data-ttu-id="b141f-1344">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="b141f-1344">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="b141f-1345">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="b141f-1345">Add support for windows clusters.</span></span> <span data-ttu-id="b141f-1346">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="b141f-1346">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="b141f-1347">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="b141f-1347">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="b141f-1348">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="b141f-1348">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="b141f-1349">AppService</span><span class="sxs-lookup"><span data-stu-id="b141f-1349">AppService</span></span>

* <span data-ttu-id="b141f-1350">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="b141f-1350">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="b141f-1351">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="b141f-1351">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="b141f-1352">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="b141f-1352">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="b141f-1353">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="b141f-1353">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="b141f-1354">DataLake</span><span class="sxs-lookup"><span data-stu-id="b141f-1354">DataLake</span></span>

* <span data-ttu-id="b141f-1355">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b141f-1355">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="b141f-1356">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b141f-1356">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="b141f-1357">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="b141f-1357">DocuemntDB</span></span>

* <span data-ttu-id="b141f-1358">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="b141f-1358">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="b141f-1359">VM</span><span class="sxs-lookup"><span data-stu-id="b141f-1359">VM</span></span>

* <span data-ttu-id="b141f-1360">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="b141f-1360">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="b141f-1361">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="b141f-1361">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="b141f-1362">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="b141f-1362">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="b141f-1363">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="b141f-1363">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="b141f-1364">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="b141f-1364">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="b141f-1365">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="b141f-1365">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="b141f-1366">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="b141f-1366">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="b141f-1367">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="b141f-1367">February 27, 2017</span></span>

<span data-ttu-id="b141f-1368">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="b141f-1368">Version 2.0.0</span></span>

<span data-ttu-id="b141f-1369">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="b141f-1369">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="b141f-1370">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="b141f-1370">Container Service (acs)</span></span>
- <span data-ttu-id="b141f-1371">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="b141f-1371">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="b141f-1372">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b141f-1372">Networking</span></span>
- <span data-ttu-id="b141f-1373">Storage</span><span class="sxs-lookup"><span data-stu-id="b141f-1373">Storage</span></span>

<span data-ttu-id="b141f-1374">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="b141f-1374">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="b141f-1375">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="b141f-1375">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="b141f-1376">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="b141f-1376">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

```text
azure-cli (2.0.0)

acs (2.0.0)
appservice (0.1.1b5)
batch (0.1.1b4)
cloud (2.0.0)
component (2.0.0)
configure (2.0.0)
container (0.1.1b4)
core (2.0.0)
documentdb (0.1.1b2)
feedback (2.0.0)
iot (0.1.1b3)
keyvault (0.1.1b5)
network (2.0.0)
nspkg (2.0.0)
profile (2.0.0)
redis (0.1.1b3)
resource (2.0.0)
role (2.0.0)
sql (0.1.1b5)
storage (2.0.0)
vm (2.0.0)

Python (Darwin) 2.7.10 (default, Jul 30 2016, 19:40:32)
[GCC 4.2.1 Compatible Apple LLVM 8.0.0 (clang-800.0.34)]
```

> [!Note]
> <span data-ttu-id="b141f-1377">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="b141f-1377">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="b141f-1378">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="b141f-1378">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="b141f-1379">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="b141f-1379">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="b141f-1380">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="b141f-1380">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="b141f-1381">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="b141f-1381">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="b141f-1382">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="b141f-1382">Provide feedback from the command line with the `az feedback` command</span></span>

