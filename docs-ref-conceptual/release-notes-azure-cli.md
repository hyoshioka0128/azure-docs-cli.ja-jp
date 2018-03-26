---
title: Azure CLI 2.0 リリース ノート
description: Azure CLI 2.0 の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 02/27/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 116fa95e51399b9b97c1b35c38445f30db7efc94
ms.sourcegitcommit: fefb5bb6a21cab30c44592c0577408a8d1a2ccc7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/17/2018
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="ba5d6-103">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="ba5d6-103">Azure CLI 2.0 release notes</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="ba5d6-104">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-104">March 13, 2018</span></span>

<span data-ttu-id="ba5d6-105">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="ba5d6-105">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="ba5d6-106">ACR</span><span class="sxs-lookup"><span data-stu-id="ba5d6-106">ACR</span></span>

* <span data-ttu-id="ba5d6-107">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-107">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="ba5d6-108">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-108">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="ba5d6-109">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-109">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-110">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-110">ACS</span></span>

* <span data-ttu-id="ba5d6-111">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-111">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="ba5d6-112">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-112">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="ba5d6-113">Advisor</span><span class="sxs-lookup"><span data-stu-id="ba5d6-113">Advisor</span></span>

* <span data-ttu-id="ba5d6-114">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-114">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="ba5d6-115">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-115">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="ba5d6-116">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-116">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span> 
* <span data-ttu-id="ba5d6-117">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-117">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="ba5d6-118">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-118">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-119">Appservice</span><span class="sxs-lookup"><span data-stu-id="ba5d6-119">Appservice</span></span>

* <span data-ttu-id="ba5d6-120">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-120">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="ba5d6-121">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-121">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="ba5d6-122">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="ba5d6-122">Eventhubs</span></span>

* <span data-ttu-id="ba5d6-123">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-123">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="ba5d6-124">内線番号</span><span class="sxs-lookup"><span data-stu-id="ba5d6-124">Extension</span></span>

* <span data-ttu-id="ba5d6-125">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-125">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="ba5d6-126">対話</span><span class="sxs-lookup"><span data-stu-id="ba5d6-126">Interactive</span></span>

* <span data-ttu-id="ba5d6-127">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました: 異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="ba5d6-127">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="ba5d6-128">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました: スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="ba5d6-128">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="ba5d6-129">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました: コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="ba5d6-129">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="ba5d6-130">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-130">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="ba5d6-131">監視</span><span class="sxs-lookup"><span data-stu-id="ba5d6-131">Monitor</span></span>

* <span data-ttu-id="ba5d6-132">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-132">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="ba5d6-133">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-133">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="ba5d6-134">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-134">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="ba5d6-135">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-135">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="ba5d6-136">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-136">Network</span></span>

* <span data-ttu-id="ba5d6-137">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-137">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="ba5d6-138">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-138">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="ba5d6-139">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-139">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="ba5d6-140">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-140">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="ba5d6-141">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ba5d6-141">Profile</span></span>

* <span data-ttu-id="ba5d6-142">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-142">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="ba5d6-143">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-143">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="ba5d6-144">RDBMS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-144">RDBMS</span></span>

* <span data-ttu-id="ba5d6-145">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-145">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="ba5d6-146">Service Bus</span><span class="sxs-lookup"><span data-stu-id="ba5d6-146">Service Bus</span></span>

* <span data-ttu-id="ba5d6-147">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-147">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="ba5d6-148">Storage</span><span class="sxs-lookup"><span data-stu-id="ba5d6-148">Storage</span></span>

* <span data-ttu-id="ba5d6-149">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-149">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds.</span></span>
* <span data-ttu-id="ba5d6-150">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました: Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-150">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-151">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-151">VM</span></span>

* <span data-ttu-id="ba5d6-152">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-152">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="ba5d6-153">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-153">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="ba5d6-154">非推奨にしたコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-154">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="ba5d6-155">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-155">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="ba5d6-156">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-156">February 27, 2018</span></span>

<span data-ttu-id="ba5d6-157">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="ba5d6-157">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="ba5d6-158">コア</span><span class="sxs-lookup"><span data-stu-id="ba5d6-158">Core</span></span>

* <span data-ttu-id="ba5d6-159">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正: Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="ba5d6-159">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="ba5d6-160">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-160">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="ba5d6-161">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-161">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-162">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-162">ACS</span></span>

* <span data-ttu-id="ba5d6-163">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-163">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="ba5d6-164">修正された問題: ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="ba5d6-164">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="ba5d6-165">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-165">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="ba5d6-166">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-166">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-167">Appservice</span><span class="sxs-lookup"><span data-stu-id="ba5d6-167">Appservice</span></span>

* <span data-ttu-id="ba5d6-168">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="ba5d6-168">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="ba5d6-169">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="ba5d6-169">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="ba5d6-170">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="ba5d6-170">Cognitive Services</span></span>

* <span data-ttu-id="ba5d6-171">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-171">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="ba5d6-172">消費</span><span class="sxs-lookup"><span data-stu-id="ba5d6-172">Consumption</span></span>

* <span data-ttu-id="ba5d6-173">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-173">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="ba5d6-174">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-174">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="ba5d6-175">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ba5d6-175">Container</span></span>

* <span data-ttu-id="ba5d6-176">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-176">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="ba5d6-177">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-177">Network</span></span>

* <span data-ttu-id="ba5d6-178">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正: `network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="ba5d6-178">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="ba5d6-179">リソース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-179">Resource</span></span>

* <span data-ttu-id="ba5d6-180">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-180">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="ba5d6-181">役割</span><span class="sxs-lookup"><span data-stu-id="ba5d6-181">Role</span></span>

* <span data-ttu-id="ba5d6-182">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-182">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="ba5d6-183">SQL</span><span class="sxs-lookup"><span data-stu-id="ba5d6-183">SQL</span></span>

* <span data-ttu-id="ba5d6-184">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-184">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="ba5d6-185">Storage</span><span class="sxs-lookup"><span data-stu-id="ba5d6-185">Storage</span></span>

* <span data-ttu-id="ba5d6-186">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-186">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-187">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-187">VM</span></span>

* <span data-ttu-id="ba5d6-188">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-188">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="ba5d6-189">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-189">February 13, 2018</span></span>

<span data-ttu-id="ba5d6-190">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="ba5d6-190">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="ba5d6-191">コア</span><span class="sxs-lookup"><span data-stu-id="ba5d6-191">Core</span></span>

* <span data-ttu-id="ba5d6-192">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-192">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-193">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-193">ACS</span></span>

* <span data-ttu-id="ba5d6-194">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-194">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="ba5d6-195">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-195">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="ba5d6-196">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-196">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="ba5d6-197">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-197">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="ba5d6-198">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-198">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="ba5d6-199">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-199">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="ba5d6-200">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-200">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="ba5d6-201">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="ba5d6-201">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-202">Appservice</span><span class="sxs-lookup"><span data-stu-id="ba5d6-202">Appservice</span></span>

* <span data-ttu-id="ba5d6-203">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-203">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="ba5d6-204">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-204">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="ba5d6-205">CDN</span><span class="sxs-lookup"><span data-stu-id="ba5d6-205">CDN</span></span>

* <span data-ttu-id="ba5d6-206">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-206">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="ba5d6-207">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ba5d6-207">Container</span></span>

* <span data-ttu-id="ba5d6-208">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-208">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="ba5d6-209">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-209">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ba5d6-210">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ba5d6-210">CosmosDB</span></span>

* <span data-ttu-id="ba5d6-211">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-211">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="ba5d6-212">内線番号</span><span class="sxs-lookup"><span data-stu-id="ba5d6-212">Extension</span></span>

* <span data-ttu-id="ba5d6-213">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-213">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="ba5d6-214">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-214">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="ba5d6-215">フィードバック</span><span class="sxs-lookup"><span data-stu-id="ba5d6-215">Feedback</span></span>

* <span data-ttu-id="ba5d6-216">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-216">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="ba5d6-217">対話</span><span class="sxs-lookup"><span data-stu-id="ba5d6-217">Interactive</span></span>

* <span data-ttu-id="ba5d6-218">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-218">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="ba5d6-219">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-219">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="ba5d6-220">IoT</span><span class="sxs-lookup"><span data-stu-id="ba5d6-220">IoT</span></span>

* <span data-ttu-id="ba5d6-221">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-221">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success.</span></span>
* <span data-ttu-id="ba5d6-222">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-222">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success.</span></span>
* <span data-ttu-id="ba5d6-223">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-223">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="ba5d6-224">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-224">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="ba5d6-225">監視</span><span class="sxs-lookup"><span data-stu-id="ba5d6-225">Monitor</span></span>

* <span data-ttu-id="ba5d6-226">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-226">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="ba5d6-227">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-227">Network</span></span>

* <span data-ttu-id="ba5d6-228">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-228">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="ba5d6-229">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ba5d6-229">Profile</span></span>

* <span data-ttu-id="ba5d6-230">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-230">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="ba5d6-231">リソース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-231">Resource</span></span>

* <span data-ttu-id="ba5d6-232">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-232">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="ba5d6-233">役割</span><span class="sxs-lookup"><span data-stu-id="ba5d6-233">Role</span></span>

* <span data-ttu-id="ba5d6-234">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-234">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="ba5d6-235">SQL</span><span class="sxs-lookup"><span data-stu-id="ba5d6-235">SQL</span></span>

* <span data-ttu-id="ba5d6-236">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-236">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="ba5d6-237">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-237">Added `sql db rename`</span></span>
* <span data-ttu-id="ba5d6-238">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-238">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="ba5d6-239">Storage</span><span class="sxs-lookup"><span data-stu-id="ba5d6-239">Storage</span></span>

* <span data-ttu-id="ba5d6-240">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-240">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-241">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-241">VM</span></span>

* <span data-ttu-id="ba5d6-242">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-242">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="ba5d6-243">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-243">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="ba5d6-244">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-244">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="ba5d6-245">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-245">January 31, 2018</span></span>

<span data-ttu-id="ba5d6-246">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="ba5d6-246">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="ba5d6-247">コア</span><span class="sxs-lookup"><span data-stu-id="ba5d6-247">Core</span></span>

* <span data-ttu-id="ba5d6-248">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-248">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="ba5d6-249">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-249">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="ba5d6-250">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-250">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="ba5d6-251">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-251">Use `--verbose` to see</span></span>
* <span data-ttu-id="ba5d6-252">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-252">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-253">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-253">ACS</span></span>

* <span data-ttu-id="ba5d6-254">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-254">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="ba5d6-255">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-255">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-256">Appservice</span><span class="sxs-lookup"><span data-stu-id="ba5d6-256">Appservice</span></span>

* <span data-ttu-id="ba5d6-257">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-257">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="ba5d6-258">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-258">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="ba5d6-259">CDN</span><span class="sxs-lookup"><span data-stu-id="ba5d6-259">CDN</span></span>

* <span data-ttu-id="ba5d6-260">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-260">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ba5d6-261">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ba5d6-261">CosmosDB</span></span>

* <span data-ttu-id="ba5d6-262">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-262">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="ba5d6-263">対話</span><span class="sxs-lookup"><span data-stu-id="ba5d6-263">Interactive</span></span>

* <span data-ttu-id="ba5d6-264">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-264">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="ba5d6-265">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-265">Network</span></span>

* <span data-ttu-id="ba5d6-266">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-266">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="ba5d6-267">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-267">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="ba5d6-268">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-268">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="ba5d6-269">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-269">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="ba5d6-270">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-270">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="ba5d6-271">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-271">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="ba5d6-272">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-272">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="ba5d6-273">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-273">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="ba5d6-274">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-274">Fixed issue where certain records were imported twice with `dns zone import`</span></span> 
* <span data-ttu-id="ba5d6-275">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-275">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="ba5d6-276">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ba5d6-276">Profile</span></span>

* <span data-ttu-id="ba5d6-277">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-277">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="ba5d6-278">リソース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-278">Resource</span></span>

* <span data-ttu-id="ba5d6-279">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-279">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="ba5d6-280">Storage</span><span class="sxs-lookup"><span data-stu-id="ba5d6-280">Storage</span></span>

* <span data-ttu-id="ba5d6-281">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-281">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="ba5d6-282">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-282">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="ba5d6-283">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-283">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>  
* <span data-ttu-id="ba5d6-284">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-284">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="ba5d6-285">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-285">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-286">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-286">VM</span></span>

* <span data-ttu-id="ba5d6-287">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-287">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="ba5d6-288">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-288">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="ba5d6-289">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-289">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="ba5d6-290">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-290">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="ba5d6-291">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-291">January 17, 2018</span></span>

<span data-ttu-id="ba5d6-292">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="ba5d6-292">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="ba5d6-293">ACR</span><span class="sxs-lookup"><span data-stu-id="ba5d6-293">ACR</span></span>

* <span data-ttu-id="ba5d6-294">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-294">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="ba5d6-295">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-295">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-296">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-296">ACS</span></span>

* <span data-ttu-id="ba5d6-297">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-297">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="ba5d6-298">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-298">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-299">Appservice</span><span class="sxs-lookup"><span data-stu-id="ba5d6-299">Appservice</span></span>

* <span data-ttu-id="ba5d6-300">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-300">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="ba5d6-301">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-301">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="ba5d6-302">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-302">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="ba5d6-303">バックアップ</span><span class="sxs-lookup"><span data-stu-id="ba5d6-303">Backup</span></span>

* <span data-ttu-id="ba5d6-304">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-304">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="ba5d6-305">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-305">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="ba5d6-306">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-306">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="ba5d6-307">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-307">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="ba5d6-308">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-308">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="ba5d6-309">Batch</span><span class="sxs-lookup"><span data-stu-id="ba5d6-309">Batch</span></span>

* <span data-ttu-id="ba5d6-310">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-310">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="ba5d6-311">クラウド</span><span class="sxs-lookup"><span data-stu-id="ba5d6-311">Cloud</span></span>

* <span data-ttu-id="ba5d6-312">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-312">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="ba5d6-313">消費</span><span class="sxs-lookup"><span data-stu-id="ba5d6-313">Consumption</span></span>

* <span data-ttu-id="ba5d6-314">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-314">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="ba5d6-315">Event Grid</span><span class="sxs-lookup"><span data-stu-id="ba5d6-315">Event Grid</span></span>

* <span data-ttu-id="ba5d6-316">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-316">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="ba5d6-317">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-317">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="ba5d6-318">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-318">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="ba5d6-319">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="ba5d6-319">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="ba5d6-320">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-320">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="ba5d6-321">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-321">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="ba5d6-322">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-322">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="ba5d6-323">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-323">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="ba5d6-324">対話</span><span class="sxs-lookup"><span data-stu-id="ba5d6-324">Interactive</span></span>

* <span data-ttu-id="ba5d6-325">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-325">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="ba5d6-326">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-326">Fixed errors on startup</span></span>
* <span data-ttu-id="ba5d6-327">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-327">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="ba5d6-328">IoT</span><span class="sxs-lookup"><span data-stu-id="ba5d6-328">IoT</span></span>

* <span data-ttu-id="ba5d6-329">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-329">Added support for device provisioning service</span></span>
* <span data-ttu-id="ba5d6-330">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-330">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="ba5d6-331">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-331">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="ba5d6-332">監視</span><span class="sxs-lookup"><span data-stu-id="ba5d6-332">Monitor</span></span>

* <span data-ttu-id="ba5d6-333">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-333">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="ba5d6-334">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-334">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="ba5d6-335">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-335">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="ba5d6-336">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-336">Network</span></span>

* <span data-ttu-id="ba5d6-337">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-337">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="ba5d6-338">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-338">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="ba5d6-339">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ba5d6-339">Profile</span></span>

* <span data-ttu-id="ba5d6-340">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-340">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="ba5d6-341">役割</span><span class="sxs-lookup"><span data-stu-id="ba5d6-341">Role</span></span>

* <span data-ttu-id="ba5d6-342">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-342">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="ba5d6-343">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ba5d6-343">Service Fabric</span></span>

* <span data-ttu-id="ba5d6-344">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-344">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="ba5d6-345">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-345">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-346">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-346">VM</span></span>

* <span data-ttu-id="ba5d6-347">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="ba5d6-347">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="ba5d6-348">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-348">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="ba5d6-349">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-349">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="ba5d6-350">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-350">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="ba5d6-351">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-351">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="ba5d6-352">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-352">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="ba5d6-353">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-353">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="ba5d6-354">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-354">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="ba5d6-355">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-355">December 19, 2017</span></span>

<span data-ttu-id="ba5d6-356">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="ba5d6-356">Version 2.0.23</span></span>

* <span data-ttu-id="ba5d6-357">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-357">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="ba5d6-358">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ba5d6-358">Container</span></span>

* <span data-ttu-id="ba5d6-359">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-359">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="ba5d6-360">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-360">Network</span></span>

* <span data-ttu-id="ba5d6-361">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-361">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="ba5d6-362">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-362">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="ba5d6-363">Storage</span><span class="sxs-lookup"><span data-stu-id="ba5d6-363">Storage</span></span>

* <span data-ttu-id="ba5d6-364">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-364">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-365">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-365">VM</span></span>

* <span data-ttu-id="ba5d6-366">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-366">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="ba5d6-367">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-367">December 5, 2017</span></span>

<span data-ttu-id="ba5d6-368">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="ba5d6-368">Version 2.0.22</span></span>

* <span data-ttu-id="ba5d6-369">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-369">Removed `az component` commands.</span></span> <span data-ttu-id="ba5d6-370">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="ba5d6-370">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="ba5d6-371">コア</span><span class="sxs-lookup"><span data-stu-id="ba5d6-371">Core</span></span>
* <span data-ttu-id="ba5d6-372">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-372">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="ba5d6-373">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-373">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-374">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-374">ACS</span></span>

* <span data-ttu-id="ba5d6-375">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-375">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="ba5d6-376">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-376">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="ba5d6-377">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-377">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="ba5d6-378">Advisor</span><span class="sxs-lookup"><span data-stu-id="ba5d6-378">Advisor</span></span>

* <span data-ttu-id="ba5d6-379">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-379">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-380">Appservice</span><span class="sxs-lookup"><span data-stu-id="ba5d6-380">Appservice</span></span>

* <span data-ttu-id="ba5d6-381">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-381">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="ba5d6-382">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-382">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="ba5d6-383">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-383">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="ba5d6-384">消費</span><span class="sxs-lookup"><span data-stu-id="ba5d6-384">Consumption</span></span>

* <span data-ttu-id="ba5d6-385">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-385">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="ba5d6-386">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ba5d6-386">Container</span></span>

* <span data-ttu-id="ba5d6-387">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-387">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="ba5d6-388">監視</span><span class="sxs-lookup"><span data-stu-id="ba5d6-388">Monitor</span></span>

* <span data-ttu-id="ba5d6-389">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-389">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="ba5d6-390">リソース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-390">Resource</span></span>

* <span data-ttu-id="ba5d6-391">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-391">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="ba5d6-392">役割</span><span class="sxs-lookup"><span data-stu-id="ba5d6-392">Role</span></span>

* <span data-ttu-id="ba5d6-393">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-393">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="ba5d6-394">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-394">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="ba5d6-395">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-395">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="ba5d6-396">SQL</span><span class="sxs-lookup"><span data-stu-id="ba5d6-396">SQL</span></span>

* <span data-ttu-id="ba5d6-397">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-397">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="ba5d6-398">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-398">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-399">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-399">VM</span></span>

* <span data-ttu-id="ba5d6-400">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-400">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="ba5d6-401">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-401">November 14, 2017</span></span>

<span data-ttu-id="ba5d6-402">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="ba5d6-402">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="ba5d6-403">ACR</span><span class="sxs-lookup"><span data-stu-id="ba5d6-403">ACR</span></span>

* <span data-ttu-id="ba5d6-404">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-404">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="ba5d6-405">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-405">ACS</span></span>

* <span data-ttu-id="ba5d6-406">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-406">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="ba5d6-407">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-407">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="ba5d6-408">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-408">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="ba5d6-409">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-409">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="ba5d6-410">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-410">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-411">Appservice</span><span class="sxs-lookup"><span data-stu-id="ba5d6-411">Appservice</span></span>

* <span data-ttu-id="ba5d6-412">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-412">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="ba5d6-413">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-413">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="ba5d6-414">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-414">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="ba5d6-415">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-415">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="ba5d6-416">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-416">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="ba5d6-417">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-417">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="ba5d6-418">Batch</span><span class="sxs-lookup"><span data-stu-id="ba5d6-418">Batch</span></span>

* <span data-ttu-id="ba5d6-419">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-419">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="ba5d6-420">Batchai</span><span class="sxs-lookup"><span data-stu-id="ba5d6-420">Batchai</span></span>

* <span data-ttu-id="ba5d6-421">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-421">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="ba5d6-422">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-422">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="ba5d6-423">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-423">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="ba5d6-424">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-424">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="ba5d6-425">クラウド</span><span class="sxs-lookup"><span data-stu-id="ba5d6-425">Cloud</span></span>

* <span data-ttu-id="ba5d6-426">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-426">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="ba5d6-427">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ba5d6-427">Container</span></span>

* <span data-ttu-id="ba5d6-428">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-428">Added support to open multiple ports</span></span>
* <span data-ttu-id="ba5d6-429">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-429">Added container group restart policy</span></span>
* <span data-ttu-id="ba5d6-430">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-430">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="ba5d6-431">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-431">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="ba5d6-432">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="ba5d6-432">Data Lake Analytics</span></span>

* <span data-ttu-id="ba5d6-433">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-433">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="ba5d6-434">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ba5d6-434">Data Lake Store</span></span>

* <span data-ttu-id="ba5d6-435">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-435">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="ba5d6-436">内線番号</span><span class="sxs-lookup"><span data-stu-id="ba5d6-436">Extension</span></span>

* <span data-ttu-id="ba5d6-437">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-437">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="ba5d6-438">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-438">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="ba5d6-439">IoT</span><span class="sxs-lookup"><span data-stu-id="ba5d6-439">IoT</span></span>

* <span data-ttu-id="ba5d6-440">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-440">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="ba5d6-441">監視</span><span class="sxs-lookup"><span data-stu-id="ba5d6-441">Monitor</span></span>

* <span data-ttu-id="ba5d6-442">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-442">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="ba5d6-443">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-443">Network</span></span>

* <span data-ttu-id="ba5d6-444">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-444">Added support for CAA DNS records</span></span>
* <span data-ttu-id="ba5d6-445">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-445">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="ba5d6-446">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-446">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="ba5d6-447">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-447">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="ba5d6-448">Reservations</span><span class="sxs-lookup"><span data-stu-id="ba5d6-448">Reservations</span></span>

* <span data-ttu-id="ba5d6-449">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-449">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="ba5d6-450">リソース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-450">Resource</span></span>

* <span data-ttu-id="ba5d6-451">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-451">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="ba5d6-452">SQL</span><span class="sxs-lookup"><span data-stu-id="ba5d6-452">SQL</span></span>

* <span data-ttu-id="ba5d6-453">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-453">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="ba5d6-454">Storage</span><span class="sxs-lookup"><span data-stu-id="ba5d6-454">Storage</span></span>

* <span data-ttu-id="ba5d6-455">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-455">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="ba5d6-456">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-456">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="ba5d6-457">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-457">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="ba5d6-458">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-458">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="ba5d6-459">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-459">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="ba5d6-460">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-460">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="ba5d6-461">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-461">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-462">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-462">VM</span></span>

* <span data-ttu-id="ba5d6-463">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-463">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="ba5d6-464">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-464">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="ba5d6-465">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-465">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="ba5d6-466">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-466">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="ba5d6-467">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-467">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="ba5d6-468">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-468">October 24, 2017</span></span>

<span data-ttu-id="ba5d6-469">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="ba5d6-469">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="ba5d6-470">コア</span><span class="sxs-lookup"><span data-stu-id="ba5d6-470">Core</span></span>

* <span data-ttu-id="ba5d6-471">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-471">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="ba5d6-472">ACR</span><span class="sxs-lookup"><span data-stu-id="ba5d6-472">ACR</span></span>

* <span data-ttu-id="ba5d6-473">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-473">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="ba5d6-474">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-474">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="ba5d6-475">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-475">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-476">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-476">ACS</span></span>

* <span data-ttu-id="ba5d6-477">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-477">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="ba5d6-478">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-478">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-479">Appservice</span><span class="sxs-lookup"><span data-stu-id="ba5d6-479">Appservice</span></span>

* <span data-ttu-id="ba5d6-480">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-480">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="ba5d6-481">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ba5d6-481">Component</span></span>

* <span data-ttu-id="ba5d6-482">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-482">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="ba5d6-483">監視</span><span class="sxs-lookup"><span data-stu-id="ba5d6-483">Monitor</span></span>

* <span data-ttu-id="ba5d6-484">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-484">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="ba5d6-485">リソース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-485">Resource</span></span>

* <span data-ttu-id="ba5d6-486">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-486">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="ba5d6-487">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-487">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-488">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-488">VM</span></span>

* <span data-ttu-id="ba5d6-489">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-489">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="ba5d6-490">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-490">October 9, 2017</span></span>

<span data-ttu-id="ba5d6-491">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="ba5d6-491">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="ba5d6-492">コア</span><span class="sxs-lookup"><span data-stu-id="ba5d6-492">Core</span></span>

* <span data-ttu-id="ba5d6-493">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-493">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-494">Appservice</span><span class="sxs-lookup"><span data-stu-id="ba5d6-494">Appservice</span></span>

* <span data-ttu-id="ba5d6-495">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-495">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="ba5d6-496">Batch</span><span class="sxs-lookup"><span data-stu-id="ba5d6-496">Batch</span></span>

* <span data-ttu-id="ba5d6-497">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-497">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="ba5d6-498">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-498">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="ba5d6-499">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-499">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="ba5d6-500">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-500">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="ba5d6-501">Batchai</span><span class="sxs-lookup"><span data-stu-id="ba5d6-501">Batchai</span></span>

* <span data-ttu-id="ba5d6-502">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-502">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="ba5d6-503">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba5d6-503">Keyvault</span></span>

* <span data-ttu-id="ba5d6-504">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-504">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="ba5d6-505">(#4448)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-505">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="ba5d6-506">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-506">Network</span></span>

* <span data-ttu-id="ba5d6-507">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-507">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="ba5d6-508">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-508">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="ba5d6-509">リソース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-509">Resource</span></span>

* <span data-ttu-id="ba5d6-510">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-510">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="ba5d6-511">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-511">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="ba5d6-512">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-512">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="ba5d6-513">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-513">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="ba5d6-514">SQL</span><span class="sxs-lookup"><span data-stu-id="ba5d6-514">Sql</span></span>

* <span data-ttu-id="ba5d6-515">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-515">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="ba5d6-516">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-516">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="ba5d6-517">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-517">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="ba5d6-518">Storage</span><span class="sxs-lookup"><span data-stu-id="ba5d6-518">Storage</span></span>

* <span data-ttu-id="ba5d6-519">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-519">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-520">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-520">Vm</span></span>

* <span data-ttu-id="ba5d6-521">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-521">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="ba5d6-522">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-522">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="ba5d6-523">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-523">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="ba5d6-524">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-524">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="ba5d6-525">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-525">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="ba5d6-526">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-526">September 22, 2017</span></span>

<span data-ttu-id="ba5d6-527">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="ba5d6-527">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="ba5d6-528">リソース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-528">Resource</span></span>

* <span data-ttu-id="ba5d6-529">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-529">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="ba5d6-530">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-530">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="ba5d6-531">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-531">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="ba5d6-532">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-532">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="ba5d6-533">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-533">Network</span></span>

* <span data-ttu-id="ba5d6-534">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-534">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="ba5d6-535">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-535">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="ba5d6-536">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-536">Added `asg` application security group commands</span></span>
* <span data-ttu-id="ba5d6-537">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-537">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="ba5d6-538">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-538">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="ba5d6-539">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-539">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="ba5d6-540">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-540">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="ba5d6-541">Storage</span><span class="sxs-lookup"><span data-stu-id="ba5d6-541">Storage</span></span>

* <span data-ttu-id="ba5d6-542">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-542">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="ba5d6-543">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="ba5d6-543">Eventgrid</span></span>

* <span data-ttu-id="ba5d6-544">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-544">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="ba5d6-545">SQL</span><span class="sxs-lookup"><span data-stu-id="ba5d6-545">SQL</span></span>

* <span data-ttu-id="ba5d6-546">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-546">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="ba5d6-547">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="ba5d6-547">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="ba5d6-548">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-548">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="ba5d6-549">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba5d6-549">Keyvault</span></span>

* <span data-ttu-id="ba5d6-550">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-550">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-551">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-551">VM</span></span>

* <span data-ttu-id="ba5d6-552">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-552">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="ba5d6-553">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-553">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="ba5d6-554">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-554">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="ba5d6-555">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-555">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="ba5d6-556">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-556">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="ba5d6-557">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-557">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-558">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-558">ACS</span></span>

* <span data-ttu-id="ba5d6-559">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-559">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-560">Appservice</span><span class="sxs-lookup"><span data-stu-id="ba5d6-560">Appservice</span></span>

* <span data-ttu-id="ba5d6-561">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-561">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="ba5d6-562">バックアップ</span><span class="sxs-lookup"><span data-stu-id="ba5d6-562">Backup</span></span>

* <span data-ttu-id="ba5d6-563">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-563">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="ba5d6-564">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-564">September 11, 2017</span></span>

<span data-ttu-id="ba5d6-565">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="ba5d6-565">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="ba5d6-566">コア</span><span class="sxs-lookup"><span data-stu-id="ba5d6-566">Core</span></span>

* <span data-ttu-id="ba5d6-567">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-567">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="ba5d6-568">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-568">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-569">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-569">Acs</span></span>

* <span data-ttu-id="ba5d6-570">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-570">Added `acs list-locations` command</span></span>
* <span data-ttu-id="ba5d6-571">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-571">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-572">Appservice</span><span class="sxs-lookup"><span data-stu-id="ba5d6-572">Appservice</span></span>

* <span data-ttu-id="ba5d6-573">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-573">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="ba5d6-574">CDN</span><span class="sxs-lookup"><span data-stu-id="ba5d6-574">CDN</span></span>

* <span data-ttu-id="ba5d6-575">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-575">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="ba5d6-576">内線番号</span><span class="sxs-lookup"><span data-stu-id="ba5d6-576">Extension</span></span>

* <span data-ttu-id="ba5d6-577">最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-577">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="ba5d6-578">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba5d6-578">Keyvault</span></span>

* <span data-ttu-id="ba5d6-579">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-579">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="ba5d6-580">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-580">Network</span></span>

* <span data-ttu-id="ba5d6-581">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-581">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="ba5d6-582">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-582">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="ba5d6-583">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-583">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="ba5d6-584">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-584">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="ba5d6-585">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-585">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="ba5d6-586">リソース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-586">Resource</span></span>

* <span data-ttu-id="ba5d6-587">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-587">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="ba5d6-588">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-588">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="ba5d6-589">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-589">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="ba5d6-590">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-590">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="ba5d6-591">SQL</span><span class="sxs-lookup"><span data-stu-id="ba5d6-591">SQL</span></span>

* <span data-ttu-id="ba5d6-592">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-592">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-593">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-593">VM</span></span>

* <span data-ttu-id="ba5d6-594">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="ba5d6-594">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="ba5d6-595">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="ba5d6-595">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="ba5d6-596">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-596">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="ba5d6-597">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="ba5d6-597">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="ba5d6-598">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="ba5d6-598">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="ba5d6-599">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-599">August 31, 2017</span></span>

<span data-ttu-id="ba5d6-600">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="ba5d6-600">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="ba5d6-601">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba5d6-601">Keyvault</span></span>

* <span data-ttu-id="ba5d6-602">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-602">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="ba5d6-603">SF</span><span class="sxs-lookup"><span data-stu-id="ba5d6-603">Sf</span></span>

* <span data-ttu-id="ba5d6-604">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="ba5d6-604">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="ba5d6-605">Storage</span><span class="sxs-lookup"><span data-stu-id="ba5d6-605">Storage</span></span>

* <span data-ttu-id="ba5d6-606">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-606">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="ba5d6-607">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-607">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="ba5d6-608">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-608">August 28, 2017</span></span>

<span data-ttu-id="ba5d6-609">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="ba5d6-609">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="ba5d6-610">CLI</span><span class="sxs-lookup"><span data-stu-id="ba5d6-610">CLI</span></span>

* <span data-ttu-id="ba5d6-611">`--version` に法的事項を追加しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-611">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-612">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-612">ACS</span></span>

* <span data-ttu-id="ba5d6-613">プレビュー リージョンを修正しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-613">Corrected preview regions.</span></span>
* <span data-ttu-id="ba5d6-614">既定の `dns_name_prefix` を正しい形式にしました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-614">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="ba5d6-615">ACS コマンド出力を最適化しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-615">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-616">Appservice</span><span class="sxs-lookup"><span data-stu-id="ba5d6-616">Appservice</span></span>

* <span data-ttu-id="ba5d6-617">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-617">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="ba5d6-618">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-618">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="ba5d6-619">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-619">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="ba5d6-620">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-620">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="ba5d6-621">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="ba5d6-621">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="ba5d6-622">IoT</span><span class="sxs-lookup"><span data-stu-id="ba5d6-622">IoT</span></span>

* <span data-ttu-id="ba5d6-623">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-623">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="ba5d6-624">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-624">Network</span></span>

* <span data-ttu-id="ba5d6-625">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-625">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="ba5d6-626">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-626">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="ba5d6-627">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-627">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="ba5d6-628">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-628">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="ba5d6-629">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-629">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="ba5d6-630">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ba5d6-630">Profile</span></span>

* <span data-ttu-id="ba5d6-631">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-631">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="ba5d6-632">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ba5d6-632">Service Fabric</span></span>

* <span data-ttu-id="ba5d6-633">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-633">Preview release</span></span>
* <span data-ttu-id="ba5d6-634">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-634">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="ba5d6-635">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-635">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="ba5d6-636">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-636">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="ba5d6-637">Storage</span><span class="sxs-lookup"><span data-stu-id="ba5d6-637">Storage</span></span>

* <span data-ttu-id="ba5d6-638">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-638">Enabled setting blob tier</span></span>
* <span data-ttu-id="ba5d6-639">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-639">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="ba5d6-640">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-640">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="ba5d6-641">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-641">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="ba5d6-642">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-642">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="ba5d6-643">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="ba5d6-643">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-644">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-644">VM</span></span>

* <span data-ttu-id="ba5d6-645">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-645">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="ba5d6-646">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-646">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="ba5d6-647">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-647">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="ba5d6-648">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-648">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="ba5d6-649">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-649">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="ba5d6-650">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-650">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="ba5d6-651">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-651">August 15, 2017</span></span>

<span data-ttu-id="ba5d6-652">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="ba5d6-652">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-653">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-653">ACS</span></span>

* <span data-ttu-id="ba5d6-654">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-654">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-655">Appservice</span><span class="sxs-lookup"><span data-stu-id="ba5d6-655">Appservice</span></span>

* <span data-ttu-id="ba5d6-656">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-656">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="ba5d6-657">Event Grid</span><span class="sxs-lookup"><span data-stu-id="ba5d6-657">Event Grid</span></span>

* <span data-ttu-id="ba5d6-658">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-658">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="ba5d6-659">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-659">August 11, 2017</span></span>

<span data-ttu-id="ba5d6-660">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="ba5d6-660">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-661">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-661">ACS</span></span>

* <span data-ttu-id="ba5d6-662">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-662">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="ba5d6-663">Batch</span><span class="sxs-lookup"><span data-stu-id="ba5d6-663">Batch</span></span>

* <span data-ttu-id="ba5d6-664">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-664">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="ba5d6-665">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-665">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="ba5d6-666">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-666">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="ba5d6-667">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-667">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="ba5d6-668">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-668">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="ba5d6-669">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-669">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="ba5d6-670">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ba5d6-670">Component</span></span>

* <span data-ttu-id="ba5d6-671">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-671">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="ba5d6-672">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ba5d6-672">Container</span></span>

* <span data-ttu-id="ba5d6-673">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-673">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="ba5d6-674">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ba5d6-674">Data Lake Store</span></span>

* <span data-ttu-id="ba5d6-675">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-675">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="ba5d6-676">Event Grid</span><span class="sxs-lookup"><span data-stu-id="ba5d6-676">Event Grid</span></span>

* <span data-ttu-id="ba5d6-677">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-677">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="ba5d6-678">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-678">Network</span></span>

* <span data-ttu-id="ba5d6-679">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-679">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="ba5d6-680">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-680">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="ba5d6-681">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-681">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="ba5d6-682">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-682">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="ba5d6-683">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ba5d6-683">Profile</span></span>

* <span data-ttu-id="ba5d6-684">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-684">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="ba5d6-685">Storage</span><span class="sxs-lookup"><span data-stu-id="ba5d6-685">Storage</span></span>

* <span data-ttu-id="ba5d6-686">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-686">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-687">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-687">VM</span></span>

* <span data-ttu-id="ba5d6-688">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-688">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="ba5d6-689">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-689">Exposed `list-skus` command</span></span>
* <span data-ttu-id="ba5d6-690">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-690">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="ba5d6-691">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-691">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="ba5d6-692">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-692">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="ba5d6-693">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-693">July 28, 2017</span></span>

<span data-ttu-id="ba5d6-694">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="ba5d6-694">Version 2.0.12</span></span>

* <span data-ttu-id="ba5d6-695">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-695">Added container commands</span></span>
* <span data-ttu-id="ba5d6-696">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-696">Added billing and consumption modules</span></span>

```
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

### <a name="core"></a><span data-ttu-id="ba5d6-697">コア</span><span class="sxs-lookup"><span data-stu-id="ba5d6-697">Core</span></span>

* <span data-ttu-id="ba5d6-698">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-698">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="ba5d6-699">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-699">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="ba5d6-700">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-700">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="ba5d6-701">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-701">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="ba5d6-702">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-702">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="ba5d6-703">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-703">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="ba5d6-704">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-704">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="ba5d6-705">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-705">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="ba5d6-706">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-706">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="ba5d6-707">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-707">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="ba5d6-708">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-708">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="ba5d6-709">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-709">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="ba5d6-710">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-710">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="ba5d6-711">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-711">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="ba5d6-712">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-712">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="ba5d6-713">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-713">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="ba5d6-714">ACR</span><span class="sxs-lookup"><span data-stu-id="ba5d6-714">ACR</span></span>

* <span data-ttu-id="ba5d6-715">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-715">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="ba5d6-716">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-716">Support SKU update for managed registries</span></span>
* <span data-ttu-id="ba5d6-717">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-717">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="ba5d6-718">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-718">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="ba5d6-719">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-719">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="ba5d6-720">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-720">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-721">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-721">ACS</span></span>

* <span data-ttu-id="ba5d6-722">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-722">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-723">Appservice</span><span class="sxs-lookup"><span data-stu-id="ba5d6-723">Appservice</span></span>

* <span data-ttu-id="ba5d6-724">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-724">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="ba5d6-725">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-725">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="ba5d6-726">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-726">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="ba5d6-727">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-727">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="ba5d6-728">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-728">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="ba5d6-729">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-729">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="ba5d6-730">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-730">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="ba5d6-731">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-731">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="ba5d6-732">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-732">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="ba5d6-733">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="ba5d6-733">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="ba5d6-734">Batch</span><span class="sxs-lookup"><span data-stu-id="ba5d6-734">Batch</span></span>

* <span data-ttu-id="ba5d6-735">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-735">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="ba5d6-736">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-736">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="ba5d6-737">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-737">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="ba5d6-738">CDN</span><span class="sxs-lookup"><span data-stu-id="ba5d6-738">CDN</span></span>

* <span data-ttu-id="ba5d6-739">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-739">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="ba5d6-740">クラウド</span><span class="sxs-lookup"><span data-stu-id="ba5d6-740">Cloud</span></span>

* <span data-ttu-id="ba5d6-741">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-741">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="ba5d6-742">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="ba5d6-742">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="ba5d6-743">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-743">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="ba5d6-744">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-744">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="ba5d6-745">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-745">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ba5d6-746">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ba5d6-746">CosmosDB</span></span>

* <span data-ttu-id="ba5d6-747">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-747">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="ba5d6-748">既定のコレクション TTL のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-748">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="ba5d6-749">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="ba5d6-749">Data Lake Analytics</span></span>

* <span data-ttu-id="ba5d6-750">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-750">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="ba5d6-751">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-751">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="ba5d6-752">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-752">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="ba5d6-753">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ba5d6-753">Data Lake Store</span></span>

* <span data-ttu-id="ba5d6-754">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-754">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="ba5d6-755">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-755">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="ba5d6-756">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-756">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="ba5d6-757">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="ba5d6-757">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="ba5d6-758">対話</span><span class="sxs-lookup"><span data-stu-id="ba5d6-758">Interactive</span></span>

* <span data-ttu-id="ba5d6-759">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-759">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="ba5d6-760">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-760">Increased test coverage</span></span>
* <span data-ttu-id="ba5d6-761">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-761">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="ba5d6-762">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-762">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="ba5d6-763">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-763">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="ba5d6-764">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-764">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="ba5d6-765">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-765">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="ba5d6-766">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-766">Added `--progress` flag</span></span>
* <span data-ttu-id="ba5d6-767">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-767">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="ba5d6-768">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-768">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="ba5d6-769">IoT</span><span class="sxs-lookup"><span data-stu-id="ba5d6-769">IoT</span></span>

* <span data-ttu-id="ba5d6-770">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-770">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="ba5d6-771">(#3934)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-771">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="ba5d6-772">Key Vault</span><span class="sxs-lookup"><span data-stu-id="ba5d6-772">Key vault</span></span>

* <span data-ttu-id="ba5d6-773">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-773">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="ba5d6-774">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ba5d6-774">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="ba5d6-775">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ba5d6-775">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="ba5d6-776">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ba5d6-776">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="ba5d6-777">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ba5d6-777">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="ba5d6-778">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-778">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="ba5d6-779">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-779">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="ba5d6-780">(#3307)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-780">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="ba5d6-781">ラボ</span><span class="sxs-lookup"><span data-stu-id="ba5d6-781">Lab</span></span>

* <span data-ttu-id="ba5d6-782">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-782">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="ba5d6-783">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-783">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="ba5d6-784">監視</span><span class="sxs-lookup"><span data-stu-id="ba5d6-784">Monitor</span></span>

* <span data-ttu-id="ba5d6-785">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-785">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="ba5d6-786">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-786">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="ba5d6-787">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-787">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="ba5d6-788">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-788">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="ba5d6-789">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-789">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="ba5d6-790">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-790">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="ba5d6-791">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-791">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="ba5d6-792">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-792">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="ba5d6-793">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-793">`location` no longer required</span></span>
  * <span data-ttu-id="ba5d6-794">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-794">Add name and ID support for target</span></span>
  * <span data-ttu-id="ba5d6-795">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-795">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="ba5d6-796">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-796">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="ba5d6-797">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-797">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="ba5d6-798">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-798">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="ba5d6-799">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-799">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="ba5d6-800">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-800">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="ba5d6-801">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-801">Network</span></span>

* <span data-ttu-id="ba5d6-802">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-802">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="ba5d6-803">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-803">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="ba5d6-804">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-804">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="ba5d6-805">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-805">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="ba5d6-806">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-806">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="ba5d6-807">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-807">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="ba5d6-808">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-808">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="ba5d6-809">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-809">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="ba5d6-810">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-810">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="ba5d6-811">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-811">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="ba5d6-812">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-812">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="ba5d6-813">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-813">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="ba5d6-814">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-814">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="ba5d6-815">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-815">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="ba5d6-816">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-816">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="ba5d6-817">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-817">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="ba5d6-818">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-818">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="ba5d6-819">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-819">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="ba5d6-820">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-820">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="ba5d6-821">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-821">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="ba5d6-822">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-822">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="ba5d6-823">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-823">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="ba5d6-824">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-824">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="ba5d6-825">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-825">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="ba5d6-826">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-826">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="ba5d6-827">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-827">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="ba5d6-828">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-828">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="ba5d6-829">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ba5d6-829">Profile</span></span>

* <span data-ttu-id="ba5d6-830">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-830">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="ba5d6-831">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-831">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="ba5d6-832">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-832">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="ba5d6-833">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-833">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="ba5d6-834">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-834">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="ba5d6-835">RDBMS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-835">RDBMS</span></span>

* <span data-ttu-id="ba5d6-836">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-836">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="ba5d6-837">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-837">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="ba5d6-838">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-838">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="ba5d6-839">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-839">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="ba5d6-840">リソース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-840">Resource</span></span>

* <span data-ttu-id="ba5d6-841">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-841">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="ba5d6-842">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-842">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="ba5d6-843">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-843">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="ba5d6-844">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-844">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="ba5d6-845">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-845">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="ba5d6-846">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-846">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="ba5d6-847">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-847">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="ba5d6-848">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-848">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="ba5d6-849">役割</span><span class="sxs-lookup"><span data-stu-id="ba5d6-849">Role</span></span>

* <span data-ttu-id="ba5d6-850">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-850">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="ba5d6-851">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-851">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="ba5d6-852">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="ba5d6-852">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="ba5d6-853">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-853">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="ba5d6-854">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-854">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="ba5d6-855">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ba5d6-855">Service Fabric</span></span>
* <span data-ttu-id="ba5d6-856">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-856">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="ba5d6-857">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-857">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="ba5d6-858">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-858">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="ba5d6-859">SQL</span><span class="sxs-lookup"><span data-stu-id="ba5d6-859">SQL</span></span>

* <span data-ttu-id="ba5d6-860">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-860">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="ba5d6-861">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-861">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="ba5d6-862">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-862">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="ba5d6-863">Storage</span><span class="sxs-lookup"><span data-stu-id="ba5d6-863">Storage</span></span>

* <span data-ttu-id="ba5d6-864">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-864">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="ba5d6-865">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-865">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="ba5d6-866">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-866">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="ba5d6-867">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-867">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="ba5d6-868">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-868">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="ba5d6-869">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-869">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-870">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-870">VM</span></span>

* <span data-ttu-id="ba5d6-871">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-871">Support configuring nsg</span></span>
* <span data-ttu-id="ba5d6-872">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-872">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="ba5d6-873">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="ba5d6-873">Support managed service identities</span></span>
* <span data-ttu-id="ba5d6-874">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-874">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="ba5d6-875">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-875">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="ba5d6-876">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-876">May 10, 2017</span></span>

<span data-ttu-id="ba5d6-877">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="ba5d6-877">Version 2.0.6</span></span>

* <span data-ttu-id="ba5d6-878">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-878">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="ba5d6-879">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-879">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="ba5d6-880">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-880">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="ba5d6-881">Cognitive Services モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-881">Include Cognitive Services module.</span></span>
* <span data-ttu-id="ba5d6-882">Service Fabric モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-882">Include Service Fabric module.</span></span>
* <span data-ttu-id="ba5d6-883">対話型モジュールが追加されました (az-shell の名前変更)。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-883">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="ba5d6-884">CDN コマンドに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-884">Add support for CDN commands.</span></span>
* <span data-ttu-id="ba5d6-885">コンテナー モジュールが削除されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-885">Remove Container module.</span></span>
* <span data-ttu-id="ba5d6-886">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-886">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="ba5d6-887">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-887">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

```
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

### <a name="core"></a><span data-ttu-id="ba5d6-888">コア</span><span class="sxs-lookup"><span data-stu-id="ba5d6-888">Core</span></span>

* <span data-ttu-id="ba5d6-889">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="ba5d6-889">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="ba5d6-890">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-890">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="ba5d6-891">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-891">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="ba5d6-892">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-892">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="ba5d6-893">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-893">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="ba5d6-894">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-894">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="ba5d6-895">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-895">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="ba5d6-896">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-896">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="ba5d6-897">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-897">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="ba5d6-898">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="ba5d6-898">core: Improved performance</span></span>
* <span data-ttu-id="ba5d6-899">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="ba5d6-899">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="ba5d6-900">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="ba5d6-900">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-901">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-901">ACS</span></span>

* <span data-ttu-id="ba5d6-902">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-902">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="ba5d6-903">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-903">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="ba5d6-904">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-904">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="ba5d6-905">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-905">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-906">AppService</span><span class="sxs-lookup"><span data-stu-id="ba5d6-906">AppService</span></span>

* <span data-ttu-id="ba5d6-907">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-907">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="ba5d6-908">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-908">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="ba5d6-909">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-909">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="ba5d6-910">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-910">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="ba5d6-911">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-911">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="ba5d6-912">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-912">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="ba5d6-913">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="ba5d6-913">support slot swap with preview</span></span>
* <span data-ttu-id="ba5d6-914">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-914">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="ba5d6-915">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-915">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ba5d6-916">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ba5d6-916">CosmosDB</span></span>

* <span data-ttu-id="ba5d6-917">documentdb モジュールから cosmosdb に名前が変更されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-917">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="ba5d6-918">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-918">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="ba5d6-919">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-919">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="ba5d6-920">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-920">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="ba5d6-921">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="ba5d6-921">Data Lake Analytics</span></span>

* <span data-ttu-id="ba5d6-922">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-922">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="ba5d6-923">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-923">Add support for new catalog item type: package.</span></span> <span data-ttu-id="ba5d6-924">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="ba5d6-924">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="ba5d6-925">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-925">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="ba5d6-926">テーブル</span><span class="sxs-lookup"><span data-stu-id="ba5d6-926">Table</span></span>
  * <span data-ttu-id="ba5d6-927">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="ba5d6-927">Table valued function</span></span>
  * <span data-ttu-id="ba5d6-928">表示</span><span class="sxs-lookup"><span data-stu-id="ba5d6-928">View</span></span>
  * <span data-ttu-id="ba5d6-929">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-929">Table Statistics.</span></span> <span data-ttu-id="ba5d6-930">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-930">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="ba5d6-931">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ba5d6-931">Data Lake Store</span></span>

* <span data-ttu-id="ba5d6-932">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-932">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="ba5d6-933">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-933">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="ba5d6-934">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="ba5d6-934">missed help for access show.</span></span> <span data-ttu-id="ba5d6-935">追加しました </span><span class="sxs-lookup"><span data-stu-id="ba5d6-935">adding it.</span></span> <span data-ttu-id="ba5d6-936">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-936">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="ba5d6-937">検索</span><span class="sxs-lookup"><span data-stu-id="ba5d6-937">Find</span></span>

* <span data-ttu-id="ba5d6-938">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-938">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="ba5d6-939">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba5d6-939">KeyVault</span></span>

* <span data-ttu-id="ba5d6-940">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-940">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="ba5d6-941">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-941">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="ba5d6-942">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的に上書きされます</span><span class="sxs-lookup"><span data-stu-id="ba5d6-942">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="ba5d6-943">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-943">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="ba5d6-944">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-944">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="ba5d6-945">ラボ</span><span class="sxs-lookup"><span data-stu-id="ba5d6-945">Lab</span></span>

* <span data-ttu-id="ba5d6-946">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-946">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="ba5d6-947">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-947">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="ba5d6-948">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-948">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="ba5d6-949">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-949">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="ba5d6-950">ラボ内でシークレットを管理するためのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-950">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="ba5d6-951">監視</span><span class="sxs-lookup"><span data-stu-id="ba5d6-951">Monitor</span></span>

* <span data-ttu-id="ba5d6-952">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-952">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="ba5d6-953">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-953">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="ba5d6-954">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-954">Network</span></span>

* <span data-ttu-id="ba5d6-955">`network watcher test-connectivity` コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-955">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="ba5d6-956">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-956">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="ba5d6-957">Application Gateway 接続のドレインに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-957">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="ba5d6-958">Application Gateway WAF 規則セットの構成に対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-958">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="ba5d6-959">ExpressRoute ルート フィルターとルールに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-959">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="ba5d6-960">TrafficManager の地理的なルーティングに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-960">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="ba5d6-961">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-961">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="ba5d6-962">VPN 接続 IPSec ポリシーに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-962">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="ba5d6-963">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-963">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="ba5d6-964">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-964">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="ba5d6-965">`network vpn-connection list/show` コマンドの出力から null 値が削除されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-965">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="ba5d6-966">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-966">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="ba5d6-967">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-967">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="ba5d6-968">`dns zone import` でレコードが適切にインポートされないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-968">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="ba5d6-969">`traffic-manager endpoint update` が動作しないバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-969">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="ba5d6-970">"Network Watcher" プレビューのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-970">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="ba5d6-971">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ba5d6-971">Profile</span></span>

* <span data-ttu-id="ba5d6-972">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-972">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="ba5d6-973">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-973">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="ba5d6-974">Redis</span><span class="sxs-lookup"><span data-stu-id="ba5d6-974">Redis</span></span>

* <span data-ttu-id="ba5d6-975">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-975">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="ba5d6-976">"update-settings" コマンドが廃止されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-976">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="ba5d6-977">リソース</span><span class="sxs-lookup"><span data-stu-id="ba5d6-977">Resource</span></span>

* <span data-ttu-id="ba5d6-978">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-978">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="ba5d6-979">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-979">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="ba5d6-980">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-980">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="ba5d6-981">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="ba5d6-981">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="ba5d6-982">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-982">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="ba5d6-983">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="ba5d6-983">Add docs for az lock update.</span></span> <span data-ttu-id="ba5d6-984">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-984">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="ba5d6-985">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="ba5d6-985">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="ba5d6-986">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-986">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="ba5d6-987">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-987">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="ba5d6-988">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-988">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="ba5d6-989">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-989">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="ba5d6-990">役割</span><span class="sxs-lookup"><span data-stu-id="ba5d6-990">Role</span></span>

* <span data-ttu-id="ba5d6-991">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-991">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="ba5d6-992">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-992">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="ba5d6-993">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-993">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="ba5d6-994">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="ba5d6-994">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="ba5d6-995">SQL</span><span class="sxs-lookup"><span data-stu-id="ba5d6-995">SQL</span></span>

* <span data-ttu-id="ba5d6-996">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-996">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="ba5d6-997">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-997">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="ba5d6-998">Storage</span><span class="sxs-lookup"><span data-stu-id="ba5d6-998">Storage</span></span>

* <span data-ttu-id="ba5d6-999">`storage account create` のリソース グループの場所に対する既定の場所。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-999">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="ba5d6-1000">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1000">Add support for incremental blob copy</span></span>
* <span data-ttu-id="ba5d6-1001">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1001">Add support for large block blob upload</span></span>
* <span data-ttu-id="ba5d6-1002">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1002">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-1003">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1003">VM</span></span>

* <span data-ttu-id="ba5d6-1004">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1004">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="ba5d6-1005">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1005">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="ba5d6-1006">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1006">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="ba5d6-1007">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1007">az vm/vmss disk</span></span>
  3. <span data-ttu-id="ba5d6-1008">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1008">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="ba5d6-1009">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1009">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="ba5d6-1010">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1010">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="ba5d6-1011">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1011">April 3, 2017</span></span>

<span data-ttu-id="ba5d6-1012">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1012">Version 2.0.2</span></span>

<span data-ttu-id="ba5d6-1013">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1013">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

```
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

### <a name="core"></a><span data-ttu-id="ba5d6-1014">コア</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1014">Core</span></span>

* <span data-ttu-id="ba5d6-1015">既定の一覧に acr、lab、monitor、find モジュールを追加。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1015">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="ba5d6-1016">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1016">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="ba5d6-1017">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1017">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="ba5d6-1018">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1018">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="ba5d6-1019">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1019">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="ba5d6-1020">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="ba5d6-1020">Add prompting for missing template parameters.</span></span> <span data-ttu-id="ba5d6-1021">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1021">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="ba5d6-1022">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1022">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="ba5d6-1023">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1023">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="ba5d6-1024">ACS</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1024">ACS</span></span>

* <span data-ttu-id="ba5d6-1025">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1025">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="ba5d6-1026">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="ba5d6-1026">Add support for ssh key password prompting.</span></span> <span data-ttu-id="ba5d6-1027">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1027">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="ba5d6-1028">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="ba5d6-1028">Add support for windows clusters.</span></span> <span data-ttu-id="ba5d6-1029">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1029">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="ba5d6-1030">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="ba5d6-1030">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="ba5d6-1031">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1031">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="ba5d6-1032">AppService</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1032">AppService</span></span>

* <span data-ttu-id="ba5d6-1033">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1033">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="ba5d6-1034">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1034">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="ba5d6-1035">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1035">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="ba5d6-1036">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1036">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="ba5d6-1037">DataLake</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1037">DataLake</span></span>

* <span data-ttu-id="ba5d6-1038">Data Lake Analytics モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1038">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="ba5d6-1039">Data Lake Store モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1039">Initial release of Data Lake Store module.</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="ba5d6-1040">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1040">DocuemntDB</span></span>

* <span data-ttu-id="ba5d6-1041">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1041">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="ba5d6-1042">VM</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1042">VM</span></span>

* <span data-ttu-id="ba5d6-1043">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1043">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="ba5d6-1044">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1044">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="ba5d6-1045">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1045">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="ba5d6-1046">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1046">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="ba5d6-1047">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1047">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="ba5d6-1048">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1048">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="ba5d6-1049">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1049">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="ba5d6-1050">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1050">February 27, 2017</span></span>

<span data-ttu-id="ba5d6-1051">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1051">Version 2.0.0</span></span>

<span data-ttu-id="ba5d6-1052">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1052">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="ba5d6-1053">一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1053">General availability applies to these command modules:</span></span>
- <span data-ttu-id="ba5d6-1054">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1054">Container Service (acs)</span></span>
- <span data-ttu-id="ba5d6-1055">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1055">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="ba5d6-1056">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1056">Networking</span></span>
- <span data-ttu-id="ba5d6-1057">Storage</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1057">Storage</span></span>

<span data-ttu-id="ba5d6-1058">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1058">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="ba5d6-1059">問題は、Microsoft サポートで直接開くことも、[github の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1059">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="ba5d6-1060">[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1060">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="ba5d6-1061">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1061">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="ba5d6-1062">CLI のバージョンを確認するには、`az --version` を使用します。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1062">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="ba5d6-1063">出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1063">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

```
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
> <span data-ttu-id="ba5d6-1064">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1064">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="ba5d6-1065">これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1065">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="ba5d6-1066">CLI のナイトリー プレビュー ビルドもあります。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1066">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="ba5d6-1067">詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1067">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="ba5d6-1068">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1068">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="ba5d6-1069">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1069">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="ba5d6-1070">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1070">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="ba5d6-1071">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る。</span><span class="sxs-lookup"><span data-stu-id="ba5d6-1071">Provide feedback from the command line with the `az feedback` command.</span></span>

