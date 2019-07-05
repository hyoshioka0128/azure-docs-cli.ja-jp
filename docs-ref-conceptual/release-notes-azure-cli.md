---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 07/02/2019
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 26757193628cff65603a04e440f9e2aa7bf5a248
ms.sourcegitcommit: e06d34682710e77840b0c51f4718184101bd8a03
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "67527304"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="eab41-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="eab41-103">Azure CLI release notes</span></span>

## <a name="july-2-2019"></a><span data-ttu-id="eab41-104">2019 年 7 月 2 日</span><span class="sxs-lookup"><span data-stu-id="eab41-104">July 2, 2019</span></span>

<span data-ttu-id="eab41-105">バージョン 2.0.68</span><span class="sxs-lookup"><span data-stu-id="eab41-105">Version 2.0.68</span></span>

### <a name="core"></a><span data-ttu-id="eab41-106">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-106">Core</span></span>

* <span data-ttu-id="eab41-107">コマンド モジュールが再頒布可能な 1 つの Python コードに統合されました。</span><span class="sxs-lookup"><span data-stu-id="eab41-107">Command modules are now consolidated into a single Python distributable.</span></span> <span data-ttu-id="eab41-108">これにより、PyPI での多くの `azure-cli-` パッケージの直接使用が廃止されます。</span><span class="sxs-lookup"><span data-stu-id="eab41-108">This deprecates direct use of many `azure-cli-` packages on PyPI.</span></span>
  <span data-ttu-id="eab41-109">またこれにより、インストール サイズが削減され、`pip` 経由で直接インストールしたユーザーにのみ影響が出ます。</span><span class="sxs-lookup"><span data-stu-id="eab41-109">This should reduce install size and only affect users who have directly installed via `pip`.</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-110">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-110">ACR</span></span>

* <span data-ttu-id="eab41-111">タスクへのタイマー トリガーのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-111">Added support for Timer Triggers to Task</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-112">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-112">Appservice</span></span>

* <span data-ttu-id="eab41-113">既定でアプリケーション インサイトを有効にするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-113">Changed `functionapp create` to enable application insights by default</span></span>
* <span data-ttu-id="eab41-114">[重大な変更] 非推奨の `functionapp devops-build` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-114">[BREAKING CHANGE] Removed deprecated `functionapp devops-build` command.</span></span>
  *  <span data-ttu-id="eab41-115">代わりに新しいコマンド `az functionapp devops-pipeline` を使用</span><span class="sxs-lookup"><span data-stu-id="eab41-115">Use the new command `az functionapp devops-pipeline` instead</span></span>
* <span data-ttu-id="eab41-116">Linux 従量課金プランの関数アプリのプラン サポートを `functionapp deployment config-zip` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-116">Added Linux Consumption function app plan support to `functionapp deployment config-zip`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="eab41-117">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="eab41-117">Cosmos DB</span></span>

* <span data-ttu-id="eab41-118">ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-118">Added support for disabling TTL</span></span>

### <a name="dls"></a><span data-ttu-id="eab41-119">DLS</span><span class="sxs-lookup"><span data-stu-id="eab41-119">DLS</span></span>

* <span data-ttu-id="eab41-120">ADLS バージョンを更新しました (0.0.45)</span><span class="sxs-lookup"><span data-stu-id="eab41-120">Updated ADLS version (0.0.45)</span></span>

### <a name="feedback"></a><span data-ttu-id="eab41-121">フィードバック</span><span class="sxs-lookup"><span data-stu-id="eab41-121">Feedback</span></span>

* <span data-ttu-id="eab41-122">失敗した拡張機能コマンドを報告するときに、`az feedback` はインデックスからの拡張機能のプロジェクト/リポジトリの url にブラウザーを開こうとするようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-122">When reporting a failed extension command, `az feedback` now attempts to open the browser to the project/repo url of the extension from the index</span></span>

### <a name="hdinsight"></a><span data-ttu-id="eab41-123">HDInsight</span><span class="sxs-lookup"><span data-stu-id="eab41-123">HDInsight</span></span>

* <span data-ttu-id="eab41-124">[重大な変更] `oms` コマンド グループ名を `monitor` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-124">[BREAKING CHANGE] Changed `oms` command group name to `monitor`</span></span>
* <span data-ttu-id="eab41-125">[重大な変更] `--http-password/-p` が必須パラメーターになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-125">[BREAKING CHANGE] Made `--http-password/-p` a required parameter</span></span> 
* <span data-ttu-id="eab41-126">`--cluster-admin-account` および `cluster-users-group-dns` パラメーター入力候補の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-126">Added completers for `--cluster-admin-account` and `cluster-users-group-dns` parameters completer</span></span> 
* <span data-ttu-id="eab41-127">`cluster-users-group-dns` パラメーターを `—esp` が存在するときに必要となるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-127">Changed `cluster-users-group-dns` parameter to be required when `—esp` is present</span></span>
* <span data-ttu-id="eab41-128">既存の引数自動オートコンプリートすべてにタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-128">Added a timeout for all existing argument auto-completers</span></span>
* <span data-ttu-id="eab41-129">リソース名をリソース id に変換する際のタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-129">Added a timeout for transforming resource name to resource id</span></span>
* <span data-ttu-id="eab41-130">任意のリソース グループからリソースを選択するようにオートコンプリートを変更しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-130">Changed Auto-completers to select resources from any resource group.</span></span> <span data-ttu-id="eab41-131">`-g` で指定されるリソース グループとは別のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="eab41-131">It can be a different resource group than the one specified with `-g`</span></span>
* <span data-ttu-id="eab41-132">`hdinsight application create` コマンドで `--sub-domain-suffix` および `--disable_gateway_auth` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-132">Added support for `--sub-domain-suffix` and `--disable_gateway_auth` parameters in the `hdinsight application create` command</span></span>

### <a name="managed-services"></a><span data-ttu-id="eab41-133">マネージド サービス</span><span class="sxs-lookup"><span data-stu-id="eab41-133">Managed Services</span></span>

* <span data-ttu-id="eab41-134">プレビューにマネージド サービス コマンド モジュールを導入</span><span class="sxs-lookup"><span data-stu-id="eab41-134">Introducing managed service command module in preview</span></span>

### <a name="profile"></a><span data-ttu-id="eab41-135">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-135">Profile</span></span>
* <span data-ttu-id="eab41-136">ログアウト コマンドの `--subscription` 引数を抑制</span><span class="sxs-lookup"><span data-stu-id="eab41-136">Suppress `--subscription` argument for logout command</span></span>

### <a name="rbac"></a><span data-ttu-id="eab41-137">RBAC</span><span class="sxs-lookup"><span data-stu-id="eab41-137">RBAC</span></span>

* <span data-ttu-id="eab41-138">[重大な変更] `create-for-rbac` の `--password` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-138">[BREAKING CHANGE] Removed `--password` argument for `create-for-rbac`</span></span>
* <span data-ttu-id="eab41-139">AAD グラフ サーバー レプリケーションの待機時間によって発生する断続的なエラーを回避するために `--assignee-principal-type` パラメーターを `create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-139">Added `--assignee-principal-type` parameter to `create` command to avoid intermittent failures caused by AAD graph server replication latency</span></span>
* <span data-ttu-id="eab41-140">所有オブジェクトの一覧表示時の `ad signed-in-user` のクラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-140">Fixed a crash in `ad signed-in-user` when listing owned objects</span></span>
* <span data-ttu-id="eab41-141">`ad sp` によってサービス プリンシパルから適切なアプリケーションが検出されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-141">Fixed issue where `ad sp` would not find the right application from a service principal</span></span>

### <a name="rdbms"></a><span data-ttu-id="eab41-142">RDBMS</span><span class="sxs-lookup"><span data-stu-id="eab41-142">RDBMS</span></span>

* <span data-ttu-id="eab41-143">MariaDB のレプリケーション サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-143">Added support for replication for MariaDB</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-144">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-144">SQL</span></span>

* <span data-ttu-id="eab41-145">`sql db create --sample-name` に使用できる値を文書化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-145">Documented allowed values for `sql db create --sample-name`</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-146">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-146">Storage</span></span>

* <span data-ttu-id="eab41-147">`--as-user` を使用した `storage blob generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-147">Added user delegation SAS token support with `--as-user` to `storage blob generate-sas`</span></span> 
* <span data-ttu-id="eab41-148">`--as-user` を使用した `storage container generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-148">Added user delegation SAS token support with `--as-user` to `storage container generate-sas`</span></span> 

### <a name="vm"></a><span data-ttu-id="eab41-149">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-149">VM</span></span>

* <span data-ttu-id="eab41-150">`--no-wait` による実行時に `vmss create` によってエラー メッセージが返されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-150">Fixed bug where `vmss create` returns an error message when run with `--no-wait`</span></span>
* <span data-ttu-id="eab41-151">`vmss create --single-placement-group` のクライアント側の検証を削除しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-151">Removed client-side validation for `vmss create --single-placement-group`.</span></span> <span data-ttu-id="eab41-152">`--single-placement-group` が `true` に設定され、`--instance-count` が 100 より大きいか、可用性ゾーンが指定されていても失敗にはならず、この検証はコンピューティング サービスに任されます</span><span class="sxs-lookup"><span data-stu-id="eab41-152">Does not fail if `--single-placement-group` is set to `true` and`--instance-count` is greater than 100 or availability zones are specified, but leaves this validation to the compute service</span></span>
* <span data-ttu-id="eab41-153">`--latest` と共に使用したときに `[vm|vmss] extension image list` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-153">Fixed bug where `[vm|vmss] extension image list` fails when used with `--latest`</span></span>


## <a name="june-18-2019"></a><span data-ttu-id="eab41-154">2019 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="eab41-154">June 18, 2019</span></span>

<span data-ttu-id="eab41-155">バージョン 2.0.67</span><span class="sxs-lookup"><span data-stu-id="eab41-155">Version 2.0.67</span></span>

### <a name="core"></a><span data-ttu-id="eab41-156">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-156">Core</span></span>

<span data-ttu-id="eab41-157">このリリースでは、新しい [プレビュー] タグが導入され、コマンド グループ、コマンド、または引数がプレビュー状態である場合に、お客様により明確に通知できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="eab41-157">This release introduces a new [Preview] tag to more clearly communicate to customers when a command group, command or argument is in preview status.</span></span> <span data-ttu-id="eab41-158">以前は、これはヘルプ テキストで通知されていたか、コマンド モジュールのバージョン番号によって暗黙的に通知されていました。</span><span class="sxs-lookup"><span data-stu-id="eab41-158">This was previously called out in help text or communicated implicitly by the command module version number.</span></span>
<span data-ttu-id="eab41-159">CLI では、将来、個々のパッケージのバージョン番号が削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="eab41-159">The CLI will be removing version numbers for individual packages in the future.</span></span> <span data-ttu-id="eab41-160">コマンドがプレビュー状態の場合は、そのすべての引数もプレビュー状態です。</span><span class="sxs-lookup"><span data-stu-id="eab41-160">If a command is in preview, all of its arguments are as well.</span></span> <span data-ttu-id="eab41-161">コマンド グループにプレビュー状態のラベルが付いている場合、すべてのコマンドと引数もプレビュー状態と見なされます。</span><span class="sxs-lookup"><span data-stu-id="eab41-161">If a command group is labeled as being in preview, then all commands and arguments are considered to be in preview as well.</span></span>

<span data-ttu-id="eab41-162">この変更の結果、このリリースでは、一部のコマンド グループが "突然" プレビュー状態になったように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="eab41-162">As a result of this change, several command groups may seem to "suddenly" appear to be in a preview status with this release.</span></span> <span data-ttu-id="eab41-163">ほとんどのパッケージがプレビュー状態にあったのですが、このリリースでは一般提供と見なされていることがその真相です</span><span class="sxs-lookup"><span data-stu-id="eab41-163">What actually happened is that most packages were in a preview status, but are being deemed GA with this release</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-164">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-164">ACR</span></span>
* <span data-ttu-id="eab41-165">'acr check-health' コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-165">Added 'acr check-health' command</span></span>
* <span data-ttu-id="eab41-166">AAD トークンおよび外部コマンドの取得に関するエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-166">Improved error handling for AAD tokens and for retrieving external commands</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-167">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-167">ACS</span></span>
* <span data-ttu-id="eab41-168">非推奨の ACS コマンドがヘルプ ビューで非表示になりました</span><span class="sxs-lookup"><span data-stu-id="eab41-168">Deprecated ACS commands are now hidden from help view</span></span>

### <a name="ams"></a><span data-ttu-id="eab41-169">AMS</span><span class="sxs-lookup"><span data-stu-id="eab41-169">AMS</span></span>
* <span data-ttu-id="eab41-170">[重大な変更] archive-window-length および key-frame-interval-duration の ISO 8601 時間文字列を返すように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-170">[BREAKING CHANGE] Changed to return ISO 8601 time strings for archive-window-length and key-frame-interval-duration</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-171">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-171">AppService</span></span>
* <span data-ttu-id="eab41-172">`webapp deleted list` および `webapp deleted restore` に対してロケーション ベースのルーティングを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-172">Added location based routing for `webapp deleted list` and `webapp deleted restore`</span></span>
* <span data-ttu-id="eab41-173">Azure Cloud Shell で Web アプリのログに記録されたターゲット URL ("You can launch the app at...") がクリックできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-173">Fixed issue where webapp up logged target URL ("You can launch the app at...") was not clickable in Azure Cloud Shell</span></span>
* <span data-ttu-id="eab41-174">一部の SKU でのアプリ作成が AlwaysOn エラーで失敗するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-174">Fixed an issue where creating apps with the some SKUs was failing with an AlwaysOn error</span></span>
* <span data-ttu-id="eab41-175">`[appservice|webapp] create` に事前検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-175">Added pre-validation to `[appservice|webapp] create`</span></span>
* <span data-ttu-id="eab41-176">正しい actionHostName を使用するように `[webapp|functionapp] traffic-routing` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-176">Fixed `[webapp|functionapp] traffic-routing` to use the correct actionHostName</span></span>
* <span data-ttu-id="eab41-177">`functionapp` コマンドにスロット サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-177">Added slot support to `functionapp` commands</span></span>

### <a name="batch"></a><span data-ttu-id="eab41-178">Batch</span><span class="sxs-lookup"><span data-stu-id="eab41-178">Batch</span></span>
* <span data-ttu-id="eab41-179">共有キー認証の過度のエラー報告による AAD 認証の回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-179">Fixed AAD auth regression caused by over-aggressive error reporting for Shared Key Auth</span></span>

### <a name="batchai"></a><span data-ttu-id="eab41-180">BatchAI</span><span class="sxs-lookup"><span data-stu-id="eab41-180">BatchAI</span></span>
* <span data-ttu-id="eab41-181">BatchAI コマンドが非推奨となり、非表示になりました</span><span class="sxs-lookup"><span data-stu-id="eab41-181">BatchAI commands are now deprecated and hidden</span></span>

### <a name="botservice"></a><span data-ttu-id="eab41-182">BotService</span><span class="sxs-lookup"><span data-stu-id="eab41-182">BotService</span></span>
* <span data-ttu-id="eab41-183">v3 SDK をサポートするコマンドに "廃止されたサポート"/"保守モード" 警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-183">Added "discontinued support"/"maintenance mode" warning messages for commands that support the v3 SDK</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="eab41-184">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="eab41-184">CosmosDB</span></span>
* <span data-ttu-id="eab41-185">[非推奨] `cosmosdb list-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-185">[DEPRECATED] Deprecated the `cosmosdb list-keys` command</span></span>
* <span data-ttu-id="eab41-186">`cosmosdb keys list` コマンドを追加しました。`cosmosdb list-keys` に置き換わるものです</span><span class="sxs-lookup"><span data-stu-id="eab41-186">Added the `cosmosdb keys list` command - replaces `cosmosdb list-keys`</span></span>
* <span data-ttu-id="eab41-187">`cosmsodb create/update`:"isZoneRedundant" プロパティを設定できるように --location の新しいフォーマットを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-187">`cosmsodb create/update`: Added new format for --location to allow setting "isZoneRedundant" property.</span></span> <span data-ttu-id="eab41-188">古いフォーマットを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-188">Deprecated old format</span></span>

### <a name="eventgrid"></a><span data-ttu-id="eab41-189">EventGrid</span><span class="sxs-lookup"><span data-stu-id="eab41-189">EventGrid</span></span>
* <span data-ttu-id="eab41-190">ドメイン CRUD 操作のための `eventgrid domain` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-190">Added `eventgrid domain` commands for domain CRUD operations</span></span>
* <span data-ttu-id="eab41-191">ドメイン トピック CRUD 操作のための `eventgrid domain topic` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-191">Added `eventgrid domain topic` commands for domain topics CRUD operations</span></span>
* <span data-ttu-id="eab41-192">OData 構文を使用して結果をフィルタリングするための `--odata-query` 引数を `eventgrid [topic|event-subscription] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-192">Added `--odata-query` argument to `eventgrid [topic|event-subscription] list` for filtering results using OData syntax</span></span>
* <span data-ttu-id="eab41-193">`event-subscription create/update`:`--endpoint-type` パラメーターの新しい値として servicebusqueue を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-193">`event-subscription create/update`: Added servicebusqueue as new values for the `--endpoint-type` parameter</span></span>
* <span data-ttu-id="eab41-194">[重大な変更] `eventgrid event-subscription [create|update]` での `--included-event-types All` のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-194">[BREAKING CHANGE] Removed support for `--included-event-types All` with `eventgrid event-subscription [create|update]`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="eab41-195">HDInsight</span><span class="sxs-lookup"><span data-stu-id="eab41-195">HDInsight</span></span>
* <span data-ttu-id="eab41-196">`hdinsight create` コマンドでの `--ssh-public-key` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-196">Added support for `--ssh-public-key` parameter in `hdinsight create` command</span></span>

### <a name="iot"></a><span data-ttu-id="eab41-197">IoT</span><span class="sxs-lookup"><span data-stu-id="eab41-197">IoT</span></span>
* <span data-ttu-id="eab41-198">承認ポリシー キーの再生成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-198">Added support to regenerate authorization policy keys</span></span>
* <span data-ttu-id="eab41-199">DigitalTwin リポジトリ プロビジョニング サービスの SDK およびサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-199">Added SDK and support for DigitalTwin Repository Provisioning Service</span></span>

### <a name="network"></a><span data-ttu-id="eab41-200">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-200">Network</span></span>
* <span data-ttu-id="eab41-201">Nat Gateway に対するゾーン サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-201">Added Zone support for Nat Gateway</span></span>
* <span data-ttu-id="eab41-202">`network list-service-tags` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-202">Added command `network list-service-tags`</span></span>
* <span data-ttu-id="eab41-203">ユーザーがワイルドカード A レコードをインポートできない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-203">Fixed issue with `dns zone import` where users could not import wildcard A records</span></span>
* <span data-ttu-id="eab41-204">特定のリージョンでフロー ロギングを有効にできない `watcher flow-log configure` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-204">Fixed issue with `watcher flow-log configure` where flow logging could not be enabled in certain regions</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-205">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-205">Resource</span></span>
* <span data-ttu-id="eab41-206">REST 呼び出しを行うための `az rest` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-206">Added `az rest` command for making REST calls</span></span>
* <span data-ttu-id="eab41-207">リソース グループまたはサブスクリプション レベル`--scope` で `policy assignment list` を使用する場合のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-207">Fixed error when using `policy assignment list` with a resource group or subscription level `--scope`</span></span>

### <a name="servicebus"></a><span data-ttu-id="eab41-208">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eab41-208">ServiceBus</span></span>
* <span data-ttu-id="eab41-209">`servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319) での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-209">Fixed issue with `servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319)</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-210">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-210">SQL</span></span>
* <span data-ttu-id="eab41-211">`--location` を `sql [server|mi] create` のオプションに変更しました - 指定されていない場合、リソース グループの場所を使用します</span><span class="sxs-lookup"><span data-stu-id="eab41-211">Changed `--location` to be optional for `sql [server|mi] create` - uses resource group location if not specified</span></span>
* <span data-ttu-id="eab41-212">`sql db list-editions --available` の "'NoneType' object is not iterable" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-212">Fixed "'NoneType' object is not iterable" error for `sql db list-editions --available`</span></span>

### <a name="sqlvm"></a><span data-ttu-id="eab41-213">SQLVm</span><span class="sxs-lookup"><span data-stu-id="eab41-213">SQLVm</span></span>
* <span data-ttu-id="eab41-214">[破壊的変更] `--license-type` パラメーターを必要とするように `sql vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-214">[BREAKING CHNAGE] Changed `sql vm create` to require `--license-type` parameter</span></span>
* <span data-ttu-id="eab41-215">sql vm の作成または更新時に SQL イメージ SKU を設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-215">Changed to allow setting SQL image SKU when creating or updating a sql vm</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-216">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-216">Storage</span></span>
* <span data-ttu-id="eab41-217">`storage container generate-sas` のアカウント キーが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-217">Fixed issue with missing account key for `storage container generate-sas`</span></span>
* <span data-ttu-id="eab41-218">Linux での `storage blob sync` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-218">Fixed issue with `storage blob sync` on Linux</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-219">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-219">VM</span></span>
* <span data-ttu-id="eab41-220">[プレビュー] VM イメージを構築するための `vm image template` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-220">[PREVIEW] Added `vm image template` commands to build VM images</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="eab41-221">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="eab41-221">June 4, 2019</span></span>

<span data-ttu-id="eab41-222">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="eab41-222">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="eab41-223">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-223">Core</span></span>
* <span data-ttu-id="eab41-224">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-224">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-225">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-225">ACR</span></span>
* <span data-ttu-id="eab41-226">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-226">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-227">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-227">ACS</span></span>
* <span data-ttu-id="eab41-228">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-228">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="eab41-229">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="eab41-229">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="eab41-230">Batch</span><span class="sxs-lookup"><span data-stu-id="eab41-230">Batch</span></span>
* <span data-ttu-id="eab41-231">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-231">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="eab41-232">IoT</span><span class="sxs-lookup"><span data-stu-id="eab41-232">IoT</span></span>
* <span data-ttu-id="eab41-233">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-233">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="eab41-234">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-234">Network</span></span>
* <span data-ttu-id="eab41-235">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-235">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="eab41-236">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-236">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="eab41-237">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-237">Resource</span></span>
* <span data-ttu-id="eab41-238">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-238">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="eab41-239">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-239">Role</span></span>
* <span data-ttu-id="eab41-240">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-240">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="eab41-241">Compute</span><span class="sxs-lookup"><span data-stu-id="eab41-241">Compute</span></span>
* <span data-ttu-id="eab41-242">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-242">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="eab41-243">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="eab41-243">May 21, 2019</span></span>

<span data-ttu-id="eab41-244">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="eab41-244">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="eab41-245">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-245">Core</span></span>
* <span data-ttu-id="eab41-246">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-246">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="eab41-247">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-247">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="eab41-248">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-248">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-249">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-249">ACR</span></span>
* <span data-ttu-id="eab41-250">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-250">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-251">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-251">ACS</span></span>
* <span data-ttu-id="eab41-252">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-252">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-253">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-253">AppService</span></span>
* <span data-ttu-id="eab41-254">[非推奨] `functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="eab41-254">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="eab41-255">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-255">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="eab41-256">[重大な変更] `--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="eab41-256">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="eab41-257">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-257">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="eab41-258">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-258">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="eab41-259">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-259">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="eab41-260">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-260">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="eab41-261">BotService</span><span class="sxs-lookup"><span data-stu-id="eab41-261">BotService</span></span>
* <span data-ttu-id="eab41-262">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-262">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="eab41-263">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-263">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="eab41-264">消費</span><span class="sxs-lookup"><span data-stu-id="eab41-264">Consumption</span></span>
* <span data-ttu-id="eab41-265">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-265">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="eab41-266">IoT</span><span class="sxs-lookup"><span data-stu-id="eab41-266">IoT</span></span>
* <span data-ttu-id="eab41-267">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-267">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="eab41-268">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-268">Network</span></span>
* [重大な変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="eab41-270">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-270">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="eab41-271">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-271">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="eab41-272">RDBMS</span><span class="sxs-lookup"><span data-stu-id="eab41-272">RDBMS</span></span>
* <span data-ttu-id="eab41-273">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-273">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="eab41-274">RBAC</span><span class="sxs-lookup"><span data-stu-id="eab41-274">RBAC</span></span>
* <span data-ttu-id="eab41-275">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-275">Added support for mangement group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-276">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-276">Storage</span></span>
* <span data-ttu-id="eab41-277">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="eab41-277">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="eab41-278">Compute</span><span class="sxs-lookup"><span data-stu-id="eab41-278">Compute</span></span>
* <span data-ttu-id="eab41-279">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-279">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="eab41-280">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-280">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="eab41-281">__メモ__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="eab41-281">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="eab41-282">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-282">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="eab41-283">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="eab41-283">May 6, 2019</span></span>

<span data-ttu-id="eab41-284">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="eab41-284">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-285">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-285">ACS</span></span>
* <span data-ttu-id="eab41-286">[重大な変更] `--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-286">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="eab41-287">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-287">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="eab41-288">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-288">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="eab41-289">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-289">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-290">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-290">Appservice</span></span>
* <span data-ttu-id="eab41-291">[非推奨] `functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-291">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="eab41-292">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-292">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="eab41-293">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="eab41-293">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="eab41-294">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-294">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="eab41-295">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-295">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="eab41-296">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-296">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="eab41-297">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-297">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="eab41-298">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-298">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="eab41-299">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-299">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="eab41-300">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-300">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="eab41-301">Batch</span><span class="sxs-lookup"><span data-stu-id="eab41-301">Batch</span></span>
* <span data-ttu-id="eab41-302">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-302">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="eab41-303">Botservice</span><span class="sxs-lookup"><span data-stu-id="eab41-303">Botservice</span></span>
* <span data-ttu-id="eab41-304">[重大な変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="eab41-304">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="eab41-305">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-305">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="eab41-306">[重大な変更] `--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-306">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="eab41-307">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="eab41-307">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="eab41-308">[重大な変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-308">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="eab41-309">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="eab41-309">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="eab41-310">[重大な変更] `bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-310">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="eab41-311">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-311">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="eab41-312">[重大な変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-312">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="eab41-313">[重大な変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-313">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="eab41-314">[重大な変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-314">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="eab41-315">[重大な変更] `Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-315">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="eab41-316">[重大な変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-316">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="eab41-317">[重大な変更] `SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-317">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="eab41-318">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="eab41-318">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="eab41-319">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-319">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="eab41-320">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-320">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="eab41-321">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-321">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="eab41-322">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-322">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="eab41-323">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-323">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="eab41-324">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-324">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="eab41-325">構成</span><span class="sxs-lookup"><span data-stu-id="eab41-325">Configure</span></span>
* <span data-ttu-id="eab41-326">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-326">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="eab41-327">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="eab41-327">Eventhubs</span></span>
* <span data-ttu-id="eab41-328">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-328">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="eab41-329">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-329">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="eab41-330">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-330">Network</span></span>
* <span data-ttu-id="eab41-331">[重大な変更] `vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="eab41-331">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="eab41-332">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="eab41-332">Policy Insights</span></span>
* <span data-ttu-id="eab41-333">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-333">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="eab41-334">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-334">Role</span></span>
* <span data-ttu-id="eab41-335">[非推奨] `create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="eab41-335">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="eab41-336">Service Bus</span><span class="sxs-lookup"><span data-stu-id="eab41-336">Service Bus</span></span>
* <span data-ttu-id="eab41-337">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-337">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="eab41-338">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-338">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="eab41-339">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-339">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-340">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-340">SQL</span></span>
* <span data-ttu-id="eab41-341">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-341">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-342">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-342">VM</span></span>
* <span data-ttu-id="eab41-343">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-343">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="eab41-344">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-344">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="eab41-345">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-345">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="eab41-346">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-346">Added new `ppg` command group for manging Proximity Placement Groups</span></span>
* <span data-ttu-id="eab41-347">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-347">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="eab41-348">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-348">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="eab41-349">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="eab41-349">April 23, 2019</span></span>

<span data-ttu-id="eab41-350">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="eab41-350">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-351">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-351">ACS</span></span>
* <span data-ttu-id="eab41-352">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-352">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="eab41-353">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-353">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="eab41-354">AMS</span><span class="sxs-lookup"><span data-stu-id="eab41-354">AMS</span></span>
* <span data-ttu-id="eab41-355">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-355">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-356">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-356">AppService</span></span>
* <span data-ttu-id="eab41-357">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-357">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="eab41-358">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-358">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="eab41-359">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-359">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="eab41-360">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-360">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="eab41-361">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-361">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="eab41-362">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-362">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="eab41-363">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-363">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="eab41-364">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-364">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="eab41-365">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-365">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="eab41-366">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="eab41-366">Deployment Manager</span></span>
* <span data-ttu-id="eab41-367">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="eab41-367">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="eab41-368">ラボ</span><span class="sxs-lookup"><span data-stu-id="eab41-368">Lab</span></span>
* <span data-ttu-id="eab41-369">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-369">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="eab41-370">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-370">Network</span></span>
* <span data-ttu-id="eab41-371">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-371">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-372">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-372">Resource</span></span>
* <span data-ttu-id="eab41-373">[非推奨] `resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="eab41-373">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="eab41-374">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="eab41-374">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="eab41-375">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-375">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="eab41-376">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-376">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-377">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-377">SQL</span></span>
* <span data-ttu-id="eab41-378">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-378">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="eab41-379">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-379">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="eab41-380">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-380">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="eab41-381">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-381">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-382">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-382">Storage</span></span>
* <span data-ttu-id="eab41-383">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-383">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-384">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-384">VM</span></span>
* <span data-ttu-id="eab41-385">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-385">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="eab41-386">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-386">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="eab41-387">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-387">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="eab41-388">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="eab41-388">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="eab41-389">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-389">Core</span></span>
* <span data-ttu-id="eab41-390">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-390">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-391">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-391">ACR</span></span>
* <span data-ttu-id="eab41-392">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-392">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="eab41-393">AMS</span><span class="sxs-lookup"><span data-stu-id="eab41-393">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="eab41-396">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-396">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="eab41-397">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-397">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-398">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-398">AppService</span></span>
* <span data-ttu-id="eab41-399">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-399">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="eab41-400">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-400">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="eab41-401">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-401">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="eab41-402">[重大な変更] `devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="eab41-402">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="eab41-403">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-403">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="eab41-404">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-404">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="eab41-405">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-405">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="eab41-406">CDN</span><span class="sxs-lookup"><span data-stu-id="eab41-406">CDN</span></span>
* <span data-ttu-id="eab41-407">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-407">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="eab41-408">フィードバック</span><span class="sxs-lookup"><span data-stu-id="eab41-408">Feedback</span></span>
* <span data-ttu-id="eab41-409">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-409">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="eab41-410">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-410">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="eab41-411">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-411">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-412">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-412">Monitor</span></span>
* <span data-ttu-id="eab41-413">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-413">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="eab41-414">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-414">Network</span></span>
* <span data-ttu-id="eab41-415">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-415">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="eab41-416">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-416">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="eab41-417">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-417">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="eab41-418">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-418">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="eab41-419">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="eab41-419">PrivateDNS</span></span>
* <span data-ttu-id="eab41-420">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-420">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-421">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-421">Resource</span></span>
* <span data-ttu-id="eab41-422">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-422">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="eab41-423">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-423">Role</span></span>
* <span data-ttu-id="eab41-424">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-424">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="eab41-425">[重大な変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-425">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-426">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-426">SQL</span></span>
* <span data-ttu-id="eab41-427">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-427">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-428">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-428">Storage</span></span>
* <span data-ttu-id="eab41-429">[重大な変更] `storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-429">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="eab41-430">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-430">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="eab41-431">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-431">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="eab41-432">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-432">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="eab41-433">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="eab41-433">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="eab41-434">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-434">Core</span></span>
* <span data-ttu-id="eab41-435">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-435">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="eab41-436">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-436">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="eab41-437">クラウド</span><span class="sxs-lookup"><span data-stu-id="eab41-437">Cloud</span></span>
* <span data-ttu-id="eab41-438">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-438">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-439">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-439">ACR</span></span>
* <span data-ttu-id="eab41-440">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-440">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="eab41-441">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-441">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="eab41-442">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-442">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="eab41-443">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-443">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-444">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-444">AppService</span></span>
* <span data-ttu-id="eab41-445">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-445">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="eab41-446">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-446">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="eab41-447">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="eab41-447">BOT Service</span></span>
* <span data-ttu-id="eab41-448">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-448">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="eab41-449">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-449">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="eab41-450">[重大な変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-450">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="eab41-451">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-451">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="eab41-452">CDN</span><span class="sxs-lookup"><span data-stu-id="eab41-452">CDN</span></span>
* <span data-ttu-id="eab41-453">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-453">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [重大な変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="eab41-455">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="eab41-455">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="eab41-456">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-456">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="eab41-457">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="eab41-457">Cosmosdb</span></span>
* <span data-ttu-id="eab41-458">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-458">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="eab41-459">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-459">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="eab41-460">Interactive</span><span class="sxs-lookup"><span data-stu-id="eab41-460">Interactive</span></span>
* <span data-ttu-id="eab41-461">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-461">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-462">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-462">Monitor</span></span>
* <span data-ttu-id="eab41-463">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-463">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="eab41-464">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-464">Network</span></span>
* <span data-ttu-id="eab41-465">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-465">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="eab41-466">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-466">Profile</span></span>
* <span data-ttu-id="eab41-467">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-467">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="eab41-468">Postgres</span><span class="sxs-lookup"><span data-stu-id="eab41-468">Postgres</span></span> 
* <span data-ttu-id="eab41-469">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-469">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="eab41-470">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="eab41-470">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-471">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-471">Resource</span></span>
* <span data-ttu-id="eab41-472">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-472">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="eab41-473">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-473">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="eab41-474">Graph</span><span class="sxs-lookup"><span data-stu-id="eab41-474">Graph</span></span>
* <span data-ttu-id="eab41-475">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-475">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="eab41-476">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-476">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="eab41-477">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-477">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="eab41-478">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-478">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="eab41-479">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-479">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-480">storage</span><span class="sxs-lookup"><span data-stu-id="eab41-480">storage</span></span>
* <span data-ttu-id="eab41-481">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-481">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="eab41-482">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-482">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="eab41-483">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-483">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="eab41-484">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-484">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-485">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-485">VM</span></span>
* <span data-ttu-id="eab41-486">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-486">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="eab41-487">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="eab41-487">March 12, 2019</span></span>

<span data-ttu-id="eab41-488">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="eab41-488">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="eab41-489">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-489">Core</span></span>

* <span data-ttu-id="eab41-490">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-490">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-491">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-491">ACR</span></span>

* <span data-ttu-id="eab41-492">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-492">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-493">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-493">ACS</span></span>

* <span data-ttu-id="eab41-494">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-494">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="eab41-495">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-495">AppService</span></span>

* <span data-ttu-id="eab41-496">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-496">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="eab41-497">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-497">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="eab41-498">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-498">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="eab41-499">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-499">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="eab41-500">Botservice</span><span class="sxs-lookup"><span data-stu-id="eab41-500">Botservice</span></span>

* <span data-ttu-id="eab41-501">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-501">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="eab41-502">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-502">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="eab41-503">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-503">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="eab41-504">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-504">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="eab41-505">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-505">Container</span></span>

* <span data-ttu-id="eab41-506">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-506">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="eab41-507">EventHub</span><span class="sxs-lookup"><span data-stu-id="eab41-507">EventHub</span></span>

* <span data-ttu-id="eab41-508">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-508">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="eab41-509">Find</span><span class="sxs-lookup"><span data-stu-id="eab41-509">Find</span></span>

* <span data-ttu-id="eab41-510">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="eab41-510">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="eab41-511">HDInsight</span><span class="sxs-lookup"><span data-stu-id="eab41-511">HDInsight</span></span>

* <span data-ttu-id="eab41-512">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-512">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="eab41-513">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-513">Network</span></span>

* <span data-ttu-id="eab41-514">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-514">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="eab41-515">Rdbms</span><span class="sxs-lookup"><span data-stu-id="eab41-515">Rdbms</span></span>

* <span data-ttu-id="eab41-516">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="eab41-516">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="eab41-517">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-517">Role</span></span>

* <span data-ttu-id="eab41-518">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-518">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="eab41-519">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-519">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="eab41-520">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="eab41-520">Service Fabric</span></span>

* <span data-ttu-id="eab41-521">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-521">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="eab41-522">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="eab41-522">February 26, 2019</span></span>

<span data-ttu-id="eab41-523">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="eab41-523">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="eab41-524">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-524">Core</span></span>

* <span data-ttu-id="eab41-525">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-525">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-526">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-526">ACR</span></span>

* <span data-ttu-id="eab41-527">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-527">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="eab41-528">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-528">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-529">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-529">ACS</span></span>

* <span data-ttu-id="eab41-530">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-530">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-531">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-531">AppService</span></span>

* <span data-ttu-id="eab41-532">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-532">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="eab41-533">Batch</span><span class="sxs-lookup"><span data-stu-id="eab41-533">Batch</span></span>
* <span data-ttu-id="eab41-534">[重大な変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-534">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="eab41-535">[重大な変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-535">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="eab41-536">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-536">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="eab41-537">[重大な変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-537">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="eab41-538">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-538">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="eab41-539">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="eab41-539">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="eab41-540">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="eab41-540">CosmosDB</span></span>

* <span data-ttu-id="eab41-541">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-541">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="eab41-542">Kusto</span><span class="sxs-lookup"><span data-stu-id="eab41-542">Kusto</span></span>

* <span data-ttu-id="eab41-543">[重大な変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-543">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="eab41-544">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-544">Network</span></span>

* <span data-ttu-id="eab41-545">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-545">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="eab41-546">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-546">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="eab41-547">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-547">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="eab41-548">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-548">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="eab41-549">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-549">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="eab41-550">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-550">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="eab41-551">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-551">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-552">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-552">Resource</span></span>

* <span data-ttu-id="eab41-553">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-553">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="eab41-554">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-554">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="eab41-555">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-555">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="eab41-556">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-556">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="eab41-557">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-557">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="eab41-558">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-558">Role</span></span>

* <span data-ttu-id="eab41-559">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-559">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-560">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-560">VM</span></span>

* <span data-ttu-id="eab41-561">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-561">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="eab41-562">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="eab41-562">February 12, 2019</span></span>

<span data-ttu-id="eab41-563">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="eab41-563">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="eab41-564">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-564">Core</span></span>

* <span data-ttu-id="eab41-565">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-565">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="eab41-566">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-566">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-567">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-567">ACR</span></span>
* <span data-ttu-id="eab41-568">[重大な変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-568">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="eab41-569">[重大な変更] `acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-569">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-570">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-570">ACS</span></span>
* <span data-ttu-id="eab41-571">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-571">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="eab41-572">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-572">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="eab41-573">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-573">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="eab41-574">AMS</span><span class="sxs-lookup"><span data-stu-id="eab41-574">AMS</span></span>
* <span data-ttu-id="eab41-575">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-575">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="eab41-576">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-576">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-577">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-577">Appservice</span></span>
* <span data-ttu-id="eab41-578">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-578">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="eab41-579">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-579">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="eab41-580">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-580">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="eab41-581">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-581">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="eab41-582">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-582">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="eab41-583">Botservice</span><span class="sxs-lookup"><span data-stu-id="eab41-583">Botservice</span></span>
* <span data-ttu-id="eab41-584">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-584">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="eab41-585">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-585">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="eab41-586">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-586">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="eab41-587">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-587">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="eab41-588">[非推奨] `--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-588">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="eab41-589">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-589">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="eab41-590">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-590">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="eab41-591">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-591">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="eab41-592">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="eab41-592">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="eab41-593">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-593">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="eab41-594">Key Vault</span><span class="sxs-lookup"><span data-stu-id="eab41-594">Key Vault</span></span>
* <span data-ttu-id="eab41-595">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-595">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-596">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-596">Monitor</span></span>
* <span data-ttu-id="eab41-597">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-597">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="eab41-598">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-598">Network</span></span>
* <span data-ttu-id="eab41-599">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-599">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="eab41-600">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-600">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="eab41-601">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-601">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="eab41-602">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-602">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="eab41-603">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="eab41-603">Policy Insights</span></span>
* <span data-ttu-id="eab41-604">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-604">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="eab41-605">RDBMS</span><span class="sxs-lookup"><span data-stu-id="eab41-605">RDBMS</span></span>
* <span data-ttu-id="eab41-606">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-606">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="eab41-607">Redis</span><span class="sxs-lookup"><span data-stu-id="eab41-607">Redis</span></span>
* <span data-ttu-id="eab41-608">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-608">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="eab41-609">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-609">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="eab41-610">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-610">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="eab41-611">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-611">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="eab41-612">[重大な変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-612">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="eab41-613">[重大な変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="eab41-613">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="eab41-614">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-614">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="eab41-615">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-615">Role</span></span>
* <span data-ttu-id="eab41-616">[重大な変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="eab41-616">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="eab41-617">SQL VM</span><span class="sxs-lookup"><span data-stu-id="eab41-617">SQL VM</span></span>
* <span data-ttu-id="eab41-618">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-618">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-619">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-619">VM</span></span>
* <span data-ttu-id="eab41-620">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-620">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="eab41-621">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-621">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="eab41-622">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-622">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="eab41-623">[重大な変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="eab41-623">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="eab41-624">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="eab41-624">January 31, 2019</span></span>

<span data-ttu-id="eab41-625">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="eab41-625">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="eab41-626">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-626">Core</span></span>

* <span data-ttu-id="eab41-627">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="eab41-627">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="eab41-628">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="eab41-628">January 28, 2019</span></span>

<span data-ttu-id="eab41-629">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="eab41-629">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-630">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-630">ACR</span></span>
* <span data-ttu-id="eab41-631">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-631">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-632">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-632">ACS</span></span>
* <span data-ttu-id="eab41-633">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-633">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="eab41-634">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-634">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="eab41-635">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-635">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="eab41-636">AMS</span><span class="sxs-lookup"><span data-stu-id="eab41-636">AMS</span></span>
* <span data-ttu-id="eab41-637">[重大な変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-637">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="eab41-638">[重大な変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-638">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-639">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-639">Appservice</span></span>
* <span data-ttu-id="eab41-640">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-640">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="eab41-641">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-641">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="eab41-642">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-642">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="eab41-643">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-643">Container</span></span>
* <span data-ttu-id="eab41-644">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-644">Added `container start` command</span></span>
* <span data-ttu-id="eab41-645">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-645">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="eab41-646">EventGrid</span><span class="sxs-lookup"><span data-stu-id="eab41-646">EventGrid</span></span>
* <span data-ttu-id="eab41-647">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-647">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="eab41-648">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-648">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="eab41-649">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-649">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="eab41-650">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-650">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="eab41-651">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="eab41-651">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="eab41-652">HDInsight</span><span class="sxs-lookup"><span data-stu-id="eab41-652">HDInsight</span></span>
* <span data-ttu-id="eab41-653">[重大な変更] `hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-653">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="eab41-654">[重大な変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-654">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="eab41-655">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-655">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="eab41-656">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-656">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="eab41-657">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-657">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="eab41-658">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-658">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="eab41-659">IoT</span><span class="sxs-lookup"><span data-stu-id="eab41-659">IoT</span></span>
* <span data-ttu-id="eab41-660">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-660">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="eab41-661">Kusto</span><span class="sxs-lookup"><span data-stu-id="eab41-661">Kusto</span></span>
* <span data-ttu-id="eab41-662">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="eab41-662">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-663">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-663">Monitor</span></span>
* <span data-ttu-id="eab41-664">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-664">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="eab41-665">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-665">Profile</span></span>
* <span data-ttu-id="eab41-666">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-666">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="eab41-667">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-667">Network</span></span>
* <span data-ttu-id="eab41-668">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-668">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="eab41-669">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-669">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-670">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-670">Resource</span></span>
* <span data-ttu-id="eab41-671">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-671">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="eab41-672">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-672">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="eab41-673">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="eab41-673">SQL Virtual Machine</span></span>
* <span data-ttu-id="eab41-674">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="eab41-674">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-675">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-675">Storage</span></span>
* <span data-ttu-id="eab41-676">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-676">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="eab41-677">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="eab41-677">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-678">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-678">VM</span></span>
* <span data-ttu-id="eab41-679">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-679">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="eab41-680">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-680">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="eab41-681">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="eab41-681">January 15, 2019</span></span>

<span data-ttu-id="eab41-682">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="eab41-682">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-683">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-683">ACR</span></span>
* <span data-ttu-id="eab41-684">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-684">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="eab41-685">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-685">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="eab41-686">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-686">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="eab41-687">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-687">ACS</span></span>
* <span data-ttu-id="eab41-688">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-688">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-689">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-689">Appservice</span></span>
* <span data-ttu-id="eab41-690">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-690">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="eab41-691">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-691">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="eab41-692">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-692">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="eab41-693">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-693">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="eab41-694">Botservice</span><span class="sxs-lookup"><span data-stu-id="eab41-694">Botservice</span></span>
* <span data-ttu-id="eab41-695">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-695">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="eab41-696">構成</span><span class="sxs-lookup"><span data-stu-id="eab41-696">Configure</span></span>
* <span data-ttu-id="eab41-697">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-697">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="eab41-698">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="eab41-698">CosmosDB</span></span>
* <span data-ttu-id="eab41-699">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-699">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="eab41-700">HDInsight</span><span class="sxs-lookup"><span data-stu-id="eab41-700">HDInsight</span></span>
* <span data-ttu-id="eab41-701">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-701">Added commands for managing applications</span></span>
* <span data-ttu-id="eab41-702">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-702">Added commands for managing script actions</span></span>
* <span data-ttu-id="eab41-703">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-703">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="eab41-704">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-704">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="eab41-705">[重大な変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-705">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="eab41-706">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-706">Network</span></span>
* <span data-ttu-id="eab41-707">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-707">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="eab41-708">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-708">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="eab41-709">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-709">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="eab41-710">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-710">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="eab41-711">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-711">Role</span></span>
* <span data-ttu-id="eab41-712">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="eab41-712">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="eab41-713">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="eab41-713">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="eab41-714">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="eab41-714">Security</span></span>
* <span data-ttu-id="eab41-715">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="eab41-715">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-716">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-716">Storage</span></span>
* <span data-ttu-id="eab41-717">[重大な変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-717">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="eab41-718">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="eab41-718">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="eab41-719">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-719">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="eab41-720">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-720">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="eab41-721">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-721">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-722">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-722">VM</span></span>
* <span data-ttu-id="eab41-723">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-723">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="eab41-724">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-724">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="eab41-725">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-725">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="eab41-726">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-726">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="eab41-727">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-727">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="eab41-728">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-728">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="eab41-729">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="eab41-729">December 20, 2018</span></span>

<span data-ttu-id="eab41-730">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="eab41-730">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="eab41-731">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-731">Appservice</span></span>
* <span data-ttu-id="eab41-732">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-732">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="eab41-733">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-733">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="eab41-734">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-734">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="eab41-735">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="eab41-735">IoTCentral</span></span>
* <span data-ttu-id="eab41-736">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-736">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="eab41-737">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-737">Role</span></span>
* <span data-ttu-id="eab41-738">[重大な変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-738">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-739">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-739">SQL</span></span>
* <span data-ttu-id="eab41-740">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-740">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-741">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-741">VM</span></span>
* <span data-ttu-id="eab41-742">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-742">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="eab41-743">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="eab41-743">December 18, 2018</span></span>

<span data-ttu-id="eab41-744">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="eab41-744">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="eab41-745">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-745">ACR</span></span>
* <span data-ttu-id="eab41-746">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-746">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="eab41-747">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="eab41-747">Condensed the table layout for task list</span></span>
* <span data-ttu-id="eab41-748">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-748">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-749">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-749">ACS</span></span>
* <span data-ttu-id="eab41-750">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-750">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="eab41-751">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-751">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="eab41-752">[非推奨] `az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="eab41-752">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="eab41-753">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="eab41-753">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="eab41-754">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-754">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="eab41-755">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-755">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-756">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-756">Appservice</span></span>
* <span data-ttu-id="eab41-757">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-757">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="eab41-758">Botservice</span><span class="sxs-lookup"><span data-stu-id="eab41-758">Botservice</span></span>
* <span data-ttu-id="eab41-759">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-759">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="eab41-760">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-760">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="eab41-761">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-761">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="eab41-762">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="eab41-762">Reduced Kudu network calls</span></span>
* <span data-ttu-id="eab41-763">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-763">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="eab41-764">消費</span><span class="sxs-lookup"><span data-stu-id="eab41-764">Consumption</span></span>
* <span data-ttu-id="eab41-765">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-765">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="eab41-766">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="eab41-766">CosmosDB</span></span>
* <span data-ttu-id="eab41-767">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-767">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="eab41-768">マップ</span><span class="sxs-lookup"><span data-stu-id="eab41-768">Maps</span></span>
* <span data-ttu-id="eab41-769">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-769">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="eab41-770">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-770">Network</span></span>
* <span data-ttu-id="eab41-771">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-771">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="eab41-772">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-772">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-773">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-773">Resource</span></span>
* <span data-ttu-id="eab41-774">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-774">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="eab41-775">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-775">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-776">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-776">Storage</span></span>
*  <span data-ttu-id="eab41-777">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-777">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-778">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-778">VM</span></span>
* <span data-ttu-id="eab41-779">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-779">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="eab41-780">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="eab41-780">December 4, 2018</span></span>

<span data-ttu-id="eab41-781">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="eab41-781">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="eab41-782">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-782">Core</span></span>
* <span data-ttu-id="eab41-783">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-783">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="eab41-784">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-784">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-785">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-785">Appservice</span></span>
* <span data-ttu-id="eab41-786">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-786">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="eab41-787">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-787">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="eab41-788">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-788">Network</span></span>
* <span data-ttu-id="eab41-789">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-789">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="eab41-790">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-790">Role</span></span>
* <span data-ttu-id="eab41-791">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-791">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="eab41-792">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-792">VM</span></span>
* <span data-ttu-id="eab41-793">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-793">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="eab41-794">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-794">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="eab41-795">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-795">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="eab41-796">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-796">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="eab41-797">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="eab41-797">November 20, 2018</span></span>

<span data-ttu-id="eab41-798">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="eab41-798">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="eab41-799">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-799">Core</span></span>
* <span data-ttu-id="eab41-800">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-800">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-801">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-801">ACR</span></span>
* <span data-ttu-id="eab41-802">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-802">Added context token to task step</span></span>
* <span data-ttu-id="eab41-803">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-803">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="eab41-804">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-804">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-805">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-805">Appservice</span></span>
* <span data-ttu-id="eab41-806">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-806">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="eab41-807">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-807">Updated the default `node_version`.</span></span> <span data-ttu-id="eab41-808">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="eab41-808">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="eab41-809">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-809">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="eab41-810">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-810">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="eab41-811">IotCentral</span><span class="sxs-lookup"><span data-stu-id="eab41-811">IotCentral</span></span>
* <span data-ttu-id="eab41-812">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-812">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="eab41-813">KeyVault</span><span class="sxs-lookup"><span data-stu-id="eab41-813">KeyVault</span></span>
* <span data-ttu-id="eab41-814">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-814">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="eab41-815">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-815">Network</span></span>
* <span data-ttu-id="eab41-816">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-816">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="eab41-817">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-817">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="eab41-818">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-818">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="eab41-819">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-819">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="eab41-820">Rdbms</span><span class="sxs-lookup"><span data-stu-id="eab41-820">Rdbms</span></span>
* <span data-ttu-id="eab41-821">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-821">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="eab41-822">Rbac</span><span class="sxs-lookup"><span data-stu-id="eab41-822">Rbac</span></span>
* <span data-ttu-id="eab41-823">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-823">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="eab41-824">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-824">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="eab41-825">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-825">Storage</span></span>
* <span data-ttu-id="eab41-826">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-826">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="eab41-827">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-827">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="eab41-828">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-828">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="eab41-829">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="eab41-829">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-830">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-830">VM</span></span>
* <span data-ttu-id="eab41-831">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-831">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="eab41-832">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-832">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="eab41-833">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="eab41-833">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="eab41-834">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-834">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="eab41-835">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-835">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="eab41-836">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-836">Added `snapshot wait` command</span></span>
* <span data-ttu-id="eab41-837">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-837">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="eab41-838">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="eab41-838">November 6, 2018</span></span>

<span data-ttu-id="eab41-839">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="eab41-839">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="eab41-840">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-840">Core</span></span>
* <span data-ttu-id="eab41-841">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-841">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-842">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-842">ACR</span></span>
* <span data-ttu-id="eab41-843">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-843">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="eab41-844">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-844">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-845">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-845">ACS</span></span>
* <span data-ttu-id="eab41-846">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-846">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="eab41-847">Advisor</span><span class="sxs-lookup"><span data-stu-id="eab41-847">Advisor</span></span>
* <span data-ttu-id="eab41-848">GA リリース</span><span class="sxs-lookup"><span data-stu-id="eab41-848">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="eab41-849">AMS</span><span class="sxs-lookup"><span data-stu-id="eab41-849">AMS</span></span>
* <span data-ttu-id="eab41-850">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-850">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="eab41-851">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-851">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="eab41-852">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-852">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="eab41-853">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-853">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="eab41-854">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-854">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="eab41-855">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-855">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="eab41-856">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-856">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="eab41-857">[重大な変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="eab41-857">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="eab41-858">[重大な変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-858">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="eab41-859">[重大な変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-859">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="eab41-860">[重大な変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="eab41-860">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="eab41-861">[重大な変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="eab41-861">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="eab41-862">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="eab41-862">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="eab41-863">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="eab41-863">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="eab41-864">[重大な変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-864">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="eab41-865">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="eab41-865">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="eab41-866">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="eab41-866">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-867">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-867">AppService</span></span>
* <span data-ttu-id="eab41-868">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-868">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="eab41-869">構成</span><span class="sxs-lookup"><span data-stu-id="eab41-869">Configure</span></span>
* <span data-ttu-id="eab41-870">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-870">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="eab41-871">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-871">Container</span></span>
* <span data-ttu-id="eab41-872">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-872">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="eab41-873">EventHub</span><span class="sxs-lookup"><span data-stu-id="eab41-873">EventHub</span></span>
* <span data-ttu-id="eab41-874">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-874">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="eab41-875">Interactive</span><span class="sxs-lookup"><span data-stu-id="eab41-875">Interactive</span></span>
* <span data-ttu-id="eab41-876">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="eab41-876">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-877">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-877">Monitor</span></span>
* <span data-ttu-id="eab41-878">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-878">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="eab41-879">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-879">Network</span></span>
* <span data-ttu-id="eab41-880">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-880">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="eab41-881">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-881">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="eab41-882">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-882">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="eab41-883">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-883">Profile</span></span>
* <span data-ttu-id="eab41-884">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-884">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="eab41-885">RDBMS</span><span class="sxs-lookup"><span data-stu-id="eab41-885">RDBMS</span></span>
* <span data-ttu-id="eab41-886">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-886">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-887">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-887">Resource</span></span>
* <span data-ttu-id="eab41-888">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-888">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="eab41-889">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-889">Role</span></span>
* <span data-ttu-id="eab41-890">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-890">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="eab41-891">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-891">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="eab41-892">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-892">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-893">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-893">Storage</span></span>
* <span data-ttu-id="eab41-894">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="eab41-894">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-895">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-895">VM</span></span>
* <span data-ttu-id="eab41-896">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-896">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="eab41-897">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-897">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="eab41-898">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-898">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="eab41-899">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-899">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="eab41-900">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="eab41-900">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="eab41-901">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-901">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="eab41-902">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="eab41-902">October 23, 2018</span></span>

<span data-ttu-id="eab41-903">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="eab41-903">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="eab41-904">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-904">Core</span></span>
* <span data-ttu-id="eab41-905">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-905">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="eab41-906">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-906">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-907">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-907">ACR</span></span>
* <span data-ttu-id="eab41-908">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-908">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="eab41-909">CDN</span><span class="sxs-lookup"><span data-stu-id="eab41-909">CDN</span></span>
* <span data-ttu-id="eab41-910">[重大な変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="eab41-910">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="eab41-911">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-911">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="eab41-912">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-912">Container</span></span>
* <span data-ttu-id="eab41-913">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-913">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="eab41-914">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-914">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="eab41-915">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-915">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="eab41-916">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-916">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="eab41-917">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-917">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="eab41-918">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-918">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="eab41-919">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-919">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="eab41-920">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="eab41-920">CosmosDB</span></span>
* <span data-ttu-id="eab41-921">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-921">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="eab41-922">Interactive</span><span class="sxs-lookup"><span data-stu-id="eab41-922">Interactive</span></span>
* <span data-ttu-id="eab41-923">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-923">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="eab41-924">IoT Central</span><span class="sxs-lookup"><span data-stu-id="eab41-924">IoT Central</span></span>
* <span data-ttu-id="eab41-925">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-925">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="eab41-926">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="eab41-926">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-927">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-927">Monitor</span></span>
* <span data-ttu-id="eab41-928">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="eab41-928">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="eab41-929">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-929">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="eab41-930">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-930">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="eab41-931">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-931">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="eab41-932">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-932">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="eab41-933">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-933">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="eab41-934">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="eab41-934">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="eab41-935">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-935">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="eab41-936">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-936">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="eab41-937">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-937">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="eab41-938">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-938">Network</span></span>
* <span data-ttu-id="eab41-939">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-939">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="eab41-940">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-940">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="eab41-941">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eab41-941">ServiceBus</span></span>
* <span data-ttu-id="eab41-942">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-942">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-943">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-943">SQL</span></span>
* <span data-ttu-id="eab41-944">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-944">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-945">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-945">Storage</span></span>
* <span data-ttu-id="eab41-946">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-946">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="eab41-947">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-947">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-948">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-948">VM</span></span>
* <span data-ttu-id="eab41-949">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="eab41-949">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="eab41-950">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-950">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="eab41-951">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-951">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="eab41-952">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="eab41-952">October 16, 2018</span></span>

<span data-ttu-id="eab41-953">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="eab41-953">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-954">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-954">VM</span></span>
* <span data-ttu-id="eab41-955">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-955">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="eab41-956">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="eab41-956">October 9, 2018</span></span>

<span data-ttu-id="eab41-957">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="eab41-957">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="eab41-958">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-958">Core</span></span>
* <span data-ttu-id="eab41-959">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-959">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-960">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-960">ACR</span></span>
* <span data-ttu-id="eab41-961">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-961">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-962">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-962">ACS</span></span>
* <span data-ttu-id="eab41-963">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="eab41-963">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="eab41-964">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-964">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="eab41-965">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-965">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="eab41-966">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-966">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="eab41-967">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-967">Container</span></span>
* <span data-ttu-id="eab41-968">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-968">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="eab41-969">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-969">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="eab41-970">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="eab41-970">Event Hub</span></span>
* <span data-ttu-id="eab41-971">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-971">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="eab41-972">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-972">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="eab41-973">Extensions</span><span class="sxs-lookup"><span data-stu-id="eab41-973">Extensions</span></span>
* <span data-ttu-id="eab41-974">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-974">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="eab41-975">HDInsight</span><span class="sxs-lookup"><span data-stu-id="eab41-975">HDInsight</span></span>
* <span data-ttu-id="eab41-976">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="eab41-976">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="eab41-977">IoT</span><span class="sxs-lookup"><span data-stu-id="eab41-977">IoT</span></span>
* <span data-ttu-id="eab41-978">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-978">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="eab41-979">KeyVault</span><span class="sxs-lookup"><span data-stu-id="eab41-979">KeyVault</span></span>
* <span data-ttu-id="eab41-980">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-980">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="eab41-981">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-981">Network</span></span>
* <span data-ttu-id="eab41-982">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="eab41-982">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="eab41-983">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="eab41-983">See #6052</span></span>
* <span data-ttu-id="eab41-984">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-984">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="eab41-985">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="eab41-985">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="eab41-986">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-986">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="eab41-987">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-987">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="eab41-988">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-988">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="eab41-989">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-989">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="eab41-990">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-990">Role</span></span>
* <span data-ttu-id="eab41-991">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-991">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="eab41-992">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-992">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="eab41-993">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-993">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="eab41-994">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-994">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="eab41-995">Service Bus</span><span class="sxs-lookup"><span data-stu-id="eab41-995">Service Bus</span></span>
* <span data-ttu-id="eab41-996">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-996">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-997">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-997">VM</span></span>
* <span data-ttu-id="eab41-998">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-998">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="eab41-999">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-999">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="eab41-1000">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1000">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="eab41-1001">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1001">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="eab41-1002">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1002">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="eab41-1003">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1003">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="eab41-1004">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1004">September 21, 2018</span></span>

<span data-ttu-id="eab41-1005">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="eab41-1005">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-1006">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-1006">ACR</span></span>
* <span data-ttu-id="eab41-1007">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1007">Added ACR Task commands</span></span>
* <span data-ttu-id="eab41-1008">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1008">Added quick run command</span></span>
* <span data-ttu-id="eab41-1009">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1009">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="eab41-1010">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1010">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="eab41-1011">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1011">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="eab41-1012">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1012">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1013">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1013">ACS</span></span>
* <span data-ttu-id="eab41-1014">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1014">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="eab41-1015">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1015">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1016">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-1016">AppService</span></span>

* <span data-ttu-id="eab41-1017">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1017">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="eab41-1018">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1018">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="eab41-1019">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1019">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="eab41-1020">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1020">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="eab41-1021">Batch</span><span class="sxs-lookup"><span data-stu-id="eab41-1021">Batch</span></span>
* <span data-ttu-id="eab41-1022">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1022">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="eab41-1023">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1023">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="eab41-1024">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1024">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="eab41-1025">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1025">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="eab41-1026">Batch AI</span><span class="sxs-lookup"><span data-stu-id="eab41-1026">Batch AI</span></span> 
* <span data-ttu-id="eab41-1027">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1027">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="eab41-1028">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="eab41-1028">Cognitive Services</span></span>
* <span data-ttu-id="eab41-1029">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1029">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="eab41-1030">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1030">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="eab41-1031">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1031">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="eab41-1032">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1032">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="eab41-1033">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1033">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="eab41-1034">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1034">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="eab41-1035">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-1035">Container</span></span>
* <span data-ttu-id="eab41-1036">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1036">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="eab41-1037">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1037">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="eab41-1038">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1038">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="eab41-1039">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1039">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="eab41-1040">DataLake</span><span class="sxs-lookup"><span data-stu-id="eab41-1040">Datalake</span></span>
* <span data-ttu-id="eab41-1041">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1041">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="eab41-1042">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="eab41-1042">Interactive Shell</span></span>
* <span data-ttu-id="eab41-1043">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1043">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="eab41-1044">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1044">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="eab41-1045">IoT</span><span class="sxs-lookup"><span data-stu-id="eab41-1045">IoT</span></span>
* <span data-ttu-id="eab41-1046">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1046">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="eab41-1047">Key Vault</span><span class="sxs-lookup"><span data-stu-id="eab41-1047">Key Vault</span></span>
* <span data-ttu-id="eab41-1048">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1048">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1049">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1049">Network</span></span>
* <span data-ttu-id="eab41-1050">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1050">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="eab41-1051">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1051">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="eab41-1052">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1052">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="eab41-1053">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1053">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="eab41-1054">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1054">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="eab41-1055">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1055">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="eab41-1056">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1056">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="eab41-1057">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-1057">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="eab41-1058">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1058">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="eab41-1059">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1059">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="eab41-1060">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1060">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="eab41-1061">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1061">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="eab41-1062">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1062">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="eab41-1063">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="eab41-1063">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="eab41-1064">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1064">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="eab41-1065">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1065">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="eab41-1066">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1066">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="eab41-1067">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1067">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="eab41-1068">RDBMS</span><span class="sxs-lookup"><span data-stu-id="eab41-1068">RDBMS</span></span>
* <span data-ttu-id="eab41-1069">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1069">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="eab41-1070">予約</span><span class="sxs-lookup"><span data-stu-id="eab41-1070">Reservation</span></span>
* <span data-ttu-id="eab41-1071">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1071">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="eab41-1072">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1072">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="eab41-1073">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="eab41-1073">Manage App</span></span>
* <span data-ttu-id="eab41-1074">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1074">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="eab41-1075">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1075">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="eab41-1076">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-1076">Role</span></span>
* <span data-ttu-id="eab41-1077">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1077">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="eab41-1078">SignalR</span><span class="sxs-lookup"><span data-stu-id="eab41-1078">SignalR</span></span>
* <span data-ttu-id="eab41-1079">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="eab41-1079">First release</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1080">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1080">Storage</span></span>
* <span data-ttu-id="eab41-1081">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1081">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="eab41-1082">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1082">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1083">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1083">VM</span></span>
* <span data-ttu-id="eab41-1084">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="eab41-1084">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="eab41-1085">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1085">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="eab41-1086">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1086">August 28, 2018</span></span>

<span data-ttu-id="eab41-1087">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="eab41-1087">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="eab41-1088">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-1088">Core</span></span>

* <span data-ttu-id="eab41-1089">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1089">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="eab41-1090">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1090">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-1091">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-1091">ACR</span></span>

* <span data-ttu-id="eab41-1092">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1092">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="eab41-1093">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1093">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1094">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1094">ACS</span></span>

* <span data-ttu-id="eab41-1095">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1095">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="eab41-1096">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1096">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1097">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-1097">AppService</span></span>

* <span data-ttu-id="eab41-1098">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1098">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="eab41-1099">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1099">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="eab41-1100">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1100">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="eab41-1101">バックアップ</span><span class="sxs-lookup"><span data-stu-id="eab41-1101">Backup</span></span>

* <span data-ttu-id="eab41-1102">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1102">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="eab41-1103">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="eab41-1103">Bot Service</span></span>

* <span data-ttu-id="eab41-1104">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="eab41-1104">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="eab41-1105">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="eab41-1105">Cognitive Services</span></span>

* <span data-ttu-id="eab41-1106">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1106">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="eab41-1107">IoT</span><span class="sxs-lookup"><span data-stu-id="eab41-1107">IoT</span></span>

* <span data-ttu-id="eab41-1108">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1108">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-1109">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-1109">Monitor</span></span>

* <span data-ttu-id="eab41-1110">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1110">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="eab41-1111">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1111">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1112">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1112">Network</span></span>

* <span data-ttu-id="eab41-1113">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1113">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-1114">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-1114">Resource</span></span>

* <span data-ttu-id="eab41-1115">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1115">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1116">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1116">Storage</span></span>

* <span data-ttu-id="eab41-1117">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1117">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1118">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1118">VM</span></span>

* <span data-ttu-id="eab41-1119">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1119">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="eab41-1120">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1120">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="eab41-1121">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1121">Auguest 14, 2018</span></span>

<span data-ttu-id="eab41-1122">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="eab41-1122">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="eab41-1123">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-1123">Core</span></span>

* <span data-ttu-id="eab41-1124">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1124">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="eab41-1125">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1125">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="eab41-1126">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="eab41-1126">Telemetry</span></span>

* <span data-ttu-id="eab41-1127">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1127">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-1128">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-1128">ACR</span></span>

* <span data-ttu-id="eab41-1129">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1129">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="eab41-1130">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1130">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1131">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1131">ACS</span></span>

* <span data-ttu-id="eab41-1132">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1132">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="eab41-1133">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1133">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="eab41-1134">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1134">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="eab41-1135">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1135">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="eab41-1136">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1136">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="eab41-1137">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-1137">AppService</span></span>

* <span data-ttu-id="eab41-1138">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1138">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="eab41-1139">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1139">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="eab41-1140">BatchAI</span><span class="sxs-lookup"><span data-stu-id="eab41-1140">BatchAI</span></span>

* <span data-ttu-id="eab41-1141">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1141">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="eab41-1142">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-1142">Container</span></span>

* <span data-ttu-id="eab41-1143">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1143">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="eab41-1144">IoT</span><span class="sxs-lookup"><span data-stu-id="eab41-1144">IoT</span></span>

* <span data-ttu-id="eab41-1145">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1145">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="eab41-1146">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1146">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="eab41-1147">Iot Central</span><span class="sxs-lookup"><span data-stu-id="eab41-1147">Iot Central</span></span>

* <span data-ttu-id="eab41-1148">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="eab41-1148">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="eab41-1149">KeyVault</span><span class="sxs-lookup"><span data-stu-id="eab41-1149">KeyVault</span></span>


* <span data-ttu-id="eab41-1150">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1150">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="eab41-1151">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1151">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="eab41-1152">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1152">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="eab41-1153">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1153">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="eab41-1154">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1154">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="eab41-1155">リレー</span><span class="sxs-lookup"><span data-stu-id="eab41-1155">Relay</span></span>

* <span data-ttu-id="eab41-1156">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="eab41-1156">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-1157">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-1157">Sql</span></span>

* <span data-ttu-id="eab41-1158">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1158">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1159">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1159">Storage</span></span>

* <span data-ttu-id="eab41-1160">[重大な変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="eab41-1160">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="eab41-1161">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1161">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="eab41-1162">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1162">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="eab41-1163">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1163">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="eab41-1164">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1164">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1165">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1165">VM</span></span>

* <span data-ttu-id="eab41-1166">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1166">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="eab41-1167">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="eab41-1167">July 31, 2018</span></span>

<span data-ttu-id="eab41-1168">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="eab41-1168">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-1169">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-1169">ACR</span></span>

* <span data-ttu-id="eab41-1170">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1170">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="eab41-1171">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1171">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1172">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1172">ACS</span></span>

* <span data-ttu-id="eab41-1173">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1173">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="eab41-1174">Batch</span><span class="sxs-lookup"><span data-stu-id="eab41-1174">Batch</span></span>

* <span data-ttu-id="eab41-1175">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1175">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="eab41-1176">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-1176">Container</span></span>

* <span data-ttu-id="eab41-1177">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1177">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1178">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1178">Network</span></span>

* <span data-ttu-id="eab41-1179">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1179">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="eab41-1180">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-1180">Resource</span></span>

* <span data-ttu-id="eab41-1181">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1181">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="eab41-1182">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1182">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="eab41-1183">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-1183">Role</span></span>

* <span data-ttu-id="eab41-1184">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1184">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="eab41-1185">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1185">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="eab41-1186">Search</span><span class="sxs-lookup"><span data-stu-id="eab41-1186">Search</span></span>

* <span data-ttu-id="eab41-1187">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1187">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="eab41-1188">Service Bus</span><span class="sxs-lookup"><span data-stu-id="eab41-1188">Service Bus</span></span>

* <span data-ttu-id="eab41-1189">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1189">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="eab41-1190">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1190">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="eab41-1191">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="eab41-1191">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="eab41-1192">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="eab41-1192">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1193">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1193">Storage</span></span>

* <span data-ttu-id="eab41-1194">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-1194">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="eab41-1195">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1195">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1196">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1196">VM</span></span>

* <span data-ttu-id="eab41-1197">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-1197">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="eab41-1198">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1198">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="eab41-1199">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1199">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="eab41-1200">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1200">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="eab41-1201">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1201">July 18, 2018</span></span>

<span data-ttu-id="eab41-1202">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="eab41-1202">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="eab41-1203">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-1203">Core</span></span>

* <span data-ttu-id="eab41-1204">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1204">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="eab41-1205">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1205">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="eab41-1206">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1206">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-1207">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-1207">ACR</span></span>

* <span data-ttu-id="eab41-1208">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1208">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="eab41-1209">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1209">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="eab41-1210">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1210">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="eab41-1211">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1211">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1212">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1212">ACS</span></span>

* <span data-ttu-id="eab41-1213">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1213">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1214">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-1214">AppService</span></span>

* <span data-ttu-id="eab41-1215">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1215">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="eab41-1216">Batch</span><span class="sxs-lookup"><span data-stu-id="eab41-1216">Batch</span></span>

* <span data-ttu-id="eab41-1217">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1217">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="eab41-1218">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1218">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="eab41-1219">Batch AI</span><span class="sxs-lookup"><span data-stu-id="eab41-1219">Batch AI</span></span>

* <span data-ttu-id="eab41-1220">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1220">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="eab41-1221">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-1221">Container</span></span>

* <span data-ttu-id="eab41-1222">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1222">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="eab41-1223">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1223">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1224">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1224">Network</span></span>

* <span data-ttu-id="eab41-1225">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1225">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="eab41-1226">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1226">Added `network nic wait`</span></span>
* <span data-ttu-id="eab41-1227">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1227">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="eab41-1228">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1228">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="eab41-1229">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-1229">Resource</span></span>

* <span data-ttu-id="eab41-1230">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1230">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="eab41-1231">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1231">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="eab41-1232">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1232">Added `deployment wait` command</span></span>
* <span data-ttu-id="eab41-1233">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1233">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-1234">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-1234">SQL</span></span>

* <span data-ttu-id="eab41-1235">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1235">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="eab41-1236">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-1236">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="eab41-1237">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1237">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1238">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1238">Storage</span></span>

* <span data-ttu-id="eab41-1239">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1239">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1240">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1240">VM</span></span>

* <span data-ttu-id="eab41-1241">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1241">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="eab41-1242">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1242">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="eab41-1243">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1243">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="eab41-1244">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1244">July 3, 2018</span></span>

<span data-ttu-id="eab41-1245">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="eab41-1245">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="eab41-1246">AKS</span><span class="sxs-lookup"><span data-stu-id="eab41-1246">AKS</span></span>

* <span data-ttu-id="eab41-1247">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1247">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="eab41-1248">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1248">July 3, 2018</span></span>

<span data-ttu-id="eab41-1249">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="eab41-1249">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="eab41-1250">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-1250">Core</span></span>

* <span data-ttu-id="eab41-1251">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1251">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-1252">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-1252">ACR</span></span>

* <span data-ttu-id="eab41-1253">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1253">Added polling build status</span></span>
* <span data-ttu-id="eab41-1254">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1254">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="eab41-1255">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1255">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1256">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1256">ACS</span></span>

* <span data-ttu-id="eab41-1257">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1257">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="eab41-1258">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1258">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="eab41-1259">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1259">Updated options for `aks browse` command.</span></span> <span data-ttu-id="eab41-1260">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1260">Added `--listen-port` support</span></span>
* <span data-ttu-id="eab41-1261">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1261">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="eab41-1262">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="eab41-1262">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="eab41-1263">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1263">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1264">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-1264">AppService</span></span>

* <span data-ttu-id="eab41-1265">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-1265">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="eab41-1266">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1266">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="eab41-1267">バックアップ</span><span class="sxs-lookup"><span data-stu-id="eab41-1267">Backup</span></span>

* <span data-ttu-id="eab41-1268">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1268">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="eab41-1269">BatchAI</span><span class="sxs-lookup"><span data-stu-id="eab41-1269">BatchAI</span></span>

* <span data-ttu-id="eab41-1270">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1270">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="eab41-1271">クラウド</span><span class="sxs-lookup"><span data-stu-id="eab41-1271">Cloud</span></span>

* <span data-ttu-id="eab41-1272">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1272">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="eab41-1273">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-1273">Container</span></span>

* <span data-ttu-id="eab41-1274">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1274">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="eab41-1275">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1275">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="eab41-1276">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1276">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="eab41-1277">拡張機能</span><span class="sxs-lookup"><span data-stu-id="eab41-1277">Extension</span></span>

* <span data-ttu-id="eab41-1278">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1278">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1279">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1279">Network</span></span>

* <span data-ttu-id="eab41-1280">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1280">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="eab41-1281">Rdbms</span><span class="sxs-lookup"><span data-stu-id="eab41-1281">Rdbms</span></span>

* <span data-ttu-id="eab41-1282">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1282">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-1283">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-1283">Resource</span></span>

* <span data-ttu-id="eab41-1284">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1284">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1285">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1285">VM</span></span>

* <span data-ttu-id="eab41-1286">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-1286">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="eab41-1287">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1287">June 25, 2018</span></span>

<span data-ttu-id="eab41-1288">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="eab41-1288">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="eab41-1289">CLI</span><span class="sxs-lookup"><span data-stu-id="eab41-1289">CLI</span></span>

* <span data-ttu-id="eab41-1290">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1290">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="eab41-1291">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1291">June 19, 2018</span></span>

<span data-ttu-id="eab41-1292">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="eab41-1292">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="eab41-1293">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-1293">Core</span></span>

* <span data-ttu-id="eab41-1294">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1294">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-1295">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-1295">ACR</span></span>

* <span data-ttu-id="eab41-1296">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1296">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="eab41-1297">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1297">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1298">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1298">ACS</span></span>

* <span data-ttu-id="eab41-1299">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1299">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="eab41-1300">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1300">Added `--update` support</span></span>
* <span data-ttu-id="eab41-1301">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1301">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="eab41-1302">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1302">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="eab41-1303">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1303">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="eab41-1304">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1304">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="eab41-1305">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1305">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="eab41-1306">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1306">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1307">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-1307">AppService</span></span>

* <span data-ttu-id="eab41-1308">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1308">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="eab41-1309">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1309">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="eab41-1310">Batch</span><span class="sxs-lookup"><span data-stu-id="eab41-1310">Batch</span></span>

* <span data-ttu-id="eab41-1311">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1311">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="eab41-1312">Batch AI</span><span class="sxs-lookup"><span data-stu-id="eab41-1312">Batch AI</span></span>

* <span data-ttu-id="eab41-1313">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1313">Added support for workspaces.</span></span> <span data-ttu-id="eab41-1314">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="eab41-1314">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="eab41-1315">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1315">Added support for experiments.</span></span> <span data-ttu-id="eab41-1316">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="eab41-1316">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="eab41-1317">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1317">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="eab41-1318">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1318">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="eab41-1319">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="eab41-1319">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="eab41-1320">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1320">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="eab41-1321">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="eab41-1321">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="eab41-1322">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="eab41-1322">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="eab41-1323">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1323">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="eab41-1324">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="eab41-1324">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="eab41-1325">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1325">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="eab41-1326">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="eab41-1326">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="eab41-1327">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1327">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="eab41-1328">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="eab41-1328">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="eab41-1329">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1329">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="eab41-1330">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1330">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="eab41-1331">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1331">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="eab41-1332">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1332">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="eab41-1333">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1333">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="eab41-1334">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1334">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="eab41-1335">マップ</span><span class="sxs-lookup"><span data-stu-id="eab41-1335">Maps</span></span>

* <span data-ttu-id="eab41-1336">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1336">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1337">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1337">Network</span></span>

* <span data-ttu-id="eab41-1338">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="eab41-1338">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="eab41-1339">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1339">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="eab41-1340">#6502</span><span class="sxs-lookup"><span data-stu-id="eab41-1340">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="eab41-1341">Reservations</span><span class="sxs-lookup"><span data-stu-id="eab41-1341">Reservations</span></span>

* <span data-ttu-id="eab41-1342">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1342">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="eab41-1343">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1343">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="eab41-1344">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1344">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="eab41-1345">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1345">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="eab41-1346">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1346">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="eab41-1347">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1347">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="eab41-1348">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-1348">Role</span></span>

* <span data-ttu-id="eab41-1349">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1349">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-1350">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-1350">SQL</span></span>

* <span data-ttu-id="eab41-1351">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1351">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1352">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1352">Storage</span></span>

* <span data-ttu-id="eab41-1353">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1353">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1354">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1354">VM</span></span>

* <span data-ttu-id="eab41-1355">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1355">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="eab41-1356">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1356">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="eab41-1357">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1357">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="eab41-1358">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1358">June 13, 2018</span></span>

<span data-ttu-id="eab41-1359">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="eab41-1359">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="eab41-1360">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-1360">Core</span></span>

* <span data-ttu-id="eab41-1361">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1361">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="eab41-1362">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1362">June 13, 2018</span></span>

<span data-ttu-id="eab41-1363">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="eab41-1363">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="eab41-1364">AKS</span><span class="sxs-lookup"><span data-stu-id="eab41-1364">AKS</span></span>

* <span data-ttu-id="eab41-1365">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1365">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="eab41-1366">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1366">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="eab41-1367">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1367">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="eab41-1368">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1368">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="eab41-1369">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1369">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1370">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-1370">AppService</span></span>

* <span data-ttu-id="eab41-1371">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1371">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="eab41-1372">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1372">June 5, 2018</span></span>

<span data-ttu-id="eab41-1373">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="eab41-1373">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="eab41-1374">Interactive</span><span class="sxs-lookup"><span data-stu-id="eab41-1374">Interactive</span></span>

* <span data-ttu-id="eab41-1375">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1375">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="eab41-1376">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1376">June 5, 2018</span></span>

<span data-ttu-id="eab41-1377">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="eab41-1377">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="eab41-1378">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-1378">Core</span></span>

* <span data-ttu-id="eab41-1379">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1379">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="eab41-1380">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1380">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-1381">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-1381">ACR</span></span>

* <span data-ttu-id="eab41-1382">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1382">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="eab41-1383">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1383">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="eab41-1384">AKS</span><span class="sxs-lookup"><span data-stu-id="eab41-1384">AKS</span></span>

* <span data-ttu-id="eab41-1385">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1385">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="eab41-1386">Batch</span><span class="sxs-lookup"><span data-stu-id="eab41-1386">Batch</span></span>

* <span data-ttu-id="eab41-1387">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1387">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="eab41-1388">IoT</span><span class="sxs-lookup"><span data-stu-id="eab41-1388">IOT</span></span>

* <span data-ttu-id="eab41-1389">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1389">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1390">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1390">Network</span></span>

* <span data-ttu-id="eab41-1391">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1391">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="eab41-1392">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="eab41-1392">Policy Insights</span></span>

* <span data-ttu-id="eab41-1393">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="eab41-1393">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="eab41-1394">ARM</span><span class="sxs-lookup"><span data-stu-id="eab41-1394">ARM</span></span>

* <span data-ttu-id="eab41-1395">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1395">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-1396">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-1396">SQL</span></span>

* <span data-ttu-id="eab41-1397">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1397">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="eab41-1398">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1398">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="eab41-1399">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1399">Storage</span></span>

* <span data-ttu-id="eab41-1400">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1400">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1401">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1401">VM</span></span>

* <span data-ttu-id="eab41-1402">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1402">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="eab41-1403">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1403">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="eab41-1404">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1404">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="eab41-1405">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1405">May 22, 2018</span></span>

<span data-ttu-id="eab41-1406">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="eab41-1406">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="eab41-1407">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-1407">Core</span></span>

* <span data-ttu-id="eab41-1408">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1408">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1409">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1409">ACS</span></span>

* <span data-ttu-id="eab41-1410">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1410">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="eab41-1411">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1411">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1412">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-1412">AppService</span></span>

* <span data-ttu-id="eab41-1413">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1413">Improved generic update commands</span></span>
* <span data-ttu-id="eab41-1414">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1414">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="eab41-1415">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-1415">Container</span></span>

* <span data-ttu-id="eab41-1416">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1416">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="eab41-1417">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1417">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="eab41-1418">拡張機能</span><span class="sxs-lookup"><span data-stu-id="eab41-1418">Extension</span></span>

* <span data-ttu-id="eab41-1419">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1419">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="eab41-1420">Interactive</span><span class="sxs-lookup"><span data-stu-id="eab41-1420">Interactive</span></span>

* <span data-ttu-id="eab41-1421">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1421">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="eab41-1422">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1422">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="eab41-1423">KeyVault</span><span class="sxs-lookup"><span data-stu-id="eab41-1423">KeyVault</span></span>

* <span data-ttu-id="eab41-1424">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1424">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1425">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1425">Network</span></span>

* <span data-ttu-id="eab41-1426">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1426">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="eab41-1427">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1427">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-1428">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-1428">SQL</span></span>

* <span data-ttu-id="eab41-1429">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1429">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="eab41-1430">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1430">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="eab41-1431">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1431">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="eab41-1432">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1432">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="eab41-1433">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1433">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="eab41-1434">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="eab41-1434">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="eab41-1435">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="eab41-1435">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="eab41-1436">`edition`</span><span class="sxs-lookup"><span data-stu-id="eab41-1436">`edition`.</span></span> <span data-ttu-id="eab41-1437">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="eab41-1437">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="eab41-1438">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="eab41-1438">`elasticPoolName`.</span></span> <span data-ttu-id="eab41-1439">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="eab41-1439">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="eab41-1440">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1440">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="eab41-1441">`edition`</span><span class="sxs-lookup"><span data-stu-id="eab41-1441">`edition`.</span></span> <span data-ttu-id="eab41-1442">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="eab41-1442">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="eab41-1443">`dtu`</span><span class="sxs-lookup"><span data-stu-id="eab41-1443">`dtu`.</span></span> <span data-ttu-id="eab41-1444">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="eab41-1444">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="eab41-1445">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="eab41-1445">`databaseDtuMin`.</span></span> <span data-ttu-id="eab41-1446">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="eab41-1446">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="eab41-1447">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="eab41-1447">`databaseDtuMax`.</span></span> <span data-ttu-id="eab41-1448">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="eab41-1448">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="eab41-1449">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1449">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="eab41-1450">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1450">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1451">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1451">Storage</span></span>

* <span data-ttu-id="eab41-1452">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1452">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="eab41-1453">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1453">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1454">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1454">VM</span></span>

* <span data-ttu-id="eab41-1455">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1455">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="eab41-1456">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="eab41-1456">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="eab41-1457">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1457">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="eab41-1458">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1458">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="eab41-1459">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1459">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="eab41-1460">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1460">May 7, 2018</span></span>

<span data-ttu-id="eab41-1461">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="eab41-1461">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="eab41-1462">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-1462">Core</span></span>

* <span data-ttu-id="eab41-1463">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1463">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="eab41-1464">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1464">Added limited support for positional arguments</span></span>
* <span data-ttu-id="eab41-1465">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1465">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="eab41-1466">#5591</span><span class="sxs-lookup"><span data-stu-id="eab41-1466">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="eab41-1467">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1467">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="eab41-1468">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="eab41-1468">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="eab41-1469">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1469">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="eab41-1470">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1470">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="eab41-1471">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1471">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-1472">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-1472">ACR</span></span>

* <span data-ttu-id="eab41-1473">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1473">Added ACR Build commands</span></span>
* <span data-ttu-id="eab41-1474">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1474">Improved resource not found error messages</span></span>
* <span data-ttu-id="eab41-1475">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1475">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="eab41-1476">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1476">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="eab41-1477">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1477">Improved repository commands error messages</span></span>
* <span data-ttu-id="eab41-1478">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1478">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1479">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1479">ACS</span></span>

* <span data-ttu-id="eab41-1480">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1480">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="eab41-1481">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1481">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="eab41-1482">AMS</span><span class="sxs-lookup"><span data-stu-id="eab41-1482">AMS</span></span>

* <span data-ttu-id="eab41-1483">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="eab41-1483">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1484">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-1484">Appservice</span></span>

* <span data-ttu-id="eab41-1485">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1485">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="eab41-1486">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1486">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="eab41-1487">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1487">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="eab41-1488">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1488">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="eab41-1489">Batch AI</span><span class="sxs-lookup"><span data-stu-id="eab41-1489">Batch AI</span></span>

* <span data-ttu-id="eab41-1490">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1490">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="eab41-1491">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="eab41-1491">Cognitive Services</span></span>

* <span data-ttu-id="eab41-1492">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1492">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="eab41-1493">消費</span><span class="sxs-lookup"><span data-stu-id="eab41-1493">Consumption</span></span>

* <span data-ttu-id="eab41-1494">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1494">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="eab41-1495">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-1495">Container</span></span>

* <span data-ttu-id="eab41-1496">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1496">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="eab41-1497">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="eab41-1497">Cosmos DB</span></span>

* <span data-ttu-id="eab41-1498">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1498">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="eab41-1499">DMS</span><span class="sxs-lookup"><span data-stu-id="eab41-1499">DMS</span></span>

* <span data-ttu-id="eab41-1500">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1500">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="eab41-1501">拡張機能</span><span class="sxs-lookup"><span data-stu-id="eab41-1501">Extension</span></span>

* <span data-ttu-id="eab41-1502">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1502">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="eab41-1503">Interactive</span><span class="sxs-lookup"><span data-stu-id="eab41-1503">Interactive</span></span>

* <span data-ttu-id="eab41-1504">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-1504">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="eab41-1505">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1505">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="eab41-1506">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1506">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="eab41-1507">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1507">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="eab41-1508">ラボ</span><span class="sxs-lookup"><span data-stu-id="eab41-1508">Lab</span></span>

* <span data-ttu-id="eab41-1509">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1509">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1510">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1510">Network</span></span>

* <span data-ttu-id="eab41-1511">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1511">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="eab41-1512">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-1512">Profile</span></span>

* <span data-ttu-id="eab41-1513">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1513">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="eab41-1514">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1514">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="eab41-1515">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1515">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="eab41-1516">Redis</span><span class="sxs-lookup"><span data-stu-id="eab41-1516">Redis</span></span>

* <span data-ttu-id="eab41-1517">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1517">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="eab41-1518">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1518">Deprecated `redis list-all`.</span></span> <span data-ttu-id="eab41-1519">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="eab41-1519">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="eab41-1520">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1520">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="eab41-1521">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1521">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="eab41-1522">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-1522">Role</span></span>

* <span data-ttu-id="eab41-1523">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1523">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1524">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1524">Storage</span></span>

* <span data-ttu-id="eab41-1525">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="eab41-1525">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="eab41-1526">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1526">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="eab41-1527">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="eab41-1527">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="eab41-1528">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="eab41-1528">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="eab41-1529">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1529">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1530">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1530">VM</span></span>

* <span data-ttu-id="eab41-1531">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1531">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="eab41-1532">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1532">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="eab41-1533">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="eab41-1533">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="eab41-1534">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1534">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="eab41-1535">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1535">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="eab41-1536">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1536">Added write accelerator support</span></span>
* <span data-ttu-id="eab41-1537">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1537">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="eab41-1538">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1538">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="eab41-1539">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1539">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="eab41-1540">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1540">April 10, 2018</span></span>

<span data-ttu-id="eab41-1541">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="eab41-1541">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-1542">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-1542">ACR</span></span>

* <span data-ttu-id="eab41-1543">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1543">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1544">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1544">ACS</span></span>

* <span data-ttu-id="eab41-1545">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1545">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1546">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-1546">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="eab41-1548">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1548">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="eab41-1549">BatchAI</span><span class="sxs-lookup"><span data-stu-id="eab41-1549">BatchAI</span></span>

* <span data-ttu-id="eab41-1550">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1550">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="eab41-1551">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="eab41-1551">Job level mounting</span></span>
  - <span data-ttu-id="eab41-1552">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="eab41-1552">Environment variables with secret values</span></span>
  - <span data-ttu-id="eab41-1553">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="eab41-1553">Performance counters settings</span></span>
  - <span data-ttu-id="eab41-1554">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="eab41-1554">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="eab41-1555">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="eab41-1555">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="eab41-1556">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="eab41-1556">Usage and limits reporting</span></span>
  - <span data-ttu-id="eab41-1557">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="eab41-1557">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="eab41-1558">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="eab41-1558">Support for custom images</span></span>
  - <span data-ttu-id="eab41-1559">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1559">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="eab41-1560">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-1560">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="eab41-1561">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="eab41-1561">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="eab41-1562">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="eab41-1562">National clouds are supported</span></span>
* <span data-ttu-id="eab41-1563">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1563">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="eab41-1564">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1564">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="eab41-1565">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1565">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="eab41-1566">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1566">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="eab41-1567">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="eab41-1567">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="eab41-1568">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="eab41-1568">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="eab41-1569">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1569">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="eab41-1570">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1570">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="eab41-1571">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="eab41-1571">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="eab41-1572">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1572">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="eab41-1573">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1573">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="eab41-1574">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1574">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="eab41-1575">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1575">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="eab41-1576">課金</span><span class="sxs-lookup"><span data-stu-id="eab41-1576">Billing</span></span>

* <span data-ttu-id="eab41-1577">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1577">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="eab41-1578">消費</span><span class="sxs-lookup"><span data-stu-id="eab41-1578">Consumption</span></span>

* <span data-ttu-id="eab41-1579">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1579">Added `marketplace` commands</span></span>
* <span data-ttu-id="eab41-1580">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1580">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="eab41-1581">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1581">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="eab41-1582">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1582">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="eab41-1583">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1583">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="eab41-1584">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1584">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="eab41-1585">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-1585">Container</span></span>

* <span data-ttu-id="eab41-1586">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1586">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="eab41-1587">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1587">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="eab41-1588">拡張機能</span><span class="sxs-lookup"><span data-stu-id="eab41-1588">Extension</span></span>

* <span data-ttu-id="eab41-1589">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1589">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="eab41-1590">Interactive</span><span class="sxs-lookup"><span data-stu-id="eab41-1590">Interactive</span></span>

* <span data-ttu-id="eab41-1591">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1591">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="eab41-1592">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1592">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="eab41-1593">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1593">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1594">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1594">Network</span></span>

* <span data-ttu-id="eab41-1595">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1595">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="eab41-1596">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1596">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="eab41-1597">#4910</span><span class="sxs-lookup"><span data-stu-id="eab41-1597">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="eab41-1598">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1598">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="eab41-1599">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="eab41-1599">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="eab41-1600">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1600">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="eab41-1601">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1601">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="eab41-1602">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1602">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="eab41-1603">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-1603">Profile</span></span>

* <span data-ttu-id="eab41-1604">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1604">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="eab41-1605">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1605">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="eab41-1606">RDBMS</span><span class="sxs-lookup"><span data-stu-id="eab41-1606">RDBMS</span></span>

* <span data-ttu-id="eab41-1607">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1607">Added `georestore` command</span></span>
* <span data-ttu-id="eab41-1608">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1608">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-1609">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-1609">Resource</span></span>

* <span data-ttu-id="eab41-1610">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1610">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="eab41-1611">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1611">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-1612">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-1612">SQL</span></span>

* <span data-ttu-id="eab41-1613">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1613">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1614">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1614">Storage</span></span>

* <span data-ttu-id="eab41-1615">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1615">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1616">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1616">VM</span></span>

* <span data-ttu-id="eab41-1617">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1617">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="eab41-1618">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1618">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="eab41-1620">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1620">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="eab41-1621">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1621">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="eab41-1622">#5718</span><span class="sxs-lookup"><span data-stu-id="eab41-1622">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="eab41-1623">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1623">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="eab41-1624">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1624">March 27, 2018</span></span>

<span data-ttu-id="eab41-1625">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="eab41-1625">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="eab41-1626">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-1626">Core</span></span>

* <span data-ttu-id="eab41-1627">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="eab41-1627">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1628">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1628">ACS</span></span>

* <span data-ttu-id="eab41-1629">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1629">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1630">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-1630">Appservice</span></span>

* <span data-ttu-id="eab41-1631">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1631">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="eab41-1632">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1632">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="eab41-1633">バックアップ</span><span class="sxs-lookup"><span data-stu-id="eab41-1633">Backup</span></span>

* <span data-ttu-id="eab41-1634">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1634">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="eab41-1635">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="eab41-1635">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="eab41-1636">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1636">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="eab41-1637">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1637">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="eab41-1638">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-1638">Container</span></span>

* <span data-ttu-id="eab41-1639">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1639">Added `container exec` command.</span></span> <span data-ttu-id="eab41-1640">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="eab41-1640">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="eab41-1641">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="eab41-1641">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="eab41-1642">拡張機能</span><span class="sxs-lookup"><span data-stu-id="eab41-1642">Extension</span></span>

* <span data-ttu-id="eab41-1643">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1643">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="eab41-1644">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1644">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="eab41-1645">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1645">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="eab41-1646">Interactive</span><span class="sxs-lookup"><span data-stu-id="eab41-1646">Interactive</span></span>

* <span data-ttu-id="eab41-1647">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1647">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="eab41-1648">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1648">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="eab41-1649">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="eab41-1649">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="eab41-1650">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1650">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="eab41-1651">ラボ</span><span class="sxs-lookup"><span data-stu-id="eab41-1651">Lab</span></span>

* <span data-ttu-id="eab41-1652">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1652">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-1653">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-1653">Monitor</span></span>

* <span data-ttu-id="eab41-1654">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="eab41-1654">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="eab41-1655">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="eab41-1655">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="eab41-1656">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="eab41-1656">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1657">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1657">Network</span></span>

* <span data-ttu-id="eab41-1658">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1658">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="eab41-1659">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-1659">Profile</span></span>

* <span data-ttu-id="eab41-1660">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1660">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="eab41-1661">RDBMS</span><span class="sxs-lookup"><span data-stu-id="eab41-1661">RDBMS</span></span>

* <span data-ttu-id="eab41-1662">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1662">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-1663">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-1663">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="eab41-1665">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-1665">Role</span></span>

* <span data-ttu-id="eab41-1666">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1666">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="eab41-1667">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1667">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="eab41-1668">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1668">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="eab41-1669">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1669">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="eab41-1670">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1670">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1671">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1671">Storage</span></span>

* <span data-ttu-id="eab41-1672">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1672">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="eab41-1673">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="eab41-1673">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1674">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1674">VM</span></span>

* <span data-ttu-id="eab41-1675">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1675">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="eab41-1676">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1676">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="eab41-1677">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1677">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="eab41-1678">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1678">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="eab41-1679">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1679">March 13, 2018</span></span>

<span data-ttu-id="eab41-1680">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="eab41-1680">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-1681">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-1681">ACR</span></span>

* <span data-ttu-id="eab41-1682">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1682">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="eab41-1683">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1683">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="eab41-1684">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1684">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1685">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1685">ACS</span></span>

* <span data-ttu-id="eab41-1686">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1686">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="eab41-1687">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1687">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="eab41-1688">Advisor</span><span class="sxs-lookup"><span data-stu-id="eab41-1688">Advisor</span></span>

* <span data-ttu-id="eab41-1689">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1689">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="eab41-1690">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1690">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="eab41-1691">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1691">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="eab41-1692">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1692">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="eab41-1693">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1693">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1694">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-1694">Appservice</span></span>

* <span data-ttu-id="eab41-1695">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1695">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="eab41-1696">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1696">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="eab41-1697">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="eab41-1697">Eventhubs</span></span>

* <span data-ttu-id="eab41-1698">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="eab41-1698">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="eab41-1699">拡張機能</span><span class="sxs-lookup"><span data-stu-id="eab41-1699">Extension</span></span>

* <span data-ttu-id="eab41-1700">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1700">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="eab41-1701">Interactive</span><span class="sxs-lookup"><span data-stu-id="eab41-1701">Interactive</span></span>

* <span data-ttu-id="eab41-1702">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="eab41-1702">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="eab41-1703">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="eab41-1703">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="eab41-1704">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="eab41-1704">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="eab41-1705">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1705">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-1706">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-1706">Monitor</span></span>

* <span data-ttu-id="eab41-1707">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1707">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="eab41-1708">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1708">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="eab41-1709">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1709">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="eab41-1710">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1710">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1711">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1711">Network</span></span>

* <span data-ttu-id="eab41-1712">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1712">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="eab41-1713">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1713">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="eab41-1714">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1714">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="eab41-1715">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1715">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="eab41-1716">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-1716">Profile</span></span>

* <span data-ttu-id="eab41-1717">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1717">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="eab41-1718">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1718">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="eab41-1719">RDBMS</span><span class="sxs-lookup"><span data-stu-id="eab41-1719">RDBMS</span></span>

* <span data-ttu-id="eab41-1720">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1720">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="eab41-1721">Service Bus</span><span class="sxs-lookup"><span data-stu-id="eab41-1721">Service Bus</span></span>

* <span data-ttu-id="eab41-1722">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="eab41-1722">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1723">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1723">Storage</span></span>

* <span data-ttu-id="eab41-1724">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-1724">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="eab41-1725">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="eab41-1725">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1726">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1726">VM</span></span>

* <span data-ttu-id="eab41-1727">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1727">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="eab41-1728">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1728">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="eab41-1729">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1729">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="eab41-1730">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1730">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="eab41-1731">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1731">February 27, 2018</span></span>

<span data-ttu-id="eab41-1732">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="eab41-1732">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="eab41-1733">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-1733">Core</span></span>

* <span data-ttu-id="eab41-1734">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="eab41-1734">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="eab41-1735">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1735">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="eab41-1736">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1736">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1737">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1737">ACS</span></span>

* <span data-ttu-id="eab41-1738">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1738">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="eab41-1739">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="eab41-1739">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="eab41-1740">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1740">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="eab41-1741">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1741">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1742">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-1742">Appservice</span></span>

* <span data-ttu-id="eab41-1743">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="eab41-1743">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="eab41-1744">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="eab41-1744">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="eab41-1745">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="eab41-1745">Cognitive Services</span></span>

* <span data-ttu-id="eab41-1746">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1746">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="eab41-1747">消費</span><span class="sxs-lookup"><span data-stu-id="eab41-1747">Consumption</span></span>

* <span data-ttu-id="eab41-1748">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1748">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="eab41-1749">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1749">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="eab41-1750">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-1750">Container</span></span>

* <span data-ttu-id="eab41-1751">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1751">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1752">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1752">Network</span></span>

* <span data-ttu-id="eab41-1753">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="eab41-1753">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-1754">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-1754">Resource</span></span>

* <span data-ttu-id="eab41-1755">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1755">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="eab41-1756">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-1756">Role</span></span>

* <span data-ttu-id="eab41-1757">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1757">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-1758">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-1758">SQL</span></span>

* <span data-ttu-id="eab41-1759">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1759">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1760">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1760">Storage</span></span>

* <span data-ttu-id="eab41-1761">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1761">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1762">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1762">VM</span></span>

* <span data-ttu-id="eab41-1763">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1763">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="eab41-1764">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1764">February 13, 2018</span></span>

<span data-ttu-id="eab41-1765">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="eab41-1765">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="eab41-1766">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-1766">Core</span></span>

* <span data-ttu-id="eab41-1767">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1767">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1768">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1768">ACS</span></span>

* <span data-ttu-id="eab41-1769">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1769">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="eab41-1770">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1770">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="eab41-1771">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1771">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="eab41-1772">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1772">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="eab41-1773">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1773">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="eab41-1774">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1774">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="eab41-1775">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1775">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="eab41-1776">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="eab41-1776">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1777">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-1777">Appservice</span></span>

* <span data-ttu-id="eab41-1778">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1778">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="eab41-1779">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1779">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="eab41-1780">CDN</span><span class="sxs-lookup"><span data-stu-id="eab41-1780">CDN</span></span>

* <span data-ttu-id="eab41-1781">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1781">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="eab41-1782">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-1782">Container</span></span>

* <span data-ttu-id="eab41-1783">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1783">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="eab41-1784">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1784">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="eab41-1785">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="eab41-1785">CosmosDB</span></span>

* <span data-ttu-id="eab41-1786">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1786">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="eab41-1787">拡張機能</span><span class="sxs-lookup"><span data-stu-id="eab41-1787">Extension</span></span>

* <span data-ttu-id="eab41-1788">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1788">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="eab41-1789">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1789">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="eab41-1790">フィードバック</span><span class="sxs-lookup"><span data-stu-id="eab41-1790">Feedback</span></span>

* <span data-ttu-id="eab41-1791">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1791">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="eab41-1792">Interactive</span><span class="sxs-lookup"><span data-stu-id="eab41-1792">Interactive</span></span>

* <span data-ttu-id="eab41-1793">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1793">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="eab41-1794">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1794">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="eab41-1795">IoT</span><span class="sxs-lookup"><span data-stu-id="eab41-1795">IoT</span></span>

* <span data-ttu-id="eab41-1796">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1796">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="eab41-1797">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1797">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="eab41-1798">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1798">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="eab41-1799">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1799">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-1800">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-1800">Monitor</span></span>

* <span data-ttu-id="eab41-1801">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1801">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1802">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1802">Network</span></span>

* <span data-ttu-id="eab41-1803">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1803">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="eab41-1804">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-1804">Profile</span></span>

* <span data-ttu-id="eab41-1805">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1805">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-1806">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-1806">Resource</span></span>

* <span data-ttu-id="eab41-1807">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1807">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="eab41-1808">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-1808">Role</span></span>

* <span data-ttu-id="eab41-1809">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1809">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-1810">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-1810">SQL</span></span>

* <span data-ttu-id="eab41-1811">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1811">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="eab41-1812">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1812">Added `sql db rename`</span></span>
* <span data-ttu-id="eab41-1813">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1813">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1814">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1814">Storage</span></span>

* <span data-ttu-id="eab41-1815">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1815">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1816">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1816">VM</span></span>

* <span data-ttu-id="eab41-1817">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1817">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="eab41-1818">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1818">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="eab41-1819">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="eab41-1819">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="eab41-1820">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1820">January 31, 2018</span></span>

<span data-ttu-id="eab41-1821">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="eab41-1821">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="eab41-1822">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-1822">Core</span></span>

* <span data-ttu-id="eab41-1823">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1823">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="eab41-1824">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1824">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="eab41-1825">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1825">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="eab41-1826">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="eab41-1826">Use `--verbose` to see</span></span>
* <span data-ttu-id="eab41-1827">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="eab41-1827">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1828">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1828">ACS</span></span>

* <span data-ttu-id="eab41-1829">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1829">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="eab41-1830">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1830">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1831">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-1831">Appservice</span></span>

* <span data-ttu-id="eab41-1832">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="eab41-1832">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="eab41-1833">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1833">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="eab41-1834">CDN</span><span class="sxs-lookup"><span data-stu-id="eab41-1834">CDN</span></span>

* <span data-ttu-id="eab41-1835">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1835">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="eab41-1836">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="eab41-1836">CosmosDB</span></span>

* <span data-ttu-id="eab41-1837">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1837">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="eab41-1838">Interactive</span><span class="sxs-lookup"><span data-stu-id="eab41-1838">Interactive</span></span>

* <span data-ttu-id="eab41-1839">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1839">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1840">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1840">Network</span></span>

* <span data-ttu-id="eab41-1841">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1841">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="eab41-1842">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1842">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="eab41-1843">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1843">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="eab41-1844">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1844">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="eab41-1845">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1845">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="eab41-1846">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1846">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="eab41-1847">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1847">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="eab41-1848">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1848">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="eab41-1849">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1849">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="eab41-1850">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1850">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="eab41-1851">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-1851">Profile</span></span>

* <span data-ttu-id="eab41-1852">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1852">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-1853">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-1853">Resource</span></span>

* <span data-ttu-id="eab41-1854">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1854">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1855">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1855">Storage</span></span>

* <span data-ttu-id="eab41-1856">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1856">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="eab41-1857">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1857">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="eab41-1858">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1858">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="eab41-1859">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1859">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="eab41-1860">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1860">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1861">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1861">VM</span></span>

* <span data-ttu-id="eab41-1862">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1862">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="eab41-1863">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1863">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="eab41-1864">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1864">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="eab41-1865">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1865">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="eab41-1866">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1866">January 17, 2018</span></span>

<span data-ttu-id="eab41-1867">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="eab41-1867">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-1868">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-1868">ACR</span></span>

* <span data-ttu-id="eab41-1869">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1869">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="eab41-1870">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1870">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1871">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1871">ACS</span></span>

* <span data-ttu-id="eab41-1872">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1872">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="eab41-1873">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1873">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1874">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-1874">Appservice</span></span>

* <span data-ttu-id="eab41-1875">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1875">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="eab41-1876">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1876">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="eab41-1877">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1877">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="eab41-1878">バックアップ</span><span class="sxs-lookup"><span data-stu-id="eab41-1878">Backup</span></span>

* <span data-ttu-id="eab41-1879">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1879">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="eab41-1880">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1880">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="eab41-1881">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1881">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="eab41-1882">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1882">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="eab41-1883">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1883">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="eab41-1884">Batch</span><span class="sxs-lookup"><span data-stu-id="eab41-1884">Batch</span></span>

* <span data-ttu-id="eab41-1885">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1885">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="eab41-1886">クラウド</span><span class="sxs-lookup"><span data-stu-id="eab41-1886">Cloud</span></span>

* <span data-ttu-id="eab41-1887">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1887">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="eab41-1888">消費</span><span class="sxs-lookup"><span data-stu-id="eab41-1888">Consumption</span></span>

* <span data-ttu-id="eab41-1889">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1889">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="eab41-1890">Event Grid</span><span class="sxs-lookup"><span data-stu-id="eab41-1890">Event Grid</span></span>

* <span data-ttu-id="eab41-1891">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1891">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="eab41-1892">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1892">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="eab41-1893">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1893">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="eab41-1894">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="eab41-1894">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="eab41-1895">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1895">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="eab41-1896">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1896">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="eab41-1897">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1897">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="eab41-1898">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1898">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="eab41-1899">Interactive</span><span class="sxs-lookup"><span data-stu-id="eab41-1899">Interactive</span></span>

* <span data-ttu-id="eab41-1900">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1900">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="eab41-1901">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1901">Fixed errors on startup</span></span>
* <span data-ttu-id="eab41-1902">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1902">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="eab41-1903">IoT</span><span class="sxs-lookup"><span data-stu-id="eab41-1903">IoT</span></span>

* <span data-ttu-id="eab41-1904">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1904">Added support for device provisioning service</span></span>
* <span data-ttu-id="eab41-1905">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1905">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="eab41-1906">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1906">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-1907">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-1907">Monitor</span></span>

* <span data-ttu-id="eab41-1908">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1908">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="eab41-1909">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="eab41-1909">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="eab41-1910">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1910">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1911">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1911">Network</span></span>

* <span data-ttu-id="eab41-1912">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1912">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="eab41-1913">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1913">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="eab41-1914">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-1914">Profile</span></span>

* <span data-ttu-id="eab41-1915">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1915">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="eab41-1916">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-1916">Role</span></span>

* <span data-ttu-id="eab41-1917">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1917">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="eab41-1918">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="eab41-1918">Service Fabric</span></span>

* <span data-ttu-id="eab41-1919">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1919">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="eab41-1920">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1920">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1921">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1921">VM</span></span>

* <span data-ttu-id="eab41-1922">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="eab41-1922">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="eab41-1923">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1923">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="eab41-1924">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1924">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="eab41-1925">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1925">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="eab41-1926">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1926">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="eab41-1927">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1927">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="eab41-1928">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1928">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="eab41-1929">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1929">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="eab41-1930">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1930">December 19, 2017</span></span>

<span data-ttu-id="eab41-1931">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="eab41-1931">Version 2.0.23</span></span>

* <span data-ttu-id="eab41-1932">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1932">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="eab41-1933">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-1933">Container</span></span>

* <span data-ttu-id="eab41-1934">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1934">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="eab41-1935">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-1935">Network</span></span>

* <span data-ttu-id="eab41-1936">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1936">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="eab41-1937">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1937">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-1938">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-1938">Storage</span></span>

* <span data-ttu-id="eab41-1939">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1939">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1940">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1940">VM</span></span>

* <span data-ttu-id="eab41-1941">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1941">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="eab41-1942">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1942">December 5, 2017</span></span>

<span data-ttu-id="eab41-1943">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="eab41-1943">Version 2.0.22</span></span>

* <span data-ttu-id="eab41-1944">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-1944">Removed `az component` commands.</span></span> <span data-ttu-id="eab41-1945">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="eab41-1945">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="eab41-1946">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-1946">Core</span></span>
* <span data-ttu-id="eab41-1947">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1947">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="eab41-1948">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1948">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-1949">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1949">ACS</span></span>

* <span data-ttu-id="eab41-1950">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1950">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="eab41-1951">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1951">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="eab41-1952">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1952">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="eab41-1953">Advisor</span><span class="sxs-lookup"><span data-stu-id="eab41-1953">Advisor</span></span>

* <span data-ttu-id="eab41-1954">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="eab41-1954">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1955">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-1955">Appservice</span></span>

* <span data-ttu-id="eab41-1956">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1956">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="eab41-1957">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1957">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="eab41-1958">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1958">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="eab41-1959">消費</span><span class="sxs-lookup"><span data-stu-id="eab41-1959">Consumption</span></span>

* <span data-ttu-id="eab41-1960">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1960">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="eab41-1961">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-1961">Container</span></span>

* <span data-ttu-id="eab41-1962">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1962">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-1963">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-1963">Monitor</span></span>

* <span data-ttu-id="eab41-1964">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1964">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-1965">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-1965">Resource</span></span>

* <span data-ttu-id="eab41-1966">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1966">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="eab41-1967">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-1967">Role</span></span>

* <span data-ttu-id="eab41-1968">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1968">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="eab41-1969">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1969">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="eab41-1970">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1970">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-1971">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-1971">SQL</span></span>

* <span data-ttu-id="eab41-1972">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1972">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="eab41-1973">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1973">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-1974">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-1974">VM</span></span>

* <span data-ttu-id="eab41-1975">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1975">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="eab41-1976">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="eab41-1976">November 14, 2017</span></span>

<span data-ttu-id="eab41-1977">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="eab41-1977">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-1978">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-1978">ACR</span></span>

* <span data-ttu-id="eab41-1979">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1979">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="eab41-1980">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-1980">ACS</span></span>

* <span data-ttu-id="eab41-1981">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1981">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="eab41-1982">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-1982">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="eab41-1983">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1983">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="eab41-1984">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1984">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="eab41-1985">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1985">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-1986">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-1986">Appservice</span></span>

* <span data-ttu-id="eab41-1987">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1987">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="eab41-1988">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1988">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="eab41-1989">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1989">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="eab41-1990">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1990">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="eab41-1991">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1991">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="eab41-1992">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="eab41-1992">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="eab41-1993">Batch</span><span class="sxs-lookup"><span data-stu-id="eab41-1993">Batch</span></span>

* <span data-ttu-id="eab41-1994">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1994">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="eab41-1995">Batchai</span><span class="sxs-lookup"><span data-stu-id="eab41-1995">Batchai</span></span>

* <span data-ttu-id="eab41-1996">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1996">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="eab41-1997">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1997">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="eab41-1998">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1998">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="eab41-1999">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-1999">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="eab41-2000">クラウド</span><span class="sxs-lookup"><span data-stu-id="eab41-2000">Cloud</span></span>

* <span data-ttu-id="eab41-2001">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2001">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="eab41-2002">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-2002">Container</span></span>

* <span data-ttu-id="eab41-2003">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2003">Added support to open multiple ports</span></span>
* <span data-ttu-id="eab41-2004">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2004">Added container group restart policy</span></span>
* <span data-ttu-id="eab41-2005">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2005">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="eab41-2006">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2006">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="eab41-2007">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="eab41-2007">Data Lake Analytics</span></span>

* <span data-ttu-id="eab41-2008">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2008">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="eab41-2009">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="eab41-2009">Data Lake Store</span></span>

* <span data-ttu-id="eab41-2010">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2010">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="eab41-2011">拡張機能</span><span class="sxs-lookup"><span data-stu-id="eab41-2011">Extension</span></span>

* <span data-ttu-id="eab41-2012">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2012">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="eab41-2013">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2013">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="eab41-2014">IoT</span><span class="sxs-lookup"><span data-stu-id="eab41-2014">IoT</span></span>

* <span data-ttu-id="eab41-2015">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2015">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-2016">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-2016">Monitor</span></span>

* <span data-ttu-id="eab41-2017">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2017">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="eab41-2018">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-2018">Network</span></span>

* <span data-ttu-id="eab41-2019">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2019">Added support for CAA DNS records</span></span>
* <span data-ttu-id="eab41-2020">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2020">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="eab41-2021">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2021">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="eab41-2022">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2022">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="eab41-2023">Reservations</span><span class="sxs-lookup"><span data-stu-id="eab41-2023">Reservations</span></span>

* <span data-ttu-id="eab41-2024">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="eab41-2024">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-2025">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-2025">Resource</span></span>

* <span data-ttu-id="eab41-2026">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2026">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-2027">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-2027">SQL</span></span>

* <span data-ttu-id="eab41-2028">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2028">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-2029">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-2029">Storage</span></span>

* <span data-ttu-id="eab41-2030">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2030">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="eab41-2031">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2031">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="eab41-2032">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2032">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="eab41-2033">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2033">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="eab41-2034">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2034">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="eab41-2035">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2035">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="eab41-2036">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2036">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-2037">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-2037">VM</span></span>

* <span data-ttu-id="eab41-2038">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2038">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="eab41-2039">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2039">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="eab41-2040">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2040">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="eab41-2041">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2041">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="eab41-2042">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2042">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="eab41-2043">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="eab41-2043">October 24, 2017</span></span>

<span data-ttu-id="eab41-2044">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="eab41-2044">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="eab41-2045">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-2045">Core</span></span>

* <span data-ttu-id="eab41-2046">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2046">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-2047">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-2047">ACR</span></span>

* <span data-ttu-id="eab41-2048">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2048">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="eab41-2049">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2049">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="eab41-2050">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2050">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-2051">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-2051">ACS</span></span>

* <span data-ttu-id="eab41-2052">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2052">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="eab41-2053">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2053">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-2054">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-2054">Appservice</span></span>

* <span data-ttu-id="eab41-2055">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2055">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="eab41-2056">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="eab41-2056">Component</span></span>

* <span data-ttu-id="eab41-2057">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2057">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-2058">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-2058">Monitor</span></span>

* <span data-ttu-id="eab41-2059">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2059">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-2060">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-2060">Resource</span></span>

* <span data-ttu-id="eab41-2061">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2061">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="eab41-2062">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2062">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-2063">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-2063">VM</span></span>

* <span data-ttu-id="eab41-2064">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2064">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="eab41-2065">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="eab41-2065">October 9, 2017</span></span>

<span data-ttu-id="eab41-2066">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="eab41-2066">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="eab41-2067">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-2067">Core</span></span>

* <span data-ttu-id="eab41-2068">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2068">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-2069">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-2069">Appservice</span></span>

* <span data-ttu-id="eab41-2070">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2070">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="eab41-2071">Batch</span><span class="sxs-lookup"><span data-stu-id="eab41-2071">Batch</span></span>

* <span data-ttu-id="eab41-2072">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2072">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="eab41-2073">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2073">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="eab41-2074">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2074">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="eab41-2075">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2075">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="eab41-2076">Batchai</span><span class="sxs-lookup"><span data-stu-id="eab41-2076">Batchai</span></span>

* <span data-ttu-id="eab41-2077">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="eab41-2077">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="eab41-2078">KeyVault</span><span class="sxs-lookup"><span data-stu-id="eab41-2078">Keyvault</span></span>

* <span data-ttu-id="eab41-2079">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-2079">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="eab41-2080">(#4448)</span><span class="sxs-lookup"><span data-stu-id="eab41-2080">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="eab41-2081">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-2081">Network</span></span>

* <span data-ttu-id="eab41-2082">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2082">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="eab41-2083">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2083">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-2084">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-2084">Resource</span></span>

* <span data-ttu-id="eab41-2085">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2085">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="eab41-2086">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2086">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="eab41-2087">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2087">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="eab41-2088">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2088">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-2089">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-2089">Sql</span></span>

* <span data-ttu-id="eab41-2090">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2090">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="eab41-2091">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="eab41-2091">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="eab41-2092">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="eab41-2092">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-2093">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-2093">Storage</span></span>

* <span data-ttu-id="eab41-2094">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2094">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-2095">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-2095">Vm</span></span>

* <span data-ttu-id="eab41-2096">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2096">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="eab41-2097">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2097">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="eab41-2098">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2098">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="eab41-2099">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2099">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="eab41-2100">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2100">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="eab41-2101">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="eab41-2101">September 22, 2017</span></span>

<span data-ttu-id="eab41-2102">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="eab41-2102">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-2103">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-2103">Resource</span></span>

* <span data-ttu-id="eab41-2104">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2104">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="eab41-2105">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2105">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="eab41-2106">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2106">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="eab41-2107">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2107">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="eab41-2108">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-2108">Network</span></span>

* <span data-ttu-id="eab41-2109">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2109">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="eab41-2110">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2110">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="eab41-2111">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2111">Added `asg` application security group commands</span></span>
* <span data-ttu-id="eab41-2112">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2112">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="eab41-2113">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2113">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="eab41-2114">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2114">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="eab41-2115">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2115">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-2116">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-2116">Storage</span></span>

* <span data-ttu-id="eab41-2117">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2117">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="eab41-2118">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="eab41-2118">Eventgrid</span></span>

* <span data-ttu-id="eab41-2119">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2119">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-2120">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-2120">SQL</span></span>

* <span data-ttu-id="eab41-2121">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-2121">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="eab41-2122">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="eab41-2122">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="eab41-2123">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2123">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="eab41-2124">KeyVault</span><span class="sxs-lookup"><span data-stu-id="eab41-2124">Keyvault</span></span>

* <span data-ttu-id="eab41-2125">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2125">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-2126">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-2126">VM</span></span>

* <span data-ttu-id="eab41-2127">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2127">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="eab41-2128">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2128">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="eab41-2129">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2129">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="eab41-2130">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2130">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="eab41-2131">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2131">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="eab41-2132">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2132">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-2133">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-2133">ACS</span></span>

* <span data-ttu-id="eab41-2134">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2134">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-2135">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-2135">Appservice</span></span>

* <span data-ttu-id="eab41-2136">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2136">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="eab41-2137">バックアップ</span><span class="sxs-lookup"><span data-stu-id="eab41-2137">Backup</span></span>

* <span data-ttu-id="eab41-2138">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="eab41-2138">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="eab41-2139">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="eab41-2139">September 11, 2017</span></span>

<span data-ttu-id="eab41-2140">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="eab41-2140">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="eab41-2141">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-2141">Core</span></span>

* <span data-ttu-id="eab41-2142">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-2142">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="eab41-2143">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2143">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-2144">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-2144">Acs</span></span>

* <span data-ttu-id="eab41-2145">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2145">Added `acs list-locations` command</span></span>
* <span data-ttu-id="eab41-2146">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="eab41-2146">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-2147">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-2147">Appservice</span></span>

* <span data-ttu-id="eab41-2148">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2148">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="eab41-2149">CDN</span><span class="sxs-lookup"><span data-stu-id="eab41-2149">CDN</span></span>

* <span data-ttu-id="eab41-2150">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2150">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="eab41-2151">拡張機能</span><span class="sxs-lookup"><span data-stu-id="eab41-2151">Extension</span></span>

* <span data-ttu-id="eab41-2152">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="eab41-2152">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="eab41-2153">KeyVault</span><span class="sxs-lookup"><span data-stu-id="eab41-2153">Keyvault</span></span>

* <span data-ttu-id="eab41-2154">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2154">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="eab41-2155">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-2155">Network</span></span>

* <span data-ttu-id="eab41-2156">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2156">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="eab41-2157">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2157">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="eab41-2158">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2158">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="eab41-2159">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2159">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="eab41-2160">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2160">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-2161">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-2161">Resource</span></span>

* <span data-ttu-id="eab41-2162">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="eab41-2162">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="eab41-2163">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="eab41-2163">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="eab41-2164">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="eab41-2164">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="eab41-2165">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="eab41-2165">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-2166">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-2166">SQL</span></span>

* <span data-ttu-id="eab41-2167">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2167">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-2168">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-2168">VM</span></span>

* <span data-ttu-id="eab41-2169">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="eab41-2169">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="eab41-2170">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="eab41-2170">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="eab41-2171">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2171">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="eab41-2172">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="eab41-2172">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="eab41-2173">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="eab41-2173">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="eab41-2174">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="eab41-2174">August 31, 2017</span></span>

<span data-ttu-id="eab41-2175">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="eab41-2175">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="eab41-2176">KeyVault</span><span class="sxs-lookup"><span data-stu-id="eab41-2176">Keyvault</span></span>

* <span data-ttu-id="eab41-2177">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2177">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="eab41-2178">SF</span><span class="sxs-lookup"><span data-stu-id="eab41-2178">Sf</span></span>

* <span data-ttu-id="eab41-2179">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="eab41-2179">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-2180">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-2180">Storage</span></span>

* <span data-ttu-id="eab41-2181">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2181">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="eab41-2182">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="eab41-2182">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="eab41-2183">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="eab41-2183">August 28, 2017</span></span>

<span data-ttu-id="eab41-2184">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="eab41-2184">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="eab41-2185">CLI</span><span class="sxs-lookup"><span data-stu-id="eab41-2185">CLI</span></span>

* <span data-ttu-id="eab41-2186">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2186">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-2187">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-2187">ACS</span></span>

* <span data-ttu-id="eab41-2188">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2188">Corrected preview regions</span></span>
* <span data-ttu-id="eab41-2189">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-2189">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="eab41-2190">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2190">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-2191">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-2191">Appservice</span></span>

* <span data-ttu-id="eab41-2192">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2192">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="eab41-2193">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2193">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="eab41-2194">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2194">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="eab41-2195">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2195">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="eab41-2196">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="eab41-2196">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="eab41-2197">IoT</span><span class="sxs-lookup"><span data-stu-id="eab41-2197">IoT</span></span>

* <span data-ttu-id="eab41-2198">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2198">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="eab41-2199">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-2199">Network</span></span>

* <span data-ttu-id="eab41-2200">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2200">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="eab41-2201">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2201">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="eab41-2202">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2202">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="eab41-2203">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2203">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="eab41-2204">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2204">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="eab41-2205">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-2205">Profile</span></span>

* <span data-ttu-id="eab41-2206">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2206">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="eab41-2207">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="eab41-2207">Service Fabric</span></span>

* <span data-ttu-id="eab41-2208">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="eab41-2208">Preview release</span></span>
* <span data-ttu-id="eab41-2209">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2209">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="eab41-2210">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2210">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="eab41-2211">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2211">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-2212">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-2212">Storage</span></span>

* <span data-ttu-id="eab41-2213">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-2213">Enabled setting blob tier</span></span>
* <span data-ttu-id="eab41-2214">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2214">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="eab41-2215">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2215">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="eab41-2216">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-2216">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="eab41-2217">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2217">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="eab41-2218">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="eab41-2218">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-2219">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-2219">VM</span></span>

* <span data-ttu-id="eab41-2220">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2220">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="eab41-2221">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-2221">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="eab41-2222">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2222">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="eab41-2223">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2223">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="eab41-2224">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2224">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="eab41-2225">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2225">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="eab41-2226">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="eab41-2226">August 15, 2017</span></span>

<span data-ttu-id="eab41-2227">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="eab41-2227">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-2228">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-2228">ACS</span></span>

* <span data-ttu-id="eab41-2229">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2229">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-2230">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-2230">Appservice</span></span>

* <span data-ttu-id="eab41-2231">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2231">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="eab41-2232">Event Grid</span><span class="sxs-lookup"><span data-stu-id="eab41-2232">Event Grid</span></span>

* <span data-ttu-id="eab41-2233">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2233">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="eab41-2234">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="eab41-2234">August 11, 2017</span></span>

<span data-ttu-id="eab41-2235">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="eab41-2235">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-2236">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-2236">ACS</span></span>

* <span data-ttu-id="eab41-2237">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2237">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="eab41-2238">Batch</span><span class="sxs-lookup"><span data-stu-id="eab41-2238">Batch</span></span>

* <span data-ttu-id="eab41-2239">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2239">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="eab41-2240">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2240">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="eab41-2241">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2241">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="eab41-2242">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2242">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="eab41-2243">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2243">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="eab41-2244">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2244">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="eab41-2245">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="eab41-2245">Component</span></span>

* <span data-ttu-id="eab41-2246">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2246">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="eab41-2247">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eab41-2247">Container</span></span>

* <span data-ttu-id="eab41-2248">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2248">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="eab41-2249">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="eab41-2249">Data Lake Store</span></span>

* <span data-ttu-id="eab41-2250">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-2250">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="eab41-2251">Event Grid</span><span class="sxs-lookup"><span data-stu-id="eab41-2251">Event Grid</span></span>

* <span data-ttu-id="eab41-2252">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="eab41-2252">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="eab41-2253">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-2253">Network</span></span>

* <span data-ttu-id="eab41-2254">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2254">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="eab41-2255">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2255">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="eab41-2256">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2256">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="eab41-2257">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2257">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="eab41-2258">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-2258">Profile</span></span>

* <span data-ttu-id="eab41-2259">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2259">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-2260">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-2260">Storage</span></span>

* <span data-ttu-id="eab41-2261">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="eab41-2261">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-2262">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-2262">VM</span></span>

* <span data-ttu-id="eab41-2263">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2263">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="eab41-2264">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2264">Exposed `list-skus` command</span></span>
* <span data-ttu-id="eab41-2265">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2265">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="eab41-2266">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="eab41-2266">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="eab41-2267">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2267">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="eab41-2268">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="eab41-2268">July 28, 2017</span></span>

<span data-ttu-id="eab41-2269">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="eab41-2269">Version 2.0.12</span></span>

* <span data-ttu-id="eab41-2270">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2270">Added container commands</span></span>
* <span data-ttu-id="eab41-2271">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2271">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="eab41-2272">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-2272">Core</span></span>

* <span data-ttu-id="eab41-2273">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="eab41-2273">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="eab41-2274">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2274">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="eab41-2275">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="eab41-2275">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="eab41-2276">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="eab41-2276">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="eab41-2277">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="eab41-2277">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="eab41-2278">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="eab41-2278">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="eab41-2279">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="eab41-2279">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="eab41-2280">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="eab41-2280">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="eab41-2281">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="eab41-2281">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="eab41-2282">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="eab41-2282">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="eab41-2283">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="eab41-2283">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="eab41-2284">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="eab41-2284">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="eab41-2285">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2285">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="eab41-2286">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2286">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="eab41-2287">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2287">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="eab41-2288">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="eab41-2288">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="eab41-2289">ACR</span><span class="sxs-lookup"><span data-stu-id="eab41-2289">ACR</span></span>

* <span data-ttu-id="eab41-2290">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2290">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="eab41-2291">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2291">Support SKU update for managed registries</span></span>
* <span data-ttu-id="eab41-2292">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2292">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="eab41-2293">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2293">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="eab41-2294">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2294">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="eab41-2295">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2295">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-2296">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-2296">ACS</span></span>

* <span data-ttu-id="eab41-2297">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2297">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-2298">Appservice</span><span class="sxs-lookup"><span data-stu-id="eab41-2298">Appservice</span></span>

* <span data-ttu-id="eab41-2299">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2299">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="eab41-2300">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2300">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="eab41-2301">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="eab41-2301">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="eab41-2302">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="eab41-2302">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="eab41-2303">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="eab41-2303">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="eab41-2304">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="eab41-2304">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="eab41-2305">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="eab41-2305">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="eab41-2306">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="eab41-2306">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="eab41-2307">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-2307">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="eab41-2308">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="eab41-2308">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="eab41-2309">Batch</span><span class="sxs-lookup"><span data-stu-id="eab41-2309">Batch</span></span>

* <span data-ttu-id="eab41-2310">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="eab41-2310">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="eab41-2311">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2311">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="eab41-2312">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2312">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="eab41-2313">CDN</span><span class="sxs-lookup"><span data-stu-id="eab41-2313">CDN</span></span>

* <span data-ttu-id="eab41-2314">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2314">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="eab41-2315">クラウド</span><span class="sxs-lookup"><span data-stu-id="eab41-2315">Cloud</span></span>

* <span data-ttu-id="eab41-2316">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2316">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="eab41-2317">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="eab41-2317">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="eab41-2318">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2318">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="eab41-2319">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2319">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="eab41-2320">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2320">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="eab41-2321">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="eab41-2321">CosmosDB</span></span>

* <span data-ttu-id="eab41-2322">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2322">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="eab41-2323">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2323">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="eab41-2324">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="eab41-2324">Data Lake Analytics</span></span>

* <span data-ttu-id="eab41-2325">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2325">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="eab41-2326">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2326">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="eab41-2327">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2327">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="eab41-2328">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="eab41-2328">Data Lake Store</span></span>

* <span data-ttu-id="eab41-2329">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2329">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="eab41-2330">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2330">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="eab41-2331">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-2331">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="eab41-2332">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="eab41-2332">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="eab41-2333">対話</span><span class="sxs-lookup"><span data-stu-id="eab41-2333">Interactive</span></span>

* <span data-ttu-id="eab41-2334">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2334">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="eab41-2335">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="eab41-2335">Increased test coverage</span></span>
* <span data-ttu-id="eab41-2336">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2336">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="eab41-2337">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="eab41-2337">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="eab41-2338">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="eab41-2338">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="eab41-2339">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="eab41-2339">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="eab41-2340">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="eab41-2340">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="eab41-2341">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2341">Added `--progress` flag</span></span>
* <span data-ttu-id="eab41-2342">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2342">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="eab41-2343">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="eab41-2343">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="eab41-2344">IoT</span><span class="sxs-lookup"><span data-stu-id="eab41-2344">IoT</span></span>

* <span data-ttu-id="eab41-2345">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-2345">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="eab41-2346">(#3934)</span><span class="sxs-lookup"><span data-stu-id="eab41-2346">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="eab41-2347">Key Vault</span><span class="sxs-lookup"><span data-stu-id="eab41-2347">Key vault</span></span>

* <span data-ttu-id="eab41-2348">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-2348">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="eab41-2349">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="eab41-2349">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="eab41-2350">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="eab41-2350">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="eab41-2351">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="eab41-2351">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="eab41-2352">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="eab41-2352">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="eab41-2353">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="eab41-2353">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="eab41-2354">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-2354">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="eab41-2355">(#3307)</span><span class="sxs-lookup"><span data-stu-id="eab41-2355">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="eab41-2356">ラボ</span><span class="sxs-lookup"><span data-stu-id="eab41-2356">Lab</span></span>

* <span data-ttu-id="eab41-2357">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2357">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="eab41-2358">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2358">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-2359">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-2359">Monitor</span></span>

* <span data-ttu-id="eab41-2360">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="eab41-2360">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="eab41-2361">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2361">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="eab41-2362">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2362">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="eab41-2363">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2363">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="eab41-2364">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2364">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="eab41-2365">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="eab41-2365">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="eab41-2366">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2366">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="eab41-2367">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="eab41-2367">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="eab41-2368">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2368">`location` no longer required</span></span>
  * <span data-ttu-id="eab41-2369">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="eab41-2369">Add name and ID support for target</span></span>
  * <span data-ttu-id="eab41-2370">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="eab41-2370">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="eab41-2371">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-2371">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="eab41-2372">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2372">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="eab41-2373">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="eab41-2373">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="eab41-2374">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2374">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="eab41-2375">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2375">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="eab41-2376">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-2376">Network</span></span>

* <span data-ttu-id="eab41-2377">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2377">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="eab41-2378">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2378">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="eab41-2379">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2379">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="eab41-2380">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2380">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="eab41-2381">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2381">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="eab41-2382">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2382">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="eab41-2383">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2383">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="eab41-2384">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2384">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="eab41-2385">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2385">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="eab41-2386">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2386">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="eab41-2387">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2387">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="eab41-2388">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2388">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="eab41-2389">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2389">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="eab41-2390">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2390">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="eab41-2391">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2391">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="eab41-2392">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2392">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="eab41-2393">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2393">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="eab41-2394">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2394">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="eab41-2395">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2395">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="eab41-2396">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2396">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="eab41-2397">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2397">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="eab41-2398">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2398">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="eab41-2399">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2399">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="eab41-2400">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="eab41-2400">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="eab41-2401">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="eab41-2401">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="eab41-2402">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="eab41-2402">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="eab41-2403">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="eab41-2403">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="eab41-2404">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-2404">Profile</span></span>

* <span data-ttu-id="eab41-2405">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2405">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="eab41-2406">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2406">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="eab41-2407">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="eab41-2407">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="eab41-2408">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2408">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="eab41-2409">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2409">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="eab41-2410">RDBMS</span><span class="sxs-lookup"><span data-stu-id="eab41-2410">RDBMS</span></span>

* <span data-ttu-id="eab41-2411">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="eab41-2411">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="eab41-2412">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="eab41-2412">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="eab41-2413">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="eab41-2413">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="eab41-2414">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="eab41-2414">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-2415">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-2415">Resource</span></span>

* <span data-ttu-id="eab41-2416">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2416">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="eab41-2417">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2417">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="eab41-2418">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2418">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="eab41-2419">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2419">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="eab41-2420">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="eab41-2420">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="eab41-2421">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2421">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="eab41-2422">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="eab41-2422">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="eab41-2423">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2423">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="eab41-2424">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-2424">Role</span></span>

* <span data-ttu-id="eab41-2425">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2425">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="eab41-2426">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="eab41-2426">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="eab41-2427">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="eab41-2427">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="eab41-2428">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="eab41-2428">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="eab41-2429">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2429">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="eab41-2430">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="eab41-2430">Service Fabric</span></span>
* <span data-ttu-id="eab41-2431">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="eab41-2431">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="eab41-2432">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="eab41-2432">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="eab41-2433">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="eab41-2433">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-2434">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-2434">SQL</span></span>

* <span data-ttu-id="eab41-2435">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2435">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="eab41-2436">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2436">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="eab41-2437">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2437">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-2438">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-2438">Storage</span></span>

* <span data-ttu-id="eab41-2439">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="eab41-2439">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="eab41-2440">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-2440">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="eab41-2441">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="eab41-2441">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="eab41-2442">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="eab41-2442">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="eab41-2443">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="eab41-2443">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="eab41-2444">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="eab41-2444">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-2445">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-2445">VM</span></span>

* <span data-ttu-id="eab41-2446">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2446">Support configuring nsg</span></span>
* <span data-ttu-id="eab41-2447">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2447">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="eab41-2448">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="eab41-2448">Support managed service identities</span></span>
* <span data-ttu-id="eab41-2449">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2449">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="eab41-2450">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="eab41-2450">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="eab41-2451">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="eab41-2451">May 10, 2017</span></span>

<span data-ttu-id="eab41-2452">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="eab41-2452">Version 2.0.6</span></span>

* <span data-ttu-id="eab41-2453">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2453">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="eab41-2454">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2454">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="eab41-2455">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2455">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="eab41-2456">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2456">Include Cognitive Services module</span></span>
* <span data-ttu-id="eab41-2457">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2457">Include Service Fabric module</span></span>
* <span data-ttu-id="eab41-2458">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="eab41-2458">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="eab41-2459">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2459">Add support for CDN commands</span></span>
* <span data-ttu-id="eab41-2460">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2460">Remove Container module</span></span>
* <span data-ttu-id="eab41-2461">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="eab41-2461">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="eab41-2462">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="eab41-2462">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="eab41-2463">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-2463">Core</span></span>

* <span data-ttu-id="eab41-2464">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="eab41-2464">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="eab41-2465">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="eab41-2465">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="eab41-2466">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="eab41-2466">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="eab41-2467">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="eab41-2467">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="eab41-2468">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="eab41-2468">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="eab41-2469">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="eab41-2469">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="eab41-2470">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="eab41-2470">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="eab41-2471">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="eab41-2471">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="eab41-2472">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="eab41-2472">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="eab41-2473">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="eab41-2473">core: Improved performance</span></span>
* <span data-ttu-id="eab41-2474">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="eab41-2474">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="eab41-2475">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="eab41-2475">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-2476">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-2476">ACS</span></span>

* <span data-ttu-id="eab41-2477">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2477">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="eab41-2478">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2478">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="eab41-2479">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2479">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="eab41-2480">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="eab41-2480">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-2481">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-2481">AppService</span></span>

* <span data-ttu-id="eab41-2482">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2482">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="eab41-2483">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2483">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="eab41-2484">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="eab41-2484">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="eab41-2485">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2485">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="eab41-2486">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2486">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="eab41-2487">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="eab41-2487">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="eab41-2488">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="eab41-2488">support slot swap with preview</span></span>
* <span data-ttu-id="eab41-2489">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="eab41-2489">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="eab41-2490">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="eab41-2490">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="eab41-2491">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="eab41-2491">CosmosDB</span></span>

* <span data-ttu-id="eab41-2492">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2492">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="eab41-2493">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2493">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="eab41-2494">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2494">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="eab41-2495">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2495">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="eab41-2496">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="eab41-2496">Data Lake Analytics</span></span>

* <span data-ttu-id="eab41-2497">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2497">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="eab41-2498">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="eab41-2498">Add support for new catalog item type: package.</span></span> <span data-ttu-id="eab41-2499">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="eab41-2499">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="eab41-2500">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="eab41-2500">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="eab41-2501">テーブル</span><span class="sxs-lookup"><span data-stu-id="eab41-2501">Table</span></span>
  * <span data-ttu-id="eab41-2502">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="eab41-2502">Table valued function</span></span>
  * <span data-ttu-id="eab41-2503">表示</span><span class="sxs-lookup"><span data-stu-id="eab41-2503">View</span></span>
  * <span data-ttu-id="eab41-2504">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="eab41-2504">Table Statistics.</span></span> <span data-ttu-id="eab41-2505">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="eab41-2505">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="eab41-2506">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="eab41-2506">Data Lake Store</span></span>

* <span data-ttu-id="eab41-2507">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2507">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="eab41-2508">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="eab41-2508">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="eab41-2509">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="eab41-2509">missed help for access show.</span></span> <span data-ttu-id="eab41-2510">追加しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2510">adding it.</span></span> <span data-ttu-id="eab41-2511">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="eab41-2511">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="eab41-2512">検索</span><span class="sxs-lookup"><span data-stu-id="eab41-2512">Find</span></span>

* <span data-ttu-id="eab41-2513">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="eab41-2513">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="eab41-2514">KeyVault</span><span class="sxs-lookup"><span data-stu-id="eab41-2514">KeyVault</span></span>

* <span data-ttu-id="eab41-2515">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2515">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="eab41-2516">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2516">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="eab41-2517">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="eab41-2517">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="eab41-2518">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2518">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="eab41-2519">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="eab41-2519">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="eab41-2520">ラボ</span><span class="sxs-lookup"><span data-stu-id="eab41-2520">Lab</span></span>

* <span data-ttu-id="eab41-2521">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2521">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="eab41-2522">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2522">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="eab41-2523">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2523">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="eab41-2524">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2524">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="eab41-2525">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2525">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="eab41-2526">監視</span><span class="sxs-lookup"><span data-stu-id="eab41-2526">Monitor</span></span>

* <span data-ttu-id="eab41-2527">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="eab41-2527">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="eab41-2528">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="eab41-2528">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="eab41-2529">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-2529">Network</span></span>

* <span data-ttu-id="eab41-2530">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2530">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="eab41-2531">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2531">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="eab41-2532">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2532">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="eab41-2533">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2533">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="eab41-2534">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2534">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="eab41-2535">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2535">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="eab41-2536">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2536">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="eab41-2537">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2537">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="eab41-2538">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2538">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="eab41-2539">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2539">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="eab41-2540">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2540">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="eab41-2541">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2541">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="eab41-2542">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2542">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="eab41-2543">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2543">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="eab41-2544">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="eab41-2544">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="eab41-2545">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2545">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="eab41-2546">プロファイル</span><span class="sxs-lookup"><span data-stu-id="eab41-2546">Profile</span></span>

* <span data-ttu-id="eab41-2547">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="eab41-2547">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="eab41-2548">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="eab41-2548">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="eab41-2549">Redis</span><span class="sxs-lookup"><span data-stu-id="eab41-2549">Redis</span></span>

* <span data-ttu-id="eab41-2550">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2550">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="eab41-2551">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2551">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="eab41-2552">Resource</span><span class="sxs-lookup"><span data-stu-id="eab41-2552">Resource</span></span>

* <span data-ttu-id="eab41-2553">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="eab41-2553">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="eab41-2554">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="eab41-2554">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="eab41-2555">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="eab41-2555">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="eab41-2556">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2556">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="eab41-2557">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="eab41-2557">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="eab41-2558">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2558">Add docs for az lock update.</span></span> <span data-ttu-id="eab41-2559">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="eab41-2559">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="eab41-2560">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="eab41-2560">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="eab41-2561">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="eab41-2561">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="eab41-2562">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="eab41-2562">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="eab41-2563">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="eab41-2563">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="eab41-2564">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="eab41-2564">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="eab41-2565">Role</span><span class="sxs-lookup"><span data-stu-id="eab41-2565">Role</span></span>

* <span data-ttu-id="eab41-2566">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="eab41-2566">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="eab41-2567">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="eab41-2567">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="eab41-2568">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="eab41-2568">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="eab41-2569">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="eab41-2569">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="eab41-2570">SQL</span><span class="sxs-lookup"><span data-stu-id="eab41-2570">SQL</span></span>

* <span data-ttu-id="eab41-2571">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="eab41-2571">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="eab41-2572">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="eab41-2572">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="eab41-2573">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-2573">Storage</span></span>

* <span data-ttu-id="eab41-2574">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="eab41-2574">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="eab41-2575">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2575">Add support for incremental blob copy</span></span>
* <span data-ttu-id="eab41-2576">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2576">Add support for large block blob upload</span></span>
* <span data-ttu-id="eab41-2577">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="eab41-2577">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-2578">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-2578">VM</span></span>

* <span data-ttu-id="eab41-2579">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="eab41-2579">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="eab41-2580">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="eab41-2580">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="eab41-2581">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="eab41-2581">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="eab41-2582">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="eab41-2582">az vm/vmss disk</span></span>
  3. <span data-ttu-id="eab41-2583">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="eab41-2583">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="eab41-2584">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="eab41-2584">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="eab41-2585">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="eab41-2585">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="eab41-2586">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="eab41-2586">April 3, 2017</span></span>

<span data-ttu-id="eab41-2587">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="eab41-2587">Version 2.0.2</span></span>

<span data-ttu-id="eab41-2588">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="eab41-2588">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="eab41-2589">コア</span><span class="sxs-lookup"><span data-stu-id="eab41-2589">Core</span></span>

* <span data-ttu-id="eab41-2590">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="eab41-2590">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="eab41-2591">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="eab41-2591">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="eab41-2592">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="eab41-2592">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="eab41-2593">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="eab41-2593">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="eab41-2594">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="eab41-2594">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="eab41-2595">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="eab41-2595">Add prompting for missing template parameters.</span></span> <span data-ttu-id="eab41-2596">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="eab41-2596">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="eab41-2597">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="eab41-2597">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="eab41-2598">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="eab41-2598">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="eab41-2599">ACS</span><span class="sxs-lookup"><span data-stu-id="eab41-2599">ACS</span></span>

* <span data-ttu-id="eab41-2600">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="eab41-2600">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="eab41-2601">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="eab41-2601">Add support for ssh key password prompting.</span></span> <span data-ttu-id="eab41-2602">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="eab41-2602">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="eab41-2603">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="eab41-2603">Add support for windows clusters.</span></span> <span data-ttu-id="eab41-2604">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="eab41-2604">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="eab41-2605">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="eab41-2605">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="eab41-2606">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="eab41-2606">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="eab41-2607">AppService</span><span class="sxs-lookup"><span data-stu-id="eab41-2607">AppService</span></span>

* <span data-ttu-id="eab41-2608">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="eab41-2608">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="eab41-2609">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="eab41-2609">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="eab41-2610">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="eab41-2610">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="eab41-2611">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="eab41-2611">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="eab41-2612">DataLake</span><span class="sxs-lookup"><span data-stu-id="eab41-2612">DataLake</span></span>

* <span data-ttu-id="eab41-2613">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="eab41-2613">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="eab41-2614">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="eab41-2614">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="eab41-2615">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="eab41-2615">DocuemntDB</span></span>

* <span data-ttu-id="eab41-2616">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="eab41-2616">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="eab41-2617">VM</span><span class="sxs-lookup"><span data-stu-id="eab41-2617">VM</span></span>

* <span data-ttu-id="eab41-2618">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="eab41-2618">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="eab41-2619">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="eab41-2619">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="eab41-2620">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="eab41-2620">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="eab41-2621">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="eab41-2621">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="eab41-2622">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="eab41-2622">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="eab41-2623">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="eab41-2623">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="eab41-2624">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="eab41-2624">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="eab41-2625">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="eab41-2625">February 27, 2017</span></span>

<span data-ttu-id="eab41-2626">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="eab41-2626">Version 2.0.0</span></span>

<span data-ttu-id="eab41-2627">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="eab41-2627">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="eab41-2628">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="eab41-2628">Container Service (acs)</span></span>
- <span data-ttu-id="eab41-2629">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="eab41-2629">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="eab41-2630">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="eab41-2630">Networking</span></span>
- <span data-ttu-id="eab41-2631">Storage</span><span class="sxs-lookup"><span data-stu-id="eab41-2631">Storage</span></span>

<span data-ttu-id="eab41-2632">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="eab41-2632">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="eab41-2633">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="eab41-2633">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="eab41-2634">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="eab41-2634">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="eab41-2635">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="eab41-2635">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="eab41-2636">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="eab41-2636">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="eab41-2637">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="eab41-2637">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="eab41-2638">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="eab41-2638">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="eab41-2639">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="eab41-2639">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="eab41-2640">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="eab41-2640">Provide feedback from the command line with the `az feedback` command</span></span>

