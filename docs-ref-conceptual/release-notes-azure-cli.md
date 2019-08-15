---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 08/13/2019
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: d315046287a552e89112fa415e1219f9a97d4944
ms.sourcegitcommit: b00555c528697c0a6419cf23380e48c8705026db
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "68974274"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="d2504-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="d2504-103">Azure CLI release notes</span></span>

## <a name="august-13-2019"></a><span data-ttu-id="d2504-104">2019 年 8 月 13 日</span><span class="sxs-lookup"><span data-stu-id="d2504-104">August 13, 2019</span></span>

<span data-ttu-id="d2504-105">バージョン 2.0.71</span><span class="sxs-lookup"><span data-stu-id="d2504-105">Version 2.0.71</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-106">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-106">AppService</span></span>

* <span data-ttu-id="d2504-107">`webapp webjob continuous` コマンドがスロットで失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-107">Fixed issue where `webapp webjob continuous` commands were failing for slots</span></span>

### <a name="botservice"></a><span data-ttu-id="d2504-108">BotService</span><span class="sxs-lookup"><span data-stu-id="d2504-108">BotService</span></span>

* <span data-ttu-id="d2504-109">[重大な変更] v3 SDK ボットの作成のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-109">[BREAKING CHANGE] Removed support for creating v3 SDK bots</span></span>

### <a name="cognitiveservices"></a><span data-ttu-id="d2504-110">CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d2504-110">CognitiveServices</span></span>

* <span data-ttu-id="d2504-111">`cognitiveservices account network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-111">Added `cognitiveservices account network-rule` commands</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="d2504-112">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d2504-112">Cosmos DB</span></span>

* <span data-ttu-id="d2504-113">複数の書き込み場所を更新するときの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-113">Removed warning when updating multiple write locations</span></span>
* <span data-ttu-id="d2504-114">CosmosDB SQL、MongoDB、Cassandra、Gremlin、およびテーブル リソースとリソースのスループットのための CRUD コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-114">Added CRUD commands for CosmosDB SQL, MongoDB, Cassandra, Gremlin and Table resources and resource's throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="d2504-115">HDInsight</span><span class="sxs-lookup"><span data-stu-id="d2504-115">HDInsight</span></span>

<span data-ttu-id="d2504-116">このリリースには、多数の破壊的変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d2504-116">This release contains a large number of breaking changes.</span></span>

* <span data-ttu-id="d2504-117">[重大な変更] `hdinsight create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-117">[BREAKING CHANGE] Renamed parameters for `hdinsight create`:</span></span>
  * <span data-ttu-id="d2504-118">`--storage-default-container` の名前を `--storage-container` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-118">Renamed `--storage-default-container` to `--storage-container`</span></span>
  * <span data-ttu-id="d2504-119">`--storage-default-filesystem` の名前を `--storage-filesystem` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-119">Renamed `--storage-default-filesystem` to `--storage-filesystem`</span></span>
* <span data-ttu-id="d2504-120">[重大な変更] `application create` の `--name` 引数が、クラスター名の代わりにアプリケーション名を表すように変更されました</span><span class="sxs-lookup"><span data-stu-id="d2504-120">[BREAKING CHANGE] Changed the `--name` argument of `application create` to represent the application name instead of the cluster name</span></span>
* <span data-ttu-id="d2504-121">`--cluster-name` 引数が `application create` に追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="d2504-121">Added `--cluster-name` argument to `application create` to replace old `--name` functionality</span></span>
* <span data-ttu-id="d2504-122">[重大な変更] `application create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-122">[BREAKING CHANGE] Renamed parameters for `application create`:</span></span>
  * <span data-ttu-id="d2504-123">`--application-type` の名前を `--type` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-123">Renamed `--application-type` to `--type`</span></span>
  * <span data-ttu-id="d2504-124">`--marketplace-identifier` の名前を `--marketplace-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-124">Renamed `--marketplace-identifier` to `--marketplace-id`</span></span>
  * <span data-ttu-id="d2504-125">`--https-endpoint-access-mode` の名前を `--access-mode` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-125">Renamed `--https-endpoint-access-mode` to `--access-mode`</span></span>
  * <span data-ttu-id="d2504-126">`--https-endpoint-destination-port` の名前を `--destination-port` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-126">Renamed  `--https-endpoint-destination-port` to `--destination-port`</span></span>
* <span data-ttu-id="d2504-127">[重大な変更] `application create` のパラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-127">[BREAKING CHANGE] Removed parameters for `application create`:</span></span>
  * `--https-endpoint-location`
  * `--https-endpoint-public-port`
  * `--ssh-endpoint-destination-port`
  * `--ssh-endpoint-location`
  * `--ssh-endpoint-public-port`
* <span data-ttu-id="d2504-128">[破壊的変更] `hdinsight resize`の `--target-instance-count` の名前を `--workernode-count` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-128">[BREAKING CHNAGE] Renamed `--target-instance-count` to `--workernode-count` for `hdinsight resize`</span></span>
* <span data-ttu-id="d2504-129">[重大な変更] `hdinsight script-action` グループのすべてのコマンドが、スクリプト アクションの名前として `--name` パラメーターを使用するように変更されました。</span><span class="sxs-lookup"><span data-stu-id="d2504-129">[BREAKING CHANGE] Changed all commands in the `hdinsight script-action` group to use the `--name` parameter as the name of the script action.</span></span>
* <span data-ttu-id="d2504-130">`--cluster-name` 引数がすべての `hdinsight script-action` コマンドに追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="d2504-130">Added `--cluster-name` argument to all `hdinsight script-action` commands to replace old `--name` functionality</span></span>
* <span data-ttu-id="d2504-131">[重大な変更] すべての `hdinsight script-action` コマンドで `--script-execution-id` の名前を `--execution-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-131">[BREAKING CHANGE] Renamed `--script-execution-id` to `--execution-id` for all `hdinsight script-action` commands</span></span>
* <span data-ttu-id="d2504-132">[重大な変更] 名前を `hdinsight script-action show` から `hdinsight script-action show-execution-details` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-132">[BREAKING CHANGE] Renamed `hdinsight script-action show` to `hdinsight script-action show-execution-details`</span></span>
* <span data-ttu-id="d2504-133">[破壊的変更] `hdinsight script-action execute --roles` に対するパラメーターを、コンマ区切りではなくスペース区切りにしました</span><span class="sxs-lookup"><span data-stu-id="d2504-133">[BREAKING CHNAGE] Changed parameters to `hdinsight script-action execute --roles` to be space-separated instead of comma-separated</span></span>
* <span data-ttu-id="d2504-134">[重大な変更] `hdinsight script-action list`の `--persisted` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-134">[BREAKING CHANGE] Removed the `--persisted` parameter of `hdinsight script-action list`</span></span>
* <span data-ttu-id="d2504-135">ローカル JSON ファイルへのパスまたは JSON 文字列を受け入れるように `hdinsight create --cluster-configurations` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-135">Changed the `hdinsight create --cluster-configurations` parameter to accept a path to a local JSON file or a JSON string</span></span>
* <span data-ttu-id="d2504-136">`hdinsight script-action list-execution-history` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-136">Added command `hdinsight script-action list-execution-history`</span></span>
* <span data-ttu-id="d2504-137">Log Analytics ワークスペース ID またはワークスペース名を受け入れるように `hdinsight monitor enable --workspace` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-137">Changed `hdinsight monitor enable --workspace` to accept a Log Analytics workspace ID or workspace name</span></span>
* <span data-ttu-id="d2504-138">`hdinsight monitor enable --primary-key` 引数を追加しました。これは、ワークスペース ID がパラメーターとして指定されている場合に必要です</span><span class="sxs-lookup"><span data-stu-id="d2504-138">Added the `hdinsight monitor enable --primary-key` argument, which is needed if a workspace ID is provided as the parameter</span></span>
* <span data-ttu-id="d2504-139">例をさらに追加し、ヘルプ メッセージの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-139">Added more examples and updated descriptions for help messages</span></span>

### <a name="interactive"></a><span data-ttu-id="d2504-140">Interactive</span><span class="sxs-lookup"><span data-stu-id="d2504-140">Interactive</span></span>

* <span data-ttu-id="d2504-141">読み込みエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-141">Fixed a loading error</span></span>

### <a name="kubernetes"></a><span data-ttu-id="d2504-142">Kubernetes</span><span class="sxs-lookup"><span data-stu-id="d2504-142">Kubernetes</span></span>

* <span data-ttu-id="d2504-143">ダッシュボードのコンテナー ポートで `https` が使用されている場合に `https` を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-143">Changed to use `https` if dashboard container port is using `https`</span></span>

### <a name="network"></a><span data-ttu-id="d2504-144">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-144">Network</span></span>

* <span data-ttu-id="d2504-145">`--yes` 引数を `network dns record-set cname delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-145">Added `--yes` argument `network dns record-set cname delete`</span></span>

### <a name="profile"></a><span data-ttu-id="d2504-146">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-146">Profile</span></span>

* <span data-ttu-id="d2504-147">リソースのアクセス トークンを取得するための `account get-access-token` に `--resource-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-147">Added `--resource-type` argument to `account get-access-token` to get resource access tokens</span></span>

### <a name="servicefabric"></a><span data-ttu-id="d2504-148">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d2504-148">ServiceFabric</span></span>

* <span data-ttu-id="d2504-149">sf cluster create でサポートされているすべての OS バージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-149">Added all supported os version for sf cluster create</span></span>
* <span data-ttu-id="d2504-150">プライマリ証明書の検証のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-150">Fixed primary certificate validation bug</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-151">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-151">Storage</span></span>

* <span data-ttu-id="d2504-152">`storage copy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-152">Added command `storage copy`</span></span>

## <a name="july-30-2019"></a><span data-ttu-id="d2504-153">2019 年 7 月 30 日</span><span class="sxs-lookup"><span data-stu-id="d2504-153">July 30, 2019</span></span>

<span data-ttu-id="d2504-154">バージョン 2.0.70</span><span class="sxs-lookup"><span data-stu-id="d2504-154">Version 2.0.70</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-155">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-155">ACR</span></span>

* <span data-ttu-id="d2504-156">問題 #9952 (`acr pack build` コマンドでの回帰) を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-156">Fixed issue #9952 (a regression in the `acr pack build` command)</span></span>
* <span data-ttu-id="d2504-157">`acr pack build` の既定のビルダー イメージ名を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-157">Removed the default builder image name in `acr pack build`</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-158">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-158">Appservice</span></span>

* <span data-ttu-id="d2504-159">リソースが見つからない場合にメッセージ表示するように `webapp config ssl` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-159">Changed `webapp config ssl` to show a message if a resource is not found</span></span>
* <span data-ttu-id="d2504-160">`functionapp create` がストレージ アカウントの種類 `Standard_RAGRS` を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-160">Fixed issue where `functionapp create` does not accept `Standard_RAGRS` storage account type</span></span>
* <span data-ttu-id="d2504-161">古いバージョンの python を使用して `webapp up` を実行すると失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-161">Fixed an issue where `webapp up` would fail if run using older versions of python</span></span>

### <a name="network"></a><span data-ttu-id="d2504-162">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-162">Network</span></span>

* <span data-ttu-id="d2504-163">`network nic ip-config add` から無効なパラメーター `--ids` を削除しました (#9861 の修正)</span><span class="sxs-lookup"><span data-stu-id="d2504-163">Removed invalid parameter `--ids` from `network nic ip-config add` (fixes #9861)</span></span>
* <span data-ttu-id="d2504-164">#9604 を修正しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-164">Fixes #9604.</span></span> <span data-ttu-id="d2504-165">信頼されたルート証明書へのユーザーの関連付けをサポートするために、`network application-gateway http-settings [create|update]` に `--root-certs` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-165">Added `--root-certs` parameter to `network application-gateway http-settings [create|update]` to support user associate trusted root certificates.</span></span>
* <span data-ttu-id="d2504-166">`network dns record-set ns create` の引数 `--subscription` を修正しました (#9965)</span><span class="sxs-lookup"><span data-stu-id="d2504-166">Fixed arguent `--subscription` for `network dns record-set ns create` (#9965)</span></span>

### <a name="rbac"></a><span data-ttu-id="d2504-167">RBAC</span><span class="sxs-lookup"><span data-stu-id="d2504-167">RBAC</span></span>

* <span data-ttu-id="d2504-168">`user update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-168">Added `user update` command</span></span>
* <span data-ttu-id="d2504-169">[非推奨] ユーザー関連コマンドで `--upn-or-object-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-169">[DEPRECATED] Deprecated `--upn-or-object-id` from user-related commands</span></span>
    * <span data-ttu-id="d2504-170">代替引数の `--id` を使用してください</span><span class="sxs-lookup"><span data-stu-id="d2504-170">Use replacement argument `--id`</span></span>
* <span data-ttu-id="d2504-171">ユーザー関連コマンドに `--id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-171">Added `--id` argument to user-related commands</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-172">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-172">SQL</span></span>

* <span data-ttu-id="d2504-173">マネージド インスタンス キーおよび TDE 保護機能の管理コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-173">Added management commands for managed instance keys and TDE protector</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-174">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-174">Storage</span></span>

* <span data-ttu-id="d2504-175">`storage remove` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-175">Added `storage remove` command</span></span>
* <span data-ttu-id="d2504-176">`storage blob update` での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-176">Fixed an issue with `storage blob update`</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-177">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-177">VM</span></span>

* <span data-ttu-id="d2504-178">ゾーンの詳細を出力するための新しい API バージョンを使用するように `list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-178">Changed `list-skus` to use newer api-version to output zone details</span></span>
* <span data-ttu-id="d2504-179">`vmss create` の `--single-placement-group` の既定値を`false` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-179">Changed default of `--single-placement-group` to `false` for `vmss create`</span></span>
* <span data-ttu-id="d2504-180">`[snapshot|disk] create` において ZRS ストレージ SKU を選択する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-180">Added ability to select ZRS storage SKUs for `[snapshot|disk] create`</span></span>
* <span data-ttu-id="d2504-181">専用ホストをサポートするために、新しいコマンド グループ `vm host` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-181">Added new command group `vm host` to support dedicated hosts</span></span>
* <span data-ttu-id="d2504-182">VM 専用ホストを設定するためのパラメーター `--host` と `--host-group` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-182">Added parameters `--host` and `--host-group` on `vm create` to set VM dedicated host</span></span>

## <a name="july-16-2019"></a><span data-ttu-id="d2504-183">2019 年 7 月 16 日</span><span class="sxs-lookup"><span data-stu-id="d2504-183">July 16, 2019</span></span>

<span data-ttu-id="d2504-184">バージョン 2.0.69</span><span class="sxs-lookup"><span data-stu-id="d2504-184">Version 2.0.69</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-185">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-185">Appservice</span></span>

* <span data-ttu-id="d2504-186">ResourceGroupName または App の名前が無効な場合に適切なエラー メッセージを返すように `webapp identity` コマンドが変更されました</span><span class="sxs-lookup"><span data-stu-id="d2504-186">Changed `webapp identity` commands to return a proper error message if ResourceGroupName or App name are invalid</span></span>
* <span data-ttu-id="d2504-187">ResourceGroup が指定されなかった場合に numberOfSites の正しい値を返すように `webapp list` が修正されました</span><span class="sxs-lookup"><span data-stu-id="d2504-187">Fixed `webapp list` to return the correct value for numberOfSites if no ResourceGroup was provided</span></span>
* <span data-ttu-id="d2504-188">`appservice plan create` と `webapp create` の副作用が修正されました</span><span class="sxs-lookup"><span data-stu-id="d2504-188">Fixed side-effects of `appservice plan create` and `webapp create`</span></span>

### <a name="core"></a><span data-ttu-id="d2504-189">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-189">Core</span></span>

* <span data-ttu-id="d2504-190">`--subscription` が適用不可にもかかわらず表示される問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="d2504-190">Fixed issue where `--subscription` would appear despite being not applicable</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-191">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-191">Batch</span></span>

* <span data-ttu-id="d2504-192">[重大な変更] `batch pool node-agent-skus list` が `batch pool supported-images list` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="d2504-192">[BREAKING CHANGE] Replaced `batch pool node-agent-skus list` with `batch pool supported-images list`</span></span>
* <span data-ttu-id="d2504-193">`batch pool create network` の `--json-file` オプションを使用するときに、トラフィックのソース ポートに基づいてプールへのネットワーク アクセスをブロックするセキュリティ規則のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-193">Added support for security rules blocking network access to a pool based on the source port of the traffic when using the `--json-file` option of `batch pool create network`</span></span>
* <span data-ttu-id="d2504-194">`batch task create`の `--json-file` オプションを使用するときに、コンテナーの作業ディレクトリまたは Batch タスクの作業ディレクトリでタスクを実行するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-194">Added support for executing the task in the container working directory or in the Batch task working directory when using the `--json-file` option of `batch task create`</span></span>
* <span data-ttu-id="d2504-195">`batch pool create`の `--application-package-references` オプションが、既定値でのみ動作するというエラーが修正されました</span><span class="sxs-lookup"><span data-stu-id="d2504-195">Fixed error in `--application-package-references` option of `batch pool create` where it would only work with defaults</span></span>

### <a name="eventhubs"></a><span data-ttu-id="d2504-196">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="d2504-196">Eventhubs</span></span>

* <span data-ttu-id="d2504-197">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-197">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="rdbms"></a><span data-ttu-id="d2504-198">RDBMS</span><span class="sxs-lookup"><span data-stu-id="d2504-198">RDBMS</span></span>

* <span data-ttu-id="d2504-199">レプリカ作成コマンドでレプリカ SKU を指定するためのオプション パラメーターが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-199">Added optional parameter to specify replica SKU for create replica command</span></span>
* <span data-ttu-id="d2504-200">MySQL レプリカの作成で CI テストが失敗する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="d2504-200">Fixed the issue with CI test failure with creating MySQL replica</span></span>

### <a name="relay"></a><span data-ttu-id="d2504-201">リレー</span><span class="sxs-lookup"><span data-stu-id="d2504-201">Relay</span></span>

* <span data-ttu-id="d2504-202">クライアント承認が無効になっているときのハイブリッド接続の問題が修正されました ([#8775](https://github.com/azure/azure-cli/issues/8775))</span><span class="sxs-lookup"><span data-stu-id="d2504-202">Fixed issue with hybrid connection when client authroization disabled [#8775](https://github.com/azure/azure-cli/issues/8775)</span></span>
* <span data-ttu-id="d2504-203">パラメーター `--requires-transport-security` を `relay wcfrelay create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-203">Added parameter `--requires-transport-security` to `relay wcfrelay create`</span></span>

### <a name="servicebus"></a><span data-ttu-id="d2504-204">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d2504-204">Servicebus</span></span>

* <span data-ttu-id="d2504-205">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-205">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-206">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-206">Storage</span></span>

* <span data-ttu-id="d2504-207">ストレージ アカウントの更新で Files AADDS を有効にします</span><span class="sxs-lookup"><span data-stu-id="d2504-207">Enable Files AADDS for storage account update</span></span>
* <span data-ttu-id="d2504-208">修正された問題 `storage blob service-properties update --set`</span><span class="sxs-lookup"><span data-stu-id="d2504-208">Fixed issue `storage blob service-properties update --set`</span></span>

## <a name="july-2-2019"></a><span data-ttu-id="d2504-209">2019 年 7 月 2 日</span><span class="sxs-lookup"><span data-stu-id="d2504-209">July 2, 2019</span></span>

<span data-ttu-id="d2504-210">バージョン 2.0.68</span><span class="sxs-lookup"><span data-stu-id="d2504-210">Version 2.0.68</span></span>

### <a name="core"></a><span data-ttu-id="d2504-211">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-211">Core</span></span>

* <span data-ttu-id="d2504-212">コマンド モジュールが再頒布可能な 1 つの Python コードに統合されました。</span><span class="sxs-lookup"><span data-stu-id="d2504-212">Command modules are now consolidated into a single Python distributable.</span></span> <span data-ttu-id="d2504-213">これにより、PyPI での多くの `azure-cli-` パッケージの直接使用が廃止されます。</span><span class="sxs-lookup"><span data-stu-id="d2504-213">This deprecates direct use of many `azure-cli-` packages on PyPI.</span></span>
  <span data-ttu-id="d2504-214">またこれにより、インストール サイズが削減され、`pip` 経由で直接インストールしたユーザーにのみ影響が出ます。</span><span class="sxs-lookup"><span data-stu-id="d2504-214">This should reduce install size and only affect users who have directly installed via `pip`.</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-215">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-215">ACR</span></span>

* <span data-ttu-id="d2504-216">タスクへのタイマー トリガーのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-216">Added support for Timer Triggers to Task</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-217">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-217">Appservice</span></span>

* <span data-ttu-id="d2504-218">既定でアプリケーション インサイトを有効にするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-218">Changed `functionapp create` to enable application insights by default</span></span>
* <span data-ttu-id="d2504-219">[重大な変更] 非推奨の `functionapp devops-build` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-219">[BREAKING CHANGE] Removed deprecated `functionapp devops-build` command.</span></span>
  *  <span data-ttu-id="d2504-220">代わりに新しいコマンド `az functionapp devops-pipeline` を使用</span><span class="sxs-lookup"><span data-stu-id="d2504-220">Use the new command `az functionapp devops-pipeline` instead</span></span>
* <span data-ttu-id="d2504-221">Linux 従量課金プランの関数アプリのプラン サポートを `functionapp deployment config-zip` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-221">Added Linux Consumption function app plan support to `functionapp deployment config-zip`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="d2504-222">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d2504-222">Cosmos DB</span></span>

* <span data-ttu-id="d2504-223">ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-223">Added support for disabling TTL</span></span>

### <a name="dls"></a><span data-ttu-id="d2504-224">DLS</span><span class="sxs-lookup"><span data-stu-id="d2504-224">DLS</span></span>

* <span data-ttu-id="d2504-225">ADLS バージョンを更新しました (0.0.45)</span><span class="sxs-lookup"><span data-stu-id="d2504-225">Updated ADLS version (0.0.45)</span></span>

### <a name="feedback"></a><span data-ttu-id="d2504-226">フィードバック</span><span class="sxs-lookup"><span data-stu-id="d2504-226">Feedback</span></span>

* <span data-ttu-id="d2504-227">失敗した拡張機能コマンドを報告するときに、`az feedback` はインデックスからの拡張機能のプロジェクト/リポジトリの url にブラウザーを開こうとするようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-227">When reporting a failed extension command, `az feedback` now attempts to open the browser to the project/repo url of the extension from the index</span></span>

### <a name="hdinsight"></a><span data-ttu-id="d2504-228">HDInsight</span><span class="sxs-lookup"><span data-stu-id="d2504-228">HDInsight</span></span>

* <span data-ttu-id="d2504-229">[重大な変更] `oms` コマンド グループ名を `monitor` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-229">[BREAKING CHANGE] Changed `oms` command group name to `monitor`</span></span>
* <span data-ttu-id="d2504-230">[重大な変更] `--http-password/-p` が必須パラメーターになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-230">[BREAKING CHANGE] Made `--http-password/-p` a required parameter</span></span> 
* <span data-ttu-id="d2504-231">`--cluster-admin-account` および `cluster-users-group-dns` パラメーター入力候補の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-231">Added completers for `--cluster-admin-account` and `cluster-users-group-dns` parameters completer</span></span> 
* <span data-ttu-id="d2504-232">`cluster-users-group-dns` パラメーターを `—esp` が存在するときに必要となるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-232">Changed `cluster-users-group-dns` parameter to be required when `—esp` is present</span></span>
* <span data-ttu-id="d2504-233">既存の引数自動オートコンプリートすべてにタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-233">Added a timeout for all existing argument auto-completers</span></span>
* <span data-ttu-id="d2504-234">リソース名をリソース id に変換する際のタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-234">Added a timeout for transforming resource name to resource id</span></span>
* <span data-ttu-id="d2504-235">任意のリソース グループからリソースを選択するようにオートコンプリートを変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-235">Changed Auto-completers to select resources from any resource group.</span></span> <span data-ttu-id="d2504-236">`-g` で指定されるリソース グループとは別のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="d2504-236">It can be a different resource group than the one specified with `-g`</span></span>
* <span data-ttu-id="d2504-237">`hdinsight application create` コマンドで `--sub-domain-suffix` および `--disable_gateway_auth` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-237">Added support for `--sub-domain-suffix` and `--disable_gateway_auth` parameters in the `hdinsight application create` command</span></span>

### <a name="managed-services"></a><span data-ttu-id="d2504-238">マネージド サービス</span><span class="sxs-lookup"><span data-stu-id="d2504-238">Managed Services</span></span>

* <span data-ttu-id="d2504-239">プレビューにマネージド サービス コマンド モジュールを導入</span><span class="sxs-lookup"><span data-stu-id="d2504-239">Introducing managed service command module in preview</span></span>

### <a name="profile"></a><span data-ttu-id="d2504-240">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-240">Profile</span></span>
* <span data-ttu-id="d2504-241">ログアウト コマンドの `--subscription` 引数を抑制</span><span class="sxs-lookup"><span data-stu-id="d2504-241">Suppress `--subscription` argument for logout command</span></span>

### <a name="rbac"></a><span data-ttu-id="d2504-242">RBAC</span><span class="sxs-lookup"><span data-stu-id="d2504-242">RBAC</span></span>

* <span data-ttu-id="d2504-243">[重大な変更] `create-for-rbac` の `--password` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-243">[BREAKING CHANGE] Removed `--password` argument for `create-for-rbac`</span></span>
* <span data-ttu-id="d2504-244">AAD グラフ サーバー レプリケーションの待機時間によって発生する断続的なエラーを回避するために `--assignee-principal-type` パラメーターを `create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-244">Added `--assignee-principal-type` parameter to `create` command to avoid intermittent failures caused by AAD graph server replication latency</span></span>
* <span data-ttu-id="d2504-245">所有オブジェクトの一覧表示時の `ad signed-in-user` のクラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-245">Fixed a crash in `ad signed-in-user` when listing owned objects</span></span>
* <span data-ttu-id="d2504-246">`ad sp` によってサービス プリンシパルから適切なアプリケーションが検出されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-246">Fixed issue where `ad sp` would not find the right application from a service principal</span></span>

### <a name="rdbms"></a><span data-ttu-id="d2504-247">RDBMS</span><span class="sxs-lookup"><span data-stu-id="d2504-247">RDBMS</span></span>

* <span data-ttu-id="d2504-248">MariaDB のレプリケーション サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-248">Added support for replication for MariaDB</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-249">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-249">SQL</span></span>

* <span data-ttu-id="d2504-250">`sql db create --sample-name` に使用できる値を文書化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-250">Documented allowed values for `sql db create --sample-name`</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-251">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-251">Storage</span></span>

* <span data-ttu-id="d2504-252">`--as-user` を使用した `storage blob generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-252">Added user delegation SAS token support with `--as-user` to `storage blob generate-sas`</span></span> 
* <span data-ttu-id="d2504-253">`--as-user` を使用した `storage container generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-253">Added user delegation SAS token support with `--as-user` to `storage container generate-sas`</span></span> 

### <a name="vm"></a><span data-ttu-id="d2504-254">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-254">VM</span></span>

* <span data-ttu-id="d2504-255">`--no-wait` による実行時に `vmss create` によってエラー メッセージが返されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-255">Fixed bug where `vmss create` returns an error message when run with `--no-wait`</span></span>
* <span data-ttu-id="d2504-256">`vmss create --single-placement-group` のクライアント側の検証を削除しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-256">Removed client-side validation for `vmss create --single-placement-group`.</span></span> <span data-ttu-id="d2504-257">`--single-placement-group` が `true` に設定され、`--instance-count` が 100 より大きいか、可用性ゾーンが指定されていても失敗にはならず、この検証はコンピューティング サービスに任されます</span><span class="sxs-lookup"><span data-stu-id="d2504-257">Does not fail if `--single-placement-group` is set to `true` and`--instance-count` is greater than 100 or availability zones are specified, but leaves this validation to the compute service</span></span>
* <span data-ttu-id="d2504-258">`--latest` と共に使用したときに `[vm|vmss] extension image list` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-258">Fixed bug where `[vm|vmss] extension image list` fails when used with `--latest`</span></span>


## <a name="june-18-2019"></a><span data-ttu-id="d2504-259">2019 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="d2504-259">June 18, 2019</span></span>

<span data-ttu-id="d2504-260">バージョン 2.0.67</span><span class="sxs-lookup"><span data-stu-id="d2504-260">Version 2.0.67</span></span>

### <a name="core"></a><span data-ttu-id="d2504-261">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-261">Core</span></span>

<span data-ttu-id="d2504-262">このリリースでは、新しい [プレビュー] タグが導入され、コマンド グループ、コマンド、または引数がプレビュー状態である場合に、お客様により明確に通知できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d2504-262">This release introduces a new [Preview] tag to more clearly communicate to customers when a command group, command or argument is in preview status.</span></span> <span data-ttu-id="d2504-263">以前は、これはヘルプ テキストで通知されていたか、コマンド モジュールのバージョン番号によって暗黙的に通知されていました。</span><span class="sxs-lookup"><span data-stu-id="d2504-263">This was previously called out in help text or communicated implicitly by the command module version number.</span></span>
<span data-ttu-id="d2504-264">CLI では、将来、個々のパッケージのバージョン番号が削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="d2504-264">The CLI will be removing version numbers for individual packages in the future.</span></span> <span data-ttu-id="d2504-265">コマンドがプレビュー状態の場合は、そのすべての引数もプレビュー状態です。</span><span class="sxs-lookup"><span data-stu-id="d2504-265">If a command is in preview, all of its arguments are as well.</span></span> <span data-ttu-id="d2504-266">コマンド グループにプレビュー状態のラベルが付いている場合、すべてのコマンドと引数もプレビュー状態と見なされます。</span><span class="sxs-lookup"><span data-stu-id="d2504-266">If a command group is labeled as being in preview, then all commands and arguments are considered to be in preview as well.</span></span>

<span data-ttu-id="d2504-267">この変更の結果、このリリースでは、一部のコマンド グループが "突然" プレビュー状態になったように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="d2504-267">As a result of this change, several command groups may seem to "suddenly" appear to be in a preview status with this release.</span></span> <span data-ttu-id="d2504-268">ほとんどのパッケージがプレビュー状態にあったのですが、このリリースでは一般提供と見なされていることがその真相です</span><span class="sxs-lookup"><span data-stu-id="d2504-268">What actually happened is that most packages were in a preview status, but are being deemed GA with this release</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-269">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-269">ACR</span></span>
* <span data-ttu-id="d2504-270">'acr check-health' コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-270">Added 'acr check-health' command</span></span>
* <span data-ttu-id="d2504-271">AAD トークンおよび外部コマンドの取得に関するエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-271">Improved error handling for AAD tokens and for retrieving external commands</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-272">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-272">ACS</span></span>
* <span data-ttu-id="d2504-273">非推奨の ACS コマンドがヘルプ ビューで非表示になりました</span><span class="sxs-lookup"><span data-stu-id="d2504-273">Deprecated ACS commands are now hidden from help view</span></span>

### <a name="ams"></a><span data-ttu-id="d2504-274">AMS</span><span class="sxs-lookup"><span data-stu-id="d2504-274">AMS</span></span>
* <span data-ttu-id="d2504-275">[重大な変更] archive-window-length および key-frame-interval-duration の ISO 8601 時間文字列を返すように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-275">[BREAKING CHANGE] Changed to return ISO 8601 time strings for archive-window-length and key-frame-interval-duration</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-276">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-276">AppService</span></span>
* <span data-ttu-id="d2504-277">`webapp deleted list` および `webapp deleted restore` に対してロケーション ベースのルーティングを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-277">Added location based routing for `webapp deleted list` and `webapp deleted restore`</span></span>
* <span data-ttu-id="d2504-278">Azure Cloud Shell で Web アプリのログに記録されたターゲット URL ("You can launch the app at...") がクリックできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-278">Fixed issue where webapp up logged target URL ("You can launch the app at...") was not clickable in Azure Cloud Shell</span></span>
* <span data-ttu-id="d2504-279">一部の SKU でのアプリ作成が AlwaysOn エラーで失敗するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-279">Fixed an issue where creating apps with the some SKUs was failing with an AlwaysOn error</span></span>
* <span data-ttu-id="d2504-280">`[appservice|webapp] create` に事前検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-280">Added pre-validation to `[appservice|webapp] create`</span></span>
* <span data-ttu-id="d2504-281">正しい actionHostName を使用するように `[webapp|functionapp] traffic-routing` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-281">Fixed `[webapp|functionapp] traffic-routing` to use the correct actionHostName</span></span>
* <span data-ttu-id="d2504-282">`functionapp` コマンドにスロット サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-282">Added slot support to `functionapp` commands</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-283">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-283">Batch</span></span>
* <span data-ttu-id="d2504-284">共有キー認証の過度のエラー報告による AAD 認証の回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-284">Fixed AAD auth regression caused by over-aggressive error reporting for Shared Key Auth</span></span>

### <a name="batchai"></a><span data-ttu-id="d2504-285">BatchAI</span><span class="sxs-lookup"><span data-stu-id="d2504-285">BatchAI</span></span>
* <span data-ttu-id="d2504-286">BatchAI コマンドが非推奨となり、非表示になりました</span><span class="sxs-lookup"><span data-stu-id="d2504-286">BatchAI commands are now deprecated and hidden</span></span>

### <a name="botservice"></a><span data-ttu-id="d2504-287">BotService</span><span class="sxs-lookup"><span data-stu-id="d2504-287">BotService</span></span>
* <span data-ttu-id="d2504-288">v3 SDK をサポートするコマンドに "廃止されたサポート"/"保守モード" 警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-288">Added "discontinued support"/"maintenance mode" warning messages for commands that support the v3 SDK</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="d2504-289">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d2504-289">CosmosDB</span></span>
* <span data-ttu-id="d2504-290">[非推奨] `cosmosdb list-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-290">[DEPRECATED] Deprecated the `cosmosdb list-keys` command</span></span>
* <span data-ttu-id="d2504-291">`cosmosdb keys list` コマンドを追加しました。`cosmosdb list-keys` に置き換わるものです</span><span class="sxs-lookup"><span data-stu-id="d2504-291">Added the `cosmosdb keys list` command - replaces `cosmosdb list-keys`</span></span>
* <span data-ttu-id="d2504-292">`cosmsodb create/update`:"isZoneRedundant" プロパティを設定できるように --location の新しいフォーマットを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-292">`cosmsodb create/update`: Added new format for --location to allow setting "isZoneRedundant" property.</span></span> <span data-ttu-id="d2504-293">古いフォーマットを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-293">Deprecated old format</span></span>

### <a name="eventgrid"></a><span data-ttu-id="d2504-294">EventGrid</span><span class="sxs-lookup"><span data-stu-id="d2504-294">EventGrid</span></span>
* <span data-ttu-id="d2504-295">ドメイン CRUD 操作のための `eventgrid domain` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-295">Added `eventgrid domain` commands for domain CRUD operations</span></span>
* <span data-ttu-id="d2504-296">ドメイン トピック CRUD 操作のための `eventgrid domain topic` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-296">Added `eventgrid domain topic` commands for domain topics CRUD operations</span></span>
* <span data-ttu-id="d2504-297">OData 構文を使用して結果をフィルタリングするための `--odata-query` 引数を `eventgrid [topic|event-subscription] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-297">Added `--odata-query` argument to `eventgrid [topic|event-subscription] list` for filtering results using OData syntax</span></span>
* <span data-ttu-id="d2504-298">`event-subscription create/update`:`--endpoint-type` パラメーターの新しい値として servicebusqueue を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-298">`event-subscription create/update`: Added servicebusqueue as new values for the `--endpoint-type` parameter</span></span>
* <span data-ttu-id="d2504-299">[重大な変更] `eventgrid event-subscription [create|update]` での `--included-event-types All` のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-299">[BREAKING CHANGE] Removed support for `--included-event-types All` with `eventgrid event-subscription [create|update]`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="d2504-300">HDInsight</span><span class="sxs-lookup"><span data-stu-id="d2504-300">HDInsight</span></span>
* <span data-ttu-id="d2504-301">`hdinsight create` コマンドでの `--ssh-public-key` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-301">Added support for `--ssh-public-key` parameter in `hdinsight create` command</span></span>

### <a name="iot"></a><span data-ttu-id="d2504-302">IoT</span><span class="sxs-lookup"><span data-stu-id="d2504-302">IoT</span></span>
* <span data-ttu-id="d2504-303">承認ポリシー キーの再生成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-303">Added support to regenerate authorization policy keys</span></span>
* <span data-ttu-id="d2504-304">DigitalTwin リポジトリ プロビジョニング サービスの SDK およびサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-304">Added SDK and support for DigitalTwin Repository Provisioning Service</span></span>

### <a name="network"></a><span data-ttu-id="d2504-305">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-305">Network</span></span>
* <span data-ttu-id="d2504-306">Nat Gateway に対するゾーン サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-306">Added Zone support for Nat Gateway</span></span>
* <span data-ttu-id="d2504-307">`network list-service-tags` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-307">Added command `network list-service-tags`</span></span>
* <span data-ttu-id="d2504-308">ユーザーがワイルドカード A レコードをインポートできない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-308">Fixed issue with `dns zone import` where users could not import wildcard A records</span></span>
* <span data-ttu-id="d2504-309">特定のリージョンでフロー ロギングを有効にできない `watcher flow-log configure` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-309">Fixed issue with `watcher flow-log configure` where flow logging could not be enabled in certain regions</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-310">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-310">Resource</span></span>
* <span data-ttu-id="d2504-311">REST 呼び出しを行うための `az rest` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-311">Added `az rest` command for making REST calls</span></span>
* <span data-ttu-id="d2504-312">リソース グループまたはサブスクリプション レベル`--scope` で `policy assignment list` を使用する場合のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-312">Fixed error when using `policy assignment list` with a resource group or subscription level `--scope`</span></span>

### <a name="servicebus"></a><span data-ttu-id="d2504-313">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d2504-313">ServiceBus</span></span>
* <span data-ttu-id="d2504-314">`servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319) での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-314">Fixed issue with `servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319)</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-315">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-315">SQL</span></span>
* <span data-ttu-id="d2504-316">`--location` を `sql [server|mi] create` のオプションに変更しました - 指定されていない場合、リソース グループの場所を使用します</span><span class="sxs-lookup"><span data-stu-id="d2504-316">Changed `--location` to be optional for `sql [server|mi] create` - uses resource group location if not specified</span></span>
* <span data-ttu-id="d2504-317">`sql db list-editions --available` の "'NoneType' object is not iterable" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-317">Fixed "'NoneType' object is not iterable" error for `sql db list-editions --available`</span></span>

### <a name="sqlvm"></a><span data-ttu-id="d2504-318">SQLVm</span><span class="sxs-lookup"><span data-stu-id="d2504-318">SQLVm</span></span>
* <span data-ttu-id="d2504-319">[破壊的変更] `--license-type` パラメーターを必要とするように `sql vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-319">[BREAKING CHNAGE] Changed `sql vm create` to require `--license-type` parameter</span></span>
* <span data-ttu-id="d2504-320">sql vm の作成または更新時に SQL イメージ SKU を設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-320">Changed to allow setting SQL image SKU when creating or updating a sql vm</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-321">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-321">Storage</span></span>
* <span data-ttu-id="d2504-322">`storage container generate-sas` のアカウント キーが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-322">Fixed issue with missing account key for `storage container generate-sas`</span></span>
* <span data-ttu-id="d2504-323">Linux での `storage blob sync` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-323">Fixed issue with `storage blob sync` on Linux</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-324">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-324">VM</span></span>
* <span data-ttu-id="d2504-325">[プレビュー] VM イメージを構築するための `vm image template` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-325">[PREVIEW] Added `vm image template` commands to build VM images</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="d2504-326">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="d2504-326">June 4, 2019</span></span>

<span data-ttu-id="d2504-327">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="d2504-327">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="d2504-328">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-328">Core</span></span>
* <span data-ttu-id="d2504-329">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-329">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-330">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-330">ACR</span></span>
* <span data-ttu-id="d2504-331">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-331">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-332">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-332">ACS</span></span>
* <span data-ttu-id="d2504-333">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-333">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="d2504-334">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="d2504-334">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-335">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-335">Batch</span></span>
* <span data-ttu-id="d2504-336">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-336">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="d2504-337">IoT</span><span class="sxs-lookup"><span data-stu-id="d2504-337">IoT</span></span>
* <span data-ttu-id="d2504-338">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-338">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="d2504-339">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-339">Network</span></span>
* <span data-ttu-id="d2504-340">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-340">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="d2504-341">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-341">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="d2504-342">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-342">Resource</span></span>
* <span data-ttu-id="d2504-343">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-343">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="d2504-344">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-344">Role</span></span>
* <span data-ttu-id="d2504-345">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-345">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="d2504-346">Compute</span><span class="sxs-lookup"><span data-stu-id="d2504-346">Compute</span></span>
* <span data-ttu-id="d2504-347">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-347">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="d2504-348">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="d2504-348">May 21, 2019</span></span>

<span data-ttu-id="d2504-349">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="d2504-349">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="d2504-350">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-350">Core</span></span>
* <span data-ttu-id="d2504-351">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-351">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="d2504-352">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-352">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="d2504-353">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-353">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-354">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-354">ACR</span></span>
* <span data-ttu-id="d2504-355">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-355">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-356">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-356">ACS</span></span>
* <span data-ttu-id="d2504-357">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-357">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-358">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-358">AppService</span></span>
* <span data-ttu-id="d2504-359">[非推奨] `functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="d2504-359">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="d2504-360">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-360">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="d2504-361">[重大な変更] `--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="d2504-361">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="d2504-362">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-362">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="d2504-363">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-363">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="d2504-364">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-364">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="d2504-365">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-365">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="d2504-366">BotService</span><span class="sxs-lookup"><span data-stu-id="d2504-366">BotService</span></span>
* <span data-ttu-id="d2504-367">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-367">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="d2504-368">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-368">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="d2504-369">消費</span><span class="sxs-lookup"><span data-stu-id="d2504-369">Consumption</span></span>
* <span data-ttu-id="d2504-370">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-370">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="d2504-371">IoT</span><span class="sxs-lookup"><span data-stu-id="d2504-371">IoT</span></span>
* <span data-ttu-id="d2504-372">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-372">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="d2504-373">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-373">Network</span></span>
* [重大な変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="d2504-375">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-375">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="d2504-376">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-376">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="d2504-377">RDBMS</span><span class="sxs-lookup"><span data-stu-id="d2504-377">RDBMS</span></span>
* <span data-ttu-id="d2504-378">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-378">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="d2504-379">RBAC</span><span class="sxs-lookup"><span data-stu-id="d2504-379">RBAC</span></span>
* <span data-ttu-id="d2504-380">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-380">Added support for mangement group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-381">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-381">Storage</span></span>
* <span data-ttu-id="d2504-382">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="d2504-382">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="d2504-383">Compute</span><span class="sxs-lookup"><span data-stu-id="d2504-383">Compute</span></span>
* <span data-ttu-id="d2504-384">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-384">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="d2504-385">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-385">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="d2504-386">__メモ__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="d2504-386">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="d2504-387">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-387">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="d2504-388">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="d2504-388">May 6, 2019</span></span>

<span data-ttu-id="d2504-389">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="d2504-389">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-390">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-390">ACS</span></span>
* <span data-ttu-id="d2504-391">[重大な変更] `--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-391">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="d2504-392">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-392">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="d2504-393">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-393">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="d2504-394">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-394">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-395">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-395">Appservice</span></span>
* <span data-ttu-id="d2504-396">[非推奨] `functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-396">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="d2504-397">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-397">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="d2504-398">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="d2504-398">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="d2504-399">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-399">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="d2504-400">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-400">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="d2504-401">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-401">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="d2504-402">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-402">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="d2504-403">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-403">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="d2504-404">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-404">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="d2504-405">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-405">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-406">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-406">Batch</span></span>
* <span data-ttu-id="d2504-407">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-407">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="d2504-408">Botservice</span><span class="sxs-lookup"><span data-stu-id="d2504-408">Botservice</span></span>
* <span data-ttu-id="d2504-409">[重大な変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="d2504-409">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="d2504-410">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-410">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="d2504-411">[重大な変更] `--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-411">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="d2504-412">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="d2504-412">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="d2504-413">[重大な変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-413">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="d2504-414">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="d2504-414">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="d2504-415">[重大な変更] `bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-415">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="d2504-416">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-416">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="d2504-417">[重大な変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-417">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="d2504-418">[重大な変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-418">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="d2504-419">[重大な変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-419">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="d2504-420">[重大な変更] `Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-420">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="d2504-421">[重大な変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-421">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="d2504-422">[重大な変更] `SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-422">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="d2504-423">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="d2504-423">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="d2504-424">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-424">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="d2504-425">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-425">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="d2504-426">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-426">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="d2504-427">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-427">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="d2504-428">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-428">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="d2504-429">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-429">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="d2504-430">構成</span><span class="sxs-lookup"><span data-stu-id="d2504-430">Configure</span></span>
* <span data-ttu-id="d2504-431">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-431">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="d2504-432">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="d2504-432">Eventhubs</span></span>
* <span data-ttu-id="d2504-433">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-433">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="d2504-434">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-434">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="d2504-435">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-435">Network</span></span>
* <span data-ttu-id="d2504-436">[重大な変更] `vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="d2504-436">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="d2504-437">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="d2504-437">Policy Insights</span></span>
* <span data-ttu-id="d2504-438">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-438">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="d2504-439">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-439">Role</span></span>
* <span data-ttu-id="d2504-440">[非推奨] `create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="d2504-440">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="d2504-441">Service Bus</span><span class="sxs-lookup"><span data-stu-id="d2504-441">Service Bus</span></span>
* <span data-ttu-id="d2504-442">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-442">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="d2504-443">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-443">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="d2504-444">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-444">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-445">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-445">SQL</span></span>
* <span data-ttu-id="d2504-446">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-446">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-447">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-447">VM</span></span>
* <span data-ttu-id="d2504-448">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-448">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="d2504-449">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-449">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="d2504-450">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-450">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="d2504-451">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-451">Added new `ppg` command group for manging Proximity Placement Groups</span></span>
* <span data-ttu-id="d2504-452">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-452">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="d2504-453">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-453">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="d2504-454">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="d2504-454">April 23, 2019</span></span>

<span data-ttu-id="d2504-455">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="d2504-455">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-456">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-456">ACS</span></span>
* <span data-ttu-id="d2504-457">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-457">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="d2504-458">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-458">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="d2504-459">AMS</span><span class="sxs-lookup"><span data-stu-id="d2504-459">AMS</span></span>
* <span data-ttu-id="d2504-460">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-460">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-461">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-461">AppService</span></span>
* <span data-ttu-id="d2504-462">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-462">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="d2504-463">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-463">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="d2504-464">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-464">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="d2504-465">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-465">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="d2504-466">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-466">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="d2504-467">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-467">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="d2504-468">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-468">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="d2504-469">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-469">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="d2504-470">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-470">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="d2504-471">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="d2504-471">Deployment Manager</span></span>
* <span data-ttu-id="d2504-472">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="d2504-472">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="d2504-473">ラボ</span><span class="sxs-lookup"><span data-stu-id="d2504-473">Lab</span></span>
* <span data-ttu-id="d2504-474">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-474">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="d2504-475">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-475">Network</span></span>
* <span data-ttu-id="d2504-476">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-476">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-477">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-477">Resource</span></span>
* <span data-ttu-id="d2504-478">[非推奨] `resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="d2504-478">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="d2504-479">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="d2504-479">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="d2504-480">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-480">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="d2504-481">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-481">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-482">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-482">SQL</span></span>
* <span data-ttu-id="d2504-483">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-483">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="d2504-484">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-484">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="d2504-485">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-485">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="d2504-486">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-486">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-487">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-487">Storage</span></span>
* <span data-ttu-id="d2504-488">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-488">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-489">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-489">VM</span></span>
* <span data-ttu-id="d2504-490">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-490">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="d2504-491">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-491">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="d2504-492">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-492">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="d2504-493">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="d2504-493">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="d2504-494">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-494">Core</span></span>
* <span data-ttu-id="d2504-495">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-495">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-496">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-496">ACR</span></span>
* <span data-ttu-id="d2504-497">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-497">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="d2504-498">AMS</span><span class="sxs-lookup"><span data-stu-id="d2504-498">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="d2504-501">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-501">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="d2504-502">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-502">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-503">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-503">AppService</span></span>
* <span data-ttu-id="d2504-504">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-504">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="d2504-505">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-505">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="d2504-506">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-506">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="d2504-507">[重大な変更] `devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="d2504-507">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="d2504-508">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-508">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="d2504-509">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-509">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="d2504-510">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-510">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="d2504-511">CDN</span><span class="sxs-lookup"><span data-stu-id="d2504-511">CDN</span></span>
* <span data-ttu-id="d2504-512">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-512">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="d2504-513">フィードバック</span><span class="sxs-lookup"><span data-stu-id="d2504-513">Feedback</span></span>
* <span data-ttu-id="d2504-514">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-514">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="d2504-515">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-515">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="d2504-516">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-516">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-517">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-517">Monitor</span></span>
* <span data-ttu-id="d2504-518">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-518">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="d2504-519">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-519">Network</span></span>
* <span data-ttu-id="d2504-520">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-520">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="d2504-521">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-521">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="d2504-522">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-522">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="d2504-523">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-523">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="d2504-524">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="d2504-524">PrivateDNS</span></span>
* <span data-ttu-id="d2504-525">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-525">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-526">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-526">Resource</span></span>
* <span data-ttu-id="d2504-527">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-527">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="d2504-528">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-528">Role</span></span>
* <span data-ttu-id="d2504-529">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-529">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="d2504-530">[重大な変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-530">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-531">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-531">SQL</span></span>
* <span data-ttu-id="d2504-532">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-532">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-533">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-533">Storage</span></span>
* <span data-ttu-id="d2504-534">[重大な変更] `storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-534">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="d2504-535">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-535">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="d2504-536">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-536">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="d2504-537">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-537">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="d2504-538">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="d2504-538">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="d2504-539">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-539">Core</span></span>
* <span data-ttu-id="d2504-540">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-540">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="d2504-541">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-541">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="d2504-542">クラウド</span><span class="sxs-lookup"><span data-stu-id="d2504-542">Cloud</span></span>
* <span data-ttu-id="d2504-543">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-543">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-544">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-544">ACR</span></span>
* <span data-ttu-id="d2504-545">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-545">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="d2504-546">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-546">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="d2504-547">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-547">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="d2504-548">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-548">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-549">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-549">AppService</span></span>
* <span data-ttu-id="d2504-550">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-550">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="d2504-551">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-551">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="d2504-552">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="d2504-552">BOT Service</span></span>
* <span data-ttu-id="d2504-553">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-553">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="d2504-554">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-554">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="d2504-555">[重大な変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-555">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="d2504-556">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-556">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="d2504-557">CDN</span><span class="sxs-lookup"><span data-stu-id="d2504-557">CDN</span></span>
* <span data-ttu-id="d2504-558">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-558">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [重大な変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="d2504-560">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="d2504-560">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="d2504-561">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-561">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="d2504-562">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="d2504-562">Cosmosdb</span></span>
* <span data-ttu-id="d2504-563">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-563">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="d2504-564">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-564">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="d2504-565">Interactive</span><span class="sxs-lookup"><span data-stu-id="d2504-565">Interactive</span></span>
* <span data-ttu-id="d2504-566">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-566">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-567">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-567">Monitor</span></span>
* <span data-ttu-id="d2504-568">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-568">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="d2504-569">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-569">Network</span></span>
* <span data-ttu-id="d2504-570">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-570">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="d2504-571">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-571">Profile</span></span>
* <span data-ttu-id="d2504-572">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-572">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="d2504-573">Postgres</span><span class="sxs-lookup"><span data-stu-id="d2504-573">Postgres</span></span> 
* <span data-ttu-id="d2504-574">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-574">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="d2504-575">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="d2504-575">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-576">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-576">Resource</span></span>
* <span data-ttu-id="d2504-577">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-577">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="d2504-578">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-578">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="d2504-579">Graph</span><span class="sxs-lookup"><span data-stu-id="d2504-579">Graph</span></span>
* <span data-ttu-id="d2504-580">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-580">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="d2504-581">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-581">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="d2504-582">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-582">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="d2504-583">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-583">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="d2504-584">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-584">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-585">storage</span><span class="sxs-lookup"><span data-stu-id="d2504-585">storage</span></span>
* <span data-ttu-id="d2504-586">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-586">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="d2504-587">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-587">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="d2504-588">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-588">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="d2504-589">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-589">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-590">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-590">VM</span></span>
* <span data-ttu-id="d2504-591">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-591">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="d2504-592">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="d2504-592">March 12, 2019</span></span>

<span data-ttu-id="d2504-593">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="d2504-593">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="d2504-594">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-594">Core</span></span>

* <span data-ttu-id="d2504-595">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-595">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-596">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-596">ACR</span></span>

* <span data-ttu-id="d2504-597">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-597">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-598">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-598">ACS</span></span>

* <span data-ttu-id="d2504-599">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-599">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="d2504-600">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-600">AppService</span></span>

* <span data-ttu-id="d2504-601">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-601">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="d2504-602">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-602">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="d2504-603">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-603">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="d2504-604">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-604">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="d2504-605">Botservice</span><span class="sxs-lookup"><span data-stu-id="d2504-605">Botservice</span></span>

* <span data-ttu-id="d2504-606">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-606">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="d2504-607">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-607">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="d2504-608">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-608">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="d2504-609">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-609">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="d2504-610">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-610">Container</span></span>

* <span data-ttu-id="d2504-611">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-611">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="d2504-612">EventHub</span><span class="sxs-lookup"><span data-stu-id="d2504-612">EventHub</span></span>

* <span data-ttu-id="d2504-613">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-613">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="d2504-614">Find</span><span class="sxs-lookup"><span data-stu-id="d2504-614">Find</span></span>

* <span data-ttu-id="d2504-615">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="d2504-615">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="d2504-616">HDInsight</span><span class="sxs-lookup"><span data-stu-id="d2504-616">HDInsight</span></span>

* <span data-ttu-id="d2504-617">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-617">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="d2504-618">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-618">Network</span></span>

* <span data-ttu-id="d2504-619">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-619">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="d2504-620">Rdbms</span><span class="sxs-lookup"><span data-stu-id="d2504-620">Rdbms</span></span>

* <span data-ttu-id="d2504-621">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="d2504-621">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="d2504-622">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-622">Role</span></span>

* <span data-ttu-id="d2504-623">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-623">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="d2504-624">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-624">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="d2504-625">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d2504-625">Service Fabric</span></span>

* <span data-ttu-id="d2504-626">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-626">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="d2504-627">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="d2504-627">February 26, 2019</span></span>

<span data-ttu-id="d2504-628">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="d2504-628">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="d2504-629">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-629">Core</span></span>

* <span data-ttu-id="d2504-630">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-630">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-631">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-631">ACR</span></span>

* <span data-ttu-id="d2504-632">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-632">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="d2504-633">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-633">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-634">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-634">ACS</span></span>

* <span data-ttu-id="d2504-635">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-635">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-636">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-636">AppService</span></span>

* <span data-ttu-id="d2504-637">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-637">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-638">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-638">Batch</span></span>
* <span data-ttu-id="d2504-639">[重大な変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-639">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="d2504-640">[重大な変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-640">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="d2504-641">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-641">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="d2504-642">[重大な変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-642">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="d2504-643">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-643">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="d2504-644">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="d2504-644">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="d2504-645">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d2504-645">CosmosDB</span></span>

* <span data-ttu-id="d2504-646">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-646">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="d2504-647">Kusto</span><span class="sxs-lookup"><span data-stu-id="d2504-647">Kusto</span></span>

* <span data-ttu-id="d2504-648">[重大な変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-648">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="d2504-649">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-649">Network</span></span>

* <span data-ttu-id="d2504-650">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-650">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="d2504-651">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-651">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="d2504-652">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-652">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="d2504-653">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-653">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="d2504-654">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-654">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="d2504-655">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-655">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="d2504-656">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-656">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-657">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-657">Resource</span></span>

* <span data-ttu-id="d2504-658">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-658">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="d2504-659">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-659">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="d2504-660">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-660">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="d2504-661">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-661">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="d2504-662">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-662">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="d2504-663">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-663">Role</span></span>

* <span data-ttu-id="d2504-664">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-664">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-665">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-665">VM</span></span>

* <span data-ttu-id="d2504-666">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-666">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="d2504-667">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="d2504-667">February 12, 2019</span></span>

<span data-ttu-id="d2504-668">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="d2504-668">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="d2504-669">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-669">Core</span></span>

* <span data-ttu-id="d2504-670">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-670">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="d2504-671">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-671">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-672">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-672">ACR</span></span>
* <span data-ttu-id="d2504-673">[重大な変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-673">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="d2504-674">[重大な変更] `acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-674">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-675">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-675">ACS</span></span>
* <span data-ttu-id="d2504-676">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-676">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="d2504-677">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-677">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="d2504-678">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-678">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="d2504-679">AMS</span><span class="sxs-lookup"><span data-stu-id="d2504-679">AMS</span></span>
* <span data-ttu-id="d2504-680">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-680">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="d2504-681">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-681">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-682">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-682">Appservice</span></span>
* <span data-ttu-id="d2504-683">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-683">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="d2504-684">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-684">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="d2504-685">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-685">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="d2504-686">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-686">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="d2504-687">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-687">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="d2504-688">Botservice</span><span class="sxs-lookup"><span data-stu-id="d2504-688">Botservice</span></span>
* <span data-ttu-id="d2504-689">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-689">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="d2504-690">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-690">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="d2504-691">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-691">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="d2504-692">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-692">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="d2504-693">[非推奨] `--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-693">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="d2504-694">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-694">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="d2504-695">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-695">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="d2504-696">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-696">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="d2504-697">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="d2504-697">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="d2504-698">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-698">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="d2504-699">Key Vault</span><span class="sxs-lookup"><span data-stu-id="d2504-699">Key Vault</span></span>
* <span data-ttu-id="d2504-700">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-700">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-701">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-701">Monitor</span></span>
* <span data-ttu-id="d2504-702">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-702">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="d2504-703">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-703">Network</span></span>
* <span data-ttu-id="d2504-704">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-704">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="d2504-705">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-705">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="d2504-706">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-706">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="d2504-707">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-707">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="d2504-708">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="d2504-708">Policy Insights</span></span>
* <span data-ttu-id="d2504-709">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-709">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="d2504-710">RDBMS</span><span class="sxs-lookup"><span data-stu-id="d2504-710">RDBMS</span></span>
* <span data-ttu-id="d2504-711">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-711">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="d2504-712">Redis</span><span class="sxs-lookup"><span data-stu-id="d2504-712">Redis</span></span>
* <span data-ttu-id="d2504-713">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-713">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="d2504-714">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-714">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="d2504-715">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-715">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="d2504-716">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-716">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="d2504-717">[重大な変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-717">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="d2504-718">[重大な変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="d2504-718">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="d2504-719">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-719">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="d2504-720">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-720">Role</span></span>
* <span data-ttu-id="d2504-721">[重大な変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="d2504-721">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="d2504-722">SQL VM</span><span class="sxs-lookup"><span data-stu-id="d2504-722">SQL VM</span></span>
* <span data-ttu-id="d2504-723">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-723">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-724">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-724">VM</span></span>
* <span data-ttu-id="d2504-725">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-725">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="d2504-726">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-726">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="d2504-727">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-727">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="d2504-728">[重大な変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="d2504-728">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="d2504-729">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d2504-729">January 31, 2019</span></span>

<span data-ttu-id="d2504-730">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="d2504-730">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="d2504-731">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-731">Core</span></span>

* <span data-ttu-id="d2504-732">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="d2504-732">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="d2504-733">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="d2504-733">January 28, 2019</span></span>

<span data-ttu-id="d2504-734">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="d2504-734">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-735">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-735">ACR</span></span>
* <span data-ttu-id="d2504-736">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-736">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-737">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-737">ACS</span></span>
* <span data-ttu-id="d2504-738">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-738">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="d2504-739">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-739">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="d2504-740">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-740">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="d2504-741">AMS</span><span class="sxs-lookup"><span data-stu-id="d2504-741">AMS</span></span>
* <span data-ttu-id="d2504-742">[重大な変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-742">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="d2504-743">[重大な変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-743">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-744">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-744">Appservice</span></span>
* <span data-ttu-id="d2504-745">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-745">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="d2504-746">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-746">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="d2504-747">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-747">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="d2504-748">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-748">Container</span></span>
* <span data-ttu-id="d2504-749">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-749">Added `container start` command</span></span>
* <span data-ttu-id="d2504-750">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-750">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="d2504-751">EventGrid</span><span class="sxs-lookup"><span data-stu-id="d2504-751">EventGrid</span></span>
* <span data-ttu-id="d2504-752">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-752">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="d2504-753">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-753">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="d2504-754">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-754">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="d2504-755">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-755">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="d2504-756">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="d2504-756">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="d2504-757">HDInsight</span><span class="sxs-lookup"><span data-stu-id="d2504-757">HDInsight</span></span>
* <span data-ttu-id="d2504-758">[重大な変更] `hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-758">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="d2504-759">[重大な変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-759">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="d2504-760">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-760">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="d2504-761">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-761">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="d2504-762">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-762">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="d2504-763">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-763">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="d2504-764">IoT</span><span class="sxs-lookup"><span data-stu-id="d2504-764">IoT</span></span>
* <span data-ttu-id="d2504-765">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-765">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="d2504-766">Kusto</span><span class="sxs-lookup"><span data-stu-id="d2504-766">Kusto</span></span>
* <span data-ttu-id="d2504-767">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="d2504-767">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-768">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-768">Monitor</span></span>
* <span data-ttu-id="d2504-769">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-769">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="d2504-770">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-770">Profile</span></span>
* <span data-ttu-id="d2504-771">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-771">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="d2504-772">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-772">Network</span></span>
* <span data-ttu-id="d2504-773">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-773">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="d2504-774">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-774">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-775">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-775">Resource</span></span>
* <span data-ttu-id="d2504-776">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-776">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="d2504-777">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-777">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="d2504-778">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="d2504-778">SQL Virtual Machine</span></span>
* <span data-ttu-id="d2504-779">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="d2504-779">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-780">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-780">Storage</span></span>
* <span data-ttu-id="d2504-781">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-781">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="d2504-782">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="d2504-782">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-783">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-783">VM</span></span>
* <span data-ttu-id="d2504-784">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-784">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="d2504-785">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-785">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="d2504-786">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="d2504-786">January 15, 2019</span></span>

<span data-ttu-id="d2504-787">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="d2504-787">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-788">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-788">ACR</span></span>
* <span data-ttu-id="d2504-789">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-789">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="d2504-790">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-790">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="d2504-791">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-791">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="d2504-792">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-792">ACS</span></span>
* <span data-ttu-id="d2504-793">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-793">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-794">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-794">Appservice</span></span>
* <span data-ttu-id="d2504-795">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-795">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="d2504-796">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-796">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="d2504-797">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-797">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="d2504-798">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-798">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="d2504-799">Botservice</span><span class="sxs-lookup"><span data-stu-id="d2504-799">Botservice</span></span>
* <span data-ttu-id="d2504-800">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-800">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="d2504-801">構成</span><span class="sxs-lookup"><span data-stu-id="d2504-801">Configure</span></span>
* <span data-ttu-id="d2504-802">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-802">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="d2504-803">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d2504-803">CosmosDB</span></span>
* <span data-ttu-id="d2504-804">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-804">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="d2504-805">HDInsight</span><span class="sxs-lookup"><span data-stu-id="d2504-805">HDInsight</span></span>
* <span data-ttu-id="d2504-806">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-806">Added commands for managing applications</span></span>
* <span data-ttu-id="d2504-807">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-807">Added commands for managing script actions</span></span>
* <span data-ttu-id="d2504-808">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-808">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="d2504-809">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-809">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="d2504-810">[重大な変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-810">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="d2504-811">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-811">Network</span></span>
* <span data-ttu-id="d2504-812">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-812">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="d2504-813">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-813">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="d2504-814">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-814">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="d2504-815">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-815">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="d2504-816">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-816">Role</span></span>
* <span data-ttu-id="d2504-817">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="d2504-817">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="d2504-818">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="d2504-818">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="d2504-819">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="d2504-819">Security</span></span>
* <span data-ttu-id="d2504-820">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="d2504-820">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-821">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-821">Storage</span></span>
* <span data-ttu-id="d2504-822">[重大な変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-822">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="d2504-823">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="d2504-823">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="d2504-824">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-824">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="d2504-825">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-825">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="d2504-826">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-826">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-827">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-827">VM</span></span>
* <span data-ttu-id="d2504-828">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-828">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="d2504-829">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-829">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="d2504-830">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-830">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="d2504-831">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-831">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="d2504-832">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-832">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="d2504-833">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-833">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="d2504-834">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="d2504-834">December 20, 2018</span></span>

<span data-ttu-id="d2504-835">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="d2504-835">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="d2504-836">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-836">Appservice</span></span>
* <span data-ttu-id="d2504-837">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-837">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="d2504-838">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-838">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="d2504-839">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-839">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="d2504-840">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="d2504-840">IoTCentral</span></span>
* <span data-ttu-id="d2504-841">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-841">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="d2504-842">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-842">Role</span></span>
* <span data-ttu-id="d2504-843">[重大な変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-843">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-844">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-844">SQL</span></span>
* <span data-ttu-id="d2504-845">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-845">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-846">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-846">VM</span></span>
* <span data-ttu-id="d2504-847">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-847">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="d2504-848">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="d2504-848">December 18, 2018</span></span>

<span data-ttu-id="d2504-849">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="d2504-849">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="d2504-850">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-850">ACR</span></span>
* <span data-ttu-id="d2504-851">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-851">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="d2504-852">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="d2504-852">Condensed the table layout for task list</span></span>
* <span data-ttu-id="d2504-853">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-853">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-854">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-854">ACS</span></span>
* <span data-ttu-id="d2504-855">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-855">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="d2504-856">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-856">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="d2504-857">[非推奨] `az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="d2504-857">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="d2504-858">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="d2504-858">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="d2504-859">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-859">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="d2504-860">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-860">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-861">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-861">Appservice</span></span>
* <span data-ttu-id="d2504-862">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-862">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="d2504-863">Botservice</span><span class="sxs-lookup"><span data-stu-id="d2504-863">Botservice</span></span>
* <span data-ttu-id="d2504-864">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-864">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="d2504-865">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-865">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="d2504-866">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-866">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="d2504-867">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="d2504-867">Reduced Kudu network calls</span></span>
* <span data-ttu-id="d2504-868">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-868">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="d2504-869">消費</span><span class="sxs-lookup"><span data-stu-id="d2504-869">Consumption</span></span>
* <span data-ttu-id="d2504-870">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-870">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="d2504-871">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d2504-871">CosmosDB</span></span>
* <span data-ttu-id="d2504-872">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-872">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="d2504-873">マップ</span><span class="sxs-lookup"><span data-stu-id="d2504-873">Maps</span></span>
* <span data-ttu-id="d2504-874">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-874">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="d2504-875">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-875">Network</span></span>
* <span data-ttu-id="d2504-876">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-876">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="d2504-877">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-877">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-878">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-878">Resource</span></span>
* <span data-ttu-id="d2504-879">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-879">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="d2504-880">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-880">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-881">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-881">Storage</span></span>
*  <span data-ttu-id="d2504-882">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-882">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-883">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-883">VM</span></span>
* <span data-ttu-id="d2504-884">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-884">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="d2504-885">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="d2504-885">December 4, 2018</span></span>

<span data-ttu-id="d2504-886">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="d2504-886">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="d2504-887">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-887">Core</span></span>
* <span data-ttu-id="d2504-888">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-888">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="d2504-889">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-889">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-890">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-890">Appservice</span></span>
* <span data-ttu-id="d2504-891">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-891">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="d2504-892">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-892">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="d2504-893">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-893">Network</span></span>
* <span data-ttu-id="d2504-894">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-894">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="d2504-895">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-895">Role</span></span>
* <span data-ttu-id="d2504-896">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-896">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="d2504-897">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-897">VM</span></span>
* <span data-ttu-id="d2504-898">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-898">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="d2504-899">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-899">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="d2504-900">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-900">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="d2504-901">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-901">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="d2504-902">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="d2504-902">November 20, 2018</span></span>

<span data-ttu-id="d2504-903">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="d2504-903">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="d2504-904">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-904">Core</span></span>
* <span data-ttu-id="d2504-905">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-905">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-906">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-906">ACR</span></span>
* <span data-ttu-id="d2504-907">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-907">Added context token to task step</span></span>
* <span data-ttu-id="d2504-908">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-908">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="d2504-909">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-909">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-910">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-910">Appservice</span></span>
* <span data-ttu-id="d2504-911">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-911">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="d2504-912">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-912">Updated the default `node_version`.</span></span> <span data-ttu-id="d2504-913">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="d2504-913">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="d2504-914">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-914">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="d2504-915">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-915">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="d2504-916">IotCentral</span><span class="sxs-lookup"><span data-stu-id="d2504-916">IotCentral</span></span>
* <span data-ttu-id="d2504-917">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-917">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="d2504-918">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d2504-918">KeyVault</span></span>
* <span data-ttu-id="d2504-919">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-919">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="d2504-920">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-920">Network</span></span>
* <span data-ttu-id="d2504-921">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-921">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="d2504-922">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-922">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="d2504-923">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-923">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="d2504-924">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-924">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="d2504-925">Rdbms</span><span class="sxs-lookup"><span data-stu-id="d2504-925">Rdbms</span></span>
* <span data-ttu-id="d2504-926">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-926">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="d2504-927">Rbac</span><span class="sxs-lookup"><span data-stu-id="d2504-927">Rbac</span></span>
* <span data-ttu-id="d2504-928">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-928">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="d2504-929">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-929">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="d2504-930">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-930">Storage</span></span>
* <span data-ttu-id="d2504-931">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-931">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="d2504-932">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-932">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="d2504-933">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-933">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="d2504-934">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="d2504-934">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-935">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-935">VM</span></span>
* <span data-ttu-id="d2504-936">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-936">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="d2504-937">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-937">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="d2504-938">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="d2504-938">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="d2504-939">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-939">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="d2504-940">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-940">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="d2504-941">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-941">Added `snapshot wait` command</span></span>
* <span data-ttu-id="d2504-942">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-942">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="d2504-943">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="d2504-943">November 6, 2018</span></span>

<span data-ttu-id="d2504-944">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="d2504-944">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="d2504-945">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-945">Core</span></span>
* <span data-ttu-id="d2504-946">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-946">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-947">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-947">ACR</span></span>
* <span data-ttu-id="d2504-948">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-948">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="d2504-949">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-949">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-950">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-950">ACS</span></span>
* <span data-ttu-id="d2504-951">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-951">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="d2504-952">Advisor</span><span class="sxs-lookup"><span data-stu-id="d2504-952">Advisor</span></span>
* <span data-ttu-id="d2504-953">GA リリース</span><span class="sxs-lookup"><span data-stu-id="d2504-953">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="d2504-954">AMS</span><span class="sxs-lookup"><span data-stu-id="d2504-954">AMS</span></span>
* <span data-ttu-id="d2504-955">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-955">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="d2504-956">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-956">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="d2504-957">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-957">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="d2504-958">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-958">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="d2504-959">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-959">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="d2504-960">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-960">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="d2504-961">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-961">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="d2504-962">[重大な変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="d2504-962">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="d2504-963">[重大な変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-963">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="d2504-964">[重大な変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-964">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="d2504-965">[重大な変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="d2504-965">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="d2504-966">[重大な変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="d2504-966">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="d2504-967">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="d2504-967">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="d2504-968">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="d2504-968">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="d2504-969">[重大な変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-969">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="d2504-970">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d2504-970">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="d2504-971">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="d2504-971">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-972">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-972">AppService</span></span>
* <span data-ttu-id="d2504-973">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-973">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="d2504-974">構成</span><span class="sxs-lookup"><span data-stu-id="d2504-974">Configure</span></span>
* <span data-ttu-id="d2504-975">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-975">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="d2504-976">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-976">Container</span></span>
* <span data-ttu-id="d2504-977">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-977">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="d2504-978">EventHub</span><span class="sxs-lookup"><span data-stu-id="d2504-978">EventHub</span></span>
* <span data-ttu-id="d2504-979">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-979">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="d2504-980">Interactive</span><span class="sxs-lookup"><span data-stu-id="d2504-980">Interactive</span></span>
* <span data-ttu-id="d2504-981">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="d2504-981">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-982">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-982">Monitor</span></span>
* <span data-ttu-id="d2504-983">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-983">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="d2504-984">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-984">Network</span></span>
* <span data-ttu-id="d2504-985">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-985">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="d2504-986">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-986">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="d2504-987">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-987">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="d2504-988">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-988">Profile</span></span>
* <span data-ttu-id="d2504-989">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-989">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="d2504-990">RDBMS</span><span class="sxs-lookup"><span data-stu-id="d2504-990">RDBMS</span></span>
* <span data-ttu-id="d2504-991">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-991">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-992">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-992">Resource</span></span>
* <span data-ttu-id="d2504-993">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-993">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="d2504-994">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-994">Role</span></span>
* <span data-ttu-id="d2504-995">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-995">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="d2504-996">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-996">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="d2504-997">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-997">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-998">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-998">Storage</span></span>
* <span data-ttu-id="d2504-999">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="d2504-999">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1000">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1000">VM</span></span>
* <span data-ttu-id="d2504-1001">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1001">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="d2504-1002">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1002">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="d2504-1003">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1003">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="d2504-1004">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1004">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="d2504-1005">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="d2504-1005">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="d2504-1006">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1006">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="d2504-1007">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1007">October 23, 2018</span></span>

<span data-ttu-id="d2504-1008">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="d2504-1008">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1009">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1009">Core</span></span>
* <span data-ttu-id="d2504-1010">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1010">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="d2504-1011">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1011">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-1012">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-1012">ACR</span></span>
* <span data-ttu-id="d2504-1013">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1013">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="d2504-1014">CDN</span><span class="sxs-lookup"><span data-stu-id="d2504-1014">CDN</span></span>
* <span data-ttu-id="d2504-1015">[重大な変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1015">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="d2504-1016">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-1016">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="d2504-1017">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-1017">Container</span></span>
* <span data-ttu-id="d2504-1018">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1018">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="d2504-1019">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1019">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="d2504-1020">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1020">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="d2504-1021">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1021">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="d2504-1022">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1022">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="d2504-1023">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1023">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="d2504-1024">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1024">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="d2504-1025">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d2504-1025">CosmosDB</span></span>
* <span data-ttu-id="d2504-1026">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1026">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="d2504-1027">Interactive</span><span class="sxs-lookup"><span data-stu-id="d2504-1027">Interactive</span></span>
* <span data-ttu-id="d2504-1028">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1028">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="d2504-1029">IoT Central</span><span class="sxs-lookup"><span data-stu-id="d2504-1029">IoT Central</span></span>
* <span data-ttu-id="d2504-1030">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1030">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="d2504-1031">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="d2504-1031">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-1032">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-1032">Monitor</span></span>
* <span data-ttu-id="d2504-1033">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="d2504-1033">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="d2504-1034">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1034">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="d2504-1035">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1035">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="d2504-1036">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1036">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="d2504-1037">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1037">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="d2504-1038">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1038">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="d2504-1039">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="d2504-1039">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="d2504-1040">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1040">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="d2504-1041">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1041">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="d2504-1042">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1042">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1043">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1043">Network</span></span>
* <span data-ttu-id="d2504-1044">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1044">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="d2504-1045">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1045">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="d2504-1046">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d2504-1046">ServiceBus</span></span>
* <span data-ttu-id="d2504-1047">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1047">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-1048">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-1048">SQL</span></span>
* <span data-ttu-id="d2504-1049">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1049">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1050">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1050">Storage</span></span>
* <span data-ttu-id="d2504-1051">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1051">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="d2504-1052">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1052">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1053">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1053">VM</span></span>
* <span data-ttu-id="d2504-1054">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="d2504-1054">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="d2504-1055">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1055">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="d2504-1056">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1056">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="d2504-1057">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1057">October 16, 2018</span></span>

<span data-ttu-id="d2504-1058">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="d2504-1058">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1059">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1059">VM</span></span>
* <span data-ttu-id="d2504-1060">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1060">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="d2504-1061">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1061">October 9, 2018</span></span>

<span data-ttu-id="d2504-1062">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="d2504-1062">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1063">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1063">Core</span></span>
* <span data-ttu-id="d2504-1064">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1064">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-1065">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-1065">ACR</span></span>
* <span data-ttu-id="d2504-1066">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1066">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1067">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1067">ACS</span></span>
* <span data-ttu-id="d2504-1068">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="d2504-1068">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="d2504-1069">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1069">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="d2504-1070">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1070">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="d2504-1071">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1071">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="d2504-1072">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-1072">Container</span></span>
* <span data-ttu-id="d2504-1073">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1073">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="d2504-1074">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1074">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="d2504-1075">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="d2504-1075">Event Hub</span></span>
* <span data-ttu-id="d2504-1076">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1076">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="d2504-1077">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1077">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="d2504-1078">Extensions</span><span class="sxs-lookup"><span data-stu-id="d2504-1078">Extensions</span></span>
* <span data-ttu-id="d2504-1079">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1079">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="d2504-1080">HDInsight</span><span class="sxs-lookup"><span data-stu-id="d2504-1080">HDInsight</span></span>
* <span data-ttu-id="d2504-1081">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="d2504-1081">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="d2504-1082">IoT</span><span class="sxs-lookup"><span data-stu-id="d2504-1082">IoT</span></span>
* <span data-ttu-id="d2504-1083">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1083">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="d2504-1084">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d2504-1084">KeyVault</span></span>
* <span data-ttu-id="d2504-1085">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1085">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1086">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1086">Network</span></span>
* <span data-ttu-id="d2504-1087">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="d2504-1087">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="d2504-1088">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="d2504-1088">See #6052</span></span>
* <span data-ttu-id="d2504-1089">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1089">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="d2504-1090">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="d2504-1090">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="d2504-1091">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1091">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="d2504-1092">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1092">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="d2504-1093">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1093">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="d2504-1094">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1094">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="d2504-1095">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-1095">Role</span></span>
* <span data-ttu-id="d2504-1096">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1096">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="d2504-1097">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1097">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="d2504-1098">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1098">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="d2504-1099">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1099">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="d2504-1100">Service Bus</span><span class="sxs-lookup"><span data-stu-id="d2504-1100">Service Bus</span></span>
* <span data-ttu-id="d2504-1101">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1101">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1102">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1102">VM</span></span>
* <span data-ttu-id="d2504-1103">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1103">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="d2504-1104">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1104">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="d2504-1105">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1105">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="d2504-1106">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1106">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="d2504-1107">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1107">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="d2504-1108">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1108">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="d2504-1109">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1109">September 21, 2018</span></span>

<span data-ttu-id="d2504-1110">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="d2504-1110">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-1111">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-1111">ACR</span></span>
* <span data-ttu-id="d2504-1112">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1112">Added ACR Task commands</span></span>
* <span data-ttu-id="d2504-1113">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1113">Added quick run command</span></span>
* <span data-ttu-id="d2504-1114">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1114">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="d2504-1115">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1115">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="d2504-1116">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1116">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="d2504-1117">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1117">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1118">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1118">ACS</span></span>
* <span data-ttu-id="d2504-1119">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1119">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="d2504-1120">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1120">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1121">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-1121">AppService</span></span>

* <span data-ttu-id="d2504-1122">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1122">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="d2504-1123">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1123">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="d2504-1124">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1124">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="d2504-1125">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1125">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-1126">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-1126">Batch</span></span>
* <span data-ttu-id="d2504-1127">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1127">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="d2504-1128">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1128">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="d2504-1129">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1129">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="d2504-1130">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1130">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="d2504-1131">Batch AI</span><span class="sxs-lookup"><span data-stu-id="d2504-1131">Batch AI</span></span> 
* <span data-ttu-id="d2504-1132">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1132">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="d2504-1133">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="d2504-1133">Cognitive Services</span></span>
* <span data-ttu-id="d2504-1134">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1134">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="d2504-1135">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1135">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="d2504-1136">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1136">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="d2504-1137">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1137">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="d2504-1138">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1138">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="d2504-1139">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1139">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="d2504-1140">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-1140">Container</span></span>
* <span data-ttu-id="d2504-1141">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1141">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="d2504-1142">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1142">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="d2504-1143">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1143">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="d2504-1144">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1144">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="d2504-1145">DataLake</span><span class="sxs-lookup"><span data-stu-id="d2504-1145">Datalake</span></span>
* <span data-ttu-id="d2504-1146">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1146">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="d2504-1147">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="d2504-1147">Interactive Shell</span></span>
* <span data-ttu-id="d2504-1148">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1148">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="d2504-1149">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1149">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="d2504-1150">IoT</span><span class="sxs-lookup"><span data-stu-id="d2504-1150">IoT</span></span>
* <span data-ttu-id="d2504-1151">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1151">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="d2504-1152">Key Vault</span><span class="sxs-lookup"><span data-stu-id="d2504-1152">Key Vault</span></span>
* <span data-ttu-id="d2504-1153">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1153">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1154">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1154">Network</span></span>
* <span data-ttu-id="d2504-1155">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1155">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="d2504-1156">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1156">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="d2504-1157">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1157">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="d2504-1158">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1158">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="d2504-1159">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1159">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="d2504-1160">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1160">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="d2504-1161">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1161">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="d2504-1162">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-1162">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="d2504-1163">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1163">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="d2504-1164">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1164">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="d2504-1165">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1165">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="d2504-1166">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1166">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="d2504-1167">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1167">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="d2504-1168">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="d2504-1168">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="d2504-1169">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1169">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="d2504-1170">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1170">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="d2504-1171">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1171">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="d2504-1172">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1172">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="d2504-1173">RDBMS</span><span class="sxs-lookup"><span data-stu-id="d2504-1173">RDBMS</span></span>
* <span data-ttu-id="d2504-1174">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1174">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="d2504-1175">予約</span><span class="sxs-lookup"><span data-stu-id="d2504-1175">Reservation</span></span>
* <span data-ttu-id="d2504-1176">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1176">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="d2504-1177">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1177">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="d2504-1178">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="d2504-1178">Manage App</span></span>
* <span data-ttu-id="d2504-1179">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1179">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="d2504-1180">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1180">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="d2504-1181">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-1181">Role</span></span>
* <span data-ttu-id="d2504-1182">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1182">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="d2504-1183">SignalR</span><span class="sxs-lookup"><span data-stu-id="d2504-1183">SignalR</span></span>
* <span data-ttu-id="d2504-1184">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="d2504-1184">First release</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1185">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1185">Storage</span></span>
* <span data-ttu-id="d2504-1186">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1186">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="d2504-1187">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1187">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1188">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1188">VM</span></span>
* <span data-ttu-id="d2504-1189">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="d2504-1189">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="d2504-1190">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1190">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="d2504-1191">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1191">August 28, 2018</span></span>

<span data-ttu-id="d2504-1192">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="d2504-1192">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1193">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1193">Core</span></span>

* <span data-ttu-id="d2504-1194">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1194">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="d2504-1195">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1195">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-1196">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-1196">ACR</span></span>

* <span data-ttu-id="d2504-1197">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1197">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="d2504-1198">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1198">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1199">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1199">ACS</span></span>

* <span data-ttu-id="d2504-1200">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1200">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="d2504-1201">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1201">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1202">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-1202">AppService</span></span>

* <span data-ttu-id="d2504-1203">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1203">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="d2504-1204">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1204">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="d2504-1205">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1205">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="d2504-1206">バックアップ</span><span class="sxs-lookup"><span data-stu-id="d2504-1206">Backup</span></span>

* <span data-ttu-id="d2504-1207">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1207">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="d2504-1208">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="d2504-1208">Bot Service</span></span>

* <span data-ttu-id="d2504-1209">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="d2504-1209">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="d2504-1210">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="d2504-1210">Cognitive Services</span></span>

* <span data-ttu-id="d2504-1211">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1211">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="d2504-1212">IoT</span><span class="sxs-lookup"><span data-stu-id="d2504-1212">IoT</span></span>

* <span data-ttu-id="d2504-1213">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1213">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-1214">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-1214">Monitor</span></span>

* <span data-ttu-id="d2504-1215">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1215">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="d2504-1216">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1216">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1217">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1217">Network</span></span>

* <span data-ttu-id="d2504-1218">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1218">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-1219">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-1219">Resource</span></span>

* <span data-ttu-id="d2504-1220">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1220">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1221">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1221">Storage</span></span>

* <span data-ttu-id="d2504-1222">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1222">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1223">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1223">VM</span></span>

* <span data-ttu-id="d2504-1224">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1224">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="d2504-1225">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1225">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="d2504-1226">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1226">Auguest 14, 2018</span></span>

<span data-ttu-id="d2504-1227">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="d2504-1227">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1228">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1228">Core</span></span>

* <span data-ttu-id="d2504-1229">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1229">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="d2504-1230">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1230">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="d2504-1231">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="d2504-1231">Telemetry</span></span>

* <span data-ttu-id="d2504-1232">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1232">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-1233">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-1233">ACR</span></span>

* <span data-ttu-id="d2504-1234">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1234">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="d2504-1235">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1235">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1236">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1236">ACS</span></span>

* <span data-ttu-id="d2504-1237">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1237">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="d2504-1238">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1238">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="d2504-1239">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1239">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="d2504-1240">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1240">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="d2504-1241">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1241">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="d2504-1242">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-1242">AppService</span></span>

* <span data-ttu-id="d2504-1243">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1243">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="d2504-1244">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1244">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="d2504-1245">BatchAI</span><span class="sxs-lookup"><span data-stu-id="d2504-1245">BatchAI</span></span>

* <span data-ttu-id="d2504-1246">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1246">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="d2504-1247">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-1247">Container</span></span>

* <span data-ttu-id="d2504-1248">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1248">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="d2504-1249">IoT</span><span class="sxs-lookup"><span data-stu-id="d2504-1249">IoT</span></span>

* <span data-ttu-id="d2504-1250">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1250">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="d2504-1251">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1251">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="d2504-1252">Iot Central</span><span class="sxs-lookup"><span data-stu-id="d2504-1252">Iot Central</span></span>

* <span data-ttu-id="d2504-1253">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="d2504-1253">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="d2504-1254">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d2504-1254">KeyVault</span></span>


* <span data-ttu-id="d2504-1255">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1255">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="d2504-1256">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1256">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="d2504-1257">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1257">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="d2504-1258">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1258">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="d2504-1259">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1259">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="d2504-1260">リレー</span><span class="sxs-lookup"><span data-stu-id="d2504-1260">Relay</span></span>

* <span data-ttu-id="d2504-1261">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="d2504-1261">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-1262">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-1262">Sql</span></span>

* <span data-ttu-id="d2504-1263">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1263">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1264">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1264">Storage</span></span>

* <span data-ttu-id="d2504-1265">[重大な変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="d2504-1265">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="d2504-1266">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1266">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="d2504-1267">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1267">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="d2504-1268">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1268">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="d2504-1269">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1269">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1270">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1270">VM</span></span>

* <span data-ttu-id="d2504-1271">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1271">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="d2504-1272">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="d2504-1272">July 31, 2018</span></span>

<span data-ttu-id="d2504-1273">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="d2504-1273">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-1274">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-1274">ACR</span></span>

* <span data-ttu-id="d2504-1275">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1275">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="d2504-1276">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1276">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1277">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1277">ACS</span></span>

* <span data-ttu-id="d2504-1278">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1278">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-1279">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-1279">Batch</span></span>

* <span data-ttu-id="d2504-1280">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1280">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="d2504-1281">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-1281">Container</span></span>

* <span data-ttu-id="d2504-1282">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1282">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1283">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1283">Network</span></span>

* <span data-ttu-id="d2504-1284">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1284">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="d2504-1285">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-1285">Resource</span></span>

* <span data-ttu-id="d2504-1286">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1286">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="d2504-1287">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1287">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="d2504-1288">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-1288">Role</span></span>

* <span data-ttu-id="d2504-1289">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1289">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="d2504-1290">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1290">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="d2504-1291">Search</span><span class="sxs-lookup"><span data-stu-id="d2504-1291">Search</span></span>

* <span data-ttu-id="d2504-1292">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1292">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="d2504-1293">Service Bus</span><span class="sxs-lookup"><span data-stu-id="d2504-1293">Service Bus</span></span>

* <span data-ttu-id="d2504-1294">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1294">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="d2504-1295">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1295">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="d2504-1296">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="d2504-1296">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="d2504-1297">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="d2504-1297">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1298">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1298">Storage</span></span>

* <span data-ttu-id="d2504-1299">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-1299">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="d2504-1300">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1300">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1301">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1301">VM</span></span>

* <span data-ttu-id="d2504-1302">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-1302">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="d2504-1303">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1303">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="d2504-1304">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1304">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="d2504-1305">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1305">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="d2504-1306">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1306">July 18, 2018</span></span>

<span data-ttu-id="d2504-1307">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="d2504-1307">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1308">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1308">Core</span></span>

* <span data-ttu-id="d2504-1309">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1309">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="d2504-1310">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1310">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="d2504-1311">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1311">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-1312">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-1312">ACR</span></span>

* <span data-ttu-id="d2504-1313">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1313">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="d2504-1314">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1314">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="d2504-1315">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1315">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="d2504-1316">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1316">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1317">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1317">ACS</span></span>

* <span data-ttu-id="d2504-1318">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1318">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1319">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-1319">AppService</span></span>

* <span data-ttu-id="d2504-1320">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1320">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-1321">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-1321">Batch</span></span>

* <span data-ttu-id="d2504-1322">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1322">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="d2504-1323">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1323">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="d2504-1324">Batch AI</span><span class="sxs-lookup"><span data-stu-id="d2504-1324">Batch AI</span></span>

* <span data-ttu-id="d2504-1325">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1325">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="d2504-1326">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-1326">Container</span></span>

* <span data-ttu-id="d2504-1327">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1327">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="d2504-1328">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1328">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1329">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1329">Network</span></span>

* <span data-ttu-id="d2504-1330">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1330">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="d2504-1331">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1331">Added `network nic wait`</span></span>
* <span data-ttu-id="d2504-1332">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1332">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="d2504-1333">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1333">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="d2504-1334">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-1334">Resource</span></span>

* <span data-ttu-id="d2504-1335">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1335">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="d2504-1336">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1336">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="d2504-1337">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1337">Added `deployment wait` command</span></span>
* <span data-ttu-id="d2504-1338">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1338">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-1339">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-1339">SQL</span></span>

* <span data-ttu-id="d2504-1340">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1340">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="d2504-1341">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-1341">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="d2504-1342">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1342">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1343">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1343">Storage</span></span>

* <span data-ttu-id="d2504-1344">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1344">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1345">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1345">VM</span></span>

* <span data-ttu-id="d2504-1346">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1346">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="d2504-1347">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1347">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="d2504-1348">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1348">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="d2504-1349">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1349">July 3, 2018</span></span>

<span data-ttu-id="d2504-1350">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="d2504-1350">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="d2504-1351">AKS</span><span class="sxs-lookup"><span data-stu-id="d2504-1351">AKS</span></span>

* <span data-ttu-id="d2504-1352">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1352">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="d2504-1353">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1353">July 3, 2018</span></span>

<span data-ttu-id="d2504-1354">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="d2504-1354">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1355">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1355">Core</span></span>

* <span data-ttu-id="d2504-1356">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1356">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-1357">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-1357">ACR</span></span>

* <span data-ttu-id="d2504-1358">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1358">Added polling build status</span></span>
* <span data-ttu-id="d2504-1359">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1359">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="d2504-1360">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1360">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1361">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1361">ACS</span></span>

* <span data-ttu-id="d2504-1362">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1362">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="d2504-1363">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1363">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="d2504-1364">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1364">Updated options for `aks browse` command.</span></span> <span data-ttu-id="d2504-1365">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1365">Added `--listen-port` support</span></span>
* <span data-ttu-id="d2504-1366">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1366">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="d2504-1367">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="d2504-1367">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="d2504-1368">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1368">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1369">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-1369">AppService</span></span>

* <span data-ttu-id="d2504-1370">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-1370">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="d2504-1371">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1371">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="d2504-1372">バックアップ</span><span class="sxs-lookup"><span data-stu-id="d2504-1372">Backup</span></span>

* <span data-ttu-id="d2504-1373">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1373">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="d2504-1374">BatchAI</span><span class="sxs-lookup"><span data-stu-id="d2504-1374">BatchAI</span></span>

* <span data-ttu-id="d2504-1375">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1375">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="d2504-1376">クラウド</span><span class="sxs-lookup"><span data-stu-id="d2504-1376">Cloud</span></span>

* <span data-ttu-id="d2504-1377">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1377">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="d2504-1378">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-1378">Container</span></span>

* <span data-ttu-id="d2504-1379">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1379">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="d2504-1380">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1380">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="d2504-1381">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1381">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="d2504-1382">拡張機能</span><span class="sxs-lookup"><span data-stu-id="d2504-1382">Extension</span></span>

* <span data-ttu-id="d2504-1383">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1383">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1384">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1384">Network</span></span>

* <span data-ttu-id="d2504-1385">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1385">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="d2504-1386">Rdbms</span><span class="sxs-lookup"><span data-stu-id="d2504-1386">Rdbms</span></span>

* <span data-ttu-id="d2504-1387">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1387">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-1388">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-1388">Resource</span></span>

* <span data-ttu-id="d2504-1389">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1389">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1390">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1390">VM</span></span>

* <span data-ttu-id="d2504-1391">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-1391">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="d2504-1392">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1392">June 25, 2018</span></span>

<span data-ttu-id="d2504-1393">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="d2504-1393">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="d2504-1394">CLI</span><span class="sxs-lookup"><span data-stu-id="d2504-1394">CLI</span></span>

* <span data-ttu-id="d2504-1395">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1395">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="d2504-1396">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1396">June 19, 2018</span></span>

<span data-ttu-id="d2504-1397">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="d2504-1397">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1398">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1398">Core</span></span>

* <span data-ttu-id="d2504-1399">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1399">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-1400">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-1400">ACR</span></span>

* <span data-ttu-id="d2504-1401">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1401">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="d2504-1402">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1402">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1403">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1403">ACS</span></span>

* <span data-ttu-id="d2504-1404">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1404">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="d2504-1405">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1405">Added `--update` support</span></span>
* <span data-ttu-id="d2504-1406">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1406">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="d2504-1407">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1407">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="d2504-1408">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1408">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="d2504-1409">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1409">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="d2504-1410">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1410">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="d2504-1411">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1411">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1412">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-1412">AppService</span></span>

* <span data-ttu-id="d2504-1413">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1413">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="d2504-1414">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1414">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-1415">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-1415">Batch</span></span>

* <span data-ttu-id="d2504-1416">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1416">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="d2504-1417">Batch AI</span><span class="sxs-lookup"><span data-stu-id="d2504-1417">Batch AI</span></span>

* <span data-ttu-id="d2504-1418">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1418">Added support for workspaces.</span></span> <span data-ttu-id="d2504-1419">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="d2504-1419">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="d2504-1420">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1420">Added support for experiments.</span></span> <span data-ttu-id="d2504-1421">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="d2504-1421">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="d2504-1422">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1422">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="d2504-1423">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1423">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="d2504-1424">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="d2504-1424">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="d2504-1425">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1425">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="d2504-1426">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="d2504-1426">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="d2504-1427">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="d2504-1427">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="d2504-1428">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1428">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="d2504-1429">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="d2504-1429">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="d2504-1430">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1430">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="d2504-1431">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="d2504-1431">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="d2504-1432">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1432">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="d2504-1433">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="d2504-1433">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="d2504-1434">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1434">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="d2504-1435">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1435">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="d2504-1436">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1436">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="d2504-1437">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1437">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="d2504-1438">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1438">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="d2504-1439">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1439">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="d2504-1440">マップ</span><span class="sxs-lookup"><span data-stu-id="d2504-1440">Maps</span></span>

* <span data-ttu-id="d2504-1441">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1441">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1442">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1442">Network</span></span>

* <span data-ttu-id="d2504-1443">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="d2504-1443">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="d2504-1444">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1444">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="d2504-1445">#6502</span><span class="sxs-lookup"><span data-stu-id="d2504-1445">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="d2504-1446">Reservations</span><span class="sxs-lookup"><span data-stu-id="d2504-1446">Reservations</span></span>

* <span data-ttu-id="d2504-1447">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1447">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="d2504-1448">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1448">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="d2504-1449">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1449">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="d2504-1450">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1450">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="d2504-1451">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1451">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="d2504-1452">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1452">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="d2504-1453">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-1453">Role</span></span>

* <span data-ttu-id="d2504-1454">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1454">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-1455">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-1455">SQL</span></span>

* <span data-ttu-id="d2504-1456">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1456">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1457">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1457">Storage</span></span>

* <span data-ttu-id="d2504-1458">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1458">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1459">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1459">VM</span></span>

* <span data-ttu-id="d2504-1460">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1460">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="d2504-1461">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1461">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="d2504-1462">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1462">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="d2504-1463">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1463">June 13, 2018</span></span>

<span data-ttu-id="d2504-1464">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="d2504-1464">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1465">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1465">Core</span></span>

* <span data-ttu-id="d2504-1466">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1466">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="d2504-1467">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1467">June 13, 2018</span></span>

<span data-ttu-id="d2504-1468">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="d2504-1468">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="d2504-1469">AKS</span><span class="sxs-lookup"><span data-stu-id="d2504-1469">AKS</span></span>

* <span data-ttu-id="d2504-1470">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1470">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="d2504-1471">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1471">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="d2504-1472">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1472">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="d2504-1473">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1473">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="d2504-1474">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1474">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1475">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-1475">AppService</span></span>

* <span data-ttu-id="d2504-1476">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1476">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="d2504-1477">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1477">June 5, 2018</span></span>

<span data-ttu-id="d2504-1478">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="d2504-1478">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="d2504-1479">Interactive</span><span class="sxs-lookup"><span data-stu-id="d2504-1479">Interactive</span></span>

* <span data-ttu-id="d2504-1480">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1480">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="d2504-1481">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1481">June 5, 2018</span></span>

<span data-ttu-id="d2504-1482">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="d2504-1482">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1483">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1483">Core</span></span>

* <span data-ttu-id="d2504-1484">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1484">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="d2504-1485">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1485">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-1486">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-1486">ACR</span></span>

* <span data-ttu-id="d2504-1487">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1487">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="d2504-1488">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1488">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="d2504-1489">AKS</span><span class="sxs-lookup"><span data-stu-id="d2504-1489">AKS</span></span>

* <span data-ttu-id="d2504-1490">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1490">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-1491">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-1491">Batch</span></span>

* <span data-ttu-id="d2504-1492">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1492">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="d2504-1493">IoT</span><span class="sxs-lookup"><span data-stu-id="d2504-1493">IOT</span></span>

* <span data-ttu-id="d2504-1494">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1494">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1495">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1495">Network</span></span>

* <span data-ttu-id="d2504-1496">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1496">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="d2504-1497">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="d2504-1497">Policy Insights</span></span>

* <span data-ttu-id="d2504-1498">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="d2504-1498">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="d2504-1499">ARM</span><span class="sxs-lookup"><span data-stu-id="d2504-1499">ARM</span></span>

* <span data-ttu-id="d2504-1500">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1500">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-1501">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-1501">SQL</span></span>

* <span data-ttu-id="d2504-1502">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1502">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="d2504-1503">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1503">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="d2504-1504">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1504">Storage</span></span>

* <span data-ttu-id="d2504-1505">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1505">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1506">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1506">VM</span></span>

* <span data-ttu-id="d2504-1507">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1507">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="d2504-1508">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1508">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="d2504-1509">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1509">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="d2504-1510">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1510">May 22, 2018</span></span>

<span data-ttu-id="d2504-1511">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="d2504-1511">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1512">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1512">Core</span></span>

* <span data-ttu-id="d2504-1513">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1513">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1514">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1514">ACS</span></span>

* <span data-ttu-id="d2504-1515">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1515">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="d2504-1516">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1516">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1517">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-1517">AppService</span></span>

* <span data-ttu-id="d2504-1518">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1518">Improved generic update commands</span></span>
* <span data-ttu-id="d2504-1519">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1519">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="d2504-1520">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-1520">Container</span></span>

* <span data-ttu-id="d2504-1521">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1521">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="d2504-1522">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1522">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="d2504-1523">拡張機能</span><span class="sxs-lookup"><span data-stu-id="d2504-1523">Extension</span></span>

* <span data-ttu-id="d2504-1524">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1524">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="d2504-1525">Interactive</span><span class="sxs-lookup"><span data-stu-id="d2504-1525">Interactive</span></span>

* <span data-ttu-id="d2504-1526">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1526">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="d2504-1527">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1527">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="d2504-1528">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d2504-1528">KeyVault</span></span>

* <span data-ttu-id="d2504-1529">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1529">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1530">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1530">Network</span></span>

* <span data-ttu-id="d2504-1531">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1531">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="d2504-1532">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1532">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-1533">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-1533">SQL</span></span>

* <span data-ttu-id="d2504-1534">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1534">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="d2504-1535">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1535">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="d2504-1536">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1536">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="d2504-1537">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1537">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="d2504-1538">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1538">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="d2504-1539">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="d2504-1539">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="d2504-1540">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="d2504-1540">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="d2504-1541">`edition`</span><span class="sxs-lookup"><span data-stu-id="d2504-1541">`edition`.</span></span> <span data-ttu-id="d2504-1542">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="d2504-1542">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="d2504-1543">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="d2504-1543">`elasticPoolName`.</span></span> <span data-ttu-id="d2504-1544">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="d2504-1544">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="d2504-1545">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1545">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="d2504-1546">`edition`</span><span class="sxs-lookup"><span data-stu-id="d2504-1546">`edition`.</span></span> <span data-ttu-id="d2504-1547">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="d2504-1547">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="d2504-1548">`dtu`</span><span class="sxs-lookup"><span data-stu-id="d2504-1548">`dtu`.</span></span> <span data-ttu-id="d2504-1549">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="d2504-1549">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="d2504-1550">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="d2504-1550">`databaseDtuMin`.</span></span> <span data-ttu-id="d2504-1551">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="d2504-1551">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="d2504-1552">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="d2504-1552">`databaseDtuMax`.</span></span> <span data-ttu-id="d2504-1553">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="d2504-1553">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="d2504-1554">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1554">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="d2504-1555">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1555">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1556">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1556">Storage</span></span>

* <span data-ttu-id="d2504-1557">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1557">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="d2504-1558">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1558">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1559">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1559">VM</span></span>

* <span data-ttu-id="d2504-1560">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1560">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="d2504-1561">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="d2504-1561">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="d2504-1562">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1562">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="d2504-1563">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1563">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="d2504-1564">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1564">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="d2504-1565">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1565">May 7, 2018</span></span>

<span data-ttu-id="d2504-1566">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="d2504-1566">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1567">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1567">Core</span></span>

* <span data-ttu-id="d2504-1568">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1568">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="d2504-1569">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1569">Added limited support for positional arguments</span></span>
* <span data-ttu-id="d2504-1570">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1570">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="d2504-1571">#5591</span><span class="sxs-lookup"><span data-stu-id="d2504-1571">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="d2504-1572">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1572">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="d2504-1573">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="d2504-1573">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="d2504-1574">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1574">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="d2504-1575">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1575">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="d2504-1576">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1576">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-1577">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-1577">ACR</span></span>

* <span data-ttu-id="d2504-1578">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1578">Added ACR Build commands</span></span>
* <span data-ttu-id="d2504-1579">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1579">Improved resource not found error messages</span></span>
* <span data-ttu-id="d2504-1580">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1580">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="d2504-1581">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1581">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="d2504-1582">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1582">Improved repository commands error messages</span></span>
* <span data-ttu-id="d2504-1583">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1583">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1584">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1584">ACS</span></span>

* <span data-ttu-id="d2504-1585">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1585">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="d2504-1586">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1586">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="d2504-1587">AMS</span><span class="sxs-lookup"><span data-stu-id="d2504-1587">AMS</span></span>

* <span data-ttu-id="d2504-1588">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="d2504-1588">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1589">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-1589">Appservice</span></span>

* <span data-ttu-id="d2504-1590">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1590">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="d2504-1591">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1591">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="d2504-1592">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1592">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="d2504-1593">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1593">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="d2504-1594">Batch AI</span><span class="sxs-lookup"><span data-stu-id="d2504-1594">Batch AI</span></span>

* <span data-ttu-id="d2504-1595">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1595">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="d2504-1596">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="d2504-1596">Cognitive Services</span></span>

* <span data-ttu-id="d2504-1597">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1597">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="d2504-1598">消費</span><span class="sxs-lookup"><span data-stu-id="d2504-1598">Consumption</span></span>

* <span data-ttu-id="d2504-1599">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1599">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="d2504-1600">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-1600">Container</span></span>

* <span data-ttu-id="d2504-1601">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1601">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="d2504-1602">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d2504-1602">Cosmos DB</span></span>

* <span data-ttu-id="d2504-1603">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1603">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="d2504-1604">DMS</span><span class="sxs-lookup"><span data-stu-id="d2504-1604">DMS</span></span>

* <span data-ttu-id="d2504-1605">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1605">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="d2504-1606">拡張機能</span><span class="sxs-lookup"><span data-stu-id="d2504-1606">Extension</span></span>

* <span data-ttu-id="d2504-1607">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1607">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="d2504-1608">Interactive</span><span class="sxs-lookup"><span data-stu-id="d2504-1608">Interactive</span></span>

* <span data-ttu-id="d2504-1609">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-1609">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="d2504-1610">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1610">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="d2504-1611">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1611">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="d2504-1612">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1612">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="d2504-1613">ラボ</span><span class="sxs-lookup"><span data-stu-id="d2504-1613">Lab</span></span>

* <span data-ttu-id="d2504-1614">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1614">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1615">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1615">Network</span></span>

* <span data-ttu-id="d2504-1616">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1616">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="d2504-1617">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-1617">Profile</span></span>

* <span data-ttu-id="d2504-1618">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1618">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="d2504-1619">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1619">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="d2504-1620">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1620">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="d2504-1621">Redis</span><span class="sxs-lookup"><span data-stu-id="d2504-1621">Redis</span></span>

* <span data-ttu-id="d2504-1622">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1622">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="d2504-1623">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1623">Deprecated `redis list-all`.</span></span> <span data-ttu-id="d2504-1624">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="d2504-1624">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="d2504-1625">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1625">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="d2504-1626">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1626">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="d2504-1627">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-1627">Role</span></span>

* <span data-ttu-id="d2504-1628">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1628">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1629">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1629">Storage</span></span>

* <span data-ttu-id="d2504-1630">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="d2504-1630">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="d2504-1631">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1631">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="d2504-1632">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="d2504-1632">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="d2504-1633">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="d2504-1633">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="d2504-1634">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1634">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1635">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1635">VM</span></span>

* <span data-ttu-id="d2504-1636">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1636">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="d2504-1637">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1637">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="d2504-1638">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="d2504-1638">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="d2504-1639">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1639">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="d2504-1640">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1640">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="d2504-1641">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1641">Added write accelerator support</span></span>
* <span data-ttu-id="d2504-1642">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1642">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="d2504-1643">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1643">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="d2504-1644">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1644">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="d2504-1645">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1645">April 10, 2018</span></span>

<span data-ttu-id="d2504-1646">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="d2504-1646">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-1647">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-1647">ACR</span></span>

* <span data-ttu-id="d2504-1648">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1648">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1649">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1649">ACS</span></span>

* <span data-ttu-id="d2504-1650">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1650">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1651">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-1651">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="d2504-1653">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1653">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="d2504-1654">BatchAI</span><span class="sxs-lookup"><span data-stu-id="d2504-1654">BatchAI</span></span>

* <span data-ttu-id="d2504-1655">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1655">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="d2504-1656">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="d2504-1656">Job level mounting</span></span>
  - <span data-ttu-id="d2504-1657">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="d2504-1657">Environment variables with secret values</span></span>
  - <span data-ttu-id="d2504-1658">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="d2504-1658">Performance counters settings</span></span>
  - <span data-ttu-id="d2504-1659">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="d2504-1659">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="d2504-1660">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="d2504-1660">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="d2504-1661">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="d2504-1661">Usage and limits reporting</span></span>
  - <span data-ttu-id="d2504-1662">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="d2504-1662">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="d2504-1663">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="d2504-1663">Support for custom images</span></span>
  - <span data-ttu-id="d2504-1664">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1664">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="d2504-1665">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-1665">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="d2504-1666">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="d2504-1666">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="d2504-1667">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="d2504-1667">National clouds are supported</span></span>
* <span data-ttu-id="d2504-1668">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1668">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="d2504-1669">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1669">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="d2504-1670">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1670">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="d2504-1671">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1671">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="d2504-1672">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="d2504-1672">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="d2504-1673">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="d2504-1673">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="d2504-1674">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1674">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="d2504-1675">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1675">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="d2504-1676">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="d2504-1676">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="d2504-1677">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1677">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="d2504-1678">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1678">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="d2504-1679">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1679">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="d2504-1680">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1680">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="d2504-1681">課金</span><span class="sxs-lookup"><span data-stu-id="d2504-1681">Billing</span></span>

* <span data-ttu-id="d2504-1682">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1682">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="d2504-1683">消費</span><span class="sxs-lookup"><span data-stu-id="d2504-1683">Consumption</span></span>

* <span data-ttu-id="d2504-1684">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1684">Added `marketplace` commands</span></span>
* <span data-ttu-id="d2504-1685">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1685">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="d2504-1686">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1686">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="d2504-1687">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1687">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="d2504-1688">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1688">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="d2504-1689">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1689">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="d2504-1690">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-1690">Container</span></span>

* <span data-ttu-id="d2504-1691">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1691">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="d2504-1692">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1692">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="d2504-1693">拡張機能</span><span class="sxs-lookup"><span data-stu-id="d2504-1693">Extension</span></span>

* <span data-ttu-id="d2504-1694">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1694">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="d2504-1695">Interactive</span><span class="sxs-lookup"><span data-stu-id="d2504-1695">Interactive</span></span>

* <span data-ttu-id="d2504-1696">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1696">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="d2504-1697">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1697">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="d2504-1698">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1698">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1699">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1699">Network</span></span>

* <span data-ttu-id="d2504-1700">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1700">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="d2504-1701">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1701">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="d2504-1702">#4910</span><span class="sxs-lookup"><span data-stu-id="d2504-1702">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="d2504-1703">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1703">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="d2504-1704">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="d2504-1704">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="d2504-1705">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1705">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="d2504-1706">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1706">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="d2504-1707">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1707">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="d2504-1708">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-1708">Profile</span></span>

* <span data-ttu-id="d2504-1709">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1709">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="d2504-1710">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1710">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="d2504-1711">RDBMS</span><span class="sxs-lookup"><span data-stu-id="d2504-1711">RDBMS</span></span>

* <span data-ttu-id="d2504-1712">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1712">Added `georestore` command</span></span>
* <span data-ttu-id="d2504-1713">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1713">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-1714">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-1714">Resource</span></span>

* <span data-ttu-id="d2504-1715">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1715">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="d2504-1716">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1716">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-1717">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-1717">SQL</span></span>

* <span data-ttu-id="d2504-1718">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1718">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1719">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1719">Storage</span></span>

* <span data-ttu-id="d2504-1720">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1720">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1721">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1721">VM</span></span>

* <span data-ttu-id="d2504-1722">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1722">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="d2504-1723">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1723">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="d2504-1725">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1725">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="d2504-1726">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1726">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="d2504-1727">#5718</span><span class="sxs-lookup"><span data-stu-id="d2504-1727">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="d2504-1728">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1728">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="d2504-1729">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1729">March 27, 2018</span></span>

<span data-ttu-id="d2504-1730">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="d2504-1730">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1731">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1731">Core</span></span>

* <span data-ttu-id="d2504-1732">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="d2504-1732">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1733">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1733">ACS</span></span>

* <span data-ttu-id="d2504-1734">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1734">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1735">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-1735">Appservice</span></span>

* <span data-ttu-id="d2504-1736">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1736">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="d2504-1737">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1737">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="d2504-1738">バックアップ</span><span class="sxs-lookup"><span data-stu-id="d2504-1738">Backup</span></span>

* <span data-ttu-id="d2504-1739">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1739">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="d2504-1740">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="d2504-1740">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="d2504-1741">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1741">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="d2504-1742">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1742">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="d2504-1743">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-1743">Container</span></span>

* <span data-ttu-id="d2504-1744">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1744">Added `container exec` command.</span></span> <span data-ttu-id="d2504-1745">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="d2504-1745">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="d2504-1746">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="d2504-1746">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="d2504-1747">拡張機能</span><span class="sxs-lookup"><span data-stu-id="d2504-1747">Extension</span></span>

* <span data-ttu-id="d2504-1748">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1748">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="d2504-1749">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1749">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="d2504-1750">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1750">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="d2504-1751">Interactive</span><span class="sxs-lookup"><span data-stu-id="d2504-1751">Interactive</span></span>

* <span data-ttu-id="d2504-1752">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1752">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="d2504-1753">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1753">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="d2504-1754">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="d2504-1754">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="d2504-1755">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1755">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="d2504-1756">ラボ</span><span class="sxs-lookup"><span data-stu-id="d2504-1756">Lab</span></span>

* <span data-ttu-id="d2504-1757">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1757">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-1758">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-1758">Monitor</span></span>

* <span data-ttu-id="d2504-1759">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="d2504-1759">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="d2504-1760">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="d2504-1760">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="d2504-1761">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="d2504-1761">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1762">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1762">Network</span></span>

* <span data-ttu-id="d2504-1763">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1763">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="d2504-1764">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-1764">Profile</span></span>

* <span data-ttu-id="d2504-1765">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1765">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="d2504-1766">RDBMS</span><span class="sxs-lookup"><span data-stu-id="d2504-1766">RDBMS</span></span>

* <span data-ttu-id="d2504-1767">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1767">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-1768">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-1768">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="d2504-1770">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-1770">Role</span></span>

* <span data-ttu-id="d2504-1771">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1771">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="d2504-1772">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1772">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="d2504-1773">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1773">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="d2504-1774">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1774">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="d2504-1775">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1775">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1776">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1776">Storage</span></span>

* <span data-ttu-id="d2504-1777">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1777">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="d2504-1778">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="d2504-1778">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1779">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1779">VM</span></span>

* <span data-ttu-id="d2504-1780">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1780">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="d2504-1781">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1781">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="d2504-1782">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1782">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="d2504-1783">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1783">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="d2504-1784">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1784">March 13, 2018</span></span>

<span data-ttu-id="d2504-1785">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="d2504-1785">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-1786">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-1786">ACR</span></span>

* <span data-ttu-id="d2504-1787">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1787">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="d2504-1788">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1788">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="d2504-1789">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1789">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1790">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1790">ACS</span></span>

* <span data-ttu-id="d2504-1791">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1791">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="d2504-1792">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1792">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="d2504-1793">Advisor</span><span class="sxs-lookup"><span data-stu-id="d2504-1793">Advisor</span></span>

* <span data-ttu-id="d2504-1794">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1794">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="d2504-1795">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1795">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="d2504-1796">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1796">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="d2504-1797">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1797">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="d2504-1798">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1798">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1799">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-1799">Appservice</span></span>

* <span data-ttu-id="d2504-1800">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1800">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="d2504-1801">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1801">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="d2504-1802">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="d2504-1802">Eventhubs</span></span>

* <span data-ttu-id="d2504-1803">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="d2504-1803">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="d2504-1804">拡張機能</span><span class="sxs-lookup"><span data-stu-id="d2504-1804">Extension</span></span>

* <span data-ttu-id="d2504-1805">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1805">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="d2504-1806">Interactive</span><span class="sxs-lookup"><span data-stu-id="d2504-1806">Interactive</span></span>

* <span data-ttu-id="d2504-1807">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="d2504-1807">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="d2504-1808">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="d2504-1808">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="d2504-1809">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="d2504-1809">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="d2504-1810">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1810">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-1811">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-1811">Monitor</span></span>

* <span data-ttu-id="d2504-1812">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1812">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="d2504-1813">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1813">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="d2504-1814">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1814">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="d2504-1815">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1815">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1816">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1816">Network</span></span>

* <span data-ttu-id="d2504-1817">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1817">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="d2504-1818">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1818">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="d2504-1819">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1819">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="d2504-1820">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1820">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="d2504-1821">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-1821">Profile</span></span>

* <span data-ttu-id="d2504-1822">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1822">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="d2504-1823">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1823">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="d2504-1824">RDBMS</span><span class="sxs-lookup"><span data-stu-id="d2504-1824">RDBMS</span></span>

* <span data-ttu-id="d2504-1825">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1825">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="d2504-1826">Service Bus</span><span class="sxs-lookup"><span data-stu-id="d2504-1826">Service Bus</span></span>

* <span data-ttu-id="d2504-1827">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="d2504-1827">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1828">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1828">Storage</span></span>

* <span data-ttu-id="d2504-1829">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-1829">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="d2504-1830">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="d2504-1830">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1831">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1831">VM</span></span>

* <span data-ttu-id="d2504-1832">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1832">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="d2504-1833">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1833">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="d2504-1834">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1834">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="d2504-1835">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1835">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="d2504-1836">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1836">February 27, 2018</span></span>

<span data-ttu-id="d2504-1837">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="d2504-1837">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1838">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1838">Core</span></span>

* <span data-ttu-id="d2504-1839">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="d2504-1839">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="d2504-1840">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1840">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="d2504-1841">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1841">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1842">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1842">ACS</span></span>

* <span data-ttu-id="d2504-1843">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1843">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="d2504-1844">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="d2504-1844">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="d2504-1845">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1845">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="d2504-1846">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1846">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1847">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-1847">Appservice</span></span>

* <span data-ttu-id="d2504-1848">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="d2504-1848">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="d2504-1849">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="d2504-1849">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="d2504-1850">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="d2504-1850">Cognitive Services</span></span>

* <span data-ttu-id="d2504-1851">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1851">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="d2504-1852">消費</span><span class="sxs-lookup"><span data-stu-id="d2504-1852">Consumption</span></span>

* <span data-ttu-id="d2504-1853">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1853">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="d2504-1854">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1854">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="d2504-1855">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-1855">Container</span></span>

* <span data-ttu-id="d2504-1856">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1856">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1857">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1857">Network</span></span>

* <span data-ttu-id="d2504-1858">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="d2504-1858">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-1859">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-1859">Resource</span></span>

* <span data-ttu-id="d2504-1860">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1860">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="d2504-1861">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-1861">Role</span></span>

* <span data-ttu-id="d2504-1862">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1862">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-1863">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-1863">SQL</span></span>

* <span data-ttu-id="d2504-1864">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1864">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1865">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1865">Storage</span></span>

* <span data-ttu-id="d2504-1866">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1866">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1867">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1867">VM</span></span>

* <span data-ttu-id="d2504-1868">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1868">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="d2504-1869">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1869">February 13, 2018</span></span>

<span data-ttu-id="d2504-1870">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="d2504-1870">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1871">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1871">Core</span></span>

* <span data-ttu-id="d2504-1872">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1872">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1873">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1873">ACS</span></span>

* <span data-ttu-id="d2504-1874">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1874">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="d2504-1875">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1875">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="d2504-1876">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1876">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="d2504-1877">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1877">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="d2504-1878">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1878">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="d2504-1879">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1879">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="d2504-1880">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1880">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="d2504-1881">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="d2504-1881">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1882">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-1882">Appservice</span></span>

* <span data-ttu-id="d2504-1883">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1883">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="d2504-1884">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1884">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="d2504-1885">CDN</span><span class="sxs-lookup"><span data-stu-id="d2504-1885">CDN</span></span>

* <span data-ttu-id="d2504-1886">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1886">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="d2504-1887">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-1887">Container</span></span>

* <span data-ttu-id="d2504-1888">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1888">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="d2504-1889">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1889">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="d2504-1890">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d2504-1890">CosmosDB</span></span>

* <span data-ttu-id="d2504-1891">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1891">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="d2504-1892">拡張機能</span><span class="sxs-lookup"><span data-stu-id="d2504-1892">Extension</span></span>

* <span data-ttu-id="d2504-1893">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1893">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="d2504-1894">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1894">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="d2504-1895">フィードバック</span><span class="sxs-lookup"><span data-stu-id="d2504-1895">Feedback</span></span>

* <span data-ttu-id="d2504-1896">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1896">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="d2504-1897">Interactive</span><span class="sxs-lookup"><span data-stu-id="d2504-1897">Interactive</span></span>

* <span data-ttu-id="d2504-1898">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1898">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="d2504-1899">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1899">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="d2504-1900">IoT</span><span class="sxs-lookup"><span data-stu-id="d2504-1900">IoT</span></span>

* <span data-ttu-id="d2504-1901">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1901">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="d2504-1902">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1902">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="d2504-1903">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1903">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="d2504-1904">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1904">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-1905">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-1905">Monitor</span></span>

* <span data-ttu-id="d2504-1906">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1906">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1907">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1907">Network</span></span>

* <span data-ttu-id="d2504-1908">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1908">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="d2504-1909">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-1909">Profile</span></span>

* <span data-ttu-id="d2504-1910">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1910">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-1911">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-1911">Resource</span></span>

* <span data-ttu-id="d2504-1912">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1912">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="d2504-1913">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-1913">Role</span></span>

* <span data-ttu-id="d2504-1914">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1914">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-1915">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-1915">SQL</span></span>

* <span data-ttu-id="d2504-1916">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1916">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="d2504-1917">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1917">Added `sql db rename`</span></span>
* <span data-ttu-id="d2504-1918">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1918">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1919">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1919">Storage</span></span>

* <span data-ttu-id="d2504-1920">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1920">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1921">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1921">VM</span></span>

* <span data-ttu-id="d2504-1922">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1922">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="d2504-1923">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1923">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="d2504-1924">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="d2504-1924">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="d2504-1925">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1925">January 31, 2018</span></span>

<span data-ttu-id="d2504-1926">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="d2504-1926">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="d2504-1927">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-1927">Core</span></span>

* <span data-ttu-id="d2504-1928">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1928">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="d2504-1929">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1929">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="d2504-1930">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1930">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="d2504-1931">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="d2504-1931">Use `--verbose` to see</span></span>
* <span data-ttu-id="d2504-1932">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="d2504-1932">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1933">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1933">ACS</span></span>

* <span data-ttu-id="d2504-1934">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1934">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="d2504-1935">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1935">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1936">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-1936">Appservice</span></span>

* <span data-ttu-id="d2504-1937">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="d2504-1937">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="d2504-1938">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1938">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="d2504-1939">CDN</span><span class="sxs-lookup"><span data-stu-id="d2504-1939">CDN</span></span>

* <span data-ttu-id="d2504-1940">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1940">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="d2504-1941">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d2504-1941">CosmosDB</span></span>

* <span data-ttu-id="d2504-1942">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1942">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="d2504-1943">Interactive</span><span class="sxs-lookup"><span data-stu-id="d2504-1943">Interactive</span></span>

* <span data-ttu-id="d2504-1944">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1944">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="d2504-1945">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-1945">Network</span></span>

* <span data-ttu-id="d2504-1946">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1946">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="d2504-1947">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1947">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="d2504-1948">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1948">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="d2504-1949">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1949">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="d2504-1950">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1950">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="d2504-1951">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-1951">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="d2504-1952">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1952">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="d2504-1953">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1953">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="d2504-1954">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1954">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="d2504-1955">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1955">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="d2504-1956">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-1956">Profile</span></span>

* <span data-ttu-id="d2504-1957">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1957">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-1958">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-1958">Resource</span></span>

* <span data-ttu-id="d2504-1959">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1959">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-1960">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-1960">Storage</span></span>

* <span data-ttu-id="d2504-1961">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1961">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="d2504-1962">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1962">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="d2504-1963">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1963">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="d2504-1964">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1964">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="d2504-1965">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1965">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-1966">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-1966">VM</span></span>

* <span data-ttu-id="d2504-1967">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1967">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="d2504-1968">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1968">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="d2504-1969">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1969">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="d2504-1970">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1970">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="d2504-1971">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="d2504-1971">January 17, 2018</span></span>

<span data-ttu-id="d2504-1972">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="d2504-1972">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-1973">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-1973">ACR</span></span>

* <span data-ttu-id="d2504-1974">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1974">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="d2504-1975">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-1975">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-1976">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-1976">ACS</span></span>

* <span data-ttu-id="d2504-1977">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1977">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="d2504-1978">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1978">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-1979">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-1979">Appservice</span></span>

* <span data-ttu-id="d2504-1980">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1980">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="d2504-1981">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1981">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="d2504-1982">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1982">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="d2504-1983">バックアップ</span><span class="sxs-lookup"><span data-stu-id="d2504-1983">Backup</span></span>

* <span data-ttu-id="d2504-1984">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1984">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="d2504-1985">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1985">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="d2504-1986">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1986">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="d2504-1987">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1987">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="d2504-1988">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1988">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-1989">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-1989">Batch</span></span>

* <span data-ttu-id="d2504-1990">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1990">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="d2504-1991">クラウド</span><span class="sxs-lookup"><span data-stu-id="d2504-1991">Cloud</span></span>

* <span data-ttu-id="d2504-1992">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1992">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="d2504-1993">消費</span><span class="sxs-lookup"><span data-stu-id="d2504-1993">Consumption</span></span>

* <span data-ttu-id="d2504-1994">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1994">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="d2504-1995">Event Grid</span><span class="sxs-lookup"><span data-stu-id="d2504-1995">Event Grid</span></span>

* <span data-ttu-id="d2504-1996">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1996">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="d2504-1997">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1997">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="d2504-1998">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-1998">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="d2504-1999">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="d2504-1999">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="d2504-2000">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2000">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="d2504-2001">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2001">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="d2504-2002">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2002">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="d2504-2003">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2003">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="d2504-2004">Interactive</span><span class="sxs-lookup"><span data-stu-id="d2504-2004">Interactive</span></span>

* <span data-ttu-id="d2504-2005">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2005">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="d2504-2006">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2006">Fixed errors on startup</span></span>
* <span data-ttu-id="d2504-2007">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2007">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="d2504-2008">IoT</span><span class="sxs-lookup"><span data-stu-id="d2504-2008">IoT</span></span>

* <span data-ttu-id="d2504-2009">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2009">Added support for device provisioning service</span></span>
* <span data-ttu-id="d2504-2010">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2010">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="d2504-2011">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2011">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-2012">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-2012">Monitor</span></span>

* <span data-ttu-id="d2504-2013">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2013">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="d2504-2014">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2014">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="d2504-2015">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2015">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="d2504-2016">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-2016">Network</span></span>

* <span data-ttu-id="d2504-2017">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2017">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="d2504-2018">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2018">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="d2504-2019">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-2019">Profile</span></span>

* <span data-ttu-id="d2504-2020">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2020">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="d2504-2021">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-2021">Role</span></span>

* <span data-ttu-id="d2504-2022">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2022">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="d2504-2023">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d2504-2023">Service Fabric</span></span>

* <span data-ttu-id="d2504-2024">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2024">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="d2504-2025">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2025">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-2026">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-2026">VM</span></span>

* <span data-ttu-id="d2504-2027">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="d2504-2027">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="d2504-2028">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2028">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="d2504-2029">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2029">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="d2504-2030">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2030">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="d2504-2031">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2031">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="d2504-2032">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2032">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="d2504-2033">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2033">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="d2504-2034">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2034">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="d2504-2035">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2035">December 19, 2017</span></span>

<span data-ttu-id="d2504-2036">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="d2504-2036">Version 2.0.23</span></span>

* <span data-ttu-id="d2504-2037">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2037">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="d2504-2038">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-2038">Container</span></span>

* <span data-ttu-id="d2504-2039">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2039">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="d2504-2040">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-2040">Network</span></span>

* <span data-ttu-id="d2504-2041">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2041">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="d2504-2042">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2042">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-2043">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-2043">Storage</span></span>

* <span data-ttu-id="d2504-2044">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2044">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-2045">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-2045">VM</span></span>

* <span data-ttu-id="d2504-2046">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2046">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="d2504-2047">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2047">December 5, 2017</span></span>

<span data-ttu-id="d2504-2048">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="d2504-2048">Version 2.0.22</span></span>

* <span data-ttu-id="d2504-2049">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-2049">Removed `az component` commands.</span></span> <span data-ttu-id="d2504-2050">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="d2504-2050">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="d2504-2051">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-2051">Core</span></span>
* <span data-ttu-id="d2504-2052">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2052">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="d2504-2053">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2053">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-2054">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-2054">ACS</span></span>

* <span data-ttu-id="d2504-2055">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2055">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="d2504-2056">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2056">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="d2504-2057">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2057">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="d2504-2058">Advisor</span><span class="sxs-lookup"><span data-stu-id="d2504-2058">Advisor</span></span>

* <span data-ttu-id="d2504-2059">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="d2504-2059">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-2060">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-2060">Appservice</span></span>

* <span data-ttu-id="d2504-2061">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2061">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="d2504-2062">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2062">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="d2504-2063">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2063">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="d2504-2064">消費</span><span class="sxs-lookup"><span data-stu-id="d2504-2064">Consumption</span></span>

* <span data-ttu-id="d2504-2065">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2065">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="d2504-2066">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-2066">Container</span></span>

* <span data-ttu-id="d2504-2067">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2067">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-2068">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-2068">Monitor</span></span>

* <span data-ttu-id="d2504-2069">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2069">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-2070">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-2070">Resource</span></span>

* <span data-ttu-id="d2504-2071">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2071">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="d2504-2072">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-2072">Role</span></span>

* <span data-ttu-id="d2504-2073">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2073">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="d2504-2074">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="d2504-2074">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="d2504-2075">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2075">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-2076">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-2076">SQL</span></span>

* <span data-ttu-id="d2504-2077">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2077">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="d2504-2078">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2078">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-2079">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-2079">VM</span></span>

* <span data-ttu-id="d2504-2080">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2080">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="d2504-2081">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2081">November 14, 2017</span></span>

<span data-ttu-id="d2504-2082">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="d2504-2082">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-2083">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-2083">ACR</span></span>

* <span data-ttu-id="d2504-2084">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2084">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="d2504-2085">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-2085">ACS</span></span>

* <span data-ttu-id="d2504-2086">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2086">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="d2504-2087">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-2087">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="d2504-2088">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2088">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="d2504-2089">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2089">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="d2504-2090">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2090">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-2091">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-2091">Appservice</span></span>

* <span data-ttu-id="d2504-2092">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2092">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="d2504-2093">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2093">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="d2504-2094">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2094">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="d2504-2095">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2095">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="d2504-2096">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2096">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="d2504-2097">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="d2504-2097">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-2098">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-2098">Batch</span></span>

* <span data-ttu-id="d2504-2099">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2099">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="d2504-2100">Batchai</span><span class="sxs-lookup"><span data-stu-id="d2504-2100">Batchai</span></span>

* <span data-ttu-id="d2504-2101">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2101">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="d2504-2102">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2102">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="d2504-2103">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2103">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="d2504-2104">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2104">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="d2504-2105">クラウド</span><span class="sxs-lookup"><span data-stu-id="d2504-2105">Cloud</span></span>

* <span data-ttu-id="d2504-2106">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2106">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="d2504-2107">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-2107">Container</span></span>

* <span data-ttu-id="d2504-2108">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2108">Added support to open multiple ports</span></span>
* <span data-ttu-id="d2504-2109">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2109">Added container group restart policy</span></span>
* <span data-ttu-id="d2504-2110">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2110">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="d2504-2111">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2111">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="d2504-2112">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="d2504-2112">Data Lake Analytics</span></span>

* <span data-ttu-id="d2504-2113">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2113">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="d2504-2114">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="d2504-2114">Data Lake Store</span></span>

* <span data-ttu-id="d2504-2115">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2115">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="d2504-2116">拡張機能</span><span class="sxs-lookup"><span data-stu-id="d2504-2116">Extension</span></span>

* <span data-ttu-id="d2504-2117">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2117">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="d2504-2118">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2118">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="d2504-2119">IoT</span><span class="sxs-lookup"><span data-stu-id="d2504-2119">IoT</span></span>

* <span data-ttu-id="d2504-2120">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2120">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-2121">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-2121">Monitor</span></span>

* <span data-ttu-id="d2504-2122">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2122">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="d2504-2123">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-2123">Network</span></span>

* <span data-ttu-id="d2504-2124">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2124">Added support for CAA DNS records</span></span>
* <span data-ttu-id="d2504-2125">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2125">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="d2504-2126">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2126">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="d2504-2127">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2127">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="d2504-2128">Reservations</span><span class="sxs-lookup"><span data-stu-id="d2504-2128">Reservations</span></span>

* <span data-ttu-id="d2504-2129">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="d2504-2129">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-2130">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-2130">Resource</span></span>

* <span data-ttu-id="d2504-2131">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2131">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-2132">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-2132">SQL</span></span>

* <span data-ttu-id="d2504-2133">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2133">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-2134">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-2134">Storage</span></span>

* <span data-ttu-id="d2504-2135">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2135">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="d2504-2136">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2136">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="d2504-2137">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2137">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="d2504-2138">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2138">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="d2504-2139">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2139">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="d2504-2140">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2140">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="d2504-2141">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2141">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-2142">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-2142">VM</span></span>

* <span data-ttu-id="d2504-2143">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2143">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="d2504-2144">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2144">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="d2504-2145">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2145">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="d2504-2146">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2146">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="d2504-2147">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2147">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="d2504-2148">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2148">October 24, 2017</span></span>

<span data-ttu-id="d2504-2149">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="d2504-2149">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="d2504-2150">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-2150">Core</span></span>

* <span data-ttu-id="d2504-2151">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2151">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-2152">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-2152">ACR</span></span>

* <span data-ttu-id="d2504-2153">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2153">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="d2504-2154">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2154">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="d2504-2155">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2155">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-2156">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-2156">ACS</span></span>

* <span data-ttu-id="d2504-2157">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2157">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="d2504-2158">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2158">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-2159">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-2159">Appservice</span></span>

* <span data-ttu-id="d2504-2160">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2160">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="d2504-2161">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d2504-2161">Component</span></span>

* <span data-ttu-id="d2504-2162">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2162">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-2163">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-2163">Monitor</span></span>

* <span data-ttu-id="d2504-2164">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2164">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-2165">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-2165">Resource</span></span>

* <span data-ttu-id="d2504-2166">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2166">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="d2504-2167">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2167">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-2168">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-2168">VM</span></span>

* <span data-ttu-id="d2504-2169">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2169">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="d2504-2170">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2170">October 9, 2017</span></span>

<span data-ttu-id="d2504-2171">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="d2504-2171">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="d2504-2172">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-2172">Core</span></span>

* <span data-ttu-id="d2504-2173">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2173">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-2174">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-2174">Appservice</span></span>

* <span data-ttu-id="d2504-2175">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2175">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-2176">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-2176">Batch</span></span>

* <span data-ttu-id="d2504-2177">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2177">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="d2504-2178">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2178">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="d2504-2179">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2179">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="d2504-2180">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2180">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="d2504-2181">Batchai</span><span class="sxs-lookup"><span data-stu-id="d2504-2181">Batchai</span></span>

* <span data-ttu-id="d2504-2182">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="d2504-2182">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="d2504-2183">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d2504-2183">Keyvault</span></span>

* <span data-ttu-id="d2504-2184">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-2184">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="d2504-2185">(#4448)</span><span class="sxs-lookup"><span data-stu-id="d2504-2185">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="d2504-2186">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-2186">Network</span></span>

* <span data-ttu-id="d2504-2187">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2187">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="d2504-2188">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2188">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-2189">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-2189">Resource</span></span>

* <span data-ttu-id="d2504-2190">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2190">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="d2504-2191">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2191">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="d2504-2192">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2192">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="d2504-2193">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2193">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-2194">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-2194">Sql</span></span>

* <span data-ttu-id="d2504-2195">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2195">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="d2504-2196">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="d2504-2196">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="d2504-2197">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="d2504-2197">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-2198">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-2198">Storage</span></span>

* <span data-ttu-id="d2504-2199">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2199">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-2200">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-2200">Vm</span></span>

* <span data-ttu-id="d2504-2201">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2201">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="d2504-2202">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2202">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="d2504-2203">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2203">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="d2504-2204">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2204">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="d2504-2205">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2205">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="d2504-2206">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2206">September 22, 2017</span></span>

<span data-ttu-id="d2504-2207">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="d2504-2207">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-2208">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-2208">Resource</span></span>

* <span data-ttu-id="d2504-2209">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2209">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="d2504-2210">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2210">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="d2504-2211">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2211">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="d2504-2212">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2212">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="d2504-2213">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-2213">Network</span></span>

* <span data-ttu-id="d2504-2214">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2214">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="d2504-2215">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2215">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="d2504-2216">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2216">Added `asg` application security group commands</span></span>
* <span data-ttu-id="d2504-2217">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2217">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="d2504-2218">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2218">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="d2504-2219">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2219">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="d2504-2220">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2220">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-2221">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-2221">Storage</span></span>

* <span data-ttu-id="d2504-2222">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2222">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="d2504-2223">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="d2504-2223">Eventgrid</span></span>

* <span data-ttu-id="d2504-2224">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2224">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-2225">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-2225">SQL</span></span>

* <span data-ttu-id="d2504-2226">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-2226">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="d2504-2227">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="d2504-2227">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="d2504-2228">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2228">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="d2504-2229">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d2504-2229">Keyvault</span></span>

* <span data-ttu-id="d2504-2230">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2230">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-2231">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-2231">VM</span></span>

* <span data-ttu-id="d2504-2232">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2232">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="d2504-2233">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2233">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="d2504-2234">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2234">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="d2504-2235">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2235">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="d2504-2236">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2236">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="d2504-2237">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2237">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-2238">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-2238">ACS</span></span>

* <span data-ttu-id="d2504-2239">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2239">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-2240">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-2240">Appservice</span></span>

* <span data-ttu-id="d2504-2241">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2241">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="d2504-2242">バックアップ</span><span class="sxs-lookup"><span data-stu-id="d2504-2242">Backup</span></span>

* <span data-ttu-id="d2504-2243">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="d2504-2243">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="d2504-2244">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2244">September 11, 2017</span></span>

<span data-ttu-id="d2504-2245">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="d2504-2245">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="d2504-2246">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-2246">Core</span></span>

* <span data-ttu-id="d2504-2247">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-2247">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="d2504-2248">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2248">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-2249">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-2249">Acs</span></span>

* <span data-ttu-id="d2504-2250">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2250">Added `acs list-locations` command</span></span>
* <span data-ttu-id="d2504-2251">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="d2504-2251">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-2252">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-2252">Appservice</span></span>

* <span data-ttu-id="d2504-2253">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2253">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="d2504-2254">CDN</span><span class="sxs-lookup"><span data-stu-id="d2504-2254">CDN</span></span>

* <span data-ttu-id="d2504-2255">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2255">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="d2504-2256">拡張機能</span><span class="sxs-lookup"><span data-stu-id="d2504-2256">Extension</span></span>

* <span data-ttu-id="d2504-2257">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="d2504-2257">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="d2504-2258">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d2504-2258">Keyvault</span></span>

* <span data-ttu-id="d2504-2259">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2259">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="d2504-2260">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-2260">Network</span></span>

* <span data-ttu-id="d2504-2261">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2261">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="d2504-2262">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2262">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="d2504-2263">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2263">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="d2504-2264">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2264">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="d2504-2265">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2265">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-2266">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-2266">Resource</span></span>

* <span data-ttu-id="d2504-2267">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="d2504-2267">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="d2504-2268">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="d2504-2268">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="d2504-2269">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="d2504-2269">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="d2504-2270">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="d2504-2270">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-2271">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-2271">SQL</span></span>

* <span data-ttu-id="d2504-2272">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2272">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-2273">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-2273">VM</span></span>

* <span data-ttu-id="d2504-2274">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="d2504-2274">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="d2504-2275">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="d2504-2275">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="d2504-2276">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2276">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="d2504-2277">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="d2504-2277">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="d2504-2278">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="d2504-2278">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="d2504-2279">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2279">August 31, 2017</span></span>

<span data-ttu-id="d2504-2280">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="d2504-2280">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="d2504-2281">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d2504-2281">Keyvault</span></span>

* <span data-ttu-id="d2504-2282">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2282">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="d2504-2283">SF</span><span class="sxs-lookup"><span data-stu-id="d2504-2283">Sf</span></span>

* <span data-ttu-id="d2504-2284">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="d2504-2284">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-2285">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-2285">Storage</span></span>

* <span data-ttu-id="d2504-2286">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2286">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="d2504-2287">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="d2504-2287">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="d2504-2288">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2288">August 28, 2017</span></span>

<span data-ttu-id="d2504-2289">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="d2504-2289">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="d2504-2290">CLI</span><span class="sxs-lookup"><span data-stu-id="d2504-2290">CLI</span></span>

* <span data-ttu-id="d2504-2291">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2291">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-2292">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-2292">ACS</span></span>

* <span data-ttu-id="d2504-2293">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2293">Corrected preview regions</span></span>
* <span data-ttu-id="d2504-2294">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-2294">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="d2504-2295">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2295">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-2296">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-2296">Appservice</span></span>

* <span data-ttu-id="d2504-2297">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2297">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="d2504-2298">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2298">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="d2504-2299">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2299">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="d2504-2300">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2300">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="d2504-2301">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="d2504-2301">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="d2504-2302">IoT</span><span class="sxs-lookup"><span data-stu-id="d2504-2302">IoT</span></span>

* <span data-ttu-id="d2504-2303">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2303">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="d2504-2304">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-2304">Network</span></span>

* <span data-ttu-id="d2504-2305">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2305">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="d2504-2306">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2306">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="d2504-2307">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2307">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="d2504-2308">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2308">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="d2504-2309">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2309">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="d2504-2310">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-2310">Profile</span></span>

* <span data-ttu-id="d2504-2311">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2311">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="d2504-2312">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d2504-2312">Service Fabric</span></span>

* <span data-ttu-id="d2504-2313">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="d2504-2313">Preview release</span></span>
* <span data-ttu-id="d2504-2314">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2314">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="d2504-2315">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2315">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="d2504-2316">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2316">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-2317">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-2317">Storage</span></span>

* <span data-ttu-id="d2504-2318">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-2318">Enabled setting blob tier</span></span>
* <span data-ttu-id="d2504-2319">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2319">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="d2504-2320">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2320">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="d2504-2321">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-2321">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="d2504-2322">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2322">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="d2504-2323">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="d2504-2323">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-2324">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-2324">VM</span></span>

* <span data-ttu-id="d2504-2325">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2325">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="d2504-2326">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-2326">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="d2504-2327">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2327">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="d2504-2328">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2328">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="d2504-2329">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2329">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="d2504-2330">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2330">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="d2504-2331">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2331">August 15, 2017</span></span>

<span data-ttu-id="d2504-2332">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="d2504-2332">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-2333">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-2333">ACS</span></span>

* <span data-ttu-id="d2504-2334">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2334">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-2335">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-2335">Appservice</span></span>

* <span data-ttu-id="d2504-2336">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2336">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="d2504-2337">Event Grid</span><span class="sxs-lookup"><span data-stu-id="d2504-2337">Event Grid</span></span>

* <span data-ttu-id="d2504-2338">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2338">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="d2504-2339">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2339">August 11, 2017</span></span>

<span data-ttu-id="d2504-2340">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="d2504-2340">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-2341">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-2341">ACS</span></span>

* <span data-ttu-id="d2504-2342">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2342">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-2343">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-2343">Batch</span></span>

* <span data-ttu-id="d2504-2344">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2344">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="d2504-2345">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2345">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="d2504-2346">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2346">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="d2504-2347">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2347">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="d2504-2348">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2348">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="d2504-2349">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2349">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="d2504-2350">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d2504-2350">Component</span></span>

* <span data-ttu-id="d2504-2351">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2351">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="d2504-2352">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d2504-2352">Container</span></span>

* <span data-ttu-id="d2504-2353">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2353">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="d2504-2354">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="d2504-2354">Data Lake Store</span></span>

* <span data-ttu-id="d2504-2355">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-2355">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="d2504-2356">Event Grid</span><span class="sxs-lookup"><span data-stu-id="d2504-2356">Event Grid</span></span>

* <span data-ttu-id="d2504-2357">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="d2504-2357">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="d2504-2358">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-2358">Network</span></span>

* <span data-ttu-id="d2504-2359">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2359">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="d2504-2360">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2360">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="d2504-2361">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2361">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="d2504-2362">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2362">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="d2504-2363">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-2363">Profile</span></span>

* <span data-ttu-id="d2504-2364">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2364">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-2365">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-2365">Storage</span></span>

* <span data-ttu-id="d2504-2366">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="d2504-2366">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-2367">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-2367">VM</span></span>

* <span data-ttu-id="d2504-2368">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2368">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="d2504-2369">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2369">Exposed `list-skus` command</span></span>
* <span data-ttu-id="d2504-2370">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2370">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="d2504-2371">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="d2504-2371">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="d2504-2372">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2372">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="d2504-2373">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2373">July 28, 2017</span></span>

<span data-ttu-id="d2504-2374">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="d2504-2374">Version 2.0.12</span></span>

* <span data-ttu-id="d2504-2375">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2375">Added container commands</span></span>
* <span data-ttu-id="d2504-2376">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2376">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="d2504-2377">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-2377">Core</span></span>

* <span data-ttu-id="d2504-2378">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="d2504-2378">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="d2504-2379">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2379">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="d2504-2380">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="d2504-2380">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="d2504-2381">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="d2504-2381">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="d2504-2382">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="d2504-2382">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="d2504-2383">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="d2504-2383">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="d2504-2384">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="d2504-2384">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="d2504-2385">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="d2504-2385">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="d2504-2386">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="d2504-2386">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="d2504-2387">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="d2504-2387">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="d2504-2388">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="d2504-2388">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="d2504-2389">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="d2504-2389">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="d2504-2390">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2390">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="d2504-2391">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2391">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="d2504-2392">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2392">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="d2504-2393">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="d2504-2393">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="d2504-2394">ACR</span><span class="sxs-lookup"><span data-stu-id="d2504-2394">ACR</span></span>

* <span data-ttu-id="d2504-2395">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2395">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="d2504-2396">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2396">Support SKU update for managed registries</span></span>
* <span data-ttu-id="d2504-2397">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2397">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="d2504-2398">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2398">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="d2504-2399">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2399">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="d2504-2400">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2400">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-2401">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-2401">ACS</span></span>

* <span data-ttu-id="d2504-2402">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2402">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-2403">Appservice</span><span class="sxs-lookup"><span data-stu-id="d2504-2403">Appservice</span></span>

* <span data-ttu-id="d2504-2404">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2404">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="d2504-2405">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2405">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="d2504-2406">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="d2504-2406">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="d2504-2407">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="d2504-2407">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="d2504-2408">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="d2504-2408">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="d2504-2409">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="d2504-2409">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="d2504-2410">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="d2504-2410">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="d2504-2411">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="d2504-2411">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="d2504-2412">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-2412">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="d2504-2413">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="d2504-2413">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="d2504-2414">Batch</span><span class="sxs-lookup"><span data-stu-id="d2504-2414">Batch</span></span>

* <span data-ttu-id="d2504-2415">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="d2504-2415">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="d2504-2416">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2416">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="d2504-2417">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2417">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="d2504-2418">CDN</span><span class="sxs-lookup"><span data-stu-id="d2504-2418">CDN</span></span>

* <span data-ttu-id="d2504-2419">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2419">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="d2504-2420">クラウド</span><span class="sxs-lookup"><span data-stu-id="d2504-2420">Cloud</span></span>

* <span data-ttu-id="d2504-2421">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2421">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="d2504-2422">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="d2504-2422">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="d2504-2423">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2423">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="d2504-2424">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2424">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="d2504-2425">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2425">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="d2504-2426">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d2504-2426">CosmosDB</span></span>

* <span data-ttu-id="d2504-2427">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2427">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="d2504-2428">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2428">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="d2504-2429">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="d2504-2429">Data Lake Analytics</span></span>

* <span data-ttu-id="d2504-2430">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2430">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="d2504-2431">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2431">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="d2504-2432">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2432">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="d2504-2433">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="d2504-2433">Data Lake Store</span></span>

* <span data-ttu-id="d2504-2434">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2434">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="d2504-2435">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2435">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="d2504-2436">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-2436">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="d2504-2437">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="d2504-2437">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="d2504-2438">対話</span><span class="sxs-lookup"><span data-stu-id="d2504-2438">Interactive</span></span>

* <span data-ttu-id="d2504-2439">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2439">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="d2504-2440">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="d2504-2440">Increased test coverage</span></span>
* <span data-ttu-id="d2504-2441">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2441">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="d2504-2442">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="d2504-2442">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="d2504-2443">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="d2504-2443">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="d2504-2444">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="d2504-2444">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="d2504-2445">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="d2504-2445">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="d2504-2446">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2446">Added `--progress` flag</span></span>
* <span data-ttu-id="d2504-2447">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2447">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="d2504-2448">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="d2504-2448">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="d2504-2449">IoT</span><span class="sxs-lookup"><span data-stu-id="d2504-2449">IoT</span></span>

* <span data-ttu-id="d2504-2450">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-2450">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="d2504-2451">(#3934)</span><span class="sxs-lookup"><span data-stu-id="d2504-2451">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="d2504-2452">Key Vault</span><span class="sxs-lookup"><span data-stu-id="d2504-2452">Key vault</span></span>

* <span data-ttu-id="d2504-2453">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-2453">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="d2504-2454">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="d2504-2454">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="d2504-2455">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="d2504-2455">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="d2504-2456">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="d2504-2456">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="d2504-2457">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="d2504-2457">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="d2504-2458">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="d2504-2458">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="d2504-2459">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-2459">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="d2504-2460">(#3307)</span><span class="sxs-lookup"><span data-stu-id="d2504-2460">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="d2504-2461">ラボ</span><span class="sxs-lookup"><span data-stu-id="d2504-2461">Lab</span></span>

* <span data-ttu-id="d2504-2462">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2462">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="d2504-2463">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2463">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-2464">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-2464">Monitor</span></span>

* <span data-ttu-id="d2504-2465">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="d2504-2465">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="d2504-2466">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2466">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="d2504-2467">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2467">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="d2504-2468">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2468">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="d2504-2469">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2469">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="d2504-2470">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="d2504-2470">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="d2504-2471">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2471">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="d2504-2472">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="d2504-2472">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="d2504-2473">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2473">`location` no longer required</span></span>
  * <span data-ttu-id="d2504-2474">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="d2504-2474">Add name and ID support for target</span></span>
  * <span data-ttu-id="d2504-2475">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="d2504-2475">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="d2504-2476">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-2476">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="d2504-2477">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2477">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="d2504-2478">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="d2504-2478">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="d2504-2479">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2479">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="d2504-2480">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2480">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="d2504-2481">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-2481">Network</span></span>

* <span data-ttu-id="d2504-2482">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2482">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="d2504-2483">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2483">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="d2504-2484">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2484">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="d2504-2485">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2485">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="d2504-2486">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2486">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="d2504-2487">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2487">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="d2504-2488">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2488">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="d2504-2489">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2489">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="d2504-2490">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2490">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="d2504-2491">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2491">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="d2504-2492">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2492">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="d2504-2493">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2493">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="d2504-2494">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2494">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="d2504-2495">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2495">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="d2504-2496">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2496">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="d2504-2497">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2497">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="d2504-2498">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2498">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="d2504-2499">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2499">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="d2504-2500">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2500">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="d2504-2501">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2501">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="d2504-2502">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2502">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="d2504-2503">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2503">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="d2504-2504">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2504">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="d2504-2505">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="d2504-2505">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="d2504-2506">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="d2504-2506">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="d2504-2507">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="d2504-2507">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="d2504-2508">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="d2504-2508">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="d2504-2509">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-2509">Profile</span></span>

* <span data-ttu-id="d2504-2510">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2510">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="d2504-2511">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2511">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="d2504-2512">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="d2504-2512">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="d2504-2513">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2513">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="d2504-2514">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2514">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="d2504-2515">RDBMS</span><span class="sxs-lookup"><span data-stu-id="d2504-2515">RDBMS</span></span>

* <span data-ttu-id="d2504-2516">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="d2504-2516">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="d2504-2517">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="d2504-2517">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="d2504-2518">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="d2504-2518">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="d2504-2519">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="d2504-2519">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-2520">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-2520">Resource</span></span>

* <span data-ttu-id="d2504-2521">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2521">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="d2504-2522">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2522">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="d2504-2523">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2523">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="d2504-2524">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2524">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="d2504-2525">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="d2504-2525">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="d2504-2526">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2526">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="d2504-2527">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="d2504-2527">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="d2504-2528">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2528">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="d2504-2529">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-2529">Role</span></span>

* <span data-ttu-id="d2504-2530">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2530">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="d2504-2531">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="d2504-2531">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="d2504-2532">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="d2504-2532">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="d2504-2533">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="d2504-2533">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="d2504-2534">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2534">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="d2504-2535">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d2504-2535">Service Fabric</span></span>
* <span data-ttu-id="d2504-2536">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="d2504-2536">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="d2504-2537">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="d2504-2537">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="d2504-2538">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="d2504-2538">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-2539">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-2539">SQL</span></span>

* <span data-ttu-id="d2504-2540">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2540">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="d2504-2541">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2541">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="d2504-2542">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2542">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-2543">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-2543">Storage</span></span>

* <span data-ttu-id="d2504-2544">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="d2504-2544">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="d2504-2545">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-2545">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="d2504-2546">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="d2504-2546">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="d2504-2547">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="d2504-2547">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="d2504-2548">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="d2504-2548">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="d2504-2549">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="d2504-2549">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-2550">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-2550">VM</span></span>

* <span data-ttu-id="d2504-2551">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2551">Support configuring nsg</span></span>
* <span data-ttu-id="d2504-2552">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2552">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="d2504-2553">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="d2504-2553">Support managed service identities</span></span>
* <span data-ttu-id="d2504-2554">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2554">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="d2504-2555">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="d2504-2555">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="d2504-2556">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2556">May 10, 2017</span></span>

<span data-ttu-id="d2504-2557">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="d2504-2557">Version 2.0.6</span></span>

* <span data-ttu-id="d2504-2558">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2558">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="d2504-2559">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2559">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="d2504-2560">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2560">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="d2504-2561">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2561">Include Cognitive Services module</span></span>
* <span data-ttu-id="d2504-2562">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2562">Include Service Fabric module</span></span>
* <span data-ttu-id="d2504-2563">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="d2504-2563">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="d2504-2564">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2564">Add support for CDN commands</span></span>
* <span data-ttu-id="d2504-2565">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2565">Remove Container module</span></span>
* <span data-ttu-id="d2504-2566">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="d2504-2566">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="d2504-2567">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="d2504-2567">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="d2504-2568">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-2568">Core</span></span>

* <span data-ttu-id="d2504-2569">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="d2504-2569">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="d2504-2570">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="d2504-2570">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="d2504-2571">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="d2504-2571">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="d2504-2572">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="d2504-2572">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="d2504-2573">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="d2504-2573">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="d2504-2574">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="d2504-2574">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="d2504-2575">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="d2504-2575">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="d2504-2576">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="d2504-2576">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="d2504-2577">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="d2504-2577">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="d2504-2578">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="d2504-2578">core: Improved performance</span></span>
* <span data-ttu-id="d2504-2579">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="d2504-2579">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="d2504-2580">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="d2504-2580">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-2581">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-2581">ACS</span></span>

* <span data-ttu-id="d2504-2582">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2582">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="d2504-2583">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2583">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="d2504-2584">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2584">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="d2504-2585">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="d2504-2585">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-2586">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-2586">AppService</span></span>

* <span data-ttu-id="d2504-2587">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2587">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="d2504-2588">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2588">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="d2504-2589">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="d2504-2589">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="d2504-2590">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2590">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="d2504-2591">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2591">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="d2504-2592">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="d2504-2592">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="d2504-2593">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="d2504-2593">support slot swap with preview</span></span>
* <span data-ttu-id="d2504-2594">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="d2504-2594">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="d2504-2595">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="d2504-2595">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="d2504-2596">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d2504-2596">CosmosDB</span></span>

* <span data-ttu-id="d2504-2597">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2597">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="d2504-2598">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2598">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="d2504-2599">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2599">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="d2504-2600">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2600">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="d2504-2601">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="d2504-2601">Data Lake Analytics</span></span>

* <span data-ttu-id="d2504-2602">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2602">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="d2504-2603">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="d2504-2603">Add support for new catalog item type: package.</span></span> <span data-ttu-id="d2504-2604">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="d2504-2604">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="d2504-2605">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="d2504-2605">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="d2504-2606">テーブル</span><span class="sxs-lookup"><span data-stu-id="d2504-2606">Table</span></span>
  * <span data-ttu-id="d2504-2607">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="d2504-2607">Table valued function</span></span>
  * <span data-ttu-id="d2504-2608">表示</span><span class="sxs-lookup"><span data-stu-id="d2504-2608">View</span></span>
  * <span data-ttu-id="d2504-2609">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="d2504-2609">Table Statistics.</span></span> <span data-ttu-id="d2504-2610">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="d2504-2610">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="d2504-2611">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="d2504-2611">Data Lake Store</span></span>

* <span data-ttu-id="d2504-2612">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2612">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="d2504-2613">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="d2504-2613">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="d2504-2614">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="d2504-2614">missed help for access show.</span></span> <span data-ttu-id="d2504-2615">追加しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2615">adding it.</span></span> <span data-ttu-id="d2504-2616">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="d2504-2616">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="d2504-2617">検索</span><span class="sxs-lookup"><span data-stu-id="d2504-2617">Find</span></span>

* <span data-ttu-id="d2504-2618">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="d2504-2618">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="d2504-2619">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d2504-2619">KeyVault</span></span>

* <span data-ttu-id="d2504-2620">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2620">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="d2504-2621">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2621">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="d2504-2622">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="d2504-2622">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="d2504-2623">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2623">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="d2504-2624">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="d2504-2624">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="d2504-2625">ラボ</span><span class="sxs-lookup"><span data-stu-id="d2504-2625">Lab</span></span>

* <span data-ttu-id="d2504-2626">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2626">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="d2504-2627">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2627">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="d2504-2628">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2628">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="d2504-2629">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2629">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="d2504-2630">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2630">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="d2504-2631">監視</span><span class="sxs-lookup"><span data-stu-id="d2504-2631">Monitor</span></span>

* <span data-ttu-id="d2504-2632">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="d2504-2632">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="d2504-2633">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="d2504-2633">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="d2504-2634">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-2634">Network</span></span>

* <span data-ttu-id="d2504-2635">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2635">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="d2504-2636">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2636">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="d2504-2637">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2637">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="d2504-2638">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2638">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="d2504-2639">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2639">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="d2504-2640">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2640">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="d2504-2641">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2641">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="d2504-2642">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2642">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="d2504-2643">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2643">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="d2504-2644">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2644">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="d2504-2645">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2645">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="d2504-2646">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2646">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="d2504-2647">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2647">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="d2504-2648">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2648">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="d2504-2649">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d2504-2649">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="d2504-2650">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2650">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="d2504-2651">プロファイル</span><span class="sxs-lookup"><span data-stu-id="d2504-2651">Profile</span></span>

* <span data-ttu-id="d2504-2652">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="d2504-2652">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="d2504-2653">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="d2504-2653">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="d2504-2654">Redis</span><span class="sxs-lookup"><span data-stu-id="d2504-2654">Redis</span></span>

* <span data-ttu-id="d2504-2655">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2655">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="d2504-2656">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2656">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="d2504-2657">Resource</span><span class="sxs-lookup"><span data-stu-id="d2504-2657">Resource</span></span>

* <span data-ttu-id="d2504-2658">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="d2504-2658">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="d2504-2659">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="d2504-2659">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="d2504-2660">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="d2504-2660">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="d2504-2661">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2661">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="d2504-2662">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="d2504-2662">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="d2504-2663">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2663">Add docs for az lock update.</span></span> <span data-ttu-id="d2504-2664">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="d2504-2664">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="d2504-2665">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="d2504-2665">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="d2504-2666">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="d2504-2666">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="d2504-2667">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="d2504-2667">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="d2504-2668">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="d2504-2668">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="d2504-2669">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="d2504-2669">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="d2504-2670">Role</span><span class="sxs-lookup"><span data-stu-id="d2504-2670">Role</span></span>

* <span data-ttu-id="d2504-2671">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="d2504-2671">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="d2504-2672">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="d2504-2672">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="d2504-2673">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="d2504-2673">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="d2504-2674">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="d2504-2674">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="d2504-2675">SQL</span><span class="sxs-lookup"><span data-stu-id="d2504-2675">SQL</span></span>

* <span data-ttu-id="d2504-2676">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2504-2676">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="d2504-2677">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="d2504-2677">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="d2504-2678">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-2678">Storage</span></span>

* <span data-ttu-id="d2504-2679">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="d2504-2679">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="d2504-2680">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2680">Add support for incremental blob copy</span></span>
* <span data-ttu-id="d2504-2681">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2681">Add support for large block blob upload</span></span>
* <span data-ttu-id="d2504-2682">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="d2504-2682">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-2683">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-2683">VM</span></span>

* <span data-ttu-id="d2504-2684">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="d2504-2684">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="d2504-2685">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="d2504-2685">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="d2504-2686">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="d2504-2686">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="d2504-2687">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="d2504-2687">az vm/vmss disk</span></span>
  3. <span data-ttu-id="d2504-2688">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="d2504-2688">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="d2504-2689">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="d2504-2689">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="d2504-2690">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="d2504-2690">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="d2504-2691">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2691">April 3, 2017</span></span>

<span data-ttu-id="d2504-2692">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="d2504-2692">Version 2.0.2</span></span>

<span data-ttu-id="d2504-2693">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="d2504-2693">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="d2504-2694">コア</span><span class="sxs-lookup"><span data-stu-id="d2504-2694">Core</span></span>

* <span data-ttu-id="d2504-2695">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="d2504-2695">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="d2504-2696">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="d2504-2696">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="d2504-2697">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="d2504-2697">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="d2504-2698">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="d2504-2698">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="d2504-2699">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="d2504-2699">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="d2504-2700">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="d2504-2700">Add prompting for missing template parameters.</span></span> <span data-ttu-id="d2504-2701">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="d2504-2701">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="d2504-2702">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="d2504-2702">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="d2504-2703">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="d2504-2703">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="d2504-2704">ACS</span><span class="sxs-lookup"><span data-stu-id="d2504-2704">ACS</span></span>

* <span data-ttu-id="d2504-2705">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="d2504-2705">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="d2504-2706">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="d2504-2706">Add support for ssh key password prompting.</span></span> <span data-ttu-id="d2504-2707">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="d2504-2707">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="d2504-2708">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="d2504-2708">Add support for windows clusters.</span></span> <span data-ttu-id="d2504-2709">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="d2504-2709">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="d2504-2710">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="d2504-2710">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="d2504-2711">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="d2504-2711">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="d2504-2712">AppService</span><span class="sxs-lookup"><span data-stu-id="d2504-2712">AppService</span></span>

* <span data-ttu-id="d2504-2713">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="d2504-2713">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="d2504-2714">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="d2504-2714">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="d2504-2715">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="d2504-2715">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="d2504-2716">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="d2504-2716">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="d2504-2717">DataLake</span><span class="sxs-lookup"><span data-stu-id="d2504-2717">DataLake</span></span>

* <span data-ttu-id="d2504-2718">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="d2504-2718">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="d2504-2719">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="d2504-2719">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="d2504-2720">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="d2504-2720">DocuemntDB</span></span>

* <span data-ttu-id="d2504-2721">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="d2504-2721">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="d2504-2722">VM</span><span class="sxs-lookup"><span data-stu-id="d2504-2722">VM</span></span>

* <span data-ttu-id="d2504-2723">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="d2504-2723">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="d2504-2724">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="d2504-2724">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="d2504-2725">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="d2504-2725">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="d2504-2726">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="d2504-2726">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="d2504-2727">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="d2504-2727">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="d2504-2728">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="d2504-2728">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="d2504-2729">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="d2504-2729">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="d2504-2730">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="d2504-2730">February 27, 2017</span></span>

<span data-ttu-id="d2504-2731">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="d2504-2731">Version 2.0.0</span></span>

<span data-ttu-id="d2504-2732">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="d2504-2732">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="d2504-2733">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="d2504-2733">Container Service (acs)</span></span>
- <span data-ttu-id="d2504-2734">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="d2504-2734">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="d2504-2735">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d2504-2735">Networking</span></span>
- <span data-ttu-id="d2504-2736">Storage</span><span class="sxs-lookup"><span data-stu-id="d2504-2736">Storage</span></span>

<span data-ttu-id="d2504-2737">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="d2504-2737">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="d2504-2738">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="d2504-2738">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="d2504-2739">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="d2504-2739">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="d2504-2740">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="d2504-2740">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="d2504-2741">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="d2504-2741">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="d2504-2742">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="d2504-2742">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="d2504-2743">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="d2504-2743">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="d2504-2744">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="d2504-2744">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="d2504-2745">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="d2504-2745">Provide feedback from the command line with the `az feedback` command</span></span>

