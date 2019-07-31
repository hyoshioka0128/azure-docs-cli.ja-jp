---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 07/30/2019
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 673014c3fd86e20148fe5ffa9fa5160e490da0cb
ms.sourcegitcommit: d29d86d33916d5551b4aeb984b06d7a85c4f6b06
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/30/2019
ms.locfileid: "68658933"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="f6344-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="f6344-103">Azure CLI release notes</span></span>

## <a name="july-30-2019"></a><span data-ttu-id="f6344-104">2019 年 7 月 30 日</span><span class="sxs-lookup"><span data-stu-id="f6344-104">July 30, 2019</span></span>

<span data-ttu-id="f6344-105">バージョン 2.0.70</span><span class="sxs-lookup"><span data-stu-id="f6344-105">Version 2.0.70</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-106">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-106">ACR</span></span>

* <span data-ttu-id="f6344-107">問題 #9952 (`acr pack build` コマンドでの回帰) を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-107">Fixed issue #9952 (a regression in the `acr pack build` command)</span></span>
* <span data-ttu-id="f6344-108">`acr pack build` の既定のビルダー イメージ名を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-108">Removed the default builder image name in `acr pack build`</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-109">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-109">Appservice</span></span>

* <span data-ttu-id="f6344-110">リソースが見つからない場合にメッセージ表示するように `webapp config ssl` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-110">Changed `webapp config ssl` to show a message if a resource is not found</span></span>
* <span data-ttu-id="f6344-111">`functionapp create` がストレージ アカウントの種類 `Standard_RAGRS` を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-111">Fixed issue where `functionapp create` does not accept `Standard_RAGRS` storage account type</span></span>
* <span data-ttu-id="f6344-112">古いバージョンの python を使用して `webapp up` を実行すると失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-112">Fixed an issue where `webapp up` would fail if run using older versions of python</span></span>

### <a name="network"></a><span data-ttu-id="f6344-113">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-113">Network</span></span>

* <span data-ttu-id="f6344-114">`network nic ip-config add` から無効なパラメーター `--ids` を削除しました (#9861 の修正)</span><span class="sxs-lookup"><span data-stu-id="f6344-114">Removed invalid parameter `--ids` from `network nic ip-config add` (fixes #9861)</span></span>
* <span data-ttu-id="f6344-115">#9604 を修正しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-115">Fixes #9604.</span></span> <span data-ttu-id="f6344-116">信頼されたルート証明書へのユーザーの関連付けをサポートするために、`network application-gateway http-settings [create|update]` に `--root-certs` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-116">Added `--root-certs` parameter to `network application-gateway http-settings [create|update]` to support user associate trusted root certificates.</span></span>
* <span data-ttu-id="f6344-117">`network dns record-set ns create` の引数 `--subscription` を修正しました (#9965)</span><span class="sxs-lookup"><span data-stu-id="f6344-117">Fixed arguent `--subscription` for `network dns record-set ns create` (#9965)</span></span>

### <a name="rbac"></a><span data-ttu-id="f6344-118">RBAC</span><span class="sxs-lookup"><span data-stu-id="f6344-118">RBAC</span></span>

* <span data-ttu-id="f6344-119">`user update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-119">Added `user update` command</span></span>
* <span data-ttu-id="f6344-120">[非推奨] ユーザー関連コマンドで `--upn-or-object-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-120">[DEPRECATED] Deprecated `--upn-or-object-id` from user-related commands</span></span>
    * <span data-ttu-id="f6344-121">代替引数の `--id` を使用してください</span><span class="sxs-lookup"><span data-stu-id="f6344-121">Use replacement argument `--id`</span></span>
* <span data-ttu-id="f6344-122">ユーザー関連コマンドに `--id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-122">Added `--id` argument to user-related commands</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-123">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-123">SQL</span></span>

* <span data-ttu-id="f6344-124">マネージド インスタンス キーおよび TDE 保護機能の管理コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-124">Added management commands for managed instance keys and TDE protector</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-125">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-125">Storage</span></span>

* <span data-ttu-id="f6344-126">`storage remove` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-126">Added `storage remove` command</span></span>
* <span data-ttu-id="f6344-127">`storage blob update` での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-127">Fixed an issue with `storage blob update`</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-128">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-128">VM</span></span>

* <span data-ttu-id="f6344-129">ゾーンの詳細を出力するための新しい API バージョンを使用するように `list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-129">Changed `list-skus` to use newer api-version to output zone details</span></span>
* <span data-ttu-id="f6344-130">`vmss create` の `--single-placement-group` の既定値を`false` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-130">Changed default of `--single-placement-group` to `false` for `vmss create`</span></span>
* <span data-ttu-id="f6344-131">`[snapshot|disk] create` において ZRS ストレージ SKU を選択する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-131">Added ability to select ZRS storage SKUs for `[snapshot|disk] create`</span></span>
* <span data-ttu-id="f6344-132">専用ホストをサポートするために、新しいコマンド グループ `vm host` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-132">Added new command group `vm host` to support dedicated hosts</span></span>
* <span data-ttu-id="f6344-133">VM 専用ホストを設定するためのパラメーター `--host` と `--host-group` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-133">Added parameters `--host` and `--host-group` on `vm create` to set VM dedicated host</span></span>

## <a name="july-16-2019"></a><span data-ttu-id="f6344-134">2019 年 7 月 16 日</span><span class="sxs-lookup"><span data-stu-id="f6344-134">July 16, 2019</span></span>

<span data-ttu-id="f6344-135">バージョン 2.0.69</span><span class="sxs-lookup"><span data-stu-id="f6344-135">Version 2.0.69</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-136">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-136">Appservice</span></span>

* <span data-ttu-id="f6344-137">ResourceGroupName または App の名前が無効な場合に適切なエラー メッセージを返すように `webapp identity` コマンドが変更されました</span><span class="sxs-lookup"><span data-stu-id="f6344-137">Changed `webapp identity` commands to return a proper error message if ResourceGroupName or App name are invalid</span></span>
* <span data-ttu-id="f6344-138">ResourceGroup が指定されなかった場合に numberOfSites の正しい値を返すように `webapp list` が修正されました</span><span class="sxs-lookup"><span data-stu-id="f6344-138">Fixed `webapp list` to return the correct value for numberOfSites if no ResourceGroup was provided</span></span>
* <span data-ttu-id="f6344-139">`appservice plan create` と `webapp create` の副作用が修正されました</span><span class="sxs-lookup"><span data-stu-id="f6344-139">Fixed side-effects of `appservice plan create` and `webapp create`</span></span>

### <a name="core"></a><span data-ttu-id="f6344-140">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-140">Core</span></span>

* <span data-ttu-id="f6344-141">`--subscription` が適用不可にもかかわらず表示される問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="f6344-141">Fixed issue where `--subscription` would appear despite being not applicable</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-142">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-142">Batch</span></span>

* <span data-ttu-id="f6344-143">[重大な変更] `batch pool node-agent-skus list` が `batch pool supported-images list` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="f6344-143">[BREAKING CHANGE] Replaced `batch pool node-agent-skus list` with `batch pool supported-images list`</span></span>
* <span data-ttu-id="f6344-144">`batch pool create network` の `--json-file` オプションを使用するときに、トラフィックのソース ポートに基づいてプールへのネットワーク アクセスをブロックするセキュリティ規則のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-144">Added support for security rules blocking network access to a pool based on the source port of the traffic when using the `--json-file` option of `batch pool create network`</span></span>
* <span data-ttu-id="f6344-145">`batch task create`の `--json-file` オプションを使用するときに、コンテナーの作業ディレクトリまたは Batch タスクの作業ディレクトリでタスクを実行するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-145">Added support for executing the task in the container working directory or in the Batch task working directory when using the `--json-file` option of `batch task create`</span></span>
* <span data-ttu-id="f6344-146">`batch pool create`の `--application-package-references` オプションが、既定値でのみ動作するというエラーが修正されました</span><span class="sxs-lookup"><span data-stu-id="f6344-146">Fixed error in `--application-package-references` option of `batch pool create` where it would only work with defaults</span></span>

### <a name="eventhubs"></a><span data-ttu-id="f6344-147">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="f6344-147">Eventhubs</span></span>

* <span data-ttu-id="f6344-148">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-148">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="rdbms"></a><span data-ttu-id="f6344-149">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f6344-149">RDBMS</span></span>

* <span data-ttu-id="f6344-150">レプリカ作成コマンドでレプリカ SKU を指定するためのオプション パラメーターが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-150">Added optional parameter to specify replica SKU for create replica command</span></span>
* <span data-ttu-id="f6344-151">MySQL レプリカの作成で CI テストが失敗する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="f6344-151">Fixed the issue with CI test failure with creating MySQL replica</span></span>

### <a name="relay"></a><span data-ttu-id="f6344-152">リレー</span><span class="sxs-lookup"><span data-stu-id="f6344-152">Relay</span></span>

* <span data-ttu-id="f6344-153">クライアント承認が無効になっているときのハイブリッド接続の問題が修正されました ([#8775](https://github.com/azure/azure-cli/issues/8775))</span><span class="sxs-lookup"><span data-stu-id="f6344-153">Fixed issue with hybrid connection when client authroization disabled [#8775](https://github.com/azure/azure-cli/issues/8775)</span></span>
* <span data-ttu-id="f6344-154">パラメーター `--requires-transport-security` を `relay wcfrelay create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-154">Added parameter `--requires-transport-security` to `relay wcfrelay create`</span></span>

### <a name="servicebus"></a><span data-ttu-id="f6344-155">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f6344-155">Servicebus</span></span>

* <span data-ttu-id="f6344-156">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-156">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-157">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-157">Storage</span></span>

* <span data-ttu-id="f6344-158">ストレージ アカウントの更新で Files AADDS を有効にします</span><span class="sxs-lookup"><span data-stu-id="f6344-158">Enable Files AADDS for storage account update</span></span>
* <span data-ttu-id="f6344-159">修正された問題 `storage blob service-properties update --set`</span><span class="sxs-lookup"><span data-stu-id="f6344-159">Fixed issue `storage blob service-properties update --set`</span></span>

## <a name="july-2-2019"></a><span data-ttu-id="f6344-160">2019 年 7 月 2 日</span><span class="sxs-lookup"><span data-stu-id="f6344-160">July 2, 2019</span></span>

<span data-ttu-id="f6344-161">バージョン 2.0.68</span><span class="sxs-lookup"><span data-stu-id="f6344-161">Version 2.0.68</span></span>

### <a name="core"></a><span data-ttu-id="f6344-162">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-162">Core</span></span>

* <span data-ttu-id="f6344-163">コマンド モジュールが再頒布可能な 1 つの Python コードに統合されました。</span><span class="sxs-lookup"><span data-stu-id="f6344-163">Command modules are now consolidated into a single Python distributable.</span></span> <span data-ttu-id="f6344-164">これにより、PyPI での多くの `azure-cli-` パッケージの直接使用が廃止されます。</span><span class="sxs-lookup"><span data-stu-id="f6344-164">This deprecates direct use of many `azure-cli-` packages on PyPI.</span></span>
  <span data-ttu-id="f6344-165">またこれにより、インストール サイズが削減され、`pip` 経由で直接インストールしたユーザーにのみ影響が出ます。</span><span class="sxs-lookup"><span data-stu-id="f6344-165">This should reduce install size and only affect users who have directly installed via `pip`.</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-166">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-166">ACR</span></span>

* <span data-ttu-id="f6344-167">タスクへのタイマー トリガーのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-167">Added support for Timer Triggers to Task</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-168">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-168">Appservice</span></span>

* <span data-ttu-id="f6344-169">既定でアプリケーション インサイトを有効にするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-169">Changed `functionapp create` to enable application insights by default</span></span>
* <span data-ttu-id="f6344-170">[重大な変更] 非推奨の `functionapp devops-build` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-170">[BREAKING CHANGE] Removed deprecated `functionapp devops-build` command.</span></span>
  *  <span data-ttu-id="f6344-171">代わりに新しいコマンド `az functionapp devops-pipeline` を使用</span><span class="sxs-lookup"><span data-stu-id="f6344-171">Use the new command `az functionapp devops-pipeline` instead</span></span>
* <span data-ttu-id="f6344-172">Linux 従量課金プランの関数アプリのプラン サポートを `functionapp deployment config-zip` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-172">Added Linux Consumption function app plan support to `functionapp deployment config-zip`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="f6344-173">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f6344-173">Cosmos DB</span></span>

* <span data-ttu-id="f6344-174">ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-174">Added support for disabling TTL</span></span>

### <a name="dls"></a><span data-ttu-id="f6344-175">DLS</span><span class="sxs-lookup"><span data-stu-id="f6344-175">DLS</span></span>

* <span data-ttu-id="f6344-176">ADLS バージョンを更新しました (0.0.45)</span><span class="sxs-lookup"><span data-stu-id="f6344-176">Updated ADLS version (0.0.45)</span></span>

### <a name="feedback"></a><span data-ttu-id="f6344-177">フィードバック</span><span class="sxs-lookup"><span data-stu-id="f6344-177">Feedback</span></span>

* <span data-ttu-id="f6344-178">失敗した拡張機能コマンドを報告するときに、`az feedback` はインデックスからの拡張機能のプロジェクト/リポジトリの url にブラウザーを開こうとするようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-178">When reporting a failed extension command, `az feedback` now attempts to open the browser to the project/repo url of the extension from the index</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f6344-179">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f6344-179">HDInsight</span></span>

* <span data-ttu-id="f6344-180">[重大な変更] `oms` コマンド グループ名を `monitor` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-180">[BREAKING CHANGE] Changed `oms` command group name to `monitor`</span></span>
* <span data-ttu-id="f6344-181">[重大な変更] `--http-password/-p` が必須パラメーターになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-181">[BREAKING CHANGE] Made `--http-password/-p` a required parameter</span></span> 
* <span data-ttu-id="f6344-182">`--cluster-admin-account` および `cluster-users-group-dns` パラメーター入力候補の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-182">Added completers for `--cluster-admin-account` and `cluster-users-group-dns` parameters completer</span></span> 
* <span data-ttu-id="f6344-183">`cluster-users-group-dns` パラメーターを `—esp` が存在するときに必要となるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-183">Changed `cluster-users-group-dns` parameter to be required when `—esp` is present</span></span>
* <span data-ttu-id="f6344-184">既存の引数自動オートコンプリートすべてにタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-184">Added a timeout for all existing argument auto-completers</span></span>
* <span data-ttu-id="f6344-185">リソース名をリソース id に変換する際のタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-185">Added a timeout for transforming resource name to resource id</span></span>
* <span data-ttu-id="f6344-186">任意のリソース グループからリソースを選択するようにオートコンプリートを変更しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-186">Changed Auto-completers to select resources from any resource group.</span></span> <span data-ttu-id="f6344-187">`-g` で指定されるリソース グループとは別のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f6344-187">It can be a different resource group than the one specified with `-g`</span></span>
* <span data-ttu-id="f6344-188">`hdinsight application create` コマンドで `--sub-domain-suffix` および `--disable_gateway_auth` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-188">Added support for `--sub-domain-suffix` and `--disable_gateway_auth` parameters in the `hdinsight application create` command</span></span>

### <a name="managed-services"></a><span data-ttu-id="f6344-189">マネージド サービス</span><span class="sxs-lookup"><span data-stu-id="f6344-189">Managed Services</span></span>

* <span data-ttu-id="f6344-190">プレビューにマネージド サービス コマンド モジュールを導入</span><span class="sxs-lookup"><span data-stu-id="f6344-190">Introducing managed service command module in preview</span></span>

### <a name="profile"></a><span data-ttu-id="f6344-191">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-191">Profile</span></span>
* <span data-ttu-id="f6344-192">ログアウト コマンドの `--subscription` 引数を抑制</span><span class="sxs-lookup"><span data-stu-id="f6344-192">Suppress `--subscription` argument for logout command</span></span>

### <a name="rbac"></a><span data-ttu-id="f6344-193">RBAC</span><span class="sxs-lookup"><span data-stu-id="f6344-193">RBAC</span></span>

* <span data-ttu-id="f6344-194">[重大な変更] `create-for-rbac` の `--password` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-194">[BREAKING CHANGE] Removed `--password` argument for `create-for-rbac`</span></span>
* <span data-ttu-id="f6344-195">AAD グラフ サーバー レプリケーションの待機時間によって発生する断続的なエラーを回避するために `--assignee-principal-type` パラメーターを `create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-195">Added `--assignee-principal-type` parameter to `create` command to avoid intermittent failures caused by AAD graph server replication latency</span></span>
* <span data-ttu-id="f6344-196">所有オブジェクトの一覧表示時の `ad signed-in-user` のクラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-196">Fixed a crash in `ad signed-in-user` when listing owned objects</span></span>
* <span data-ttu-id="f6344-197">`ad sp` によってサービス プリンシパルから適切なアプリケーションが検出されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-197">Fixed issue where `ad sp` would not find the right application from a service principal</span></span>

### <a name="rdbms"></a><span data-ttu-id="f6344-198">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f6344-198">RDBMS</span></span>

* <span data-ttu-id="f6344-199">MariaDB のレプリケーション サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-199">Added support for replication for MariaDB</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-200">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-200">SQL</span></span>

* <span data-ttu-id="f6344-201">`sql db create --sample-name` に使用できる値を文書化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-201">Documented allowed values for `sql db create --sample-name`</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-202">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-202">Storage</span></span>

* <span data-ttu-id="f6344-203">`--as-user` を使用した `storage blob generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-203">Added user delegation SAS token support with `--as-user` to `storage blob generate-sas`</span></span> 
* <span data-ttu-id="f6344-204">`--as-user` を使用した `storage container generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-204">Added user delegation SAS token support with `--as-user` to `storage container generate-sas`</span></span> 

### <a name="vm"></a><span data-ttu-id="f6344-205">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-205">VM</span></span>

* <span data-ttu-id="f6344-206">`--no-wait` による実行時に `vmss create` によってエラー メッセージが返されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-206">Fixed bug where `vmss create` returns an error message when run with `--no-wait`</span></span>
* <span data-ttu-id="f6344-207">`vmss create --single-placement-group` のクライアント側の検証を削除しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-207">Removed client-side validation for `vmss create --single-placement-group`.</span></span> <span data-ttu-id="f6344-208">`--single-placement-group` が `true` に設定され、`--instance-count` が 100 より大きいか、可用性ゾーンが指定されていても失敗にはならず、この検証はコンピューティング サービスに任されます</span><span class="sxs-lookup"><span data-stu-id="f6344-208">Does not fail if `--single-placement-group` is set to `true` and`--instance-count` is greater than 100 or availability zones are specified, but leaves this validation to the compute service</span></span>
* <span data-ttu-id="f6344-209">`--latest` と共に使用したときに `[vm|vmss] extension image list` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-209">Fixed bug where `[vm|vmss] extension image list` fails when used with `--latest`</span></span>


## <a name="june-18-2019"></a><span data-ttu-id="f6344-210">2019 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="f6344-210">June 18, 2019</span></span>

<span data-ttu-id="f6344-211">バージョン 2.0.67</span><span class="sxs-lookup"><span data-stu-id="f6344-211">Version 2.0.67</span></span>

### <a name="core"></a><span data-ttu-id="f6344-212">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-212">Core</span></span>

<span data-ttu-id="f6344-213">このリリースでは、新しい [プレビュー] タグが導入され、コマンド グループ、コマンド、または引数がプレビュー状態である場合に、お客様により明確に通知できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f6344-213">This release introduces a new [Preview] tag to more clearly communicate to customers when a command group, command or argument is in preview status.</span></span> <span data-ttu-id="f6344-214">以前は、これはヘルプ テキストで通知されていたか、コマンド モジュールのバージョン番号によって暗黙的に通知されていました。</span><span class="sxs-lookup"><span data-stu-id="f6344-214">This was previously called out in help text or communicated implicitly by the command module version number.</span></span>
<span data-ttu-id="f6344-215">CLI では、将来、個々のパッケージのバージョン番号が削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="f6344-215">The CLI will be removing version numbers for individual packages in the future.</span></span> <span data-ttu-id="f6344-216">コマンドがプレビュー状態の場合は、そのすべての引数もプレビュー状態です。</span><span class="sxs-lookup"><span data-stu-id="f6344-216">If a command is in preview, all of its arguments are as well.</span></span> <span data-ttu-id="f6344-217">コマンド グループにプレビュー状態のラベルが付いている場合、すべてのコマンドと引数もプレビュー状態と見なされます。</span><span class="sxs-lookup"><span data-stu-id="f6344-217">If a command group is labeled as being in preview, then all commands and arguments are considered to be in preview as well.</span></span>

<span data-ttu-id="f6344-218">この変更の結果、このリリースでは、一部のコマンド グループが "突然" プレビュー状態になったように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="f6344-218">As a result of this change, several command groups may seem to "suddenly" appear to be in a preview status with this release.</span></span> <span data-ttu-id="f6344-219">ほとんどのパッケージがプレビュー状態にあったのですが、このリリースでは一般提供と見なされていることがその真相です</span><span class="sxs-lookup"><span data-stu-id="f6344-219">What actually happened is that most packages were in a preview status, but are being deemed GA with this release</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-220">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-220">ACR</span></span>
* <span data-ttu-id="f6344-221">'acr check-health' コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-221">Added 'acr check-health' command</span></span>
* <span data-ttu-id="f6344-222">AAD トークンおよび外部コマンドの取得に関するエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-222">Improved error handling for AAD tokens and for retrieving external commands</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-223">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-223">ACS</span></span>
* <span data-ttu-id="f6344-224">非推奨の ACS コマンドがヘルプ ビューで非表示になりました</span><span class="sxs-lookup"><span data-stu-id="f6344-224">Deprecated ACS commands are now hidden from help view</span></span>

### <a name="ams"></a><span data-ttu-id="f6344-225">AMS</span><span class="sxs-lookup"><span data-stu-id="f6344-225">AMS</span></span>
* <span data-ttu-id="f6344-226">[重大な変更] archive-window-length および key-frame-interval-duration の ISO 8601 時間文字列を返すように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-226">[BREAKING CHANGE] Changed to return ISO 8601 time strings for archive-window-length and key-frame-interval-duration</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-227">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-227">AppService</span></span>
* <span data-ttu-id="f6344-228">`webapp deleted list` および `webapp deleted restore` に対してロケーション ベースのルーティングを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-228">Added location based routing for `webapp deleted list` and `webapp deleted restore`</span></span>
* <span data-ttu-id="f6344-229">Azure Cloud Shell で Web アプリのログに記録されたターゲット URL ("You can launch the app at...") がクリックできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-229">Fixed issue where webapp up logged target URL ("You can launch the app at...") was not clickable in Azure Cloud Shell</span></span>
* <span data-ttu-id="f6344-230">一部の SKU でのアプリ作成が AlwaysOn エラーで失敗するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-230">Fixed an issue where creating apps with the some SKUs was failing with an AlwaysOn error</span></span>
* <span data-ttu-id="f6344-231">`[appservice|webapp] create` に事前検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-231">Added pre-validation to `[appservice|webapp] create`</span></span>
* <span data-ttu-id="f6344-232">正しい actionHostName を使用するように `[webapp|functionapp] traffic-routing` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-232">Fixed `[webapp|functionapp] traffic-routing` to use the correct actionHostName</span></span>
* <span data-ttu-id="f6344-233">`functionapp` コマンドにスロット サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-233">Added slot support to `functionapp` commands</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-234">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-234">Batch</span></span>
* <span data-ttu-id="f6344-235">共有キー認証の過度のエラー報告による AAD 認証の回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-235">Fixed AAD auth regression caused by over-aggressive error reporting for Shared Key Auth</span></span>

### <a name="batchai"></a><span data-ttu-id="f6344-236">BatchAI</span><span class="sxs-lookup"><span data-stu-id="f6344-236">BatchAI</span></span>
* <span data-ttu-id="f6344-237">BatchAI コマンドが非推奨となり、非表示になりました</span><span class="sxs-lookup"><span data-stu-id="f6344-237">BatchAI commands are now deprecated and hidden</span></span>

### <a name="botservice"></a><span data-ttu-id="f6344-238">BotService</span><span class="sxs-lookup"><span data-stu-id="f6344-238">BotService</span></span>
* <span data-ttu-id="f6344-239">v3 SDK をサポートするコマンドに "廃止されたサポート"/"保守モード" 警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-239">Added "discontinued support"/"maintenance mode" warning messages for commands that support the v3 SDK</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f6344-240">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f6344-240">CosmosDB</span></span>
* <span data-ttu-id="f6344-241">[非推奨] `cosmosdb list-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-241">[DEPRECATED] Deprecated the `cosmosdb list-keys` command</span></span>
* <span data-ttu-id="f6344-242">`cosmosdb keys list` コマンドを追加しました。`cosmosdb list-keys` に置き換わるものです</span><span class="sxs-lookup"><span data-stu-id="f6344-242">Added the `cosmosdb keys list` command - replaces `cosmosdb list-keys`</span></span>
* <span data-ttu-id="f6344-243">`cosmsodb create/update`:"isZoneRedundant" プロパティを設定できるように --location の新しいフォーマットを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-243">`cosmsodb create/update`: Added new format for --location to allow setting "isZoneRedundant" property.</span></span> <span data-ttu-id="f6344-244">古いフォーマットを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-244">Deprecated old format</span></span>

### <a name="eventgrid"></a><span data-ttu-id="f6344-245">EventGrid</span><span class="sxs-lookup"><span data-stu-id="f6344-245">EventGrid</span></span>
* <span data-ttu-id="f6344-246">ドメイン CRUD 操作のための `eventgrid domain` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-246">Added `eventgrid domain` commands for domain CRUD operations</span></span>
* <span data-ttu-id="f6344-247">ドメイン トピック CRUD 操作のための `eventgrid domain topic` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-247">Added `eventgrid domain topic` commands for domain topics CRUD operations</span></span>
* <span data-ttu-id="f6344-248">OData 構文を使用して結果をフィルタリングするための `--odata-query` 引数を `eventgrid [topic|event-subscription] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-248">Added `--odata-query` argument to `eventgrid [topic|event-subscription] list` for filtering results using OData syntax</span></span>
* <span data-ttu-id="f6344-249">`event-subscription create/update`:`--endpoint-type` パラメーターの新しい値として servicebusqueue を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-249">`event-subscription create/update`: Added servicebusqueue as new values for the `--endpoint-type` parameter</span></span>
* <span data-ttu-id="f6344-250">[重大な変更] `eventgrid event-subscription [create|update]` での `--included-event-types All` のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-250">[BREAKING CHANGE] Removed support for `--included-event-types All` with `eventgrid event-subscription [create|update]`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f6344-251">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f6344-251">HDInsight</span></span>
* <span data-ttu-id="f6344-252">`hdinsight create` コマンドでの `--ssh-public-key` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-252">Added support for `--ssh-public-key` parameter in `hdinsight create` command</span></span>

### <a name="iot"></a><span data-ttu-id="f6344-253">IoT</span><span class="sxs-lookup"><span data-stu-id="f6344-253">IoT</span></span>
* <span data-ttu-id="f6344-254">承認ポリシー キーの再生成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-254">Added support to regenerate authorization policy keys</span></span>
* <span data-ttu-id="f6344-255">DigitalTwin リポジトリ プロビジョニング サービスの SDK およびサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-255">Added SDK and support for DigitalTwin Repository Provisioning Service</span></span>

### <a name="network"></a><span data-ttu-id="f6344-256">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-256">Network</span></span>
* <span data-ttu-id="f6344-257">Nat Gateway に対するゾーン サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-257">Added Zone support for Nat Gateway</span></span>
* <span data-ttu-id="f6344-258">`network list-service-tags` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-258">Added command `network list-service-tags`</span></span>
* <span data-ttu-id="f6344-259">ユーザーがワイルドカード A レコードをインポートできない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-259">Fixed issue with `dns zone import` where users could not import wildcard A records</span></span>
* <span data-ttu-id="f6344-260">特定のリージョンでフロー ロギングを有効にできない `watcher flow-log configure` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-260">Fixed issue with `watcher flow-log configure` where flow logging could not be enabled in certain regions</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-261">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-261">Resource</span></span>
* <span data-ttu-id="f6344-262">REST 呼び出しを行うための `az rest` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-262">Added `az rest` command for making REST calls</span></span>
* <span data-ttu-id="f6344-263">リソース グループまたはサブスクリプション レベル`--scope` で `policy assignment list` を使用する場合のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-263">Fixed error when using `policy assignment list` with a resource group or subscription level `--scope`</span></span>

### <a name="servicebus"></a><span data-ttu-id="f6344-264">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f6344-264">ServiceBus</span></span>
* <span data-ttu-id="f6344-265">`servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319) での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-265">Fixed issue with `servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319)</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-266">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-266">SQL</span></span>
* <span data-ttu-id="f6344-267">`--location` を `sql [server|mi] create` のオプションに変更しました - 指定されていない場合、リソース グループの場所を使用します</span><span class="sxs-lookup"><span data-stu-id="f6344-267">Changed `--location` to be optional for `sql [server|mi] create` - uses resource group location if not specified</span></span>
* <span data-ttu-id="f6344-268">`sql db list-editions --available` の "'NoneType' object is not iterable" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-268">Fixed "'NoneType' object is not iterable" error for `sql db list-editions --available`</span></span>

### <a name="sqlvm"></a><span data-ttu-id="f6344-269">SQLVm</span><span class="sxs-lookup"><span data-stu-id="f6344-269">SQLVm</span></span>
* <span data-ttu-id="f6344-270">[破壊的変更] `--license-type` パラメーターを必要とするように `sql vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-270">[BREAKING CHNAGE] Changed `sql vm create` to require `--license-type` parameter</span></span>
* <span data-ttu-id="f6344-271">sql vm の作成または更新時に SQL イメージ SKU を設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-271">Changed to allow setting SQL image SKU when creating or updating a sql vm</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-272">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-272">Storage</span></span>
* <span data-ttu-id="f6344-273">`storage container generate-sas` のアカウント キーが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-273">Fixed issue with missing account key for `storage container generate-sas`</span></span>
* <span data-ttu-id="f6344-274">Linux での `storage blob sync` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-274">Fixed issue with `storage blob sync` on Linux</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-275">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-275">VM</span></span>
* <span data-ttu-id="f6344-276">[プレビュー] VM イメージを構築するための `vm image template` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-276">[PREVIEW] Added `vm image template` commands to build VM images</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="f6344-277">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="f6344-277">June 4, 2019</span></span>

<span data-ttu-id="f6344-278">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="f6344-278">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="f6344-279">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-279">Core</span></span>
* <span data-ttu-id="f6344-280">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-280">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-281">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-281">ACR</span></span>
* <span data-ttu-id="f6344-282">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-282">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-283">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-283">ACS</span></span>
* <span data-ttu-id="f6344-284">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-284">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="f6344-285">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="f6344-285">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-286">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-286">Batch</span></span>
* <span data-ttu-id="f6344-287">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-287">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="f6344-288">IoT</span><span class="sxs-lookup"><span data-stu-id="f6344-288">IoT</span></span>
* <span data-ttu-id="f6344-289">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-289">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="f6344-290">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-290">Network</span></span>
* <span data-ttu-id="f6344-291">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-291">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="f6344-292">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-292">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="f6344-293">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-293">Resource</span></span>
* <span data-ttu-id="f6344-294">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-294">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="f6344-295">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-295">Role</span></span>
* <span data-ttu-id="f6344-296">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-296">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="f6344-297">Compute</span><span class="sxs-lookup"><span data-stu-id="f6344-297">Compute</span></span>
* <span data-ttu-id="f6344-298">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-298">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="f6344-299">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="f6344-299">May 21, 2019</span></span>

<span data-ttu-id="f6344-300">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="f6344-300">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="f6344-301">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-301">Core</span></span>
* <span data-ttu-id="f6344-302">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-302">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="f6344-303">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-303">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="f6344-304">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-304">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-305">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-305">ACR</span></span>
* <span data-ttu-id="f6344-306">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-306">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-307">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-307">ACS</span></span>
* <span data-ttu-id="f6344-308">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-308">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-309">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-309">AppService</span></span>
* <span data-ttu-id="f6344-310">[非推奨] `functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="f6344-310">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="f6344-311">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-311">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="f6344-312">[重大な変更] `--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="f6344-312">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="f6344-313">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-313">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="f6344-314">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-314">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="f6344-315">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-315">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="f6344-316">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-316">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="f6344-317">BotService</span><span class="sxs-lookup"><span data-stu-id="f6344-317">BotService</span></span>
* <span data-ttu-id="f6344-318">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-318">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="f6344-319">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-319">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="f6344-320">消費</span><span class="sxs-lookup"><span data-stu-id="f6344-320">Consumption</span></span>
* <span data-ttu-id="f6344-321">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-321">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="f6344-322">IoT</span><span class="sxs-lookup"><span data-stu-id="f6344-322">IoT</span></span>
* <span data-ttu-id="f6344-323">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-323">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="f6344-324">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-324">Network</span></span>
* [重大な変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="f6344-326">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-326">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="f6344-327">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-327">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="f6344-328">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f6344-328">RDBMS</span></span>
* <span data-ttu-id="f6344-329">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-329">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="f6344-330">RBAC</span><span class="sxs-lookup"><span data-stu-id="f6344-330">RBAC</span></span>
* <span data-ttu-id="f6344-331">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-331">Added support for mangement group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-332">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-332">Storage</span></span>
* <span data-ttu-id="f6344-333">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="f6344-333">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="f6344-334">Compute</span><span class="sxs-lookup"><span data-stu-id="f6344-334">Compute</span></span>
* <span data-ttu-id="f6344-335">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-335">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="f6344-336">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-336">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="f6344-337">__メモ__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="f6344-337">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="f6344-338">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-338">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="f6344-339">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="f6344-339">May 6, 2019</span></span>

<span data-ttu-id="f6344-340">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="f6344-340">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-341">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-341">ACS</span></span>
* <span data-ttu-id="f6344-342">[重大な変更] `--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-342">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="f6344-343">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-343">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="f6344-344">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-344">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="f6344-345">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-345">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-346">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-346">Appservice</span></span>
* <span data-ttu-id="f6344-347">[非推奨] `functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-347">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="f6344-348">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-348">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="f6344-349">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="f6344-349">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="f6344-350">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-350">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="f6344-351">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-351">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="f6344-352">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-352">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="f6344-353">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-353">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="f6344-354">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-354">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="f6344-355">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-355">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="f6344-356">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-356">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-357">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-357">Batch</span></span>
* <span data-ttu-id="f6344-358">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-358">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="f6344-359">Botservice</span><span class="sxs-lookup"><span data-stu-id="f6344-359">Botservice</span></span>
* <span data-ttu-id="f6344-360">[重大な変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="f6344-360">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="f6344-361">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-361">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="f6344-362">[重大な変更] `--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-362">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="f6344-363">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="f6344-363">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="f6344-364">[重大な変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-364">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="f6344-365">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="f6344-365">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="f6344-366">[重大な変更] `bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-366">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="f6344-367">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-367">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="f6344-368">[重大な変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-368">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="f6344-369">[重大な変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-369">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="f6344-370">[重大な変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-370">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="f6344-371">[重大な変更] `Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-371">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="f6344-372">[重大な変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-372">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="f6344-373">[重大な変更] `SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-373">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="f6344-374">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="f6344-374">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="f6344-375">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-375">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="f6344-376">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-376">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="f6344-377">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-377">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="f6344-378">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-378">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="f6344-379">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-379">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="f6344-380">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-380">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="f6344-381">構成</span><span class="sxs-lookup"><span data-stu-id="f6344-381">Configure</span></span>
* <span data-ttu-id="f6344-382">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-382">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="f6344-383">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="f6344-383">Eventhubs</span></span>
* <span data-ttu-id="f6344-384">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-384">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="f6344-385">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-385">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="f6344-386">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-386">Network</span></span>
* <span data-ttu-id="f6344-387">[重大な変更] `vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="f6344-387">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="f6344-388">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="f6344-388">Policy Insights</span></span>
* <span data-ttu-id="f6344-389">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-389">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="f6344-390">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-390">Role</span></span>
* <span data-ttu-id="f6344-391">[非推奨] `create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="f6344-391">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="f6344-392">Service Bus</span><span class="sxs-lookup"><span data-stu-id="f6344-392">Service Bus</span></span>
* <span data-ttu-id="f6344-393">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-393">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="f6344-394">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-394">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="f6344-395">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-395">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-396">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-396">SQL</span></span>
* <span data-ttu-id="f6344-397">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-397">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-398">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-398">VM</span></span>
* <span data-ttu-id="f6344-399">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-399">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="f6344-400">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-400">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="f6344-401">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-401">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="f6344-402">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-402">Added new `ppg` command group for manging Proximity Placement Groups</span></span>
* <span data-ttu-id="f6344-403">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-403">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="f6344-404">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-404">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="f6344-405">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="f6344-405">April 23, 2019</span></span>

<span data-ttu-id="f6344-406">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="f6344-406">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-407">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-407">ACS</span></span>
* <span data-ttu-id="f6344-408">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-408">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="f6344-409">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-409">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="f6344-410">AMS</span><span class="sxs-lookup"><span data-stu-id="f6344-410">AMS</span></span>
* <span data-ttu-id="f6344-411">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-411">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-412">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-412">AppService</span></span>
* <span data-ttu-id="f6344-413">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-413">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="f6344-414">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-414">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="f6344-415">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-415">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="f6344-416">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-416">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="f6344-417">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-417">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="f6344-418">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-418">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="f6344-419">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-419">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="f6344-420">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-420">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="f6344-421">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-421">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="f6344-422">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="f6344-422">Deployment Manager</span></span>
* <span data-ttu-id="f6344-423">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="f6344-423">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="f6344-424">ラボ</span><span class="sxs-lookup"><span data-stu-id="f6344-424">Lab</span></span>
* <span data-ttu-id="f6344-425">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-425">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="f6344-426">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-426">Network</span></span>
* <span data-ttu-id="f6344-427">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-427">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-428">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-428">Resource</span></span>
* <span data-ttu-id="f6344-429">[非推奨] `resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="f6344-429">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="f6344-430">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="f6344-430">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="f6344-431">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-431">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="f6344-432">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-432">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-433">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-433">SQL</span></span>
* <span data-ttu-id="f6344-434">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-434">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="f6344-435">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-435">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="f6344-436">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-436">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="f6344-437">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-437">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-438">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-438">Storage</span></span>
* <span data-ttu-id="f6344-439">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-439">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-440">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-440">VM</span></span>
* <span data-ttu-id="f6344-441">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-441">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="f6344-442">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-442">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="f6344-443">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-443">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="f6344-444">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="f6344-444">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="f6344-445">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-445">Core</span></span>
* <span data-ttu-id="f6344-446">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-446">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-447">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-447">ACR</span></span>
* <span data-ttu-id="f6344-448">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-448">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="f6344-449">AMS</span><span class="sxs-lookup"><span data-stu-id="f6344-449">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="f6344-452">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-452">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="f6344-453">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-453">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-454">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-454">AppService</span></span>
* <span data-ttu-id="f6344-455">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-455">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="f6344-456">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-456">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="f6344-457">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-457">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="f6344-458">[重大な変更] `devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="f6344-458">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="f6344-459">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-459">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="f6344-460">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-460">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="f6344-461">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-461">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="f6344-462">CDN</span><span class="sxs-lookup"><span data-stu-id="f6344-462">CDN</span></span>
* <span data-ttu-id="f6344-463">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-463">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="f6344-464">フィードバック</span><span class="sxs-lookup"><span data-stu-id="f6344-464">Feedback</span></span>
* <span data-ttu-id="f6344-465">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-465">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="f6344-466">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-466">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="f6344-467">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-467">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-468">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-468">Monitor</span></span>
* <span data-ttu-id="f6344-469">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-469">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="f6344-470">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-470">Network</span></span>
* <span data-ttu-id="f6344-471">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-471">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="f6344-472">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-472">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="f6344-473">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-473">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="f6344-474">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-474">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="f6344-475">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="f6344-475">PrivateDNS</span></span>
* <span data-ttu-id="f6344-476">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-476">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-477">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-477">Resource</span></span>
* <span data-ttu-id="f6344-478">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-478">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="f6344-479">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-479">Role</span></span>
* <span data-ttu-id="f6344-480">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-480">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="f6344-481">[重大な変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-481">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-482">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-482">SQL</span></span>
* <span data-ttu-id="f6344-483">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-483">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-484">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-484">Storage</span></span>
* <span data-ttu-id="f6344-485">[重大な変更] `storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-485">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="f6344-486">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-486">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="f6344-487">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-487">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="f6344-488">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-488">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="f6344-489">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="f6344-489">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="f6344-490">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-490">Core</span></span>
* <span data-ttu-id="f6344-491">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-491">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="f6344-492">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-492">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="f6344-493">クラウド</span><span class="sxs-lookup"><span data-stu-id="f6344-493">Cloud</span></span>
* <span data-ttu-id="f6344-494">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-494">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-495">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-495">ACR</span></span>
* <span data-ttu-id="f6344-496">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-496">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="f6344-497">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-497">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="f6344-498">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-498">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="f6344-499">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-499">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-500">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-500">AppService</span></span>
* <span data-ttu-id="f6344-501">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-501">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="f6344-502">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-502">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="f6344-503">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="f6344-503">BOT Service</span></span>
* <span data-ttu-id="f6344-504">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-504">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="f6344-505">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-505">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="f6344-506">[重大な変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-506">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="f6344-507">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-507">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="f6344-508">CDN</span><span class="sxs-lookup"><span data-stu-id="f6344-508">CDN</span></span>
* <span data-ttu-id="f6344-509">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-509">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [重大な変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="f6344-511">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="f6344-511">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="f6344-512">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-512">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f6344-513">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="f6344-513">Cosmosdb</span></span>
* <span data-ttu-id="f6344-514">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-514">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="f6344-515">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-515">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="f6344-516">Interactive</span><span class="sxs-lookup"><span data-stu-id="f6344-516">Interactive</span></span>
* <span data-ttu-id="f6344-517">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-517">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-518">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-518">Monitor</span></span>
* <span data-ttu-id="f6344-519">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-519">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="f6344-520">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-520">Network</span></span>
* <span data-ttu-id="f6344-521">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-521">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="f6344-522">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-522">Profile</span></span>
* <span data-ttu-id="f6344-523">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-523">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="f6344-524">Postgres</span><span class="sxs-lookup"><span data-stu-id="f6344-524">Postgres</span></span> 
* <span data-ttu-id="f6344-525">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-525">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="f6344-526">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="f6344-526">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-527">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-527">Resource</span></span>
* <span data-ttu-id="f6344-528">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-528">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="f6344-529">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-529">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="f6344-530">Graph</span><span class="sxs-lookup"><span data-stu-id="f6344-530">Graph</span></span>
* <span data-ttu-id="f6344-531">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-531">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="f6344-532">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-532">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="f6344-533">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-533">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="f6344-534">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-534">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="f6344-535">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-535">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-536">storage</span><span class="sxs-lookup"><span data-stu-id="f6344-536">storage</span></span>
* <span data-ttu-id="f6344-537">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-537">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="f6344-538">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-538">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="f6344-539">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-539">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="f6344-540">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-540">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-541">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-541">VM</span></span>
* <span data-ttu-id="f6344-542">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-542">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="f6344-543">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="f6344-543">March 12, 2019</span></span>

<span data-ttu-id="f6344-544">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="f6344-544">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="f6344-545">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-545">Core</span></span>

* <span data-ttu-id="f6344-546">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-546">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-547">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-547">ACR</span></span>

* <span data-ttu-id="f6344-548">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-548">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-549">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-549">ACS</span></span>

* <span data-ttu-id="f6344-550">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-550">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="f6344-551">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-551">AppService</span></span>

* <span data-ttu-id="f6344-552">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-552">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="f6344-553">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-553">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="f6344-554">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-554">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="f6344-555">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-555">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="f6344-556">Botservice</span><span class="sxs-lookup"><span data-stu-id="f6344-556">Botservice</span></span>

* <span data-ttu-id="f6344-557">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-557">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="f6344-558">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-558">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="f6344-559">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-559">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="f6344-560">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-560">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="f6344-561">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-561">Container</span></span>

* <span data-ttu-id="f6344-562">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-562">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="f6344-563">EventHub</span><span class="sxs-lookup"><span data-stu-id="f6344-563">EventHub</span></span>

* <span data-ttu-id="f6344-564">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-564">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="f6344-565">Find</span><span class="sxs-lookup"><span data-stu-id="f6344-565">Find</span></span>

* <span data-ttu-id="f6344-566">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="f6344-566">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f6344-567">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f6344-567">HDInsight</span></span>

* <span data-ttu-id="f6344-568">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-568">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="f6344-569">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-569">Network</span></span>

* <span data-ttu-id="f6344-570">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-570">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="f6344-571">Rdbms</span><span class="sxs-lookup"><span data-stu-id="f6344-571">Rdbms</span></span>

* <span data-ttu-id="f6344-572">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="f6344-572">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="f6344-573">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-573">Role</span></span>

* <span data-ttu-id="f6344-574">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-574">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="f6344-575">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-575">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="f6344-576">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="f6344-576">Service Fabric</span></span>

* <span data-ttu-id="f6344-577">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-577">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="f6344-578">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="f6344-578">February 26, 2019</span></span>

<span data-ttu-id="f6344-579">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="f6344-579">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="f6344-580">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-580">Core</span></span>

* <span data-ttu-id="f6344-581">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-581">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-582">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-582">ACR</span></span>

* <span data-ttu-id="f6344-583">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-583">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="f6344-584">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-584">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-585">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-585">ACS</span></span>

* <span data-ttu-id="f6344-586">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-586">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-587">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-587">AppService</span></span>

* <span data-ttu-id="f6344-588">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-588">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-589">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-589">Batch</span></span>
* <span data-ttu-id="f6344-590">[重大な変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-590">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="f6344-591">[重大な変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-591">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="f6344-592">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-592">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="f6344-593">[重大な変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-593">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="f6344-594">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-594">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="f6344-595">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="f6344-595">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f6344-596">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f6344-596">CosmosDB</span></span>

* <span data-ttu-id="f6344-597">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-597">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="f6344-598">Kusto</span><span class="sxs-lookup"><span data-stu-id="f6344-598">Kusto</span></span>

* <span data-ttu-id="f6344-599">[重大な変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-599">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="f6344-600">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-600">Network</span></span>

* <span data-ttu-id="f6344-601">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-601">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="f6344-602">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-602">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="f6344-603">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-603">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="f6344-604">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-604">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="f6344-605">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-605">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="f6344-606">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-606">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="f6344-607">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-607">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-608">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-608">Resource</span></span>

* <span data-ttu-id="f6344-609">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-609">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="f6344-610">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-610">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="f6344-611">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-611">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="f6344-612">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-612">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="f6344-613">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-613">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="f6344-614">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-614">Role</span></span>

* <span data-ttu-id="f6344-615">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-615">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-616">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-616">VM</span></span>

* <span data-ttu-id="f6344-617">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-617">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="f6344-618">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="f6344-618">February 12, 2019</span></span>

<span data-ttu-id="f6344-619">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="f6344-619">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="f6344-620">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-620">Core</span></span>

* <span data-ttu-id="f6344-621">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-621">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="f6344-622">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-622">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-623">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-623">ACR</span></span>
* <span data-ttu-id="f6344-624">[重大な変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-624">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="f6344-625">[重大な変更] `acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-625">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-626">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-626">ACS</span></span>
* <span data-ttu-id="f6344-627">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-627">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="f6344-628">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-628">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="f6344-629">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-629">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="f6344-630">AMS</span><span class="sxs-lookup"><span data-stu-id="f6344-630">AMS</span></span>
* <span data-ttu-id="f6344-631">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-631">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="f6344-632">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-632">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-633">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-633">Appservice</span></span>
* <span data-ttu-id="f6344-634">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-634">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="f6344-635">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-635">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="f6344-636">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-636">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="f6344-637">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-637">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="f6344-638">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-638">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="f6344-639">Botservice</span><span class="sxs-lookup"><span data-stu-id="f6344-639">Botservice</span></span>
* <span data-ttu-id="f6344-640">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-640">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="f6344-641">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-641">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="f6344-642">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-642">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="f6344-643">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-643">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="f6344-644">[非推奨] `--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-644">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="f6344-645">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-645">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="f6344-646">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-646">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="f6344-647">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-647">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="f6344-648">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="f6344-648">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="f6344-649">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-649">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="f6344-650">Key Vault</span><span class="sxs-lookup"><span data-stu-id="f6344-650">Key Vault</span></span>
* <span data-ttu-id="f6344-651">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-651">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-652">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-652">Monitor</span></span>
* <span data-ttu-id="f6344-653">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-653">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="f6344-654">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-654">Network</span></span>
* <span data-ttu-id="f6344-655">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-655">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="f6344-656">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-656">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="f6344-657">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-657">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="f6344-658">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-658">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="f6344-659">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="f6344-659">Policy Insights</span></span>
* <span data-ttu-id="f6344-660">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-660">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="f6344-661">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f6344-661">RDBMS</span></span>
* <span data-ttu-id="f6344-662">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-662">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="f6344-663">Redis</span><span class="sxs-lookup"><span data-stu-id="f6344-663">Redis</span></span>
* <span data-ttu-id="f6344-664">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-664">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="f6344-665">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-665">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="f6344-666">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-666">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="f6344-667">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-667">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="f6344-668">[重大な変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-668">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="f6344-669">[重大な変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="f6344-669">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="f6344-670">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-670">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="f6344-671">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-671">Role</span></span>
* <span data-ttu-id="f6344-672">[重大な変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="f6344-672">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="f6344-673">SQL VM</span><span class="sxs-lookup"><span data-stu-id="f6344-673">SQL VM</span></span>
* <span data-ttu-id="f6344-674">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-674">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-675">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-675">VM</span></span>
* <span data-ttu-id="f6344-676">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-676">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="f6344-677">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-677">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="f6344-678">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-678">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="f6344-679">[重大な変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="f6344-679">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="f6344-680">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="f6344-680">January 31, 2019</span></span>

<span data-ttu-id="f6344-681">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="f6344-681">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="f6344-682">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-682">Core</span></span>

* <span data-ttu-id="f6344-683">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="f6344-683">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="f6344-684">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="f6344-684">January 28, 2019</span></span>

<span data-ttu-id="f6344-685">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="f6344-685">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-686">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-686">ACR</span></span>
* <span data-ttu-id="f6344-687">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-687">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-688">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-688">ACS</span></span>
* <span data-ttu-id="f6344-689">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-689">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="f6344-690">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-690">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="f6344-691">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-691">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="f6344-692">AMS</span><span class="sxs-lookup"><span data-stu-id="f6344-692">AMS</span></span>
* <span data-ttu-id="f6344-693">[重大な変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-693">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="f6344-694">[重大な変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-694">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-695">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-695">Appservice</span></span>
* <span data-ttu-id="f6344-696">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-696">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="f6344-697">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-697">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="f6344-698">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-698">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="f6344-699">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-699">Container</span></span>
* <span data-ttu-id="f6344-700">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-700">Added `container start` command</span></span>
* <span data-ttu-id="f6344-701">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-701">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="f6344-702">EventGrid</span><span class="sxs-lookup"><span data-stu-id="f6344-702">EventGrid</span></span>
* <span data-ttu-id="f6344-703">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-703">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="f6344-704">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-704">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="f6344-705">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-705">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="f6344-706">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-706">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="f6344-707">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="f6344-707">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f6344-708">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f6344-708">HDInsight</span></span>
* <span data-ttu-id="f6344-709">[重大な変更] `hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-709">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="f6344-710">[重大な変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-710">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="f6344-711">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-711">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="f6344-712">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-712">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="f6344-713">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-713">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="f6344-714">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-714">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="f6344-715">IoT</span><span class="sxs-lookup"><span data-stu-id="f6344-715">IoT</span></span>
* <span data-ttu-id="f6344-716">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-716">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="f6344-717">Kusto</span><span class="sxs-lookup"><span data-stu-id="f6344-717">Kusto</span></span>
* <span data-ttu-id="f6344-718">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="f6344-718">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-719">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-719">Monitor</span></span>
* <span data-ttu-id="f6344-720">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-720">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="f6344-721">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-721">Profile</span></span>
* <span data-ttu-id="f6344-722">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-722">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="f6344-723">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-723">Network</span></span>
* <span data-ttu-id="f6344-724">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-724">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="f6344-725">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-725">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-726">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-726">Resource</span></span>
* <span data-ttu-id="f6344-727">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-727">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="f6344-728">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-728">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="f6344-729">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="f6344-729">SQL Virtual Machine</span></span>
* <span data-ttu-id="f6344-730">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="f6344-730">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-731">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-731">Storage</span></span>
* <span data-ttu-id="f6344-732">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-732">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="f6344-733">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="f6344-733">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-734">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-734">VM</span></span>
* <span data-ttu-id="f6344-735">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-735">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="f6344-736">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-736">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="f6344-737">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="f6344-737">January 15, 2019</span></span>

<span data-ttu-id="f6344-738">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="f6344-738">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-739">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-739">ACR</span></span>
* <span data-ttu-id="f6344-740">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-740">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="f6344-741">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-741">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="f6344-742">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-742">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="f6344-743">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-743">ACS</span></span>
* <span data-ttu-id="f6344-744">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-744">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-745">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-745">Appservice</span></span>
* <span data-ttu-id="f6344-746">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-746">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="f6344-747">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-747">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="f6344-748">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-748">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="f6344-749">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-749">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="f6344-750">Botservice</span><span class="sxs-lookup"><span data-stu-id="f6344-750">Botservice</span></span>
* <span data-ttu-id="f6344-751">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-751">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="f6344-752">構成</span><span class="sxs-lookup"><span data-stu-id="f6344-752">Configure</span></span>
* <span data-ttu-id="f6344-753">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-753">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f6344-754">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f6344-754">CosmosDB</span></span>
* <span data-ttu-id="f6344-755">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-755">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f6344-756">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f6344-756">HDInsight</span></span>
* <span data-ttu-id="f6344-757">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-757">Added commands for managing applications</span></span>
* <span data-ttu-id="f6344-758">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-758">Added commands for managing script actions</span></span>
* <span data-ttu-id="f6344-759">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-759">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="f6344-760">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-760">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="f6344-761">[重大な変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-761">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="f6344-762">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-762">Network</span></span>
* <span data-ttu-id="f6344-763">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-763">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="f6344-764">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-764">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="f6344-765">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-765">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="f6344-766">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-766">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="f6344-767">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-767">Role</span></span>
* <span data-ttu-id="f6344-768">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="f6344-768">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="f6344-769">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="f6344-769">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="f6344-770">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="f6344-770">Security</span></span>
* <span data-ttu-id="f6344-771">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f6344-771">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-772">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-772">Storage</span></span>
* <span data-ttu-id="f6344-773">[重大な変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-773">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="f6344-774">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="f6344-774">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="f6344-775">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-775">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="f6344-776">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-776">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="f6344-777">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-777">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-778">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-778">VM</span></span>
* <span data-ttu-id="f6344-779">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-779">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="f6344-780">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-780">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="f6344-781">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-781">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="f6344-782">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-782">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="f6344-783">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-783">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="f6344-784">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-784">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="f6344-785">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="f6344-785">December 20, 2018</span></span>

<span data-ttu-id="f6344-786">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="f6344-786">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="f6344-787">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-787">Appservice</span></span>
* <span data-ttu-id="f6344-788">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-788">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="f6344-789">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-789">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="f6344-790">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-790">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="f6344-791">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="f6344-791">IoTCentral</span></span>
* <span data-ttu-id="f6344-792">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-792">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="f6344-793">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-793">Role</span></span>
* <span data-ttu-id="f6344-794">[重大な変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-794">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-795">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-795">SQL</span></span>
* <span data-ttu-id="f6344-796">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-796">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-797">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-797">VM</span></span>
* <span data-ttu-id="f6344-798">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-798">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="f6344-799">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="f6344-799">December 18, 2018</span></span>

<span data-ttu-id="f6344-800">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="f6344-800">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="f6344-801">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-801">ACR</span></span>
* <span data-ttu-id="f6344-802">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-802">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="f6344-803">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="f6344-803">Condensed the table layout for task list</span></span>
* <span data-ttu-id="f6344-804">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-804">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-805">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-805">ACS</span></span>
* <span data-ttu-id="f6344-806">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-806">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="f6344-807">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-807">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="f6344-808">[非推奨] `az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="f6344-808">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="f6344-809">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="f6344-809">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="f6344-810">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-810">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="f6344-811">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-811">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-812">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-812">Appservice</span></span>
* <span data-ttu-id="f6344-813">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-813">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="f6344-814">Botservice</span><span class="sxs-lookup"><span data-stu-id="f6344-814">Botservice</span></span>
* <span data-ttu-id="f6344-815">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-815">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="f6344-816">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-816">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="f6344-817">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-817">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="f6344-818">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="f6344-818">Reduced Kudu network calls</span></span>
* <span data-ttu-id="f6344-819">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-819">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="f6344-820">消費</span><span class="sxs-lookup"><span data-stu-id="f6344-820">Consumption</span></span>
* <span data-ttu-id="f6344-821">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-821">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f6344-822">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f6344-822">CosmosDB</span></span>
* <span data-ttu-id="f6344-823">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-823">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="f6344-824">マップ</span><span class="sxs-lookup"><span data-stu-id="f6344-824">Maps</span></span>
* <span data-ttu-id="f6344-825">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-825">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="f6344-826">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-826">Network</span></span>
* <span data-ttu-id="f6344-827">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-827">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="f6344-828">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-828">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-829">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-829">Resource</span></span>
* <span data-ttu-id="f6344-830">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-830">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="f6344-831">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-831">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-832">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-832">Storage</span></span>
*  <span data-ttu-id="f6344-833">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-833">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-834">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-834">VM</span></span>
* <span data-ttu-id="f6344-835">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-835">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="f6344-836">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="f6344-836">December 4, 2018</span></span>

<span data-ttu-id="f6344-837">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="f6344-837">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="f6344-838">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-838">Core</span></span>
* <span data-ttu-id="f6344-839">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-839">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="f6344-840">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-840">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-841">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-841">Appservice</span></span>
* <span data-ttu-id="f6344-842">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-842">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="f6344-843">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-843">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="f6344-844">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-844">Network</span></span>
* <span data-ttu-id="f6344-845">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-845">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="f6344-846">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-846">Role</span></span>
* <span data-ttu-id="f6344-847">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-847">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="f6344-848">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-848">VM</span></span>
* <span data-ttu-id="f6344-849">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-849">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="f6344-850">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-850">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="f6344-851">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-851">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="f6344-852">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-852">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="f6344-853">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="f6344-853">November 20, 2018</span></span>

<span data-ttu-id="f6344-854">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="f6344-854">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="f6344-855">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-855">Core</span></span>
* <span data-ttu-id="f6344-856">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-856">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-857">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-857">ACR</span></span>
* <span data-ttu-id="f6344-858">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-858">Added context token to task step</span></span>
* <span data-ttu-id="f6344-859">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-859">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="f6344-860">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-860">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-861">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-861">Appservice</span></span>
* <span data-ttu-id="f6344-862">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-862">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="f6344-863">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-863">Updated the default `node_version`.</span></span> <span data-ttu-id="f6344-864">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="f6344-864">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="f6344-865">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-865">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="f6344-866">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-866">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="f6344-867">IotCentral</span><span class="sxs-lookup"><span data-stu-id="f6344-867">IotCentral</span></span>
* <span data-ttu-id="f6344-868">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-868">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="f6344-869">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f6344-869">KeyVault</span></span>
* <span data-ttu-id="f6344-870">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-870">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="f6344-871">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-871">Network</span></span>
* <span data-ttu-id="f6344-872">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-872">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="f6344-873">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-873">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="f6344-874">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-874">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="f6344-875">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-875">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="f6344-876">Rdbms</span><span class="sxs-lookup"><span data-stu-id="f6344-876">Rdbms</span></span>
* <span data-ttu-id="f6344-877">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-877">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="f6344-878">Rbac</span><span class="sxs-lookup"><span data-stu-id="f6344-878">Rbac</span></span>
* <span data-ttu-id="f6344-879">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-879">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="f6344-880">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-880">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="f6344-881">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-881">Storage</span></span>
* <span data-ttu-id="f6344-882">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-882">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="f6344-883">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-883">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="f6344-884">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-884">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="f6344-885">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="f6344-885">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-886">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-886">VM</span></span>
* <span data-ttu-id="f6344-887">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-887">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="f6344-888">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-888">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="f6344-889">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="f6344-889">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="f6344-890">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-890">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="f6344-891">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-891">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="f6344-892">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-892">Added `snapshot wait` command</span></span>
* <span data-ttu-id="f6344-893">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-893">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="f6344-894">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="f6344-894">November 6, 2018</span></span>

<span data-ttu-id="f6344-895">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="f6344-895">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="f6344-896">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-896">Core</span></span>
* <span data-ttu-id="f6344-897">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-897">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-898">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-898">ACR</span></span>
* <span data-ttu-id="f6344-899">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-899">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="f6344-900">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-900">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-901">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-901">ACS</span></span>
* <span data-ttu-id="f6344-902">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-902">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="f6344-903">Advisor</span><span class="sxs-lookup"><span data-stu-id="f6344-903">Advisor</span></span>
* <span data-ttu-id="f6344-904">GA リリース</span><span class="sxs-lookup"><span data-stu-id="f6344-904">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="f6344-905">AMS</span><span class="sxs-lookup"><span data-stu-id="f6344-905">AMS</span></span>
* <span data-ttu-id="f6344-906">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-906">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="f6344-907">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-907">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="f6344-908">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-908">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="f6344-909">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-909">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="f6344-910">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-910">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="f6344-911">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-911">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="f6344-912">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-912">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="f6344-913">[重大な変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="f6344-913">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="f6344-914">[重大な変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-914">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="f6344-915">[重大な変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-915">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="f6344-916">[重大な変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="f6344-916">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="f6344-917">[重大な変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="f6344-917">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="f6344-918">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="f6344-918">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="f6344-919">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="f6344-919">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="f6344-920">[重大な変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-920">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="f6344-921">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f6344-921">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="f6344-922">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="f6344-922">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-923">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-923">AppService</span></span>
* <span data-ttu-id="f6344-924">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-924">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="f6344-925">構成</span><span class="sxs-lookup"><span data-stu-id="f6344-925">Configure</span></span>
* <span data-ttu-id="f6344-926">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-926">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="f6344-927">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-927">Container</span></span>
* <span data-ttu-id="f6344-928">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-928">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="f6344-929">EventHub</span><span class="sxs-lookup"><span data-stu-id="f6344-929">EventHub</span></span>
* <span data-ttu-id="f6344-930">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-930">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="f6344-931">Interactive</span><span class="sxs-lookup"><span data-stu-id="f6344-931">Interactive</span></span>
* <span data-ttu-id="f6344-932">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="f6344-932">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-933">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-933">Monitor</span></span>
* <span data-ttu-id="f6344-934">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-934">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="f6344-935">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-935">Network</span></span>
* <span data-ttu-id="f6344-936">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-936">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="f6344-937">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-937">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="f6344-938">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-938">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="f6344-939">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-939">Profile</span></span>
* <span data-ttu-id="f6344-940">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-940">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="f6344-941">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f6344-941">RDBMS</span></span>
* <span data-ttu-id="f6344-942">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-942">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-943">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-943">Resource</span></span>
* <span data-ttu-id="f6344-944">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-944">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="f6344-945">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-945">Role</span></span>
* <span data-ttu-id="f6344-946">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-946">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="f6344-947">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-947">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="f6344-948">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-948">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-949">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-949">Storage</span></span>
* <span data-ttu-id="f6344-950">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="f6344-950">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-951">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-951">VM</span></span>
* <span data-ttu-id="f6344-952">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-952">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="f6344-953">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-953">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="f6344-954">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-954">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="f6344-955">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-955">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="f6344-956">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="f6344-956">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="f6344-957">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-957">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="f6344-958">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="f6344-958">October 23, 2018</span></span>

<span data-ttu-id="f6344-959">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="f6344-959">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="f6344-960">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-960">Core</span></span>
* <span data-ttu-id="f6344-961">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-961">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="f6344-962">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-962">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-963">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-963">ACR</span></span>
* <span data-ttu-id="f6344-964">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-964">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="f6344-965">CDN</span><span class="sxs-lookup"><span data-stu-id="f6344-965">CDN</span></span>
* <span data-ttu-id="f6344-966">[重大な変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="f6344-966">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="f6344-967">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-967">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="f6344-968">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-968">Container</span></span>
* <span data-ttu-id="f6344-969">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-969">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="f6344-970">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-970">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="f6344-971">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-971">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="f6344-972">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-972">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="f6344-973">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-973">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="f6344-974">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-974">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="f6344-975">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-975">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f6344-976">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f6344-976">CosmosDB</span></span>
* <span data-ttu-id="f6344-977">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-977">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="f6344-978">Interactive</span><span class="sxs-lookup"><span data-stu-id="f6344-978">Interactive</span></span>
* <span data-ttu-id="f6344-979">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-979">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="f6344-980">IoT Central</span><span class="sxs-lookup"><span data-stu-id="f6344-980">IoT Central</span></span>
* <span data-ttu-id="f6344-981">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-981">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="f6344-982">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="f6344-982">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-983">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-983">Monitor</span></span>
* <span data-ttu-id="f6344-984">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="f6344-984">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="f6344-985">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-985">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="f6344-986">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-986">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="f6344-987">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-987">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="f6344-988">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-988">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="f6344-989">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-989">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="f6344-990">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="f6344-990">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="f6344-991">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-991">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="f6344-992">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-992">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="f6344-993">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-993">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="f6344-994">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-994">Network</span></span>
* <span data-ttu-id="f6344-995">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-995">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="f6344-996">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-996">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="f6344-997">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f6344-997">ServiceBus</span></span>
* <span data-ttu-id="f6344-998">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-998">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-999">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-999">SQL</span></span>
* <span data-ttu-id="f6344-1000">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1000">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1001">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1001">Storage</span></span>
* <span data-ttu-id="f6344-1002">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1002">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="f6344-1003">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1003">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1004">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1004">VM</span></span>
* <span data-ttu-id="f6344-1005">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="f6344-1005">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="f6344-1006">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1006">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="f6344-1007">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1007">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="f6344-1008">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1008">October 16, 2018</span></span>

<span data-ttu-id="f6344-1009">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="f6344-1009">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1010">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1010">VM</span></span>
* <span data-ttu-id="f6344-1011">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1011">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="f6344-1012">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1012">October 9, 2018</span></span>

<span data-ttu-id="f6344-1013">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="f6344-1013">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="f6344-1014">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-1014">Core</span></span>
* <span data-ttu-id="f6344-1015">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1015">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-1016">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-1016">ACR</span></span>
* <span data-ttu-id="f6344-1017">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1017">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1018">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1018">ACS</span></span>
* <span data-ttu-id="f6344-1019">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="f6344-1019">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="f6344-1020">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1020">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="f6344-1021">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1021">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="f6344-1022">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1022">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="f6344-1023">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-1023">Container</span></span>
* <span data-ttu-id="f6344-1024">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1024">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="f6344-1025">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1025">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="f6344-1026">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="f6344-1026">Event Hub</span></span>
* <span data-ttu-id="f6344-1027">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1027">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="f6344-1028">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1028">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="f6344-1029">Extensions</span><span class="sxs-lookup"><span data-stu-id="f6344-1029">Extensions</span></span>
* <span data-ttu-id="f6344-1030">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1030">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="f6344-1031">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f6344-1031">HDInsight</span></span>
* <span data-ttu-id="f6344-1032">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f6344-1032">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="f6344-1033">IoT</span><span class="sxs-lookup"><span data-stu-id="f6344-1033">IoT</span></span>
* <span data-ttu-id="f6344-1034">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1034">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="f6344-1035">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f6344-1035">KeyVault</span></span>
* <span data-ttu-id="f6344-1036">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1036">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1037">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1037">Network</span></span>
* <span data-ttu-id="f6344-1038">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="f6344-1038">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="f6344-1039">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="f6344-1039">See #6052</span></span>
* <span data-ttu-id="f6344-1040">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1040">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="f6344-1041">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="f6344-1041">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="f6344-1042">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1042">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="f6344-1043">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1043">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="f6344-1044">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1044">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="f6344-1045">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1045">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="f6344-1046">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-1046">Role</span></span>
* <span data-ttu-id="f6344-1047">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1047">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="f6344-1048">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1048">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="f6344-1049">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1049">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="f6344-1050">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1050">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="f6344-1051">Service Bus</span><span class="sxs-lookup"><span data-stu-id="f6344-1051">Service Bus</span></span>
* <span data-ttu-id="f6344-1052">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1052">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1053">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1053">VM</span></span>
* <span data-ttu-id="f6344-1054">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1054">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="f6344-1055">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1055">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="f6344-1056">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1056">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="f6344-1057">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1057">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="f6344-1058">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1058">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="f6344-1059">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1059">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="f6344-1060">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1060">September 21, 2018</span></span>

<span data-ttu-id="f6344-1061">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="f6344-1061">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-1062">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-1062">ACR</span></span>
* <span data-ttu-id="f6344-1063">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1063">Added ACR Task commands</span></span>
* <span data-ttu-id="f6344-1064">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1064">Added quick run command</span></span>
* <span data-ttu-id="f6344-1065">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1065">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="f6344-1066">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1066">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="f6344-1067">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1067">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="f6344-1068">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1068">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1069">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1069">ACS</span></span>
* <span data-ttu-id="f6344-1070">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1070">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="f6344-1071">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1071">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1072">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-1072">AppService</span></span>

* <span data-ttu-id="f6344-1073">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1073">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="f6344-1074">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1074">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="f6344-1075">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1075">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="f6344-1076">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1076">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-1077">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-1077">Batch</span></span>
* <span data-ttu-id="f6344-1078">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1078">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="f6344-1079">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1079">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="f6344-1080">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1080">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="f6344-1081">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1081">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="f6344-1082">Batch AI</span><span class="sxs-lookup"><span data-stu-id="f6344-1082">Batch AI</span></span> 
* <span data-ttu-id="f6344-1083">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1083">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="f6344-1084">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="f6344-1084">Cognitive Services</span></span>
* <span data-ttu-id="f6344-1085">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1085">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="f6344-1086">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1086">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="f6344-1087">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1087">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="f6344-1088">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1088">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="f6344-1089">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1089">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="f6344-1090">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1090">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="f6344-1091">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-1091">Container</span></span>
* <span data-ttu-id="f6344-1092">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1092">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="f6344-1093">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1093">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="f6344-1094">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1094">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="f6344-1095">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1095">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="f6344-1096">DataLake</span><span class="sxs-lookup"><span data-stu-id="f6344-1096">Datalake</span></span>
* <span data-ttu-id="f6344-1097">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1097">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="f6344-1098">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="f6344-1098">Interactive Shell</span></span>
* <span data-ttu-id="f6344-1099">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1099">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="f6344-1100">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1100">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="f6344-1101">IoT</span><span class="sxs-lookup"><span data-stu-id="f6344-1101">IoT</span></span>
* <span data-ttu-id="f6344-1102">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1102">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="f6344-1103">Key Vault</span><span class="sxs-lookup"><span data-stu-id="f6344-1103">Key Vault</span></span>
* <span data-ttu-id="f6344-1104">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1104">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1105">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1105">Network</span></span>
* <span data-ttu-id="f6344-1106">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1106">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="f6344-1107">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1107">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="f6344-1108">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1108">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="f6344-1109">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1109">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="f6344-1110">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1110">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="f6344-1111">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1111">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="f6344-1112">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1112">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="f6344-1113">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-1113">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="f6344-1114">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1114">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="f6344-1115">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1115">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="f6344-1116">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1116">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="f6344-1117">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1117">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="f6344-1118">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1118">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="f6344-1119">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="f6344-1119">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="f6344-1120">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1120">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="f6344-1121">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1121">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="f6344-1122">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1122">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="f6344-1123">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1123">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="f6344-1124">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f6344-1124">RDBMS</span></span>
* <span data-ttu-id="f6344-1125">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1125">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="f6344-1126">予約</span><span class="sxs-lookup"><span data-stu-id="f6344-1126">Reservation</span></span>
* <span data-ttu-id="f6344-1127">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1127">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="f6344-1128">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1128">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="f6344-1129">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="f6344-1129">Manage App</span></span>
* <span data-ttu-id="f6344-1130">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1130">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="f6344-1131">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1131">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="f6344-1132">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-1132">Role</span></span>
* <span data-ttu-id="f6344-1133">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1133">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="f6344-1134">SignalR</span><span class="sxs-lookup"><span data-stu-id="f6344-1134">SignalR</span></span>
* <span data-ttu-id="f6344-1135">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f6344-1135">First release</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1136">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1136">Storage</span></span>
* <span data-ttu-id="f6344-1137">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1137">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="f6344-1138">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1138">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1139">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1139">VM</span></span>
* <span data-ttu-id="f6344-1140">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="f6344-1140">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="f6344-1141">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1141">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="f6344-1142">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1142">August 28, 2018</span></span>

<span data-ttu-id="f6344-1143">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="f6344-1143">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="f6344-1144">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-1144">Core</span></span>

* <span data-ttu-id="f6344-1145">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1145">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="f6344-1146">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1146">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-1147">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-1147">ACR</span></span>

* <span data-ttu-id="f6344-1148">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1148">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="f6344-1149">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1149">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1150">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1150">ACS</span></span>

* <span data-ttu-id="f6344-1151">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1151">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="f6344-1152">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1152">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1153">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-1153">AppService</span></span>

* <span data-ttu-id="f6344-1154">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1154">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="f6344-1155">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1155">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="f6344-1156">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1156">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="f6344-1157">バックアップ</span><span class="sxs-lookup"><span data-stu-id="f6344-1157">Backup</span></span>

* <span data-ttu-id="f6344-1158">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1158">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="f6344-1159">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="f6344-1159">Bot Service</span></span>

* <span data-ttu-id="f6344-1160">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="f6344-1160">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="f6344-1161">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="f6344-1161">Cognitive Services</span></span>

* <span data-ttu-id="f6344-1162">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1162">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="f6344-1163">IoT</span><span class="sxs-lookup"><span data-stu-id="f6344-1163">IoT</span></span>

* <span data-ttu-id="f6344-1164">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1164">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-1165">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-1165">Monitor</span></span>

* <span data-ttu-id="f6344-1166">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1166">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="f6344-1167">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1167">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1168">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1168">Network</span></span>

* <span data-ttu-id="f6344-1169">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1169">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-1170">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-1170">Resource</span></span>

* <span data-ttu-id="f6344-1171">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1171">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1172">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1172">Storage</span></span>

* <span data-ttu-id="f6344-1173">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1173">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1174">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1174">VM</span></span>

* <span data-ttu-id="f6344-1175">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1175">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="f6344-1176">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1176">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="f6344-1177">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1177">Auguest 14, 2018</span></span>

<span data-ttu-id="f6344-1178">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="f6344-1178">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="f6344-1179">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-1179">Core</span></span>

* <span data-ttu-id="f6344-1180">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1180">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="f6344-1181">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1181">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="f6344-1182">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="f6344-1182">Telemetry</span></span>

* <span data-ttu-id="f6344-1183">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1183">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-1184">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-1184">ACR</span></span>

* <span data-ttu-id="f6344-1185">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1185">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="f6344-1186">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1186">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1187">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1187">ACS</span></span>

* <span data-ttu-id="f6344-1188">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1188">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="f6344-1189">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1189">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="f6344-1190">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1190">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="f6344-1191">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1191">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="f6344-1192">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1192">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="f6344-1193">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-1193">AppService</span></span>

* <span data-ttu-id="f6344-1194">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1194">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="f6344-1195">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1195">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="f6344-1196">BatchAI</span><span class="sxs-lookup"><span data-stu-id="f6344-1196">BatchAI</span></span>

* <span data-ttu-id="f6344-1197">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1197">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="f6344-1198">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-1198">Container</span></span>

* <span data-ttu-id="f6344-1199">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1199">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="f6344-1200">IoT</span><span class="sxs-lookup"><span data-stu-id="f6344-1200">IoT</span></span>

* <span data-ttu-id="f6344-1201">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1201">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="f6344-1202">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1202">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="f6344-1203">Iot Central</span><span class="sxs-lookup"><span data-stu-id="f6344-1203">Iot Central</span></span>

* <span data-ttu-id="f6344-1204">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f6344-1204">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="f6344-1205">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f6344-1205">KeyVault</span></span>


* <span data-ttu-id="f6344-1206">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1206">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="f6344-1207">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1207">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="f6344-1208">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1208">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="f6344-1209">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1209">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="f6344-1210">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1210">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="f6344-1211">リレー</span><span class="sxs-lookup"><span data-stu-id="f6344-1211">Relay</span></span>

* <span data-ttu-id="f6344-1212">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f6344-1212">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-1213">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-1213">Sql</span></span>

* <span data-ttu-id="f6344-1214">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1214">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1215">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1215">Storage</span></span>

* <span data-ttu-id="f6344-1216">[重大な変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="f6344-1216">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="f6344-1217">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1217">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="f6344-1218">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1218">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="f6344-1219">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1219">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="f6344-1220">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1220">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1221">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1221">VM</span></span>

* <span data-ttu-id="f6344-1222">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1222">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="f6344-1223">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="f6344-1223">July 31, 2018</span></span>

<span data-ttu-id="f6344-1224">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="f6344-1224">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-1225">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-1225">ACR</span></span>

* <span data-ttu-id="f6344-1226">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1226">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="f6344-1227">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1227">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1228">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1228">ACS</span></span>

* <span data-ttu-id="f6344-1229">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1229">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-1230">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-1230">Batch</span></span>

* <span data-ttu-id="f6344-1231">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1231">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="f6344-1232">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-1232">Container</span></span>

* <span data-ttu-id="f6344-1233">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1233">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1234">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1234">Network</span></span>

* <span data-ttu-id="f6344-1235">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1235">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="f6344-1236">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-1236">Resource</span></span>

* <span data-ttu-id="f6344-1237">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1237">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="f6344-1238">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1238">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="f6344-1239">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-1239">Role</span></span>

* <span data-ttu-id="f6344-1240">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1240">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="f6344-1241">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1241">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="f6344-1242">Search</span><span class="sxs-lookup"><span data-stu-id="f6344-1242">Search</span></span>

* <span data-ttu-id="f6344-1243">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1243">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="f6344-1244">Service Bus</span><span class="sxs-lookup"><span data-stu-id="f6344-1244">Service Bus</span></span>

* <span data-ttu-id="f6344-1245">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1245">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="f6344-1246">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1246">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="f6344-1247">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="f6344-1247">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="f6344-1248">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="f6344-1248">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1249">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1249">Storage</span></span>

* <span data-ttu-id="f6344-1250">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-1250">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="f6344-1251">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1251">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1252">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1252">VM</span></span>

* <span data-ttu-id="f6344-1253">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-1253">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="f6344-1254">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1254">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="f6344-1255">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1255">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="f6344-1256">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1256">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="f6344-1257">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1257">July 18, 2018</span></span>

<span data-ttu-id="f6344-1258">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="f6344-1258">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="f6344-1259">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-1259">Core</span></span>

* <span data-ttu-id="f6344-1260">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1260">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="f6344-1261">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1261">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="f6344-1262">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1262">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-1263">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-1263">ACR</span></span>

* <span data-ttu-id="f6344-1264">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1264">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="f6344-1265">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1265">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="f6344-1266">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1266">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="f6344-1267">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1267">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1268">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1268">ACS</span></span>

* <span data-ttu-id="f6344-1269">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1269">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1270">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-1270">AppService</span></span>

* <span data-ttu-id="f6344-1271">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1271">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-1272">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-1272">Batch</span></span>

* <span data-ttu-id="f6344-1273">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1273">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="f6344-1274">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1274">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="f6344-1275">Batch AI</span><span class="sxs-lookup"><span data-stu-id="f6344-1275">Batch AI</span></span>

* <span data-ttu-id="f6344-1276">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1276">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="f6344-1277">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-1277">Container</span></span>

* <span data-ttu-id="f6344-1278">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1278">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="f6344-1279">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1279">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1280">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1280">Network</span></span>

* <span data-ttu-id="f6344-1281">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1281">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="f6344-1282">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1282">Added `network nic wait`</span></span>
* <span data-ttu-id="f6344-1283">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1283">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="f6344-1284">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1284">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="f6344-1285">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-1285">Resource</span></span>

* <span data-ttu-id="f6344-1286">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1286">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="f6344-1287">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1287">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="f6344-1288">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1288">Added `deployment wait` command</span></span>
* <span data-ttu-id="f6344-1289">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1289">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-1290">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-1290">SQL</span></span>

* <span data-ttu-id="f6344-1291">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1291">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="f6344-1292">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-1292">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="f6344-1293">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1293">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1294">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1294">Storage</span></span>

* <span data-ttu-id="f6344-1295">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1295">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1296">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1296">VM</span></span>

* <span data-ttu-id="f6344-1297">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1297">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="f6344-1298">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1298">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="f6344-1299">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1299">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="f6344-1300">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1300">July 3, 2018</span></span>

<span data-ttu-id="f6344-1301">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="f6344-1301">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="f6344-1302">AKS</span><span class="sxs-lookup"><span data-stu-id="f6344-1302">AKS</span></span>

* <span data-ttu-id="f6344-1303">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1303">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="f6344-1304">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1304">July 3, 2018</span></span>

<span data-ttu-id="f6344-1305">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="f6344-1305">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="f6344-1306">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-1306">Core</span></span>

* <span data-ttu-id="f6344-1307">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1307">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-1308">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-1308">ACR</span></span>

* <span data-ttu-id="f6344-1309">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1309">Added polling build status</span></span>
* <span data-ttu-id="f6344-1310">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1310">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="f6344-1311">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1311">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1312">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1312">ACS</span></span>

* <span data-ttu-id="f6344-1313">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1313">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="f6344-1314">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1314">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="f6344-1315">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1315">Updated options for `aks browse` command.</span></span> <span data-ttu-id="f6344-1316">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1316">Added `--listen-port` support</span></span>
* <span data-ttu-id="f6344-1317">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1317">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="f6344-1318">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="f6344-1318">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="f6344-1319">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1319">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1320">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-1320">AppService</span></span>

* <span data-ttu-id="f6344-1321">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-1321">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="f6344-1322">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1322">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="f6344-1323">バックアップ</span><span class="sxs-lookup"><span data-stu-id="f6344-1323">Backup</span></span>

* <span data-ttu-id="f6344-1324">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1324">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="f6344-1325">BatchAI</span><span class="sxs-lookup"><span data-stu-id="f6344-1325">BatchAI</span></span>

* <span data-ttu-id="f6344-1326">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1326">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="f6344-1327">クラウド</span><span class="sxs-lookup"><span data-stu-id="f6344-1327">Cloud</span></span>

* <span data-ttu-id="f6344-1328">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1328">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="f6344-1329">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-1329">Container</span></span>

* <span data-ttu-id="f6344-1330">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1330">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="f6344-1331">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1331">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="f6344-1332">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1332">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="f6344-1333">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f6344-1333">Extension</span></span>

* <span data-ttu-id="f6344-1334">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1334">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1335">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1335">Network</span></span>

* <span data-ttu-id="f6344-1336">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1336">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="f6344-1337">Rdbms</span><span class="sxs-lookup"><span data-stu-id="f6344-1337">Rdbms</span></span>

* <span data-ttu-id="f6344-1338">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1338">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-1339">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-1339">Resource</span></span>

* <span data-ttu-id="f6344-1340">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1340">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1341">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1341">VM</span></span>

* <span data-ttu-id="f6344-1342">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-1342">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="f6344-1343">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1343">June 25, 2018</span></span>

<span data-ttu-id="f6344-1344">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="f6344-1344">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="f6344-1345">CLI</span><span class="sxs-lookup"><span data-stu-id="f6344-1345">CLI</span></span>

* <span data-ttu-id="f6344-1346">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1346">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="f6344-1347">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1347">June 19, 2018</span></span>

<span data-ttu-id="f6344-1348">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="f6344-1348">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="f6344-1349">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-1349">Core</span></span>

* <span data-ttu-id="f6344-1350">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1350">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-1351">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-1351">ACR</span></span>

* <span data-ttu-id="f6344-1352">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1352">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="f6344-1353">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1353">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1354">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1354">ACS</span></span>

* <span data-ttu-id="f6344-1355">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1355">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="f6344-1356">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1356">Added `--update` support</span></span>
* <span data-ttu-id="f6344-1357">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1357">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="f6344-1358">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1358">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="f6344-1359">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1359">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="f6344-1360">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1360">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="f6344-1361">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1361">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="f6344-1362">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1362">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1363">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-1363">AppService</span></span>

* <span data-ttu-id="f6344-1364">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1364">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="f6344-1365">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1365">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-1366">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-1366">Batch</span></span>

* <span data-ttu-id="f6344-1367">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1367">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="f6344-1368">Batch AI</span><span class="sxs-lookup"><span data-stu-id="f6344-1368">Batch AI</span></span>

* <span data-ttu-id="f6344-1369">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1369">Added support for workspaces.</span></span> <span data-ttu-id="f6344-1370">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="f6344-1370">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="f6344-1371">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1371">Added support for experiments.</span></span> <span data-ttu-id="f6344-1372">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="f6344-1372">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="f6344-1373">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1373">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="f6344-1374">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1374">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="f6344-1375">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="f6344-1375">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="f6344-1376">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1376">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="f6344-1377">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="f6344-1377">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="f6344-1378">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="f6344-1378">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="f6344-1379">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1379">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="f6344-1380">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="f6344-1380">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="f6344-1381">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1381">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="f6344-1382">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="f6344-1382">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="f6344-1383">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1383">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="f6344-1384">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="f6344-1384">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="f6344-1385">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1385">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="f6344-1386">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1386">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="f6344-1387">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1387">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="f6344-1388">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1388">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="f6344-1389">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1389">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="f6344-1390">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1390">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="f6344-1391">マップ</span><span class="sxs-lookup"><span data-stu-id="f6344-1391">Maps</span></span>

* <span data-ttu-id="f6344-1392">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1392">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1393">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1393">Network</span></span>

* <span data-ttu-id="f6344-1394">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="f6344-1394">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="f6344-1395">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1395">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="f6344-1396">#6502</span><span class="sxs-lookup"><span data-stu-id="f6344-1396">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="f6344-1397">Reservations</span><span class="sxs-lookup"><span data-stu-id="f6344-1397">Reservations</span></span>

* <span data-ttu-id="f6344-1398">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1398">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="f6344-1399">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1399">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="f6344-1400">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1400">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="f6344-1401">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1401">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="f6344-1402">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1402">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="f6344-1403">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1403">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="f6344-1404">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-1404">Role</span></span>

* <span data-ttu-id="f6344-1405">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1405">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-1406">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-1406">SQL</span></span>

* <span data-ttu-id="f6344-1407">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1407">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1408">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1408">Storage</span></span>

* <span data-ttu-id="f6344-1409">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1409">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1410">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1410">VM</span></span>

* <span data-ttu-id="f6344-1411">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1411">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="f6344-1412">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1412">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="f6344-1413">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1413">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="f6344-1414">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1414">June 13, 2018</span></span>

<span data-ttu-id="f6344-1415">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="f6344-1415">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="f6344-1416">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-1416">Core</span></span>

* <span data-ttu-id="f6344-1417">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1417">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="f6344-1418">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1418">June 13, 2018</span></span>

<span data-ttu-id="f6344-1419">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="f6344-1419">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="f6344-1420">AKS</span><span class="sxs-lookup"><span data-stu-id="f6344-1420">AKS</span></span>

* <span data-ttu-id="f6344-1421">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1421">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="f6344-1422">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1422">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="f6344-1423">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1423">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="f6344-1424">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1424">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="f6344-1425">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1425">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1426">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-1426">AppService</span></span>

* <span data-ttu-id="f6344-1427">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1427">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="f6344-1428">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1428">June 5, 2018</span></span>

<span data-ttu-id="f6344-1429">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="f6344-1429">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="f6344-1430">Interactive</span><span class="sxs-lookup"><span data-stu-id="f6344-1430">Interactive</span></span>

* <span data-ttu-id="f6344-1431">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1431">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="f6344-1432">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1432">June 5, 2018</span></span>

<span data-ttu-id="f6344-1433">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="f6344-1433">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="f6344-1434">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-1434">Core</span></span>

* <span data-ttu-id="f6344-1435">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1435">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="f6344-1436">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1436">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-1437">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-1437">ACR</span></span>

* <span data-ttu-id="f6344-1438">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1438">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="f6344-1439">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1439">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="f6344-1440">AKS</span><span class="sxs-lookup"><span data-stu-id="f6344-1440">AKS</span></span>

* <span data-ttu-id="f6344-1441">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1441">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-1442">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-1442">Batch</span></span>

* <span data-ttu-id="f6344-1443">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1443">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="f6344-1444">IoT</span><span class="sxs-lookup"><span data-stu-id="f6344-1444">IOT</span></span>

* <span data-ttu-id="f6344-1445">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1445">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1446">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1446">Network</span></span>

* <span data-ttu-id="f6344-1447">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1447">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="f6344-1448">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="f6344-1448">Policy Insights</span></span>

* <span data-ttu-id="f6344-1449">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f6344-1449">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="f6344-1450">ARM</span><span class="sxs-lookup"><span data-stu-id="f6344-1450">ARM</span></span>

* <span data-ttu-id="f6344-1451">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1451">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-1452">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-1452">SQL</span></span>

* <span data-ttu-id="f6344-1453">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1453">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="f6344-1454">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1454">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="f6344-1455">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1455">Storage</span></span>

* <span data-ttu-id="f6344-1456">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1456">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1457">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1457">VM</span></span>

* <span data-ttu-id="f6344-1458">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1458">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="f6344-1459">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1459">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="f6344-1460">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1460">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="f6344-1461">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1461">May 22, 2018</span></span>

<span data-ttu-id="f6344-1462">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="f6344-1462">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="f6344-1463">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-1463">Core</span></span>

* <span data-ttu-id="f6344-1464">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1464">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1465">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1465">ACS</span></span>

* <span data-ttu-id="f6344-1466">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1466">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="f6344-1467">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1467">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1468">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-1468">AppService</span></span>

* <span data-ttu-id="f6344-1469">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1469">Improved generic update commands</span></span>
* <span data-ttu-id="f6344-1470">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1470">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="f6344-1471">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-1471">Container</span></span>

* <span data-ttu-id="f6344-1472">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1472">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="f6344-1473">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1473">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="f6344-1474">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f6344-1474">Extension</span></span>

* <span data-ttu-id="f6344-1475">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1475">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="f6344-1476">Interactive</span><span class="sxs-lookup"><span data-stu-id="f6344-1476">Interactive</span></span>

* <span data-ttu-id="f6344-1477">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1477">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="f6344-1478">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1478">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="f6344-1479">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f6344-1479">KeyVault</span></span>

* <span data-ttu-id="f6344-1480">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1480">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1481">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1481">Network</span></span>

* <span data-ttu-id="f6344-1482">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1482">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="f6344-1483">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1483">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-1484">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-1484">SQL</span></span>

* <span data-ttu-id="f6344-1485">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1485">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="f6344-1486">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1486">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="f6344-1487">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1487">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="f6344-1488">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1488">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="f6344-1489">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1489">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="f6344-1490">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="f6344-1490">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="f6344-1491">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="f6344-1491">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="f6344-1492">`edition`</span><span class="sxs-lookup"><span data-stu-id="f6344-1492">`edition`.</span></span> <span data-ttu-id="f6344-1493">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="f6344-1493">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="f6344-1494">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="f6344-1494">`elasticPoolName`.</span></span> <span data-ttu-id="f6344-1495">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="f6344-1495">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="f6344-1496">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1496">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="f6344-1497">`edition`</span><span class="sxs-lookup"><span data-stu-id="f6344-1497">`edition`.</span></span> <span data-ttu-id="f6344-1498">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="f6344-1498">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="f6344-1499">`dtu`</span><span class="sxs-lookup"><span data-stu-id="f6344-1499">`dtu`.</span></span> <span data-ttu-id="f6344-1500">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="f6344-1500">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="f6344-1501">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="f6344-1501">`databaseDtuMin`.</span></span> <span data-ttu-id="f6344-1502">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="f6344-1502">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="f6344-1503">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="f6344-1503">`databaseDtuMax`.</span></span> <span data-ttu-id="f6344-1504">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="f6344-1504">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="f6344-1505">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1505">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="f6344-1506">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1506">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1507">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1507">Storage</span></span>

* <span data-ttu-id="f6344-1508">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1508">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="f6344-1509">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1509">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1510">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1510">VM</span></span>

* <span data-ttu-id="f6344-1511">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1511">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="f6344-1512">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="f6344-1512">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="f6344-1513">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1513">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="f6344-1514">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1514">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="f6344-1515">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1515">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="f6344-1516">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1516">May 7, 2018</span></span>

<span data-ttu-id="f6344-1517">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="f6344-1517">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="f6344-1518">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-1518">Core</span></span>

* <span data-ttu-id="f6344-1519">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1519">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="f6344-1520">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1520">Added limited support for positional arguments</span></span>
* <span data-ttu-id="f6344-1521">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1521">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="f6344-1522">#5591</span><span class="sxs-lookup"><span data-stu-id="f6344-1522">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="f6344-1523">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1523">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="f6344-1524">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="f6344-1524">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="f6344-1525">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1525">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="f6344-1526">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1526">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="f6344-1527">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1527">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-1528">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-1528">ACR</span></span>

* <span data-ttu-id="f6344-1529">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1529">Added ACR Build commands</span></span>
* <span data-ttu-id="f6344-1530">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1530">Improved resource not found error messages</span></span>
* <span data-ttu-id="f6344-1531">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1531">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="f6344-1532">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1532">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="f6344-1533">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1533">Improved repository commands error messages</span></span>
* <span data-ttu-id="f6344-1534">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1534">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1535">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1535">ACS</span></span>

* <span data-ttu-id="f6344-1536">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1536">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="f6344-1537">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1537">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="f6344-1538">AMS</span><span class="sxs-lookup"><span data-stu-id="f6344-1538">AMS</span></span>

* <span data-ttu-id="f6344-1539">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="f6344-1539">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1540">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-1540">Appservice</span></span>

* <span data-ttu-id="f6344-1541">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1541">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="f6344-1542">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1542">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="f6344-1543">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1543">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="f6344-1544">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1544">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="f6344-1545">Batch AI</span><span class="sxs-lookup"><span data-stu-id="f6344-1545">Batch AI</span></span>

* <span data-ttu-id="f6344-1546">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1546">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="f6344-1547">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="f6344-1547">Cognitive Services</span></span>

* <span data-ttu-id="f6344-1548">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1548">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="f6344-1549">消費</span><span class="sxs-lookup"><span data-stu-id="f6344-1549">Consumption</span></span>

* <span data-ttu-id="f6344-1550">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1550">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="f6344-1551">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-1551">Container</span></span>

* <span data-ttu-id="f6344-1552">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1552">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="f6344-1553">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f6344-1553">Cosmos DB</span></span>

* <span data-ttu-id="f6344-1554">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1554">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="f6344-1555">DMS</span><span class="sxs-lookup"><span data-stu-id="f6344-1555">DMS</span></span>

* <span data-ttu-id="f6344-1556">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1556">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="f6344-1557">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f6344-1557">Extension</span></span>

* <span data-ttu-id="f6344-1558">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1558">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="f6344-1559">Interactive</span><span class="sxs-lookup"><span data-stu-id="f6344-1559">Interactive</span></span>

* <span data-ttu-id="f6344-1560">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-1560">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="f6344-1561">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1561">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="f6344-1562">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1562">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="f6344-1563">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1563">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="f6344-1564">ラボ</span><span class="sxs-lookup"><span data-stu-id="f6344-1564">Lab</span></span>

* <span data-ttu-id="f6344-1565">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1565">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1566">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1566">Network</span></span>

* <span data-ttu-id="f6344-1567">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1567">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="f6344-1568">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-1568">Profile</span></span>

* <span data-ttu-id="f6344-1569">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1569">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="f6344-1570">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1570">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="f6344-1571">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1571">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="f6344-1572">Redis</span><span class="sxs-lookup"><span data-stu-id="f6344-1572">Redis</span></span>

* <span data-ttu-id="f6344-1573">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1573">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="f6344-1574">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1574">Deprecated `redis list-all`.</span></span> <span data-ttu-id="f6344-1575">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="f6344-1575">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="f6344-1576">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1576">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="f6344-1577">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1577">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="f6344-1578">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-1578">Role</span></span>

* <span data-ttu-id="f6344-1579">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1579">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1580">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1580">Storage</span></span>

* <span data-ttu-id="f6344-1581">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="f6344-1581">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="f6344-1582">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1582">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="f6344-1583">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="f6344-1583">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="f6344-1584">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="f6344-1584">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="f6344-1585">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1585">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1586">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1586">VM</span></span>

* <span data-ttu-id="f6344-1587">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1587">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="f6344-1588">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1588">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="f6344-1589">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="f6344-1589">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="f6344-1590">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1590">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="f6344-1591">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1591">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="f6344-1592">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1592">Added write accelerator support</span></span>
* <span data-ttu-id="f6344-1593">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1593">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="f6344-1594">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1594">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="f6344-1595">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1595">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="f6344-1596">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1596">April 10, 2018</span></span>

<span data-ttu-id="f6344-1597">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="f6344-1597">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-1598">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-1598">ACR</span></span>

* <span data-ttu-id="f6344-1599">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1599">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1600">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1600">ACS</span></span>

* <span data-ttu-id="f6344-1601">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1601">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1602">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-1602">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="f6344-1604">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1604">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="f6344-1605">BatchAI</span><span class="sxs-lookup"><span data-stu-id="f6344-1605">BatchAI</span></span>

* <span data-ttu-id="f6344-1606">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1606">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="f6344-1607">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="f6344-1607">Job level mounting</span></span>
  - <span data-ttu-id="f6344-1608">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="f6344-1608">Environment variables with secret values</span></span>
  - <span data-ttu-id="f6344-1609">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="f6344-1609">Performance counters settings</span></span>
  - <span data-ttu-id="f6344-1610">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="f6344-1610">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="f6344-1611">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="f6344-1611">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="f6344-1612">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="f6344-1612">Usage and limits reporting</span></span>
  - <span data-ttu-id="f6344-1613">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="f6344-1613">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="f6344-1614">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="f6344-1614">Support for custom images</span></span>
  - <span data-ttu-id="f6344-1615">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1615">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="f6344-1616">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-1616">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="f6344-1617">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="f6344-1617">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="f6344-1618">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="f6344-1618">National clouds are supported</span></span>
* <span data-ttu-id="f6344-1619">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1619">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="f6344-1620">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1620">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="f6344-1621">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1621">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="f6344-1622">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1622">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="f6344-1623">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="f6344-1623">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="f6344-1624">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="f6344-1624">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="f6344-1625">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1625">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="f6344-1626">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1626">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="f6344-1627">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="f6344-1627">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="f6344-1628">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1628">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="f6344-1629">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1629">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="f6344-1630">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1630">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="f6344-1631">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1631">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="f6344-1632">課金</span><span class="sxs-lookup"><span data-stu-id="f6344-1632">Billing</span></span>

* <span data-ttu-id="f6344-1633">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1633">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="f6344-1634">消費</span><span class="sxs-lookup"><span data-stu-id="f6344-1634">Consumption</span></span>

* <span data-ttu-id="f6344-1635">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1635">Added `marketplace` commands</span></span>
* <span data-ttu-id="f6344-1636">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1636">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="f6344-1637">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1637">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="f6344-1638">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1638">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="f6344-1639">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1639">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="f6344-1640">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1640">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="f6344-1641">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-1641">Container</span></span>

* <span data-ttu-id="f6344-1642">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1642">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="f6344-1643">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1643">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="f6344-1644">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f6344-1644">Extension</span></span>

* <span data-ttu-id="f6344-1645">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1645">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="f6344-1646">Interactive</span><span class="sxs-lookup"><span data-stu-id="f6344-1646">Interactive</span></span>

* <span data-ttu-id="f6344-1647">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1647">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="f6344-1648">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1648">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="f6344-1649">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1649">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1650">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1650">Network</span></span>

* <span data-ttu-id="f6344-1651">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1651">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="f6344-1652">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1652">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="f6344-1653">#4910</span><span class="sxs-lookup"><span data-stu-id="f6344-1653">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="f6344-1654">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1654">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="f6344-1655">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="f6344-1655">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="f6344-1656">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1656">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="f6344-1657">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1657">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="f6344-1658">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1658">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="f6344-1659">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-1659">Profile</span></span>

* <span data-ttu-id="f6344-1660">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1660">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="f6344-1661">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1661">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="f6344-1662">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f6344-1662">RDBMS</span></span>

* <span data-ttu-id="f6344-1663">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1663">Added `georestore` command</span></span>
* <span data-ttu-id="f6344-1664">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1664">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-1665">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-1665">Resource</span></span>

* <span data-ttu-id="f6344-1666">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1666">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="f6344-1667">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1667">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-1668">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-1668">SQL</span></span>

* <span data-ttu-id="f6344-1669">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1669">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1670">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1670">Storage</span></span>

* <span data-ttu-id="f6344-1671">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1671">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1672">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1672">VM</span></span>

* <span data-ttu-id="f6344-1673">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1673">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="f6344-1674">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1674">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="f6344-1676">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1676">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="f6344-1677">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1677">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="f6344-1678">#5718</span><span class="sxs-lookup"><span data-stu-id="f6344-1678">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="f6344-1679">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1679">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="f6344-1680">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1680">March 27, 2018</span></span>

<span data-ttu-id="f6344-1681">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="f6344-1681">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="f6344-1682">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-1682">Core</span></span>

* <span data-ttu-id="f6344-1683">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="f6344-1683">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1684">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1684">ACS</span></span>

* <span data-ttu-id="f6344-1685">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1685">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1686">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-1686">Appservice</span></span>

* <span data-ttu-id="f6344-1687">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1687">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="f6344-1688">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1688">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="f6344-1689">バックアップ</span><span class="sxs-lookup"><span data-stu-id="f6344-1689">Backup</span></span>

* <span data-ttu-id="f6344-1690">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1690">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="f6344-1691">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="f6344-1691">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="f6344-1692">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1692">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="f6344-1693">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1693">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="f6344-1694">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-1694">Container</span></span>

* <span data-ttu-id="f6344-1695">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1695">Added `container exec` command.</span></span> <span data-ttu-id="f6344-1696">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="f6344-1696">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="f6344-1697">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="f6344-1697">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="f6344-1698">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f6344-1698">Extension</span></span>

* <span data-ttu-id="f6344-1699">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1699">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="f6344-1700">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1700">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="f6344-1701">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1701">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="f6344-1702">Interactive</span><span class="sxs-lookup"><span data-stu-id="f6344-1702">Interactive</span></span>

* <span data-ttu-id="f6344-1703">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1703">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="f6344-1704">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1704">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="f6344-1705">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="f6344-1705">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="f6344-1706">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1706">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="f6344-1707">ラボ</span><span class="sxs-lookup"><span data-stu-id="f6344-1707">Lab</span></span>

* <span data-ttu-id="f6344-1708">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1708">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-1709">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-1709">Monitor</span></span>

* <span data-ttu-id="f6344-1710">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="f6344-1710">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="f6344-1711">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="f6344-1711">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="f6344-1712">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="f6344-1712">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1713">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1713">Network</span></span>

* <span data-ttu-id="f6344-1714">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1714">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="f6344-1715">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-1715">Profile</span></span>

* <span data-ttu-id="f6344-1716">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1716">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="f6344-1717">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f6344-1717">RDBMS</span></span>

* <span data-ttu-id="f6344-1718">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1718">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-1719">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-1719">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="f6344-1721">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-1721">Role</span></span>

* <span data-ttu-id="f6344-1722">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1722">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="f6344-1723">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1723">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="f6344-1724">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1724">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="f6344-1725">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1725">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="f6344-1726">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1726">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1727">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1727">Storage</span></span>

* <span data-ttu-id="f6344-1728">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1728">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="f6344-1729">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="f6344-1729">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1730">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1730">VM</span></span>

* <span data-ttu-id="f6344-1731">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1731">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="f6344-1732">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1732">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="f6344-1733">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1733">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="f6344-1734">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1734">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="f6344-1735">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1735">March 13, 2018</span></span>

<span data-ttu-id="f6344-1736">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="f6344-1736">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-1737">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-1737">ACR</span></span>

* <span data-ttu-id="f6344-1738">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1738">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="f6344-1739">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1739">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="f6344-1740">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1740">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1741">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1741">ACS</span></span>

* <span data-ttu-id="f6344-1742">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1742">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="f6344-1743">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1743">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="f6344-1744">Advisor</span><span class="sxs-lookup"><span data-stu-id="f6344-1744">Advisor</span></span>

* <span data-ttu-id="f6344-1745">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1745">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="f6344-1746">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1746">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="f6344-1747">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1747">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="f6344-1748">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1748">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="f6344-1749">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1749">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1750">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-1750">Appservice</span></span>

* <span data-ttu-id="f6344-1751">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1751">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="f6344-1752">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1752">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="f6344-1753">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="f6344-1753">Eventhubs</span></span>

* <span data-ttu-id="f6344-1754">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f6344-1754">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="f6344-1755">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f6344-1755">Extension</span></span>

* <span data-ttu-id="f6344-1756">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1756">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="f6344-1757">Interactive</span><span class="sxs-lookup"><span data-stu-id="f6344-1757">Interactive</span></span>

* <span data-ttu-id="f6344-1758">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="f6344-1758">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="f6344-1759">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="f6344-1759">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="f6344-1760">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="f6344-1760">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="f6344-1761">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1761">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-1762">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-1762">Monitor</span></span>

* <span data-ttu-id="f6344-1763">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1763">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="f6344-1764">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1764">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="f6344-1765">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1765">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="f6344-1766">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1766">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1767">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1767">Network</span></span>

* <span data-ttu-id="f6344-1768">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1768">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="f6344-1769">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1769">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="f6344-1770">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1770">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="f6344-1771">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1771">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="f6344-1772">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-1772">Profile</span></span>

* <span data-ttu-id="f6344-1773">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1773">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="f6344-1774">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1774">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="f6344-1775">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f6344-1775">RDBMS</span></span>

* <span data-ttu-id="f6344-1776">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1776">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="f6344-1777">Service Bus</span><span class="sxs-lookup"><span data-stu-id="f6344-1777">Service Bus</span></span>

* <span data-ttu-id="f6344-1778">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f6344-1778">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1779">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1779">Storage</span></span>

* <span data-ttu-id="f6344-1780">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-1780">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="f6344-1781">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="f6344-1781">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1782">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1782">VM</span></span>

* <span data-ttu-id="f6344-1783">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1783">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="f6344-1784">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1784">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="f6344-1785">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1785">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="f6344-1786">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1786">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="f6344-1787">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1787">February 27, 2018</span></span>

<span data-ttu-id="f6344-1788">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="f6344-1788">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="f6344-1789">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-1789">Core</span></span>

* <span data-ttu-id="f6344-1790">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="f6344-1790">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="f6344-1791">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1791">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="f6344-1792">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1792">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1793">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1793">ACS</span></span>

* <span data-ttu-id="f6344-1794">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1794">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="f6344-1795">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="f6344-1795">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="f6344-1796">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1796">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="f6344-1797">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1797">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1798">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-1798">Appservice</span></span>

* <span data-ttu-id="f6344-1799">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="f6344-1799">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="f6344-1800">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="f6344-1800">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="f6344-1801">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="f6344-1801">Cognitive Services</span></span>

* <span data-ttu-id="f6344-1802">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1802">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="f6344-1803">消費</span><span class="sxs-lookup"><span data-stu-id="f6344-1803">Consumption</span></span>

* <span data-ttu-id="f6344-1804">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1804">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="f6344-1805">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1805">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="f6344-1806">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-1806">Container</span></span>

* <span data-ttu-id="f6344-1807">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1807">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1808">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1808">Network</span></span>

* <span data-ttu-id="f6344-1809">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="f6344-1809">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-1810">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-1810">Resource</span></span>

* <span data-ttu-id="f6344-1811">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1811">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="f6344-1812">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-1812">Role</span></span>

* <span data-ttu-id="f6344-1813">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1813">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-1814">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-1814">SQL</span></span>

* <span data-ttu-id="f6344-1815">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1815">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1816">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1816">Storage</span></span>

* <span data-ttu-id="f6344-1817">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1817">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1818">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1818">VM</span></span>

* <span data-ttu-id="f6344-1819">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1819">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="f6344-1820">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1820">February 13, 2018</span></span>

<span data-ttu-id="f6344-1821">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="f6344-1821">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="f6344-1822">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-1822">Core</span></span>

* <span data-ttu-id="f6344-1823">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1823">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1824">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1824">ACS</span></span>

* <span data-ttu-id="f6344-1825">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1825">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="f6344-1826">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1826">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="f6344-1827">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1827">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="f6344-1828">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1828">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="f6344-1829">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1829">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="f6344-1830">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1830">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="f6344-1831">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1831">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="f6344-1832">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="f6344-1832">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1833">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-1833">Appservice</span></span>

* <span data-ttu-id="f6344-1834">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1834">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="f6344-1835">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1835">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="f6344-1836">CDN</span><span class="sxs-lookup"><span data-stu-id="f6344-1836">CDN</span></span>

* <span data-ttu-id="f6344-1837">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1837">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="f6344-1838">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-1838">Container</span></span>

* <span data-ttu-id="f6344-1839">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1839">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="f6344-1840">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1840">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f6344-1841">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f6344-1841">CosmosDB</span></span>

* <span data-ttu-id="f6344-1842">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1842">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="f6344-1843">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f6344-1843">Extension</span></span>

* <span data-ttu-id="f6344-1844">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1844">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="f6344-1845">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1845">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="f6344-1846">フィードバック</span><span class="sxs-lookup"><span data-stu-id="f6344-1846">Feedback</span></span>

* <span data-ttu-id="f6344-1847">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1847">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="f6344-1848">Interactive</span><span class="sxs-lookup"><span data-stu-id="f6344-1848">Interactive</span></span>

* <span data-ttu-id="f6344-1849">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1849">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="f6344-1850">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1850">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="f6344-1851">IoT</span><span class="sxs-lookup"><span data-stu-id="f6344-1851">IoT</span></span>

* <span data-ttu-id="f6344-1852">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1852">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="f6344-1853">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1853">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="f6344-1854">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1854">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="f6344-1855">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1855">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-1856">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-1856">Monitor</span></span>

* <span data-ttu-id="f6344-1857">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1857">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1858">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1858">Network</span></span>

* <span data-ttu-id="f6344-1859">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1859">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="f6344-1860">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-1860">Profile</span></span>

* <span data-ttu-id="f6344-1861">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1861">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-1862">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-1862">Resource</span></span>

* <span data-ttu-id="f6344-1863">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1863">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="f6344-1864">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-1864">Role</span></span>

* <span data-ttu-id="f6344-1865">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1865">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-1866">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-1866">SQL</span></span>

* <span data-ttu-id="f6344-1867">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1867">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="f6344-1868">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1868">Added `sql db rename`</span></span>
* <span data-ttu-id="f6344-1869">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1869">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1870">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1870">Storage</span></span>

* <span data-ttu-id="f6344-1871">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1871">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1872">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1872">VM</span></span>

* <span data-ttu-id="f6344-1873">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1873">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="f6344-1874">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1874">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="f6344-1875">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="f6344-1875">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="f6344-1876">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1876">January 31, 2018</span></span>

<span data-ttu-id="f6344-1877">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="f6344-1877">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="f6344-1878">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-1878">Core</span></span>

* <span data-ttu-id="f6344-1879">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1879">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="f6344-1880">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1880">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="f6344-1881">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1881">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="f6344-1882">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="f6344-1882">Use `--verbose` to see</span></span>
* <span data-ttu-id="f6344-1883">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="f6344-1883">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1884">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1884">ACS</span></span>

* <span data-ttu-id="f6344-1885">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1885">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="f6344-1886">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1886">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1887">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-1887">Appservice</span></span>

* <span data-ttu-id="f6344-1888">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="f6344-1888">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="f6344-1889">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1889">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="f6344-1890">CDN</span><span class="sxs-lookup"><span data-stu-id="f6344-1890">CDN</span></span>

* <span data-ttu-id="f6344-1891">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1891">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f6344-1892">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f6344-1892">CosmosDB</span></span>

* <span data-ttu-id="f6344-1893">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1893">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="f6344-1894">Interactive</span><span class="sxs-lookup"><span data-stu-id="f6344-1894">Interactive</span></span>

* <span data-ttu-id="f6344-1895">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1895">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1896">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1896">Network</span></span>

* <span data-ttu-id="f6344-1897">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1897">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="f6344-1898">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1898">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="f6344-1899">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1899">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="f6344-1900">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1900">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="f6344-1901">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1901">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="f6344-1902">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-1902">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="f6344-1903">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1903">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="f6344-1904">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1904">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="f6344-1905">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1905">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="f6344-1906">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1906">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="f6344-1907">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-1907">Profile</span></span>

* <span data-ttu-id="f6344-1908">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1908">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-1909">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-1909">Resource</span></span>

* <span data-ttu-id="f6344-1910">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1910">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1911">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1911">Storage</span></span>

* <span data-ttu-id="f6344-1912">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1912">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="f6344-1913">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1913">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="f6344-1914">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1914">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="f6344-1915">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1915">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="f6344-1916">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1916">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1917">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1917">VM</span></span>

* <span data-ttu-id="f6344-1918">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1918">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="f6344-1919">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1919">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="f6344-1920">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1920">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="f6344-1921">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1921">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="f6344-1922">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1922">January 17, 2018</span></span>

<span data-ttu-id="f6344-1923">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="f6344-1923">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-1924">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-1924">ACR</span></span>

* <span data-ttu-id="f6344-1925">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1925">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="f6344-1926">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-1926">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-1927">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-1927">ACS</span></span>

* <span data-ttu-id="f6344-1928">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1928">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="f6344-1929">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1929">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-1930">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-1930">Appservice</span></span>

* <span data-ttu-id="f6344-1931">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1931">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="f6344-1932">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1932">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="f6344-1933">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1933">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="f6344-1934">バックアップ</span><span class="sxs-lookup"><span data-stu-id="f6344-1934">Backup</span></span>

* <span data-ttu-id="f6344-1935">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1935">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="f6344-1936">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1936">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="f6344-1937">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1937">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="f6344-1938">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1938">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="f6344-1939">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1939">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-1940">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-1940">Batch</span></span>

* <span data-ttu-id="f6344-1941">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1941">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="f6344-1942">クラウド</span><span class="sxs-lookup"><span data-stu-id="f6344-1942">Cloud</span></span>

* <span data-ttu-id="f6344-1943">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1943">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="f6344-1944">消費</span><span class="sxs-lookup"><span data-stu-id="f6344-1944">Consumption</span></span>

* <span data-ttu-id="f6344-1945">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1945">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="f6344-1946">Event Grid</span><span class="sxs-lookup"><span data-stu-id="f6344-1946">Event Grid</span></span>

* <span data-ttu-id="f6344-1947">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1947">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="f6344-1948">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1948">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="f6344-1949">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1949">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="f6344-1950">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="f6344-1950">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="f6344-1951">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1951">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="f6344-1952">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1952">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="f6344-1953">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1953">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="f6344-1954">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1954">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="f6344-1955">Interactive</span><span class="sxs-lookup"><span data-stu-id="f6344-1955">Interactive</span></span>

* <span data-ttu-id="f6344-1956">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1956">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="f6344-1957">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1957">Fixed errors on startup</span></span>
* <span data-ttu-id="f6344-1958">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1958">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="f6344-1959">IoT</span><span class="sxs-lookup"><span data-stu-id="f6344-1959">IoT</span></span>

* <span data-ttu-id="f6344-1960">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1960">Added support for device provisioning service</span></span>
* <span data-ttu-id="f6344-1961">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1961">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="f6344-1962">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1962">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-1963">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-1963">Monitor</span></span>

* <span data-ttu-id="f6344-1964">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1964">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="f6344-1965">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="f6344-1965">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="f6344-1966">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1966">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1967">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1967">Network</span></span>

* <span data-ttu-id="f6344-1968">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1968">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="f6344-1969">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1969">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="f6344-1970">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-1970">Profile</span></span>

* <span data-ttu-id="f6344-1971">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1971">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="f6344-1972">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-1972">Role</span></span>

* <span data-ttu-id="f6344-1973">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1973">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="f6344-1974">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="f6344-1974">Service Fabric</span></span>

* <span data-ttu-id="f6344-1975">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1975">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="f6344-1976">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1976">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1977">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1977">VM</span></span>

* <span data-ttu-id="f6344-1978">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="f6344-1978">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="f6344-1979">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1979">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="f6344-1980">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1980">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="f6344-1981">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1981">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="f6344-1982">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1982">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="f6344-1983">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1983">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="f6344-1984">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1984">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="f6344-1985">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1985">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="f6344-1986">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1986">December 19, 2017</span></span>

<span data-ttu-id="f6344-1987">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="f6344-1987">Version 2.0.23</span></span>

* <span data-ttu-id="f6344-1988">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1988">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="f6344-1989">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-1989">Container</span></span>

* <span data-ttu-id="f6344-1990">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1990">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="f6344-1991">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-1991">Network</span></span>

* <span data-ttu-id="f6344-1992">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1992">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="f6344-1993">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1993">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-1994">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-1994">Storage</span></span>

* <span data-ttu-id="f6344-1995">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1995">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-1996">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-1996">VM</span></span>

* <span data-ttu-id="f6344-1997">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-1997">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="f6344-1998">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="f6344-1998">December 5, 2017</span></span>

<span data-ttu-id="f6344-1999">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="f6344-1999">Version 2.0.22</span></span>

* <span data-ttu-id="f6344-2000">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-2000">Removed `az component` commands.</span></span> <span data-ttu-id="f6344-2001">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="f6344-2001">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="f6344-2002">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-2002">Core</span></span>
* <span data-ttu-id="f6344-2003">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2003">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="f6344-2004">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2004">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-2005">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-2005">ACS</span></span>

* <span data-ttu-id="f6344-2006">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2006">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="f6344-2007">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2007">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="f6344-2008">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2008">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="f6344-2009">Advisor</span><span class="sxs-lookup"><span data-stu-id="f6344-2009">Advisor</span></span>

* <span data-ttu-id="f6344-2010">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f6344-2010">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-2011">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-2011">Appservice</span></span>

* <span data-ttu-id="f6344-2012">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2012">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="f6344-2013">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2013">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="f6344-2014">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2014">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="f6344-2015">消費</span><span class="sxs-lookup"><span data-stu-id="f6344-2015">Consumption</span></span>

* <span data-ttu-id="f6344-2016">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2016">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="f6344-2017">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-2017">Container</span></span>

* <span data-ttu-id="f6344-2018">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2018">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-2019">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-2019">Monitor</span></span>

* <span data-ttu-id="f6344-2020">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2020">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-2021">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-2021">Resource</span></span>

* <span data-ttu-id="f6344-2022">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2022">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="f6344-2023">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-2023">Role</span></span>

* <span data-ttu-id="f6344-2024">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2024">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="f6344-2025">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="f6344-2025">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="f6344-2026">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2026">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-2027">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-2027">SQL</span></span>

* <span data-ttu-id="f6344-2028">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2028">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="f6344-2029">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2029">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-2030">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-2030">VM</span></span>

* <span data-ttu-id="f6344-2031">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2031">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="f6344-2032">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="f6344-2032">November 14, 2017</span></span>

<span data-ttu-id="f6344-2033">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="f6344-2033">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-2034">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-2034">ACR</span></span>

* <span data-ttu-id="f6344-2035">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2035">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="f6344-2036">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-2036">ACS</span></span>

* <span data-ttu-id="f6344-2037">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2037">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="f6344-2038">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-2038">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="f6344-2039">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2039">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="f6344-2040">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2040">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="f6344-2041">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2041">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-2042">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-2042">Appservice</span></span>

* <span data-ttu-id="f6344-2043">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2043">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="f6344-2044">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2044">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="f6344-2045">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2045">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="f6344-2046">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2046">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="f6344-2047">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2047">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="f6344-2048">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="f6344-2048">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-2049">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-2049">Batch</span></span>

* <span data-ttu-id="f6344-2050">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2050">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="f6344-2051">Batchai</span><span class="sxs-lookup"><span data-stu-id="f6344-2051">Batchai</span></span>

* <span data-ttu-id="f6344-2052">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2052">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="f6344-2053">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2053">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="f6344-2054">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2054">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="f6344-2055">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2055">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="f6344-2056">クラウド</span><span class="sxs-lookup"><span data-stu-id="f6344-2056">Cloud</span></span>

* <span data-ttu-id="f6344-2057">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2057">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="f6344-2058">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-2058">Container</span></span>

* <span data-ttu-id="f6344-2059">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2059">Added support to open multiple ports</span></span>
* <span data-ttu-id="f6344-2060">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2060">Added container group restart policy</span></span>
* <span data-ttu-id="f6344-2061">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2061">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="f6344-2062">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2062">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="f6344-2063">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="f6344-2063">Data Lake Analytics</span></span>

* <span data-ttu-id="f6344-2064">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2064">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="f6344-2065">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="f6344-2065">Data Lake Store</span></span>

* <span data-ttu-id="f6344-2066">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2066">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="f6344-2067">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f6344-2067">Extension</span></span>

* <span data-ttu-id="f6344-2068">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2068">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="f6344-2069">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2069">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="f6344-2070">IoT</span><span class="sxs-lookup"><span data-stu-id="f6344-2070">IoT</span></span>

* <span data-ttu-id="f6344-2071">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2071">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-2072">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-2072">Monitor</span></span>

* <span data-ttu-id="f6344-2073">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2073">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="f6344-2074">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-2074">Network</span></span>

* <span data-ttu-id="f6344-2075">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2075">Added support for CAA DNS records</span></span>
* <span data-ttu-id="f6344-2076">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2076">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="f6344-2077">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2077">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="f6344-2078">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2078">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="f6344-2079">Reservations</span><span class="sxs-lookup"><span data-stu-id="f6344-2079">Reservations</span></span>

* <span data-ttu-id="f6344-2080">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="f6344-2080">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-2081">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-2081">Resource</span></span>

* <span data-ttu-id="f6344-2082">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2082">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-2083">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-2083">SQL</span></span>

* <span data-ttu-id="f6344-2084">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2084">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-2085">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-2085">Storage</span></span>

* <span data-ttu-id="f6344-2086">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2086">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="f6344-2087">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2087">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="f6344-2088">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2088">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="f6344-2089">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2089">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="f6344-2090">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2090">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="f6344-2091">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2091">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="f6344-2092">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2092">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-2093">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-2093">VM</span></span>

* <span data-ttu-id="f6344-2094">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2094">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="f6344-2095">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2095">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="f6344-2096">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2096">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="f6344-2097">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2097">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="f6344-2098">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2098">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="f6344-2099">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="f6344-2099">October 24, 2017</span></span>

<span data-ttu-id="f6344-2100">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="f6344-2100">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="f6344-2101">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-2101">Core</span></span>

* <span data-ttu-id="f6344-2102">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2102">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-2103">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-2103">ACR</span></span>

* <span data-ttu-id="f6344-2104">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2104">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="f6344-2105">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2105">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="f6344-2106">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2106">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-2107">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-2107">ACS</span></span>

* <span data-ttu-id="f6344-2108">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2108">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="f6344-2109">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2109">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-2110">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-2110">Appservice</span></span>

* <span data-ttu-id="f6344-2111">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2111">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="f6344-2112">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f6344-2112">Component</span></span>

* <span data-ttu-id="f6344-2113">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2113">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-2114">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-2114">Monitor</span></span>

* <span data-ttu-id="f6344-2115">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2115">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-2116">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-2116">Resource</span></span>

* <span data-ttu-id="f6344-2117">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2117">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="f6344-2118">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2118">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-2119">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-2119">VM</span></span>

* <span data-ttu-id="f6344-2120">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2120">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="f6344-2121">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="f6344-2121">October 9, 2017</span></span>

<span data-ttu-id="f6344-2122">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="f6344-2122">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="f6344-2123">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-2123">Core</span></span>

* <span data-ttu-id="f6344-2124">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2124">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-2125">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-2125">Appservice</span></span>

* <span data-ttu-id="f6344-2126">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2126">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-2127">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-2127">Batch</span></span>

* <span data-ttu-id="f6344-2128">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2128">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="f6344-2129">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2129">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="f6344-2130">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2130">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="f6344-2131">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2131">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="f6344-2132">Batchai</span><span class="sxs-lookup"><span data-stu-id="f6344-2132">Batchai</span></span>

* <span data-ttu-id="f6344-2133">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f6344-2133">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="f6344-2134">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f6344-2134">Keyvault</span></span>

* <span data-ttu-id="f6344-2135">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-2135">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="f6344-2136">(#4448)</span><span class="sxs-lookup"><span data-stu-id="f6344-2136">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="f6344-2137">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-2137">Network</span></span>

* <span data-ttu-id="f6344-2138">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2138">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="f6344-2139">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2139">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-2140">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-2140">Resource</span></span>

* <span data-ttu-id="f6344-2141">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2141">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="f6344-2142">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2142">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="f6344-2143">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2143">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="f6344-2144">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2144">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-2145">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-2145">Sql</span></span>

* <span data-ttu-id="f6344-2146">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2146">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="f6344-2147">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="f6344-2147">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="f6344-2148">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="f6344-2148">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-2149">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-2149">Storage</span></span>

* <span data-ttu-id="f6344-2150">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2150">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-2151">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-2151">Vm</span></span>

* <span data-ttu-id="f6344-2152">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2152">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="f6344-2153">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2153">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="f6344-2154">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2154">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="f6344-2155">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2155">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="f6344-2156">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2156">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="f6344-2157">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="f6344-2157">September 22, 2017</span></span>

<span data-ttu-id="f6344-2158">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="f6344-2158">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-2159">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-2159">Resource</span></span>

* <span data-ttu-id="f6344-2160">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2160">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="f6344-2161">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2161">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="f6344-2162">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2162">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="f6344-2163">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2163">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="f6344-2164">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-2164">Network</span></span>

* <span data-ttu-id="f6344-2165">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2165">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="f6344-2166">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2166">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="f6344-2167">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2167">Added `asg` application security group commands</span></span>
* <span data-ttu-id="f6344-2168">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2168">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="f6344-2169">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2169">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="f6344-2170">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2170">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="f6344-2171">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2171">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-2172">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-2172">Storage</span></span>

* <span data-ttu-id="f6344-2173">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2173">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="f6344-2174">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="f6344-2174">Eventgrid</span></span>

* <span data-ttu-id="f6344-2175">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2175">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-2176">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-2176">SQL</span></span>

* <span data-ttu-id="f6344-2177">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-2177">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="f6344-2178">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="f6344-2178">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="f6344-2179">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2179">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="f6344-2180">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f6344-2180">Keyvault</span></span>

* <span data-ttu-id="f6344-2181">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2181">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-2182">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-2182">VM</span></span>

* <span data-ttu-id="f6344-2183">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2183">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="f6344-2184">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2184">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="f6344-2185">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2185">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="f6344-2186">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2186">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="f6344-2187">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2187">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="f6344-2188">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2188">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-2189">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-2189">ACS</span></span>

* <span data-ttu-id="f6344-2190">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2190">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-2191">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-2191">Appservice</span></span>

* <span data-ttu-id="f6344-2192">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2192">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="f6344-2193">バックアップ</span><span class="sxs-lookup"><span data-stu-id="f6344-2193">Backup</span></span>

* <span data-ttu-id="f6344-2194">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="f6344-2194">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="f6344-2195">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="f6344-2195">September 11, 2017</span></span>

<span data-ttu-id="f6344-2196">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="f6344-2196">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="f6344-2197">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-2197">Core</span></span>

* <span data-ttu-id="f6344-2198">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-2198">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="f6344-2199">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2199">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-2200">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-2200">Acs</span></span>

* <span data-ttu-id="f6344-2201">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2201">Added `acs list-locations` command</span></span>
* <span data-ttu-id="f6344-2202">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="f6344-2202">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-2203">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-2203">Appservice</span></span>

* <span data-ttu-id="f6344-2204">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2204">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="f6344-2205">CDN</span><span class="sxs-lookup"><span data-stu-id="f6344-2205">CDN</span></span>

* <span data-ttu-id="f6344-2206">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2206">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="f6344-2207">拡張機能</span><span class="sxs-lookup"><span data-stu-id="f6344-2207">Extension</span></span>

* <span data-ttu-id="f6344-2208">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f6344-2208">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="f6344-2209">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f6344-2209">Keyvault</span></span>

* <span data-ttu-id="f6344-2210">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2210">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="f6344-2211">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-2211">Network</span></span>

* <span data-ttu-id="f6344-2212">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2212">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="f6344-2213">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2213">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="f6344-2214">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2214">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="f6344-2215">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2215">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="f6344-2216">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2216">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-2217">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-2217">Resource</span></span>

* <span data-ttu-id="f6344-2218">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="f6344-2218">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="f6344-2219">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="f6344-2219">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="f6344-2220">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="f6344-2220">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="f6344-2221">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="f6344-2221">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-2222">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-2222">SQL</span></span>

* <span data-ttu-id="f6344-2223">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2223">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-2224">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-2224">VM</span></span>

* <span data-ttu-id="f6344-2225">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="f6344-2225">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="f6344-2226">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="f6344-2226">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="f6344-2227">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2227">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="f6344-2228">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="f6344-2228">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="f6344-2229">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="f6344-2229">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="f6344-2230">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="f6344-2230">August 31, 2017</span></span>

<span data-ttu-id="f6344-2231">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="f6344-2231">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="f6344-2232">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f6344-2232">Keyvault</span></span>

* <span data-ttu-id="f6344-2233">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2233">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="f6344-2234">SF</span><span class="sxs-lookup"><span data-stu-id="f6344-2234">Sf</span></span>

* <span data-ttu-id="f6344-2235">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="f6344-2235">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-2236">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-2236">Storage</span></span>

* <span data-ttu-id="f6344-2237">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2237">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="f6344-2238">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="f6344-2238">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="f6344-2239">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="f6344-2239">August 28, 2017</span></span>

<span data-ttu-id="f6344-2240">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="f6344-2240">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="f6344-2241">CLI</span><span class="sxs-lookup"><span data-stu-id="f6344-2241">CLI</span></span>

* <span data-ttu-id="f6344-2242">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2242">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-2243">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-2243">ACS</span></span>

* <span data-ttu-id="f6344-2244">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2244">Corrected preview regions</span></span>
* <span data-ttu-id="f6344-2245">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-2245">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="f6344-2246">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2246">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-2247">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-2247">Appservice</span></span>

* <span data-ttu-id="f6344-2248">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2248">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="f6344-2249">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2249">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="f6344-2250">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2250">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="f6344-2251">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2251">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="f6344-2252">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="f6344-2252">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="f6344-2253">IoT</span><span class="sxs-lookup"><span data-stu-id="f6344-2253">IoT</span></span>

* <span data-ttu-id="f6344-2254">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2254">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="f6344-2255">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-2255">Network</span></span>

* <span data-ttu-id="f6344-2256">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2256">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="f6344-2257">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2257">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="f6344-2258">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2258">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="f6344-2259">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2259">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="f6344-2260">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2260">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="f6344-2261">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-2261">Profile</span></span>

* <span data-ttu-id="f6344-2262">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2262">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="f6344-2263">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="f6344-2263">Service Fabric</span></span>

* <span data-ttu-id="f6344-2264">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="f6344-2264">Preview release</span></span>
* <span data-ttu-id="f6344-2265">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2265">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="f6344-2266">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2266">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="f6344-2267">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2267">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-2268">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-2268">Storage</span></span>

* <span data-ttu-id="f6344-2269">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-2269">Enabled setting blob tier</span></span>
* <span data-ttu-id="f6344-2270">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2270">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="f6344-2271">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2271">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="f6344-2272">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-2272">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="f6344-2273">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2273">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="f6344-2274">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="f6344-2274">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-2275">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-2275">VM</span></span>

* <span data-ttu-id="f6344-2276">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2276">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="f6344-2277">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-2277">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="f6344-2278">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2278">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="f6344-2279">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2279">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="f6344-2280">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2280">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="f6344-2281">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2281">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="f6344-2282">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="f6344-2282">August 15, 2017</span></span>

<span data-ttu-id="f6344-2283">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="f6344-2283">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-2284">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-2284">ACS</span></span>

* <span data-ttu-id="f6344-2285">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2285">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-2286">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-2286">Appservice</span></span>

* <span data-ttu-id="f6344-2287">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2287">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="f6344-2288">Event Grid</span><span class="sxs-lookup"><span data-stu-id="f6344-2288">Event Grid</span></span>

* <span data-ttu-id="f6344-2289">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2289">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="f6344-2290">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="f6344-2290">August 11, 2017</span></span>

<span data-ttu-id="f6344-2291">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="f6344-2291">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-2292">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-2292">ACS</span></span>

* <span data-ttu-id="f6344-2293">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2293">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-2294">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-2294">Batch</span></span>

* <span data-ttu-id="f6344-2295">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2295">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="f6344-2296">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2296">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="f6344-2297">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2297">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="f6344-2298">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2298">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="f6344-2299">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2299">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="f6344-2300">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2300">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="f6344-2301">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f6344-2301">Component</span></span>

* <span data-ttu-id="f6344-2302">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2302">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="f6344-2303">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f6344-2303">Container</span></span>

* <span data-ttu-id="f6344-2304">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2304">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="f6344-2305">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="f6344-2305">Data Lake Store</span></span>

* <span data-ttu-id="f6344-2306">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-2306">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="f6344-2307">Event Grid</span><span class="sxs-lookup"><span data-stu-id="f6344-2307">Event Grid</span></span>

* <span data-ttu-id="f6344-2308">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f6344-2308">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="f6344-2309">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-2309">Network</span></span>

* <span data-ttu-id="f6344-2310">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2310">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="f6344-2311">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2311">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="f6344-2312">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2312">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="f6344-2313">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2313">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="f6344-2314">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-2314">Profile</span></span>

* <span data-ttu-id="f6344-2315">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2315">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-2316">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-2316">Storage</span></span>

* <span data-ttu-id="f6344-2317">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="f6344-2317">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-2318">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-2318">VM</span></span>

* <span data-ttu-id="f6344-2319">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2319">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="f6344-2320">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2320">Exposed `list-skus` command</span></span>
* <span data-ttu-id="f6344-2321">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2321">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="f6344-2322">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="f6344-2322">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="f6344-2323">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2323">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="f6344-2324">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="f6344-2324">July 28, 2017</span></span>

<span data-ttu-id="f6344-2325">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="f6344-2325">Version 2.0.12</span></span>

* <span data-ttu-id="f6344-2326">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2326">Added container commands</span></span>
* <span data-ttu-id="f6344-2327">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2327">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="f6344-2328">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-2328">Core</span></span>

* <span data-ttu-id="f6344-2329">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="f6344-2329">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="f6344-2330">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2330">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="f6344-2331">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="f6344-2331">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="f6344-2332">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="f6344-2332">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="f6344-2333">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="f6344-2333">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="f6344-2334">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="f6344-2334">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="f6344-2335">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="f6344-2335">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="f6344-2336">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="f6344-2336">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="f6344-2337">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="f6344-2337">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="f6344-2338">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="f6344-2338">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="f6344-2339">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="f6344-2339">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="f6344-2340">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="f6344-2340">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="f6344-2341">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2341">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="f6344-2342">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2342">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="f6344-2343">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2343">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="f6344-2344">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="f6344-2344">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="f6344-2345">ACR</span><span class="sxs-lookup"><span data-stu-id="f6344-2345">ACR</span></span>

* <span data-ttu-id="f6344-2346">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2346">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="f6344-2347">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2347">Support SKU update for managed registries</span></span>
* <span data-ttu-id="f6344-2348">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2348">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="f6344-2349">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2349">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="f6344-2350">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2350">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="f6344-2351">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2351">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-2352">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-2352">ACS</span></span>

* <span data-ttu-id="f6344-2353">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2353">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-2354">Appservice</span><span class="sxs-lookup"><span data-stu-id="f6344-2354">Appservice</span></span>

* <span data-ttu-id="f6344-2355">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2355">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="f6344-2356">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2356">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="f6344-2357">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="f6344-2357">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="f6344-2358">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="f6344-2358">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="f6344-2359">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="f6344-2359">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="f6344-2360">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="f6344-2360">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="f6344-2361">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="f6344-2361">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="f6344-2362">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="f6344-2362">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="f6344-2363">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-2363">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="f6344-2364">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="f6344-2364">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="f6344-2365">Batch</span><span class="sxs-lookup"><span data-stu-id="f6344-2365">Batch</span></span>

* <span data-ttu-id="f6344-2366">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="f6344-2366">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="f6344-2367">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2367">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="f6344-2368">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2368">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="f6344-2369">CDN</span><span class="sxs-lookup"><span data-stu-id="f6344-2369">CDN</span></span>

* <span data-ttu-id="f6344-2370">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2370">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="f6344-2371">クラウド</span><span class="sxs-lookup"><span data-stu-id="f6344-2371">Cloud</span></span>

* <span data-ttu-id="f6344-2372">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2372">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="f6344-2373">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="f6344-2373">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="f6344-2374">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2374">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="f6344-2375">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2375">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="f6344-2376">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2376">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f6344-2377">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f6344-2377">CosmosDB</span></span>

* <span data-ttu-id="f6344-2378">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2378">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="f6344-2379">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2379">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="f6344-2380">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="f6344-2380">Data Lake Analytics</span></span>

* <span data-ttu-id="f6344-2381">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2381">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="f6344-2382">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2382">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="f6344-2383">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2383">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="f6344-2384">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="f6344-2384">Data Lake Store</span></span>

* <span data-ttu-id="f6344-2385">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2385">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="f6344-2386">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2386">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="f6344-2387">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-2387">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="f6344-2388">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="f6344-2388">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="f6344-2389">対話</span><span class="sxs-lookup"><span data-stu-id="f6344-2389">Interactive</span></span>

* <span data-ttu-id="f6344-2390">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2390">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="f6344-2391">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="f6344-2391">Increased test coverage</span></span>
* <span data-ttu-id="f6344-2392">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2392">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="f6344-2393">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="f6344-2393">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="f6344-2394">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="f6344-2394">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="f6344-2395">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="f6344-2395">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="f6344-2396">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="f6344-2396">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="f6344-2397">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2397">Added `--progress` flag</span></span>
* <span data-ttu-id="f6344-2398">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2398">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="f6344-2399">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="f6344-2399">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="f6344-2400">IoT</span><span class="sxs-lookup"><span data-stu-id="f6344-2400">IoT</span></span>

* <span data-ttu-id="f6344-2401">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-2401">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="f6344-2402">(#3934)</span><span class="sxs-lookup"><span data-stu-id="f6344-2402">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="f6344-2403">Key Vault</span><span class="sxs-lookup"><span data-stu-id="f6344-2403">Key vault</span></span>

* <span data-ttu-id="f6344-2404">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-2404">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="f6344-2405">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="f6344-2405">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="f6344-2406">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="f6344-2406">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="f6344-2407">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="f6344-2407">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="f6344-2408">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="f6344-2408">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="f6344-2409">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="f6344-2409">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="f6344-2410">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-2410">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="f6344-2411">(#3307)</span><span class="sxs-lookup"><span data-stu-id="f6344-2411">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="f6344-2412">ラボ</span><span class="sxs-lookup"><span data-stu-id="f6344-2412">Lab</span></span>

* <span data-ttu-id="f6344-2413">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2413">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="f6344-2414">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2414">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-2415">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-2415">Monitor</span></span>

* <span data-ttu-id="f6344-2416">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="f6344-2416">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="f6344-2417">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2417">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="f6344-2418">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2418">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="f6344-2419">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2419">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="f6344-2420">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2420">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="f6344-2421">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="f6344-2421">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="f6344-2422">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2422">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="f6344-2423">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="f6344-2423">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="f6344-2424">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2424">`location` no longer required</span></span>
  * <span data-ttu-id="f6344-2425">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="f6344-2425">Add name and ID support for target</span></span>
  * <span data-ttu-id="f6344-2426">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="f6344-2426">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="f6344-2427">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-2427">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="f6344-2428">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2428">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="f6344-2429">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="f6344-2429">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="f6344-2430">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2430">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="f6344-2431">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2431">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="f6344-2432">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-2432">Network</span></span>

* <span data-ttu-id="f6344-2433">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2433">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="f6344-2434">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2434">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="f6344-2435">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2435">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="f6344-2436">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2436">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="f6344-2437">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2437">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="f6344-2438">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2438">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="f6344-2439">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2439">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="f6344-2440">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2440">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="f6344-2441">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2441">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="f6344-2442">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2442">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="f6344-2443">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2443">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="f6344-2444">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2444">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="f6344-2445">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2445">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="f6344-2446">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2446">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="f6344-2447">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2447">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="f6344-2448">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2448">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="f6344-2449">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2449">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="f6344-2450">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2450">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="f6344-2451">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2451">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="f6344-2452">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2452">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="f6344-2453">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2453">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="f6344-2454">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2454">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="f6344-2455">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2455">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="f6344-2456">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="f6344-2456">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="f6344-2457">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="f6344-2457">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="f6344-2458">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="f6344-2458">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="f6344-2459">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="f6344-2459">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="f6344-2460">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-2460">Profile</span></span>

* <span data-ttu-id="f6344-2461">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2461">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="f6344-2462">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2462">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="f6344-2463">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="f6344-2463">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="f6344-2464">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2464">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="f6344-2465">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2465">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="f6344-2466">RDBMS</span><span class="sxs-lookup"><span data-stu-id="f6344-2466">RDBMS</span></span>

* <span data-ttu-id="f6344-2467">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="f6344-2467">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="f6344-2468">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="f6344-2468">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="f6344-2469">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="f6344-2469">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="f6344-2470">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="f6344-2470">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-2471">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-2471">Resource</span></span>

* <span data-ttu-id="f6344-2472">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2472">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="f6344-2473">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2473">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="f6344-2474">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2474">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="f6344-2475">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2475">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="f6344-2476">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="f6344-2476">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="f6344-2477">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2477">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="f6344-2478">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="f6344-2478">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="f6344-2479">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2479">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="f6344-2480">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-2480">Role</span></span>

* <span data-ttu-id="f6344-2481">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2481">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="f6344-2482">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="f6344-2482">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="f6344-2483">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="f6344-2483">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="f6344-2484">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="f6344-2484">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="f6344-2485">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2485">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="f6344-2486">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="f6344-2486">Service Fabric</span></span>
* <span data-ttu-id="f6344-2487">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="f6344-2487">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="f6344-2488">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="f6344-2488">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="f6344-2489">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="f6344-2489">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-2490">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-2490">SQL</span></span>

* <span data-ttu-id="f6344-2491">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2491">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="f6344-2492">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2492">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="f6344-2493">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2493">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-2494">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-2494">Storage</span></span>

* <span data-ttu-id="f6344-2495">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="f6344-2495">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="f6344-2496">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-2496">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="f6344-2497">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="f6344-2497">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="f6344-2498">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="f6344-2498">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="f6344-2499">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="f6344-2499">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="f6344-2500">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="f6344-2500">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-2501">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-2501">VM</span></span>

* <span data-ttu-id="f6344-2502">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2502">Support configuring nsg</span></span>
* <span data-ttu-id="f6344-2503">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2503">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="f6344-2504">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="f6344-2504">Support managed service identities</span></span>
* <span data-ttu-id="f6344-2505">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2505">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="f6344-2506">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="f6344-2506">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="f6344-2507">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="f6344-2507">May 10, 2017</span></span>

<span data-ttu-id="f6344-2508">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="f6344-2508">Version 2.0.6</span></span>

* <span data-ttu-id="f6344-2509">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2509">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="f6344-2510">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2510">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="f6344-2511">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2511">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="f6344-2512">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2512">Include Cognitive Services module</span></span>
* <span data-ttu-id="f6344-2513">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2513">Include Service Fabric module</span></span>
* <span data-ttu-id="f6344-2514">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="f6344-2514">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="f6344-2515">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2515">Add support for CDN commands</span></span>
* <span data-ttu-id="f6344-2516">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2516">Remove Container module</span></span>
* <span data-ttu-id="f6344-2517">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="f6344-2517">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="f6344-2518">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="f6344-2518">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="f6344-2519">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-2519">Core</span></span>

* <span data-ttu-id="f6344-2520">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="f6344-2520">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="f6344-2521">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="f6344-2521">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="f6344-2522">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="f6344-2522">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="f6344-2523">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="f6344-2523">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="f6344-2524">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="f6344-2524">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="f6344-2525">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="f6344-2525">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="f6344-2526">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="f6344-2526">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="f6344-2527">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="f6344-2527">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="f6344-2528">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="f6344-2528">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="f6344-2529">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="f6344-2529">core: Improved performance</span></span>
* <span data-ttu-id="f6344-2530">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="f6344-2530">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="f6344-2531">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="f6344-2531">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-2532">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-2532">ACS</span></span>

* <span data-ttu-id="f6344-2533">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2533">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="f6344-2534">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2534">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="f6344-2535">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2535">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="f6344-2536">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="f6344-2536">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-2537">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-2537">AppService</span></span>

* <span data-ttu-id="f6344-2538">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2538">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="f6344-2539">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2539">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="f6344-2540">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="f6344-2540">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="f6344-2541">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2541">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="f6344-2542">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2542">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="f6344-2543">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="f6344-2543">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="f6344-2544">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="f6344-2544">support slot swap with preview</span></span>
* <span data-ttu-id="f6344-2545">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="f6344-2545">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="f6344-2546">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="f6344-2546">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="f6344-2547">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="f6344-2547">CosmosDB</span></span>

* <span data-ttu-id="f6344-2548">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2548">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="f6344-2549">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2549">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="f6344-2550">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2550">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="f6344-2551">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2551">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="f6344-2552">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="f6344-2552">Data Lake Analytics</span></span>

* <span data-ttu-id="f6344-2553">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2553">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="f6344-2554">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="f6344-2554">Add support for new catalog item type: package.</span></span> <span data-ttu-id="f6344-2555">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="f6344-2555">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="f6344-2556">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="f6344-2556">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="f6344-2557">テーブル</span><span class="sxs-lookup"><span data-stu-id="f6344-2557">Table</span></span>
  * <span data-ttu-id="f6344-2558">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="f6344-2558">Table valued function</span></span>
  * <span data-ttu-id="f6344-2559">表示</span><span class="sxs-lookup"><span data-stu-id="f6344-2559">View</span></span>
  * <span data-ttu-id="f6344-2560">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="f6344-2560">Table Statistics.</span></span> <span data-ttu-id="f6344-2561">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="f6344-2561">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="f6344-2562">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="f6344-2562">Data Lake Store</span></span>

* <span data-ttu-id="f6344-2563">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2563">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="f6344-2564">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="f6344-2564">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="f6344-2565">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="f6344-2565">missed help for access show.</span></span> <span data-ttu-id="f6344-2566">追加しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2566">adding it.</span></span> <span data-ttu-id="f6344-2567">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="f6344-2567">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="f6344-2568">検索</span><span class="sxs-lookup"><span data-stu-id="f6344-2568">Find</span></span>

* <span data-ttu-id="f6344-2569">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="f6344-2569">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="f6344-2570">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f6344-2570">KeyVault</span></span>

* <span data-ttu-id="f6344-2571">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2571">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="f6344-2572">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2572">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="f6344-2573">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="f6344-2573">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="f6344-2574">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2574">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="f6344-2575">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="f6344-2575">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="f6344-2576">ラボ</span><span class="sxs-lookup"><span data-stu-id="f6344-2576">Lab</span></span>

* <span data-ttu-id="f6344-2577">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2577">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="f6344-2578">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2578">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="f6344-2579">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2579">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="f6344-2580">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2580">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="f6344-2581">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2581">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="f6344-2582">監視</span><span class="sxs-lookup"><span data-stu-id="f6344-2582">Monitor</span></span>

* <span data-ttu-id="f6344-2583">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="f6344-2583">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="f6344-2584">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="f6344-2584">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="f6344-2585">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-2585">Network</span></span>

* <span data-ttu-id="f6344-2586">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2586">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="f6344-2587">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2587">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="f6344-2588">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2588">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="f6344-2589">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2589">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="f6344-2590">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2590">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="f6344-2591">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2591">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="f6344-2592">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2592">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="f6344-2593">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2593">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="f6344-2594">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2594">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="f6344-2595">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2595">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="f6344-2596">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2596">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="f6344-2597">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2597">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="f6344-2598">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2598">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="f6344-2599">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2599">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="f6344-2600">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="f6344-2600">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="f6344-2601">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2601">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="f6344-2602">プロファイル</span><span class="sxs-lookup"><span data-stu-id="f6344-2602">Profile</span></span>

* <span data-ttu-id="f6344-2603">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="f6344-2603">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="f6344-2604">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="f6344-2604">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="f6344-2605">Redis</span><span class="sxs-lookup"><span data-stu-id="f6344-2605">Redis</span></span>

* <span data-ttu-id="f6344-2606">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2606">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="f6344-2607">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2607">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="f6344-2608">Resource</span><span class="sxs-lookup"><span data-stu-id="f6344-2608">Resource</span></span>

* <span data-ttu-id="f6344-2609">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="f6344-2609">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="f6344-2610">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="f6344-2610">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="f6344-2611">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="f6344-2611">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="f6344-2612">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2612">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="f6344-2613">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="f6344-2613">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="f6344-2614">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2614">Add docs for az lock update.</span></span> <span data-ttu-id="f6344-2615">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="f6344-2615">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="f6344-2616">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="f6344-2616">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="f6344-2617">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="f6344-2617">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="f6344-2618">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="f6344-2618">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="f6344-2619">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="f6344-2619">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="f6344-2620">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="f6344-2620">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="f6344-2621">Role</span><span class="sxs-lookup"><span data-stu-id="f6344-2621">Role</span></span>

* <span data-ttu-id="f6344-2622">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="f6344-2622">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="f6344-2623">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="f6344-2623">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="f6344-2624">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="f6344-2624">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="f6344-2625">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="f6344-2625">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="f6344-2626">SQL</span><span class="sxs-lookup"><span data-stu-id="f6344-2626">SQL</span></span>

* <span data-ttu-id="f6344-2627">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="f6344-2627">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="f6344-2628">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="f6344-2628">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="f6344-2629">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-2629">Storage</span></span>

* <span data-ttu-id="f6344-2630">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="f6344-2630">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="f6344-2631">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2631">Add support for incremental blob copy</span></span>
* <span data-ttu-id="f6344-2632">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2632">Add support for large block blob upload</span></span>
* <span data-ttu-id="f6344-2633">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="f6344-2633">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-2634">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-2634">VM</span></span>

* <span data-ttu-id="f6344-2635">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="f6344-2635">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="f6344-2636">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="f6344-2636">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="f6344-2637">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="f6344-2637">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="f6344-2638">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="f6344-2638">az vm/vmss disk</span></span>
  3. <span data-ttu-id="f6344-2639">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="f6344-2639">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="f6344-2640">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="f6344-2640">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="f6344-2641">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="f6344-2641">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="f6344-2642">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="f6344-2642">April 3, 2017</span></span>

<span data-ttu-id="f6344-2643">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="f6344-2643">Version 2.0.2</span></span>

<span data-ttu-id="f6344-2644">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="f6344-2644">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="f6344-2645">コア</span><span class="sxs-lookup"><span data-stu-id="f6344-2645">Core</span></span>

* <span data-ttu-id="f6344-2646">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="f6344-2646">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="f6344-2647">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="f6344-2647">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="f6344-2648">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="f6344-2648">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="f6344-2649">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="f6344-2649">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="f6344-2650">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="f6344-2650">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="f6344-2651">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="f6344-2651">Add prompting for missing template parameters.</span></span> <span data-ttu-id="f6344-2652">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="f6344-2652">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="f6344-2653">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="f6344-2653">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="f6344-2654">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="f6344-2654">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="f6344-2655">ACS</span><span class="sxs-lookup"><span data-stu-id="f6344-2655">ACS</span></span>

* <span data-ttu-id="f6344-2656">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="f6344-2656">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="f6344-2657">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="f6344-2657">Add support for ssh key password prompting.</span></span> <span data-ttu-id="f6344-2658">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="f6344-2658">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="f6344-2659">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="f6344-2659">Add support for windows clusters.</span></span> <span data-ttu-id="f6344-2660">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="f6344-2660">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="f6344-2661">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="f6344-2661">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="f6344-2662">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="f6344-2662">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="f6344-2663">AppService</span><span class="sxs-lookup"><span data-stu-id="f6344-2663">AppService</span></span>

* <span data-ttu-id="f6344-2664">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="f6344-2664">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="f6344-2665">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="f6344-2665">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="f6344-2666">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="f6344-2666">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="f6344-2667">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="f6344-2667">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="f6344-2668">DataLake</span><span class="sxs-lookup"><span data-stu-id="f6344-2668">DataLake</span></span>

* <span data-ttu-id="f6344-2669">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f6344-2669">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="f6344-2670">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="f6344-2670">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="f6344-2671">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="f6344-2671">DocuemntDB</span></span>

* <span data-ttu-id="f6344-2672">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="f6344-2672">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="f6344-2673">VM</span><span class="sxs-lookup"><span data-stu-id="f6344-2673">VM</span></span>

* <span data-ttu-id="f6344-2674">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="f6344-2674">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="f6344-2675">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="f6344-2675">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="f6344-2676">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="f6344-2676">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="f6344-2677">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="f6344-2677">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="f6344-2678">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="f6344-2678">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="f6344-2679">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="f6344-2679">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="f6344-2680">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="f6344-2680">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="f6344-2681">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="f6344-2681">February 27, 2017</span></span>

<span data-ttu-id="f6344-2682">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="f6344-2682">Version 2.0.0</span></span>

<span data-ttu-id="f6344-2683">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="f6344-2683">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="f6344-2684">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="f6344-2684">Container Service (acs)</span></span>
- <span data-ttu-id="f6344-2685">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="f6344-2685">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="f6344-2686">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="f6344-2686">Networking</span></span>
- <span data-ttu-id="f6344-2687">Storage</span><span class="sxs-lookup"><span data-stu-id="f6344-2687">Storage</span></span>

<span data-ttu-id="f6344-2688">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="f6344-2688">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="f6344-2689">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="f6344-2689">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="f6344-2690">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="f6344-2690">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="f6344-2691">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="f6344-2691">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="f6344-2692">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="f6344-2692">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="f6344-2693">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="f6344-2693">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="f6344-2694">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="f6344-2694">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="f6344-2695">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="f6344-2695">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="f6344-2696">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="f6344-2696">Provide feedback from the command line with the `az feedback` command</span></span>

