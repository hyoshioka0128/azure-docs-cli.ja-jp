---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 06/18/2019
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 8431946b169b550bfd3f5120cf26e2feeb5c9f2c
ms.sourcegitcommit: 399f0a2997675fbb280243e4234cf63c3bbca819
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2019
ms.locfileid: "67194865"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="b63ae-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="b63ae-103">Azure CLI release notes</span></span>

## <a name="june-18-2019"></a><span data-ttu-id="b63ae-104">2019 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-104">June 18, 2019</span></span>

<span data-ttu-id="b63ae-105">バージョン 2.0.67</span><span class="sxs-lookup"><span data-stu-id="b63ae-105">Version 2.0.67</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-106">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-106">Core</span></span>

<span data-ttu-id="b63ae-107">このリリースでは、新しい [プレビュー] タグが導入され、コマンド グループ、コマンド、または引数がプレビュー状態である場合に、お客様により明確に通知できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-107">This release introduces a new [Preview] tag to more clearly communicate to customers when a command group, command or argument is in preview status.</span></span> <span data-ttu-id="b63ae-108">以前は、これはヘルプ テキストで通知されていたか、コマンド モジュールのバージョン番号によって暗黙的に通知されていました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-108">This was previously called out in help text or communicated implicitly by the command module version number.</span></span>
<span data-ttu-id="b63ae-109">CLI では、将来、個々のパッケージのバージョン番号が削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="b63ae-109">The CLI will be removing version numbers for individual packages in the future.</span></span> <span data-ttu-id="b63ae-110">コマンドがプレビュー状態の場合は、そのすべての引数もプレビュー状態です。</span><span class="sxs-lookup"><span data-stu-id="b63ae-110">If a command is in preview, all of its arguments are as well.</span></span> <span data-ttu-id="b63ae-111">コマンド グループにプレビュー状態のラベルが付いている場合、すべてのコマンドと引数もプレビュー状態と見なされます。</span><span class="sxs-lookup"><span data-stu-id="b63ae-111">If a command group is labeled as being in preview, then all commands and arguments are considered to be in preview as well.</span></span>

<span data-ttu-id="b63ae-112">この変更の結果、このリリースでは、一部のコマンド グループが "突然" プレビュー状態になったように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="b63ae-112">As a result of this change, several command groups may seem to "suddenly" appear to be in a preview status with this release.</span></span> <span data-ttu-id="b63ae-113">ほとんどのパッケージがプレビュー状態にあったのですが、このリリースでは一般提供と見なされていることがその真相です</span><span class="sxs-lookup"><span data-stu-id="b63ae-113">What actually happened is that most packages were in a preview status, but are being deemed GA with this release</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-114">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-114">ACR</span></span>
* <span data-ttu-id="b63ae-115">'acr check-health' コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-115">Added 'acr check-health' command</span></span>
* <span data-ttu-id="b63ae-116">AAD トークンおよび外部コマンドの取得に関するエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-116">Improved error handling for AAD tokens and for retrieving external commands</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-117">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-117">ACS</span></span>
* <span data-ttu-id="b63ae-118">非推奨の ACS コマンドがヘルプ ビューで非表示になりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-118">Deprecated ACS commands are now hidden from help view</span></span>

### <a name="ams"></a><span data-ttu-id="b63ae-119">AMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-119">AMS</span></span>
* <span data-ttu-id="b63ae-120">[破壊的変更] archive-window-length および key-frame-interval-duration の ISO 8601 時間文字列を返すように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-120">[BREAKING CHANGE] Changed to return ISO 8601 time strings for archive-window-length and key-frame-interval-duration</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-121">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-121">AppService</span></span>
* <span data-ttu-id="b63ae-122">`webapp deleted list` および `webapp deleted restore` に対してロケーション ベースのルーティングを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-122">Added location based routing for `webapp deleted list` and `webapp deleted restore`</span></span>
* <span data-ttu-id="b63ae-123">Azure Cloud Shell で Web アプリのログに記録されたターゲット URL ("You can launch the app at...") がクリックできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-123">Fixed issue where webapp up logged target URL ("You can launch the app at...") was not clickable in Azure Cloud Shell</span></span>
* <span data-ttu-id="b63ae-124">一部の SKU でのアプリ作成が AlwaysOn エラーで失敗するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-124">Fixed an issue where creating apps with the some SKUs was failing with an AlwaysOn error</span></span>
* <span data-ttu-id="b63ae-125">`[appservice|webapp] create` に事前検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-125">Added pre-validation to `[appservice|webapp] create`</span></span>
* <span data-ttu-id="b63ae-126">正しい actionHostName を使用するように `[webapp|functionapp] traffic-routing` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-126">Fixed `[webapp|functionapp] traffic-routing` to use the correct actionHostName</span></span>
* <span data-ttu-id="b63ae-127">`functionapp` コマンドにスロット サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-127">Added slot support to `functionapp` commands</span></span>

### <a name="batch"></a><span data-ttu-id="b63ae-128">Batch</span><span class="sxs-lookup"><span data-stu-id="b63ae-128">Batch</span></span>
* <span data-ttu-id="b63ae-129">共有キー認証の過度のエラー報告による AAD 認証の回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-129">Fixed AAD auth regression caused by over-aggressive error reporting for Shared Key Auth</span></span>

### <a name="batchai"></a><span data-ttu-id="b63ae-130">BatchAI</span><span class="sxs-lookup"><span data-stu-id="b63ae-130">BatchAI</span></span>
* <span data-ttu-id="b63ae-131">BatchAI コマンドが非推奨となり、非表示になりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-131">BatchAI commands are now deprecated and hidden</span></span>

### <a name="botservice"></a><span data-ttu-id="b63ae-132">BotService</span><span class="sxs-lookup"><span data-stu-id="b63ae-132">BotService</span></span>
* <span data-ttu-id="b63ae-133">v3 SDK をサポートするコマンドに "廃止されたサポート"/"保守モード" 警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-133">Added "discontinued support"/"maintenance mode" warning messages for commands that support the v3 SDK</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b63ae-134">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b63ae-134">CosmosDB</span></span>
* <span data-ttu-id="b63ae-135">[非推奨] `cosmosdb list-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-135">[DEPRECATED] Deprecated the `cosmosdb list-keys` command</span></span>
* <span data-ttu-id="b63ae-136">`cosmosdb keys list` コマンドを追加しました。`cosmosdb list-keys` に置き換わるものです</span><span class="sxs-lookup"><span data-stu-id="b63ae-136">Added the `cosmosdb keys list` command - replaces `cosmosdb list-keys`</span></span>
* <span data-ttu-id="b63ae-137">`cosmsodb create/update`:"isZoneRedundant" プロパティを設定できるように --location の新しいフォーマットを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-137">`cosmsodb create/update`: Added new format for --location to allow setting "isZoneRedundant" property.</span></span> <span data-ttu-id="b63ae-138">古いフォーマットを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-138">Deprecated old format</span></span>

### <a name="eventgrid"></a><span data-ttu-id="b63ae-139">EventGrid</span><span class="sxs-lookup"><span data-stu-id="b63ae-139">EventGrid</span></span>
* <span data-ttu-id="b63ae-140">ドメイン CRUD 操作のための `eventgrid domain` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-140">Added `eventgrid domain` commands for domain CRUD operations</span></span>
* <span data-ttu-id="b63ae-141">ドメイン トピック CRUD 操作のための `eventgrid domain topic` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-141">Added `eventgrid domain topic` commands for domain topics CRUD operations</span></span>
* <span data-ttu-id="b63ae-142">OData 構文を使用して結果をフィルタリングするための `--odata-query` 引数を `eventgrid [topic|event-subscription] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-142">Added `--odata-query` argument to `eventgrid [topic|event-subscription] list` for filtering results using OData syntax</span></span>
* <span data-ttu-id="b63ae-143">`event-subscription create/update`:`--endpoint-type` パラメーターの新しい値として servicebusqueue を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-143">`event-subscription create/update`: Added servicebusqueue as new values for the `--endpoint-type` parameter</span></span>
* <span data-ttu-id="b63ae-144">[破壊的変更] `eventgrid event-subscription [create|update]` での `--included-event-types All` のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-144">[BREAKING CHANGE] Removed support for `--included-event-types All` with `eventgrid event-subscription [create|update]`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="b63ae-145">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b63ae-145">HDInsight</span></span>
* <span data-ttu-id="b63ae-146">`hdinsight create` コマンドでの `--ssh-public-key` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-146">Added support for `--ssh-public-key` parameter in `hdinsight create` command</span></span>

### <a name="iot"></a><span data-ttu-id="b63ae-147">IoT</span><span class="sxs-lookup"><span data-stu-id="b63ae-147">IoT</span></span>
* <span data-ttu-id="b63ae-148">承認ポリシー キーの再生成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-148">Added support to regenerate authorization policy keys</span></span>
* <span data-ttu-id="b63ae-149">DigitalTwin リポジトリ プロビジョニング サービスの SDK およびサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-149">Added SDK and support for DigitalTwin Repository Provisioning Service</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-150">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-150">Network</span></span>
* <span data-ttu-id="b63ae-151">Nat Gateway に対するゾーン サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-151">Added Zone support for Nat Gateway</span></span>
* <span data-ttu-id="b63ae-152">`network list-service-tags` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-152">Added command `network list-service-tags`</span></span>
* <span data-ttu-id="b63ae-153">ユーザーがワイルドカード A レコードをインポートできない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-153">Fixed issue with `dns zone import` where users could not import wildcard A records</span></span>
* <span data-ttu-id="b63ae-154">特定のリージョンでフロー ロギングを有効にできない `watcher flow-log configure` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-154">Fixed issue with `watcher flow-log configure` where flow logging could not be enabled in certain regions</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-155">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-155">Resource</span></span>
* <span data-ttu-id="b63ae-156">REST 呼び出しを行うための `az rest` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-156">Added `az rest` command for making REST calls</span></span>
* <span data-ttu-id="b63ae-157">リソース グループまたはサブスクリプション レベル`--scope` で `policy assignment list` を使用する場合のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-157">Fixed error when using `policy assignment list` with a resource group or subscription level `--scope`</span></span>

### <a name="servicebus"></a><span data-ttu-id="b63ae-158">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b63ae-158">ServiceBus</span></span>
* <span data-ttu-id="b63ae-159">`servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319) での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-159">Fixed issue with `servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319)</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-160">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-160">SQL</span></span>
* <span data-ttu-id="b63ae-161">`--location` を `sql [server|mi] create` のオプションに変更しました - 指定されていない場合、リソース グループの場所を使用します</span><span class="sxs-lookup"><span data-stu-id="b63ae-161">Changed `--location` to be optional for `sql [server|mi] create` - uses resource group location if not specified</span></span>
* <span data-ttu-id="b63ae-162">`sql db list-editions --available` の "'NoneType' object is not iterable" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-162">Fixed "'NoneType' object is not iterable" error for `sql db list-editions --available`</span></span>

### <a name="sqlvm"></a><span data-ttu-id="b63ae-163">SQLVm</span><span class="sxs-lookup"><span data-stu-id="b63ae-163">SQLVm</span></span>
* <span data-ttu-id="b63ae-164">[破壊的変更] `--license-type` パラメーターを必要とするように `sql vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-164">[BREAKING CHNAGE] Changed `sql vm create` to require `--license-type` parameter</span></span>
* <span data-ttu-id="b63ae-165">sql vm の作成または更新時に SQL イメージ SKU を設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-165">Changed to allow setting SQL image SKU when creating or updating a sql vm</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-166">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-166">Storage</span></span>
* <span data-ttu-id="b63ae-167">`storage container generate-sas` のアカウント キーが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-167">Fixed issue with missing account key for `storage container generate-sas`</span></span>
* <span data-ttu-id="b63ae-168">Linux での `storage blob sync` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-168">Fixed issue with `storage blob sync` on Linux</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-169">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-169">VM</span></span>
* <span data-ttu-id="b63ae-170">[プレビュー] VM イメージを構築するための `vm image template` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-170">[PREVIEW] Added `vm image template` commands to build VM images</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="b63ae-171">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-171">June 4, 2019</span></span>

<span data-ttu-id="b63ae-172">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="b63ae-172">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-173">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-173">Core</span></span>
* <span data-ttu-id="b63ae-174">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-174">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-175">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-175">ACR</span></span>
* <span data-ttu-id="b63ae-176">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-176">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-177">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-177">ACS</span></span>
* <span data-ttu-id="b63ae-178">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-178">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="b63ae-179">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-179">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="b63ae-180">Batch</span><span class="sxs-lookup"><span data-stu-id="b63ae-180">Batch</span></span>
* <span data-ttu-id="b63ae-181">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-181">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="b63ae-182">IoT</span><span class="sxs-lookup"><span data-stu-id="b63ae-182">IoT</span></span>
* <span data-ttu-id="b63ae-183">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-183">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-184">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-184">Network</span></span>
* <span data-ttu-id="b63ae-185">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-185">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="b63ae-186">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-186">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="b63ae-187">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-187">Resource</span></span>
* <span data-ttu-id="b63ae-188">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-188">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-189">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-189">Role</span></span>
* <span data-ttu-id="b63ae-190">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-190">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="b63ae-191">Compute</span><span class="sxs-lookup"><span data-stu-id="b63ae-191">Compute</span></span>
* <span data-ttu-id="b63ae-192">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-192">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="b63ae-193">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-193">May 21, 2019</span></span>

<span data-ttu-id="b63ae-194">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="b63ae-194">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-195">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-195">Core</span></span>
* <span data-ttu-id="b63ae-196">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-196">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="b63ae-197">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-197">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="b63ae-198">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-198">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-199">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-199">ACR</span></span>
* <span data-ttu-id="b63ae-200">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-200">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-201">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-201">ACS</span></span>
* <span data-ttu-id="b63ae-202">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-202">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-203">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-203">AppService</span></span>
* <span data-ttu-id="b63ae-204">[非推奨] `functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-204">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="b63ae-205">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-205">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="b63ae-206">[破壊的変更] `--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="b63ae-206">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="b63ae-207">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-207">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="b63ae-208">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-208">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="b63ae-209">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-209">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="b63ae-210">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-210">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="b63ae-211">BotService</span><span class="sxs-lookup"><span data-stu-id="b63ae-211">BotService</span></span>
* <span data-ttu-id="b63ae-212">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-212">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="b63ae-213">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-213">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="b63ae-214">消費</span><span class="sxs-lookup"><span data-stu-id="b63ae-214">Consumption</span></span>
* <span data-ttu-id="b63ae-215">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-215">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="b63ae-216">IoT</span><span class="sxs-lookup"><span data-stu-id="b63ae-216">IoT</span></span>
* <span data-ttu-id="b63ae-217">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-217">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-218">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-218">Network</span></span>
* [破壊的変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="b63ae-220">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-220">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="b63ae-221">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-221">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="b63ae-222">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-222">RDBMS</span></span>
* <span data-ttu-id="b63ae-223">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-223">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="b63ae-224">RBAC</span><span class="sxs-lookup"><span data-stu-id="b63ae-224">RBAC</span></span>
* <span data-ttu-id="b63ae-225">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-225">Added support for mangement group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-226">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-226">Storage</span></span>
* <span data-ttu-id="b63ae-227">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="b63ae-227">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="b63ae-228">Compute</span><span class="sxs-lookup"><span data-stu-id="b63ae-228">Compute</span></span>
* <span data-ttu-id="b63ae-229">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-229">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="b63ae-230">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-230">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="b63ae-231">__メモ__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-231">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="b63ae-232">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-232">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="b63ae-233">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-233">May 6, 2019</span></span>

<span data-ttu-id="b63ae-234">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="b63ae-234">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-235">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-235">ACS</span></span>
* <span data-ttu-id="b63ae-236">[破壊的変更] `--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-236">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="b63ae-237">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-237">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="b63ae-238">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-238">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="b63ae-239">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-239">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-240">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-240">Appservice</span></span>
* <span data-ttu-id="b63ae-241">[非推奨] `functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-241">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="b63ae-242">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-242">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="b63ae-243">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-243">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="b63ae-244">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-244">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="b63ae-245">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-245">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="b63ae-246">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-246">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="b63ae-247">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-247">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="b63ae-248">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-248">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="b63ae-249">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-249">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="b63ae-250">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-250">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="b63ae-251">Batch</span><span class="sxs-lookup"><span data-stu-id="b63ae-251">Batch</span></span>
* <span data-ttu-id="b63ae-252">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-252">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="b63ae-253">Botservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-253">Botservice</span></span>
* <span data-ttu-id="b63ae-254">[破壊的変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="b63ae-254">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="b63ae-255">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-255">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="b63ae-256">[破壊的変更] `--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-256">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="b63ae-257">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="b63ae-257">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="b63ae-258">[破壊的変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-258">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="b63ae-259">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-259">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="b63ae-260">[破壊的変更] `bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-260">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="b63ae-261">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-261">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="b63ae-262">[破壊的変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-262">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="b63ae-263">[破壊的変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-263">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="b63ae-264">[破壊的変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-264">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="b63ae-265">[破壊的変更] `Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-265">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="b63ae-266">[破壊的変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-266">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="b63ae-267">[破壊的変更] `SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-267">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="b63ae-268">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="b63ae-268">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="b63ae-269">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-269">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="b63ae-270">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-270">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="b63ae-271">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-271">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="b63ae-272">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-272">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="b63ae-273">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-273">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="b63ae-274">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-274">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="b63ae-275">構成</span><span class="sxs-lookup"><span data-stu-id="b63ae-275">Configure</span></span>
* <span data-ttu-id="b63ae-276">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-276">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="b63ae-277">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="b63ae-277">Eventhubs</span></span>
* <span data-ttu-id="b63ae-278">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-278">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="b63ae-279">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-279">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-280">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-280">Network</span></span>
* <span data-ttu-id="b63ae-281">[破壊的変更] `vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="b63ae-281">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="b63ae-282">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="b63ae-282">Policy Insights</span></span>
* <span data-ttu-id="b63ae-283">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-283">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-284">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-284">Role</span></span>
* <span data-ttu-id="b63ae-285">[非推奨] `create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-285">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="b63ae-286">Service Bus</span><span class="sxs-lookup"><span data-stu-id="b63ae-286">Service Bus</span></span>
* <span data-ttu-id="b63ae-287">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-287">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="b63ae-288">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-288">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="b63ae-289">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-289">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-290">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-290">SQL</span></span>
* <span data-ttu-id="b63ae-291">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-291">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-292">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-292">VM</span></span>
* <span data-ttu-id="b63ae-293">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-293">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="b63ae-294">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-294">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="b63ae-295">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-295">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="b63ae-296">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-296">Added new `ppg` command group for manging Proximity Placement Groups</span></span>
* <span data-ttu-id="b63ae-297">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-297">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="b63ae-298">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-298">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="b63ae-299">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-299">April 23, 2019</span></span>

<span data-ttu-id="b63ae-300">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="b63ae-300">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-301">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-301">ACS</span></span>
* <span data-ttu-id="b63ae-302">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-302">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="b63ae-303">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-303">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="b63ae-304">AMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-304">AMS</span></span>
* <span data-ttu-id="b63ae-305">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-305">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-306">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-306">AppService</span></span>
* <span data-ttu-id="b63ae-307">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-307">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="b63ae-308">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-308">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="b63ae-309">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-309">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="b63ae-310">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-310">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="b63ae-311">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-311">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="b63ae-312">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-312">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="b63ae-313">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-313">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="b63ae-314">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-314">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="b63ae-315">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-315">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="b63ae-316">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="b63ae-316">Deployment Manager</span></span>
* <span data-ttu-id="b63ae-317">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="b63ae-317">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="b63ae-318">ラボ</span><span class="sxs-lookup"><span data-stu-id="b63ae-318">Lab</span></span>
* <span data-ttu-id="b63ae-319">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-319">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-320">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-320">Network</span></span>
* <span data-ttu-id="b63ae-321">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-321">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-322">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-322">Resource</span></span>
* <span data-ttu-id="b63ae-323">[非推奨] `resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-323">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="b63ae-324">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="b63ae-324">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="b63ae-325">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-325">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="b63ae-326">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-326">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-327">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-327">SQL</span></span>
* <span data-ttu-id="b63ae-328">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-328">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="b63ae-329">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-329">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="b63ae-330">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-330">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="b63ae-331">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-331">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-332">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-332">Storage</span></span>
* <span data-ttu-id="b63ae-333">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-333">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-334">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-334">VM</span></span>
* <span data-ttu-id="b63ae-335">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-335">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="b63ae-336">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-336">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="b63ae-337">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-337">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="b63ae-338">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-338">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-339">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-339">Core</span></span>
* <span data-ttu-id="b63ae-340">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-340">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-341">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-341">ACR</span></span>
* <span data-ttu-id="b63ae-342">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-342">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="b63ae-343">AMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-343">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="b63ae-346">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-346">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="b63ae-347">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-347">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-348">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-348">AppService</span></span>
* <span data-ttu-id="b63ae-349">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-349">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="b63ae-350">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-350">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="b63ae-351">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-351">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="b63ae-352">[破壊的変更] `devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-352">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="b63ae-353">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-353">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="b63ae-354">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-354">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="b63ae-355">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-355">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="b63ae-356">CDN</span><span class="sxs-lookup"><span data-stu-id="b63ae-356">CDN</span></span>
* <span data-ttu-id="b63ae-357">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-357">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="b63ae-358">フィードバック</span><span class="sxs-lookup"><span data-stu-id="b63ae-358">Feedback</span></span>
* <span data-ttu-id="b63ae-359">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-359">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="b63ae-360">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-360">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="b63ae-361">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-361">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-362">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-362">Monitor</span></span>
* <span data-ttu-id="b63ae-363">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-363">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="b63ae-364">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-364">Network</span></span>
* <span data-ttu-id="b63ae-365">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-365">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="b63ae-366">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-366">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="b63ae-367">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-367">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="b63ae-368">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-368">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="b63ae-369">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="b63ae-369">PrivateDNS</span></span>
* <span data-ttu-id="b63ae-370">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-370">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-371">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-371">Resource</span></span>
* <span data-ttu-id="b63ae-372">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-372">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-373">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-373">Role</span></span>
* <span data-ttu-id="b63ae-374">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-374">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="b63ae-375">[破壊的変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-375">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-376">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-376">SQL</span></span>
* <span data-ttu-id="b63ae-377">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-377">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-378">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-378">Storage</span></span>
* <span data-ttu-id="b63ae-379">[破壊的変更] `storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-379">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="b63ae-380">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-380">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="b63ae-381">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-381">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="b63ae-382">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-382">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="b63ae-383">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-383">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="b63ae-384">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-384">Core</span></span>
* <span data-ttu-id="b63ae-385">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-385">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="b63ae-386">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-386">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="b63ae-387">クラウド</span><span class="sxs-lookup"><span data-stu-id="b63ae-387">Cloud</span></span>
* <span data-ttu-id="b63ae-388">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-388">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-389">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-389">ACR</span></span>
* <span data-ttu-id="b63ae-390">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-390">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="b63ae-391">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-391">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="b63ae-392">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-392">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="b63ae-393">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-393">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-394">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-394">AppService</span></span>
* <span data-ttu-id="b63ae-395">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-395">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="b63ae-396">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-396">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="b63ae-397">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="b63ae-397">BOT Service</span></span>
* <span data-ttu-id="b63ae-398">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-398">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="b63ae-399">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-399">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="b63ae-400">[破壊的変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-400">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="b63ae-401">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-401">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="b63ae-402">CDN</span><span class="sxs-lookup"><span data-stu-id="b63ae-402">CDN</span></span>
* <span data-ttu-id="b63ae-403">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-403">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [破壊的変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="b63ae-405">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-405">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="b63ae-406">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-406">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b63ae-407">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="b63ae-407">Cosmosdb</span></span>
* <span data-ttu-id="b63ae-408">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-408">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="b63ae-409">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-409">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="b63ae-410">Interactive</span><span class="sxs-lookup"><span data-stu-id="b63ae-410">Interactive</span></span>
* <span data-ttu-id="b63ae-411">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-411">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-412">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-412">Monitor</span></span>
* <span data-ttu-id="b63ae-413">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-413">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-414">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-414">Network</span></span>
* <span data-ttu-id="b63ae-415">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-415">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="b63ae-416">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b63ae-416">Profile</span></span>
* <span data-ttu-id="b63ae-417">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-417">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="b63ae-418">Postgres</span><span class="sxs-lookup"><span data-stu-id="b63ae-418">Postgres</span></span> 
* <span data-ttu-id="b63ae-419">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-419">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="b63ae-420">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="b63ae-420">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-421">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-421">Resource</span></span>
* <span data-ttu-id="b63ae-422">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-422">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="b63ae-423">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-423">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="b63ae-424">Graph</span><span class="sxs-lookup"><span data-stu-id="b63ae-424">Graph</span></span>
* <span data-ttu-id="b63ae-425">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-425">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="b63ae-426">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-426">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="b63ae-427">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-427">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="b63ae-428">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-428">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="b63ae-429">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-429">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-430">storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-430">storage</span></span>
* <span data-ttu-id="b63ae-431">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-431">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="b63ae-432">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-432">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="b63ae-433">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-433">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="b63ae-434">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-434">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-435">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-435">VM</span></span>
* <span data-ttu-id="b63ae-436">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-436">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="b63ae-437">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-437">March 12, 2019</span></span>

<span data-ttu-id="b63ae-438">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="b63ae-438">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-439">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-439">Core</span></span>

* <span data-ttu-id="b63ae-440">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-440">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-441">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-441">ACR</span></span>

* <span data-ttu-id="b63ae-442">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-442">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-443">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-443">ACS</span></span>

* <span data-ttu-id="b63ae-444">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-444">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="b63ae-445">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-445">AppService</span></span>

* <span data-ttu-id="b63ae-446">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-446">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="b63ae-447">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-447">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="b63ae-448">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-448">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="b63ae-449">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-449">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="b63ae-450">Botservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-450">Botservice</span></span>

* <span data-ttu-id="b63ae-451">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-451">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="b63ae-452">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-452">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="b63ae-453">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-453">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="b63ae-454">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-454">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-455">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-455">Container</span></span>

* <span data-ttu-id="b63ae-456">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-456">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="b63ae-457">EventHub</span><span class="sxs-lookup"><span data-stu-id="b63ae-457">EventHub</span></span>

* <span data-ttu-id="b63ae-458">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-458">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="b63ae-459">Find</span><span class="sxs-lookup"><span data-stu-id="b63ae-459">Find</span></span>

* <span data-ttu-id="b63ae-460">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="b63ae-460">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="b63ae-461">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b63ae-461">HDInsight</span></span>

* <span data-ttu-id="b63ae-462">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-462">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-463">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-463">Network</span></span>

* <span data-ttu-id="b63ae-464">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-464">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="b63ae-465">Rdbms</span><span class="sxs-lookup"><span data-stu-id="b63ae-465">Rdbms</span></span>

* <span data-ttu-id="b63ae-466">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="b63ae-466">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-467">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-467">Role</span></span>

* <span data-ttu-id="b63ae-468">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-468">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="b63ae-469">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-469">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="b63ae-470">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b63ae-470">Service Fabric</span></span>

* <span data-ttu-id="b63ae-471">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-471">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="b63ae-472">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-472">February 26, 2019</span></span>

<span data-ttu-id="b63ae-473">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="b63ae-473">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-474">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-474">Core</span></span>

* <span data-ttu-id="b63ae-475">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-475">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-476">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-476">ACR</span></span>

* <span data-ttu-id="b63ae-477">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-477">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="b63ae-478">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-478">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-479">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-479">ACS</span></span>

* <span data-ttu-id="b63ae-480">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-480">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-481">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-481">AppService</span></span>

* <span data-ttu-id="b63ae-482">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-482">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="b63ae-483">Batch</span><span class="sxs-lookup"><span data-stu-id="b63ae-483">Batch</span></span>
* <span data-ttu-id="b63ae-484">[破壊的変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-484">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="b63ae-485">[破壊的変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-485">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="b63ae-486">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-486">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="b63ae-487">[破壊的変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-487">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="b63ae-488">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-488">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="b63ae-489">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="b63ae-489">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b63ae-490">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b63ae-490">CosmosDB</span></span>

* <span data-ttu-id="b63ae-491">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-491">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="b63ae-492">Kusto</span><span class="sxs-lookup"><span data-stu-id="b63ae-492">Kusto</span></span>

* <span data-ttu-id="b63ae-493">[破壊的変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-493">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-494">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-494">Network</span></span>

* <span data-ttu-id="b63ae-495">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-495">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="b63ae-496">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-496">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="b63ae-497">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-497">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="b63ae-498">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-498">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="b63ae-499">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-499">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="b63ae-500">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-500">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="b63ae-501">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-501">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-502">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-502">Resource</span></span>

* <span data-ttu-id="b63ae-503">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-503">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="b63ae-504">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-504">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="b63ae-505">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-505">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="b63ae-506">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-506">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="b63ae-507">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-507">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-508">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-508">Role</span></span>

* <span data-ttu-id="b63ae-509">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-509">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-510">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-510">VM</span></span>

* <span data-ttu-id="b63ae-511">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-511">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="b63ae-512">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-512">February 12, 2019</span></span>

<span data-ttu-id="b63ae-513">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="b63ae-513">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-514">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-514">Core</span></span>

* <span data-ttu-id="b63ae-515">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-515">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="b63ae-516">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-516">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-517">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-517">ACR</span></span>
* <span data-ttu-id="b63ae-518">[破壊的変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-518">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="b63ae-519">[破壊的変更] `acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-519">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-520">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-520">ACS</span></span>
* <span data-ttu-id="b63ae-521">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-521">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="b63ae-522">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-522">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="b63ae-523">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-523">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="b63ae-524">AMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-524">AMS</span></span>
* <span data-ttu-id="b63ae-525">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-525">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="b63ae-526">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-526">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-527">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-527">Appservice</span></span>
* <span data-ttu-id="b63ae-528">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-528">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="b63ae-529">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-529">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="b63ae-530">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-530">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="b63ae-531">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-531">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="b63ae-532">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-532">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="b63ae-533">Botservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-533">Botservice</span></span>
* <span data-ttu-id="b63ae-534">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-534">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="b63ae-535">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-535">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="b63ae-536">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-536">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="b63ae-537">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-537">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="b63ae-538">[非推奨] `--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-538">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="b63ae-539">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-539">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="b63ae-540">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-540">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="b63ae-541">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-541">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="b63ae-542">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="b63ae-542">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="b63ae-543">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-543">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="b63ae-544">Key Vault</span><span class="sxs-lookup"><span data-stu-id="b63ae-544">Key Vault</span></span>
* <span data-ttu-id="b63ae-545">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-545">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-546">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-546">Monitor</span></span>
* <span data-ttu-id="b63ae-547">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-547">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-548">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-548">Network</span></span>
* <span data-ttu-id="b63ae-549">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-549">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="b63ae-550">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-550">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="b63ae-551">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-551">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="b63ae-552">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-552">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="b63ae-553">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="b63ae-553">Policy Insights</span></span>
* <span data-ttu-id="b63ae-554">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-554">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="b63ae-555">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-555">RDBMS</span></span>
* <span data-ttu-id="b63ae-556">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-556">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="b63ae-557">Redis</span><span class="sxs-lookup"><span data-stu-id="b63ae-557">Redis</span></span>
* <span data-ttu-id="b63ae-558">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-558">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="b63ae-559">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-559">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="b63ae-560">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-560">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="b63ae-561">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-561">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="b63ae-562">[破壊的変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-562">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="b63ae-563">[破壊的変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-563">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="b63ae-564">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-564">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-565">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-565">Role</span></span>
* <span data-ttu-id="b63ae-566">[破壊的変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-566">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="b63ae-567">SQL VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-567">SQL VM</span></span>
* <span data-ttu-id="b63ae-568">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-568">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-569">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-569">VM</span></span>
* <span data-ttu-id="b63ae-570">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-570">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="b63ae-571">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-571">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="b63ae-572">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-572">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="b63ae-573">[破壊的変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-573">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="b63ae-574">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-574">January 31, 2019</span></span>

<span data-ttu-id="b63ae-575">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="b63ae-575">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-576">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-576">Core</span></span>

* <span data-ttu-id="b63ae-577">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="b63ae-577">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="b63ae-578">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-578">January 28, 2019</span></span>

<span data-ttu-id="b63ae-579">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="b63ae-579">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-580">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-580">ACR</span></span>
* <span data-ttu-id="b63ae-581">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-581">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-582">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-582">ACS</span></span>
* <span data-ttu-id="b63ae-583">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-583">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="b63ae-584">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-584">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="b63ae-585">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-585">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="b63ae-586">AMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-586">AMS</span></span>
* <span data-ttu-id="b63ae-587">[破壊的変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-587">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="b63ae-588">[破壊的変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-588">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-589">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-589">Appservice</span></span>
* <span data-ttu-id="b63ae-590">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-590">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="b63ae-591">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-591">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="b63ae-592">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-592">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-593">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-593">Container</span></span>
* <span data-ttu-id="b63ae-594">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-594">Added `container start` command</span></span>
* <span data-ttu-id="b63ae-595">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-595">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="b63ae-596">EventGrid</span><span class="sxs-lookup"><span data-stu-id="b63ae-596">EventGrid</span></span>
* <span data-ttu-id="b63ae-597">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-597">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="b63ae-598">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-598">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="b63ae-599">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-599">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="b63ae-600">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-600">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="b63ae-601">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-601">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="b63ae-602">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b63ae-602">HDInsight</span></span>
* <span data-ttu-id="b63ae-603">[破壊的変更] `hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-603">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="b63ae-604">[破壊的変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-604">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="b63ae-605">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-605">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="b63ae-606">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-606">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="b63ae-607">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-607">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="b63ae-608">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-608">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="b63ae-609">IoT</span><span class="sxs-lookup"><span data-stu-id="b63ae-609">IoT</span></span>
* <span data-ttu-id="b63ae-610">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-610">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="b63ae-611">Kusto</span><span class="sxs-lookup"><span data-stu-id="b63ae-611">Kusto</span></span>
* <span data-ttu-id="b63ae-612">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-612">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-613">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-613">Monitor</span></span>
* <span data-ttu-id="b63ae-614">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-614">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="b63ae-615">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b63ae-615">Profile</span></span>
* <span data-ttu-id="b63ae-616">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-616">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-617">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-617">Network</span></span>
* <span data-ttu-id="b63ae-618">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-618">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="b63ae-619">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-619">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-620">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-620">Resource</span></span>
* <span data-ttu-id="b63ae-621">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-621">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="b63ae-622">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-622">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="b63ae-623">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="b63ae-623">SQL Virtual Machine</span></span>
* <span data-ttu-id="b63ae-624">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-624">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-625">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-625">Storage</span></span>
* <span data-ttu-id="b63ae-626">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-626">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="b63ae-627">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="b63ae-627">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-628">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-628">VM</span></span>
* <span data-ttu-id="b63ae-629">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-629">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="b63ae-630">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-630">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="b63ae-631">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-631">January 15, 2019</span></span>

<span data-ttu-id="b63ae-632">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="b63ae-632">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-633">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-633">ACR</span></span>
* <span data-ttu-id="b63ae-634">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-634">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="b63ae-635">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-635">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="b63ae-636">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-636">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="b63ae-637">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-637">ACS</span></span>
* <span data-ttu-id="b63ae-638">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-638">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-639">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-639">Appservice</span></span>
* <span data-ttu-id="b63ae-640">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-640">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="b63ae-641">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-641">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="b63ae-642">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-642">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="b63ae-643">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-643">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="b63ae-644">Botservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-644">Botservice</span></span>
* <span data-ttu-id="b63ae-645">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-645">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="b63ae-646">構成</span><span class="sxs-lookup"><span data-stu-id="b63ae-646">Configure</span></span>
* <span data-ttu-id="b63ae-647">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-647">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b63ae-648">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b63ae-648">CosmosDB</span></span>
* <span data-ttu-id="b63ae-649">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-649">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="b63ae-650">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b63ae-650">HDInsight</span></span>
* <span data-ttu-id="b63ae-651">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-651">Added commands for managing applications</span></span>
* <span data-ttu-id="b63ae-652">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-652">Added commands for managing script actions</span></span>
* <span data-ttu-id="b63ae-653">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-653">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="b63ae-654">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-654">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="b63ae-655">[破壊的変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-655">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-656">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-656">Network</span></span>
* <span data-ttu-id="b63ae-657">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-657">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="b63ae-658">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-658">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="b63ae-659">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-659">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="b63ae-660">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-660">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-661">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-661">Role</span></span>
* <span data-ttu-id="b63ae-662">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-662">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="b63ae-663">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="b63ae-663">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="b63ae-664">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="b63ae-664">Security</span></span>
* <span data-ttu-id="b63ae-665">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-665">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-666">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-666">Storage</span></span>
* <span data-ttu-id="b63ae-667">[破壊的変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-667">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="b63ae-668">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b63ae-668">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="b63ae-669">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-669">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="b63ae-670">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-670">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="b63ae-671">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-671">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-672">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-672">VM</span></span>
* <span data-ttu-id="b63ae-673">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-673">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="b63ae-674">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-674">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="b63ae-675">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-675">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="b63ae-676">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-676">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="b63ae-677">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-677">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="b63ae-678">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-678">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="b63ae-679">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-679">December 20, 2018</span></span>

<span data-ttu-id="b63ae-680">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="b63ae-680">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="b63ae-681">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-681">Appservice</span></span>
* <span data-ttu-id="b63ae-682">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-682">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="b63ae-683">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-683">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="b63ae-684">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-684">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="b63ae-685">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="b63ae-685">IoTCentral</span></span>
* <span data-ttu-id="b63ae-686">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-686">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-687">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-687">Role</span></span>
* <span data-ttu-id="b63ae-688">[破壊的変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-688">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-689">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-689">SQL</span></span>
* <span data-ttu-id="b63ae-690">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-690">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-691">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-691">VM</span></span>
* <span data-ttu-id="b63ae-692">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-692">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="b63ae-693">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-693">December 18, 2018</span></span>

<span data-ttu-id="b63ae-694">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="b63ae-694">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="b63ae-695">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-695">ACR</span></span>
* <span data-ttu-id="b63ae-696">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-696">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="b63ae-697">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-697">Condensed the table layout for task list</span></span>
* <span data-ttu-id="b63ae-698">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-698">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-699">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-699">ACS</span></span>
* <span data-ttu-id="b63ae-700">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-700">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="b63ae-701">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-701">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="b63ae-702">[非推奨] `az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-702">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="b63ae-703">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="b63ae-703">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="b63ae-704">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-704">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="b63ae-705">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-705">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-706">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-706">Appservice</span></span>
* <span data-ttu-id="b63ae-707">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-707">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="b63ae-708">Botservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-708">Botservice</span></span>
* <span data-ttu-id="b63ae-709">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-709">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="b63ae-710">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-710">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="b63ae-711">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-711">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="b63ae-712">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-712">Reduced Kudu network calls</span></span>
* <span data-ttu-id="b63ae-713">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-713">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="b63ae-714">消費</span><span class="sxs-lookup"><span data-stu-id="b63ae-714">Consumption</span></span>
* <span data-ttu-id="b63ae-715">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-715">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b63ae-716">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b63ae-716">CosmosDB</span></span>
* <span data-ttu-id="b63ae-717">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-717">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="b63ae-718">マップ</span><span class="sxs-lookup"><span data-stu-id="b63ae-718">Maps</span></span>
* <span data-ttu-id="b63ae-719">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-719">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-720">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-720">Network</span></span>
* <span data-ttu-id="b63ae-721">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-721">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="b63ae-722">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-722">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-723">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-723">Resource</span></span>
* <span data-ttu-id="b63ae-724">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-724">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="b63ae-725">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-725">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-726">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-726">Storage</span></span>
*  <span data-ttu-id="b63ae-727">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-727">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-728">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-728">VM</span></span>
* <span data-ttu-id="b63ae-729">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-729">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="b63ae-730">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-730">December 4, 2018</span></span>

<span data-ttu-id="b63ae-731">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="b63ae-731">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="b63ae-732">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-732">Core</span></span>
* <span data-ttu-id="b63ae-733">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-733">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="b63ae-734">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-734">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-735">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-735">Appservice</span></span>
* <span data-ttu-id="b63ae-736">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-736">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="b63ae-737">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-737">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-738">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-738">Network</span></span>
* <span data-ttu-id="b63ae-739">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-739">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-740">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-740">Role</span></span>
* <span data-ttu-id="b63ae-741">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-741">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="b63ae-742">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-742">VM</span></span>
* <span data-ttu-id="b63ae-743">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-743">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="b63ae-744">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-744">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="b63ae-745">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-745">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="b63ae-746">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-746">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="b63ae-747">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-747">November 20, 2018</span></span>

<span data-ttu-id="b63ae-748">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="b63ae-748">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="b63ae-749">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-749">Core</span></span>
* <span data-ttu-id="b63ae-750">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-750">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-751">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-751">ACR</span></span>
* <span data-ttu-id="b63ae-752">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-752">Added context token to task step</span></span>
* <span data-ttu-id="b63ae-753">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-753">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="b63ae-754">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-754">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-755">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-755">Appservice</span></span>
* <span data-ttu-id="b63ae-756">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-756">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="b63ae-757">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-757">Updated the default `node_version`.</span></span> <span data-ttu-id="b63ae-758">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-758">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="b63ae-759">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-759">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="b63ae-760">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-760">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="b63ae-761">IotCentral</span><span class="sxs-lookup"><span data-stu-id="b63ae-761">IotCentral</span></span>
* <span data-ttu-id="b63ae-762">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-762">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="b63ae-763">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b63ae-763">KeyVault</span></span>
* <span data-ttu-id="b63ae-764">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-764">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-765">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-765">Network</span></span>
* <span data-ttu-id="b63ae-766">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-766">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="b63ae-767">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-767">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="b63ae-768">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-768">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="b63ae-769">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-769">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="b63ae-770">Rdbms</span><span class="sxs-lookup"><span data-stu-id="b63ae-770">Rdbms</span></span>
* <span data-ttu-id="b63ae-771">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-771">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="b63ae-772">Rbac</span><span class="sxs-lookup"><span data-stu-id="b63ae-772">Rbac</span></span>
* <span data-ttu-id="b63ae-773">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-773">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="b63ae-774">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-774">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="b63ae-775">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-775">Storage</span></span>
* <span data-ttu-id="b63ae-776">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-776">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="b63ae-777">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-777">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="b63ae-778">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-778">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="b63ae-779">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-779">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-780">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-780">VM</span></span>
* <span data-ttu-id="b63ae-781">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-781">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="b63ae-782">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-782">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="b63ae-783">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="b63ae-783">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="b63ae-784">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-784">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="b63ae-785">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-785">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="b63ae-786">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-786">Added `snapshot wait` command</span></span>
* <span data-ttu-id="b63ae-787">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-787">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="b63ae-788">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-788">November 6, 2018</span></span>

<span data-ttu-id="b63ae-789">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="b63ae-789">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-790">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-790">Core</span></span>
* <span data-ttu-id="b63ae-791">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-791">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-792">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-792">ACR</span></span>
* <span data-ttu-id="b63ae-793">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-793">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="b63ae-794">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-794">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-795">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-795">ACS</span></span>
* <span data-ttu-id="b63ae-796">[破壊的変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-796">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="b63ae-797">Advisor</span><span class="sxs-lookup"><span data-stu-id="b63ae-797">Advisor</span></span>
* <span data-ttu-id="b63ae-798">GA リリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-798">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="b63ae-799">AMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-799">AMS</span></span>
* <span data-ttu-id="b63ae-800">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-800">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="b63ae-801">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-801">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="b63ae-802">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-802">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="b63ae-803">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-803">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="b63ae-804">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-804">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="b63ae-805">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-805">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="b63ae-806">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-806">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="b63ae-807">[破壊的変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="b63ae-807">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="b63ae-808">[破壊的変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-808">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="b63ae-809">[破壊的変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-809">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="b63ae-810">[破壊的変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="b63ae-810">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="b63ae-811">[破壊的変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-811">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="b63ae-812">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="b63ae-812">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="b63ae-813">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="b63ae-813">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="b63ae-814">[破壊的変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-814">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="b63ae-815">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-815">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="b63ae-816">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="b63ae-816">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-817">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-817">AppService</span></span>
* <span data-ttu-id="b63ae-818">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-818">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="b63ae-819">構成</span><span class="sxs-lookup"><span data-stu-id="b63ae-819">Configure</span></span>
* <span data-ttu-id="b63ae-820">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-820">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-821">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-821">Container</span></span>
* <span data-ttu-id="b63ae-822">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-822">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="b63ae-823">EventHub</span><span class="sxs-lookup"><span data-stu-id="b63ae-823">EventHub</span></span>
* <span data-ttu-id="b63ae-824">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-824">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="b63ae-825">Interactive</span><span class="sxs-lookup"><span data-stu-id="b63ae-825">Interactive</span></span>
* <span data-ttu-id="b63ae-826">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="b63ae-826">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-827">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-827">Monitor</span></span>
* <span data-ttu-id="b63ae-828">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-828">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-829">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-829">Network</span></span>
* <span data-ttu-id="b63ae-830">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-830">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="b63ae-831">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-831">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="b63ae-832">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-832">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="b63ae-833">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b63ae-833">Profile</span></span>
* <span data-ttu-id="b63ae-834">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-834">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="b63ae-835">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-835">RDBMS</span></span>
* <span data-ttu-id="b63ae-836">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-836">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-837">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-837">Resource</span></span>
* <span data-ttu-id="b63ae-838">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-838">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-839">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-839">Role</span></span>
* <span data-ttu-id="b63ae-840">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-840">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="b63ae-841">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-841">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="b63ae-842">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-842">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-843">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-843">Storage</span></span>
* <span data-ttu-id="b63ae-844">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="b63ae-844">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-845">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-845">VM</span></span>
* <span data-ttu-id="b63ae-846">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-846">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="b63ae-847">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-847">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="b63ae-848">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-848">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="b63ae-849">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-849">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="b63ae-850">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="b63ae-850">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="b63ae-851">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-851">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="b63ae-852">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-852">October 23, 2018</span></span>

<span data-ttu-id="b63ae-853">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="b63ae-853">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-854">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-854">Core</span></span>
* <span data-ttu-id="b63ae-855">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-855">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="b63ae-856">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-856">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-857">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-857">ACR</span></span>
* <span data-ttu-id="b63ae-858">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-858">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="b63ae-859">CDN</span><span class="sxs-lookup"><span data-stu-id="b63ae-859">CDN</span></span>
* <span data-ttu-id="b63ae-860">[破壊的変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-860">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="b63ae-861">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-861">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-862">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-862">Container</span></span>
* <span data-ttu-id="b63ae-863">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-863">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="b63ae-864">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-864">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="b63ae-865">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-865">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="b63ae-866">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-866">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="b63ae-867">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-867">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="b63ae-868">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-868">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="b63ae-869">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-869">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b63ae-870">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b63ae-870">CosmosDB</span></span>
* <span data-ttu-id="b63ae-871">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-871">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="b63ae-872">Interactive</span><span class="sxs-lookup"><span data-stu-id="b63ae-872">Interactive</span></span>
* <span data-ttu-id="b63ae-873">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-873">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="b63ae-874">IoT Central</span><span class="sxs-lookup"><span data-stu-id="b63ae-874">IoT Central</span></span>
* <span data-ttu-id="b63ae-875">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-875">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="b63ae-876">[破壊的変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="b63ae-876">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-877">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-877">Monitor</span></span>
* <span data-ttu-id="b63ae-878">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="b63ae-878">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="b63ae-879">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-879">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="b63ae-880">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-880">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="b63ae-881">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-881">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="b63ae-882">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-882">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="b63ae-883">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-883">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="b63ae-884">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="b63ae-884">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="b63ae-885">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-885">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="b63ae-886">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-886">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="b63ae-887">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-887">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-888">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-888">Network</span></span>
* <span data-ttu-id="b63ae-889">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-889">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="b63ae-890">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-890">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="b63ae-891">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b63ae-891">ServiceBus</span></span>
* <span data-ttu-id="b63ae-892">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-892">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-893">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-893">SQL</span></span>
* <span data-ttu-id="b63ae-894">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-894">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-895">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-895">Storage</span></span>
* <span data-ttu-id="b63ae-896">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-896">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="b63ae-897">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-897">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-898">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-898">VM</span></span>
* <span data-ttu-id="b63ae-899">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-899">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="b63ae-900">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-900">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="b63ae-901">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-901">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="b63ae-902">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-902">October 16, 2018</span></span>

<span data-ttu-id="b63ae-903">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="b63ae-903">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-904">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-904">VM</span></span>
* <span data-ttu-id="b63ae-905">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-905">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="b63ae-906">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-906">October 9, 2018</span></span>

<span data-ttu-id="b63ae-907">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="b63ae-907">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-908">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-908">Core</span></span>
* <span data-ttu-id="b63ae-909">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-909">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-910">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-910">ACR</span></span>
* <span data-ttu-id="b63ae-911">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-911">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-912">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-912">ACS</span></span>
* <span data-ttu-id="b63ae-913">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="b63ae-913">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="b63ae-914">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-914">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="b63ae-915">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-915">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="b63ae-916">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-916">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-917">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-917">Container</span></span>
* <span data-ttu-id="b63ae-918">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-918">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="b63ae-919">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-919">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="b63ae-920">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="b63ae-920">Event Hub</span></span>
* <span data-ttu-id="b63ae-921">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-921">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="b63ae-922">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-922">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="b63ae-923">Extensions</span><span class="sxs-lookup"><span data-stu-id="b63ae-923">Extensions</span></span>
* <span data-ttu-id="b63ae-924">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-924">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="b63ae-925">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b63ae-925">HDInsight</span></span>
* <span data-ttu-id="b63ae-926">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-926">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="b63ae-927">IoT</span><span class="sxs-lookup"><span data-stu-id="b63ae-927">IoT</span></span>
* <span data-ttu-id="b63ae-928">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-928">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="b63ae-929">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b63ae-929">KeyVault</span></span>
* <span data-ttu-id="b63ae-930">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-930">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-931">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-931">Network</span></span>
* <span data-ttu-id="b63ae-932">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="b63ae-932">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="b63ae-933">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="b63ae-933">See #6052</span></span>
* <span data-ttu-id="b63ae-934">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-934">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="b63ae-935">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="b63ae-935">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="b63ae-936">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-936">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="b63ae-937">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-937">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="b63ae-938">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-938">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="b63ae-939">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-939">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-940">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-940">Role</span></span>
* <span data-ttu-id="b63ae-941">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-941">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="b63ae-942">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-942">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="b63ae-943">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-943">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="b63ae-944">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-944">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="b63ae-945">Service Bus</span><span class="sxs-lookup"><span data-stu-id="b63ae-945">Service Bus</span></span>
* <span data-ttu-id="b63ae-946">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-946">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-947">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-947">VM</span></span>
* <span data-ttu-id="b63ae-948">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-948">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="b63ae-949">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-949">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="b63ae-950">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-950">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="b63ae-951">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-951">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="b63ae-952">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-952">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="b63ae-953">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-953">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="b63ae-954">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-954">September 21, 2018</span></span>

<span data-ttu-id="b63ae-955">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="b63ae-955">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-956">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-956">ACR</span></span>
* <span data-ttu-id="b63ae-957">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-957">Added ACR Task commands</span></span>
* <span data-ttu-id="b63ae-958">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-958">Added quick run command</span></span>
* <span data-ttu-id="b63ae-959">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-959">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="b63ae-960">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-960">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="b63ae-961">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-961">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="b63ae-962">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-962">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-963">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-963">ACS</span></span>
* <span data-ttu-id="b63ae-964">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-964">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="b63ae-965">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-965">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-966">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-966">AppService</span></span>

* <span data-ttu-id="b63ae-967">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-967">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="b63ae-968">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-968">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="b63ae-969">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-969">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="b63ae-970">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-970">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="b63ae-971">Batch</span><span class="sxs-lookup"><span data-stu-id="b63ae-971">Batch</span></span>
* <span data-ttu-id="b63ae-972">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-972">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="b63ae-973">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-973">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="b63ae-974">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-974">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="b63ae-975">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-975">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="b63ae-976">Batch AI</span><span class="sxs-lookup"><span data-stu-id="b63ae-976">Batch AI</span></span> 
* <span data-ttu-id="b63ae-977">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-977">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="b63ae-978">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="b63ae-978">Cognitive Services</span></span>
* <span data-ttu-id="b63ae-979">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-979">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="b63ae-980">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-980">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="b63ae-981">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-981">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="b63ae-982">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-982">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="b63ae-983">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-983">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="b63ae-984">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-984">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-985">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-985">Container</span></span>
* <span data-ttu-id="b63ae-986">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-986">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="b63ae-987">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-987">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="b63ae-988">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-988">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="b63ae-989">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-989">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="b63ae-990">DataLake</span><span class="sxs-lookup"><span data-stu-id="b63ae-990">Datalake</span></span>
* <span data-ttu-id="b63ae-991">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-991">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="b63ae-992">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="b63ae-992">Interactive Shell</span></span>
* <span data-ttu-id="b63ae-993">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-993">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="b63ae-994">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-994">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="b63ae-995">IoT</span><span class="sxs-lookup"><span data-stu-id="b63ae-995">IoT</span></span>
* <span data-ttu-id="b63ae-996">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-996">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="b63ae-997">Key Vault</span><span class="sxs-lookup"><span data-stu-id="b63ae-997">Key Vault</span></span>
* <span data-ttu-id="b63ae-998">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-998">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-999">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-999">Network</span></span>
* <span data-ttu-id="b63ae-1000">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1000">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="b63ae-1001">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1001">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="b63ae-1002">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1002">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="b63ae-1003">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1003">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="b63ae-1004">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1004">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="b63ae-1005">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1005">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="b63ae-1006">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1006">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="b63ae-1007">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1007">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="b63ae-1008">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1008">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="b63ae-1009">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1009">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="b63ae-1010">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1010">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="b63ae-1011">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1011">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="b63ae-1012">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1012">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="b63ae-1013">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1013">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="b63ae-1014">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1014">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="b63ae-1015">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1015">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="b63ae-1016">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1016">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="b63ae-1017">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1017">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="b63ae-1018">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1018">RDBMS</span></span>
* <span data-ttu-id="b63ae-1019">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1019">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="b63ae-1020">予約</span><span class="sxs-lookup"><span data-stu-id="b63ae-1020">Reservation</span></span>
* <span data-ttu-id="b63ae-1021">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1021">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="b63ae-1022">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1022">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="b63ae-1023">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="b63ae-1023">Manage App</span></span>
* <span data-ttu-id="b63ae-1024">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1024">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="b63ae-1025">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1025">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-1026">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-1026">Role</span></span>
* <span data-ttu-id="b63ae-1027">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1027">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="b63ae-1028">SignalR</span><span class="sxs-lookup"><span data-stu-id="b63ae-1028">SignalR</span></span>
* <span data-ttu-id="b63ae-1029">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-1029">First release</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1030">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1030">Storage</span></span>
* <span data-ttu-id="b63ae-1031">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1031">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="b63ae-1032">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1032">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1033">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1033">VM</span></span>
* <span data-ttu-id="b63ae-1034">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="b63ae-1034">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="b63ae-1035">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1035">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="b63ae-1036">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1036">August 28, 2018</span></span>

<span data-ttu-id="b63ae-1037">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="b63ae-1037">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1038">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1038">Core</span></span>

* <span data-ttu-id="b63ae-1039">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1039">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="b63ae-1040">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1040">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-1041">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-1041">ACR</span></span>

* <span data-ttu-id="b63ae-1042">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1042">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="b63ae-1043">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1043">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1044">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1044">ACS</span></span>

* <span data-ttu-id="b63ae-1045">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1045">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="b63ae-1046">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1046">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1047">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-1047">AppService</span></span>

* <span data-ttu-id="b63ae-1048">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1048">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="b63ae-1049">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1049">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="b63ae-1050">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1050">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="b63ae-1051">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b63ae-1051">Backup</span></span>

* <span data-ttu-id="b63ae-1052">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1052">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="b63ae-1053">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="b63ae-1053">Bot Service</span></span>

* <span data-ttu-id="b63ae-1054">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-1054">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="b63ae-1055">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="b63ae-1055">Cognitive Services</span></span>

* <span data-ttu-id="b63ae-1056">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1056">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="b63ae-1057">IoT</span><span class="sxs-lookup"><span data-stu-id="b63ae-1057">IoT</span></span>

* <span data-ttu-id="b63ae-1058">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1058">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-1059">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-1059">Monitor</span></span>

* <span data-ttu-id="b63ae-1060">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1060">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="b63ae-1061">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1061">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1062">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1062">Network</span></span>

* <span data-ttu-id="b63ae-1063">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1063">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-1064">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-1064">Resource</span></span>

* <span data-ttu-id="b63ae-1065">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1065">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1066">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1066">Storage</span></span>

* <span data-ttu-id="b63ae-1067">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1067">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1068">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1068">VM</span></span>

* <span data-ttu-id="b63ae-1069">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1069">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="b63ae-1070">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1070">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="b63ae-1071">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1071">Auguest 14, 2018</span></span>

<span data-ttu-id="b63ae-1072">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="b63ae-1072">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1073">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1073">Core</span></span>

* <span data-ttu-id="b63ae-1074">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1074">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="b63ae-1075">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1075">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="b63ae-1076">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="b63ae-1076">Telemetry</span></span>

* <span data-ttu-id="b63ae-1077">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1077">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-1078">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-1078">ACR</span></span>

* <span data-ttu-id="b63ae-1079">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1079">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="b63ae-1080">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1080">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1081">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1081">ACS</span></span>

* <span data-ttu-id="b63ae-1082">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1082">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="b63ae-1083">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1083">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="b63ae-1084">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1084">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="b63ae-1085">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1085">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="b63ae-1086">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1086">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="b63ae-1087">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-1087">AppService</span></span>

* <span data-ttu-id="b63ae-1088">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1088">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="b63ae-1089">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1089">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="b63ae-1090">BatchAI</span><span class="sxs-lookup"><span data-stu-id="b63ae-1090">BatchAI</span></span>

* <span data-ttu-id="b63ae-1091">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1091">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="b63ae-1092">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-1092">Container</span></span>

* <span data-ttu-id="b63ae-1093">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1093">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="b63ae-1094">IoT</span><span class="sxs-lookup"><span data-stu-id="b63ae-1094">IoT</span></span>

* <span data-ttu-id="b63ae-1095">[破壊的変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1095">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="b63ae-1096">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1096">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="b63ae-1097">Iot Central</span><span class="sxs-lookup"><span data-stu-id="b63ae-1097">Iot Central</span></span>

* <span data-ttu-id="b63ae-1098">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-1098">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="b63ae-1099">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b63ae-1099">KeyVault</span></span>


* <span data-ttu-id="b63ae-1100">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1100">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="b63ae-1101">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1101">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="b63ae-1102">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1102">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="b63ae-1103">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1103">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="b63ae-1104">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1104">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="b63ae-1105">リレー</span><span class="sxs-lookup"><span data-stu-id="b63ae-1105">Relay</span></span>

* <span data-ttu-id="b63ae-1106">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-1106">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-1107">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-1107">Sql</span></span>

* <span data-ttu-id="b63ae-1108">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1108">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1109">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1109">Storage</span></span>

* <span data-ttu-id="b63ae-1110">[破壊的変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-1110">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="b63ae-1111">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1111">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="b63ae-1112">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1112">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="b63ae-1113">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1113">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="b63ae-1114">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1114">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1115">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1115">VM</span></span>

* <span data-ttu-id="b63ae-1116">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1116">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="b63ae-1117">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1117">July 31, 2018</span></span>

<span data-ttu-id="b63ae-1118">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="b63ae-1118">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-1119">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-1119">ACR</span></span>

* <span data-ttu-id="b63ae-1120">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1120">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="b63ae-1121">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1121">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1122">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1122">ACS</span></span>

* <span data-ttu-id="b63ae-1123">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1123">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="b63ae-1124">Batch</span><span class="sxs-lookup"><span data-stu-id="b63ae-1124">Batch</span></span>

* <span data-ttu-id="b63ae-1125">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1125">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-1126">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-1126">Container</span></span>

* <span data-ttu-id="b63ae-1127">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1127">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1128">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1128">Network</span></span>

* <span data-ttu-id="b63ae-1129">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1129">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="b63ae-1130">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-1130">Resource</span></span>

* <span data-ttu-id="b63ae-1131">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1131">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="b63ae-1132">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1132">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-1133">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-1133">Role</span></span>

* <span data-ttu-id="b63ae-1134">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1134">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="b63ae-1135">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1135">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="b63ae-1136">Search</span><span class="sxs-lookup"><span data-stu-id="b63ae-1136">Search</span></span>

* <span data-ttu-id="b63ae-1137">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1137">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="b63ae-1138">Service Bus</span><span class="sxs-lookup"><span data-stu-id="b63ae-1138">Service Bus</span></span>

* <span data-ttu-id="b63ae-1139">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1139">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="b63ae-1140">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1140">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="b63ae-1141">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="b63ae-1141">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="b63ae-1142">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="b63ae-1142">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1143">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1143">Storage</span></span>

* <span data-ttu-id="b63ae-1144">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1144">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="b63ae-1145">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1145">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1146">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1146">VM</span></span>

* <span data-ttu-id="b63ae-1147">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1147">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="b63ae-1148">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1148">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="b63ae-1149">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1149">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="b63ae-1150">[破壊的変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1150">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="b63ae-1151">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1151">July 18, 2018</span></span>

<span data-ttu-id="b63ae-1152">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="b63ae-1152">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1153">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1153">Core</span></span>

* <span data-ttu-id="b63ae-1154">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1154">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="b63ae-1155">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1155">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="b63ae-1156">[破壊的変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1156">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-1157">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-1157">ACR</span></span>

* <span data-ttu-id="b63ae-1158">[破壊的変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1158">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="b63ae-1159">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1159">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="b63ae-1160">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1160">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="b63ae-1161">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1161">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1162">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1162">ACS</span></span>

* <span data-ttu-id="b63ae-1163">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1163">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1164">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-1164">AppService</span></span>

* <span data-ttu-id="b63ae-1165">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1165">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="b63ae-1166">Batch</span><span class="sxs-lookup"><span data-stu-id="b63ae-1166">Batch</span></span>

* <span data-ttu-id="b63ae-1167">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1167">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="b63ae-1168">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1168">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="b63ae-1169">Batch AI</span><span class="sxs-lookup"><span data-stu-id="b63ae-1169">Batch AI</span></span>

* <span data-ttu-id="b63ae-1170">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1170">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-1171">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-1171">Container</span></span>

* <span data-ttu-id="b63ae-1172">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1172">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="b63ae-1173">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1173">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1174">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1174">Network</span></span>

* <span data-ttu-id="b63ae-1175">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1175">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="b63ae-1176">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1176">Added `network nic wait`</span></span>
* <span data-ttu-id="b63ae-1177">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1177">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="b63ae-1178">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1178">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="b63ae-1179">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-1179">Resource</span></span>

* <span data-ttu-id="b63ae-1180">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1180">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="b63ae-1181">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1181">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="b63ae-1182">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1182">Added `deployment wait` command</span></span>
* <span data-ttu-id="b63ae-1183">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1183">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-1184">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-1184">SQL</span></span>

* <span data-ttu-id="b63ae-1185">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1185">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="b63ae-1186">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1186">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="b63ae-1187">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1187">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1188">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1188">Storage</span></span>

* <span data-ttu-id="b63ae-1189">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1189">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1190">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1190">VM</span></span>

* <span data-ttu-id="b63ae-1191">[破壊的変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1191">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="b63ae-1192">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1192">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="b63ae-1193">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1193">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="b63ae-1194">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1194">July 3, 2018</span></span>

<span data-ttu-id="b63ae-1195">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="b63ae-1195">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="b63ae-1196">AKS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1196">AKS</span></span>

* <span data-ttu-id="b63ae-1197">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1197">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="b63ae-1198">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1198">July 3, 2018</span></span>

<span data-ttu-id="b63ae-1199">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="b63ae-1199">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1200">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1200">Core</span></span>

* <span data-ttu-id="b63ae-1201">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1201">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-1202">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-1202">ACR</span></span>

* <span data-ttu-id="b63ae-1203">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1203">Added polling build status</span></span>
* <span data-ttu-id="b63ae-1204">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1204">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="b63ae-1205">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1205">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1206">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1206">ACS</span></span>

* <span data-ttu-id="b63ae-1207">[破壊的変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1207">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="b63ae-1208">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1208">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="b63ae-1209">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1209">Updated options for `aks browse` command.</span></span> <span data-ttu-id="b63ae-1210">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1210">Added `--listen-port` support</span></span>
* <span data-ttu-id="b63ae-1211">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1211">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="b63ae-1212">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1212">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="b63ae-1213">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1213">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1214">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-1214">AppService</span></span>

* <span data-ttu-id="b63ae-1215">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1215">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="b63ae-1216">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1216">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="b63ae-1217">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b63ae-1217">Backup</span></span>

* <span data-ttu-id="b63ae-1218">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1218">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="b63ae-1219">BatchAI</span><span class="sxs-lookup"><span data-stu-id="b63ae-1219">BatchAI</span></span>

* <span data-ttu-id="b63ae-1220">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1220">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="b63ae-1221">クラウド</span><span class="sxs-lookup"><span data-stu-id="b63ae-1221">Cloud</span></span>

* <span data-ttu-id="b63ae-1222">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1222">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-1223">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-1223">Container</span></span>

* <span data-ttu-id="b63ae-1224">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1224">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="b63ae-1225">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1225">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="b63ae-1226">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1226">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="b63ae-1227">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b63ae-1227">Extension</span></span>

* <span data-ttu-id="b63ae-1228">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1228">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1229">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1229">Network</span></span>

* <span data-ttu-id="b63ae-1230">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1230">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="b63ae-1231">Rdbms</span><span class="sxs-lookup"><span data-stu-id="b63ae-1231">Rdbms</span></span>

* <span data-ttu-id="b63ae-1232">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1232">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-1233">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-1233">Resource</span></span>

* <span data-ttu-id="b63ae-1234">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1234">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1235">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1235">VM</span></span>

* <span data-ttu-id="b63ae-1236">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1236">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="b63ae-1237">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1237">June 25, 2018</span></span>

<span data-ttu-id="b63ae-1238">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="b63ae-1238">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="b63ae-1239">CLI</span><span class="sxs-lookup"><span data-stu-id="b63ae-1239">CLI</span></span>

* <span data-ttu-id="b63ae-1240">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1240">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="b63ae-1241">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1241">June 19, 2018</span></span>

<span data-ttu-id="b63ae-1242">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="b63ae-1242">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1243">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1243">Core</span></span>

* <span data-ttu-id="b63ae-1244">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1244">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-1245">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-1245">ACR</span></span>

* <span data-ttu-id="b63ae-1246">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1246">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="b63ae-1247">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1247">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1248">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1248">ACS</span></span>

* <span data-ttu-id="b63ae-1249">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1249">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="b63ae-1250">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1250">Added `--update` support</span></span>
* <span data-ttu-id="b63ae-1251">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1251">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="b63ae-1252">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1252">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="b63ae-1253">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1253">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="b63ae-1254">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1254">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="b63ae-1255">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1255">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="b63ae-1256">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1256">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1257">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-1257">AppService</span></span>

* <span data-ttu-id="b63ae-1258">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1258">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="b63ae-1259">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1259">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="b63ae-1260">Batch</span><span class="sxs-lookup"><span data-stu-id="b63ae-1260">Batch</span></span>

* <span data-ttu-id="b63ae-1261">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1261">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="b63ae-1262">Batch AI</span><span class="sxs-lookup"><span data-stu-id="b63ae-1262">Batch AI</span></span>

* <span data-ttu-id="b63ae-1263">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1263">Added support for workspaces.</span></span> <span data-ttu-id="b63ae-1264">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="b63ae-1264">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="b63ae-1265">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1265">Added support for experiments.</span></span> <span data-ttu-id="b63ae-1266">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="b63ae-1266">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="b63ae-1267">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1267">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="b63ae-1268">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1268">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="b63ae-1269">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1269">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="b63ae-1270">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1270">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="b63ae-1271">[破壊的変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="b63ae-1271">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="b63ae-1272">[破壊的変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="b63ae-1272">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="b63ae-1273">[破壊的変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1273">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="b63ae-1274">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1274">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="b63ae-1275">[破壊的変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1275">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="b63ae-1276">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1276">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="b63ae-1277">[破壊的変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1277">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="b63ae-1278">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1278">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="b63ae-1279">[破壊的変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1279">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="b63ae-1280">[破壊的変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1280">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="b63ae-1281">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1281">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="b63ae-1282">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1282">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="b63ae-1283">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1283">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="b63ae-1284">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1284">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="b63ae-1285">マップ</span><span class="sxs-lookup"><span data-stu-id="b63ae-1285">Maps</span></span>

* <span data-ttu-id="b63ae-1286">[破壊的変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1286">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1287">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1287">Network</span></span>

* <span data-ttu-id="b63ae-1288">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="b63ae-1288">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="b63ae-1289">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1289">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="b63ae-1290">#6502</span><span class="sxs-lookup"><span data-stu-id="b63ae-1290">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="b63ae-1291">Reservations</span><span class="sxs-lookup"><span data-stu-id="b63ae-1291">Reservations</span></span>

* <span data-ttu-id="b63ae-1292">[破壊的変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1292">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="b63ae-1293">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1293">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="b63ae-1294">[破壊的変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1294">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="b63ae-1295">[破壊的変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1295">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="b63ae-1296">[破壊的変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1296">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="b63ae-1297">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1297">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-1298">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-1298">Role</span></span>

* <span data-ttu-id="b63ae-1299">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1299">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-1300">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-1300">SQL</span></span>

* <span data-ttu-id="b63ae-1301">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1301">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1302">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1302">Storage</span></span>

* <span data-ttu-id="b63ae-1303">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1303">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1304">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1304">VM</span></span>

* <span data-ttu-id="b63ae-1305">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1305">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="b63ae-1306">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1306">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="b63ae-1307">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1307">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="b63ae-1308">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1308">June 13, 2018</span></span>

<span data-ttu-id="b63ae-1309">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="b63ae-1309">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1310">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1310">Core</span></span>

* <span data-ttu-id="b63ae-1311">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1311">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="b63ae-1312">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1312">June 13, 2018</span></span>

<span data-ttu-id="b63ae-1313">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="b63ae-1313">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="b63ae-1314">AKS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1314">AKS</span></span>

* <span data-ttu-id="b63ae-1315">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1315">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="b63ae-1316">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1316">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="b63ae-1317">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1317">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="b63ae-1318">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1318">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="b63ae-1319">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1319">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1320">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-1320">AppService</span></span>

* <span data-ttu-id="b63ae-1321">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1321">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="b63ae-1322">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1322">June 5, 2018</span></span>

<span data-ttu-id="b63ae-1323">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="b63ae-1323">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="b63ae-1324">Interactive</span><span class="sxs-lookup"><span data-stu-id="b63ae-1324">Interactive</span></span>

* <span data-ttu-id="b63ae-1325">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1325">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="b63ae-1326">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1326">June 5, 2018</span></span>

<span data-ttu-id="b63ae-1327">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="b63ae-1327">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1328">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1328">Core</span></span>

* <span data-ttu-id="b63ae-1329">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1329">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="b63ae-1330">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1330">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-1331">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-1331">ACR</span></span>

* <span data-ttu-id="b63ae-1332">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1332">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="b63ae-1333">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1333">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="b63ae-1334">AKS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1334">AKS</span></span>

* <span data-ttu-id="b63ae-1335">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1335">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="b63ae-1336">Batch</span><span class="sxs-lookup"><span data-stu-id="b63ae-1336">Batch</span></span>

* <span data-ttu-id="b63ae-1337">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1337">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="b63ae-1338">IoT</span><span class="sxs-lookup"><span data-stu-id="b63ae-1338">IOT</span></span>

* <span data-ttu-id="b63ae-1339">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1339">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1340">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1340">Network</span></span>

* <span data-ttu-id="b63ae-1341">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1341">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="b63ae-1342">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="b63ae-1342">Policy Insights</span></span>

* <span data-ttu-id="b63ae-1343">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-1343">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="b63ae-1344">ARM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1344">ARM</span></span>

* <span data-ttu-id="b63ae-1345">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1345">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-1346">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-1346">SQL</span></span>

* <span data-ttu-id="b63ae-1347">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1347">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="b63ae-1348">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1348">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="b63ae-1349">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1349">Storage</span></span>

* <span data-ttu-id="b63ae-1350">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1350">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1351">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1351">VM</span></span>

* <span data-ttu-id="b63ae-1352">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1352">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="b63ae-1353">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1353">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="b63ae-1354">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1354">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="b63ae-1355">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1355">May 22, 2018</span></span>

<span data-ttu-id="b63ae-1356">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="b63ae-1356">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1357">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1357">Core</span></span>

* <span data-ttu-id="b63ae-1358">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1358">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1359">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1359">ACS</span></span>

* <span data-ttu-id="b63ae-1360">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1360">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="b63ae-1361">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1361">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1362">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-1362">AppService</span></span>

* <span data-ttu-id="b63ae-1363">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1363">Improved generic update commands</span></span>
* <span data-ttu-id="b63ae-1364">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1364">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-1365">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-1365">Container</span></span>

* <span data-ttu-id="b63ae-1366">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1366">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="b63ae-1367">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1367">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="b63ae-1368">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b63ae-1368">Extension</span></span>

* <span data-ttu-id="b63ae-1369">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1369">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="b63ae-1370">Interactive</span><span class="sxs-lookup"><span data-stu-id="b63ae-1370">Interactive</span></span>

* <span data-ttu-id="b63ae-1371">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1371">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="b63ae-1372">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1372">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="b63ae-1373">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b63ae-1373">KeyVault</span></span>

* <span data-ttu-id="b63ae-1374">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1374">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1375">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1375">Network</span></span>

* <span data-ttu-id="b63ae-1376">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1376">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="b63ae-1377">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1377">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-1378">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-1378">SQL</span></span>

* <span data-ttu-id="b63ae-1379">[破壊的変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1379">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="b63ae-1380">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1380">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="b63ae-1381">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1381">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="b63ae-1382">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1382">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="b63ae-1383">[破壊的変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1383">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="b63ae-1384">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="b63ae-1384">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="b63ae-1385">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1385">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="b63ae-1386">`edition`</span><span class="sxs-lookup"><span data-stu-id="b63ae-1386">`edition`.</span></span> <span data-ttu-id="b63ae-1387">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1387">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="b63ae-1388">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="b63ae-1388">`elasticPoolName`.</span></span> <span data-ttu-id="b63ae-1389">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1389">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="b63ae-1390">[破壊的変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1390">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="b63ae-1391">`edition`</span><span class="sxs-lookup"><span data-stu-id="b63ae-1391">`edition`.</span></span> <span data-ttu-id="b63ae-1392">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1392">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="b63ae-1393">`dtu`</span><span class="sxs-lookup"><span data-stu-id="b63ae-1393">`dtu`.</span></span> <span data-ttu-id="b63ae-1394">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1394">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="b63ae-1395">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="b63ae-1395">`databaseDtuMin`.</span></span> <span data-ttu-id="b63ae-1396">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1396">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="b63ae-1397">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="b63ae-1397">`databaseDtuMax`.</span></span> <span data-ttu-id="b63ae-1398">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1398">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="b63ae-1399">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1399">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="b63ae-1400">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1400">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1401">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1401">Storage</span></span>

* <span data-ttu-id="b63ae-1402">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1402">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="b63ae-1403">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1403">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1404">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1404">VM</span></span>

* <span data-ttu-id="b63ae-1405">[破壊的変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1405">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="b63ae-1406">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="b63ae-1406">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="b63ae-1407">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1407">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="b63ae-1408">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1408">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="b63ae-1409">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1409">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="b63ae-1410">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1410">May 7, 2018</span></span>

<span data-ttu-id="b63ae-1411">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="b63ae-1411">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1412">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1412">Core</span></span>

* <span data-ttu-id="b63ae-1413">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1413">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="b63ae-1414">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1414">Added limited support for positional arguments</span></span>
* <span data-ttu-id="b63ae-1415">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1415">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="b63ae-1416">#5591</span><span class="sxs-lookup"><span data-stu-id="b63ae-1416">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="b63ae-1417">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1417">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="b63ae-1418">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="b63ae-1418">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="b63ae-1419">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1419">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="b63ae-1420">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1420">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="b63ae-1421">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1421">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-1422">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-1422">ACR</span></span>

* <span data-ttu-id="b63ae-1423">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1423">Added ACR Build commands</span></span>
* <span data-ttu-id="b63ae-1424">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1424">Improved resource not found error messages</span></span>
* <span data-ttu-id="b63ae-1425">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1425">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="b63ae-1426">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1426">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="b63ae-1427">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1427">Improved repository commands error messages</span></span>
* <span data-ttu-id="b63ae-1428">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1428">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1429">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1429">ACS</span></span>

* <span data-ttu-id="b63ae-1430">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1430">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="b63ae-1431">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1431">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="b63ae-1432">AMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1432">AMS</span></span>

* <span data-ttu-id="b63ae-1433">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="b63ae-1433">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1434">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-1434">Appservice</span></span>

* <span data-ttu-id="b63ae-1435">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1435">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="b63ae-1436">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1436">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="b63ae-1437">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1437">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="b63ae-1438">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1438">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="b63ae-1439">Batch AI</span><span class="sxs-lookup"><span data-stu-id="b63ae-1439">Batch AI</span></span>

* <span data-ttu-id="b63ae-1440">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1440">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="b63ae-1441">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="b63ae-1441">Cognitive Services</span></span>

* <span data-ttu-id="b63ae-1442">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1442">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="b63ae-1443">消費</span><span class="sxs-lookup"><span data-stu-id="b63ae-1443">Consumption</span></span>

* <span data-ttu-id="b63ae-1444">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1444">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-1445">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-1445">Container</span></span>

* <span data-ttu-id="b63ae-1446">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1446">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="b63ae-1447">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b63ae-1447">Cosmos DB</span></span>

* <span data-ttu-id="b63ae-1448">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1448">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="b63ae-1449">DMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1449">DMS</span></span>

* <span data-ttu-id="b63ae-1450">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1450">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="b63ae-1451">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b63ae-1451">Extension</span></span>

* <span data-ttu-id="b63ae-1452">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1452">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="b63ae-1453">Interactive</span><span class="sxs-lookup"><span data-stu-id="b63ae-1453">Interactive</span></span>

* <span data-ttu-id="b63ae-1454">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1454">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="b63ae-1455">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1455">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="b63ae-1456">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1456">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="b63ae-1457">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1457">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="b63ae-1458">ラボ</span><span class="sxs-lookup"><span data-stu-id="b63ae-1458">Lab</span></span>

* <span data-ttu-id="b63ae-1459">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1459">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1460">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1460">Network</span></span>

* <span data-ttu-id="b63ae-1461">[破壊的変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1461">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="b63ae-1462">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b63ae-1462">Profile</span></span>

* <span data-ttu-id="b63ae-1463">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1463">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="b63ae-1464">[破壊的変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1464">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="b63ae-1465">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1465">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="b63ae-1466">Redis</span><span class="sxs-lookup"><span data-stu-id="b63ae-1466">Redis</span></span>

* <span data-ttu-id="b63ae-1467">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1467">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="b63ae-1468">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1468">Deprecated `redis list-all`.</span></span> <span data-ttu-id="b63ae-1469">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1469">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="b63ae-1470">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1470">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="b63ae-1471">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1471">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-1472">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-1472">Role</span></span>

* <span data-ttu-id="b63ae-1473">[破壊的変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1473">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1474">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1474">Storage</span></span>

* <span data-ttu-id="b63ae-1475">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="b63ae-1475">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="b63ae-1476">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1476">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="b63ae-1477">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="b63ae-1477">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="b63ae-1478">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="b63ae-1478">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="b63ae-1479">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1479">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1480">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1480">VM</span></span>

* <span data-ttu-id="b63ae-1481">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1481">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="b63ae-1482">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1482">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="b63ae-1483">[破壊的変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="b63ae-1483">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="b63ae-1484">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1484">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="b63ae-1485">[破壊的変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1485">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="b63ae-1486">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1486">Added write accelerator support</span></span>
* <span data-ttu-id="b63ae-1487">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1487">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="b63ae-1488">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1488">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="b63ae-1489">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1489">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="b63ae-1490">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1490">April 10, 2018</span></span>

<span data-ttu-id="b63ae-1491">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="b63ae-1491">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-1492">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-1492">ACR</span></span>

* <span data-ttu-id="b63ae-1493">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1493">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1494">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1494">ACS</span></span>

* <span data-ttu-id="b63ae-1495">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1495">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1496">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-1496">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="b63ae-1498">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1498">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="b63ae-1499">BatchAI</span><span class="sxs-lookup"><span data-stu-id="b63ae-1499">BatchAI</span></span>

* <span data-ttu-id="b63ae-1500">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1500">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="b63ae-1501">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="b63ae-1501">Job level mounting</span></span>
  - <span data-ttu-id="b63ae-1502">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="b63ae-1502">Environment variables with secret values</span></span>
  - <span data-ttu-id="b63ae-1503">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="b63ae-1503">Performance counters settings</span></span>
  - <span data-ttu-id="b63ae-1504">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="b63ae-1504">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="b63ae-1505">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="b63ae-1505">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="b63ae-1506">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="b63ae-1506">Usage and limits reporting</span></span>
  - <span data-ttu-id="b63ae-1507">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="b63ae-1507">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="b63ae-1508">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="b63ae-1508">Support for custom images</span></span>
  - <span data-ttu-id="b63ae-1509">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1509">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="b63ae-1510">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-1510">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="b63ae-1511">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1511">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="b63ae-1512">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="b63ae-1512">National clouds are supported</span></span>
* <span data-ttu-id="b63ae-1513">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1513">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="b63ae-1514">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1514">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="b63ae-1515">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1515">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="b63ae-1516">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1516">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="b63ae-1517">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="b63ae-1517">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="b63ae-1518">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="b63ae-1518">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="b63ae-1519">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1519">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="b63ae-1520">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1520">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="b63ae-1521">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="b63ae-1521">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="b63ae-1522">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1522">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="b63ae-1523">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1523">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="b63ae-1524">[破壊的変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1524">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="b63ae-1525">[破壊的変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1525">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="b63ae-1526">課金</span><span class="sxs-lookup"><span data-stu-id="b63ae-1526">Billing</span></span>

* <span data-ttu-id="b63ae-1527">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1527">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="b63ae-1528">消費</span><span class="sxs-lookup"><span data-stu-id="b63ae-1528">Consumption</span></span>

* <span data-ttu-id="b63ae-1529">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1529">Added `marketplace` commands</span></span>
* <span data-ttu-id="b63ae-1530">[破壊的変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1530">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="b63ae-1531">[破壊的変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1531">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="b63ae-1532">[破壊的変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1532">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="b63ae-1533">[破壊的変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1533">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="b63ae-1534">[破壊的変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1534">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-1535">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-1535">Container</span></span>

* <span data-ttu-id="b63ae-1536">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1536">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="b63ae-1537">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1537">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="b63ae-1538">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b63ae-1538">Extension</span></span>

* <span data-ttu-id="b63ae-1539">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1539">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="b63ae-1540">Interactive</span><span class="sxs-lookup"><span data-stu-id="b63ae-1540">Interactive</span></span>

* <span data-ttu-id="b63ae-1541">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1541">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="b63ae-1542">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1542">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="b63ae-1543">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1543">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1544">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1544">Network</span></span>

* <span data-ttu-id="b63ae-1545">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1545">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="b63ae-1546">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1546">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="b63ae-1547">#4910</span><span class="sxs-lookup"><span data-stu-id="b63ae-1547">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="b63ae-1548">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1548">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="b63ae-1549">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1549">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="b63ae-1550">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1550">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="b63ae-1551">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1551">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="b63ae-1552">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1552">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="b63ae-1553">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b63ae-1553">Profile</span></span>

* <span data-ttu-id="b63ae-1554">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1554">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="b63ae-1555">[破壊的変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1555">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="b63ae-1556">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1556">RDBMS</span></span>

* <span data-ttu-id="b63ae-1557">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1557">Added `georestore` command</span></span>
* <span data-ttu-id="b63ae-1558">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1558">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-1559">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-1559">Resource</span></span>

* <span data-ttu-id="b63ae-1560">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1560">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="b63ae-1561">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1561">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-1562">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-1562">SQL</span></span>

* <span data-ttu-id="b63ae-1563">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1563">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1564">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1564">Storage</span></span>

* <span data-ttu-id="b63ae-1565">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1565">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1566">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1566">VM</span></span>

* <span data-ttu-id="b63ae-1567">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1567">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="b63ae-1568">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1568">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="b63ae-1570">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1570">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="b63ae-1571">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1571">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="b63ae-1572">#5718</span><span class="sxs-lookup"><span data-stu-id="b63ae-1572">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="b63ae-1573">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1573">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="b63ae-1574">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1574">March 27, 2018</span></span>

<span data-ttu-id="b63ae-1575">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="b63ae-1575">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1576">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1576">Core</span></span>

* <span data-ttu-id="b63ae-1577">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1577">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1578">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1578">ACS</span></span>

* <span data-ttu-id="b63ae-1579">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1579">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1580">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-1580">Appservice</span></span>

* <span data-ttu-id="b63ae-1581">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1581">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="b63ae-1582">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1582">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="b63ae-1583">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b63ae-1583">Backup</span></span>

* <span data-ttu-id="b63ae-1584">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1584">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="b63ae-1585">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="b63ae-1585">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="b63ae-1586">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1586">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="b63ae-1587">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1587">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-1588">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-1588">Container</span></span>

* <span data-ttu-id="b63ae-1589">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1589">Added `container exec` command.</span></span> <span data-ttu-id="b63ae-1590">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1590">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="b63ae-1591">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-1591">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="b63ae-1592">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b63ae-1592">Extension</span></span>

* <span data-ttu-id="b63ae-1593">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1593">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="b63ae-1594">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1594">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="b63ae-1595">[破壊的変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1595">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="b63ae-1596">Interactive</span><span class="sxs-lookup"><span data-stu-id="b63ae-1596">Interactive</span></span>

* <span data-ttu-id="b63ae-1597">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1597">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="b63ae-1598">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1598">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="b63ae-1599">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1599">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="b63ae-1600">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1600">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="b63ae-1601">ラボ</span><span class="sxs-lookup"><span data-stu-id="b63ae-1601">Lab</span></span>

* <span data-ttu-id="b63ae-1602">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1602">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-1603">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-1603">Monitor</span></span>

* <span data-ttu-id="b63ae-1604">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="b63ae-1604">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="b63ae-1605">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="b63ae-1605">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="b63ae-1606">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="b63ae-1606">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1607">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1607">Network</span></span>

* <span data-ttu-id="b63ae-1608">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1608">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="b63ae-1609">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b63ae-1609">Profile</span></span>

* <span data-ttu-id="b63ae-1610">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1610">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="b63ae-1611">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1611">RDBMS</span></span>

* <span data-ttu-id="b63ae-1612">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1612">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-1613">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-1613">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="b63ae-1615">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-1615">Role</span></span>

* <span data-ttu-id="b63ae-1616">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1616">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="b63ae-1617">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1617">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="b63ae-1618">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1618">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="b63ae-1619">[破壊的変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1619">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="b63ae-1620">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1620">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1621">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1621">Storage</span></span>

* <span data-ttu-id="b63ae-1622">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1622">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="b63ae-1623">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="b63ae-1623">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1624">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1624">VM</span></span>

* <span data-ttu-id="b63ae-1625">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1625">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="b63ae-1626">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1626">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="b63ae-1627">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1627">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="b63ae-1628">[破壊的変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1628">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="b63ae-1629">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1629">March 13, 2018</span></span>

<span data-ttu-id="b63ae-1630">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="b63ae-1630">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-1631">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-1631">ACR</span></span>

* <span data-ttu-id="b63ae-1632">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1632">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="b63ae-1633">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1633">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="b63ae-1634">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1634">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1635">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1635">ACS</span></span>

* <span data-ttu-id="b63ae-1636">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1636">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="b63ae-1637">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1637">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="b63ae-1638">Advisor</span><span class="sxs-lookup"><span data-stu-id="b63ae-1638">Advisor</span></span>

* <span data-ttu-id="b63ae-1639">[破壊的変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1639">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="b63ae-1640">[破壊的変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1640">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="b63ae-1641">[破壊的変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1641">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="b63ae-1642">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1642">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="b63ae-1643">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1643">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1644">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-1644">Appservice</span></span>

* <span data-ttu-id="b63ae-1645">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1645">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="b63ae-1646">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1646">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="b63ae-1647">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="b63ae-1647">Eventhubs</span></span>

* <span data-ttu-id="b63ae-1648">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-1648">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="b63ae-1649">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b63ae-1649">Extension</span></span>

* <span data-ttu-id="b63ae-1650">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1650">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="b63ae-1651">Interactive</span><span class="sxs-lookup"><span data-stu-id="b63ae-1651">Interactive</span></span>

* <span data-ttu-id="b63ae-1652">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-1652">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="b63ae-1653">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="b63ae-1653">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="b63ae-1654">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="b63ae-1654">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="b63ae-1655">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1655">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-1656">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-1656">Monitor</span></span>

* <span data-ttu-id="b63ae-1657">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1657">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="b63ae-1658">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1658">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="b63ae-1659">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1659">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="b63ae-1660">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1660">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1661">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1661">Network</span></span>

* <span data-ttu-id="b63ae-1662">[破壊的変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1662">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="b63ae-1663">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1663">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="b63ae-1664">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1664">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="b63ae-1665">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1665">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="b63ae-1666">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b63ae-1666">Profile</span></span>

* <span data-ttu-id="b63ae-1667">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1667">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="b63ae-1668">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1668">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="b63ae-1669">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1669">RDBMS</span></span>

* <span data-ttu-id="b63ae-1670">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1670">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="b63ae-1671">Service Bus</span><span class="sxs-lookup"><span data-stu-id="b63ae-1671">Service Bus</span></span>

* <span data-ttu-id="b63ae-1672">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-1672">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1673">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1673">Storage</span></span>

* <span data-ttu-id="b63ae-1674">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1674">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="b63ae-1675">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1675">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1676">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1676">VM</span></span>

* <span data-ttu-id="b63ae-1677">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1677">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="b63ae-1678">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1678">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="b63ae-1679">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1679">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="b63ae-1680">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1680">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="b63ae-1681">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1681">February 27, 2018</span></span>

<span data-ttu-id="b63ae-1682">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="b63ae-1682">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1683">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1683">Core</span></span>

* <span data-ttu-id="b63ae-1684">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="b63ae-1684">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="b63ae-1685">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1685">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="b63ae-1686">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1686">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1687">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1687">ACS</span></span>

* <span data-ttu-id="b63ae-1688">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1688">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="b63ae-1689">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="b63ae-1689">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="b63ae-1690">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1690">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="b63ae-1691">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1691">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1692">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-1692">Appservice</span></span>

* <span data-ttu-id="b63ae-1693">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="b63ae-1693">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="b63ae-1694">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="b63ae-1694">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="b63ae-1695">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="b63ae-1695">Cognitive Services</span></span>

* <span data-ttu-id="b63ae-1696">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1696">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="b63ae-1697">消費</span><span class="sxs-lookup"><span data-stu-id="b63ae-1697">Consumption</span></span>

* <span data-ttu-id="b63ae-1698">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1698">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="b63ae-1699">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1699">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-1700">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-1700">Container</span></span>

* <span data-ttu-id="b63ae-1701">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1701">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1702">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1702">Network</span></span>

* <span data-ttu-id="b63ae-1703">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="b63ae-1703">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-1704">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-1704">Resource</span></span>

* <span data-ttu-id="b63ae-1705">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1705">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-1706">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-1706">Role</span></span>

* <span data-ttu-id="b63ae-1707">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1707">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-1708">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-1708">SQL</span></span>

* <span data-ttu-id="b63ae-1709">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1709">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1710">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1710">Storage</span></span>

* <span data-ttu-id="b63ae-1711">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1711">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1712">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1712">VM</span></span>

* <span data-ttu-id="b63ae-1713">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1713">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="b63ae-1714">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1714">February 13, 2018</span></span>

<span data-ttu-id="b63ae-1715">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="b63ae-1715">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1716">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1716">Core</span></span>

* <span data-ttu-id="b63ae-1717">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1717">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1718">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1718">ACS</span></span>

* <span data-ttu-id="b63ae-1719">[破壊的変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1719">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="b63ae-1720">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1720">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="b63ae-1721">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1721">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="b63ae-1722">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1722">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="b63ae-1723">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1723">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="b63ae-1724">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1724">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="b63ae-1725">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1725">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="b63ae-1726">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="b63ae-1726">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1727">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-1727">Appservice</span></span>

* <span data-ttu-id="b63ae-1728">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1728">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="b63ae-1729">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1729">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="b63ae-1730">CDN</span><span class="sxs-lookup"><span data-stu-id="b63ae-1730">CDN</span></span>

* <span data-ttu-id="b63ae-1731">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1731">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-1732">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-1732">Container</span></span>

* <span data-ttu-id="b63ae-1733">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1733">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="b63ae-1734">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1734">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b63ae-1735">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b63ae-1735">CosmosDB</span></span>

* <span data-ttu-id="b63ae-1736">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1736">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="b63ae-1737">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b63ae-1737">Extension</span></span>

* <span data-ttu-id="b63ae-1738">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1738">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="b63ae-1739">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1739">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="b63ae-1740">フィードバック</span><span class="sxs-lookup"><span data-stu-id="b63ae-1740">Feedback</span></span>

* <span data-ttu-id="b63ae-1741">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1741">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="b63ae-1742">Interactive</span><span class="sxs-lookup"><span data-stu-id="b63ae-1742">Interactive</span></span>

* <span data-ttu-id="b63ae-1743">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1743">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="b63ae-1744">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1744">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="b63ae-1745">IoT</span><span class="sxs-lookup"><span data-stu-id="b63ae-1745">IoT</span></span>

* <span data-ttu-id="b63ae-1746">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1746">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="b63ae-1747">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1747">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="b63ae-1748">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1748">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="b63ae-1749">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1749">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-1750">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-1750">Monitor</span></span>

* <span data-ttu-id="b63ae-1751">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1751">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1752">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1752">Network</span></span>

* <span data-ttu-id="b63ae-1753">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1753">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="b63ae-1754">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b63ae-1754">Profile</span></span>

* <span data-ttu-id="b63ae-1755">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1755">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-1756">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-1756">Resource</span></span>

* <span data-ttu-id="b63ae-1757">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1757">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-1758">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-1758">Role</span></span>

* <span data-ttu-id="b63ae-1759">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1759">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-1760">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-1760">SQL</span></span>

* <span data-ttu-id="b63ae-1761">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1761">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="b63ae-1762">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1762">Added `sql db rename`</span></span>
* <span data-ttu-id="b63ae-1763">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1763">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1764">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1764">Storage</span></span>

* <span data-ttu-id="b63ae-1765">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1765">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1766">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1766">VM</span></span>

* <span data-ttu-id="b63ae-1767">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1767">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="b63ae-1768">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1768">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="b63ae-1769">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="b63ae-1769">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="b63ae-1770">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1770">January 31, 2018</span></span>

<span data-ttu-id="b63ae-1771">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="b63ae-1771">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1772">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1772">Core</span></span>

* <span data-ttu-id="b63ae-1773">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1773">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="b63ae-1774">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1774">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="b63ae-1775">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1775">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="b63ae-1776">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1776">Use `--verbose` to see</span></span>
* <span data-ttu-id="b63ae-1777">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="b63ae-1777">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1778">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1778">ACS</span></span>

* <span data-ttu-id="b63ae-1779">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1779">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="b63ae-1780">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1780">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1781">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-1781">Appservice</span></span>

* <span data-ttu-id="b63ae-1782">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="b63ae-1782">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="b63ae-1783">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1783">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="b63ae-1784">CDN</span><span class="sxs-lookup"><span data-stu-id="b63ae-1784">CDN</span></span>

* <span data-ttu-id="b63ae-1785">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1785">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b63ae-1786">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b63ae-1786">CosmosDB</span></span>

* <span data-ttu-id="b63ae-1787">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1787">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="b63ae-1788">Interactive</span><span class="sxs-lookup"><span data-stu-id="b63ae-1788">Interactive</span></span>

* <span data-ttu-id="b63ae-1789">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1789">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1790">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1790">Network</span></span>

* <span data-ttu-id="b63ae-1791">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1791">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="b63ae-1792">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1792">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="b63ae-1793">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1793">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="b63ae-1794">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1794">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="b63ae-1795">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1795">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="b63ae-1796">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1796">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="b63ae-1797">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1797">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="b63ae-1798">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1798">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="b63ae-1799">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1799">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="b63ae-1800">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1800">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="b63ae-1801">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b63ae-1801">Profile</span></span>

* <span data-ttu-id="b63ae-1802">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1802">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-1803">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-1803">Resource</span></span>

* <span data-ttu-id="b63ae-1804">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1804">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1805">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1805">Storage</span></span>

* <span data-ttu-id="b63ae-1806">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1806">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="b63ae-1807">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1807">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="b63ae-1808">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1808">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="b63ae-1809">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1809">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="b63ae-1810">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1810">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1811">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1811">VM</span></span>

* <span data-ttu-id="b63ae-1812">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1812">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="b63ae-1813">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1813">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="b63ae-1814">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1814">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="b63ae-1815">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1815">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="b63ae-1816">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1816">January 17, 2018</span></span>

<span data-ttu-id="b63ae-1817">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="b63ae-1817">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-1818">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-1818">ACR</span></span>

* <span data-ttu-id="b63ae-1819">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1819">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="b63ae-1820">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1820">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1821">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1821">ACS</span></span>

* <span data-ttu-id="b63ae-1822">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1822">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="b63ae-1823">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1823">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1824">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-1824">Appservice</span></span>

* <span data-ttu-id="b63ae-1825">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1825">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="b63ae-1826">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1826">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="b63ae-1827">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1827">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="b63ae-1828">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b63ae-1828">Backup</span></span>

* <span data-ttu-id="b63ae-1829">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1829">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="b63ae-1830">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1830">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="b63ae-1831">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1831">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="b63ae-1832">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1832">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="b63ae-1833">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1833">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="b63ae-1834">Batch</span><span class="sxs-lookup"><span data-stu-id="b63ae-1834">Batch</span></span>

* <span data-ttu-id="b63ae-1835">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1835">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="b63ae-1836">クラウド</span><span class="sxs-lookup"><span data-stu-id="b63ae-1836">Cloud</span></span>

* <span data-ttu-id="b63ae-1837">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1837">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="b63ae-1838">消費</span><span class="sxs-lookup"><span data-stu-id="b63ae-1838">Consumption</span></span>

* <span data-ttu-id="b63ae-1839">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1839">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="b63ae-1840">Event Grid</span><span class="sxs-lookup"><span data-stu-id="b63ae-1840">Event Grid</span></span>

* <span data-ttu-id="b63ae-1841">[破壊的変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1841">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="b63ae-1842">[破壊的変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1842">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="b63ae-1843">[破壊的変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1843">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="b63ae-1844">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b63ae-1844">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="b63ae-1845">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1845">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="b63ae-1846">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1846">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="b63ae-1847">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1847">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="b63ae-1848">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1848">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="b63ae-1849">Interactive</span><span class="sxs-lookup"><span data-stu-id="b63ae-1849">Interactive</span></span>

* <span data-ttu-id="b63ae-1850">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1850">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="b63ae-1851">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1851">Fixed errors on startup</span></span>
* <span data-ttu-id="b63ae-1852">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1852">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="b63ae-1853">IoT</span><span class="sxs-lookup"><span data-stu-id="b63ae-1853">IoT</span></span>

* <span data-ttu-id="b63ae-1854">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1854">Added support for device provisioning service</span></span>
* <span data-ttu-id="b63ae-1855">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1855">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="b63ae-1856">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1856">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-1857">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-1857">Monitor</span></span>

* <span data-ttu-id="b63ae-1858">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1858">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="b63ae-1859">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1859">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="b63ae-1860">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1860">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1861">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1861">Network</span></span>

* <span data-ttu-id="b63ae-1862">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1862">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="b63ae-1863">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1863">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="b63ae-1864">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b63ae-1864">Profile</span></span>

* <span data-ttu-id="b63ae-1865">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1865">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-1866">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-1866">Role</span></span>

* <span data-ttu-id="b63ae-1867">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1867">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="b63ae-1868">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b63ae-1868">Service Fabric</span></span>

* <span data-ttu-id="b63ae-1869">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1869">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="b63ae-1870">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1870">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1871">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1871">VM</span></span>

* <span data-ttu-id="b63ae-1872">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="b63ae-1872">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="b63ae-1873">[破壊的変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1873">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="b63ae-1874">[破壊的変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1874">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="b63ae-1875">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1875">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="b63ae-1876">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1876">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="b63ae-1877">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1877">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="b63ae-1878">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1878">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="b63ae-1879">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1879">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="b63ae-1880">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1880">December 19, 2017</span></span>

<span data-ttu-id="b63ae-1881">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="b63ae-1881">Version 2.0.23</span></span>

* <span data-ttu-id="b63ae-1882">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1882">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-1883">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-1883">Container</span></span>

* <span data-ttu-id="b63ae-1884">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1884">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1885">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1885">Network</span></span>

* <span data-ttu-id="b63ae-1886">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1886">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="b63ae-1887">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1887">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1888">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1888">Storage</span></span>

* <span data-ttu-id="b63ae-1889">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1889">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1890">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1890">VM</span></span>

* <span data-ttu-id="b63ae-1891">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1891">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="b63ae-1892">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1892">December 5, 2017</span></span>

<span data-ttu-id="b63ae-1893">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="b63ae-1893">Version 2.0.22</span></span>

* <span data-ttu-id="b63ae-1894">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-1894">Removed `az component` commands.</span></span> <span data-ttu-id="b63ae-1895">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b63ae-1895">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1896">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1896">Core</span></span>
* <span data-ttu-id="b63ae-1897">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1897">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="b63ae-1898">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1898">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-1899">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1899">ACS</span></span>

* <span data-ttu-id="b63ae-1900">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1900">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="b63ae-1901">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1901">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="b63ae-1902">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1902">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="b63ae-1903">Advisor</span><span class="sxs-lookup"><span data-stu-id="b63ae-1903">Advisor</span></span>

* <span data-ttu-id="b63ae-1904">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-1904">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1905">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-1905">Appservice</span></span>

* <span data-ttu-id="b63ae-1906">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1906">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="b63ae-1907">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1907">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="b63ae-1908">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1908">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="b63ae-1909">消費</span><span class="sxs-lookup"><span data-stu-id="b63ae-1909">Consumption</span></span>

* <span data-ttu-id="b63ae-1910">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1910">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-1911">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-1911">Container</span></span>

* <span data-ttu-id="b63ae-1912">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1912">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-1913">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-1913">Monitor</span></span>

* <span data-ttu-id="b63ae-1914">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1914">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-1915">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-1915">Resource</span></span>

* <span data-ttu-id="b63ae-1916">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1916">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-1917">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-1917">Role</span></span>

* <span data-ttu-id="b63ae-1918">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1918">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="b63ae-1919">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1919">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="b63ae-1920">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1920">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-1921">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-1921">SQL</span></span>

* <span data-ttu-id="b63ae-1922">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1922">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="b63ae-1923">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1923">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1924">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1924">VM</span></span>

* <span data-ttu-id="b63ae-1925">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1925">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="b63ae-1926">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1926">November 14, 2017</span></span>

<span data-ttu-id="b63ae-1927">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="b63ae-1927">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-1928">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-1928">ACR</span></span>

* <span data-ttu-id="b63ae-1929">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1929">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="b63ae-1930">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-1930">ACS</span></span>

* <span data-ttu-id="b63ae-1931">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1931">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="b63ae-1932">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1932">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="b63ae-1933">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1933">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="b63ae-1934">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1934">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="b63ae-1935">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1935">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-1936">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-1936">Appservice</span></span>

* <span data-ttu-id="b63ae-1937">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1937">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="b63ae-1938">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1938">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="b63ae-1939">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1939">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="b63ae-1940">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1940">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="b63ae-1941">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1941">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="b63ae-1942">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="b63ae-1942">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="b63ae-1943">Batch</span><span class="sxs-lookup"><span data-stu-id="b63ae-1943">Batch</span></span>

* <span data-ttu-id="b63ae-1944">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1944">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="b63ae-1945">Batchai</span><span class="sxs-lookup"><span data-stu-id="b63ae-1945">Batchai</span></span>

* <span data-ttu-id="b63ae-1946">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1946">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="b63ae-1947">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1947">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="b63ae-1948">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1948">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="b63ae-1949">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1949">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="b63ae-1950">クラウド</span><span class="sxs-lookup"><span data-stu-id="b63ae-1950">Cloud</span></span>

* <span data-ttu-id="b63ae-1951">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1951">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-1952">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-1952">Container</span></span>

* <span data-ttu-id="b63ae-1953">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1953">Added support to open multiple ports</span></span>
* <span data-ttu-id="b63ae-1954">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1954">Added container group restart policy</span></span>
* <span data-ttu-id="b63ae-1955">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1955">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="b63ae-1956">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1956">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="b63ae-1957">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b63ae-1957">Data Lake Analytics</span></span>

* <span data-ttu-id="b63ae-1958">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1958">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="b63ae-1959">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b63ae-1959">Data Lake Store</span></span>

* <span data-ttu-id="b63ae-1960">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1960">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="b63ae-1961">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b63ae-1961">Extension</span></span>

* <span data-ttu-id="b63ae-1962">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1962">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="b63ae-1963">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1963">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="b63ae-1964">IoT</span><span class="sxs-lookup"><span data-stu-id="b63ae-1964">IoT</span></span>

* <span data-ttu-id="b63ae-1965">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1965">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-1966">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-1966">Monitor</span></span>

* <span data-ttu-id="b63ae-1967">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1967">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-1968">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-1968">Network</span></span>

* <span data-ttu-id="b63ae-1969">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1969">Added support for CAA DNS records</span></span>
* <span data-ttu-id="b63ae-1970">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1970">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="b63ae-1971">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1971">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="b63ae-1972">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1972">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="b63ae-1973">Reservations</span><span class="sxs-lookup"><span data-stu-id="b63ae-1973">Reservations</span></span>

* <span data-ttu-id="b63ae-1974">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-1974">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-1975">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-1975">Resource</span></span>

* <span data-ttu-id="b63ae-1976">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1976">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-1977">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-1977">SQL</span></span>

* <span data-ttu-id="b63ae-1978">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1978">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-1979">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-1979">Storage</span></span>

* <span data-ttu-id="b63ae-1980">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1980">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="b63ae-1981">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1981">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="b63ae-1982">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1982">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="b63ae-1983">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1983">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="b63ae-1984">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1984">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="b63ae-1985">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1985">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="b63ae-1986">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1986">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-1987">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-1987">VM</span></span>

* <span data-ttu-id="b63ae-1988">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1988">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="b63ae-1989">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1989">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="b63ae-1990">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1990">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="b63ae-1991">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1991">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="b63ae-1992">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1992">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="b63ae-1993">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-1993">October 24, 2017</span></span>

<span data-ttu-id="b63ae-1994">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="b63ae-1994">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-1995">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-1995">Core</span></span>

* <span data-ttu-id="b63ae-1996">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1996">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-1997">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-1997">ACR</span></span>

* <span data-ttu-id="b63ae-1998">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1998">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="b63ae-1999">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-1999">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="b63ae-2000">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2000">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-2001">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-2001">ACS</span></span>

* <span data-ttu-id="b63ae-2002">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2002">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="b63ae-2003">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2003">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-2004">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-2004">Appservice</span></span>

* <span data-ttu-id="b63ae-2005">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2005">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="b63ae-2006">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b63ae-2006">Component</span></span>

* <span data-ttu-id="b63ae-2007">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2007">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-2008">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-2008">Monitor</span></span>

* <span data-ttu-id="b63ae-2009">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2009">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-2010">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-2010">Resource</span></span>

* <span data-ttu-id="b63ae-2011">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2011">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="b63ae-2012">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2012">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-2013">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-2013">VM</span></span>

* <span data-ttu-id="b63ae-2014">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2014">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="b63ae-2015">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-2015">October 9, 2017</span></span>

<span data-ttu-id="b63ae-2016">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="b63ae-2016">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-2017">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-2017">Core</span></span>

* <span data-ttu-id="b63ae-2018">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2018">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-2019">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-2019">Appservice</span></span>

* <span data-ttu-id="b63ae-2020">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2020">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="b63ae-2021">Batch</span><span class="sxs-lookup"><span data-stu-id="b63ae-2021">Batch</span></span>

* <span data-ttu-id="b63ae-2022">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2022">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="b63ae-2023">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2023">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="b63ae-2024">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2024">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="b63ae-2025">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2025">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="b63ae-2026">Batchai</span><span class="sxs-lookup"><span data-stu-id="b63ae-2026">Batchai</span></span>

* <span data-ttu-id="b63ae-2027">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-2027">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="b63ae-2028">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b63ae-2028">Keyvault</span></span>

* <span data-ttu-id="b63ae-2029">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2029">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="b63ae-2030">(#4448)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2030">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="b63ae-2031">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-2031">Network</span></span>

* <span data-ttu-id="b63ae-2032">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2032">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="b63ae-2033">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2033">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-2034">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-2034">Resource</span></span>

* <span data-ttu-id="b63ae-2035">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2035">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="b63ae-2036">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2036">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="b63ae-2037">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2037">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="b63ae-2038">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2038">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-2039">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-2039">Sql</span></span>

* <span data-ttu-id="b63ae-2040">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2040">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="b63ae-2041">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2041">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="b63ae-2042">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2042">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-2043">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-2043">Storage</span></span>

* <span data-ttu-id="b63ae-2044">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2044">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-2045">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-2045">Vm</span></span>

* <span data-ttu-id="b63ae-2046">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2046">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="b63ae-2047">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2047">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="b63ae-2048">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2048">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="b63ae-2049">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2049">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="b63ae-2050">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2050">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="b63ae-2051">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-2051">September 22, 2017</span></span>

<span data-ttu-id="b63ae-2052">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="b63ae-2052">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-2053">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-2053">Resource</span></span>

* <span data-ttu-id="b63ae-2054">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2054">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="b63ae-2055">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2055">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="b63ae-2056">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2056">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="b63ae-2057">[破壊的変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2057">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-2058">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-2058">Network</span></span>

* <span data-ttu-id="b63ae-2059">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2059">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="b63ae-2060">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2060">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="b63ae-2061">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2061">Added `asg` application security group commands</span></span>
* <span data-ttu-id="b63ae-2062">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2062">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="b63ae-2063">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2063">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="b63ae-2064">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2064">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="b63ae-2065">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2065">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-2066">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-2066">Storage</span></span>

* <span data-ttu-id="b63ae-2067">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2067">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="b63ae-2068">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="b63ae-2068">Eventgrid</span></span>

* <span data-ttu-id="b63ae-2069">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2069">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-2070">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-2070">SQL</span></span>

* <span data-ttu-id="b63ae-2071">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2071">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="b63ae-2072">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-2072">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="b63ae-2073">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2073">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="b63ae-2074">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b63ae-2074">Keyvault</span></span>

* <span data-ttu-id="b63ae-2075">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2075">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-2076">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-2076">VM</span></span>

* <span data-ttu-id="b63ae-2077">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2077">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="b63ae-2078">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2078">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="b63ae-2079">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2079">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="b63ae-2080">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2080">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="b63ae-2081">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2081">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="b63ae-2082">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2082">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-2083">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-2083">ACS</span></span>

* <span data-ttu-id="b63ae-2084">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2084">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-2085">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-2085">Appservice</span></span>

* <span data-ttu-id="b63ae-2086">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2086">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="b63ae-2087">バックアップ</span><span class="sxs-lookup"><span data-stu-id="b63ae-2087">Backup</span></span>

* <span data-ttu-id="b63ae-2088">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-2088">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="b63ae-2089">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-2089">September 11, 2017</span></span>

<span data-ttu-id="b63ae-2090">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="b63ae-2090">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="b63ae-2091">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-2091">Core</span></span>

* <span data-ttu-id="b63ae-2092">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2092">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="b63ae-2093">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2093">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-2094">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-2094">Acs</span></span>

* <span data-ttu-id="b63ae-2095">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2095">Added `acs list-locations` command</span></span>
* <span data-ttu-id="b63ae-2096">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2096">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-2097">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-2097">Appservice</span></span>

* <span data-ttu-id="b63ae-2098">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2098">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="b63ae-2099">CDN</span><span class="sxs-lookup"><span data-stu-id="b63ae-2099">CDN</span></span>

* <span data-ttu-id="b63ae-2100">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2100">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="b63ae-2101">拡張機能</span><span class="sxs-lookup"><span data-stu-id="b63ae-2101">Extension</span></span>

* <span data-ttu-id="b63ae-2102">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-2102">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="b63ae-2103">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b63ae-2103">Keyvault</span></span>

* <span data-ttu-id="b63ae-2104">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2104">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-2105">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-2105">Network</span></span>

* <span data-ttu-id="b63ae-2106">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2106">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="b63ae-2107">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2107">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="b63ae-2108">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2108">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="b63ae-2109">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2109">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="b63ae-2110">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2110">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-2111">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-2111">Resource</span></span>

* <span data-ttu-id="b63ae-2112">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2112">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="b63ae-2113">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2113">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="b63ae-2114">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2114">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="b63ae-2115">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2115">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-2116">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-2116">SQL</span></span>

* <span data-ttu-id="b63ae-2117">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2117">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-2118">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-2118">VM</span></span>

* <span data-ttu-id="b63ae-2119">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="b63ae-2119">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="b63ae-2120">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="b63ae-2120">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="b63ae-2121">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2121">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="b63ae-2122">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="b63ae-2122">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="b63ae-2123">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="b63ae-2123">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="b63ae-2124">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-2124">August 31, 2017</span></span>

<span data-ttu-id="b63ae-2125">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="b63ae-2125">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="b63ae-2126">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b63ae-2126">Keyvault</span></span>

* <span data-ttu-id="b63ae-2127">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2127">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="b63ae-2128">SF</span><span class="sxs-lookup"><span data-stu-id="b63ae-2128">Sf</span></span>

* <span data-ttu-id="b63ae-2129">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-2129">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-2130">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-2130">Storage</span></span>

* <span data-ttu-id="b63ae-2131">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2131">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="b63ae-2132">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2132">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="b63ae-2133">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-2133">August 28, 2017</span></span>

<span data-ttu-id="b63ae-2134">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="b63ae-2134">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="b63ae-2135">CLI</span><span class="sxs-lookup"><span data-stu-id="b63ae-2135">CLI</span></span>

* <span data-ttu-id="b63ae-2136">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2136">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-2137">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-2137">ACS</span></span>

* <span data-ttu-id="b63ae-2138">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2138">Corrected preview regions</span></span>
* <span data-ttu-id="b63ae-2139">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2139">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="b63ae-2140">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2140">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-2141">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-2141">Appservice</span></span>

* <span data-ttu-id="b63ae-2142">[破壊的変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2142">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="b63ae-2143">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2143">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="b63ae-2144">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2144">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="b63ae-2145">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2145">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="b63ae-2146">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="b63ae-2146">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="b63ae-2147">IoT</span><span class="sxs-lookup"><span data-stu-id="b63ae-2147">IoT</span></span>

* <span data-ttu-id="b63ae-2148">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2148">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-2149">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-2149">Network</span></span>

* <span data-ttu-id="b63ae-2150">[破壊的変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2150">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="b63ae-2151">[破壊的変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2151">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="b63ae-2152">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2152">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="b63ae-2153">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2153">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="b63ae-2154">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2154">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="b63ae-2155">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b63ae-2155">Profile</span></span>

* <span data-ttu-id="b63ae-2156">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2156">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="b63ae-2157">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b63ae-2157">Service Fabric</span></span>

* <span data-ttu-id="b63ae-2158">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-2158">Preview release</span></span>
* <span data-ttu-id="b63ae-2159">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2159">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="b63ae-2160">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2160">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="b63ae-2161">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2161">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-2162">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-2162">Storage</span></span>

* <span data-ttu-id="b63ae-2163">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2163">Enabled setting blob tier</span></span>
* <span data-ttu-id="b63ae-2164">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2164">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="b63ae-2165">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2165">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="b63ae-2166">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2166">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="b63ae-2167">[破壊的変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2167">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="b63ae-2168">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="b63ae-2168">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-2169">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-2169">VM</span></span>

* <span data-ttu-id="b63ae-2170">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2170">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="b63ae-2171">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2171">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="b63ae-2172">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2172">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="b63ae-2173">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2173">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="b63ae-2174">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2174">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="b63ae-2175">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2175">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="b63ae-2176">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-2176">August 15, 2017</span></span>

<span data-ttu-id="b63ae-2177">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="b63ae-2177">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-2178">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-2178">ACS</span></span>

* <span data-ttu-id="b63ae-2179">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2179">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-2180">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-2180">Appservice</span></span>

* <span data-ttu-id="b63ae-2181">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2181">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="b63ae-2182">Event Grid</span><span class="sxs-lookup"><span data-stu-id="b63ae-2182">Event Grid</span></span>

* <span data-ttu-id="b63ae-2183">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2183">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="b63ae-2184">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-2184">August 11, 2017</span></span>

<span data-ttu-id="b63ae-2185">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="b63ae-2185">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-2186">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-2186">ACS</span></span>

* <span data-ttu-id="b63ae-2187">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2187">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="b63ae-2188">Batch</span><span class="sxs-lookup"><span data-stu-id="b63ae-2188">Batch</span></span>

* <span data-ttu-id="b63ae-2189">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2189">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="b63ae-2190">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2190">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="b63ae-2191">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2191">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="b63ae-2192">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2192">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="b63ae-2193">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2193">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="b63ae-2194">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2194">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="b63ae-2195">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b63ae-2195">Component</span></span>

* <span data-ttu-id="b63ae-2196">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2196">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="b63ae-2197">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b63ae-2197">Container</span></span>

* <span data-ttu-id="b63ae-2198">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2198">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="b63ae-2199">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b63ae-2199">Data Lake Store</span></span>

* <span data-ttu-id="b63ae-2200">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2200">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="b63ae-2201">Event Grid</span><span class="sxs-lookup"><span data-stu-id="b63ae-2201">Event Grid</span></span>

* <span data-ttu-id="b63ae-2202">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-2202">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-2203">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-2203">Network</span></span>

* <span data-ttu-id="b63ae-2204">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2204">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="b63ae-2205">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2205">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="b63ae-2206">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2206">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="b63ae-2207">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2207">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="b63ae-2208">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b63ae-2208">Profile</span></span>

* <span data-ttu-id="b63ae-2209">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2209">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-2210">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-2210">Storage</span></span>

* <span data-ttu-id="b63ae-2211">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2211">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-2212">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-2212">VM</span></span>

* <span data-ttu-id="b63ae-2213">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2213">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="b63ae-2214">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2214">Exposed `list-skus` command</span></span>
* <span data-ttu-id="b63ae-2215">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2215">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="b63ae-2216">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2216">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="b63ae-2217">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2217">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="b63ae-2218">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-2218">July 28, 2017</span></span>

<span data-ttu-id="b63ae-2219">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="b63ae-2219">Version 2.0.12</span></span>

* <span data-ttu-id="b63ae-2220">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2220">Added container commands</span></span>
* <span data-ttu-id="b63ae-2221">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2221">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="b63ae-2222">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-2222">Core</span></span>

* <span data-ttu-id="b63ae-2223">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2223">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="b63ae-2224">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2224">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="b63ae-2225">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2225">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="b63ae-2226">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2226">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="b63ae-2227">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2227">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="b63ae-2228">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2228">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="b63ae-2229">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2229">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="b63ae-2230">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2230">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="b63ae-2231">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2231">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="b63ae-2232">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2232">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="b63ae-2233">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2233">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="b63ae-2234">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2234">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="b63ae-2235">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2235">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="b63ae-2236">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2236">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="b63ae-2237">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2237">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="b63ae-2238">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2238">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="b63ae-2239">ACR</span><span class="sxs-lookup"><span data-stu-id="b63ae-2239">ACR</span></span>

* <span data-ttu-id="b63ae-2240">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2240">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="b63ae-2241">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2241">Support SKU update for managed registries</span></span>
* <span data-ttu-id="b63ae-2242">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2242">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="b63ae-2243">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2243">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="b63ae-2244">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2244">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="b63ae-2245">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2245">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-2246">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-2246">ACS</span></span>

* <span data-ttu-id="b63ae-2247">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2247">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-2248">Appservice</span><span class="sxs-lookup"><span data-stu-id="b63ae-2248">Appservice</span></span>

* <span data-ttu-id="b63ae-2249">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2249">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="b63ae-2250">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2250">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="b63ae-2251">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2251">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="b63ae-2252">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2252">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="b63ae-2253">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2253">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="b63ae-2254">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2254">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="b63ae-2255">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2255">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="b63ae-2256">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2256">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="b63ae-2257">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2257">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="b63ae-2258">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="b63ae-2258">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="b63ae-2259">Batch</span><span class="sxs-lookup"><span data-stu-id="b63ae-2259">Batch</span></span>

* <span data-ttu-id="b63ae-2260">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2260">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="b63ae-2261">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2261">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="b63ae-2262">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2262">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="b63ae-2263">CDN</span><span class="sxs-lookup"><span data-stu-id="b63ae-2263">CDN</span></span>

* <span data-ttu-id="b63ae-2264">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2264">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="b63ae-2265">クラウド</span><span class="sxs-lookup"><span data-stu-id="b63ae-2265">Cloud</span></span>

* <span data-ttu-id="b63ae-2266">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2266">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="b63ae-2267">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="b63ae-2267">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="b63ae-2268">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2268">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="b63ae-2269">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2269">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="b63ae-2270">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2270">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b63ae-2271">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b63ae-2271">CosmosDB</span></span>

* <span data-ttu-id="b63ae-2272">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2272">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="b63ae-2273">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2273">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="b63ae-2274">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b63ae-2274">Data Lake Analytics</span></span>

* <span data-ttu-id="b63ae-2275">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2275">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="b63ae-2276">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2276">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="b63ae-2277">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2277">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="b63ae-2278">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b63ae-2278">Data Lake Store</span></span>

* <span data-ttu-id="b63ae-2279">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2279">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="b63ae-2280">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2280">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="b63ae-2281">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2281">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="b63ae-2282">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-2282">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="b63ae-2283">対話</span><span class="sxs-lookup"><span data-stu-id="b63ae-2283">Interactive</span></span>

* <span data-ttu-id="b63ae-2284">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2284">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="b63ae-2285">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2285">Increased test coverage</span></span>
* <span data-ttu-id="b63ae-2286">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2286">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="b63ae-2287">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2287">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="b63ae-2288">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2288">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="b63ae-2289">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2289">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="b63ae-2290">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2290">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="b63ae-2291">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2291">Added `--progress` flag</span></span>
* <span data-ttu-id="b63ae-2292">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2292">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="b63ae-2293">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2293">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="b63ae-2294">IoT</span><span class="sxs-lookup"><span data-stu-id="b63ae-2294">IoT</span></span>

* <span data-ttu-id="b63ae-2295">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2295">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="b63ae-2296">(#3934)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2296">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="b63ae-2297">Key Vault</span><span class="sxs-lookup"><span data-stu-id="b63ae-2297">Key vault</span></span>

* <span data-ttu-id="b63ae-2298">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2298">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="b63ae-2299">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b63ae-2299">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="b63ae-2300">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b63ae-2300">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="b63ae-2301">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b63ae-2301">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="b63ae-2302">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="b63ae-2302">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="b63ae-2303">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2303">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="b63ae-2304">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2304">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="b63ae-2305">(#3307)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2305">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="b63ae-2306">ラボ</span><span class="sxs-lookup"><span data-stu-id="b63ae-2306">Lab</span></span>

* <span data-ttu-id="b63ae-2307">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2307">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="b63ae-2308">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2308">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-2309">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-2309">Monitor</span></span>

* <span data-ttu-id="b63ae-2310">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2310">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="b63ae-2311">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2311">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="b63ae-2312">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2312">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="b63ae-2313">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2313">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="b63ae-2314">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2314">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="b63ae-2315">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2315">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="b63ae-2316">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2316">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="b63ae-2317">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2317">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="b63ae-2318">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2318">`location` no longer required</span></span>
  * <span data-ttu-id="b63ae-2319">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2319">Add name and ID support for target</span></span>
  * <span data-ttu-id="b63ae-2320">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2320">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="b63ae-2321">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2321">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="b63ae-2322">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2322">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="b63ae-2323">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2323">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="b63ae-2324">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2324">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="b63ae-2325">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2325">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-2326">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-2326">Network</span></span>

* <span data-ttu-id="b63ae-2327">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2327">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="b63ae-2328">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2328">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="b63ae-2329">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2329">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="b63ae-2330">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2330">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="b63ae-2331">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2331">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="b63ae-2332">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2332">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="b63ae-2333">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2333">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="b63ae-2334">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2334">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="b63ae-2335">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2335">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="b63ae-2336">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2336">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="b63ae-2337">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2337">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="b63ae-2338">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2338">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="b63ae-2339">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2339">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="b63ae-2340">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2340">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="b63ae-2341">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2341">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="b63ae-2342">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2342">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="b63ae-2343">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2343">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="b63ae-2344">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2344">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="b63ae-2345">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2345">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="b63ae-2346">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2346">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="b63ae-2347">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2347">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="b63ae-2348">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2348">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="b63ae-2349">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2349">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="b63ae-2350">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2350">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="b63ae-2351">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2351">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="b63ae-2352">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2352">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="b63ae-2353">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2353">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="b63ae-2354">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b63ae-2354">Profile</span></span>

* <span data-ttu-id="b63ae-2355">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2355">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="b63ae-2356">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2356">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="b63ae-2357">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2357">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="b63ae-2358">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2358">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="b63ae-2359">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2359">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="b63ae-2360">RDBMS</span><span class="sxs-lookup"><span data-stu-id="b63ae-2360">RDBMS</span></span>

* <span data-ttu-id="b63ae-2361">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2361">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="b63ae-2362">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2362">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="b63ae-2363">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2363">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="b63ae-2364">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2364">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-2365">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-2365">Resource</span></span>

* <span data-ttu-id="b63ae-2366">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2366">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="b63ae-2367">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2367">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="b63ae-2368">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2368">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="b63ae-2369">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2369">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="b63ae-2370">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2370">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="b63ae-2371">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2371">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="b63ae-2372">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2372">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="b63ae-2373">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2373">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-2374">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-2374">Role</span></span>

* <span data-ttu-id="b63ae-2375">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2375">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="b63ae-2376">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2376">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="b63ae-2377">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="b63ae-2377">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="b63ae-2378">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2378">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="b63ae-2379">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2379">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="b63ae-2380">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b63ae-2380">Service Fabric</span></span>
* <span data-ttu-id="b63ae-2381">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2381">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="b63ae-2382">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2382">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="b63ae-2383">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2383">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-2384">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-2384">SQL</span></span>

* <span data-ttu-id="b63ae-2385">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2385">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="b63ae-2386">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2386">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="b63ae-2387">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2387">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-2388">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-2388">Storage</span></span>

* <span data-ttu-id="b63ae-2389">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2389">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="b63ae-2390">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2390">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="b63ae-2391">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2391">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="b63ae-2392">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2392">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="b63ae-2393">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2393">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="b63ae-2394">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2394">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-2395">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-2395">VM</span></span>

* <span data-ttu-id="b63ae-2396">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2396">Support configuring nsg</span></span>
* <span data-ttu-id="b63ae-2397">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2397">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="b63ae-2398">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="b63ae-2398">Support managed service identities</span></span>
* <span data-ttu-id="b63ae-2399">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2399">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="b63ae-2400">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2400">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="b63ae-2401">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-2401">May 10, 2017</span></span>

<span data-ttu-id="b63ae-2402">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="b63ae-2402">Version 2.0.6</span></span>

* <span data-ttu-id="b63ae-2403">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2403">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="b63ae-2404">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2404">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="b63ae-2405">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2405">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="b63ae-2406">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2406">Include Cognitive Services module</span></span>
* <span data-ttu-id="b63ae-2407">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2407">Include Service Fabric module</span></span>
* <span data-ttu-id="b63ae-2408">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2408">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="b63ae-2409">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2409">Add support for CDN commands</span></span>
* <span data-ttu-id="b63ae-2410">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2410">Remove Container module</span></span>
* <span data-ttu-id="b63ae-2411">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2411">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="b63ae-2412">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2412">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="b63ae-2413">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-2413">Core</span></span>

* <span data-ttu-id="b63ae-2414">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-2414">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="b63ae-2415">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2415">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="b63ae-2416">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2416">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="b63ae-2417">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2417">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="b63ae-2418">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2418">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="b63ae-2419">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2419">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="b63ae-2420">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2420">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="b63ae-2421">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2421">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="b63ae-2422">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2422">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="b63ae-2423">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="b63ae-2423">core: Improved performance</span></span>
* <span data-ttu-id="b63ae-2424">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="b63ae-2424">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="b63ae-2425">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-2425">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-2426">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-2426">ACS</span></span>

* <span data-ttu-id="b63ae-2427">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2427">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="b63ae-2428">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2428">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="b63ae-2429">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2429">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="b63ae-2430">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2430">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-2431">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-2431">AppService</span></span>

* <span data-ttu-id="b63ae-2432">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2432">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="b63ae-2433">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2433">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="b63ae-2434">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2434">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="b63ae-2435">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2435">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="b63ae-2436">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2436">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="b63ae-2437">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2437">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="b63ae-2438">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="b63ae-2438">support slot swap with preview</span></span>
* <span data-ttu-id="b63ae-2439">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2439">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="b63ae-2440">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2440">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="b63ae-2441">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b63ae-2441">CosmosDB</span></span>

* <span data-ttu-id="b63ae-2442">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2442">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="b63ae-2443">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2443">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="b63ae-2444">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2444">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="b63ae-2445">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2445">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="b63ae-2446">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b63ae-2446">Data Lake Analytics</span></span>

* <span data-ttu-id="b63ae-2447">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2447">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="b63ae-2448">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2448">Add support for new catalog item type: package.</span></span> <span data-ttu-id="b63ae-2449">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="b63ae-2449">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="b63ae-2450">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2450">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="b63ae-2451">テーブル</span><span class="sxs-lookup"><span data-stu-id="b63ae-2451">Table</span></span>
  * <span data-ttu-id="b63ae-2452">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="b63ae-2452">Table valued function</span></span>
  * <span data-ttu-id="b63ae-2453">表示</span><span class="sxs-lookup"><span data-stu-id="b63ae-2453">View</span></span>
  * <span data-ttu-id="b63ae-2454">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2454">Table Statistics.</span></span> <span data-ttu-id="b63ae-2455">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="b63ae-2455">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="b63ae-2456">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b63ae-2456">Data Lake Store</span></span>

* <span data-ttu-id="b63ae-2457">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2457">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="b63ae-2458">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2458">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="b63ae-2459">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="b63ae-2459">missed help for access show.</span></span> <span data-ttu-id="b63ae-2460">追加しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2460">adding it.</span></span> <span data-ttu-id="b63ae-2461">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2461">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="b63ae-2462">検索</span><span class="sxs-lookup"><span data-stu-id="b63ae-2462">Find</span></span>

* <span data-ttu-id="b63ae-2463">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2463">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="b63ae-2464">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b63ae-2464">KeyVault</span></span>

* <span data-ttu-id="b63ae-2465">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2465">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="b63ae-2466">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2466">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="b63ae-2467">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="b63ae-2467">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="b63ae-2468">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2468">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="b63ae-2469">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2469">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="b63ae-2470">ラボ</span><span class="sxs-lookup"><span data-stu-id="b63ae-2470">Lab</span></span>

* <span data-ttu-id="b63ae-2471">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2471">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="b63ae-2472">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2472">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="b63ae-2473">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2473">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="b63ae-2474">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2474">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="b63ae-2475">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2475">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="b63ae-2476">監視</span><span class="sxs-lookup"><span data-stu-id="b63ae-2476">Monitor</span></span>

* <span data-ttu-id="b63ae-2477">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2477">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="b63ae-2478">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2478">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="b63ae-2479">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-2479">Network</span></span>

* <span data-ttu-id="b63ae-2480">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2480">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="b63ae-2481">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2481">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="b63ae-2482">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2482">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="b63ae-2483">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2483">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="b63ae-2484">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2484">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="b63ae-2485">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2485">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="b63ae-2486">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2486">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="b63ae-2487">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2487">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="b63ae-2488">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2488">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="b63ae-2489">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2489">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="b63ae-2490">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2490">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="b63ae-2491">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2491">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="b63ae-2492">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2492">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="b63ae-2493">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2493">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="b63ae-2494">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2494">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="b63ae-2495">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2495">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="b63ae-2496">プロファイル</span><span class="sxs-lookup"><span data-stu-id="b63ae-2496">Profile</span></span>

* <span data-ttu-id="b63ae-2497">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2497">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="b63ae-2498">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2498">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="b63ae-2499">Redis</span><span class="sxs-lookup"><span data-stu-id="b63ae-2499">Redis</span></span>

* <span data-ttu-id="b63ae-2500">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2500">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="b63ae-2501">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2501">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="b63ae-2502">Resource</span><span class="sxs-lookup"><span data-stu-id="b63ae-2502">Resource</span></span>

* <span data-ttu-id="b63ae-2503">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2503">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="b63ae-2504">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2504">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="b63ae-2505">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2505">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="b63ae-2506">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2506">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="b63ae-2507">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2507">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="b63ae-2508">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2508">Add docs for az lock update.</span></span> <span data-ttu-id="b63ae-2509">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2509">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="b63ae-2510">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-2510">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="b63ae-2511">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2511">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="b63ae-2512">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2512">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="b63ae-2513">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2513">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="b63ae-2514">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2514">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="b63ae-2515">Role</span><span class="sxs-lookup"><span data-stu-id="b63ae-2515">Role</span></span>

* <span data-ttu-id="b63ae-2516">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2516">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="b63ae-2517">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2517">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="b63ae-2518">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2518">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="b63ae-2519">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-2519">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="b63ae-2520">SQL</span><span class="sxs-lookup"><span data-stu-id="b63ae-2520">SQL</span></span>

* <span data-ttu-id="b63ae-2521">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2521">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="b63ae-2522">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2522">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="b63ae-2523">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-2523">Storage</span></span>

* <span data-ttu-id="b63ae-2524">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="b63ae-2524">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="b63ae-2525">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2525">Add support for incremental blob copy</span></span>
* <span data-ttu-id="b63ae-2526">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2526">Add support for large block blob upload</span></span>
* <span data-ttu-id="b63ae-2527">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="b63ae-2527">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-2528">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-2528">VM</span></span>

* <span data-ttu-id="b63ae-2529">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2529">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="b63ae-2530">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2530">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="b63ae-2531">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="b63ae-2531">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="b63ae-2532">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="b63ae-2532">az vm/vmss disk</span></span>
  3. <span data-ttu-id="b63ae-2533">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2533">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="b63ae-2534">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="b63ae-2534">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="b63ae-2535">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2535">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="b63ae-2536">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-2536">April 3, 2017</span></span>

<span data-ttu-id="b63ae-2537">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="b63ae-2537">Version 2.0.2</span></span>

<span data-ttu-id="b63ae-2538">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="b63ae-2538">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="b63ae-2539">コア</span><span class="sxs-lookup"><span data-stu-id="b63ae-2539">Core</span></span>

* <span data-ttu-id="b63ae-2540">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="b63ae-2540">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="b63ae-2541">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2541">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="b63ae-2542">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2542">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="b63ae-2543">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2543">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="b63ae-2544">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2544">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="b63ae-2545">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="b63ae-2545">Add prompting for missing template parameters.</span></span> <span data-ttu-id="b63ae-2546">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2546">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="b63ae-2547">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="b63ae-2547">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="b63ae-2548">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="b63ae-2548">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="b63ae-2549">ACS</span><span class="sxs-lookup"><span data-stu-id="b63ae-2549">ACS</span></span>

* <span data-ttu-id="b63ae-2550">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2550">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="b63ae-2551">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="b63ae-2551">Add support for ssh key password prompting.</span></span> <span data-ttu-id="b63ae-2552">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2552">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="b63ae-2553">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="b63ae-2553">Add support for windows clusters.</span></span> <span data-ttu-id="b63ae-2554">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2554">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="b63ae-2555">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="b63ae-2555">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="b63ae-2556">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2556">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="b63ae-2557">AppService</span><span class="sxs-lookup"><span data-stu-id="b63ae-2557">AppService</span></span>

* <span data-ttu-id="b63ae-2558">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2558">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="b63ae-2559">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2559">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="b63ae-2560">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2560">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="b63ae-2561">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2561">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="b63ae-2562">DataLake</span><span class="sxs-lookup"><span data-stu-id="b63ae-2562">DataLake</span></span>

* <span data-ttu-id="b63ae-2563">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-2563">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="b63ae-2564">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="b63ae-2564">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="b63ae-2565">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="b63ae-2565">DocuemntDB</span></span>

* <span data-ttu-id="b63ae-2566">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2566">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="b63ae-2567">VM</span><span class="sxs-lookup"><span data-stu-id="b63ae-2567">VM</span></span>

* <span data-ttu-id="b63ae-2568">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2568">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="b63ae-2569">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2569">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="b63ae-2570">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2570">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="b63ae-2571">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2571">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="b63ae-2572">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2572">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="b63ae-2573">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2573">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="b63ae-2574">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="b63ae-2574">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="b63ae-2575">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="b63ae-2575">February 27, 2017</span></span>

<span data-ttu-id="b63ae-2576">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="b63ae-2576">Version 2.0.0</span></span>

<span data-ttu-id="b63ae-2577">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2577">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="b63ae-2578">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2578">Container Service (acs)</span></span>
- <span data-ttu-id="b63ae-2579">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="b63ae-2579">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="b63ae-2580">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="b63ae-2580">Networking</span></span>
- <span data-ttu-id="b63ae-2581">Storage</span><span class="sxs-lookup"><span data-stu-id="b63ae-2581">Storage</span></span>

<span data-ttu-id="b63ae-2582">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2582">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="b63ae-2583">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="b63ae-2583">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="b63ae-2584">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2584">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="b63ae-2585">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="b63ae-2585">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="b63ae-2586">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="b63ae-2586">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="b63ae-2587">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2587">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="b63ae-2588">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="b63ae-2588">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="b63ae-2589">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="b63ae-2589">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="b63ae-2590">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="b63ae-2590">Provide feedback from the command line with the `az feedback` command</span></span>

