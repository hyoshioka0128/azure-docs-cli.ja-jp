---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 10/23/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 65e34ab6014c47ae92a6d4bae8cdc30d4a1413dc
ms.sourcegitcommit: aec89531c938781b4724f43b5bb4b878e106a26a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2018
ms.locfileid: "49952487"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="ec8b6-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="ec8b6-103">Azure CLI release notes</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="ec8b6-104">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-104">October 23, 2018</span></span>

<span data-ttu-id="ec8b6-105">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="ec8b6-105">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-106">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-106">Core</span></span>
* <span data-ttu-id="ec8b6-107">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-107">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="ec8b6-108">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-108">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-109">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-109">ACR</span></span>
* <span data-ttu-id="ec8b6-110">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-110">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="ec8b6-111">CDN</span><span class="sxs-lookup"><span data-stu-id="ec8b6-111">CDN</span></span>
* <span data-ttu-id="ec8b6-112">[破壊的変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-112">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="ec8b6-113">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-113">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-114">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-114">Container</span></span>
* <span data-ttu-id="ec8b6-115">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-115">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="ec8b6-116">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-116">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="ec8b6-117">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-117">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="ec8b6-118">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-118">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="ec8b6-119">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-119">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="ec8b6-120">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-120">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="ec8b6-121">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-121">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ec8b6-122">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ec8b6-122">CosmosDB</span></span>
* <span data-ttu-id="ec8b6-123">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-123">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="ec8b6-124">Interactive</span><span class="sxs-lookup"><span data-stu-id="ec8b6-124">Interactive</span></span>
* <span data-ttu-id="ec8b6-125">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-125">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="ec8b6-126">IoT Central</span><span class="sxs-lookup"><span data-stu-id="ec8b6-126">IoT Central</span></span>
* <span data-ttu-id="ec8b6-127">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-127">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="ec8b6-128">[破壊的変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-128">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="ec8b6-129">監視</span><span class="sxs-lookup"><span data-stu-id="ec8b6-129">Monitor</span></span>
* <span data-ttu-id="ec8b6-130">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="ec8b6-130">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="ec8b6-131">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-131">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="ec8b6-132">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-132">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="ec8b6-133">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-133">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="ec8b6-134">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-134">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="ec8b6-135">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-135">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="ec8b6-136">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="ec8b6-136">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="ec8b6-137">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-137">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="ec8b6-138">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-138">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="ec8b6-139">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-139">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-140">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-140">Network</span></span>
* <span data-ttu-id="ec8b6-141">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-141">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="ec8b6-142">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-142">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="ec8b6-143">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ec8b6-143">ServiceBus</span></span>
* <span data-ttu-id="ec8b6-144">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-144">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-145">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-145">SQL</span></span>
* <span data-ttu-id="ec8b6-146">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-146">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-147">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-147">Storage</span></span>
* <span data-ttu-id="ec8b6-148">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-148">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="ec8b6-149">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-149">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-150">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-150">VM</span></span>
* <span data-ttu-id="ec8b6-151">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-151">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="ec8b6-152">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-152">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="ec8b6-153">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-153">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="ec8b6-154">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-154">October 16, 2018</span></span>

<span data-ttu-id="ec8b6-155">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="ec8b6-155">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-156">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-156">VM</span></span>
* <span data-ttu-id="ec8b6-157">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-157">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="ec8b6-158">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-158">October 9, 2018</span></span>

<span data-ttu-id="ec8b6-159">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="ec8b6-159">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-160">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-160">Core</span></span>
* <span data-ttu-id="ec8b6-161">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-161">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-162">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-162">ACR</span></span>
* <span data-ttu-id="ec8b6-163">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-163">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-164">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-164">ACS</span></span>
* <span data-ttu-id="ec8b6-165">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="ec8b6-165">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="ec8b6-166">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-166">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="ec8b6-167">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-167">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="ec8b6-168">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-168">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-169">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-169">Container</span></span>
* <span data-ttu-id="ec8b6-170">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-170">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="ec8b6-171">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-171">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="ec8b6-172">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="ec8b6-172">Event Hub</span></span>
* <span data-ttu-id="ec8b6-173">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-173">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="ec8b6-174">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-174">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="ec8b6-175">拡張機能</span><span class="sxs-lookup"><span data-stu-id="ec8b6-175">Extensions</span></span>
* <span data-ttu-id="ec8b6-176">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-176">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="ec8b6-177">HDInsight</span><span class="sxs-lookup"><span data-stu-id="ec8b6-177">HDInsight</span></span>
* <span data-ttu-id="ec8b6-178">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-178">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="ec8b6-179">IoT</span><span class="sxs-lookup"><span data-stu-id="ec8b6-179">IoT</span></span>
* <span data-ttu-id="ec8b6-180">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-180">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="ec8b6-181">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ec8b6-181">KeyVault</span></span>
* <span data-ttu-id="ec8b6-182">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-182">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-183">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-183">Network</span></span>
* <span data-ttu-id="ec8b6-184">`network dns zone create` を修正しました: ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-184">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="ec8b6-185">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="ec8b6-185">See #6052</span></span>
* <span data-ttu-id="ec8b6-186">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-186">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="ec8b6-187">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-187">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="ec8b6-188">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-188">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="ec8b6-189">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-189">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="ec8b6-190">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-190">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="ec8b6-191">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-191">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="ec8b6-192">Role</span><span class="sxs-lookup"><span data-stu-id="ec8b6-192">Role</span></span>
* <span data-ttu-id="ec8b6-193">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-193">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="ec8b6-194">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-194">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="ec8b6-195">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-195">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="ec8b6-196">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-196">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="ec8b6-197">Service Bus</span><span class="sxs-lookup"><span data-stu-id="ec8b6-197">Service Bus</span></span>
* <span data-ttu-id="ec8b6-198">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-198">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-199">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-199">VM</span></span>
* <span data-ttu-id="ec8b6-200">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-200">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="ec8b6-201">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-201">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="ec8b6-202">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-202">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="ec8b6-203">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-203">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="ec8b6-204">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-204">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="ec8b6-205">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-205">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="ec8b6-206">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-206">September 21, 2018</span></span>

<span data-ttu-id="ec8b6-207">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="ec8b6-207">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-208">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-208">ACR</span></span>
* <span data-ttu-id="ec8b6-209">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-209">Added ACR Task commands</span></span>
* <span data-ttu-id="ec8b6-210">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-210">Added quick run command</span></span>
* <span data-ttu-id="ec8b6-211">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-211">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="ec8b6-212">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-212">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="ec8b6-213">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-213">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="ec8b6-214">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-214">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-215">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-215">ACS</span></span>
* <span data-ttu-id="ec8b6-216">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-216">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="ec8b6-217">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-217">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-218">AppService</span><span class="sxs-lookup"><span data-stu-id="ec8b6-218">AppService</span></span>

* <span data-ttu-id="ec8b6-219">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-219">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="ec8b6-220">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-220">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="ec8b6-221">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-221">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="ec8b6-222">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-222">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="ec8b6-223">Batch</span><span class="sxs-lookup"><span data-stu-id="ec8b6-223">Batch</span></span>
* <span data-ttu-id="ec8b6-224">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-224">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="ec8b6-225">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-225">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="ec8b6-226">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-226">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="ec8b6-227">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-227">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="ec8b6-228">Batch AI</span><span class="sxs-lookup"><span data-stu-id="ec8b6-228">Batch AI</span></span> 
* <span data-ttu-id="ec8b6-229">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-229">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="ec8b6-230">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="ec8b6-230">Cognitive Services</span></span>
* <span data-ttu-id="ec8b6-231">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-231">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="ec8b6-232">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-232">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="ec8b6-233">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-233">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="ec8b6-234">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-234">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="ec8b6-235">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-235">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="ec8b6-236">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-236">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-237">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-237">Container</span></span>
* <span data-ttu-id="ec8b6-238">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-238">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="ec8b6-239">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-239">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="ec8b6-240">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-240">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="ec8b6-241">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-241">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="ec8b6-242">DataLake</span><span class="sxs-lookup"><span data-stu-id="ec8b6-242">Datalake</span></span>
* <span data-ttu-id="ec8b6-243">仮想ネットワーク ルール用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-243">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="ec8b6-244">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="ec8b6-244">Interactive Shell</span></span>
* <span data-ttu-id="ec8b6-245">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-245">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="ec8b6-246">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-246">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="ec8b6-247">IoT</span><span class="sxs-lookup"><span data-stu-id="ec8b6-247">IoT</span></span>
* <span data-ttu-id="ec8b6-248">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-248">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="ec8b6-249">Key Vault</span><span class="sxs-lookup"><span data-stu-id="ec8b6-249">Key Vault</span></span>
* <span data-ttu-id="ec8b6-250">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-250">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-251">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-251">Network</span></span>
* <span data-ttu-id="ec8b6-252">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-252">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="ec8b6-253">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-253">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="ec8b6-254">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-254">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="ec8b6-255">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-255">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="ec8b6-256">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-256">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="ec8b6-257">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-257">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="ec8b6-258">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-258">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="ec8b6-259">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-259">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="ec8b6-260">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-260">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="ec8b6-261">`network express-route create/update`: `--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-261">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="ec8b6-262">`network vnet subnet create/update`: `--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-262">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="ec8b6-263">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-263">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="ec8b6-264">`network traffic-manager profile create/update`: 監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、`--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-264">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="ec8b6-265">`network lb frontend-ip create/update`: プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-265">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="ec8b6-266">`dns record-set * create/update`: `--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-266">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="ec8b6-267">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-267">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="ec8b6-268">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-268">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="ec8b6-269">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-269">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="ec8b6-270">RDBMS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-270">RDBMS</span></span>
* <span data-ttu-id="ec8b6-271">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-271">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="ec8b6-272">予約</span><span class="sxs-lookup"><span data-stu-id="ec8b6-272">Reservation</span></span>
* <span data-ttu-id="ec8b6-273">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-273">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="ec8b6-274">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-274">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="ec8b6-275">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="ec8b6-275">Manage App</span></span>
* <span data-ttu-id="ec8b6-276">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-276">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="ec8b6-277">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-277">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="ec8b6-278">Role</span><span class="sxs-lookup"><span data-stu-id="ec8b6-278">Role</span></span>
* <span data-ttu-id="ec8b6-279">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-279">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="ec8b6-280">SignalR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-280">SignalR</span></span>
* <span data-ttu-id="ec8b6-281">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-281">First release</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-282">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-282">Storage</span></span>
* <span data-ttu-id="ec8b6-283">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-283">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="ec8b6-284">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-284">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-285">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-285">VM</span></span>
* <span data-ttu-id="ec8b6-286">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-286">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="ec8b6-287">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-287">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="ec8b6-288">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-288">August 28, 2018</span></span>

<span data-ttu-id="ec8b6-289">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="ec8b6-289">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-290">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-290">Core</span></span>

* <span data-ttu-id="ec8b6-291">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-291">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="ec8b6-292">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-292">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-293">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-293">ACR</span></span>

* <span data-ttu-id="ec8b6-294">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-294">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="ec8b6-295">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-295">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-296">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-296">ACS</span></span>

* <span data-ttu-id="ec8b6-297">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-297">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="ec8b6-298">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-298">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-299">AppService</span><span class="sxs-lookup"><span data-stu-id="ec8b6-299">AppService</span></span>

* <span data-ttu-id="ec8b6-300">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-300">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="ec8b6-301">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-301">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="ec8b6-302">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-302">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="ec8b6-303">バックアップ</span><span class="sxs-lookup"><span data-stu-id="ec8b6-303">Backup</span></span>

* <span data-ttu-id="ec8b6-304">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-304">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="ec8b6-305">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="ec8b6-305">Bot Service</span></span>

* <span data-ttu-id="ec8b6-306">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-306">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="ec8b6-307">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="ec8b6-307">Cognitive Services</span></span>

* <span data-ttu-id="ec8b6-308">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-308">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="ec8b6-309">IoT</span><span class="sxs-lookup"><span data-stu-id="ec8b6-309">IoT</span></span>

* <span data-ttu-id="ec8b6-310">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-310">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="ec8b6-311">監視</span><span class="sxs-lookup"><span data-stu-id="ec8b6-311">Monitor</span></span>

* <span data-ttu-id="ec8b6-312">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-312">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="ec8b6-313">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-313">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-314">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-314">Network</span></span>

* <span data-ttu-id="ec8b6-315">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-315">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-316">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-316">Resource</span></span>

* <span data-ttu-id="ec8b6-317">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-317">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-318">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-318">Storage</span></span>

* <span data-ttu-id="ec8b6-319">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-319">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-320">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-320">VM</span></span>

* <span data-ttu-id="ec8b6-321">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-321">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="ec8b6-322">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-322">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="ec8b6-323">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-323">Auguest 14, 2018</span></span>

<span data-ttu-id="ec8b6-324">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="ec8b6-324">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-325">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-325">Core</span></span>

* <span data-ttu-id="ec8b6-326">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-326">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="ec8b6-327">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-327">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="ec8b6-328">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="ec8b6-328">Telemetry</span></span>

* <span data-ttu-id="ec8b6-329">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-329">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-330">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-330">ACR</span></span>

* <span data-ttu-id="ec8b6-331">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-331">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="ec8b6-332">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-332">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-333">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-333">ACS</span></span>

* <span data-ttu-id="ec8b6-334">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-334">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="ec8b6-335">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-335">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="ec8b6-336">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-336">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="ec8b6-337">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-337">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="ec8b6-338">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-338">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="ec8b6-339">AppService</span><span class="sxs-lookup"><span data-stu-id="ec8b6-339">AppService</span></span>

* <span data-ttu-id="ec8b6-340">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-340">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="ec8b6-341">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-341">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="ec8b6-342">BatchAI</span><span class="sxs-lookup"><span data-stu-id="ec8b6-342">BatchAI</span></span>

* <span data-ttu-id="ec8b6-343">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-343">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="ec8b6-344">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-344">Container</span></span>

* <span data-ttu-id="ec8b6-345">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-345">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="ec8b6-346">IoT</span><span class="sxs-lookup"><span data-stu-id="ec8b6-346">IoT</span></span>

* <span data-ttu-id="ec8b6-347">[破壊的変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-347">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="ec8b6-348">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-348">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="ec8b6-349">Iot Central</span><span class="sxs-lookup"><span data-stu-id="ec8b6-349">Iot Central</span></span>

* <span data-ttu-id="ec8b6-350">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-350">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="ec8b6-351">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ec8b6-351">KeyVault</span></span>


* <span data-ttu-id="ec8b6-352">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-352">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="ec8b6-353">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-353">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="ec8b6-354">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-354">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="ec8b6-355">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-355">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="ec8b6-356">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-356">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="ec8b6-357">リレー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-357">Relay</span></span>

* <span data-ttu-id="ec8b6-358">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-358">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-359">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-359">Sql</span></span>

* <span data-ttu-id="ec8b6-360">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-360">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-361">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-361">Storage</span></span>

* <span data-ttu-id="ec8b6-362">[破壊的変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-362">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="ec8b6-363">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-363">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="ec8b6-364">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-364">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="ec8b6-365">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-365">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="ec8b6-366">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-366">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-367">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-367">VM</span></span>

* <span data-ttu-id="ec8b6-368">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-368">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="ec8b6-369">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-369">July 31, 2018</span></span>

<span data-ttu-id="ec8b6-370">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="ec8b6-370">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-371">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-371">ACR</span></span>

* <span data-ttu-id="ec8b6-372">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-372">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="ec8b6-373">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-373">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-374">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-374">ACS</span></span>

* <span data-ttu-id="ec8b6-375">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-375">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="ec8b6-376">Batch</span><span class="sxs-lookup"><span data-stu-id="ec8b6-376">Batch</span></span>

* <span data-ttu-id="ec8b6-377">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-377">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-378">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-378">Container</span></span>

* <span data-ttu-id="ec8b6-379">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-379">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-380">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-380">Network</span></span>

* <span data-ttu-id="ec8b6-381">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-381">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="ec8b6-382">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-382">Resource</span></span>

* <span data-ttu-id="ec8b6-383">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-383">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="ec8b6-384">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-384">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="ec8b6-385">Role</span><span class="sxs-lookup"><span data-stu-id="ec8b6-385">Role</span></span>

* <span data-ttu-id="ec8b6-386">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-386">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="ec8b6-387">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-387">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="ec8b6-388">Search</span><span class="sxs-lookup"><span data-stu-id="ec8b6-388">Search</span></span>

* <span data-ttu-id="ec8b6-389">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-389">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="ec8b6-390">Service Bus</span><span class="sxs-lookup"><span data-stu-id="ec8b6-390">Service Bus</span></span>

* <span data-ttu-id="ec8b6-391">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-391">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="ec8b6-392">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-392">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="ec8b6-393">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="ec8b6-393">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="ec8b6-394">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="ec8b6-394">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-395">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-395">Storage</span></span>

* <span data-ttu-id="ec8b6-396">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-396">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="ec8b6-397">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-397">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-398">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-398">VM</span></span>

* <span data-ttu-id="ec8b6-399">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-399">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="ec8b6-400">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-400">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="ec8b6-401">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-401">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="ec8b6-402">[破壊的変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-402">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="ec8b6-403">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-403">July 18, 2018</span></span>

<span data-ttu-id="ec8b6-404">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="ec8b6-404">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-405">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-405">Core</span></span>

* <span data-ttu-id="ec8b6-406">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-406">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="ec8b6-407">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-407">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="ec8b6-408">[破壊的変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-408">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-409">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-409">ACR</span></span>

* <span data-ttu-id="ec8b6-410">[破壊的変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-410">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="ec8b6-411">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-411">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="ec8b6-412">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-412">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="ec8b6-413">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-413">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-414">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-414">ACS</span></span>

* <span data-ttu-id="ec8b6-415">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-415">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-416">AppService</span><span class="sxs-lookup"><span data-stu-id="ec8b6-416">AppService</span></span>

* <span data-ttu-id="ec8b6-417">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-417">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="ec8b6-418">Batch</span><span class="sxs-lookup"><span data-stu-id="ec8b6-418">Batch</span></span>

* <span data-ttu-id="ec8b6-419">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-419">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="ec8b6-420">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-420">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="ec8b6-421">Batch AI</span><span class="sxs-lookup"><span data-stu-id="ec8b6-421">Batch AI</span></span>

* <span data-ttu-id="ec8b6-422">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-422">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-423">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-423">Container</span></span>

* <span data-ttu-id="ec8b6-424">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-424">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="ec8b6-425">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-425">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-426">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-426">Network</span></span>

* <span data-ttu-id="ec8b6-427">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-427">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="ec8b6-428">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-428">Added `network nic wait`</span></span>
* <span data-ttu-id="ec8b6-429">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-429">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="ec8b6-430">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-430">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="ec8b6-431">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-431">Resource</span></span>

* <span data-ttu-id="ec8b6-432">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-432">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="ec8b6-433">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-433">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="ec8b6-434">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-434">Added `deployment wait` command</span></span>
* <span data-ttu-id="ec8b6-435">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-435">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-436">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-436">SQL</span></span>

* <span data-ttu-id="ec8b6-437">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-437">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="ec8b6-438">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-438">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="ec8b6-439">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-439">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-440">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-440">Storage</span></span>

* <span data-ttu-id="ec8b6-441">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-441">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-442">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-442">VM</span></span>

* <span data-ttu-id="ec8b6-443">[破壊的変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-443">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="ec8b6-444">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-444">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="ec8b6-445">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-445">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="ec8b6-446">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-446">July 3, 2018</span></span>

<span data-ttu-id="ec8b6-447">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="ec8b6-447">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="ec8b6-448">AKS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-448">AKS</span></span>

* <span data-ttu-id="ec8b6-449">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-449">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="ec8b6-450">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-450">July 3, 2018</span></span>

<span data-ttu-id="ec8b6-451">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="ec8b6-451">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-452">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-452">Core</span></span>

* <span data-ttu-id="ec8b6-453">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-453">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-454">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-454">ACR</span></span>

* <span data-ttu-id="ec8b6-455">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-455">Added polling build status</span></span>
* <span data-ttu-id="ec8b6-456">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-456">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="ec8b6-457">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-457">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-458">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-458">ACS</span></span>

* <span data-ttu-id="ec8b6-459">[破壊的変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-459">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="ec8b6-460">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-460">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="ec8b6-461">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-461">Updated options for `aks browse` command.</span></span> <span data-ttu-id="ec8b6-462">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-462">Added `--listen-port` support</span></span>
* <span data-ttu-id="ec8b6-463">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-463">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="ec8b6-464">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-464">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="ec8b6-465">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-465">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-466">AppService</span><span class="sxs-lookup"><span data-stu-id="ec8b6-466">AppService</span></span>

* <span data-ttu-id="ec8b6-467">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-467">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="ec8b6-468">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-468">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="ec8b6-469">バックアップ</span><span class="sxs-lookup"><span data-stu-id="ec8b6-469">Backup</span></span>

* <span data-ttu-id="ec8b6-470">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-470">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="ec8b6-471">BatchAI</span><span class="sxs-lookup"><span data-stu-id="ec8b6-471">BatchAI</span></span>

* <span data-ttu-id="ec8b6-472">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-472">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="ec8b6-473">クラウド</span><span class="sxs-lookup"><span data-stu-id="ec8b6-473">Cloud</span></span>

* <span data-ttu-id="ec8b6-474">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-474">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-475">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-475">Container</span></span>

* <span data-ttu-id="ec8b6-476">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-476">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="ec8b6-477">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-477">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="ec8b6-478">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-478">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="ec8b6-479">内線番号</span><span class="sxs-lookup"><span data-stu-id="ec8b6-479">Extension</span></span>

* <span data-ttu-id="ec8b6-480">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-480">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-481">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-481">Network</span></span>

* <span data-ttu-id="ec8b6-482">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-482">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="ec8b6-483">Rdbms</span><span class="sxs-lookup"><span data-stu-id="ec8b6-483">Rdbms</span></span>

* <span data-ttu-id="ec8b6-484">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-484">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-485">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-485">Resource</span></span>

* <span data-ttu-id="ec8b6-486">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-486">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-487">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-487">VM</span></span>

* <span data-ttu-id="ec8b6-488">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-488">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="ec8b6-489">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-489">June 25, 2018</span></span>

<span data-ttu-id="ec8b6-490">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="ec8b6-490">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="ec8b6-491">CLI</span><span class="sxs-lookup"><span data-stu-id="ec8b6-491">CLI</span></span>

* <span data-ttu-id="ec8b6-492">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-492">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="ec8b6-493">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-493">June 19, 2018</span></span>

<span data-ttu-id="ec8b6-494">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="ec8b6-494">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-495">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-495">Core</span></span>

* <span data-ttu-id="ec8b6-496">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-496">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-497">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-497">ACR</span></span>

* <span data-ttu-id="ec8b6-498">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-498">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="ec8b6-499">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-499">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-500">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-500">ACS</span></span>

* <span data-ttu-id="ec8b6-501">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-501">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="ec8b6-502">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-502">Added `--update` support</span></span>
* <span data-ttu-id="ec8b6-503">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-503">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="ec8b6-504">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-504">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="ec8b6-505">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-505">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="ec8b6-506">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-506">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="ec8b6-507">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-507">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="ec8b6-508">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-508">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-509">AppService</span><span class="sxs-lookup"><span data-stu-id="ec8b6-509">AppService</span></span>

* <span data-ttu-id="ec8b6-510">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-510">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="ec8b6-511">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-511">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="ec8b6-512">Batch</span><span class="sxs-lookup"><span data-stu-id="ec8b6-512">Batch</span></span>

* <span data-ttu-id="ec8b6-513">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-513">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="ec8b6-514">Batch AI</span><span class="sxs-lookup"><span data-stu-id="ec8b6-514">Batch AI</span></span>

* <span data-ttu-id="ec8b6-515">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-515">Added support for workspaces.</span></span> <span data-ttu-id="ec8b6-516">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="ec8b6-516">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="ec8b6-517">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-517">Added support for experiments.</span></span> <span data-ttu-id="ec8b6-518">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="ec8b6-518">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="ec8b6-519">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-519">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="ec8b6-520">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-520">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="ec8b6-521">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-521">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="ec8b6-522">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-522">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="ec8b6-523">[破壊的変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="ec8b6-523">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="ec8b6-524">[破壊的変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="ec8b6-524">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="ec8b6-525">[破壊的変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-525">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="ec8b6-526">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-526">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="ec8b6-527">[破壊的変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-527">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="ec8b6-528">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-528">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="ec8b6-529">[破壊的変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-529">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="ec8b6-530">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-530">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="ec8b6-531">[破壊的変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-531">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="ec8b6-532">[破壊的変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-532">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="ec8b6-533">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-533">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="ec8b6-534">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-534">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="ec8b6-535">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-535">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="ec8b6-536">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-536">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="ec8b6-537">マップ</span><span class="sxs-lookup"><span data-stu-id="ec8b6-537">Maps</span></span>

* <span data-ttu-id="ec8b6-538">[破壊的変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-538">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-539">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-539">Network</span></span>

* <span data-ttu-id="ec8b6-540">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-540">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="ec8b6-541">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-541">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="ec8b6-542">#6502</span><span class="sxs-lookup"><span data-stu-id="ec8b6-542">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="ec8b6-543">Reservations</span><span class="sxs-lookup"><span data-stu-id="ec8b6-543">Reservations</span></span>

* <span data-ttu-id="ec8b6-544">[破壊的変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-544">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="ec8b6-545">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-545">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="ec8b6-546">[破壊的変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-546">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="ec8b6-547">[破壊的変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-547">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="ec8b6-548">[破壊的変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-548">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="ec8b6-549">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-549">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="ec8b6-550">Role</span><span class="sxs-lookup"><span data-stu-id="ec8b6-550">Role</span></span>

* <span data-ttu-id="ec8b6-551">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-551">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-552">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-552">SQL</span></span>

* <span data-ttu-id="ec8b6-553">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-553">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-554">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-554">Storage</span></span>

* <span data-ttu-id="ec8b6-555">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-555">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-556">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-556">VM</span></span>

* <span data-ttu-id="ec8b6-557">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-557">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="ec8b6-558">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-558">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="ec8b6-559">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-559">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="ec8b6-560">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-560">June 13, 2018</span></span>

<span data-ttu-id="ec8b6-561">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="ec8b6-561">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-562">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-562">Core</span></span>

* <span data-ttu-id="ec8b6-563">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-563">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="ec8b6-564">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-564">June 13, 2018</span></span>

<span data-ttu-id="ec8b6-565">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="ec8b6-565">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="ec8b6-566">AKS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-566">AKS</span></span>

* <span data-ttu-id="ec8b6-567">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-567">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="ec8b6-568">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-568">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="ec8b6-569">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-569">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="ec8b6-570">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-570">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="ec8b6-571">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-571">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-572">AppService</span><span class="sxs-lookup"><span data-stu-id="ec8b6-572">AppService</span></span>

* <span data-ttu-id="ec8b6-573">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-573">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="ec8b6-574">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-574">June 5, 2018</span></span>

<span data-ttu-id="ec8b6-575">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="ec8b6-575">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="ec8b6-576">Interactive</span><span class="sxs-lookup"><span data-stu-id="ec8b6-576">Interactive</span></span>

* <span data-ttu-id="ec8b6-577">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-577">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="ec8b6-578">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-578">June 5, 2018</span></span>

<span data-ttu-id="ec8b6-579">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="ec8b6-579">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-580">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-580">Core</span></span>

* <span data-ttu-id="ec8b6-581">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-581">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="ec8b6-582">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-582">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-583">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-583">ACR</span></span>

* <span data-ttu-id="ec8b6-584">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-584">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="ec8b6-585">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-585">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="ec8b6-586">AKS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-586">AKS</span></span>

* <span data-ttu-id="ec8b6-587">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-587">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="ec8b6-588">Batch</span><span class="sxs-lookup"><span data-stu-id="ec8b6-588">Batch</span></span>

* <span data-ttu-id="ec8b6-589">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-589">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="ec8b6-590">IoT</span><span class="sxs-lookup"><span data-stu-id="ec8b6-590">IOT</span></span>

* <span data-ttu-id="ec8b6-591">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-591">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-592">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-592">Network</span></span>

* <span data-ttu-id="ec8b6-593">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-593">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="ec8b6-594">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="ec8b6-594">Policy Insights</span></span>

* <span data-ttu-id="ec8b6-595">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-595">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="ec8b6-596">ARM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-596">ARM</span></span>

* <span data-ttu-id="ec8b6-597">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-597">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-598">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-598">SQL</span></span>

* <span data-ttu-id="ec8b6-599">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-599">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="ec8b6-600">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-600">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="ec8b6-601">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-601">Storage</span></span>

* <span data-ttu-id="ec8b6-602">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-602">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-603">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-603">VM</span></span>

* <span data-ttu-id="ec8b6-604">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-604">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="ec8b6-605">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-605">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="ec8b6-606">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-606">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="ec8b6-607">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-607">May 22, 2018</span></span>

<span data-ttu-id="ec8b6-608">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="ec8b6-608">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-609">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-609">Core</span></span>

* <span data-ttu-id="ec8b6-610">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-610">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-611">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-611">ACS</span></span>

* <span data-ttu-id="ec8b6-612">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-612">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="ec8b6-613">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-613">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-614">AppService</span><span class="sxs-lookup"><span data-stu-id="ec8b6-614">AppService</span></span>

* <span data-ttu-id="ec8b6-615">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-615">Improved generic update commands</span></span>
* <span data-ttu-id="ec8b6-616">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-616">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-617">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-617">Container</span></span>

* <span data-ttu-id="ec8b6-618">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-618">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="ec8b6-619">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-619">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="ec8b6-620">内線番号</span><span class="sxs-lookup"><span data-stu-id="ec8b6-620">Extension</span></span>

* <span data-ttu-id="ec8b6-621">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-621">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="ec8b6-622">Interactive</span><span class="sxs-lookup"><span data-stu-id="ec8b6-622">Interactive</span></span>

* <span data-ttu-id="ec8b6-623">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-623">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="ec8b6-624">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-624">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="ec8b6-625">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ec8b6-625">KeyVault</span></span>

* <span data-ttu-id="ec8b6-626">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-626">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-627">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-627">Network</span></span>

* <span data-ttu-id="ec8b6-628">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-628">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="ec8b6-629">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-629">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-630">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-630">SQL</span></span>

* <span data-ttu-id="ec8b6-631">[破壊的変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-631">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="ec8b6-632">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-632">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="ec8b6-633">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-633">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="ec8b6-634">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-634">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="ec8b6-635">[破壊的変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-635">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="ec8b6-636">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="ec8b6-636">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="ec8b6-637">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-637">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="ec8b6-638">`edition`</span><span class="sxs-lookup"><span data-stu-id="ec8b6-638">`edition`.</span></span> <span data-ttu-id="ec8b6-639">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-639">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="ec8b6-640">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="ec8b6-640">`elasticPoolName`.</span></span> <span data-ttu-id="ec8b6-641">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-641">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="ec8b6-642">[破壊的変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-642">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="ec8b6-643">`edition`</span><span class="sxs-lookup"><span data-stu-id="ec8b6-643">`edition`.</span></span> <span data-ttu-id="ec8b6-644">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-644">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="ec8b6-645">`dtu`</span><span class="sxs-lookup"><span data-stu-id="ec8b6-645">`dtu`.</span></span> <span data-ttu-id="ec8b6-646">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-646">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="ec8b6-647">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="ec8b6-647">`databaseDtuMin`.</span></span> <span data-ttu-id="ec8b6-648">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-648">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="ec8b6-649">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="ec8b6-649">`databaseDtuMax`.</span></span> <span data-ttu-id="ec8b6-650">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-650">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="ec8b6-651">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-651">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="ec8b6-652">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-652">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-653">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-653">Storage</span></span>

* <span data-ttu-id="ec8b6-654">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-654">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="ec8b6-655">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-655">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-656">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-656">VM</span></span>

* <span data-ttu-id="ec8b6-657">[破壊的変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-657">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="ec8b6-658">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-658">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="ec8b6-659">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-659">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="ec8b6-660">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-660">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="ec8b6-661">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-661">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="ec8b6-662">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-662">May 7, 2018</span></span>

<span data-ttu-id="ec8b6-663">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="ec8b6-663">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-664">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-664">Core</span></span>

* <span data-ttu-id="ec8b6-665">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-665">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="ec8b6-666">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-666">Added limited support for positional arguments</span></span>
* <span data-ttu-id="ec8b6-667">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-667">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="ec8b6-668">#5591</span><span class="sxs-lookup"><span data-stu-id="ec8b6-668">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="ec8b6-669">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-669">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="ec8b6-670">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-670">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="ec8b6-671">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-671">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="ec8b6-672">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-672">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="ec8b6-673">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-673">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-674">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-674">ACR</span></span>

* <span data-ttu-id="ec8b6-675">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-675">Added ACR Build commands</span></span>
* <span data-ttu-id="ec8b6-676">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-676">Improved resource not found error messages</span></span>
* <span data-ttu-id="ec8b6-677">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-677">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="ec8b6-678">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-678">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="ec8b6-679">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-679">Improved repository commands error messages</span></span>
* <span data-ttu-id="ec8b6-680">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-680">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-681">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-681">ACS</span></span>

* <span data-ttu-id="ec8b6-682">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-682">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="ec8b6-683">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-683">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="ec8b6-684">AMS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-684">AMS</span></span>

* <span data-ttu-id="ec8b6-685">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="ec8b6-685">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-686">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-686">Appservice</span></span>

* <span data-ttu-id="ec8b6-687">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-687">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="ec8b6-688">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-688">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="ec8b6-689">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-689">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="ec8b6-690">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-690">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="ec8b6-691">Batch AI</span><span class="sxs-lookup"><span data-stu-id="ec8b6-691">Batch AI</span></span>

* <span data-ttu-id="ec8b6-692">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-692">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="ec8b6-693">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="ec8b6-693">Cognitive Services</span></span>

* <span data-ttu-id="ec8b6-694">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-694">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="ec8b6-695">消費</span><span class="sxs-lookup"><span data-stu-id="ec8b6-695">Consumption</span></span>

* <span data-ttu-id="ec8b6-696">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-696">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-697">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-697">Container</span></span>

* <span data-ttu-id="ec8b6-698">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-698">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="ec8b6-699">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ec8b6-699">Cosmos DB</span></span>

* <span data-ttu-id="ec8b6-700">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-700">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="ec8b6-701">DMS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-701">DMS</span></span>

* <span data-ttu-id="ec8b6-702">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-702">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="ec8b6-703">内線番号</span><span class="sxs-lookup"><span data-stu-id="ec8b6-703">Extension</span></span>

* <span data-ttu-id="ec8b6-704">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-704">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="ec8b6-705">Interactive</span><span class="sxs-lookup"><span data-stu-id="ec8b6-705">Interactive</span></span>

* <span data-ttu-id="ec8b6-706">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-706">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="ec8b6-707">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-707">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="ec8b6-708">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-708">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="ec8b6-709">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-709">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="ec8b6-710">ラボ</span><span class="sxs-lookup"><span data-stu-id="ec8b6-710">Lab</span></span>

* <span data-ttu-id="ec8b6-711">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-711">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-712">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-712">Network</span></span>

* <span data-ttu-id="ec8b6-713">[破壊的変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-713">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="ec8b6-714">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ec8b6-714">Profile</span></span>

* <span data-ttu-id="ec8b6-715">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-715">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="ec8b6-716">[破壊的変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-716">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="ec8b6-717">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-717">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="ec8b6-718">Redis</span><span class="sxs-lookup"><span data-stu-id="ec8b6-718">Redis</span></span>

* <span data-ttu-id="ec8b6-719">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-719">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="ec8b6-720">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-720">Deprecated `redis list-all`.</span></span> <span data-ttu-id="ec8b6-721">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-721">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="ec8b6-722">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-722">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="ec8b6-723">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-723">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="ec8b6-724">Role</span><span class="sxs-lookup"><span data-stu-id="ec8b6-724">Role</span></span>

* <span data-ttu-id="ec8b6-725">[破壊的変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-725">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-726">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-726">Storage</span></span>

* <span data-ttu-id="ec8b6-727">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-727">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="ec8b6-728">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-728">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="ec8b6-729">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="ec8b6-729">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="ec8b6-730">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-730">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="ec8b6-731">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-731">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-732">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-732">VM</span></span>

* <span data-ttu-id="ec8b6-733">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-733">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="ec8b6-734">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-734">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="ec8b6-735">[破壊的変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="ec8b6-735">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="ec8b6-736">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-736">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="ec8b6-737">[破壊的変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-737">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="ec8b6-738">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-738">Added write accelerator support</span></span>
* <span data-ttu-id="ec8b6-739">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-739">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="ec8b6-740">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-740">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="ec8b6-741">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-741">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="ec8b6-742">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-742">April 10, 2018</span></span>

<span data-ttu-id="ec8b6-743">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="ec8b6-743">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-744">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-744">ACR</span></span>

* <span data-ttu-id="ec8b6-745">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-745">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-746">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-746">ACS</span></span>

* <span data-ttu-id="ec8b6-747">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-747">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-748">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-748">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="ec8b6-750">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-750">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="ec8b6-751">BatchAI</span><span class="sxs-lookup"><span data-stu-id="ec8b6-751">BatchAI</span></span>

* <span data-ttu-id="ec8b6-752">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-752">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="ec8b6-753">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="ec8b6-753">Job level mounting</span></span>
  - <span data-ttu-id="ec8b6-754">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="ec8b6-754">Environment variables with secret values</span></span>
  - <span data-ttu-id="ec8b6-755">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="ec8b6-755">Performance counters settings</span></span>
  - <span data-ttu-id="ec8b6-756">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="ec8b6-756">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="ec8b6-757">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="ec8b6-757">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="ec8b6-758">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="ec8b6-758">Usage and limits reporting</span></span>
  - <span data-ttu-id="ec8b6-759">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="ec8b6-759">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="ec8b6-760">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="ec8b6-760">Support for custom images</span></span>
  - <span data-ttu-id="ec8b6-761">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-761">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="ec8b6-762">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-762">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="ec8b6-763">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-763">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="ec8b6-764">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="ec8b6-764">National clouds are supported</span></span>
* <span data-ttu-id="ec8b6-765">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-765">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="ec8b6-766">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-766">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="ec8b6-767">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-767">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="ec8b6-768">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-768">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="ec8b6-769">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-769">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="ec8b6-770">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-770">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="ec8b6-771">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-771">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="ec8b6-772">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-772">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="ec8b6-773">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="ec8b6-773">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="ec8b6-774">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-774">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="ec8b6-775">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-775">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="ec8b6-776">[破壊的変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-776">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="ec8b6-777">[破壊的変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-777">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="ec8b6-778">課金</span><span class="sxs-lookup"><span data-stu-id="ec8b6-778">Billing</span></span>

* <span data-ttu-id="ec8b6-779">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-779">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="ec8b6-780">消費</span><span class="sxs-lookup"><span data-stu-id="ec8b6-780">Consumption</span></span>

* <span data-ttu-id="ec8b6-781">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-781">Added `marketplace` commands</span></span>
* <span data-ttu-id="ec8b6-782">[破壊的変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-782">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="ec8b6-783">[破壊的変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-783">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="ec8b6-784">[破壊的変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-784">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="ec8b6-785">[破壊的変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-785">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="ec8b6-786">[破壊的変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-786">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-787">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-787">Container</span></span>

* <span data-ttu-id="ec8b6-788">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-788">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="ec8b6-789">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-789">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="ec8b6-790">内線番号</span><span class="sxs-lookup"><span data-stu-id="ec8b6-790">Extension</span></span>

* <span data-ttu-id="ec8b6-791">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-791">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="ec8b6-792">Interactive</span><span class="sxs-lookup"><span data-stu-id="ec8b6-792">Interactive</span></span>

* <span data-ttu-id="ec8b6-793">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-793">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="ec8b6-794">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-794">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="ec8b6-795">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-795">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-796">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-796">Network</span></span>

* <span data-ttu-id="ec8b6-797">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-797">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="ec8b6-798">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-798">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="ec8b6-799">#4910</span><span class="sxs-lookup"><span data-stu-id="ec8b6-799">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="ec8b6-800">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-800">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="ec8b6-801">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-801">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="ec8b6-802">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-802">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="ec8b6-803">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-803">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="ec8b6-804">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-804">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="ec8b6-805">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ec8b6-805">Profile</span></span>

* <span data-ttu-id="ec8b6-806">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-806">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="ec8b6-807">[破壊的変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-807">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="ec8b6-808">RDBMS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-808">RDBMS</span></span>

* <span data-ttu-id="ec8b6-809">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-809">Added `georestore` command</span></span>
* <span data-ttu-id="ec8b6-810">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-810">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-811">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-811">Resource</span></span>

* <span data-ttu-id="ec8b6-812">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-812">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="ec8b6-813">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-813">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-814">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-814">SQL</span></span>

* <span data-ttu-id="ec8b6-815">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-815">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-816">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-816">Storage</span></span>

* <span data-ttu-id="ec8b6-817">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-817">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-818">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-818">VM</span></span>

* <span data-ttu-id="ec8b6-819">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-819">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="ec8b6-820">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-820">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [重大な変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="ec8b6-822">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-822">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="ec8b6-823">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-823">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="ec8b6-824">#5718</span><span class="sxs-lookup"><span data-stu-id="ec8b6-824">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="ec8b6-825">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-825">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="ec8b6-826">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-826">March 27, 2018</span></span>

<span data-ttu-id="ec8b6-827">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="ec8b6-827">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-828">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-828">Core</span></span>

* <span data-ttu-id="ec8b6-829">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-829">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-830">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-830">ACS</span></span>

* <span data-ttu-id="ec8b6-831">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-831">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-832">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-832">Appservice</span></span>

* <span data-ttu-id="ec8b6-833">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-833">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="ec8b6-834">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-834">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="ec8b6-835">バックアップ</span><span class="sxs-lookup"><span data-stu-id="ec8b6-835">Backup</span></span>

* <span data-ttu-id="ec8b6-836">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-836">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="ec8b6-837">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-837">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="ec8b6-838">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-838">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="ec8b6-839">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-839">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-840">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-840">Container</span></span>

* <span data-ttu-id="ec8b6-841">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-841">Added `container exec` command.</span></span> <span data-ttu-id="ec8b6-842">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-842">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="ec8b6-843">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-843">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="ec8b6-844">内線番号</span><span class="sxs-lookup"><span data-stu-id="ec8b6-844">Extension</span></span>

* <span data-ttu-id="ec8b6-845">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-845">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="ec8b6-846">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-846">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="ec8b6-847">[破壊的変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-847">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="ec8b6-848">Interactive</span><span class="sxs-lookup"><span data-stu-id="ec8b6-848">Interactive</span></span>

* <span data-ttu-id="ec8b6-849">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-849">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="ec8b6-850">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-850">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="ec8b6-851">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-851">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="ec8b6-852">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-852">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="ec8b6-853">ラボ</span><span class="sxs-lookup"><span data-stu-id="ec8b6-853">Lab</span></span>

* <span data-ttu-id="ec8b6-854">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-854">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="ec8b6-855">監視</span><span class="sxs-lookup"><span data-stu-id="ec8b6-855">Monitor</span></span>

* <span data-ttu-id="ec8b6-856">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-856">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="ec8b6-857">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました: `metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-857">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="ec8b6-858">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-858">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-859">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-859">Network</span></span>

* <span data-ttu-id="ec8b6-860">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-860">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="ec8b6-861">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ec8b6-861">Profile</span></span>

* <span data-ttu-id="ec8b6-862">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-862">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="ec8b6-863">RDBMS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-863">RDBMS</span></span>

* <span data-ttu-id="ec8b6-864">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-864">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-865">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-865">Resource</span></span>

* [重大な変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="ec8b6-867">Role</span><span class="sxs-lookup"><span data-stu-id="ec8b6-867">Role</span></span>

* <span data-ttu-id="ec8b6-868">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-868">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="ec8b6-869">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-869">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="ec8b6-870">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-870">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="ec8b6-871">[破壊的変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-871">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="ec8b6-872">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-872">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-873">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-873">Storage</span></span>

* <span data-ttu-id="ec8b6-874">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-874">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="ec8b6-875">[#4049](https://github.com/Azure/azure-cli/issues/4049) (追加 BLOB のアップロードで条件のパラメーターが無視される問題) を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-875">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-876">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-876">VM</span></span>

* <span data-ttu-id="ec8b6-877">インスタンス数が 100 を超えるセットに対する今後の重大な変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-877">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="ec8b6-878">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-878">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="ec8b6-879">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-879">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="ec8b6-880">[破壊的変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-880">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="ec8b6-881">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-881">March 13, 2018</span></span>

<span data-ttu-id="ec8b6-882">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="ec8b6-882">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-883">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-883">ACR</span></span>

* <span data-ttu-id="ec8b6-884">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-884">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="ec8b6-885">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-885">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="ec8b6-886">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-886">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-887">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-887">ACS</span></span>

* <span data-ttu-id="ec8b6-888">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-888">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="ec8b6-889">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-889">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="ec8b6-890">Advisor</span><span class="sxs-lookup"><span data-stu-id="ec8b6-890">Advisor</span></span>

* <span data-ttu-id="ec8b6-891">[破壊的変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-891">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="ec8b6-892">[破壊的変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-892">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="ec8b6-893">[破壊的変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-893">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="ec8b6-894">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-894">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="ec8b6-895">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-895">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-896">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-896">Appservice</span></span>

* <span data-ttu-id="ec8b6-897">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-897">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="ec8b6-898">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-898">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="ec8b6-899">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="ec8b6-899">Eventhubs</span></span>

* <span data-ttu-id="ec8b6-900">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-900">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="ec8b6-901">内線番号</span><span class="sxs-lookup"><span data-stu-id="ec8b6-901">Extension</span></span>

* <span data-ttu-id="ec8b6-902">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-902">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="ec8b6-903">Interactive</span><span class="sxs-lookup"><span data-stu-id="ec8b6-903">Interactive</span></span>

* <span data-ttu-id="ec8b6-904">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました: 異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-904">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="ec8b6-905">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました: スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="ec8b6-905">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="ec8b6-906">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました: コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="ec8b6-906">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="ec8b6-907">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-907">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="ec8b6-908">監視</span><span class="sxs-lookup"><span data-stu-id="ec8b6-908">Monitor</span></span>

* <span data-ttu-id="ec8b6-909">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-909">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="ec8b6-910">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-910">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="ec8b6-911">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-911">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="ec8b6-912">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-912">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-913">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-913">Network</span></span>

* <span data-ttu-id="ec8b6-914">[破壊的変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-914">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="ec8b6-915">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-915">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="ec8b6-916">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-916">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="ec8b6-917">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-917">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="ec8b6-918">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ec8b6-918">Profile</span></span>

* <span data-ttu-id="ec8b6-919">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-919">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="ec8b6-920">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-920">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="ec8b6-921">RDBMS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-921">RDBMS</span></span>

* <span data-ttu-id="ec8b6-922">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-922">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="ec8b6-923">Service Bus</span><span class="sxs-lookup"><span data-stu-id="ec8b6-923">Service Bus</span></span>

* <span data-ttu-id="ec8b6-924">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-924">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-925">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-925">Storage</span></span>

* <span data-ttu-id="ec8b6-926">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-926">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="ec8b6-927">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました: Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-927">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-928">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-928">VM</span></span>

* <span data-ttu-id="ec8b6-929">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-929">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="ec8b6-930">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-930">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="ec8b6-931">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-931">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="ec8b6-932">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-932">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="ec8b6-933">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-933">February 27, 2018</span></span>

<span data-ttu-id="ec8b6-934">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="ec8b6-934">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-935">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-935">Core</span></span>

* <span data-ttu-id="ec8b6-936">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正: Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="ec8b6-936">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="ec8b6-937">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-937">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="ec8b6-938">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-938">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-939">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-939">ACS</span></span>

* <span data-ttu-id="ec8b6-940">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-940">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="ec8b6-941">修正された問題: ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="ec8b6-941">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="ec8b6-942">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-942">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="ec8b6-943">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-943">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-944">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-944">Appservice</span></span>

* <span data-ttu-id="ec8b6-945">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="ec8b6-945">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="ec8b6-946">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="ec8b6-946">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="ec8b6-947">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="ec8b6-947">Cognitive Services</span></span>

* <span data-ttu-id="ec8b6-948">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-948">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="ec8b6-949">消費</span><span class="sxs-lookup"><span data-stu-id="ec8b6-949">Consumption</span></span>

* <span data-ttu-id="ec8b6-950">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-950">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="ec8b6-951">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-951">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-952">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-952">Container</span></span>

* <span data-ttu-id="ec8b6-953">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-953">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-954">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-954">Network</span></span>

* <span data-ttu-id="ec8b6-955">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正: `network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="ec8b6-955">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-956">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-956">Resource</span></span>

* <span data-ttu-id="ec8b6-957">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-957">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="ec8b6-958">Role</span><span class="sxs-lookup"><span data-stu-id="ec8b6-958">Role</span></span>

* <span data-ttu-id="ec8b6-959">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-959">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-960">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-960">SQL</span></span>

* <span data-ttu-id="ec8b6-961">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-961">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-962">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-962">Storage</span></span>

* <span data-ttu-id="ec8b6-963">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-963">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-964">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-964">VM</span></span>

* <span data-ttu-id="ec8b6-965">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-965">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="ec8b6-966">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-966">February 13, 2018</span></span>

<span data-ttu-id="ec8b6-967">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="ec8b6-967">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-968">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-968">Core</span></span>

* <span data-ttu-id="ec8b6-969">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-969">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-970">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-970">ACS</span></span>

* <span data-ttu-id="ec8b6-971">[破壊的変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-971">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="ec8b6-972">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-972">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="ec8b6-973">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-973">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="ec8b6-974">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-974">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="ec8b6-975">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-975">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="ec8b6-976">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-976">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="ec8b6-977">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-977">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="ec8b6-978">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-978">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-979">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-979">Appservice</span></span>

* <span data-ttu-id="ec8b6-980">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-980">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="ec8b6-981">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-981">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="ec8b6-982">CDN</span><span class="sxs-lookup"><span data-stu-id="ec8b6-982">CDN</span></span>

* <span data-ttu-id="ec8b6-983">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-983">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-984">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-984">Container</span></span>

* <span data-ttu-id="ec8b6-985">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-985">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="ec8b6-986">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-986">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ec8b6-987">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ec8b6-987">CosmosDB</span></span>

* <span data-ttu-id="ec8b6-988">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-988">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="ec8b6-989">内線番号</span><span class="sxs-lookup"><span data-stu-id="ec8b6-989">Extension</span></span>

* <span data-ttu-id="ec8b6-990">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-990">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="ec8b6-991">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-991">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="ec8b6-992">フィードバック</span><span class="sxs-lookup"><span data-stu-id="ec8b6-992">Feedback</span></span>

* <span data-ttu-id="ec8b6-993">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-993">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="ec8b6-994">Interactive</span><span class="sxs-lookup"><span data-stu-id="ec8b6-994">Interactive</span></span>

* <span data-ttu-id="ec8b6-995">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-995">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="ec8b6-996">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-996">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="ec8b6-997">IoT</span><span class="sxs-lookup"><span data-stu-id="ec8b6-997">IoT</span></span>

* <span data-ttu-id="ec8b6-998">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-998">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="ec8b6-999">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-999">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="ec8b6-1000">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1000">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="ec8b6-1001">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1001">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="ec8b6-1002">監視</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1002">Monitor</span></span>

* <span data-ttu-id="ec8b6-1003">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1003">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-1004">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1004">Network</span></span>

* <span data-ttu-id="ec8b6-1005">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1005">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="ec8b6-1006">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1006">Profile</span></span>

* <span data-ttu-id="ec8b6-1007">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1007">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-1008">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1008">Resource</span></span>

* <span data-ttu-id="ec8b6-1009">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1009">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="ec8b6-1010">Role</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1010">Role</span></span>

* <span data-ttu-id="ec8b6-1011">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1011">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-1012">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1012">SQL</span></span>

* <span data-ttu-id="ec8b6-1013">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1013">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="ec8b6-1014">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1014">Added `sql db rename`</span></span>
* <span data-ttu-id="ec8b6-1015">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1015">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-1016">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1016">Storage</span></span>

* <span data-ttu-id="ec8b6-1017">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1017">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1018">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1018">VM</span></span>

* <span data-ttu-id="ec8b6-1019">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1019">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="ec8b6-1020">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1020">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="ec8b6-1021">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1021">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="ec8b6-1022">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1022">January 31, 2018</span></span>

<span data-ttu-id="ec8b6-1023">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1023">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-1024">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1024">Core</span></span>

* <span data-ttu-id="ec8b6-1025">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1025">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="ec8b6-1026">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1026">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="ec8b6-1027">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1027">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="ec8b6-1028">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1028">Use `--verbose` to see</span></span>
* <span data-ttu-id="ec8b6-1029">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1029">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-1030">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1030">ACS</span></span>

* <span data-ttu-id="ec8b6-1031">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1031">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="ec8b6-1032">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1032">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-1033">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1033">Appservice</span></span>

* <span data-ttu-id="ec8b6-1034">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1034">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="ec8b6-1035">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1035">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="ec8b6-1036">CDN</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1036">CDN</span></span>

* <span data-ttu-id="ec8b6-1037">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1037">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ec8b6-1038">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1038">CosmosDB</span></span>

* <span data-ttu-id="ec8b6-1039">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1039">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="ec8b6-1040">Interactive</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1040">Interactive</span></span>

* <span data-ttu-id="ec8b6-1041">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1041">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-1042">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1042">Network</span></span>

* <span data-ttu-id="ec8b6-1043">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1043">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="ec8b6-1044">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1044">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="ec8b6-1045">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1045">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="ec8b6-1046">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1046">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="ec8b6-1047">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1047">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="ec8b6-1048">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1048">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="ec8b6-1049">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1049">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="ec8b6-1050">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1050">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="ec8b6-1051">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1051">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="ec8b6-1052">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1052">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="ec8b6-1053">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1053">Profile</span></span>

* <span data-ttu-id="ec8b6-1054">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1054">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-1055">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1055">Resource</span></span>

* <span data-ttu-id="ec8b6-1056">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1056">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-1057">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1057">Storage</span></span>

* <span data-ttu-id="ec8b6-1058">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1058">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="ec8b6-1059">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1059">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="ec8b6-1060">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1060">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="ec8b6-1061">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1061">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="ec8b6-1062">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1062">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1063">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1063">VM</span></span>

* <span data-ttu-id="ec8b6-1064">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1064">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="ec8b6-1065">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1065">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="ec8b6-1066">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1066">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="ec8b6-1067">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1067">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="ec8b6-1068">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1068">January 17, 2018</span></span>

<span data-ttu-id="ec8b6-1069">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1069">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-1070">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1070">ACR</span></span>

* <span data-ttu-id="ec8b6-1071">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1071">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="ec8b6-1072">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1072">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-1073">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1073">ACS</span></span>

* <span data-ttu-id="ec8b6-1074">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1074">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="ec8b6-1075">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1075">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-1076">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1076">Appservice</span></span>

* <span data-ttu-id="ec8b6-1077">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1077">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="ec8b6-1078">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1078">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="ec8b6-1079">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1079">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="ec8b6-1080">バックアップ</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1080">Backup</span></span>

* <span data-ttu-id="ec8b6-1081">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1081">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="ec8b6-1082">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1082">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="ec8b6-1083">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1083">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="ec8b6-1084">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1084">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="ec8b6-1085">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1085">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="ec8b6-1086">Batch</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1086">Batch</span></span>

* <span data-ttu-id="ec8b6-1087">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1087">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="ec8b6-1088">クラウド</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1088">Cloud</span></span>

* <span data-ttu-id="ec8b6-1089">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1089">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="ec8b6-1090">消費</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1090">Consumption</span></span>

* <span data-ttu-id="ec8b6-1091">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1091">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="ec8b6-1092">Event Grid</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1092">Event Grid</span></span>

* <span data-ttu-id="ec8b6-1093">[破壊的変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1093">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="ec8b6-1094">[破壊的変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1094">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="ec8b6-1095">[破壊的変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1095">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="ec8b6-1096">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1096">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="ec8b6-1097">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1097">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="ec8b6-1098">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1098">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="ec8b6-1099">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1099">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="ec8b6-1100">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1100">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="ec8b6-1101">Interactive</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1101">Interactive</span></span>

* <span data-ttu-id="ec8b6-1102">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1102">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="ec8b6-1103">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1103">Fixed errors on startup</span></span>
* <span data-ttu-id="ec8b6-1104">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1104">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="ec8b6-1105">IoT</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1105">IoT</span></span>

* <span data-ttu-id="ec8b6-1106">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1106">Added support for device provisioning service</span></span>
* <span data-ttu-id="ec8b6-1107">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1107">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="ec8b6-1108">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1108">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="ec8b6-1109">監視</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1109">Monitor</span></span>

* <span data-ttu-id="ec8b6-1110">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1110">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="ec8b6-1111">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1111">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="ec8b6-1112">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1112">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-1113">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1113">Network</span></span>

* <span data-ttu-id="ec8b6-1114">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1114">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="ec8b6-1115">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1115">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="ec8b6-1116">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1116">Profile</span></span>

* <span data-ttu-id="ec8b6-1117">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1117">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="ec8b6-1118">Role</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1118">Role</span></span>

* <span data-ttu-id="ec8b6-1119">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1119">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="ec8b6-1120">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1120">Service Fabric</span></span>

* <span data-ttu-id="ec8b6-1121">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1121">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="ec8b6-1122">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1122">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1123">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1123">VM</span></span>

* <span data-ttu-id="ec8b6-1124">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1124">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="ec8b6-1125">[破壊的変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1125">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="ec8b6-1126">[破壊的変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1126">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="ec8b6-1127">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1127">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="ec8b6-1128">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1128">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="ec8b6-1129">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1129">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="ec8b6-1130">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1130">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="ec8b6-1131">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1131">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="ec8b6-1132">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1132">December 19, 2017</span></span>

<span data-ttu-id="ec8b6-1133">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1133">Version 2.0.23</span></span>

* <span data-ttu-id="ec8b6-1134">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1134">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-1135">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1135">Container</span></span>

* <span data-ttu-id="ec8b6-1136">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1136">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-1137">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1137">Network</span></span>

* <span data-ttu-id="ec8b6-1138">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1138">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="ec8b6-1139">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1139">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-1140">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1140">Storage</span></span>

* <span data-ttu-id="ec8b6-1141">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1141">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1142">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1142">VM</span></span>

* <span data-ttu-id="ec8b6-1143">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1143">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="ec8b6-1144">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1144">December 5, 2017</span></span>

<span data-ttu-id="ec8b6-1145">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1145">Version 2.0.22</span></span>

* <span data-ttu-id="ec8b6-1146">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1146">Removed `az component` commands.</span></span> <span data-ttu-id="ec8b6-1147">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1147">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-1148">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1148">Core</span></span>
* <span data-ttu-id="ec8b6-1149">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1149">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="ec8b6-1150">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1150">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-1151">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1151">ACS</span></span>

* <span data-ttu-id="ec8b6-1152">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1152">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="ec8b6-1153">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1153">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="ec8b6-1154">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1154">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="ec8b6-1155">Advisor</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1155">Advisor</span></span>

* <span data-ttu-id="ec8b6-1156">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1156">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-1157">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1157">Appservice</span></span>

* <span data-ttu-id="ec8b6-1158">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1158">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="ec8b6-1159">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1159">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="ec8b6-1160">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1160">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="ec8b6-1161">消費</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1161">Consumption</span></span>

* <span data-ttu-id="ec8b6-1162">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1162">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-1163">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1163">Container</span></span>

* <span data-ttu-id="ec8b6-1164">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1164">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="ec8b6-1165">監視</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1165">Monitor</span></span>

* <span data-ttu-id="ec8b6-1166">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1166">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-1167">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1167">Resource</span></span>

* <span data-ttu-id="ec8b6-1168">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1168">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="ec8b6-1169">Role</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1169">Role</span></span>

* <span data-ttu-id="ec8b6-1170">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1170">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="ec8b6-1171">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1171">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="ec8b6-1172">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1172">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-1173">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1173">SQL</span></span>

* <span data-ttu-id="ec8b6-1174">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1174">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="ec8b6-1175">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1175">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1176">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1176">VM</span></span>

* <span data-ttu-id="ec8b6-1177">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1177">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="ec8b6-1178">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1178">November 14, 2017</span></span>

<span data-ttu-id="ec8b6-1179">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1179">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-1180">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1180">ACR</span></span>

* <span data-ttu-id="ec8b6-1181">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1181">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="ec8b6-1182">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1182">ACS</span></span>

* <span data-ttu-id="ec8b6-1183">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1183">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="ec8b6-1184">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1184">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="ec8b6-1185">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1185">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="ec8b6-1186">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1186">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="ec8b6-1187">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1187">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-1188">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1188">Appservice</span></span>

* <span data-ttu-id="ec8b6-1189">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1189">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="ec8b6-1190">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1190">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="ec8b6-1191">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1191">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="ec8b6-1192">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1192">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="ec8b6-1193">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1193">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="ec8b6-1194">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1194">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="ec8b6-1195">Batch</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1195">Batch</span></span>

* <span data-ttu-id="ec8b6-1196">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1196">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="ec8b6-1197">Batchai</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1197">Batchai</span></span>

* <span data-ttu-id="ec8b6-1198">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1198">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="ec8b6-1199">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1199">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="ec8b6-1200">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1200">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="ec8b6-1201">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1201">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="ec8b6-1202">クラウド</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1202">Cloud</span></span>

* <span data-ttu-id="ec8b6-1203">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1203">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-1204">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1204">Container</span></span>

* <span data-ttu-id="ec8b6-1205">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1205">Added support to open multiple ports</span></span>
* <span data-ttu-id="ec8b6-1206">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1206">Added container group restart policy</span></span>
* <span data-ttu-id="ec8b6-1207">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1207">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="ec8b6-1208">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1208">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="ec8b6-1209">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1209">Data Lake Analytics</span></span>

* <span data-ttu-id="ec8b6-1210">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1210">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="ec8b6-1211">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1211">Data Lake Store</span></span>

* <span data-ttu-id="ec8b6-1212">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1212">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="ec8b6-1213">内線番号</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1213">Extension</span></span>

* <span data-ttu-id="ec8b6-1214">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1214">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="ec8b6-1215">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1215">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="ec8b6-1216">IoT</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1216">IoT</span></span>

* <span data-ttu-id="ec8b6-1217">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1217">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="ec8b6-1218">監視</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1218">Monitor</span></span>

* <span data-ttu-id="ec8b6-1219">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1219">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-1220">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1220">Network</span></span>

* <span data-ttu-id="ec8b6-1221">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1221">Added support for CAA DNS records</span></span>
* <span data-ttu-id="ec8b6-1222">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1222">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="ec8b6-1223">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1223">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="ec8b6-1224">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1224">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="ec8b6-1225">Reservations</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1225">Reservations</span></span>

* <span data-ttu-id="ec8b6-1226">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1226">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-1227">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1227">Resource</span></span>

* <span data-ttu-id="ec8b6-1228">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1228">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-1229">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1229">SQL</span></span>

* <span data-ttu-id="ec8b6-1230">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1230">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-1231">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1231">Storage</span></span>

* <span data-ttu-id="ec8b6-1232">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1232">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="ec8b6-1233">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1233">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="ec8b6-1234">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1234">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="ec8b6-1235">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1235">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="ec8b6-1236">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1236">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="ec8b6-1237">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1237">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="ec8b6-1238">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1238">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1239">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1239">VM</span></span>

* <span data-ttu-id="ec8b6-1240">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1240">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="ec8b6-1241">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1241">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="ec8b6-1242">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1242">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="ec8b6-1243">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1243">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="ec8b6-1244">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1244">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="ec8b6-1245">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1245">October 24, 2017</span></span>

<span data-ttu-id="ec8b6-1246">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1246">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-1247">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1247">Core</span></span>

* <span data-ttu-id="ec8b6-1248">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1248">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-1249">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1249">ACR</span></span>

* <span data-ttu-id="ec8b6-1250">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1250">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="ec8b6-1251">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1251">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="ec8b6-1252">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1252">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-1253">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1253">ACS</span></span>

* <span data-ttu-id="ec8b6-1254">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1254">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="ec8b6-1255">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1255">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-1256">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1256">Appservice</span></span>

* <span data-ttu-id="ec8b6-1257">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1257">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="ec8b6-1258">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1258">Component</span></span>

* <span data-ttu-id="ec8b6-1259">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1259">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="ec8b6-1260">監視</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1260">Monitor</span></span>

* <span data-ttu-id="ec8b6-1261">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1261">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-1262">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1262">Resource</span></span>

* <span data-ttu-id="ec8b6-1263">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1263">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="ec8b6-1264">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1264">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1265">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1265">VM</span></span>

* <span data-ttu-id="ec8b6-1266">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1266">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="ec8b6-1267">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1267">October 9, 2017</span></span>

<span data-ttu-id="ec8b6-1268">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1268">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-1269">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1269">Core</span></span>

* <span data-ttu-id="ec8b6-1270">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1270">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-1271">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1271">Appservice</span></span>

* <span data-ttu-id="ec8b6-1272">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1272">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="ec8b6-1273">Batch</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1273">Batch</span></span>

* <span data-ttu-id="ec8b6-1274">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1274">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="ec8b6-1275">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1275">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="ec8b6-1276">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1276">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="ec8b6-1277">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1277">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="ec8b6-1278">Batchai</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1278">Batchai</span></span>

* <span data-ttu-id="ec8b6-1279">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1279">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="ec8b6-1280">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1280">Keyvault</span></span>

* <span data-ttu-id="ec8b6-1281">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1281">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="ec8b6-1282">(#4448)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1282">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="ec8b6-1283">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1283">Network</span></span>

* <span data-ttu-id="ec8b6-1284">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1284">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="ec8b6-1285">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1285">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-1286">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1286">Resource</span></span>

* <span data-ttu-id="ec8b6-1287">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1287">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="ec8b6-1288">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1288">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="ec8b6-1289">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1289">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="ec8b6-1290">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1290">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-1291">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1291">Sql</span></span>

* <span data-ttu-id="ec8b6-1292">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1292">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="ec8b6-1293">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1293">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="ec8b6-1294">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1294">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-1295">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1295">Storage</span></span>

* <span data-ttu-id="ec8b6-1296">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1296">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1297">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1297">Vm</span></span>

* <span data-ttu-id="ec8b6-1298">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1298">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="ec8b6-1299">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1299">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="ec8b6-1300">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1300">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="ec8b6-1301">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1301">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="ec8b6-1302">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1302">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="ec8b6-1303">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1303">September 22, 2017</span></span>

<span data-ttu-id="ec8b6-1304">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1304">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-1305">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1305">Resource</span></span>

* <span data-ttu-id="ec8b6-1306">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1306">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="ec8b6-1307">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1307">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="ec8b6-1308">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1308">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="ec8b6-1309">[破壊的変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1309">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-1310">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1310">Network</span></span>

* <span data-ttu-id="ec8b6-1311">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1311">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="ec8b6-1312">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1312">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="ec8b6-1313">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1313">Added `asg` application security group commands</span></span>
* <span data-ttu-id="ec8b6-1314">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1314">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="ec8b6-1315">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1315">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="ec8b6-1316">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1316">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="ec8b6-1317">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1317">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-1318">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1318">Storage</span></span>

* <span data-ttu-id="ec8b6-1319">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1319">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="ec8b6-1320">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1320">Eventgrid</span></span>

* <span data-ttu-id="ec8b6-1321">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1321">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-1322">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1322">SQL</span></span>

* <span data-ttu-id="ec8b6-1323">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1323">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="ec8b6-1324">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1324">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="ec8b6-1325">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1325">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="ec8b6-1326">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1326">Keyvault</span></span>

* <span data-ttu-id="ec8b6-1327">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1327">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1328">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1328">VM</span></span>

* <span data-ttu-id="ec8b6-1329">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1329">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="ec8b6-1330">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1330">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="ec8b6-1331">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1331">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="ec8b6-1332">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1332">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="ec8b6-1333">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1333">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="ec8b6-1334">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1334">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-1335">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1335">ACS</span></span>

* <span data-ttu-id="ec8b6-1336">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1336">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-1337">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1337">Appservice</span></span>

* <span data-ttu-id="ec8b6-1338">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1338">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="ec8b6-1339">バックアップ</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1339">Backup</span></span>

* <span data-ttu-id="ec8b6-1340">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1340">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="ec8b6-1341">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1341">September 11, 2017</span></span>

<span data-ttu-id="ec8b6-1342">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1342">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="ec8b6-1343">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1343">Core</span></span>

* <span data-ttu-id="ec8b6-1344">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1344">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="ec8b6-1345">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1345">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-1346">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1346">Acs</span></span>

* <span data-ttu-id="ec8b6-1347">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1347">Added `acs list-locations` command</span></span>
* <span data-ttu-id="ec8b6-1348">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1348">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-1349">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1349">Appservice</span></span>

* <span data-ttu-id="ec8b6-1350">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1350">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="ec8b6-1351">CDN</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1351">CDN</span></span>

* <span data-ttu-id="ec8b6-1352">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1352">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="ec8b6-1353">内線番号</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1353">Extension</span></span>

* <span data-ttu-id="ec8b6-1354">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1354">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="ec8b6-1355">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1355">Keyvault</span></span>

* <span data-ttu-id="ec8b6-1356">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1356">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-1357">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1357">Network</span></span>

* <span data-ttu-id="ec8b6-1358">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1358">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="ec8b6-1359">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1359">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="ec8b6-1360">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1360">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="ec8b6-1361">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1361">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="ec8b6-1362">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1362">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-1363">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1363">Resource</span></span>

* <span data-ttu-id="ec8b6-1364">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1364">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="ec8b6-1365">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1365">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="ec8b6-1366">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1366">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="ec8b6-1367">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1367">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-1368">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1368">SQL</span></span>

* <span data-ttu-id="ec8b6-1369">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1369">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1370">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1370">VM</span></span>

* <span data-ttu-id="ec8b6-1371">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1371">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="ec8b6-1372">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1372">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="ec8b6-1373">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1373">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="ec8b6-1374">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1374">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="ec8b6-1375">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1375">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="ec8b6-1376">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1376">August 31, 2017</span></span>

<span data-ttu-id="ec8b6-1377">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1377">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="ec8b6-1378">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1378">Keyvault</span></span>

* <span data-ttu-id="ec8b6-1379">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1379">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="ec8b6-1380">SF</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1380">Sf</span></span>

* <span data-ttu-id="ec8b6-1381">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1381">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-1382">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1382">Storage</span></span>

* <span data-ttu-id="ec8b6-1383">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1383">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="ec8b6-1384">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1384">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="ec8b6-1385">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1385">August 28, 2017</span></span>

<span data-ttu-id="ec8b6-1386">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1386">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="ec8b6-1387">CLI</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1387">CLI</span></span>

* <span data-ttu-id="ec8b6-1388">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1388">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-1389">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1389">ACS</span></span>

* <span data-ttu-id="ec8b6-1390">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1390">Corrected preview regions</span></span>
* <span data-ttu-id="ec8b6-1391">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1391">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="ec8b6-1392">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1392">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-1393">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1393">Appservice</span></span>

* <span data-ttu-id="ec8b6-1394">[破壊的変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1394">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="ec8b6-1395">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1395">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="ec8b6-1396">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1396">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="ec8b6-1397">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1397">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="ec8b6-1398">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1398">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="ec8b6-1399">IoT</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1399">IoT</span></span>

* <span data-ttu-id="ec8b6-1400">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1400">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-1401">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1401">Network</span></span>

* <span data-ttu-id="ec8b6-1402">[破壊的変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1402">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="ec8b6-1403">[破壊的変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1403">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="ec8b6-1404">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1404">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="ec8b6-1405">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1405">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="ec8b6-1406">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1406">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="ec8b6-1407">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1407">Profile</span></span>

* <span data-ttu-id="ec8b6-1408">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1408">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="ec8b6-1409">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1409">Service Fabric</span></span>

* <span data-ttu-id="ec8b6-1410">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1410">Preview release</span></span>
* <span data-ttu-id="ec8b6-1411">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1411">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="ec8b6-1412">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1412">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="ec8b6-1413">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1413">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-1414">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1414">Storage</span></span>

* <span data-ttu-id="ec8b6-1415">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1415">Enabled setting blob tier</span></span>
* <span data-ttu-id="ec8b6-1416">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1416">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="ec8b6-1417">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1417">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="ec8b6-1418">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1418">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="ec8b6-1419">[破壊的変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1419">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="ec8b6-1420">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1420">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1421">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1421">VM</span></span>

* <span data-ttu-id="ec8b6-1422">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1422">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="ec8b6-1423">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1423">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="ec8b6-1424">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1424">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="ec8b6-1425">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1425">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="ec8b6-1426">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1426">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="ec8b6-1427">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1427">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="ec8b6-1428">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1428">August 15, 2017</span></span>

<span data-ttu-id="ec8b6-1429">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1429">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-1430">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1430">ACS</span></span>

* <span data-ttu-id="ec8b6-1431">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1431">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-1432">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1432">Appservice</span></span>

* <span data-ttu-id="ec8b6-1433">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1433">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="ec8b6-1434">Event Grid</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1434">Event Grid</span></span>

* <span data-ttu-id="ec8b6-1435">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1435">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="ec8b6-1436">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1436">August 11, 2017</span></span>

<span data-ttu-id="ec8b6-1437">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1437">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-1438">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1438">ACS</span></span>

* <span data-ttu-id="ec8b6-1439">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1439">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="ec8b6-1440">Batch</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1440">Batch</span></span>

* <span data-ttu-id="ec8b6-1441">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1441">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="ec8b6-1442">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1442">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="ec8b6-1443">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1443">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="ec8b6-1444">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1444">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="ec8b6-1445">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1445">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="ec8b6-1446">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1446">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="ec8b6-1447">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1447">Component</span></span>

* <span data-ttu-id="ec8b6-1448">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1448">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="ec8b6-1449">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1449">Container</span></span>

* <span data-ttu-id="ec8b6-1450">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1450">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="ec8b6-1451">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1451">Data Lake Store</span></span>

* <span data-ttu-id="ec8b6-1452">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1452">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="ec8b6-1453">Event Grid</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1453">Event Grid</span></span>

* <span data-ttu-id="ec8b6-1454">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1454">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-1455">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1455">Network</span></span>

* <span data-ttu-id="ec8b6-1456">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1456">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="ec8b6-1457">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1457">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="ec8b6-1458">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1458">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="ec8b6-1459">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1459">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="ec8b6-1460">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1460">Profile</span></span>

* <span data-ttu-id="ec8b6-1461">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1461">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-1462">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1462">Storage</span></span>

* <span data-ttu-id="ec8b6-1463">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1463">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1464">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1464">VM</span></span>

* <span data-ttu-id="ec8b6-1465">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1465">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="ec8b6-1466">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1466">Exposed `list-skus` command</span></span>
* <span data-ttu-id="ec8b6-1467">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1467">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="ec8b6-1468">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1468">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="ec8b6-1469">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1469">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="ec8b6-1470">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1470">July 28, 2017</span></span>

<span data-ttu-id="ec8b6-1471">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1471">Version 2.0.12</span></span>

* <span data-ttu-id="ec8b6-1472">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1472">Added container commands</span></span>
* <span data-ttu-id="ec8b6-1473">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1473">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="ec8b6-1474">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1474">Core</span></span>

* <span data-ttu-id="ec8b6-1475">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1475">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="ec8b6-1476">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1476">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="ec8b6-1477">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1477">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="ec8b6-1478">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1478">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="ec8b6-1479">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1479">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="ec8b6-1480">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1480">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="ec8b6-1481">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1481">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="ec8b6-1482">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1482">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="ec8b6-1483">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1483">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="ec8b6-1484">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1484">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="ec8b6-1485">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1485">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="ec8b6-1486">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1486">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="ec8b6-1487">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1487">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="ec8b6-1488">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1488">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="ec8b6-1489">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1489">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="ec8b6-1490">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1490">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="ec8b6-1491">ACR</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1491">ACR</span></span>

* <span data-ttu-id="ec8b6-1492">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1492">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="ec8b6-1493">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1493">Support SKU update for managed registries</span></span>
* <span data-ttu-id="ec8b6-1494">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1494">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="ec8b6-1495">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1495">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="ec8b6-1496">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1496">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="ec8b6-1497">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1497">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-1498">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1498">ACS</span></span>

* <span data-ttu-id="ec8b6-1499">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1499">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-1500">Appservice</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1500">Appservice</span></span>

* <span data-ttu-id="ec8b6-1501">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1501">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="ec8b6-1502">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1502">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="ec8b6-1503">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1503">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="ec8b6-1504">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1504">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="ec8b6-1505">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1505">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="ec8b6-1506">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1506">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="ec8b6-1507">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1507">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="ec8b6-1508">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1508">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="ec8b6-1509">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1509">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="ec8b6-1510">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1510">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="ec8b6-1511">Batch</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1511">Batch</span></span>

* <span data-ttu-id="ec8b6-1512">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1512">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="ec8b6-1513">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1513">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="ec8b6-1514">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1514">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="ec8b6-1515">CDN</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1515">CDN</span></span>

* <span data-ttu-id="ec8b6-1516">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1516">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="ec8b6-1517">クラウド</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1517">Cloud</span></span>

* <span data-ttu-id="ec8b6-1518">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1518">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="ec8b6-1519">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1519">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="ec8b6-1520">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1520">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="ec8b6-1521">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1521">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="ec8b6-1522">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1522">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ec8b6-1523">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1523">CosmosDB</span></span>

* <span data-ttu-id="ec8b6-1524">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1524">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="ec8b6-1525">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1525">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="ec8b6-1526">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1526">Data Lake Analytics</span></span>

* <span data-ttu-id="ec8b6-1527">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1527">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="ec8b6-1528">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1528">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="ec8b6-1529">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1529">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="ec8b6-1530">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1530">Data Lake Store</span></span>

* <span data-ttu-id="ec8b6-1531">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1531">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="ec8b6-1532">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1532">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="ec8b6-1533">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1533">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="ec8b6-1534">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1534">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="ec8b6-1535">対話</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1535">Interactive</span></span>

* <span data-ttu-id="ec8b6-1536">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1536">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="ec8b6-1537">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1537">Increased test coverage</span></span>
* <span data-ttu-id="ec8b6-1538">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1538">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="ec8b6-1539">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1539">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="ec8b6-1540">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1540">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="ec8b6-1541">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1541">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="ec8b6-1542">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1542">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="ec8b6-1543">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1543">Added `--progress` flag</span></span>
* <span data-ttu-id="ec8b6-1544">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1544">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="ec8b6-1545">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1545">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="ec8b6-1546">IoT</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1546">IoT</span></span>

* <span data-ttu-id="ec8b6-1547">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1547">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="ec8b6-1548">(#3934)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1548">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="ec8b6-1549">Key Vault</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1549">Key vault</span></span>

* <span data-ttu-id="ec8b6-1550">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1550">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="ec8b6-1551">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1551">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="ec8b6-1552">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1552">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="ec8b6-1553">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1553">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="ec8b6-1554">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1554">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="ec8b6-1555">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1555">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="ec8b6-1556">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1556">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="ec8b6-1557">(#3307)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1557">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="ec8b6-1558">ラボ</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1558">Lab</span></span>

* <span data-ttu-id="ec8b6-1559">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1559">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="ec8b6-1560">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1560">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="ec8b6-1561">監視</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1561">Monitor</span></span>

* <span data-ttu-id="ec8b6-1562">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1562">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="ec8b6-1563">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1563">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="ec8b6-1564">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1564">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="ec8b6-1565">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1565">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="ec8b6-1566">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1566">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="ec8b6-1567">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1567">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="ec8b6-1568">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1568">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="ec8b6-1569">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1569">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="ec8b6-1570">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1570">`location` no longer required</span></span>
  * <span data-ttu-id="ec8b6-1571">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1571">Add name and ID support for target</span></span>
  * <span data-ttu-id="ec8b6-1572">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1572">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="ec8b6-1573">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1573">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="ec8b6-1574">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1574">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="ec8b6-1575">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1575">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="ec8b6-1576">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1576">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="ec8b6-1577">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1577">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-1578">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1578">Network</span></span>

* <span data-ttu-id="ec8b6-1579">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1579">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="ec8b6-1580">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1580">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="ec8b6-1581">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1581">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="ec8b6-1582">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1582">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="ec8b6-1583">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1583">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="ec8b6-1584">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1584">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="ec8b6-1585">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1585">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="ec8b6-1586">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1586">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="ec8b6-1587">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1587">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="ec8b6-1588">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1588">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="ec8b6-1589">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1589">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="ec8b6-1590">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1590">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="ec8b6-1591">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1591">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="ec8b6-1592">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1592">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="ec8b6-1593">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1593">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="ec8b6-1594">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1594">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="ec8b6-1595">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1595">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="ec8b6-1596">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1596">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="ec8b6-1597">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1597">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="ec8b6-1598">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1598">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="ec8b6-1599">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1599">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="ec8b6-1600">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1600">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="ec8b6-1601">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1601">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="ec8b6-1602">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1602">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="ec8b6-1603">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1603">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="ec8b6-1604">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1604">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="ec8b6-1605">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1605">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="ec8b6-1606">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1606">Profile</span></span>

* <span data-ttu-id="ec8b6-1607">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1607">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="ec8b6-1608">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1608">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="ec8b6-1609">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1609">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="ec8b6-1610">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1610">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="ec8b6-1611">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1611">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="ec8b6-1612">RDBMS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1612">RDBMS</span></span>

* <span data-ttu-id="ec8b6-1613">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1613">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="ec8b6-1614">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1614">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="ec8b6-1615">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1615">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="ec8b6-1616">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1616">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-1617">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1617">Resource</span></span>

* <span data-ttu-id="ec8b6-1618">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1618">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="ec8b6-1619">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1619">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="ec8b6-1620">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1620">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="ec8b6-1621">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1621">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="ec8b6-1622">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1622">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="ec8b6-1623">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1623">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="ec8b6-1624">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1624">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="ec8b6-1625">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1625">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="ec8b6-1626">Role</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1626">Role</span></span>

* <span data-ttu-id="ec8b6-1627">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1627">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="ec8b6-1628">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1628">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="ec8b6-1629">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1629">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="ec8b6-1630">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1630">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="ec8b6-1631">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1631">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="ec8b6-1632">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1632">Service Fabric</span></span>
* <span data-ttu-id="ec8b6-1633">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1633">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="ec8b6-1634">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1634">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="ec8b6-1635">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1635">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-1636">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1636">SQL</span></span>

* <span data-ttu-id="ec8b6-1637">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1637">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="ec8b6-1638">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1638">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="ec8b6-1639">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1639">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-1640">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1640">Storage</span></span>

* <span data-ttu-id="ec8b6-1641">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1641">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="ec8b6-1642">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1642">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="ec8b6-1643">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1643">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="ec8b6-1644">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1644">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="ec8b6-1645">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1645">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="ec8b6-1646">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1646">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1647">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1647">VM</span></span>

* <span data-ttu-id="ec8b6-1648">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1648">Support configuring nsg</span></span>
* <span data-ttu-id="ec8b6-1649">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1649">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="ec8b6-1650">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1650">Support managed service identities</span></span>
* <span data-ttu-id="ec8b6-1651">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1651">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="ec8b6-1652">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1652">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="ec8b6-1653">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1653">May 10, 2017</span></span>

<span data-ttu-id="ec8b6-1654">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1654">Version 2.0.6</span></span>

* <span data-ttu-id="ec8b6-1655">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1655">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="ec8b6-1656">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1656">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="ec8b6-1657">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1657">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="ec8b6-1658">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1658">Include Cognitive Services module</span></span>
* <span data-ttu-id="ec8b6-1659">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1659">Include Service Fabric module</span></span>
* <span data-ttu-id="ec8b6-1660">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1660">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="ec8b6-1661">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1661">Add support for CDN commands</span></span>
* <span data-ttu-id="ec8b6-1662">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1662">Remove Container module</span></span>
* <span data-ttu-id="ec8b6-1663">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1663">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="ec8b6-1664">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1664">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="ec8b6-1665">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1665">Core</span></span>

* <span data-ttu-id="ec8b6-1666">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1666">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="ec8b6-1667">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1667">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="ec8b6-1668">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1668">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="ec8b6-1669">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1669">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="ec8b6-1670">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1670">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="ec8b6-1671">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1671">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="ec8b6-1672">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1672">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="ec8b6-1673">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1673">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="ec8b6-1674">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1674">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="ec8b6-1675">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1675">core: Improved performance</span></span>
* <span data-ttu-id="ec8b6-1676">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1676">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="ec8b6-1677">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1677">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-1678">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1678">ACS</span></span>

* <span data-ttu-id="ec8b6-1679">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1679">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="ec8b6-1680">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1680">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="ec8b6-1681">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1681">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="ec8b6-1682">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1682">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-1683">AppService</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1683">AppService</span></span>

* <span data-ttu-id="ec8b6-1684">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1684">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="ec8b6-1685">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1685">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="ec8b6-1686">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1686">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="ec8b6-1687">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1687">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="ec8b6-1688">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1688">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="ec8b6-1689">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1689">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="ec8b6-1690">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1690">support slot swap with preview</span></span>
* <span data-ttu-id="ec8b6-1691">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1691">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="ec8b6-1692">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1692">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ec8b6-1693">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1693">CosmosDB</span></span>

* <span data-ttu-id="ec8b6-1694">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1694">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="ec8b6-1695">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1695">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="ec8b6-1696">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1696">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="ec8b6-1697">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1697">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="ec8b6-1698">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1698">Data Lake Analytics</span></span>

* <span data-ttu-id="ec8b6-1699">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1699">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="ec8b6-1700">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1700">Add support for new catalog item type: package.</span></span> <span data-ttu-id="ec8b6-1701">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1701">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="ec8b6-1702">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1702">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="ec8b6-1703">テーブル</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1703">Table</span></span>
  * <span data-ttu-id="ec8b6-1704">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1704">Table valued function</span></span>
  * <span data-ttu-id="ec8b6-1705">表示</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1705">View</span></span>
  * <span data-ttu-id="ec8b6-1706">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1706">Table Statistics.</span></span> <span data-ttu-id="ec8b6-1707">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1707">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="ec8b6-1708">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1708">Data Lake Store</span></span>

* <span data-ttu-id="ec8b6-1709">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1709">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="ec8b6-1710">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1710">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="ec8b6-1711">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1711">missed help for access show.</span></span> <span data-ttu-id="ec8b6-1712">追加しました </span><span class="sxs-lookup"><span data-stu-id="ec8b6-1712">adding it.</span></span> <span data-ttu-id="ec8b6-1713">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1713">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="ec8b6-1714">検索</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1714">Find</span></span>

* <span data-ttu-id="ec8b6-1715">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1715">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="ec8b6-1716">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1716">KeyVault</span></span>

* <span data-ttu-id="ec8b6-1717">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1717">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="ec8b6-1718">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1718">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="ec8b6-1719">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1719">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="ec8b6-1720">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1720">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="ec8b6-1721">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1721">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="ec8b6-1722">ラボ</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1722">Lab</span></span>

* <span data-ttu-id="ec8b6-1723">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1723">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="ec8b6-1724">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1724">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="ec8b6-1725">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1725">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="ec8b6-1726">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1726">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="ec8b6-1727">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1727">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="ec8b6-1728">監視</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1728">Monitor</span></span>

* <span data-ttu-id="ec8b6-1729">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1729">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="ec8b6-1730">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1730">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="ec8b6-1731">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1731">Network</span></span>

* <span data-ttu-id="ec8b6-1732">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1732">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="ec8b6-1733">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1733">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="ec8b6-1734">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1734">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="ec8b6-1735">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1735">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="ec8b6-1736">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1736">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="ec8b6-1737">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1737">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="ec8b6-1738">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1738">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="ec8b6-1739">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1739">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="ec8b6-1740">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1740">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="ec8b6-1741">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1741">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="ec8b6-1742">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1742">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="ec8b6-1743">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1743">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="ec8b6-1744">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1744">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="ec8b6-1745">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1745">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="ec8b6-1746">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1746">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="ec8b6-1747">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1747">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="ec8b6-1748">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1748">Profile</span></span>

* <span data-ttu-id="ec8b6-1749">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1749">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="ec8b6-1750">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1750">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="ec8b6-1751">Redis</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1751">Redis</span></span>

* <span data-ttu-id="ec8b6-1752">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1752">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="ec8b6-1753">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1753">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="ec8b6-1754">リソース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1754">Resource</span></span>

* <span data-ttu-id="ec8b6-1755">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1755">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="ec8b6-1756">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1756">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="ec8b6-1757">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1757">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="ec8b6-1758">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="ec8b6-1758">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="ec8b6-1759">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1759">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="ec8b6-1760">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="ec8b6-1760">Add docs for az lock update.</span></span> <span data-ttu-id="ec8b6-1761">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1761">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="ec8b6-1762">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="ec8b6-1762">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="ec8b6-1763">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1763">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="ec8b6-1764">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1764">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="ec8b6-1765">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1765">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="ec8b6-1766">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1766">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="ec8b6-1767">Role</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1767">Role</span></span>

* <span data-ttu-id="ec8b6-1768">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1768">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="ec8b6-1769">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1769">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="ec8b6-1770">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1770">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="ec8b6-1771">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1771">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="ec8b6-1772">SQL</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1772">SQL</span></span>

* <span data-ttu-id="ec8b6-1773">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1773">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="ec8b6-1774">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1774">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="ec8b6-1775">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1775">Storage</span></span>

* <span data-ttu-id="ec8b6-1776">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1776">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="ec8b6-1777">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1777">Add support for incremental blob copy</span></span>
* <span data-ttu-id="ec8b6-1778">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1778">Add support for large block blob upload</span></span>
* <span data-ttu-id="ec8b6-1779">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1779">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1780">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1780">VM</span></span>

* <span data-ttu-id="ec8b6-1781">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1781">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="ec8b6-1782">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1782">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="ec8b6-1783">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1783">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="ec8b6-1784">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1784">az vm/vmss disk</span></span>
  3. <span data-ttu-id="ec8b6-1785">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1785">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="ec8b6-1786">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1786">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="ec8b6-1787">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1787">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="ec8b6-1788">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1788">April 3, 2017</span></span>

<span data-ttu-id="ec8b6-1789">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1789">Version 2.0.2</span></span>

<span data-ttu-id="ec8b6-1790">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1790">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="ec8b6-1791">コア</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1791">Core</span></span>

* <span data-ttu-id="ec8b6-1792">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1792">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="ec8b6-1793">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1793">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="ec8b6-1794">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1794">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="ec8b6-1795">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1795">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="ec8b6-1796">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1796">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="ec8b6-1797">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="ec8b6-1797">Add prompting for missing template parameters.</span></span> <span data-ttu-id="ec8b6-1798">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1798">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="ec8b6-1799">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1799">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="ec8b6-1800">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1800">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="ec8b6-1801">ACS</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1801">ACS</span></span>

* <span data-ttu-id="ec8b6-1802">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1802">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="ec8b6-1803">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="ec8b6-1803">Add support for ssh key password prompting.</span></span> <span data-ttu-id="ec8b6-1804">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1804">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="ec8b6-1805">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="ec8b6-1805">Add support for windows clusters.</span></span> <span data-ttu-id="ec8b6-1806">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1806">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="ec8b6-1807">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="ec8b6-1807">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="ec8b6-1808">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1808">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="ec8b6-1809">AppService</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1809">AppService</span></span>

* <span data-ttu-id="ec8b6-1810">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1810">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="ec8b6-1811">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1811">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="ec8b6-1812">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1812">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="ec8b6-1813">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1813">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="ec8b6-1814">DataLake</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1814">DataLake</span></span>

* <span data-ttu-id="ec8b6-1815">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1815">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="ec8b6-1816">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1816">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="ec8b6-1817">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1817">DocuemntDB</span></span>

* <span data-ttu-id="ec8b6-1818">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1818">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="ec8b6-1819">VM</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1819">VM</span></span>

* <span data-ttu-id="ec8b6-1820">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1820">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="ec8b6-1821">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1821">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="ec8b6-1822">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1822">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="ec8b6-1823">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1823">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="ec8b6-1824">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1824">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="ec8b6-1825">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1825">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="ec8b6-1826">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1826">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="ec8b6-1827">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1827">February 27, 2017</span></span>

<span data-ttu-id="ec8b6-1828">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1828">Version 2.0.0</span></span>

<span data-ttu-id="ec8b6-1829">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1829">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="ec8b6-1830">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1830">Container Service (acs)</span></span>
- <span data-ttu-id="ec8b6-1831">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1831">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="ec8b6-1832">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1832">Networking</span></span>
- <span data-ttu-id="ec8b6-1833">Storage</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1833">Storage</span></span>

<span data-ttu-id="ec8b6-1834">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1834">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="ec8b6-1835">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1835">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="ec8b6-1836">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1836">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="ec8b6-1837">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1837">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="ec8b6-1838">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1838">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="ec8b6-1839">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1839">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="ec8b6-1840">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1840">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="ec8b6-1841">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1841">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="ec8b6-1842">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="ec8b6-1842">Provide feedback from the command line with the `az feedback` command</span></span>

