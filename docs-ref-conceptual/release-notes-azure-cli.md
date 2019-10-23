---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 10/15/2019
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 0eb1ccccdeff8c3d9b97167ee74f3380d983a552
ms.sourcegitcommit: e99b39e2f14a38c9bcae1b2b5921c6d8b464ef31
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2019
ms.locfileid: "72549689"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="cfdd1-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="cfdd1-103">Azure CLI release notes</span></span>

## <a name="october-15-2019"></a><span data-ttu-id="cfdd1-104">2019 年 10 月 15 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-104">October 15, 2019</span></span>

<span data-ttu-id="cfdd1-105">バージョン 2.0.75</span><span class="sxs-lookup"><span data-stu-id="cfdd1-105">Version 2.0.75</span></span>

### <a name="aks"></a><span data-ttu-id="cfdd1-106">AKS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-106">AKS</span></span>

* <span data-ttu-id="cfdd1-107">Kubernetes のバージョンでサポートされている場合、`--load-balancer-sku` の既定値を `standard` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-107">Changed `--load-balancer-sku` default value to `standard` if supported by the kubernetes version</span></span>
* <span data-ttu-id="cfdd1-108">Kubernetes のバージョンでサポートされている場合、`--vm-set-type` の既定値を `virtualmachinescalesets` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-108">Changed `--vm-set-type` default value to `virtualmachinescalesets` if supported by the kubernetes version</span></span>

### <a name="ams"></a><span data-ttu-id="cfdd1-109">AMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-109">AMS</span></span>

* <span data-ttu-id="cfdd1-110">[重大な変更] `job start` の名前を `job create` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-110">[BREAKING CHANGE] Changed the name of `job start` to `job create`</span></span>
* <span data-ttu-id="cfdd1-111">[重大な変更] `content-key-policy create` の `--ask` パラメーターが UTF8 ではなく 32 文字の 16 進文字列を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-111">[BREAKING CHANGE] Changed the `--ask` parameter of `content-key-policy create` to use a 32-character hex string instead of UTF8</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-112">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-112">AppService</span></span>

* <span data-ttu-id="cfdd1-113">コマンド `webapp config access-restriction show|set|add|remove` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-113">Added commands `webapp config access-restriction show|set|add|remove`</span></span>
* <span data-ttu-id="cfdd1-114">より優れたエラー処理を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-114">Added better error handling to `webapp up`</span></span>
* <span data-ttu-id="cfdd1-115">`Isolated` SKU のサポートを `appservice plan update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-115">Added support for `Isolated` SKU to `appservice plan update`</span></span>

### <a name="arm"></a><span data-ttu-id="cfdd1-116">ARM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-116">ARM</span></span>

* <span data-ttu-id="cfdd1-117">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `deployment create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-117">Added `--handle-extended-json-format` parameter `deployment create` to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="cfdd1-118">Compute</span><span class="sxs-lookup"><span data-stu-id="cfdd1-118">Compute</span></span>

* <span data-ttu-id="cfdd1-119">`--enable-agent` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-119">Added `--enable-agent` parameter to `vm create`</span></span>
* <span data-ttu-id="cfdd1-120">ゾーンを使用するときに標準のパブリック IP SKU を自動的に使用するように `vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-120">Changed `vm create` to use standard public IP SKU automatically when using zones</span></span>
* <span data-ttu-id="cfdd1-121">VM の有効なコンピューター名が指定されていない場合に自動的に作成されるように `vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-121">Changed `vm create` to automatically create a valid computer name for a VM if none is provided</span></span>
* <span data-ttu-id="cfdd1-122">VMSS 内の仮想マシンのカスタム コンピューター名プレフィックスをサポートするために `--computer-name-prefix` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-122">Added `--computer-name-prefix` parameter to `vmss create` to support custom computer name prefix of virtual machines in the VMSS</span></span>
* <span data-ttu-id="cfdd1-123">ログ分析ワークスペースを自動的に有効にする `--workspace` パラメーターを `vm create` に追加します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-123">Add `--workspace` parameter to `vm create` to enable log analytics workspace automatically</span></span>
* <span data-ttu-id="cfdd1-124">ギャラリーの API バージョンが 2019-07-01 に更新されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-124">Updated galleries API version to 2019-07-01</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-125">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-125">Core</span></span>

* <span data-ttu-id="cfdd1-126">汎用の update コマンドで `--set` パラメーターの構文チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-126">Added syntax check for `--set` parameter in generic update command</span></span>

### <a name="iot"></a><span data-ttu-id="cfdd1-127">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-127">IoT</span></span>

* <span data-ttu-id="cfdd1-128">`iot hub show` で "リソースが見つかりません" のエラーが誤って発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-128">Fixed an issue where `iot hub show` would incorrectly error with "resource not found"</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-129">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-129">Monitor</span></span>

* <span data-ttu-id="cfdd1-130">CRUD のサポートを `monitor log-analytics workspace` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-130">Added support for CRUD to `monitor log-analytics workspace`</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-131">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-131">Network</span></span>

* <span data-ttu-id="cfdd1-132">クロステナントの仮想リンクのサポートを `network private-dns link vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-132">Added support for cross-tenant virtual linking to `network private-dns link vnet [create|update]`</span></span>
* <span data-ttu-id="cfdd1-133">[重大な変更] `network vnet subnet list` で `--resource-group` および `--vnet-name` パラメーターが必須に変更になりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-133">[BREAKING CHANGE] Changed `network vnet subnet list` to require `--resource-group` and `--vnet-name` parameters</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-134">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-134">SQL</span></span>

* <span data-ttu-id="cfdd1-135">マネージ インスタンスの AAD 管理者の設定をサポートするコマンドを `sql mi ad-admin` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-135">Added commands to `sql mi ad-admin` that support setting an AAD administrator on managed instances</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-136">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-136">Storage</span></span>

* <span data-ttu-id="cfdd1-137">サービス間のコピー中にアクセス層を保持する `--preserve-s2s-access-tier` パラメーターを `storage copy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-137">Added `--preserve-s2s-access-tier` parameter `storage copy` to preserve access tier during service to service copy</span></span>
* <span data-ttu-id="cfdd1-138">ストレージ アカウントで大容量ファイルの共有をサポートするために `--enable-large-file-share` パラメーターを `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-138">Added `--enable-large-file-share` parameter to `storage account [create|update]` to support large file shares for storage account</span></span>

## <a name="september-24-2019"></a><span data-ttu-id="cfdd1-139">2019 年 9 月 24 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-139">September 24, 2019</span></span>

<span data-ttu-id="cfdd1-140">バージョン 2.0.74</span><span class="sxs-lookup"><span data-stu-id="cfdd1-140">Version 2.0.74</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-141">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-141">ACR</span></span>

* <span data-ttu-id="cfdd1-142">必須の `--type` パラメーターを `acr config retention update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-142">Added a required `--type` parameter to `acr config retention update`</span></span>
* <span data-ttu-id="cfdd1-143">[破壊的変更] `acr config` コマンド グループでパラメーター `--name -n` の名前が `--registry -r ` に変更されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-143">[BREAKING CHNAGE] Renamed parameter `--name -n` changed to `--registry -r ` for `acr config` command group</span></span>

### <a name="aks"></a><span data-ttu-id="cfdd1-144">AKS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-144">AKS</span></span>

* <span data-ttu-id="cfdd1-145">`--load-balancer-sku` パラメーターを `aks create` コマンドに追加しました。これにより、SLB を使用する AKS クラスターを作成できます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-145">Added `--load-balancer-sku` parameter to `aks create` command, which allows for creating AKS cluster with SLB</span></span>
* <span data-ttu-id="cfdd1-146">`--load-balancer-managed-outbound-ip-count`、`--load-balancer-outbound-ips`、`--load-balancer-outbound-ip-prefixes` パラメーターを `aks [create|update]` コマンドに追加しました。これにより、SLB を使用する AKS クラスターのロード バランサー プロファイルを更新できます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-146">Added `--load-balancer-managed-outbound-ip-count`, `--load-balancer-outbound-ips` and `--load-balancer-outbound-ip-prefixes` parameters to `aks [create|update]` commands, which allow for updating load balancer profile of an AKS cluster with SLB</span></span>
* <span data-ttu-id="cfdd1-147">`--vm-set-type` パラメーターを `aks create` コマンドに追加しました。これにより、AKS クラスターの VM の種類 (vmas または vmss) を指定できます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-147">Added `--vm-set-type` parameter to `aks create` command, which allows to specify vm types of an AKS Cluster (vmas or vmss)</span></span>

### <a name="arm"></a><span data-ttu-id="cfdd1-148">ARM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-148">ARM</span></span>

* <span data-ttu-id="cfdd1-149">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `group deployment create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-149">Added `--handle-extended-json-format` parameter to `group deployment create` command to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="cfdd1-150">Compute</span><span class="sxs-lookup"><span data-stu-id="cfdd1-150">Compute</span></span>

* <span data-ttu-id="cfdd1-151">終了のスケジュール化されたイベントを構成しやすくするために `--terminate-notification-time` パラメーターを `vmss [create|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-151">Added `--terminate-notification-time` parameter to `vmss [create|update]` commands to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="cfdd1-152">終了のスケジュール化されたイベントを構成しやすくするために `--enable-terminate-notification` パラメーターを `vmss update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-152">Added `--enable-terminate-notification` parameter to `vmss update` command to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="cfdd1-153">`--priority,` `--eviction-policy,` `--max-billing` パラメーターを `[vm|vmss] create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-153">Added `--priority,` `--eviction-policy,` `--max-billing` parameters to `[vm|vmss] create` commands</span></span>
* <span data-ttu-id="cfdd1-154">`disk create` を変更し、ディスク アップロードの正確なサイズを指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-154">Changed `disk create` to allow specifying the exact size of the disk upload</span></span>
* <span data-ttu-id="cfdd1-155">マネージド ディスクの増分スナップショットのサポートを `snapshot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-155">Added support for incremental snapshots for managed disks to `snapshot create`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="cfdd1-156">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cfdd1-156">Cosmos DB</span></span>

* <span data-ttu-id="cfdd1-157">キー、読み取り専用キー、または接続文字列を表示する `--type <key-type>` パラメーターを `cosmosdb keys list` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-157">Added `--type <key-type>` parameter to `cosmosdb keys list` command to show key, read only keys or connection strings</span></span>
* <span data-ttu-id="cfdd1-158">`cosmosdb keys regenerate` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-158">Added `cosmosdb keys regenerate` command</span></span>
* <span data-ttu-id="cfdd1-159">[非推奨] `cosmosdb list-connection-strings`、`cosmosdb regenerate-key`、`cosmosdb list-read-only-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-159">[DEPRECATED] Deprecated `cosmosdb list-connection-strings`, `cosmosdb regenerate-key` and `cosmosdb list-read-only-keys` commands</span></span>

### <a name="eventgrid"></a><span data-ttu-id="cfdd1-160">EventGrid</span><span class="sxs-lookup"><span data-stu-id="cfdd1-160">EventGrid</span></span>

* <span data-ttu-id="cfdd1-161">正しいパラメーターを参照するようにエンドポイントのヘルプ テキストを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-161">Fixed the endpoint help text to refer to the right parameter</span></span>

### <a name="key-vault"></a><span data-ttu-id="cfdd1-162">Key Vault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-162">Key Vault</span></span>

* <span data-ttu-id="cfdd1-163">テナントを使用してログインすると (`login -t`)、`keyvault create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-163">Fixed issue where logging in with a tenant (`login -t`) could cause `keyvault create` to fail</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-164">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-164">Monitor</span></span>

* <span data-ttu-id="cfdd1-165">`monitor metrics alert create` の `--condition` 引数で `:` 文字を使用できないという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-165">Fixed issue where `:` character was not allowed in `--condition` argument to `monitor metrics alert create`</span></span>

### <a name="policy"></a><span data-ttu-id="cfdd1-166">ポリシー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-166">Policy</span></span>

* <span data-ttu-id="cfdd1-167">Policy API バージョン 2019-06-01 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-167">Added support for Policy API version 2019-06-01</span></span>
* <span data-ttu-id="cfdd1-168">`policy assignment create` コマンドに `--enforcement-mode` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-168">Added `--enforcement-mode` parameter to `policy assignment create` command</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-169">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-169">Storage</span></span>

* <span data-ttu-id="cfdd1-170">`az storage copy` コマンドに `--blob-type` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-170">Added `--blob-type` parameter to `az storage copy` command</span></span>

## <a name="september-10-2019"></a><span data-ttu-id="cfdd1-171">2019 年 9 月 10 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-171">September 10, 2019</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-172">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-172">ACR</span></span>

* <span data-ttu-id="cfdd1-173">アイテム保持ポリシーを構成するためのコマンド グループ `acr config retention` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-173">Added command group `acr config retention` to configure retention policy</span></span>

### <a name="aks"></a><span data-ttu-id="cfdd1-174">AKS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-174">AKS</span></span>

* <span data-ttu-id="cfdd1-175">次のコマンドを使用した ACR 統合のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-175">Added support for ACR integration with the following commands:</span></span>
  * <span data-ttu-id="cfdd1-176">AKS クラスターに ACR をアタッチするための `--attach-acr` パラメーターを `aks [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-176">Added `--attach-acr` parameter to `aks [create|update]` to attach an ACR to an AKS cluster</span></span>
  * <span data-ttu-id="cfdd1-177">AKS クラスターから ACR をデタッチするための `--detach-acr` パラメーターを `aks update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-177">Added `--detach-acr` parameter to `aks update` to detach the ACR from an AKS cluster</span></span>

### <a name="arm"></a><span data-ttu-id="cfdd1-178">ARM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-178">ARM</span></span>

* <span data-ttu-id="cfdd1-179">API バージョン 2019-05-10 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-179">Updated to use API version 2019-05-10</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-180">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-180">Batch</span></span>

* <span data-ttu-id="cfdd1-181">`batch pool create` の `--json-file` に新しい JSON 構成設定を追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-181">Added new JSON configuration settings to `--json-file` for `batch pool create`:</span></span>
  * <span data-ttu-id="cfdd1-182">ファイル システム マウント用の `MountConfigurations` を追加しました (詳細については https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-182">Added `MountConfigurations` for file system mounts (see https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body for details)</span></span>
  * <span data-ttu-id="cfdd1-183">プール上のパブリック IP 用に、`NetworkConfiguration` にオプションのプロパティ `publicIPs` を追加しました (詳細については https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-183">Added optional property `publicIPs` on `NetworkConfiguration` for public IPs on pools (see https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body for details)</span></span>
* <span data-ttu-id="cfdd1-184">共有イメージ ギャラリーのサポートを `--image` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-184">Added support for shared image galleries to `--image`</span></span>
* <span data-ttu-id="cfdd1-185">[重大な変更] `batch pool create` の `--start-task-wait-for-success` の既定値を `true` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-185">[BREAKING CHANGE] Changed default value of `--start-task-wait-for-success` on `batch pool create` to be `true`</span></span>
* <span data-ttu-id="cfdd1-186">[重大な変更] `AutoUserSpecification` の `Scope` の既定値が常に Pool になるように変更しました (以前は Windows ノードでは `Task`、Linux ノードでは `Pool` でした)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-186">[BREAKING CHANGE] Changed default value for `Scope` on `AutoUserSpecification` to always be Pool (was `Task` on Windows nodes, `Pool` on Linux nodes)</span></span>
  * <span data-ttu-id="cfdd1-187">この引数は、`--json-file` を使用して JSON 構成からのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-187">This argument can only be set from a JSON configuration with `--json-file`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="cfdd1-188">HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfdd1-188">HDInsight</span></span>

* <span data-ttu-id="cfdd1-189">GA リリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-189">GA release</span></span>
* <span data-ttu-id="cfdd1-190">[重大な変更] `az hdinsight resize` のパラメーター `--workernode-count/-c` が必須に変更されました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-190">[BREAKING CHANGE] Changed parameter `--workernode-count/-c` of `az hdinsight resize` to be required.</span></span>

### <a name="key-vault"></a><span data-ttu-id="cfdd1-191">Key Vault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-191">Key Vault</span></span>

* <span data-ttu-id="cfdd1-192">ネットワーク ルールからサブネットを削除できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-192">Fixed issue where subnets couldn't be deleted from network rules</span></span>
* <span data-ttu-id="cfdd1-193">重複したサブネットと IP アドレスをネットワーク ルールに追加できる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-193">Fixed issue where duplicated subnets and IP addresses could be added to network rules</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-194">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-194">Network</span></span>

* <span data-ttu-id="cfdd1-195">トラフィック分析間隔の値を設定する `--interval` パラメーターを `network watcher flow-log` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-195">Added `--interval` parameter to `network watcher flow-log` to set traffic analysis interval value</span></span>
* <span data-ttu-id="cfdd1-196">ゲートウェイ ID を管理するための `network application-gateway identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-196">Added `network application-gateway identity` to manage gateway identity</span></span>
* <span data-ttu-id="cfdd1-197">Key Vault ID を設定するためのサポートを `network application-gateway ssl-cert` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-197">Added support for setting Key Vault ID to `network application-gateway ssl-cert`</span></span>
* <span data-ttu-id="cfdd1-198">`network express-route peering peer-connection [show|list]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-198">Added `network express-route peering peer-connection [show|list]`</span></span>

### <a name="policy"></a><span data-ttu-id="cfdd1-199">ポリシー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-199">Policy</span></span>

* <span data-ttu-id="cfdd1-200">API バージョン 2019-01-01 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-200">Updated to use API version 2019-01-01</span></span>

## <a name="august-27-2019"></a><span data-ttu-id="cfdd1-201">2019 年 8 月 27 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-201">August 27, 2019</span></span>

<span data-ttu-id="cfdd1-202">バージョン 2.0.72</span><span class="sxs-lookup"><span data-stu-id="cfdd1-202">Version 2.0.72</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-203">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-203">ACR</span></span>

* <span data-ttu-id="cfdd1-204">[重大な変更] `classic` SKU のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-204">[BREAKING CHANGE] Removed support for the `classic` SKU</span></span>

### <a name="api-management"></a><span data-ttu-id="cfdd1-205">API Management</span><span class="sxs-lookup"><span data-stu-id="cfdd1-205">API Management</span></span>

* <span data-ttu-id="cfdd1-206">[プレビュー] `apim` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-206">[PREVIEW] Added `apim` command group</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-207">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-207">AppService</span></span>

* <span data-ttu-id="cfdd1-208">スロットを指定したときの `webapp webjob continuous start` コマンドに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-208">Fixed issue with `webapp webjob continuous start` command when specifying a slot</span></span>
* <span data-ttu-id="cfdd1-209">`env` フォルダーを検出してデプロイに使用されているファイルから削除するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-209">Changed `webapp up` to detect `env` folder and remove it from the file used for deployment</span></span>

### <a name="keyvault"></a><span data-ttu-id="cfdd1-210">KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-210">Keyvault</span></span>

* <span data-ttu-id="cfdd1-211">`--expires` 引数を無視する `keyvault secret set` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-211">Fixed a bug in `keyvault secret set` that igored the `--expires` argument</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-212">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-212">Network</span></span>

* <span data-ttu-id="cfdd1-213">`--private-ip-address-version` 引数に IPv6 アドレスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-213">Added support for IPv6 addresses to `--private-ip-address-version` arguments</span></span>
* <span data-ttu-id="cfdd1-214">プライベート エンドポイントの管理用に新しいコマンド `network private-endpoint [create|update|list-types]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-214">Added new commands `network private-endpoint [create|update|list-types]` for private endpoint management</span></span>
* <span data-ttu-id="cfdd1-215">コマンド グループ `network private-link-service` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-215">Added command group `network private-link-service`</span></span>
* <span data-ttu-id="cfdd1-216">`--private-endpoint-network-policies` 引数と `--private-link-service-network-policies` 引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-216">Added `--private-endpoint-network-policies` and `--private-link-service-network-policies` arguments to `network vnet subnet update`</span></span>

### <a name="rbac"></a><span data-ttu-id="cfdd1-217">RBAC</span><span class="sxs-lookup"><span data-stu-id="cfdd1-217">RBAC</span></span>

* <span data-ttu-id="cfdd1-218">ホームページが更新されない `ad app update --homepage` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-218">Fixed issue with `ad app update --homepage` where homepage would not be updated</span></span>

### <a name="servicefabric"></a><span data-ttu-id="cfdd1-219">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cfdd1-219">ServiceFabric</span></span>

* <span data-ttu-id="cfdd1-220">キー コンテナーの大文字と小文字が混在する名前のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-220">Added support for mixed-case Key Vault names</span></span>
* <span data-ttu-id="cfdd1-221">Key Vault で証明書を使用したときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-221">Fixed issue when using certificates in Key Vault</span></span>
* <span data-ttu-id="cfdd1-222">PFX 証明書ファイルの使用に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-222">Fixed issue with using PFX certificate files</span></span>
* <span data-ttu-id="cfdd1-223">Key Vault リソースグループが指定されていなかったときの `sf cluster certificate add` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-223">Fixed issue with `sf cluster certificate add` when Key Vault resource group wasn't specified</span></span>
* <span data-ttu-id="cfdd1-224">`sf cluster set` が動作しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-224">Fixed issue with `sf cluster set` not working</span></span>

### <a name="signalr"></a><span data-ttu-id="cfdd1-225">SignalR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-225">SignalR</span></span>

* <span data-ttu-id="cfdd1-226">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-226">Added new commands:</span></span>
  * <span data-ttu-id="cfdd1-227">`signalr cors`:SignalR CORS の管理</span><span class="sxs-lookup"><span data-stu-id="cfdd1-227">`signalr cors`: Manage SignalR CORS</span></span>
  * <span data-ttu-id="cfdd1-228">`signalr restart`:SignalR Service の再起動</span><span class="sxs-lookup"><span data-stu-id="cfdd1-228">`signalr restart`: Restart a SignalR service</span></span>
  * <span data-ttu-id="cfdd1-229">`signalr update`:SignalR Service の更新</span><span class="sxs-lookup"><span data-stu-id="cfdd1-229">`signalr update`: Update a SignalR service</span></span>
* <span data-ttu-id="cfdd1-230">`--service-mode` 引数を `signalr create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-230">Added `--service-mode` argument to `signalr create`</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-231">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-231">Storage</span></span>

* <span data-ttu-id="cfdd1-232">`storage account revoke-delegation-keys` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-232">Added `storage account revoke-delegation-keys` command</span></span>

## <a name="august-13-2019"></a><span data-ttu-id="cfdd1-233">2019 年 8 月 13 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-233">August 13, 2019</span></span>

<span data-ttu-id="cfdd1-234">バージョン 2.0.71</span><span class="sxs-lookup"><span data-stu-id="cfdd1-234">Version 2.0.71</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-235">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-235">AppService</span></span>

* <span data-ttu-id="cfdd1-236">`webapp webjob continuous` コマンドがスロットで失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-236">Fixed issue where `webapp webjob continuous` commands were failing for slots</span></span>

### <a name="botservice"></a><span data-ttu-id="cfdd1-237">BotService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-237">BotService</span></span>

* <span data-ttu-id="cfdd1-238">[重大な変更] v3 SDK ボットの作成のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-238">[BREAKING CHANGE] Removed support for creating v3 SDK bots</span></span>

### <a name="cognitiveservices"></a><span data-ttu-id="cfdd1-239">CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cfdd1-239">CognitiveServices</span></span>

* <span data-ttu-id="cfdd1-240">`cognitiveservices account network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-240">Added `cognitiveservices account network-rule` commands</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="cfdd1-241">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cfdd1-241">Cosmos DB</span></span>

* <span data-ttu-id="cfdd1-242">複数の書き込み場所を更新するときの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-242">Removed warning when updating multiple write locations</span></span>
* <span data-ttu-id="cfdd1-243">CosmosDB SQL、MongoDB、Cassandra、Gremlin、およびテーブル リソースとリソースのスループットのための CRUD コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-243">Added CRUD commands for CosmosDB SQL, MongoDB, Cassandra, Gremlin and Table resources and resource's throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="cfdd1-244">HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfdd1-244">HDInsight</span></span>

<span data-ttu-id="cfdd1-245">このリリースには、多数の破壊的変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-245">This release contains a large number of breaking changes.</span></span>

* <span data-ttu-id="cfdd1-246">[重大な変更] `hdinsight create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-246">[BREAKING CHANGE] Renamed parameters for `hdinsight create`:</span></span>
  * <span data-ttu-id="cfdd1-247">`--storage-default-container` の名前を `--storage-container` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-247">Renamed `--storage-default-container` to `--storage-container`</span></span>
  * <span data-ttu-id="cfdd1-248">`--storage-default-filesystem` の名前を `--storage-filesystem` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-248">Renamed `--storage-default-filesystem` to `--storage-filesystem`</span></span>
* <span data-ttu-id="cfdd1-249">[重大な変更] `application create` の `--name` 引数が、クラスター名の代わりにアプリケーション名を表すように変更されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-249">[BREAKING CHANGE] Changed the `--name` argument of `application create` to represent the application name instead of the cluster name</span></span>
* <span data-ttu-id="cfdd1-250">`--cluster-name` 引数が `application create` に追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-250">Added `--cluster-name` argument to `application create` to replace old `--name` functionality</span></span>
* <span data-ttu-id="cfdd1-251">[重大な変更] `application create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-251">[BREAKING CHANGE] Renamed parameters for `application create`:</span></span>
  * <span data-ttu-id="cfdd1-252">`--application-type` の名前を `--type` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-252">Renamed `--application-type` to `--type`</span></span>
  * <span data-ttu-id="cfdd1-253">`--marketplace-identifier` の名前を `--marketplace-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-253">Renamed `--marketplace-identifier` to `--marketplace-id`</span></span>
  * <span data-ttu-id="cfdd1-254">`--https-endpoint-access-mode` の名前を `--access-mode` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-254">Renamed `--https-endpoint-access-mode` to `--access-mode`</span></span>
  * <span data-ttu-id="cfdd1-255">`--https-endpoint-destination-port` の名前を `--destination-port` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-255">Renamed  `--https-endpoint-destination-port` to `--destination-port`</span></span>
* <span data-ttu-id="cfdd1-256">[重大な変更] `application create` のパラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-256">[BREAKING CHANGE] Removed parameters for `application create`:</span></span>
  * `--https-endpoint-location`
  * `--https-endpoint-public-port`
  * `--ssh-endpoint-destination-port`
  * `--ssh-endpoint-location`
  * `--ssh-endpoint-public-port`
* <span data-ttu-id="cfdd1-257">[破壊的変更] `hdinsight resize`の `--target-instance-count` の名前を `--workernode-count` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-257">[BREAKING CHNAGE] Renamed `--target-instance-count` to `--workernode-count` for `hdinsight resize`</span></span>
* <span data-ttu-id="cfdd1-258">[重大な変更] `hdinsight script-action` グループのすべてのコマンドが、スクリプト アクションの名前として `--name` パラメーターを使用するように変更されました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-258">[BREAKING CHANGE] Changed all commands in the `hdinsight script-action` group to use the `--name` parameter as the name of the script action.</span></span>
* <span data-ttu-id="cfdd1-259">`--cluster-name` 引数がすべての `hdinsight script-action` コマンドに追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-259">Added `--cluster-name` argument to all `hdinsight script-action` commands to replace old `--name` functionality</span></span>
* <span data-ttu-id="cfdd1-260">[重大な変更] すべての `hdinsight script-action` コマンドで `--script-execution-id` の名前を `--execution-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-260">[BREAKING CHANGE] Renamed `--script-execution-id` to `--execution-id` for all `hdinsight script-action` commands</span></span>
* <span data-ttu-id="cfdd1-261">[重大な変更] 名前を `hdinsight script-action show` から `hdinsight script-action show-execution-details` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-261">[BREAKING CHANGE] Renamed `hdinsight script-action show` to `hdinsight script-action show-execution-details`</span></span>
* <span data-ttu-id="cfdd1-262">[破壊的変更] `hdinsight script-action execute --roles` に対するパラメーターを、コンマ区切りではなくスペース区切りにしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-262">[BREAKING CHNAGE] Changed parameters to `hdinsight script-action execute --roles` to be space-separated instead of comma-separated</span></span>
* <span data-ttu-id="cfdd1-263">[重大な変更] `hdinsight script-action list`の `--persisted` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-263">[BREAKING CHANGE] Removed the `--persisted` parameter of `hdinsight script-action list`</span></span>
* <span data-ttu-id="cfdd1-264">ローカル JSON ファイルへのパスまたは JSON 文字列を受け入れるように `hdinsight create --cluster-configurations` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-264">Changed the `hdinsight create --cluster-configurations` parameter to accept a path to a local JSON file or a JSON string</span></span>
* <span data-ttu-id="cfdd1-265">`hdinsight script-action list-execution-history` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-265">Added command `hdinsight script-action list-execution-history`</span></span>
* <span data-ttu-id="cfdd1-266">Log Analytics ワークスペース ID またはワークスペース名を受け入れるように `hdinsight monitor enable --workspace` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-266">Changed `hdinsight monitor enable --workspace` to accept a Log Analytics workspace ID or workspace name</span></span>
* <span data-ttu-id="cfdd1-267">`hdinsight monitor enable --primary-key` 引数を追加しました。これは、ワークスペース ID がパラメーターとして指定されている場合に必要です</span><span class="sxs-lookup"><span data-stu-id="cfdd1-267">Added the `hdinsight monitor enable --primary-key` argument, which is needed if a workspace ID is provided as the parameter</span></span>
* <span data-ttu-id="cfdd1-268">例をさらに追加し、ヘルプ メッセージの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-268">Added more examples and updated descriptions for help messages</span></span>

### <a name="interactive"></a><span data-ttu-id="cfdd1-269">Interactive</span><span class="sxs-lookup"><span data-stu-id="cfdd1-269">Interactive</span></span>

* <span data-ttu-id="cfdd1-270">読み込みエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-270">Fixed a loading error</span></span>

### <a name="kubernetes"></a><span data-ttu-id="cfdd1-271">Kubernetes</span><span class="sxs-lookup"><span data-stu-id="cfdd1-271">Kubernetes</span></span>

* <span data-ttu-id="cfdd1-272">ダッシュボードのコンテナー ポートで `https` が使用されている場合に `https` を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-272">Changed to use `https` if dashboard container port is using `https`</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-273">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-273">Network</span></span>

* <span data-ttu-id="cfdd1-274">`--yes` 引数を `network dns record-set cname delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-274">Added `--yes` argument `network dns record-set cname delete`</span></span>

### <a name="profile"></a><span data-ttu-id="cfdd1-275">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-275">Profile</span></span>

* <span data-ttu-id="cfdd1-276">リソースのアクセス トークンを取得するための `account get-access-token` に `--resource-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-276">Added `--resource-type` argument to `account get-access-token` to get resource access tokens</span></span>

### <a name="servicefabric"></a><span data-ttu-id="cfdd1-277">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cfdd1-277">ServiceFabric</span></span>

* <span data-ttu-id="cfdd1-278">sf cluster create でサポートされているすべての OS バージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-278">Added all supported os version for sf cluster create</span></span>
* <span data-ttu-id="cfdd1-279">プライマリ証明書の検証のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-279">Fixed primary certificate validation bug</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-280">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-280">Storage</span></span>

* <span data-ttu-id="cfdd1-281">`storage copy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-281">Added command `storage copy`</span></span>

## <a name="july-30-2019"></a><span data-ttu-id="cfdd1-282">2019 年 7 月 30 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-282">July 30, 2019</span></span>

<span data-ttu-id="cfdd1-283">バージョン 2.0.70</span><span class="sxs-lookup"><span data-stu-id="cfdd1-283">Version 2.0.70</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-284">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-284">ACR</span></span>

* <span data-ttu-id="cfdd1-285">問題 #9952 (`acr pack build` コマンドでの回帰) を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-285">Fixed issue #9952 (a regression in the `acr pack build` command)</span></span>
* <span data-ttu-id="cfdd1-286">`acr pack build` の既定のビルダー イメージ名を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-286">Removed the default builder image name in `acr pack build`</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-287">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-287">Appservice</span></span>

* <span data-ttu-id="cfdd1-288">リソースが見つからない場合にメッセージ表示するように `webapp config ssl` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-288">Changed `webapp config ssl` to show a message if a resource is not found</span></span>
* <span data-ttu-id="cfdd1-289">`functionapp create` がストレージ アカウントの種類 `Standard_RAGRS` を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-289">Fixed issue where `functionapp create` does not accept `Standard_RAGRS` storage account type</span></span>
* <span data-ttu-id="cfdd1-290">古いバージョンの python を使用して `webapp up` を実行すると失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-290">Fixed an issue where `webapp up` would fail if run using older versions of python</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-291">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-291">Network</span></span>

* <span data-ttu-id="cfdd1-292">`network nic ip-config add` から無効なパラメーター `--ids` を削除しました (#9861 の修正)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-292">Removed invalid parameter `--ids` from `network nic ip-config add` (fixes #9861)</span></span>
* <span data-ttu-id="cfdd1-293">#9604 を修正しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-293">Fixes #9604.</span></span> <span data-ttu-id="cfdd1-294">信頼されたルート証明書へのユーザーの関連付けをサポートするために、`network application-gateway http-settings [create|update]` に `--root-certs` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-294">Added `--root-certs` parameter to `network application-gateway http-settings [create|update]` to support user associate trusted root certificates.</span></span>
* <span data-ttu-id="cfdd1-295">`network dns record-set ns create` の引数 `--subscription` を修正しました (#9965)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-295">Fixed arguent `--subscription` for `network dns record-set ns create` (#9965)</span></span>

### <a name="rbac"></a><span data-ttu-id="cfdd1-296">RBAC</span><span class="sxs-lookup"><span data-stu-id="cfdd1-296">RBAC</span></span>

* <span data-ttu-id="cfdd1-297">`user update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-297">Added `user update` command</span></span>
* <span data-ttu-id="cfdd1-298">[非推奨] ユーザー関連コマンドで `--upn-or-object-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-298">[DEPRECATED] Deprecated `--upn-or-object-id` from user-related commands</span></span>
    * <span data-ttu-id="cfdd1-299">代替引数の `--id` を使用してください</span><span class="sxs-lookup"><span data-stu-id="cfdd1-299">Use replacement argument `--id`</span></span>
* <span data-ttu-id="cfdd1-300">ユーザー関連コマンドに `--id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-300">Added `--id` argument to user-related commands</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-301">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-301">SQL</span></span>

* <span data-ttu-id="cfdd1-302">マネージド インスタンス キーおよび TDE 保護機能の管理コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-302">Added management commands for managed instance keys and TDE protector</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-303">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-303">Storage</span></span>

* <span data-ttu-id="cfdd1-304">`storage remove` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-304">Added `storage remove` command</span></span>
* <span data-ttu-id="cfdd1-305">`storage blob update` での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-305">Fixed an issue with `storage blob update`</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-306">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-306">VM</span></span>

* <span data-ttu-id="cfdd1-307">ゾーンの詳細を出力するための新しい API バージョンを使用するように `list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-307">Changed `list-skus` to use newer api-version to output zone details</span></span>
* <span data-ttu-id="cfdd1-308">`vmss create` の `--single-placement-group` の既定値を`false` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-308">Changed default of `--single-placement-group` to `false` for `vmss create`</span></span>
* <span data-ttu-id="cfdd1-309">`[snapshot|disk] create` において ZRS ストレージ SKU を選択する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-309">Added ability to select ZRS storage SKUs for `[snapshot|disk] create`</span></span>
* <span data-ttu-id="cfdd1-310">専用ホストをサポートするために、新しいコマンド グループ `vm host` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-310">Added new command group `vm host` to support dedicated hosts</span></span>
* <span data-ttu-id="cfdd1-311">VM 専用ホストを設定するためのパラメーター `--host` と `--host-group` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-311">Added parameters `--host` and `--host-group` on `vm create` to set VM dedicated host</span></span>

## <a name="july-16-2019"></a><span data-ttu-id="cfdd1-312">2019 年 7 月 16 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-312">July 16, 2019</span></span>

<span data-ttu-id="cfdd1-313">バージョン 2.0.69</span><span class="sxs-lookup"><span data-stu-id="cfdd1-313">Version 2.0.69</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-314">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-314">Appservice</span></span>

* <span data-ttu-id="cfdd1-315">ResourceGroupName または App の名前が無効な場合に適切なエラー メッセージを返すように `webapp identity` コマンドが変更されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-315">Changed `webapp identity` commands to return a proper error message if ResourceGroupName or App name are invalid</span></span>
* <span data-ttu-id="cfdd1-316">ResourceGroup が指定されなかった場合に numberOfSites の正しい値を返すように `webapp list` が修正されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-316">Fixed `webapp list` to return the correct value for numberOfSites if no ResourceGroup was provided</span></span>
* <span data-ttu-id="cfdd1-317">`appservice plan create` と `webapp create` の副作用が修正されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-317">Fixed side-effects of `appservice plan create` and `webapp create`</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-318">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-318">Core</span></span>

* <span data-ttu-id="cfdd1-319">`--subscription` が適用不可にもかかわらず表示される問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-319">Fixed issue where `--subscription` would appear despite being not applicable</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-320">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-320">Batch</span></span>

* <span data-ttu-id="cfdd1-321">[重大な変更] `batch pool node-agent-skus list` が `batch pool supported-images list` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-321">[BREAKING CHANGE] Replaced `batch pool node-agent-skus list` with `batch pool supported-images list`</span></span>
* <span data-ttu-id="cfdd1-322">`batch pool create network` の `--json-file` オプションを使用するときに、トラフィックのソース ポートに基づいてプールへのネットワーク アクセスをブロックするセキュリティ規則のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-322">Added support for security rules blocking network access to a pool based on the source port of the traffic when using the `--json-file` option of `batch pool create network`</span></span>
* <span data-ttu-id="cfdd1-323">`batch task create`の `--json-file` オプションを使用するときに、コンテナーの作業ディレクトリまたは Batch タスクの作業ディレクトリでタスクを実行するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-323">Added support for executing the task in the container working directory or in the Batch task working directory when using the `--json-file` option of `batch task create`</span></span>
* <span data-ttu-id="cfdd1-324">`batch pool create`の `--application-package-references` オプションが、既定値でのみ動作するというエラーが修正されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-324">Fixed error in `--application-package-references` option of `batch pool create` where it would only work with defaults</span></span>

### <a name="eventhubs"></a><span data-ttu-id="cfdd1-325">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-325">Eventhubs</span></span>

* <span data-ttu-id="cfdd1-326">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-326">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="rdbms"></a><span data-ttu-id="cfdd1-327">RDBMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-327">RDBMS</span></span>

* <span data-ttu-id="cfdd1-328">レプリカ作成コマンドでレプリカ SKU を指定するためのオプション パラメーターが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-328">Added optional parameter to specify replica SKU for create replica command</span></span>
* <span data-ttu-id="cfdd1-329">MySQL レプリカの作成で CI テストが失敗する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-329">Fixed the issue with CI test failure with creating MySQL replica</span></span>

### <a name="relay"></a><span data-ttu-id="cfdd1-330">リレー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-330">Relay</span></span>

* <span data-ttu-id="cfdd1-331">クライアント承認が無効になっているときのハイブリッド接続の問題が修正されました ([#8775](https://github.com/azure/azure-cli/issues/8775))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-331">Fixed issue with hybrid connection when client authroization disabled [#8775](https://github.com/azure/azure-cli/issues/8775)</span></span>
* <span data-ttu-id="cfdd1-332">パラメーター `--requires-transport-security` を `relay wcfrelay create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-332">Added parameter `--requires-transport-security` to `relay wcfrelay create`</span></span>

### <a name="servicebus"></a><span data-ttu-id="cfdd1-333">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cfdd1-333">Servicebus</span></span>

* <span data-ttu-id="cfdd1-334">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-334">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-335">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-335">Storage</span></span>

* <span data-ttu-id="cfdd1-336">ストレージ アカウントの更新で Files AADDS を有効にします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-336">Enable Files AADDS for storage account update</span></span>
* <span data-ttu-id="cfdd1-337">修正された問題 `storage blob service-properties update --set`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-337">Fixed issue `storage blob service-properties update --set`</span></span>

## <a name="july-2-2019"></a><span data-ttu-id="cfdd1-338">2019 年 7 月 2 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-338">July 2, 2019</span></span>

<span data-ttu-id="cfdd1-339">バージョン 2.0.68</span><span class="sxs-lookup"><span data-stu-id="cfdd1-339">Version 2.0.68</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-340">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-340">Core</span></span>

* <span data-ttu-id="cfdd1-341">コマンド モジュールが再頒布可能な 1 つの Python コードに統合されました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-341">Command modules are now consolidated into a single Python distributable.</span></span> <span data-ttu-id="cfdd1-342">これにより、PyPI での多くの `azure-cli-` パッケージの直接使用が廃止されます。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-342">This deprecates direct use of many `azure-cli-` packages on PyPI.</span></span>
  <span data-ttu-id="cfdd1-343">またこれにより、インストール サイズが削減され、`pip` 経由で直接インストールしたユーザーにのみ影響が出ます。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-343">This should reduce install size and only affect users who have directly installed via `pip`.</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-344">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-344">ACR</span></span>

* <span data-ttu-id="cfdd1-345">タスクへのタイマー トリガーのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-345">Added support for Timer Triggers to Task</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-346">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-346">Appservice</span></span>

* <span data-ttu-id="cfdd1-347">既定でアプリケーション インサイトを有効にするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-347">Changed `functionapp create` to enable application insights by default</span></span>
* <span data-ttu-id="cfdd1-348">[重大な変更] 非推奨の `functionapp devops-build` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-348">[BREAKING CHANGE] Removed deprecated `functionapp devops-build` command.</span></span>
  *  <span data-ttu-id="cfdd1-349">代わりに新しいコマンド `az functionapp devops-pipeline` を使用</span><span class="sxs-lookup"><span data-stu-id="cfdd1-349">Use the new command `az functionapp devops-pipeline` instead</span></span>
* <span data-ttu-id="cfdd1-350">Linux 従量課金プランの関数アプリのプラン サポートを `functionapp deployment config-zip` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-350">Added Linux Consumption function app plan support to `functionapp deployment config-zip`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="cfdd1-351">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cfdd1-351">Cosmos DB</span></span>

* <span data-ttu-id="cfdd1-352">ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-352">Added support for disabling TTL</span></span>

### <a name="dls"></a><span data-ttu-id="cfdd1-353">DLS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-353">DLS</span></span>

* <span data-ttu-id="cfdd1-354">ADLS バージョンを更新しました (0.0.45)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-354">Updated ADLS version (0.0.45)</span></span>

### <a name="feedback"></a><span data-ttu-id="cfdd1-355">フィードバック</span><span class="sxs-lookup"><span data-stu-id="cfdd1-355">Feedback</span></span>

* <span data-ttu-id="cfdd1-356">失敗した拡張機能コマンドを報告するときに、`az feedback` はインデックスからの拡張機能のプロジェクト/リポジトリの url にブラウザーを開こうとするようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-356">When reporting a failed extension command, `az feedback` now attempts to open the browser to the project/repo url of the extension from the index</span></span>

### <a name="hdinsight"></a><span data-ttu-id="cfdd1-357">HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfdd1-357">HDInsight</span></span>

* <span data-ttu-id="cfdd1-358">[重大な変更] `oms` コマンド グループ名を `monitor` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-358">[BREAKING CHANGE] Changed `oms` command group name to `monitor`</span></span>
* <span data-ttu-id="cfdd1-359">[重大な変更] `--http-password/-p` が必須パラメーターになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-359">[BREAKING CHANGE] Made `--http-password/-p` a required parameter</span></span> 
* <span data-ttu-id="cfdd1-360">`--cluster-admin-account` および `cluster-users-group-dns` パラメーター入力候補の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-360">Added completers for `--cluster-admin-account` and `cluster-users-group-dns` parameters completer</span></span> 
* <span data-ttu-id="cfdd1-361">`cluster-users-group-dns` パラメーターを `—esp` が存在するときに必要となるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-361">Changed `cluster-users-group-dns` parameter to be required when `—esp` is present</span></span>
* <span data-ttu-id="cfdd1-362">既存の引数自動オートコンプリートすべてにタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-362">Added a timeout for all existing argument auto-completers</span></span>
* <span data-ttu-id="cfdd1-363">リソース名をリソース id に変換する際のタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-363">Added a timeout for transforming resource name to resource id</span></span>
* <span data-ttu-id="cfdd1-364">任意のリソース グループからリソースを選択するようにオートコンプリートを変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-364">Changed Auto-completers to select resources from any resource group.</span></span> <span data-ttu-id="cfdd1-365">`-g` で指定されるリソース グループとは別のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-365">It can be a different resource group than the one specified with `-g`</span></span>
* <span data-ttu-id="cfdd1-366">`hdinsight application create` コマンドで `--sub-domain-suffix` および `--disable_gateway_auth` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-366">Added support for `--sub-domain-suffix` and `--disable_gateway_auth` parameters in the `hdinsight application create` command</span></span>

### <a name="managed-services"></a><span data-ttu-id="cfdd1-367">マネージド サービス</span><span class="sxs-lookup"><span data-stu-id="cfdd1-367">Managed Services</span></span>

* <span data-ttu-id="cfdd1-368">プレビューにマネージド サービス コマンド モジュールを導入</span><span class="sxs-lookup"><span data-stu-id="cfdd1-368">Introducing managed service command module in preview</span></span>

### <a name="profile"></a><span data-ttu-id="cfdd1-369">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-369">Profile</span></span>
* <span data-ttu-id="cfdd1-370">ログアウト コマンドの `--subscription` 引数を抑制</span><span class="sxs-lookup"><span data-stu-id="cfdd1-370">Suppress `--subscription` argument for logout command</span></span>

### <a name="rbac"></a><span data-ttu-id="cfdd1-371">RBAC</span><span class="sxs-lookup"><span data-stu-id="cfdd1-371">RBAC</span></span>

* <span data-ttu-id="cfdd1-372">[重大な変更] `create-for-rbac` の `--password` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-372">[BREAKING CHANGE] Removed `--password` argument for `create-for-rbac`</span></span>
* <span data-ttu-id="cfdd1-373">AAD グラフ サーバー レプリケーションの待機時間によって発生する断続的なエラーを回避するために `--assignee-principal-type` パラメーターを `create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-373">Added `--assignee-principal-type` parameter to `create` command to avoid intermittent failures caused by AAD graph server replication latency</span></span>
* <span data-ttu-id="cfdd1-374">所有オブジェクトの一覧表示時の `ad signed-in-user` のクラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-374">Fixed a crash in `ad signed-in-user` when listing owned objects</span></span>
* <span data-ttu-id="cfdd1-375">`ad sp` によってサービス プリンシパルから適切なアプリケーションが検出されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-375">Fixed issue where `ad sp` would not find the right application from a service principal</span></span>

### <a name="rdbms"></a><span data-ttu-id="cfdd1-376">RDBMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-376">RDBMS</span></span>

* <span data-ttu-id="cfdd1-377">MariaDB のレプリケーション サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-377">Added support for replication for MariaDB</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-378">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-378">SQL</span></span>

* <span data-ttu-id="cfdd1-379">`sql db create --sample-name` に使用できる値を文書化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-379">Documented allowed values for `sql db create --sample-name`</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-380">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-380">Storage</span></span>

* <span data-ttu-id="cfdd1-381">`--as-user` を使用した `storage blob generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-381">Added user delegation SAS token support with `--as-user` to `storage blob generate-sas`</span></span> 
* <span data-ttu-id="cfdd1-382">`--as-user` を使用した `storage container generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-382">Added user delegation SAS token support with `--as-user` to `storage container generate-sas`</span></span> 

### <a name="vm"></a><span data-ttu-id="cfdd1-383">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-383">VM</span></span>

* <span data-ttu-id="cfdd1-384">`--no-wait` による実行時に `vmss create` によってエラー メッセージが返されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-384">Fixed bug where `vmss create` returns an error message when run with `--no-wait`</span></span>
* <span data-ttu-id="cfdd1-385">`vmss create --single-placement-group` のクライアント側の検証を削除しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-385">Removed client-side validation for `vmss create --single-placement-group`.</span></span> <span data-ttu-id="cfdd1-386">`--single-placement-group` が `true` に設定され、`--instance-count` が 100 より大きいか、可用性ゾーンが指定されていても失敗にはならず、この検証はコンピューティング サービスに任されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-386">Does not fail if `--single-placement-group` is set to `true` and`--instance-count` is greater than 100 or availability zones are specified, but leaves this validation to the compute service</span></span>
* <span data-ttu-id="cfdd1-387">`--latest` と共に使用したときに `[vm|vmss] extension image list` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-387">Fixed bug where `[vm|vmss] extension image list` fails when used with `--latest`</span></span>


## <a name="june-18-2019"></a><span data-ttu-id="cfdd1-388">2019 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-388">June 18, 2019</span></span>

<span data-ttu-id="cfdd1-389">バージョン 2.0.67</span><span class="sxs-lookup"><span data-stu-id="cfdd1-389">Version 2.0.67</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-390">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-390">Core</span></span>

<span data-ttu-id="cfdd1-391">このリリースでは、新しい [プレビュー] タグが導入され、コマンド グループ、コマンド、または引数がプレビュー状態である場合に、お客様により明確に通知できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-391">This release introduces a new [Preview] tag to more clearly communicate to customers when a command group, command or argument is in preview status.</span></span> <span data-ttu-id="cfdd1-392">以前は、これはヘルプ テキストで通知されていたか、コマンド モジュールのバージョン番号によって暗黙的に通知されていました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-392">This was previously called out in help text or communicated implicitly by the command module version number.</span></span>
<span data-ttu-id="cfdd1-393">CLI では、将来、個々のパッケージのバージョン番号が削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-393">The CLI will be removing version numbers for individual packages in the future.</span></span> <span data-ttu-id="cfdd1-394">コマンドがプレビュー状態の場合は、そのすべての引数もプレビュー状態です。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-394">If a command is in preview, all of its arguments are as well.</span></span> <span data-ttu-id="cfdd1-395">コマンド グループにプレビュー状態のラベルが付いている場合、すべてのコマンドと引数もプレビュー状態と見なされます。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-395">If a command group is labeled as being in preview, then all commands and arguments are considered to be in preview as well.</span></span>

<span data-ttu-id="cfdd1-396">この変更の結果、このリリースでは、一部のコマンド グループが "突然" プレビュー状態になったように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-396">As a result of this change, several command groups may seem to "suddenly" appear to be in a preview status with this release.</span></span> <span data-ttu-id="cfdd1-397">ほとんどのパッケージがプレビュー状態にあったのですが、このリリースでは一般提供と見なされていることがその真相です</span><span class="sxs-lookup"><span data-stu-id="cfdd1-397">What actually happened is that most packages were in a preview status, but are being deemed GA with this release</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-398">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-398">ACR</span></span>
* <span data-ttu-id="cfdd1-399">'acr check-health' コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-399">Added 'acr check-health' command</span></span>
* <span data-ttu-id="cfdd1-400">AAD トークンおよび外部コマンドの取得に関するエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-400">Improved error handling for AAD tokens and for retrieving external commands</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-401">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-401">ACS</span></span>
* <span data-ttu-id="cfdd1-402">非推奨の ACS コマンドがヘルプ ビューで非表示になりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-402">Deprecated ACS commands are now hidden from help view</span></span>

### <a name="ams"></a><span data-ttu-id="cfdd1-403">AMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-403">AMS</span></span>
* <span data-ttu-id="cfdd1-404">[重大な変更] archive-window-length および key-frame-interval-duration の ISO 8601 時間文字列を返すように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-404">[BREAKING CHANGE] Changed to return ISO 8601 time strings for archive-window-length and key-frame-interval-duration</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-405">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-405">AppService</span></span>
* <span data-ttu-id="cfdd1-406">`webapp deleted list` および `webapp deleted restore` に対してロケーション ベースのルーティングを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-406">Added location based routing for `webapp deleted list` and `webapp deleted restore`</span></span>
* <span data-ttu-id="cfdd1-407">Azure Cloud Shell で Web アプリのログに記録されたターゲット URL ("You can launch the app at...") がクリックできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-407">Fixed issue where webapp up logged target URL ("You can launch the app at...") was not clickable in Azure Cloud Shell</span></span>
* <span data-ttu-id="cfdd1-408">一部の SKU でのアプリ作成が AlwaysOn エラーで失敗するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-408">Fixed an issue where creating apps with the some SKUs was failing with an AlwaysOn error</span></span>
* <span data-ttu-id="cfdd1-409">`[appservice|webapp] create` に事前検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-409">Added pre-validation to `[appservice|webapp] create`</span></span>
* <span data-ttu-id="cfdd1-410">正しい actionHostName を使用するように `[webapp|functionapp] traffic-routing` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-410">Fixed `[webapp|functionapp] traffic-routing` to use the correct actionHostName</span></span>
* <span data-ttu-id="cfdd1-411">`functionapp` コマンドにスロット サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-411">Added slot support to `functionapp` commands</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-412">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-412">Batch</span></span>
* <span data-ttu-id="cfdd1-413">共有キー認証の過度のエラー報告による AAD 認証の回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-413">Fixed AAD auth regression caused by over-aggressive error reporting for Shared Key Auth</span></span>

### <a name="batchai"></a><span data-ttu-id="cfdd1-414">BatchAI</span><span class="sxs-lookup"><span data-stu-id="cfdd1-414">BatchAI</span></span>
* <span data-ttu-id="cfdd1-415">BatchAI コマンドが非推奨となり、非表示になりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-415">BatchAI commands are now deprecated and hidden</span></span>

### <a name="botservice"></a><span data-ttu-id="cfdd1-416">BotService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-416">BotService</span></span>
* <span data-ttu-id="cfdd1-417">v3 SDK をサポートするコマンドに "廃止されたサポート"/"保守モード" 警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-417">Added "discontinued support"/"maintenance mode" warning messages for commands that support the v3 SDK</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="cfdd1-418">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cfdd1-418">CosmosDB</span></span>
* <span data-ttu-id="cfdd1-419">[非推奨] `cosmosdb list-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-419">[DEPRECATED] Deprecated the `cosmosdb list-keys` command</span></span>
* <span data-ttu-id="cfdd1-420">`cosmosdb keys list` コマンドを追加しました。`cosmosdb list-keys` に置き換わるものです</span><span class="sxs-lookup"><span data-stu-id="cfdd1-420">Added the `cosmosdb keys list` command - replaces `cosmosdb list-keys`</span></span>
* <span data-ttu-id="cfdd1-421">`cosmsodb create/update`:"isZoneRedundant" プロパティを設定できるように --location の新しいフォーマットを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-421">`cosmsodb create/update`: Added new format for --location to allow setting "isZoneRedundant" property.</span></span> <span data-ttu-id="cfdd1-422">古いフォーマットを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-422">Deprecated old format</span></span>

### <a name="eventgrid"></a><span data-ttu-id="cfdd1-423">EventGrid</span><span class="sxs-lookup"><span data-stu-id="cfdd1-423">EventGrid</span></span>
* <span data-ttu-id="cfdd1-424">ドメイン CRUD 操作のための `eventgrid domain` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-424">Added `eventgrid domain` commands for domain CRUD operations</span></span>
* <span data-ttu-id="cfdd1-425">ドメイン トピック CRUD 操作のための `eventgrid domain topic` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-425">Added `eventgrid domain topic` commands for domain topics CRUD operations</span></span>
* <span data-ttu-id="cfdd1-426">OData 構文を使用して結果をフィルタリングするための `--odata-query` 引数を `eventgrid [topic|event-subscription] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-426">Added `--odata-query` argument to `eventgrid [topic|event-subscription] list` for filtering results using OData syntax</span></span>
* <span data-ttu-id="cfdd1-427">`event-subscription create/update`:`--endpoint-type` パラメーターの新しい値として servicebusqueue を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-427">`event-subscription create/update`: Added servicebusqueue as new values for the `--endpoint-type` parameter</span></span>
* <span data-ttu-id="cfdd1-428">[重大な変更] `eventgrid event-subscription [create|update]` での `--included-event-types All` のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-428">[BREAKING CHANGE] Removed support for `--included-event-types All` with `eventgrid event-subscription [create|update]`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="cfdd1-429">HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfdd1-429">HDInsight</span></span>
* <span data-ttu-id="cfdd1-430">`hdinsight create` コマンドでの `--ssh-public-key` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-430">Added support for `--ssh-public-key` parameter in `hdinsight create` command</span></span>

### <a name="iot"></a><span data-ttu-id="cfdd1-431">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-431">IoT</span></span>
* <span data-ttu-id="cfdd1-432">承認ポリシー キーの再生成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-432">Added support to regenerate authorization policy keys</span></span>
* <span data-ttu-id="cfdd1-433">DigitalTwin リポジトリ プロビジョニング サービスの SDK およびサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-433">Added SDK and support for DigitalTwin Repository Provisioning Service</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-434">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-434">Network</span></span>
* <span data-ttu-id="cfdd1-435">Nat Gateway に対するゾーン サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-435">Added Zone support for Nat Gateway</span></span>
* <span data-ttu-id="cfdd1-436">`network list-service-tags` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-436">Added command `network list-service-tags`</span></span>
* <span data-ttu-id="cfdd1-437">ユーザーがワイルドカード A レコードをインポートできない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-437">Fixed issue with `dns zone import` where users could not import wildcard A records</span></span>
* <span data-ttu-id="cfdd1-438">特定のリージョンでフロー ロギングを有効にできない `watcher flow-log configure` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-438">Fixed issue with `watcher flow-log configure` where flow logging could not be enabled in certain regions</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-439">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-439">Resource</span></span>
* <span data-ttu-id="cfdd1-440">REST 呼び出しを行うための `az rest` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-440">Added `az rest` command for making REST calls</span></span>
* <span data-ttu-id="cfdd1-441">リソース グループまたはサブスクリプション レベル`--scope` で `policy assignment list` を使用する場合のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-441">Fixed error when using `policy assignment list` with a resource group or subscription level `--scope`</span></span>

### <a name="servicebus"></a><span data-ttu-id="cfdd1-442">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cfdd1-442">ServiceBus</span></span>
* <span data-ttu-id="cfdd1-443">`servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319) での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-443">Fixed issue with `servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319)</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-444">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-444">SQL</span></span>
* <span data-ttu-id="cfdd1-445">`--location` を `sql [server|mi] create` のオプションに変更しました - 指定されていない場合、リソース グループの場所を使用します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-445">Changed `--location` to be optional for `sql [server|mi] create` - uses resource group location if not specified</span></span>
* <span data-ttu-id="cfdd1-446">`sql db list-editions --available` の "'NoneType' object is not iterable" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-446">Fixed "'NoneType' object is not iterable" error for `sql db list-editions --available`</span></span>

### <a name="sqlvm"></a><span data-ttu-id="cfdd1-447">SQLVm</span><span class="sxs-lookup"><span data-stu-id="cfdd1-447">SQLVm</span></span>
* <span data-ttu-id="cfdd1-448">[破壊的変更] `--license-type` パラメーターを必要とするように `sql vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-448">[BREAKING CHNAGE] Changed `sql vm create` to require `--license-type` parameter</span></span>
* <span data-ttu-id="cfdd1-449">sql vm の作成または更新時に SQL イメージ SKU を設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-449">Changed to allow setting SQL image SKU when creating or updating a sql vm</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-450">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-450">Storage</span></span>
* <span data-ttu-id="cfdd1-451">`storage container generate-sas` のアカウント キーが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-451">Fixed issue with missing account key for `storage container generate-sas`</span></span>
* <span data-ttu-id="cfdd1-452">Linux での `storage blob sync` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-452">Fixed issue with `storage blob sync` on Linux</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-453">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-453">VM</span></span>
* <span data-ttu-id="cfdd1-454">[プレビュー] VM イメージを構築するための `vm image template` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-454">[PREVIEW] Added `vm image template` commands to build VM images</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="cfdd1-455">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-455">June 4, 2019</span></span>

<span data-ttu-id="cfdd1-456">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="cfdd1-456">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-457">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-457">Core</span></span>
* <span data-ttu-id="cfdd1-458">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-458">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-459">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-459">ACR</span></span>
* <span data-ttu-id="cfdd1-460">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-460">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-461">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-461">ACS</span></span>
* <span data-ttu-id="cfdd1-462">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-462">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="cfdd1-463">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-463">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-464">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-464">Batch</span></span>
* <span data-ttu-id="cfdd1-465">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-465">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="cfdd1-466">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-466">IoT</span></span>
* <span data-ttu-id="cfdd1-467">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-467">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-468">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-468">Network</span></span>
* <span data-ttu-id="cfdd1-469">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-469">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="cfdd1-470">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-470">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="cfdd1-471">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-471">Resource</span></span>
* <span data-ttu-id="cfdd1-472">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-472">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-473">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-473">Role</span></span>
* <span data-ttu-id="cfdd1-474">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-474">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="cfdd1-475">Compute</span><span class="sxs-lookup"><span data-stu-id="cfdd1-475">Compute</span></span>
* <span data-ttu-id="cfdd1-476">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-476">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="cfdd1-477">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-477">May 21, 2019</span></span>

<span data-ttu-id="cfdd1-478">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="cfdd1-478">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-479">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-479">Core</span></span>
* <span data-ttu-id="cfdd1-480">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-480">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="cfdd1-481">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-481">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="cfdd1-482">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-482">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-483">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-483">ACR</span></span>
* <span data-ttu-id="cfdd1-484">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-484">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-485">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-485">ACS</span></span>
* <span data-ttu-id="cfdd1-486">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-486">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-487">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-487">AppService</span></span>
* <span data-ttu-id="cfdd1-488">[非推奨] `functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-488">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="cfdd1-489">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-489">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="cfdd1-490">[重大な変更] `--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-490">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="cfdd1-491">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-491">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="cfdd1-492">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-492">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="cfdd1-493">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-493">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="cfdd1-494">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-494">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="cfdd1-495">BotService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-495">BotService</span></span>
* <span data-ttu-id="cfdd1-496">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-496">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="cfdd1-497">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-497">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="cfdd1-498">消費</span><span class="sxs-lookup"><span data-stu-id="cfdd1-498">Consumption</span></span>
* <span data-ttu-id="cfdd1-499">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-499">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="cfdd1-500">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-500">IoT</span></span>
* <span data-ttu-id="cfdd1-501">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-501">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-502">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-502">Network</span></span>
* [重大な変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="cfdd1-504">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-504">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="cfdd1-505">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-505">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="cfdd1-506">RDBMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-506">RDBMS</span></span>
* <span data-ttu-id="cfdd1-507">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-507">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="cfdd1-508">RBAC</span><span class="sxs-lookup"><span data-stu-id="cfdd1-508">RBAC</span></span>
* <span data-ttu-id="cfdd1-509">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-509">Added support for management group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-510">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-510">Storage</span></span>
* <span data-ttu-id="cfdd1-511">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="cfdd1-511">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="cfdd1-512">Compute</span><span class="sxs-lookup"><span data-stu-id="cfdd1-512">Compute</span></span>
* <span data-ttu-id="cfdd1-513">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-513">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="cfdd1-514">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-514">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="cfdd1-515">__メモ__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-515">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="cfdd1-516">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-516">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="cfdd1-517">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-517">May 6, 2019</span></span>

<span data-ttu-id="cfdd1-518">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="cfdd1-518">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-519">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-519">ACS</span></span>
* <span data-ttu-id="cfdd1-520">[重大な変更] `--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-520">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="cfdd1-521">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-521">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="cfdd1-522">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-522">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="cfdd1-523">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-523">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-524">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-524">Appservice</span></span>
* <span data-ttu-id="cfdd1-525">[非推奨] `functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-525">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="cfdd1-526">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-526">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="cfdd1-527">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-527">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="cfdd1-528">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-528">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="cfdd1-529">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-529">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="cfdd1-530">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-530">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="cfdd1-531">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-531">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="cfdd1-532">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-532">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="cfdd1-533">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-533">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="cfdd1-534">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-534">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-535">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-535">Batch</span></span>
* <span data-ttu-id="cfdd1-536">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-536">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="cfdd1-537">Botservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-537">Botservice</span></span>
* <span data-ttu-id="cfdd1-538">[重大な変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-538">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="cfdd1-539">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-539">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="cfdd1-540">[重大な変更] `--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-540">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="cfdd1-541">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-541">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="cfdd1-542">[重大な変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-542">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="cfdd1-543">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-543">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="cfdd1-544">[重大な変更] `bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-544">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="cfdd1-545">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-545">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="cfdd1-546">[重大な変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-546">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="cfdd1-547">[重大な変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-547">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="cfdd1-548">[重大な変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-548">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="cfdd1-549">[重大な変更] `Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-549">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="cfdd1-550">[重大な変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-550">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="cfdd1-551">[重大な変更] `SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-551">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="cfdd1-552">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-552">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="cfdd1-553">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-553">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="cfdd1-554">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-554">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="cfdd1-555">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-555">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="cfdd1-556">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-556">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="cfdd1-557">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-557">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="cfdd1-558">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-558">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="cfdd1-559">構成</span><span class="sxs-lookup"><span data-stu-id="cfdd1-559">Configure</span></span>
* <span data-ttu-id="cfdd1-560">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-560">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="cfdd1-561">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-561">Eventhubs</span></span>
* <span data-ttu-id="cfdd1-562">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-562">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="cfdd1-563">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-563">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-564">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-564">Network</span></span>
* <span data-ttu-id="cfdd1-565">[重大な変更] `vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-565">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="cfdd1-566">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="cfdd1-566">Policy Insights</span></span>
* <span data-ttu-id="cfdd1-567">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-567">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-568">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-568">Role</span></span>
* <span data-ttu-id="cfdd1-569">[非推奨] `create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-569">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="cfdd1-570">Service Bus</span><span class="sxs-lookup"><span data-stu-id="cfdd1-570">Service Bus</span></span>
* <span data-ttu-id="cfdd1-571">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-571">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="cfdd1-572">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-572">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="cfdd1-573">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-573">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-574">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-574">SQL</span></span>
* <span data-ttu-id="cfdd1-575">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-575">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-576">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-576">VM</span></span>
* <span data-ttu-id="cfdd1-577">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-577">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="cfdd1-578">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-578">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="cfdd1-579">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-579">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="cfdd1-580">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-580">Added new `ppg` command group for managing Proximity Placement Groups</span></span>
* <span data-ttu-id="cfdd1-581">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-581">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="cfdd1-582">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-582">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="cfdd1-583">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-583">April 23, 2019</span></span>

<span data-ttu-id="cfdd1-584">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="cfdd1-584">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-585">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-585">ACS</span></span>
* <span data-ttu-id="cfdd1-586">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-586">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="cfdd1-587">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-587">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="cfdd1-588">AMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-588">AMS</span></span>
* <span data-ttu-id="cfdd1-589">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-589">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-590">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-590">AppService</span></span>
* <span data-ttu-id="cfdd1-591">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-591">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="cfdd1-592">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-592">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="cfdd1-593">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-593">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="cfdd1-594">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-594">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="cfdd1-595">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-595">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="cfdd1-596">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-596">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="cfdd1-597">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-597">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="cfdd1-598">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-598">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="cfdd1-599">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-599">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="cfdd1-600">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="cfdd1-600">Deployment Manager</span></span>
* <span data-ttu-id="cfdd1-601">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-601">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="cfdd1-602">ラボ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-602">Lab</span></span>
* <span data-ttu-id="cfdd1-603">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-603">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-604">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-604">Network</span></span>
* <span data-ttu-id="cfdd1-605">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-605">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-606">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-606">Resource</span></span>
* <span data-ttu-id="cfdd1-607">[非推奨] `resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-607">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="cfdd1-608">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-608">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="cfdd1-609">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-609">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="cfdd1-610">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-610">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-611">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-611">SQL</span></span>
* <span data-ttu-id="cfdd1-612">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-612">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="cfdd1-613">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-613">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="cfdd1-614">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-614">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="cfdd1-615">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-615">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-616">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-616">Storage</span></span>
* <span data-ttu-id="cfdd1-617">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-617">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-618">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-618">VM</span></span>
* <span data-ttu-id="cfdd1-619">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-619">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="cfdd1-620">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-620">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="cfdd1-621">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-621">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="cfdd1-622">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-622">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-623">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-623">Core</span></span>
* <span data-ttu-id="cfdd1-624">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-624">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-625">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-625">ACR</span></span>
* <span data-ttu-id="cfdd1-626">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-626">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="cfdd1-627">AMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-627">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="cfdd1-630">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-630">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="cfdd1-631">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-631">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-632">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-632">AppService</span></span>
* <span data-ttu-id="cfdd1-633">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-633">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="cfdd1-634">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-634">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="cfdd1-635">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-635">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="cfdd1-636">[重大な変更] `devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-636">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="cfdd1-637">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-637">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="cfdd1-638">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-638">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="cfdd1-639">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-639">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="cfdd1-640">CDN</span><span class="sxs-lookup"><span data-stu-id="cfdd1-640">CDN</span></span>
* <span data-ttu-id="cfdd1-641">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-641">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="cfdd1-642">フィードバック</span><span class="sxs-lookup"><span data-stu-id="cfdd1-642">Feedback</span></span>
* <span data-ttu-id="cfdd1-643">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-643">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="cfdd1-644">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-644">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="cfdd1-645">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-645">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-646">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-646">Monitor</span></span>
* <span data-ttu-id="cfdd1-647">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-647">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="cfdd1-648">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-648">Network</span></span>
* <span data-ttu-id="cfdd1-649">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-649">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="cfdd1-650">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-650">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="cfdd1-651">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-651">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="cfdd1-652">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-652">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="cfdd1-653">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-653">PrivateDNS</span></span>
* <span data-ttu-id="cfdd1-654">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-654">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-655">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-655">Resource</span></span>
* <span data-ttu-id="cfdd1-656">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-656">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-657">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-657">Role</span></span>
* <span data-ttu-id="cfdd1-658">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-658">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="cfdd1-659">[重大な変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-659">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-660">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-660">SQL</span></span>
* <span data-ttu-id="cfdd1-661">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-661">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-662">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-662">Storage</span></span>
* <span data-ttu-id="cfdd1-663">[重大な変更] `storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-663">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="cfdd1-664">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-664">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="cfdd1-665">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-665">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="cfdd1-666">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-666">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="cfdd1-667">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-667">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="cfdd1-668">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-668">Core</span></span>
* <span data-ttu-id="cfdd1-669">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-669">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="cfdd1-670">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-670">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="cfdd1-671">クラウド</span><span class="sxs-lookup"><span data-stu-id="cfdd1-671">Cloud</span></span>
* <span data-ttu-id="cfdd1-672">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-672">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-673">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-673">ACR</span></span>
* <span data-ttu-id="cfdd1-674">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-674">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="cfdd1-675">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-675">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="cfdd1-676">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-676">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="cfdd1-677">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-677">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-678">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-678">AppService</span></span>
* <span data-ttu-id="cfdd1-679">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-679">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="cfdd1-680">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-680">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="cfdd1-681">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="cfdd1-681">BOT Service</span></span>
* <span data-ttu-id="cfdd1-682">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-682">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="cfdd1-683">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-683">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="cfdd1-684">[重大な変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-684">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="cfdd1-685">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-685">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="cfdd1-686">CDN</span><span class="sxs-lookup"><span data-stu-id="cfdd1-686">CDN</span></span>
* <span data-ttu-id="cfdd1-687">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-687">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [重大な変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="cfdd1-689">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-689">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="cfdd1-690">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-690">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="cfdd1-691">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="cfdd1-691">Cosmosdb</span></span>
* <span data-ttu-id="cfdd1-692">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-692">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="cfdd1-693">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-693">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="cfdd1-694">Interactive</span><span class="sxs-lookup"><span data-stu-id="cfdd1-694">Interactive</span></span>
* <span data-ttu-id="cfdd1-695">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-695">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-696">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-696">Monitor</span></span>
* <span data-ttu-id="cfdd1-697">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-697">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-698">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-698">Network</span></span>
* <span data-ttu-id="cfdd1-699">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-699">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="cfdd1-700">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-700">Profile</span></span>
* <span data-ttu-id="cfdd1-701">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-701">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="cfdd1-702">Postgres</span><span class="sxs-lookup"><span data-stu-id="cfdd1-702">Postgres</span></span> 
* <span data-ttu-id="cfdd1-703">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-703">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="cfdd1-704">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-704">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-705">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-705">Resource</span></span>
* <span data-ttu-id="cfdd1-706">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-706">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="cfdd1-707">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-707">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="cfdd1-708">Graph</span><span class="sxs-lookup"><span data-stu-id="cfdd1-708">Graph</span></span>
* <span data-ttu-id="cfdd1-709">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-709">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="cfdd1-710">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-710">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="cfdd1-711">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-711">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="cfdd1-712">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-712">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="cfdd1-713">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-713">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-714">storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-714">storage</span></span>
* <span data-ttu-id="cfdd1-715">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-715">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="cfdd1-716">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-716">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="cfdd1-717">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-717">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="cfdd1-718">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-718">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-719">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-719">VM</span></span>
* <span data-ttu-id="cfdd1-720">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-720">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="cfdd1-721">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-721">March 12, 2019</span></span>

<span data-ttu-id="cfdd1-722">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="cfdd1-722">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-723">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-723">Core</span></span>

* <span data-ttu-id="cfdd1-724">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-724">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-725">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-725">ACR</span></span>

* <span data-ttu-id="cfdd1-726">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-726">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-727">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-727">ACS</span></span>

* <span data-ttu-id="cfdd1-728">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-728">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="cfdd1-729">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-729">AppService</span></span>

* <span data-ttu-id="cfdd1-730">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-730">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="cfdd1-731">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-731">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="cfdd1-732">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-732">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="cfdd1-733">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-733">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="cfdd1-734">Botservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-734">Botservice</span></span>

* <span data-ttu-id="cfdd1-735">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-735">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="cfdd1-736">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-736">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="cfdd1-737">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-737">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="cfdd1-738">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-738">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-739">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-739">Container</span></span>

* <span data-ttu-id="cfdd1-740">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-740">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="cfdd1-741">EventHub</span><span class="sxs-lookup"><span data-stu-id="cfdd1-741">EventHub</span></span>

* <span data-ttu-id="cfdd1-742">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-742">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="cfdd1-743">Find</span><span class="sxs-lookup"><span data-stu-id="cfdd1-743">Find</span></span>

* <span data-ttu-id="cfdd1-744">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="cfdd1-744">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="cfdd1-745">HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfdd1-745">HDInsight</span></span>

* <span data-ttu-id="cfdd1-746">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-746">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-747">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-747">Network</span></span>

* <span data-ttu-id="cfdd1-748">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-748">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="cfdd1-749">Rdbms</span><span class="sxs-lookup"><span data-stu-id="cfdd1-749">Rdbms</span></span>

* <span data-ttu-id="cfdd1-750">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-750">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-751">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-751">Role</span></span>

* <span data-ttu-id="cfdd1-752">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-752">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="cfdd1-753">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-753">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="cfdd1-754">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="cfdd1-754">Service Fabric</span></span>

* <span data-ttu-id="cfdd1-755">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-755">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="cfdd1-756">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-756">February 26, 2019</span></span>

<span data-ttu-id="cfdd1-757">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="cfdd1-757">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-758">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-758">Core</span></span>

* <span data-ttu-id="cfdd1-759">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-759">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-760">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-760">ACR</span></span>

* <span data-ttu-id="cfdd1-761">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-761">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="cfdd1-762">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-762">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-763">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-763">ACS</span></span>

* <span data-ttu-id="cfdd1-764">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-764">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-765">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-765">AppService</span></span>

* <span data-ttu-id="cfdd1-766">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-766">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-767">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-767">Batch</span></span>
* <span data-ttu-id="cfdd1-768">[重大な変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-768">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="cfdd1-769">[重大な変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-769">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="cfdd1-770">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-770">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="cfdd1-771">[重大な変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-771">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="cfdd1-772">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-772">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="cfdd1-773">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-773">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="cfdd1-774">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cfdd1-774">CosmosDB</span></span>

* <span data-ttu-id="cfdd1-775">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-775">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="cfdd1-776">Kusto</span><span class="sxs-lookup"><span data-stu-id="cfdd1-776">Kusto</span></span>

* <span data-ttu-id="cfdd1-777">[重大な変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-777">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-778">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-778">Network</span></span>

* <span data-ttu-id="cfdd1-779">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-779">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="cfdd1-780">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-780">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="cfdd1-781">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-781">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="cfdd1-782">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-782">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="cfdd1-783">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-783">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="cfdd1-784">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-784">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="cfdd1-785">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-785">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-786">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-786">Resource</span></span>

* <span data-ttu-id="cfdd1-787">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-787">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="cfdd1-788">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-788">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="cfdd1-789">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-789">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="cfdd1-790">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-790">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="cfdd1-791">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-791">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-792">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-792">Role</span></span>

* <span data-ttu-id="cfdd1-793">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-793">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-794">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-794">VM</span></span>

* <span data-ttu-id="cfdd1-795">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-795">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="cfdd1-796">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-796">February 12, 2019</span></span>

<span data-ttu-id="cfdd1-797">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="cfdd1-797">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-798">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-798">Core</span></span>

* <span data-ttu-id="cfdd1-799">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-799">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="cfdd1-800">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-800">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-801">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-801">ACR</span></span>
* <span data-ttu-id="cfdd1-802">[重大な変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-802">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="cfdd1-803">[重大な変更] `acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-803">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-804">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-804">ACS</span></span>
* <span data-ttu-id="cfdd1-805">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-805">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="cfdd1-806">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-806">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="cfdd1-807">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-807">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="cfdd1-808">AMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-808">AMS</span></span>
* <span data-ttu-id="cfdd1-809">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-809">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="cfdd1-810">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-810">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-811">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-811">Appservice</span></span>
* <span data-ttu-id="cfdd1-812">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-812">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="cfdd1-813">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-813">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="cfdd1-814">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-814">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="cfdd1-815">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-815">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="cfdd1-816">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-816">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="cfdd1-817">Botservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-817">Botservice</span></span>
* <span data-ttu-id="cfdd1-818">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-818">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="cfdd1-819">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-819">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="cfdd1-820">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-820">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="cfdd1-821">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-821">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="cfdd1-822">[非推奨] `--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-822">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="cfdd1-823">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-823">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="cfdd1-824">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-824">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="cfdd1-825">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-825">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="cfdd1-826">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="cfdd1-826">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="cfdd1-827">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-827">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="cfdd1-828">Key Vault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-828">Key Vault</span></span>
* <span data-ttu-id="cfdd1-829">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-829">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-830">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-830">Monitor</span></span>
* <span data-ttu-id="cfdd1-831">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-831">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-832">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-832">Network</span></span>
* <span data-ttu-id="cfdd1-833">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-833">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="cfdd1-834">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-834">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="cfdd1-835">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-835">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="cfdd1-836">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-836">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="cfdd1-837">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="cfdd1-837">Policy Insights</span></span>
* <span data-ttu-id="cfdd1-838">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-838">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="cfdd1-839">RDBMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-839">RDBMS</span></span>
* <span data-ttu-id="cfdd1-840">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-840">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="cfdd1-841">Redis</span><span class="sxs-lookup"><span data-stu-id="cfdd1-841">Redis</span></span>
* <span data-ttu-id="cfdd1-842">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-842">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="cfdd1-843">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-843">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="cfdd1-844">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-844">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="cfdd1-845">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-845">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="cfdd1-846">[重大な変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-846">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="cfdd1-847">[重大な変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-847">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="cfdd1-848">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-848">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-849">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-849">Role</span></span>
* <span data-ttu-id="cfdd1-850">[重大な変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-850">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="cfdd1-851">SQL VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-851">SQL VM</span></span>
* <span data-ttu-id="cfdd1-852">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-852">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-853">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-853">VM</span></span>
* <span data-ttu-id="cfdd1-854">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-854">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="cfdd1-855">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-855">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="cfdd1-856">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-856">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="cfdd1-857">[重大な変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-857">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="cfdd1-858">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-858">January 31, 2019</span></span>

<span data-ttu-id="cfdd1-859">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="cfdd1-859">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-860">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-860">Core</span></span>

* <span data-ttu-id="cfdd1-861">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-861">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="cfdd1-862">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-862">January 28, 2019</span></span>

<span data-ttu-id="cfdd1-863">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="cfdd1-863">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-864">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-864">ACR</span></span>
* <span data-ttu-id="cfdd1-865">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-865">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-866">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-866">ACS</span></span>
* <span data-ttu-id="cfdd1-867">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-867">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="cfdd1-868">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-868">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="cfdd1-869">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-869">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="cfdd1-870">AMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-870">AMS</span></span>
* <span data-ttu-id="cfdd1-871">[重大な変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-871">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="cfdd1-872">[重大な変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-872">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-873">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-873">Appservice</span></span>
* <span data-ttu-id="cfdd1-874">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-874">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="cfdd1-875">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-875">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="cfdd1-876">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-876">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-877">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-877">Container</span></span>
* <span data-ttu-id="cfdd1-878">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-878">Added `container start` command</span></span>
* <span data-ttu-id="cfdd1-879">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-879">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="cfdd1-880">EventGrid</span><span class="sxs-lookup"><span data-stu-id="cfdd1-880">EventGrid</span></span>
* <span data-ttu-id="cfdd1-881">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-881">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="cfdd1-882">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-882">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="cfdd1-883">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-883">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="cfdd1-884">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-884">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="cfdd1-885">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-885">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="cfdd1-886">HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfdd1-886">HDInsight</span></span>
* <span data-ttu-id="cfdd1-887">[重大な変更] `hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-887">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="cfdd1-888">[重大な変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-888">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="cfdd1-889">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-889">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="cfdd1-890">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-890">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="cfdd1-891">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-891">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="cfdd1-892">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-892">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="cfdd1-893">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-893">IoT</span></span>
* <span data-ttu-id="cfdd1-894">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-894">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="cfdd1-895">Kusto</span><span class="sxs-lookup"><span data-stu-id="cfdd1-895">Kusto</span></span>
* <span data-ttu-id="cfdd1-896">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-896">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-897">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-897">Monitor</span></span>
* <span data-ttu-id="cfdd1-898">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-898">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="cfdd1-899">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-899">Profile</span></span>
* <span data-ttu-id="cfdd1-900">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-900">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-901">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-901">Network</span></span>
* <span data-ttu-id="cfdd1-902">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-902">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="cfdd1-903">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-903">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-904">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-904">Resource</span></span>
* <span data-ttu-id="cfdd1-905">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-905">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="cfdd1-906">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-906">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="cfdd1-907">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="cfdd1-907">SQL Virtual Machine</span></span>
* <span data-ttu-id="cfdd1-908">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-908">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-909">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-909">Storage</span></span>
* <span data-ttu-id="cfdd1-910">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-910">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="cfdd1-911">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-911">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-912">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-912">VM</span></span>
* <span data-ttu-id="cfdd1-913">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-913">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="cfdd1-914">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-914">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="cfdd1-915">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-915">January 15, 2019</span></span>

<span data-ttu-id="cfdd1-916">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="cfdd1-916">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-917">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-917">ACR</span></span>
* <span data-ttu-id="cfdd1-918">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-918">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="cfdd1-919">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-919">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="cfdd1-920">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-920">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="cfdd1-921">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-921">ACS</span></span>
* <span data-ttu-id="cfdd1-922">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-922">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-923">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-923">Appservice</span></span>
* <span data-ttu-id="cfdd1-924">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-924">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="cfdd1-925">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-925">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="cfdd1-926">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-926">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="cfdd1-927">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-927">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="cfdd1-928">Botservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-928">Botservice</span></span>
* <span data-ttu-id="cfdd1-929">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-929">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="cfdd1-930">構成</span><span class="sxs-lookup"><span data-stu-id="cfdd1-930">Configure</span></span>
* <span data-ttu-id="cfdd1-931">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-931">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="cfdd1-932">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cfdd1-932">CosmosDB</span></span>
* <span data-ttu-id="cfdd1-933">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-933">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="cfdd1-934">HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfdd1-934">HDInsight</span></span>
* <span data-ttu-id="cfdd1-935">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-935">Added commands for managing applications</span></span>
* <span data-ttu-id="cfdd1-936">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-936">Added commands for managing script actions</span></span>
* <span data-ttu-id="cfdd1-937">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-937">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="cfdd1-938">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-938">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="cfdd1-939">[重大な変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-939">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-940">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-940">Network</span></span>
* <span data-ttu-id="cfdd1-941">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-941">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="cfdd1-942">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-942">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="cfdd1-943">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-943">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="cfdd1-944">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-944">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-945">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-945">Role</span></span>
* <span data-ttu-id="cfdd1-946">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-946">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="cfdd1-947">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="cfdd1-947">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="cfdd1-948">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-948">Security</span></span>
* <span data-ttu-id="cfdd1-949">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-949">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-950">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-950">Storage</span></span>
* <span data-ttu-id="cfdd1-951">[重大な変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-951">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="cfdd1-952">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="cfdd1-952">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="cfdd1-953">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-953">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="cfdd1-954">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-954">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="cfdd1-955">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-955">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-956">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-956">VM</span></span>
* <span data-ttu-id="cfdd1-957">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-957">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="cfdd1-958">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-958">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="cfdd1-959">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-959">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="cfdd1-960">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-960">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="cfdd1-961">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-961">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="cfdd1-962">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-962">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="cfdd1-963">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-963">December 20, 2018</span></span>

<span data-ttu-id="cfdd1-964">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="cfdd1-964">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="cfdd1-965">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-965">Appservice</span></span>
* <span data-ttu-id="cfdd1-966">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-966">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="cfdd1-967">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-967">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="cfdd1-968">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-968">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="cfdd1-969">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="cfdd1-969">IoTCentral</span></span>
* <span data-ttu-id="cfdd1-970">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-970">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-971">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-971">Role</span></span>
* <span data-ttu-id="cfdd1-972">[重大な変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-972">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-973">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-973">SQL</span></span>
* <span data-ttu-id="cfdd1-974">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-974">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-975">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-975">VM</span></span>
* <span data-ttu-id="cfdd1-976">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-976">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="cfdd1-977">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-977">December 18, 2018</span></span>

<span data-ttu-id="cfdd1-978">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="cfdd1-978">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="cfdd1-979">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-979">ACR</span></span>
* <span data-ttu-id="cfdd1-980">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-980">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="cfdd1-981">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-981">Condensed the table layout for task list</span></span>
* <span data-ttu-id="cfdd1-982">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-982">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-983">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-983">ACS</span></span>
* <span data-ttu-id="cfdd1-984">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-984">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="cfdd1-985">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-985">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="cfdd1-986">[非推奨] `az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-986">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="cfdd1-987">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="cfdd1-987">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="cfdd1-988">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-988">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="cfdd1-989">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-989">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-990">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-990">Appservice</span></span>
* <span data-ttu-id="cfdd1-991">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-991">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="cfdd1-992">Botservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-992">Botservice</span></span>
* <span data-ttu-id="cfdd1-993">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-993">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="cfdd1-994">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-994">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="cfdd1-995">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-995">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="cfdd1-996">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-996">Reduced Kudu network calls</span></span>
* <span data-ttu-id="cfdd1-997">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-997">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="cfdd1-998">消費</span><span class="sxs-lookup"><span data-stu-id="cfdd1-998">Consumption</span></span>
* <span data-ttu-id="cfdd1-999">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-999">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="cfdd1-1000">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1000">CosmosDB</span></span>
* <span data-ttu-id="cfdd1-1001">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1001">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="cfdd1-1002">マップ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1002">Maps</span></span>
* <span data-ttu-id="cfdd1-1003">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1003">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1004">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1004">Network</span></span>
* <span data-ttu-id="cfdd1-1005">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1005">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="cfdd1-1006">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1006">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-1007">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1007">Resource</span></span>
* <span data-ttu-id="cfdd1-1008">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1008">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="cfdd1-1009">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1009">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1010">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1010">Storage</span></span>
*  <span data-ttu-id="cfdd1-1011">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1011">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1012">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1012">VM</span></span>
* <span data-ttu-id="cfdd1-1013">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1013">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="cfdd1-1014">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1014">December 4, 2018</span></span>

<span data-ttu-id="cfdd1-1015">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1015">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="cfdd1-1016">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1016">Core</span></span>
* <span data-ttu-id="cfdd1-1017">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1017">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="cfdd1-1018">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1018">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1019">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1019">Appservice</span></span>
* <span data-ttu-id="cfdd1-1020">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1020">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="cfdd1-1021">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1021">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1022">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1022">Network</span></span>
* <span data-ttu-id="cfdd1-1023">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1023">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-1024">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1024">Role</span></span>
* <span data-ttu-id="cfdd1-1025">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1025">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="cfdd1-1026">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1026">VM</span></span>
* <span data-ttu-id="cfdd1-1027">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1027">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="cfdd1-1028">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1028">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="cfdd1-1029">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1029">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="cfdd1-1030">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1030">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="cfdd1-1031">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1031">November 20, 2018</span></span>

<span data-ttu-id="cfdd1-1032">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1032">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="cfdd1-1033">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1033">Core</span></span>
* <span data-ttu-id="cfdd1-1034">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1034">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1035">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1035">ACR</span></span>
* <span data-ttu-id="cfdd1-1036">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1036">Added context token to task step</span></span>
* <span data-ttu-id="cfdd1-1037">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1037">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="cfdd1-1038">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1038">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1039">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1039">Appservice</span></span>
* <span data-ttu-id="cfdd1-1040">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1040">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="cfdd1-1041">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1041">Updated the default `node_version`.</span></span> <span data-ttu-id="cfdd1-1042">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1042">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="cfdd1-1043">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1043">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="cfdd1-1044">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1044">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="cfdd1-1045">IotCentral</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1045">IotCentral</span></span>
* <span data-ttu-id="cfdd1-1046">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1046">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="cfdd1-1047">KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1047">KeyVault</span></span>
* <span data-ttu-id="cfdd1-1048">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1048">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1049">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1049">Network</span></span>
* <span data-ttu-id="cfdd1-1050">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1050">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="cfdd1-1051">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1051">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="cfdd1-1052">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1052">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="cfdd1-1053">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1053">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="cfdd1-1054">Rdbms</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1054">Rdbms</span></span>
* <span data-ttu-id="cfdd1-1055">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1055">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="cfdd1-1056">Rbac</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1056">Rbac</span></span>
* <span data-ttu-id="cfdd1-1057">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1057">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="cfdd1-1058">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1058">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="cfdd1-1059">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1059">Storage</span></span>
* <span data-ttu-id="cfdd1-1060">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1060">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="cfdd1-1061">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1061">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="cfdd1-1062">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1062">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="cfdd1-1063">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1063">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1064">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1064">VM</span></span>
* <span data-ttu-id="cfdd1-1065">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1065">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="cfdd1-1066">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1066">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="cfdd1-1067">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1067">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="cfdd1-1068">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1068">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="cfdd1-1069">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1069">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="cfdd1-1070">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1070">Added `snapshot wait` command</span></span>
* <span data-ttu-id="cfdd1-1071">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1071">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="cfdd1-1072">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1072">November 6, 2018</span></span>

<span data-ttu-id="cfdd1-1073">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1073">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-1074">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1074">Core</span></span>
* <span data-ttu-id="cfdd1-1075">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1075">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1076">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1076">ACR</span></span>
* <span data-ttu-id="cfdd1-1077">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1077">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="cfdd1-1078">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1078">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1079">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1079">ACS</span></span>
* <span data-ttu-id="cfdd1-1080">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1080">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="cfdd1-1081">Advisor</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1081">Advisor</span></span>
* <span data-ttu-id="cfdd1-1082">GA リリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1082">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="cfdd1-1083">AMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1083">AMS</span></span>
* <span data-ttu-id="cfdd1-1084">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1084">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="cfdd1-1085">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1085">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="cfdd1-1086">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1086">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="cfdd1-1087">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1087">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="cfdd1-1088">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1088">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="cfdd1-1089">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1089">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="cfdd1-1090">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1090">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="cfdd1-1091">[重大な変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1091">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="cfdd1-1092">[重大な変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1092">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="cfdd1-1093">[重大な変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1093">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="cfdd1-1094">[重大な変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1094">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="cfdd1-1095">[重大な変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1095">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="cfdd1-1096">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1096">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="cfdd1-1097">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1097">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="cfdd1-1098">[重大な変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1098">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="cfdd1-1099">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1099">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="cfdd1-1100">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1100">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1101">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1101">AppService</span></span>
* <span data-ttu-id="cfdd1-1102">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1102">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="cfdd1-1103">構成</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1103">Configure</span></span>
* <span data-ttu-id="cfdd1-1104">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1104">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-1105">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1105">Container</span></span>
* <span data-ttu-id="cfdd1-1106">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1106">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="cfdd1-1107">EventHub</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1107">EventHub</span></span>
* <span data-ttu-id="cfdd1-1108">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1108">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="cfdd1-1109">Interactive</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1109">Interactive</span></span>
* <span data-ttu-id="cfdd1-1110">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1110">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-1111">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1111">Monitor</span></span>
* <span data-ttu-id="cfdd1-1112">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1112">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1113">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1113">Network</span></span>
* <span data-ttu-id="cfdd1-1114">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1114">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="cfdd1-1115">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1115">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="cfdd1-1116">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1116">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="cfdd1-1117">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1117">Profile</span></span>
* <span data-ttu-id="cfdd1-1118">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1118">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="cfdd1-1119">RDBMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1119">RDBMS</span></span>
* <span data-ttu-id="cfdd1-1120">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1120">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-1121">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1121">Resource</span></span>
* <span data-ttu-id="cfdd1-1122">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1122">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-1123">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1123">Role</span></span>
* <span data-ttu-id="cfdd1-1124">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1124">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="cfdd1-1125">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1125">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="cfdd1-1126">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1126">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1127">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1127">Storage</span></span>
* <span data-ttu-id="cfdd1-1128">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1128">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1129">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1129">VM</span></span>
* <span data-ttu-id="cfdd1-1130">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1130">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="cfdd1-1131">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1131">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="cfdd1-1132">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1132">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="cfdd1-1133">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1133">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="cfdd1-1134">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1134">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="cfdd1-1135">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1135">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="cfdd1-1136">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1136">October 23, 2018</span></span>

<span data-ttu-id="cfdd1-1137">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1137">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-1138">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1138">Core</span></span>
* <span data-ttu-id="cfdd1-1139">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1139">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="cfdd1-1140">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1140">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1141">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1141">ACR</span></span>
* <span data-ttu-id="cfdd1-1142">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1142">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="cfdd1-1143">CDN</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1143">CDN</span></span>
* <span data-ttu-id="cfdd1-1144">[重大な変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1144">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="cfdd1-1145">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1145">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-1146">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1146">Container</span></span>
* <span data-ttu-id="cfdd1-1147">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1147">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="cfdd1-1148">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1148">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="cfdd1-1149">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1149">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="cfdd1-1150">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1150">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="cfdd1-1151">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1151">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="cfdd1-1152">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1152">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="cfdd1-1153">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1153">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="cfdd1-1154">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1154">CosmosDB</span></span>
* <span data-ttu-id="cfdd1-1155">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1155">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="cfdd1-1156">Interactive</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1156">Interactive</span></span>
* <span data-ttu-id="cfdd1-1157">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1157">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="cfdd1-1158">IoT Central</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1158">IoT Central</span></span>
* <span data-ttu-id="cfdd1-1159">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1159">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="cfdd1-1160">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1160">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-1161">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1161">Monitor</span></span>
* <span data-ttu-id="cfdd1-1162">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1162">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="cfdd1-1163">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1163">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="cfdd1-1164">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1164">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="cfdd1-1165">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1165">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="cfdd1-1166">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1166">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="cfdd1-1167">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1167">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="cfdd1-1168">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1168">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="cfdd1-1169">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1169">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="cfdd1-1170">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1170">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="cfdd1-1171">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1171">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1172">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1172">Network</span></span>
* <span data-ttu-id="cfdd1-1173">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1173">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="cfdd1-1174">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1174">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="cfdd1-1175">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1175">ServiceBus</span></span>
* <span data-ttu-id="cfdd1-1176">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1176">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-1177">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1177">SQL</span></span>
* <span data-ttu-id="cfdd1-1178">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1178">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1179">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1179">Storage</span></span>
* <span data-ttu-id="cfdd1-1180">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1180">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="cfdd1-1181">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1181">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1182">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1182">VM</span></span>
* <span data-ttu-id="cfdd1-1183">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1183">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="cfdd1-1184">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1184">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="cfdd1-1185">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1185">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="cfdd1-1186">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1186">October 16, 2018</span></span>

<span data-ttu-id="cfdd1-1187">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1187">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1188">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1188">VM</span></span>
* <span data-ttu-id="cfdd1-1189">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1189">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="cfdd1-1190">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1190">October 9, 2018</span></span>

<span data-ttu-id="cfdd1-1191">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1191">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-1192">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1192">Core</span></span>
* <span data-ttu-id="cfdd1-1193">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1193">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1194">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1194">ACR</span></span>
* <span data-ttu-id="cfdd1-1195">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1195">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1196">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1196">ACS</span></span>
* <span data-ttu-id="cfdd1-1197">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1197">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="cfdd1-1198">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1198">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="cfdd1-1199">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1199">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="cfdd1-1200">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1200">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-1201">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1201">Container</span></span>
* <span data-ttu-id="cfdd1-1202">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1202">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="cfdd1-1203">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1203">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="cfdd1-1204">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1204">Event Hub</span></span>
* <span data-ttu-id="cfdd1-1205">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1205">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="cfdd1-1206">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1206">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="cfdd1-1207">Extensions</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1207">Extensions</span></span>
* <span data-ttu-id="cfdd1-1208">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1208">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="cfdd1-1209">HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1209">HDInsight</span></span>
* <span data-ttu-id="cfdd1-1210">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1210">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="cfdd1-1211">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1211">IoT</span></span>
* <span data-ttu-id="cfdd1-1212">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1212">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="cfdd1-1213">KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1213">KeyVault</span></span>
* <span data-ttu-id="cfdd1-1214">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1214">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1215">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1215">Network</span></span>
* <span data-ttu-id="cfdd1-1216">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1216">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="cfdd1-1217">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1217">See #6052</span></span>
* <span data-ttu-id="cfdd1-1218">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1218">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="cfdd1-1219">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1219">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="cfdd1-1220">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1220">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="cfdd1-1221">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1221">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="cfdd1-1222">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1222">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="cfdd1-1223">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1223">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-1224">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1224">Role</span></span>
* <span data-ttu-id="cfdd1-1225">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1225">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="cfdd1-1226">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1226">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="cfdd1-1227">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1227">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="cfdd1-1228">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1228">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="cfdd1-1229">Service Bus</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1229">Service Bus</span></span>
* <span data-ttu-id="cfdd1-1230">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1230">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1231">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1231">VM</span></span>
* <span data-ttu-id="cfdd1-1232">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1232">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="cfdd1-1233">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1233">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="cfdd1-1234">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1234">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="cfdd1-1235">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1235">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="cfdd1-1236">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1236">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="cfdd1-1237">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1237">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="cfdd1-1238">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1238">September 21, 2018</span></span>

<span data-ttu-id="cfdd1-1239">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1239">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1240">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1240">ACR</span></span>
* <span data-ttu-id="cfdd1-1241">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1241">Added ACR Task commands</span></span>
* <span data-ttu-id="cfdd1-1242">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1242">Added quick run command</span></span>
* <span data-ttu-id="cfdd1-1243">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1243">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="cfdd1-1244">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1244">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="cfdd1-1245">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1245">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="cfdd1-1246">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1246">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1247">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1247">ACS</span></span>
* <span data-ttu-id="cfdd1-1248">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1248">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="cfdd1-1249">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1249">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1250">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1250">AppService</span></span>

* <span data-ttu-id="cfdd1-1251">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1251">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="cfdd1-1252">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1252">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="cfdd1-1253">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1253">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="cfdd1-1254">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1254">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-1255">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1255">Batch</span></span>
* <span data-ttu-id="cfdd1-1256">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1256">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="cfdd1-1257">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1257">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="cfdd1-1258">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1258">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="cfdd1-1259">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1259">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="cfdd1-1260">Batch AI</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1260">Batch AI</span></span> 
* <span data-ttu-id="cfdd1-1261">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1261">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="cfdd1-1262">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1262">Cognitive Services</span></span>
* <span data-ttu-id="cfdd1-1263">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1263">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="cfdd1-1264">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1264">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="cfdd1-1265">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1265">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="cfdd1-1266">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1266">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="cfdd1-1267">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1267">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="cfdd1-1268">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1268">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-1269">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1269">Container</span></span>
* <span data-ttu-id="cfdd1-1270">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1270">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="cfdd1-1271">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1271">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="cfdd1-1272">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1272">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="cfdd1-1273">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1273">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="cfdd1-1274">DataLake</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1274">Datalake</span></span>
* <span data-ttu-id="cfdd1-1275">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1275">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="cfdd1-1276">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1276">Interactive Shell</span></span>
* <span data-ttu-id="cfdd1-1277">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1277">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="cfdd1-1278">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1278">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="cfdd1-1279">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1279">IoT</span></span>
* <span data-ttu-id="cfdd1-1280">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1280">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="cfdd1-1281">Key Vault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1281">Key Vault</span></span>
* <span data-ttu-id="cfdd1-1282">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1282">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1283">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1283">Network</span></span>
* <span data-ttu-id="cfdd1-1284">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1284">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="cfdd1-1285">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1285">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="cfdd1-1286">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1286">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="cfdd1-1287">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1287">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="cfdd1-1288">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1288">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="cfdd1-1289">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1289">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="cfdd1-1290">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1290">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="cfdd1-1291">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1291">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="cfdd1-1292">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1292">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="cfdd1-1293">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1293">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="cfdd1-1294">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1294">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="cfdd1-1295">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1295">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="cfdd1-1296">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1296">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="cfdd1-1297">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1297">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="cfdd1-1298">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1298">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="cfdd1-1299">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1299">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="cfdd1-1300">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1300">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="cfdd1-1301">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1301">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="cfdd1-1302">RDBMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1302">RDBMS</span></span>
* <span data-ttu-id="cfdd1-1303">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1303">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="cfdd1-1304">予約</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1304">Reservation</span></span>
* <span data-ttu-id="cfdd1-1305">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1305">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="cfdd1-1306">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1306">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="cfdd1-1307">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1307">Manage App</span></span>
* <span data-ttu-id="cfdd1-1308">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1308">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="cfdd1-1309">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1309">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-1310">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1310">Role</span></span>
* <span data-ttu-id="cfdd1-1311">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1311">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="cfdd1-1312">SignalR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1312">SignalR</span></span>
* <span data-ttu-id="cfdd1-1313">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1313">First release</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1314">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1314">Storage</span></span>
* <span data-ttu-id="cfdd1-1315">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1315">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="cfdd1-1316">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1316">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1317">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1317">VM</span></span>
* <span data-ttu-id="cfdd1-1318">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1318">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="cfdd1-1319">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1319">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="cfdd1-1320">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1320">August 28, 2018</span></span>

<span data-ttu-id="cfdd1-1321">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1321">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-1322">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1322">Core</span></span>

* <span data-ttu-id="cfdd1-1323">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1323">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="cfdd1-1324">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1324">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1325">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1325">ACR</span></span>

* <span data-ttu-id="cfdd1-1326">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1326">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="cfdd1-1327">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1327">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1328">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1328">ACS</span></span>

* <span data-ttu-id="cfdd1-1329">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1329">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="cfdd1-1330">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1330">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1331">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1331">AppService</span></span>

* <span data-ttu-id="cfdd1-1332">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1332">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="cfdd1-1333">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1333">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="cfdd1-1334">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1334">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="cfdd1-1335">バックアップ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1335">Backup</span></span>

* <span data-ttu-id="cfdd1-1336">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1336">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="cfdd1-1337">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1337">Bot Service</span></span>

* <span data-ttu-id="cfdd1-1338">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1338">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="cfdd1-1339">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1339">Cognitive Services</span></span>

* <span data-ttu-id="cfdd1-1340">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1340">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="cfdd1-1341">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1341">IoT</span></span>

* <span data-ttu-id="cfdd1-1342">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1342">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-1343">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1343">Monitor</span></span>

* <span data-ttu-id="cfdd1-1344">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1344">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="cfdd1-1345">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1345">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1346">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1346">Network</span></span>

* <span data-ttu-id="cfdd1-1347">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1347">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-1348">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1348">Resource</span></span>

* <span data-ttu-id="cfdd1-1349">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1349">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1350">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1350">Storage</span></span>

* <span data-ttu-id="cfdd1-1351">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1351">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1352">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1352">VM</span></span>

* <span data-ttu-id="cfdd1-1353">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1353">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="cfdd1-1354">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1354">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="cfdd1-1355">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1355">Auguest 14, 2018</span></span>

<span data-ttu-id="cfdd1-1356">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1356">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-1357">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1357">Core</span></span>

* <span data-ttu-id="cfdd1-1358">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1358">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="cfdd1-1359">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1359">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="cfdd1-1360">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1360">Telemetry</span></span>

* <span data-ttu-id="cfdd1-1361">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1361">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1362">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1362">ACR</span></span>

* <span data-ttu-id="cfdd1-1363">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1363">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="cfdd1-1364">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1364">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1365">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1365">ACS</span></span>

* <span data-ttu-id="cfdd1-1366">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1366">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="cfdd1-1367">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1367">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="cfdd1-1368">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1368">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="cfdd1-1369">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1369">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="cfdd1-1370">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1370">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="cfdd1-1371">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1371">AppService</span></span>

* <span data-ttu-id="cfdd1-1372">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1372">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="cfdd1-1373">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1373">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="cfdd1-1374">BatchAI</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1374">BatchAI</span></span>

* <span data-ttu-id="cfdd1-1375">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1375">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="cfdd1-1376">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1376">Container</span></span>

* <span data-ttu-id="cfdd1-1377">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1377">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="cfdd1-1378">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1378">IoT</span></span>

* <span data-ttu-id="cfdd1-1379">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1379">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="cfdd1-1380">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1380">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="cfdd1-1381">Iot Central</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1381">Iot Central</span></span>

* <span data-ttu-id="cfdd1-1382">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1382">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="cfdd1-1383">KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1383">KeyVault</span></span>


* <span data-ttu-id="cfdd1-1384">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1384">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="cfdd1-1385">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1385">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="cfdd1-1386">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1386">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="cfdd1-1387">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1387">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="cfdd1-1388">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1388">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="cfdd1-1389">リレー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1389">Relay</span></span>

* <span data-ttu-id="cfdd1-1390">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1390">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-1391">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1391">Sql</span></span>

* <span data-ttu-id="cfdd1-1392">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1392">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1393">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1393">Storage</span></span>

* <span data-ttu-id="cfdd1-1394">[重大な変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1394">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="cfdd1-1395">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1395">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="cfdd1-1396">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1396">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="cfdd1-1397">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1397">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="cfdd1-1398">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1398">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1399">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1399">VM</span></span>

* <span data-ttu-id="cfdd1-1400">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1400">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="cfdd1-1401">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1401">July 31, 2018</span></span>

<span data-ttu-id="cfdd1-1402">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1402">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1403">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1403">ACR</span></span>

* <span data-ttu-id="cfdd1-1404">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1404">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="cfdd1-1405">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1405">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1406">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1406">ACS</span></span>

* <span data-ttu-id="cfdd1-1407">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1407">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-1408">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1408">Batch</span></span>

* <span data-ttu-id="cfdd1-1409">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1409">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-1410">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1410">Container</span></span>

* <span data-ttu-id="cfdd1-1411">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1411">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1412">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1412">Network</span></span>

* <span data-ttu-id="cfdd1-1413">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1413">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="cfdd1-1414">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1414">Resource</span></span>

* <span data-ttu-id="cfdd1-1415">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1415">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="cfdd1-1416">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1416">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-1417">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1417">Role</span></span>

* <span data-ttu-id="cfdd1-1418">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1418">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="cfdd1-1419">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1419">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="cfdd1-1420">Search</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1420">Search</span></span>

* <span data-ttu-id="cfdd1-1421">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1421">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="cfdd1-1422">Service Bus</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1422">Service Bus</span></span>

* <span data-ttu-id="cfdd1-1423">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1423">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="cfdd1-1424">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1424">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="cfdd1-1425">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1425">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="cfdd1-1426">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1426">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1427">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1427">Storage</span></span>

* <span data-ttu-id="cfdd1-1428">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1428">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="cfdd1-1429">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1429">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1430">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1430">VM</span></span>

* <span data-ttu-id="cfdd1-1431">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1431">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="cfdd1-1432">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1432">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="cfdd1-1433">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1433">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="cfdd1-1434">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1434">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="cfdd1-1435">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1435">July 18, 2018</span></span>

<span data-ttu-id="cfdd1-1436">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1436">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-1437">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1437">Core</span></span>

* <span data-ttu-id="cfdd1-1438">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1438">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="cfdd1-1439">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1439">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="cfdd1-1440">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1440">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1441">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1441">ACR</span></span>

* <span data-ttu-id="cfdd1-1442">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1442">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="cfdd1-1443">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1443">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="cfdd1-1444">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1444">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="cfdd1-1445">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1445">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1446">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1446">ACS</span></span>

* <span data-ttu-id="cfdd1-1447">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1447">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1448">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1448">AppService</span></span>

* <span data-ttu-id="cfdd1-1449">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1449">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-1450">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1450">Batch</span></span>

* <span data-ttu-id="cfdd1-1451">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1451">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="cfdd1-1452">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1452">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="cfdd1-1453">Batch AI</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1453">Batch AI</span></span>

* <span data-ttu-id="cfdd1-1454">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1454">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-1455">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1455">Container</span></span>

* <span data-ttu-id="cfdd1-1456">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1456">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="cfdd1-1457">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1457">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1458">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1458">Network</span></span>

* <span data-ttu-id="cfdd1-1459">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1459">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="cfdd1-1460">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1460">Added `network nic wait`</span></span>
* <span data-ttu-id="cfdd1-1461">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1461">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="cfdd1-1462">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1462">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="cfdd1-1463">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1463">Resource</span></span>

* <span data-ttu-id="cfdd1-1464">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1464">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="cfdd1-1465">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1465">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="cfdd1-1466">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1466">Added `deployment wait` command</span></span>
* <span data-ttu-id="cfdd1-1467">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1467">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-1468">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1468">SQL</span></span>

* <span data-ttu-id="cfdd1-1469">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1469">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="cfdd1-1470">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1470">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="cfdd1-1471">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1471">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1472">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1472">Storage</span></span>

* <span data-ttu-id="cfdd1-1473">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1473">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1474">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1474">VM</span></span>

* <span data-ttu-id="cfdd1-1475">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1475">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="cfdd1-1476">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1476">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="cfdd1-1477">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1477">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="cfdd1-1478">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1478">July 3, 2018</span></span>

<span data-ttu-id="cfdd1-1479">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1479">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="cfdd1-1480">AKS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1480">AKS</span></span>

* <span data-ttu-id="cfdd1-1481">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1481">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="cfdd1-1482">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1482">July 3, 2018</span></span>

<span data-ttu-id="cfdd1-1483">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1483">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-1484">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1484">Core</span></span>

* <span data-ttu-id="cfdd1-1485">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1485">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1486">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1486">ACR</span></span>

* <span data-ttu-id="cfdd1-1487">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1487">Added polling build status</span></span>
* <span data-ttu-id="cfdd1-1488">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1488">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="cfdd1-1489">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1489">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1490">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1490">ACS</span></span>

* <span data-ttu-id="cfdd1-1491">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1491">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="cfdd1-1492">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1492">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="cfdd1-1493">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1493">Updated options for `aks browse` command.</span></span> <span data-ttu-id="cfdd1-1494">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1494">Added `--listen-port` support</span></span>
* <span data-ttu-id="cfdd1-1495">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1495">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="cfdd1-1496">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1496">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="cfdd1-1497">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1497">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1498">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1498">AppService</span></span>

* <span data-ttu-id="cfdd1-1499">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1499">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="cfdd1-1500">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1500">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="cfdd1-1501">バックアップ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1501">Backup</span></span>

* <span data-ttu-id="cfdd1-1502">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1502">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="cfdd1-1503">BatchAI</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1503">BatchAI</span></span>

* <span data-ttu-id="cfdd1-1504">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1504">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="cfdd1-1505">クラウド</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1505">Cloud</span></span>

* <span data-ttu-id="cfdd1-1506">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1506">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-1507">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1507">Container</span></span>

* <span data-ttu-id="cfdd1-1508">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1508">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="cfdd1-1509">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1509">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="cfdd1-1510">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1510">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="cfdd1-1511">拡張機能</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1511">Extension</span></span>

* <span data-ttu-id="cfdd1-1512">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1512">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1513">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1513">Network</span></span>

* <span data-ttu-id="cfdd1-1514">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1514">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="cfdd1-1515">Rdbms</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1515">Rdbms</span></span>

* <span data-ttu-id="cfdd1-1516">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1516">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-1517">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1517">Resource</span></span>

* <span data-ttu-id="cfdd1-1518">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1518">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1519">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1519">VM</span></span>

* <span data-ttu-id="cfdd1-1520">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1520">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="cfdd1-1521">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1521">June 25, 2018</span></span>

<span data-ttu-id="cfdd1-1522">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1522">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="cfdd1-1523">CLI</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1523">CLI</span></span>

* <span data-ttu-id="cfdd1-1524">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1524">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="cfdd1-1525">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1525">June 19, 2018</span></span>

<span data-ttu-id="cfdd1-1526">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1526">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-1527">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1527">Core</span></span>

* <span data-ttu-id="cfdd1-1528">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1528">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1529">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1529">ACR</span></span>

* <span data-ttu-id="cfdd1-1530">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1530">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="cfdd1-1531">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1531">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1532">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1532">ACS</span></span>

* <span data-ttu-id="cfdd1-1533">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1533">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="cfdd1-1534">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1534">Added `--update` support</span></span>
* <span data-ttu-id="cfdd1-1535">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1535">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="cfdd1-1536">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1536">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="cfdd1-1537">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1537">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="cfdd1-1538">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1538">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="cfdd1-1539">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1539">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="cfdd1-1540">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1540">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1541">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1541">AppService</span></span>

* <span data-ttu-id="cfdd1-1542">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1542">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="cfdd1-1543">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1543">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-1544">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1544">Batch</span></span>

* <span data-ttu-id="cfdd1-1545">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1545">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="cfdd1-1546">Batch AI</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1546">Batch AI</span></span>

* <span data-ttu-id="cfdd1-1547">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1547">Added support for workspaces.</span></span> <span data-ttu-id="cfdd1-1548">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1548">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="cfdd1-1549">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1549">Added support for experiments.</span></span> <span data-ttu-id="cfdd1-1550">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1550">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="cfdd1-1551">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1551">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="cfdd1-1552">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1552">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="cfdd1-1553">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1553">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="cfdd1-1554">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1554">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="cfdd1-1555">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1555">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="cfdd1-1556">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1556">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="cfdd1-1557">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1557">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="cfdd1-1558">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1558">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="cfdd1-1559">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1559">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="cfdd1-1560">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1560">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="cfdd1-1561">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1561">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="cfdd1-1562">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1562">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="cfdd1-1563">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1563">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="cfdd1-1564">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1564">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="cfdd1-1565">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1565">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="cfdd1-1566">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1566">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="cfdd1-1567">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1567">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="cfdd1-1568">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1568">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="cfdd1-1569">マップ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1569">Maps</span></span>

* <span data-ttu-id="cfdd1-1570">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1570">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1571">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1571">Network</span></span>

* <span data-ttu-id="cfdd1-1572">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1572">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="cfdd1-1573">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1573">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="cfdd1-1574">#6502</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1574">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="cfdd1-1575">Reservations</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1575">Reservations</span></span>

* <span data-ttu-id="cfdd1-1576">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1576">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="cfdd1-1577">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1577">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="cfdd1-1578">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1578">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="cfdd1-1579">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1579">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="cfdd1-1580">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1580">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="cfdd1-1581">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1581">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-1582">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1582">Role</span></span>

* <span data-ttu-id="cfdd1-1583">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1583">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-1584">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1584">SQL</span></span>

* <span data-ttu-id="cfdd1-1585">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1585">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1586">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1586">Storage</span></span>

* <span data-ttu-id="cfdd1-1587">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1587">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1588">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1588">VM</span></span>

* <span data-ttu-id="cfdd1-1589">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1589">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="cfdd1-1590">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1590">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="cfdd1-1591">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1591">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="cfdd1-1592">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1592">June 13, 2018</span></span>

<span data-ttu-id="cfdd1-1593">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1593">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-1594">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1594">Core</span></span>

* <span data-ttu-id="cfdd1-1595">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1595">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="cfdd1-1596">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1596">June 13, 2018</span></span>

<span data-ttu-id="cfdd1-1597">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1597">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="cfdd1-1598">AKS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1598">AKS</span></span>

* <span data-ttu-id="cfdd1-1599">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1599">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="cfdd1-1600">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1600">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="cfdd1-1601">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1601">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="cfdd1-1602">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1602">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="cfdd1-1603">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1603">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1604">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1604">AppService</span></span>

* <span data-ttu-id="cfdd1-1605">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1605">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="cfdd1-1606">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1606">June 5, 2018</span></span>

<span data-ttu-id="cfdd1-1607">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1607">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="cfdd1-1608">Interactive</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1608">Interactive</span></span>

* <span data-ttu-id="cfdd1-1609">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1609">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="cfdd1-1610">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1610">June 5, 2018</span></span>

<span data-ttu-id="cfdd1-1611">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1611">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-1612">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1612">Core</span></span>

* <span data-ttu-id="cfdd1-1613">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1613">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="cfdd1-1614">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1614">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1615">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1615">ACR</span></span>

* <span data-ttu-id="cfdd1-1616">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1616">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="cfdd1-1617">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1617">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="cfdd1-1618">AKS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1618">AKS</span></span>

* <span data-ttu-id="cfdd1-1619">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1619">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-1620">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1620">Batch</span></span>

* <span data-ttu-id="cfdd1-1621">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1621">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="cfdd1-1622">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1622">IOT</span></span>

* <span data-ttu-id="cfdd1-1623">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1623">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1624">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1624">Network</span></span>

* <span data-ttu-id="cfdd1-1625">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1625">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="cfdd1-1626">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1626">Policy Insights</span></span>

* <span data-ttu-id="cfdd1-1627">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1627">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="cfdd1-1628">ARM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1628">ARM</span></span>

* <span data-ttu-id="cfdd1-1629">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1629">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-1630">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1630">SQL</span></span>

* <span data-ttu-id="cfdd1-1631">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1631">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="cfdd1-1632">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1632">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="cfdd1-1633">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1633">Storage</span></span>

* <span data-ttu-id="cfdd1-1634">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1634">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1635">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1635">VM</span></span>

* <span data-ttu-id="cfdd1-1636">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1636">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="cfdd1-1637">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1637">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="cfdd1-1638">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1638">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="cfdd1-1639">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1639">May 22, 2018</span></span>

<span data-ttu-id="cfdd1-1640">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1640">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-1641">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1641">Core</span></span>

* <span data-ttu-id="cfdd1-1642">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1642">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1643">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1643">ACS</span></span>

* <span data-ttu-id="cfdd1-1644">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1644">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="cfdd1-1645">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1645">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1646">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1646">AppService</span></span>

* <span data-ttu-id="cfdd1-1647">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1647">Improved generic update commands</span></span>
* <span data-ttu-id="cfdd1-1648">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1648">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-1649">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1649">Container</span></span>

* <span data-ttu-id="cfdd1-1650">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1650">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="cfdd1-1651">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1651">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="cfdd1-1652">拡張機能</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1652">Extension</span></span>

* <span data-ttu-id="cfdd1-1653">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1653">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="cfdd1-1654">Interactive</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1654">Interactive</span></span>

* <span data-ttu-id="cfdd1-1655">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1655">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="cfdd1-1656">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1656">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="cfdd1-1657">KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1657">KeyVault</span></span>

* <span data-ttu-id="cfdd1-1658">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1658">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1659">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1659">Network</span></span>

* <span data-ttu-id="cfdd1-1660">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1660">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="cfdd1-1661">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1661">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-1662">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1662">SQL</span></span>

* <span data-ttu-id="cfdd1-1663">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1663">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="cfdd1-1664">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1664">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="cfdd1-1665">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1665">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="cfdd1-1666">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1666">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="cfdd1-1667">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1667">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="cfdd1-1668">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1668">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="cfdd1-1669">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1669">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="cfdd1-1670">`edition`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1670">`edition`.</span></span> <span data-ttu-id="cfdd1-1671">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1671">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="cfdd1-1672">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1672">`elasticPoolName`.</span></span> <span data-ttu-id="cfdd1-1673">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1673">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="cfdd1-1674">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1674">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="cfdd1-1675">`edition`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1675">`edition`.</span></span> <span data-ttu-id="cfdd1-1676">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1676">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="cfdd1-1677">`dtu`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1677">`dtu`.</span></span> <span data-ttu-id="cfdd1-1678">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1678">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="cfdd1-1679">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1679">`databaseDtuMin`.</span></span> <span data-ttu-id="cfdd1-1680">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1680">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="cfdd1-1681">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1681">`databaseDtuMax`.</span></span> <span data-ttu-id="cfdd1-1682">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1682">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="cfdd1-1683">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1683">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="cfdd1-1684">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1684">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1685">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1685">Storage</span></span>

* <span data-ttu-id="cfdd1-1686">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1686">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="cfdd1-1687">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1687">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1688">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1688">VM</span></span>

* <span data-ttu-id="cfdd1-1689">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1689">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="cfdd1-1690">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1690">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="cfdd1-1691">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1691">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="cfdd1-1692">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1692">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="cfdd1-1693">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1693">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="cfdd1-1694">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1694">May 7, 2018</span></span>

<span data-ttu-id="cfdd1-1695">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1695">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-1696">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1696">Core</span></span>

* <span data-ttu-id="cfdd1-1697">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1697">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="cfdd1-1698">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1698">Added limited support for positional arguments</span></span>
* <span data-ttu-id="cfdd1-1699">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1699">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="cfdd1-1700">#5591</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1700">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="cfdd1-1701">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1701">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="cfdd1-1702">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1702">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="cfdd1-1703">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1703">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="cfdd1-1704">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1704">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="cfdd1-1705">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1705">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1706">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1706">ACR</span></span>

* <span data-ttu-id="cfdd1-1707">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1707">Added ACR Build commands</span></span>
* <span data-ttu-id="cfdd1-1708">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1708">Improved resource not found error messages</span></span>
* <span data-ttu-id="cfdd1-1709">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1709">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="cfdd1-1710">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1710">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="cfdd1-1711">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1711">Improved repository commands error messages</span></span>
* <span data-ttu-id="cfdd1-1712">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1712">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1713">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1713">ACS</span></span>

* <span data-ttu-id="cfdd1-1714">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1714">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="cfdd1-1715">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1715">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="cfdd1-1716">AMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1716">AMS</span></span>

* <span data-ttu-id="cfdd1-1717">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1717">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1718">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1718">Appservice</span></span>

* <span data-ttu-id="cfdd1-1719">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1719">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="cfdd1-1720">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1720">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="cfdd1-1721">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1721">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="cfdd1-1722">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1722">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="cfdd1-1723">Batch AI</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1723">Batch AI</span></span>

* <span data-ttu-id="cfdd1-1724">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1724">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="cfdd1-1725">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1725">Cognitive Services</span></span>

* <span data-ttu-id="cfdd1-1726">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1726">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="cfdd1-1727">消費</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1727">Consumption</span></span>

* <span data-ttu-id="cfdd1-1728">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1728">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-1729">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1729">Container</span></span>

* <span data-ttu-id="cfdd1-1730">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1730">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="cfdd1-1731">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1731">Cosmos DB</span></span>

* <span data-ttu-id="cfdd1-1732">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1732">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="cfdd1-1733">DMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1733">DMS</span></span>

* <span data-ttu-id="cfdd1-1734">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1734">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="cfdd1-1735">拡張機能</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1735">Extension</span></span>

* <span data-ttu-id="cfdd1-1736">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1736">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="cfdd1-1737">Interactive</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1737">Interactive</span></span>

* <span data-ttu-id="cfdd1-1738">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1738">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="cfdd1-1739">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1739">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="cfdd1-1740">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1740">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="cfdd1-1741">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1741">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="cfdd1-1742">ラボ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1742">Lab</span></span>

* <span data-ttu-id="cfdd1-1743">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1743">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1744">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1744">Network</span></span>

* <span data-ttu-id="cfdd1-1745">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1745">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="cfdd1-1746">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1746">Profile</span></span>

* <span data-ttu-id="cfdd1-1747">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1747">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="cfdd1-1748">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1748">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="cfdd1-1749">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1749">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="cfdd1-1750">Redis</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1750">Redis</span></span>

* <span data-ttu-id="cfdd1-1751">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1751">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="cfdd1-1752">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1752">Deprecated `redis list-all`.</span></span> <span data-ttu-id="cfdd1-1753">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1753">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="cfdd1-1754">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1754">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="cfdd1-1755">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1755">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-1756">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1756">Role</span></span>

* <span data-ttu-id="cfdd1-1757">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1757">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1758">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1758">Storage</span></span>

* <span data-ttu-id="cfdd1-1759">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1759">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="cfdd1-1760">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1760">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="cfdd1-1761">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1761">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="cfdd1-1762">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1762">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="cfdd1-1763">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1763">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1764">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1764">VM</span></span>

* <span data-ttu-id="cfdd1-1765">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1765">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="cfdd1-1766">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1766">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="cfdd1-1767">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1767">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="cfdd1-1768">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1768">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="cfdd1-1769">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1769">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="cfdd1-1770">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1770">Added write accelerator support</span></span>
* <span data-ttu-id="cfdd1-1771">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1771">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="cfdd1-1772">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1772">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="cfdd1-1773">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1773">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="cfdd1-1774">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1774">April 10, 2018</span></span>

<span data-ttu-id="cfdd1-1775">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1775">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1776">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1776">ACR</span></span>

* <span data-ttu-id="cfdd1-1777">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1777">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1778">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1778">ACS</span></span>

* <span data-ttu-id="cfdd1-1779">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1779">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1780">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1780">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="cfdd1-1782">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1782">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="cfdd1-1783">BatchAI</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1783">BatchAI</span></span>

* <span data-ttu-id="cfdd1-1784">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1784">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="cfdd1-1785">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1785">Job level mounting</span></span>
  - <span data-ttu-id="cfdd1-1786">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1786">Environment variables with secret values</span></span>
  - <span data-ttu-id="cfdd1-1787">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1787">Performance counters settings</span></span>
  - <span data-ttu-id="cfdd1-1788">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1788">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="cfdd1-1789">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1789">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="cfdd1-1790">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1790">Usage and limits reporting</span></span>
  - <span data-ttu-id="cfdd1-1791">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1791">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="cfdd1-1792">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1792">Support for custom images</span></span>
  - <span data-ttu-id="cfdd1-1793">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1793">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="cfdd1-1794">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1794">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="cfdd1-1795">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1795">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="cfdd1-1796">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1796">National clouds are supported</span></span>
* <span data-ttu-id="cfdd1-1797">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1797">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="cfdd1-1798">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1798">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="cfdd1-1799">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1799">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="cfdd1-1800">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1800">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="cfdd1-1801">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1801">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="cfdd1-1802">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1802">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="cfdd1-1803">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1803">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="cfdd1-1804">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1804">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="cfdd1-1805">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1805">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="cfdd1-1806">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1806">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="cfdd1-1807">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1807">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="cfdd1-1808">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1808">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="cfdd1-1809">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1809">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="cfdd1-1810">課金</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1810">Billing</span></span>

* <span data-ttu-id="cfdd1-1811">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1811">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="cfdd1-1812">消費</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1812">Consumption</span></span>

* <span data-ttu-id="cfdd1-1813">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1813">Added `marketplace` commands</span></span>
* <span data-ttu-id="cfdd1-1814">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1814">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="cfdd1-1815">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1815">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="cfdd1-1816">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1816">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="cfdd1-1817">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1817">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="cfdd1-1818">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1818">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-1819">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1819">Container</span></span>

* <span data-ttu-id="cfdd1-1820">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1820">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="cfdd1-1821">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1821">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="cfdd1-1822">拡張機能</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1822">Extension</span></span>

* <span data-ttu-id="cfdd1-1823">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1823">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="cfdd1-1824">Interactive</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1824">Interactive</span></span>

* <span data-ttu-id="cfdd1-1825">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1825">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="cfdd1-1826">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1826">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="cfdd1-1827">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1827">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1828">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1828">Network</span></span>

* <span data-ttu-id="cfdd1-1829">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1829">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="cfdd1-1830">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1830">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="cfdd1-1831">#4910</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1831">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="cfdd1-1832">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1832">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="cfdd1-1833">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1833">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="cfdd1-1834">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1834">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="cfdd1-1835">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1835">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="cfdd1-1836">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1836">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="cfdd1-1837">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1837">Profile</span></span>

* <span data-ttu-id="cfdd1-1838">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1838">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="cfdd1-1839">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1839">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="cfdd1-1840">RDBMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1840">RDBMS</span></span>

* <span data-ttu-id="cfdd1-1841">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1841">Added `georestore` command</span></span>
* <span data-ttu-id="cfdd1-1842">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1842">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-1843">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1843">Resource</span></span>

* <span data-ttu-id="cfdd1-1844">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1844">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="cfdd1-1845">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1845">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-1846">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1846">SQL</span></span>

* <span data-ttu-id="cfdd1-1847">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1847">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1848">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1848">Storage</span></span>

* <span data-ttu-id="cfdd1-1849">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1849">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1850">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1850">VM</span></span>

* <span data-ttu-id="cfdd1-1851">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1851">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="cfdd1-1852">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1852">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="cfdd1-1854">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1854">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="cfdd1-1855">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1855">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="cfdd1-1856">#5718</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1856">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="cfdd1-1857">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1857">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="cfdd1-1858">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1858">March 27, 2018</span></span>

<span data-ttu-id="cfdd1-1859">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1859">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-1860">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1860">Core</span></span>

* <span data-ttu-id="cfdd1-1861">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1861">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1862">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1862">ACS</span></span>

* <span data-ttu-id="cfdd1-1863">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1863">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1864">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1864">Appservice</span></span>

* <span data-ttu-id="cfdd1-1865">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1865">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="cfdd1-1866">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1866">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="cfdd1-1867">バックアップ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1867">Backup</span></span>

* <span data-ttu-id="cfdd1-1868">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1868">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="cfdd1-1869">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1869">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="cfdd1-1870">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1870">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="cfdd1-1871">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1871">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-1872">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1872">Container</span></span>

* <span data-ttu-id="cfdd1-1873">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1873">Added `container exec` command.</span></span> <span data-ttu-id="cfdd1-1874">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1874">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="cfdd1-1875">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1875">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="cfdd1-1876">拡張機能</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1876">Extension</span></span>

* <span data-ttu-id="cfdd1-1877">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1877">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="cfdd1-1878">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1878">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="cfdd1-1879">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1879">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="cfdd1-1880">Interactive</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1880">Interactive</span></span>

* <span data-ttu-id="cfdd1-1881">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1881">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="cfdd1-1882">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1882">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="cfdd1-1883">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1883">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="cfdd1-1884">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1884">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="cfdd1-1885">ラボ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1885">Lab</span></span>

* <span data-ttu-id="cfdd1-1886">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1886">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-1887">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1887">Monitor</span></span>

* <span data-ttu-id="cfdd1-1888">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1888">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="cfdd1-1889">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1889">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="cfdd1-1890">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1890">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1891">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1891">Network</span></span>

* <span data-ttu-id="cfdd1-1892">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1892">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="cfdd1-1893">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1893">Profile</span></span>

* <span data-ttu-id="cfdd1-1894">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1894">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="cfdd1-1895">RDBMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1895">RDBMS</span></span>

* <span data-ttu-id="cfdd1-1896">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1896">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-1897">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1897">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="cfdd1-1899">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1899">Role</span></span>

* <span data-ttu-id="cfdd1-1900">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1900">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="cfdd1-1901">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1901">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="cfdd1-1902">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1902">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="cfdd1-1903">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1903">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="cfdd1-1904">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1904">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1905">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1905">Storage</span></span>

* <span data-ttu-id="cfdd1-1906">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1906">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="cfdd1-1907">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1907">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1908">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1908">VM</span></span>

* <span data-ttu-id="cfdd1-1909">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1909">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="cfdd1-1910">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1910">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="cfdd1-1911">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1911">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="cfdd1-1912">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1912">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="cfdd1-1913">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1913">March 13, 2018</span></span>

<span data-ttu-id="cfdd1-1914">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1914">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-1915">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1915">ACR</span></span>

* <span data-ttu-id="cfdd1-1916">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1916">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="cfdd1-1917">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1917">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="cfdd1-1918">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1918">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1919">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1919">ACS</span></span>

* <span data-ttu-id="cfdd1-1920">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1920">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="cfdd1-1921">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1921">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="cfdd1-1922">Advisor</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1922">Advisor</span></span>

* <span data-ttu-id="cfdd1-1923">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1923">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="cfdd1-1924">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1924">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="cfdd1-1925">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1925">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="cfdd1-1926">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1926">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="cfdd1-1927">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1927">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1928">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1928">Appservice</span></span>

* <span data-ttu-id="cfdd1-1929">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1929">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="cfdd1-1930">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1930">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="cfdd1-1931">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1931">Eventhubs</span></span>

* <span data-ttu-id="cfdd1-1932">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1932">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="cfdd1-1933">拡張機能</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1933">Extension</span></span>

* <span data-ttu-id="cfdd1-1934">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1934">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="cfdd1-1935">Interactive</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1935">Interactive</span></span>

* <span data-ttu-id="cfdd1-1936">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1936">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="cfdd1-1937">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1937">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="cfdd1-1938">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1938">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="cfdd1-1939">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1939">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-1940">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1940">Monitor</span></span>

* <span data-ttu-id="cfdd1-1941">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1941">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="cfdd1-1942">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1942">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="cfdd1-1943">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1943">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="cfdd1-1944">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1944">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1945">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1945">Network</span></span>

* <span data-ttu-id="cfdd1-1946">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1946">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="cfdd1-1947">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1947">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="cfdd1-1948">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1948">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="cfdd1-1949">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1949">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="cfdd1-1950">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1950">Profile</span></span>

* <span data-ttu-id="cfdd1-1951">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1951">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="cfdd1-1952">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1952">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="cfdd1-1953">RDBMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1953">RDBMS</span></span>

* <span data-ttu-id="cfdd1-1954">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1954">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="cfdd1-1955">Service Bus</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1955">Service Bus</span></span>

* <span data-ttu-id="cfdd1-1956">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1956">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1957">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1957">Storage</span></span>

* <span data-ttu-id="cfdd1-1958">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1958">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="cfdd1-1959">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1959">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1960">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1960">VM</span></span>

* <span data-ttu-id="cfdd1-1961">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1961">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="cfdd1-1962">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1962">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="cfdd1-1963">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1963">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="cfdd1-1964">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1964">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="cfdd1-1965">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1965">February 27, 2018</span></span>

<span data-ttu-id="cfdd1-1966">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1966">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-1967">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1967">Core</span></span>

* <span data-ttu-id="cfdd1-1968">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1968">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="cfdd1-1969">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1969">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="cfdd1-1970">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1970">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-1971">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1971">ACS</span></span>

* <span data-ttu-id="cfdd1-1972">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1972">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="cfdd1-1973">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1973">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="cfdd1-1974">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1974">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="cfdd1-1975">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1975">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-1976">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1976">Appservice</span></span>

* <span data-ttu-id="cfdd1-1977">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1977">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="cfdd1-1978">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1978">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="cfdd1-1979">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1979">Cognitive Services</span></span>

* <span data-ttu-id="cfdd1-1980">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1980">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="cfdd1-1981">消費</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1981">Consumption</span></span>

* <span data-ttu-id="cfdd1-1982">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1982">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="cfdd1-1983">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1983">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-1984">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1984">Container</span></span>

* <span data-ttu-id="cfdd1-1985">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1985">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-1986">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1986">Network</span></span>

* <span data-ttu-id="cfdd1-1987">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1987">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-1988">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1988">Resource</span></span>

* <span data-ttu-id="cfdd1-1989">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1989">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-1990">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1990">Role</span></span>

* <span data-ttu-id="cfdd1-1991">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1991">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-1992">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1992">SQL</span></span>

* <span data-ttu-id="cfdd1-1993">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1993">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-1994">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1994">Storage</span></span>

* <span data-ttu-id="cfdd1-1995">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1995">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-1996">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1996">VM</span></span>

* <span data-ttu-id="cfdd1-1997">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1997">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="cfdd1-1998">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1998">February 13, 2018</span></span>

<span data-ttu-id="cfdd1-1999">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="cfdd1-1999">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-2000">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2000">Core</span></span>

* <span data-ttu-id="cfdd1-2001">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2001">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-2002">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2002">ACS</span></span>

* <span data-ttu-id="cfdd1-2003">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2003">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="cfdd1-2004">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2004">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="cfdd1-2005">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2005">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="cfdd1-2006">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2006">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="cfdd1-2007">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2007">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="cfdd1-2008">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2008">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="cfdd1-2009">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2009">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="cfdd1-2010">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2010">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-2011">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2011">Appservice</span></span>

* <span data-ttu-id="cfdd1-2012">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2012">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="cfdd1-2013">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2013">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="cfdd1-2014">CDN</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2014">CDN</span></span>

* <span data-ttu-id="cfdd1-2015">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2015">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-2016">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2016">Container</span></span>

* <span data-ttu-id="cfdd1-2017">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2017">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="cfdd1-2018">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2018">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="cfdd1-2019">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2019">CosmosDB</span></span>

* <span data-ttu-id="cfdd1-2020">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2020">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="cfdd1-2021">拡張機能</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2021">Extension</span></span>

* <span data-ttu-id="cfdd1-2022">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2022">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="cfdd1-2023">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2023">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="cfdd1-2024">フィードバック</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2024">Feedback</span></span>

* <span data-ttu-id="cfdd1-2025">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2025">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="cfdd1-2026">Interactive</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2026">Interactive</span></span>

* <span data-ttu-id="cfdd1-2027">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2027">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="cfdd1-2028">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2028">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="cfdd1-2029">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2029">IoT</span></span>

* <span data-ttu-id="cfdd1-2030">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2030">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="cfdd1-2031">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2031">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="cfdd1-2032">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2032">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="cfdd1-2033">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2033">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-2034">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2034">Monitor</span></span>

* <span data-ttu-id="cfdd1-2035">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2035">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-2036">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2036">Network</span></span>

* <span data-ttu-id="cfdd1-2037">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2037">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="cfdd1-2038">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2038">Profile</span></span>

* <span data-ttu-id="cfdd1-2039">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2039">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-2040">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2040">Resource</span></span>

* <span data-ttu-id="cfdd1-2041">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2041">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-2042">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2042">Role</span></span>

* <span data-ttu-id="cfdd1-2043">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2043">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-2044">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2044">SQL</span></span>

* <span data-ttu-id="cfdd1-2045">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2045">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="cfdd1-2046">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2046">Added `sql db rename`</span></span>
* <span data-ttu-id="cfdd1-2047">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2047">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-2048">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2048">Storage</span></span>

* <span data-ttu-id="cfdd1-2049">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2049">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2050">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2050">VM</span></span>

* <span data-ttu-id="cfdd1-2051">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2051">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="cfdd1-2052">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2052">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="cfdd1-2053">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2053">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="cfdd1-2054">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2054">January 31, 2018</span></span>

<span data-ttu-id="cfdd1-2055">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2055">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-2056">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2056">Core</span></span>

* <span data-ttu-id="cfdd1-2057">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2057">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="cfdd1-2058">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2058">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="cfdd1-2059">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2059">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="cfdd1-2060">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2060">Use `--verbose` to see</span></span>
* <span data-ttu-id="cfdd1-2061">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2061">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-2062">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2062">ACS</span></span>

* <span data-ttu-id="cfdd1-2063">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2063">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="cfdd1-2064">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2064">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-2065">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2065">Appservice</span></span>

* <span data-ttu-id="cfdd1-2066">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2066">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="cfdd1-2067">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2067">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="cfdd1-2068">CDN</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2068">CDN</span></span>

* <span data-ttu-id="cfdd1-2069">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2069">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="cfdd1-2070">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2070">CosmosDB</span></span>

* <span data-ttu-id="cfdd1-2071">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2071">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="cfdd1-2072">Interactive</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2072">Interactive</span></span>

* <span data-ttu-id="cfdd1-2073">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2073">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-2074">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2074">Network</span></span>

* <span data-ttu-id="cfdd1-2075">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2075">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="cfdd1-2076">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2076">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="cfdd1-2077">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2077">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="cfdd1-2078">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2078">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="cfdd1-2079">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2079">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="cfdd1-2080">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2080">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="cfdd1-2081">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2081">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="cfdd1-2082">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2082">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="cfdd1-2083">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2083">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="cfdd1-2084">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2084">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="cfdd1-2085">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2085">Profile</span></span>

* <span data-ttu-id="cfdd1-2086">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2086">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-2087">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2087">Resource</span></span>

* <span data-ttu-id="cfdd1-2088">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2088">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-2089">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2089">Storage</span></span>

* <span data-ttu-id="cfdd1-2090">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2090">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="cfdd1-2091">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2091">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="cfdd1-2092">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2092">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="cfdd1-2093">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2093">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="cfdd1-2094">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2094">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2095">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2095">VM</span></span>

* <span data-ttu-id="cfdd1-2096">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2096">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="cfdd1-2097">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2097">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="cfdd1-2098">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2098">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="cfdd1-2099">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2099">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="cfdd1-2100">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2100">January 17, 2018</span></span>

<span data-ttu-id="cfdd1-2101">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2101">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-2102">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2102">ACR</span></span>

* <span data-ttu-id="cfdd1-2103">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2103">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="cfdd1-2104">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2104">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-2105">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2105">ACS</span></span>

* <span data-ttu-id="cfdd1-2106">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2106">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="cfdd1-2107">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2107">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-2108">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2108">Appservice</span></span>

* <span data-ttu-id="cfdd1-2109">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2109">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="cfdd1-2110">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2110">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="cfdd1-2111">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2111">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="cfdd1-2112">バックアップ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2112">Backup</span></span>

* <span data-ttu-id="cfdd1-2113">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2113">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="cfdd1-2114">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2114">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="cfdd1-2115">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2115">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="cfdd1-2116">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2116">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="cfdd1-2117">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2117">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-2118">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2118">Batch</span></span>

* <span data-ttu-id="cfdd1-2119">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2119">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="cfdd1-2120">クラウド</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2120">Cloud</span></span>

* <span data-ttu-id="cfdd1-2121">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2121">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="cfdd1-2122">消費</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2122">Consumption</span></span>

* <span data-ttu-id="cfdd1-2123">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2123">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="cfdd1-2124">Event Grid</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2124">Event Grid</span></span>

* <span data-ttu-id="cfdd1-2125">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2125">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="cfdd1-2126">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2126">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="cfdd1-2127">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2127">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="cfdd1-2128">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2128">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="cfdd1-2129">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2129">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="cfdd1-2130">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2130">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="cfdd1-2131">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2131">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="cfdd1-2132">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2132">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="cfdd1-2133">Interactive</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2133">Interactive</span></span>

* <span data-ttu-id="cfdd1-2134">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2134">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="cfdd1-2135">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2135">Fixed errors on startup</span></span>
* <span data-ttu-id="cfdd1-2136">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2136">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="cfdd1-2137">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2137">IoT</span></span>

* <span data-ttu-id="cfdd1-2138">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2138">Added support for device provisioning service</span></span>
* <span data-ttu-id="cfdd1-2139">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2139">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="cfdd1-2140">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2140">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-2141">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2141">Monitor</span></span>

* <span data-ttu-id="cfdd1-2142">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2142">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="cfdd1-2143">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2143">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="cfdd1-2144">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2144">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-2145">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2145">Network</span></span>

* <span data-ttu-id="cfdd1-2146">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2146">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="cfdd1-2147">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2147">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="cfdd1-2148">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2148">Profile</span></span>

* <span data-ttu-id="cfdd1-2149">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2149">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-2150">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2150">Role</span></span>

* <span data-ttu-id="cfdd1-2151">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2151">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="cfdd1-2152">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2152">Service Fabric</span></span>

* <span data-ttu-id="cfdd1-2153">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2153">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="cfdd1-2154">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2154">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2155">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2155">VM</span></span>

* <span data-ttu-id="cfdd1-2156">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2156">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="cfdd1-2157">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2157">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="cfdd1-2158">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2158">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="cfdd1-2159">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2159">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="cfdd1-2160">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2160">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="cfdd1-2161">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2161">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="cfdd1-2162">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2162">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="cfdd1-2163">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2163">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="cfdd1-2164">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2164">December 19, 2017</span></span>

<span data-ttu-id="cfdd1-2165">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2165">Version 2.0.23</span></span>

* <span data-ttu-id="cfdd1-2166">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2166">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-2167">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2167">Container</span></span>

* <span data-ttu-id="cfdd1-2168">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2168">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-2169">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2169">Network</span></span>

* <span data-ttu-id="cfdd1-2170">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2170">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="cfdd1-2171">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2171">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-2172">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2172">Storage</span></span>

* <span data-ttu-id="cfdd1-2173">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2173">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2174">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2174">VM</span></span>

* <span data-ttu-id="cfdd1-2175">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2175">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="cfdd1-2176">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2176">December 5, 2017</span></span>

<span data-ttu-id="cfdd1-2177">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2177">Version 2.0.22</span></span>

* <span data-ttu-id="cfdd1-2178">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2178">Removed `az component` commands.</span></span> <span data-ttu-id="cfdd1-2179">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2179">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-2180">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2180">Core</span></span>
* <span data-ttu-id="cfdd1-2181">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2181">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="cfdd1-2182">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2182">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-2183">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2183">ACS</span></span>

* <span data-ttu-id="cfdd1-2184">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2184">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="cfdd1-2185">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2185">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="cfdd1-2186">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2186">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="cfdd1-2187">Advisor</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2187">Advisor</span></span>

* <span data-ttu-id="cfdd1-2188">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2188">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-2189">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2189">Appservice</span></span>

* <span data-ttu-id="cfdd1-2190">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2190">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="cfdd1-2191">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2191">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="cfdd1-2192">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2192">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="cfdd1-2193">消費</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2193">Consumption</span></span>

* <span data-ttu-id="cfdd1-2194">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2194">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-2195">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2195">Container</span></span>

* <span data-ttu-id="cfdd1-2196">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2196">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-2197">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2197">Monitor</span></span>

* <span data-ttu-id="cfdd1-2198">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2198">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-2199">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2199">Resource</span></span>

* <span data-ttu-id="cfdd1-2200">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2200">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-2201">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2201">Role</span></span>

* <span data-ttu-id="cfdd1-2202">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2202">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="cfdd1-2203">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2203">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="cfdd1-2204">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2204">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-2205">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2205">SQL</span></span>

* <span data-ttu-id="cfdd1-2206">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2206">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="cfdd1-2207">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2207">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2208">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2208">VM</span></span>

* <span data-ttu-id="cfdd1-2209">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2209">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="cfdd1-2210">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2210">November 14, 2017</span></span>

<span data-ttu-id="cfdd1-2211">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2211">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-2212">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2212">ACR</span></span>

* <span data-ttu-id="cfdd1-2213">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2213">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="cfdd1-2214">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2214">ACS</span></span>

* <span data-ttu-id="cfdd1-2215">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2215">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="cfdd1-2216">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2216">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="cfdd1-2217">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2217">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="cfdd1-2218">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2218">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="cfdd1-2219">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2219">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-2220">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2220">Appservice</span></span>

* <span data-ttu-id="cfdd1-2221">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2221">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="cfdd1-2222">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2222">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="cfdd1-2223">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2223">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="cfdd1-2224">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2224">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="cfdd1-2225">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2225">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="cfdd1-2226">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2226">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-2227">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2227">Batch</span></span>

* <span data-ttu-id="cfdd1-2228">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2228">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="cfdd1-2229">Batchai</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2229">Batchai</span></span>

* <span data-ttu-id="cfdd1-2230">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2230">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="cfdd1-2231">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2231">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="cfdd1-2232">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2232">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="cfdd1-2233">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2233">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="cfdd1-2234">クラウド</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2234">Cloud</span></span>

* <span data-ttu-id="cfdd1-2235">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2235">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-2236">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2236">Container</span></span>

* <span data-ttu-id="cfdd1-2237">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2237">Added support to open multiple ports</span></span>
* <span data-ttu-id="cfdd1-2238">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2238">Added container group restart policy</span></span>
* <span data-ttu-id="cfdd1-2239">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2239">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="cfdd1-2240">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2240">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="cfdd1-2241">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2241">Data Lake Analytics</span></span>

* <span data-ttu-id="cfdd1-2242">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2242">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="cfdd1-2243">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2243">Data Lake Store</span></span>

* <span data-ttu-id="cfdd1-2244">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2244">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="cfdd1-2245">拡張機能</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2245">Extension</span></span>

* <span data-ttu-id="cfdd1-2246">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2246">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="cfdd1-2247">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2247">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="cfdd1-2248">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2248">IoT</span></span>

* <span data-ttu-id="cfdd1-2249">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2249">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-2250">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2250">Monitor</span></span>

* <span data-ttu-id="cfdd1-2251">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2251">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-2252">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2252">Network</span></span>

* <span data-ttu-id="cfdd1-2253">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2253">Added support for CAA DNS records</span></span>
* <span data-ttu-id="cfdd1-2254">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2254">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="cfdd1-2255">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2255">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="cfdd1-2256">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2256">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="cfdd1-2257">Reservations</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2257">Reservations</span></span>

* <span data-ttu-id="cfdd1-2258">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2258">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-2259">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2259">Resource</span></span>

* <span data-ttu-id="cfdd1-2260">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2260">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-2261">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2261">SQL</span></span>

* <span data-ttu-id="cfdd1-2262">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2262">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-2263">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2263">Storage</span></span>

* <span data-ttu-id="cfdd1-2264">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2264">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="cfdd1-2265">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2265">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="cfdd1-2266">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2266">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="cfdd1-2267">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2267">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="cfdd1-2268">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2268">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="cfdd1-2269">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2269">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="cfdd1-2270">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2270">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2271">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2271">VM</span></span>

* <span data-ttu-id="cfdd1-2272">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2272">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="cfdd1-2273">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2273">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="cfdd1-2274">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2274">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="cfdd1-2275">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2275">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="cfdd1-2276">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2276">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="cfdd1-2277">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2277">October 24, 2017</span></span>

<span data-ttu-id="cfdd1-2278">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2278">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-2279">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2279">Core</span></span>

* <span data-ttu-id="cfdd1-2280">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2280">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-2281">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2281">ACR</span></span>

* <span data-ttu-id="cfdd1-2282">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2282">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="cfdd1-2283">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2283">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="cfdd1-2284">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2284">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-2285">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2285">ACS</span></span>

* <span data-ttu-id="cfdd1-2286">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2286">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="cfdd1-2287">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2287">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-2288">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2288">Appservice</span></span>

* <span data-ttu-id="cfdd1-2289">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2289">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="cfdd1-2290">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2290">Component</span></span>

* <span data-ttu-id="cfdd1-2291">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2291">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-2292">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2292">Monitor</span></span>

* <span data-ttu-id="cfdd1-2293">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2293">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-2294">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2294">Resource</span></span>

* <span data-ttu-id="cfdd1-2295">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2295">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="cfdd1-2296">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2296">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2297">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2297">VM</span></span>

* <span data-ttu-id="cfdd1-2298">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2298">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="cfdd1-2299">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2299">October 9, 2017</span></span>

<span data-ttu-id="cfdd1-2300">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2300">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-2301">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2301">Core</span></span>

* <span data-ttu-id="cfdd1-2302">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2302">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-2303">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2303">Appservice</span></span>

* <span data-ttu-id="cfdd1-2304">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2304">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-2305">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2305">Batch</span></span>

* <span data-ttu-id="cfdd1-2306">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2306">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="cfdd1-2307">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2307">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="cfdd1-2308">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2308">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="cfdd1-2309">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2309">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="cfdd1-2310">Batchai</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2310">Batchai</span></span>

* <span data-ttu-id="cfdd1-2311">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2311">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="cfdd1-2312">KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2312">Keyvault</span></span>

* <span data-ttu-id="cfdd1-2313">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2313">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="cfdd1-2314">(#4448)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2314">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="cfdd1-2315">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2315">Network</span></span>

* <span data-ttu-id="cfdd1-2316">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2316">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="cfdd1-2317">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2317">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-2318">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2318">Resource</span></span>

* <span data-ttu-id="cfdd1-2319">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2319">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="cfdd1-2320">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2320">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="cfdd1-2321">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2321">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="cfdd1-2322">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2322">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-2323">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2323">Sql</span></span>

* <span data-ttu-id="cfdd1-2324">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2324">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="cfdd1-2325">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2325">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="cfdd1-2326">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2326">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-2327">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2327">Storage</span></span>

* <span data-ttu-id="cfdd1-2328">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2328">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2329">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2329">Vm</span></span>

* <span data-ttu-id="cfdd1-2330">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2330">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="cfdd1-2331">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2331">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="cfdd1-2332">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2332">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="cfdd1-2333">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2333">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="cfdd1-2334">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2334">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="cfdd1-2335">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2335">September 22, 2017</span></span>

<span data-ttu-id="cfdd1-2336">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2336">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-2337">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2337">Resource</span></span>

* <span data-ttu-id="cfdd1-2338">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2338">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="cfdd1-2339">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2339">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="cfdd1-2340">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2340">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="cfdd1-2341">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2341">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-2342">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2342">Network</span></span>

* <span data-ttu-id="cfdd1-2343">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2343">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="cfdd1-2344">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2344">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="cfdd1-2345">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2345">Added `asg` application security group commands</span></span>
* <span data-ttu-id="cfdd1-2346">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2346">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="cfdd1-2347">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2347">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="cfdd1-2348">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2348">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="cfdd1-2349">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2349">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-2350">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2350">Storage</span></span>

* <span data-ttu-id="cfdd1-2351">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2351">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="cfdd1-2352">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2352">Eventgrid</span></span>

* <span data-ttu-id="cfdd1-2353">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2353">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-2354">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2354">SQL</span></span>

* <span data-ttu-id="cfdd1-2355">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2355">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="cfdd1-2356">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2356">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="cfdd1-2357">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2357">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="cfdd1-2358">KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2358">Keyvault</span></span>

* <span data-ttu-id="cfdd1-2359">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2359">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2360">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2360">VM</span></span>

* <span data-ttu-id="cfdd1-2361">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2361">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="cfdd1-2362">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2362">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="cfdd1-2363">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2363">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="cfdd1-2364">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2364">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="cfdd1-2365">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2365">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="cfdd1-2366">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2366">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-2367">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2367">ACS</span></span>

* <span data-ttu-id="cfdd1-2368">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2368">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-2369">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2369">Appservice</span></span>

* <span data-ttu-id="cfdd1-2370">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2370">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="cfdd1-2371">バックアップ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2371">Backup</span></span>

* <span data-ttu-id="cfdd1-2372">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2372">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="cfdd1-2373">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2373">September 11, 2017</span></span>

<span data-ttu-id="cfdd1-2374">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2374">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="cfdd1-2375">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2375">Core</span></span>

* <span data-ttu-id="cfdd1-2376">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2376">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="cfdd1-2377">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2377">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-2378">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2378">Acs</span></span>

* <span data-ttu-id="cfdd1-2379">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2379">Added `acs list-locations` command</span></span>
* <span data-ttu-id="cfdd1-2380">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2380">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-2381">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2381">Appservice</span></span>

* <span data-ttu-id="cfdd1-2382">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2382">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="cfdd1-2383">CDN</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2383">CDN</span></span>

* <span data-ttu-id="cfdd1-2384">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2384">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="cfdd1-2385">拡張機能</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2385">Extension</span></span>

* <span data-ttu-id="cfdd1-2386">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2386">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="cfdd1-2387">KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2387">Keyvault</span></span>

* <span data-ttu-id="cfdd1-2388">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2388">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-2389">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2389">Network</span></span>

* <span data-ttu-id="cfdd1-2390">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2390">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="cfdd1-2391">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2391">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="cfdd1-2392">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2392">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="cfdd1-2393">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2393">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="cfdd1-2394">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2394">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-2395">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2395">Resource</span></span>

* <span data-ttu-id="cfdd1-2396">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2396">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="cfdd1-2397">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2397">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="cfdd1-2398">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2398">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="cfdd1-2399">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2399">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-2400">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2400">SQL</span></span>

* <span data-ttu-id="cfdd1-2401">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2401">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2402">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2402">VM</span></span>

* <span data-ttu-id="cfdd1-2403">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2403">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="cfdd1-2404">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2404">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="cfdd1-2405">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2405">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="cfdd1-2406">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2406">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="cfdd1-2407">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2407">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="cfdd1-2408">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2408">August 31, 2017</span></span>

<span data-ttu-id="cfdd1-2409">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2409">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="cfdd1-2410">KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2410">Keyvault</span></span>

* <span data-ttu-id="cfdd1-2411">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2411">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="cfdd1-2412">SF</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2412">Sf</span></span>

* <span data-ttu-id="cfdd1-2413">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2413">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-2414">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2414">Storage</span></span>

* <span data-ttu-id="cfdd1-2415">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2415">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="cfdd1-2416">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2416">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="cfdd1-2417">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2417">August 28, 2017</span></span>

<span data-ttu-id="cfdd1-2418">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2418">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="cfdd1-2419">CLI</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2419">CLI</span></span>

* <span data-ttu-id="cfdd1-2420">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2420">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-2421">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2421">ACS</span></span>

* <span data-ttu-id="cfdd1-2422">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2422">Corrected preview regions</span></span>
* <span data-ttu-id="cfdd1-2423">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2423">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="cfdd1-2424">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2424">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-2425">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2425">Appservice</span></span>

* <span data-ttu-id="cfdd1-2426">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2426">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="cfdd1-2427">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2427">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="cfdd1-2428">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2428">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="cfdd1-2429">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2429">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="cfdd1-2430">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2430">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="cfdd1-2431">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2431">IoT</span></span>

* <span data-ttu-id="cfdd1-2432">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2432">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-2433">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2433">Network</span></span>

* <span data-ttu-id="cfdd1-2434">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2434">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="cfdd1-2435">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2435">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="cfdd1-2436">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2436">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="cfdd1-2437">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2437">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="cfdd1-2438">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2438">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="cfdd1-2439">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2439">Profile</span></span>

* <span data-ttu-id="cfdd1-2440">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2440">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="cfdd1-2441">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2441">Service Fabric</span></span>

* <span data-ttu-id="cfdd1-2442">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2442">Preview release</span></span>
* <span data-ttu-id="cfdd1-2443">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2443">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="cfdd1-2444">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2444">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="cfdd1-2445">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2445">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-2446">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2446">Storage</span></span>

* <span data-ttu-id="cfdd1-2447">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2447">Enabled setting blob tier</span></span>
* <span data-ttu-id="cfdd1-2448">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2448">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="cfdd1-2449">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2449">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="cfdd1-2450">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2450">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="cfdd1-2451">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2451">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="cfdd1-2452">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2452">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2453">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2453">VM</span></span>

* <span data-ttu-id="cfdd1-2454">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2454">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="cfdd1-2455">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2455">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="cfdd1-2456">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2456">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="cfdd1-2457">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2457">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="cfdd1-2458">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2458">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="cfdd1-2459">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2459">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="cfdd1-2460">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2460">August 15, 2017</span></span>

<span data-ttu-id="cfdd1-2461">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2461">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-2462">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2462">ACS</span></span>

* <span data-ttu-id="cfdd1-2463">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2463">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-2464">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2464">Appservice</span></span>

* <span data-ttu-id="cfdd1-2465">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2465">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="cfdd1-2466">Event Grid</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2466">Event Grid</span></span>

* <span data-ttu-id="cfdd1-2467">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2467">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="cfdd1-2468">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2468">August 11, 2017</span></span>

<span data-ttu-id="cfdd1-2469">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2469">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-2470">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2470">ACS</span></span>

* <span data-ttu-id="cfdd1-2471">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2471">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-2472">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2472">Batch</span></span>

* <span data-ttu-id="cfdd1-2473">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2473">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="cfdd1-2474">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2474">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="cfdd1-2475">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2475">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="cfdd1-2476">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2476">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="cfdd1-2477">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2477">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="cfdd1-2478">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2478">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="cfdd1-2479">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2479">Component</span></span>

* <span data-ttu-id="cfdd1-2480">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2480">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="cfdd1-2481">コンテナー</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2481">Container</span></span>

* <span data-ttu-id="cfdd1-2482">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2482">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="cfdd1-2483">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2483">Data Lake Store</span></span>

* <span data-ttu-id="cfdd1-2484">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2484">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="cfdd1-2485">Event Grid</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2485">Event Grid</span></span>

* <span data-ttu-id="cfdd1-2486">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2486">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-2487">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2487">Network</span></span>

* <span data-ttu-id="cfdd1-2488">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2488">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="cfdd1-2489">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2489">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="cfdd1-2490">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2490">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="cfdd1-2491">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2491">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="cfdd1-2492">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2492">Profile</span></span>

* <span data-ttu-id="cfdd1-2493">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2493">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-2494">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2494">Storage</span></span>

* <span data-ttu-id="cfdd1-2495">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2495">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2496">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2496">VM</span></span>

* <span data-ttu-id="cfdd1-2497">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2497">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="cfdd1-2498">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2498">Exposed `list-skus` command</span></span>
* <span data-ttu-id="cfdd1-2499">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2499">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="cfdd1-2500">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2500">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="cfdd1-2501">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2501">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="cfdd1-2502">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2502">July 28, 2017</span></span>

<span data-ttu-id="cfdd1-2503">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2503">Version 2.0.12</span></span>

* <span data-ttu-id="cfdd1-2504">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2504">Added container commands</span></span>
* <span data-ttu-id="cfdd1-2505">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2505">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="cfdd1-2506">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2506">Core</span></span>

* <span data-ttu-id="cfdd1-2507">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2507">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="cfdd1-2508">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2508">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="cfdd1-2509">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2509">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="cfdd1-2510">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2510">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="cfdd1-2511">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2511">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="cfdd1-2512">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2512">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="cfdd1-2513">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2513">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="cfdd1-2514">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2514">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="cfdd1-2515">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2515">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="cfdd1-2516">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2516">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="cfdd1-2517">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2517">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="cfdd1-2518">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2518">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="cfdd1-2519">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2519">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="cfdd1-2520">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2520">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="cfdd1-2521">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2521">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="cfdd1-2522">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2522">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="cfdd1-2523">ACR</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2523">ACR</span></span>

* <span data-ttu-id="cfdd1-2524">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2524">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="cfdd1-2525">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2525">Support SKU update for managed registries</span></span>
* <span data-ttu-id="cfdd1-2526">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2526">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="cfdd1-2527">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2527">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="cfdd1-2528">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2528">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="cfdd1-2529">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2529">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-2530">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2530">ACS</span></span>

* <span data-ttu-id="cfdd1-2531">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2531">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-2532">Appservice</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2532">Appservice</span></span>

* <span data-ttu-id="cfdd1-2533">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2533">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="cfdd1-2534">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2534">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="cfdd1-2535">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2535">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="cfdd1-2536">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2536">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="cfdd1-2537">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2537">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="cfdd1-2538">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2538">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="cfdd1-2539">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2539">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="cfdd1-2540">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2540">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="cfdd1-2541">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2541">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="cfdd1-2542">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2542">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="cfdd1-2543">Batch</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2543">Batch</span></span>

* <span data-ttu-id="cfdd1-2544">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2544">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="cfdd1-2545">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2545">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="cfdd1-2546">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2546">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="cfdd1-2547">CDN</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2547">CDN</span></span>

* <span data-ttu-id="cfdd1-2548">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2548">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="cfdd1-2549">クラウド</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2549">Cloud</span></span>

* <span data-ttu-id="cfdd1-2550">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2550">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="cfdd1-2551">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2551">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="cfdd1-2552">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2552">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="cfdd1-2553">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2553">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="cfdd1-2554">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2554">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="cfdd1-2555">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2555">CosmosDB</span></span>

* <span data-ttu-id="cfdd1-2556">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2556">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="cfdd1-2557">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2557">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="cfdd1-2558">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2558">Data Lake Analytics</span></span>

* <span data-ttu-id="cfdd1-2559">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2559">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="cfdd1-2560">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2560">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="cfdd1-2561">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2561">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="cfdd1-2562">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2562">Data Lake Store</span></span>

* <span data-ttu-id="cfdd1-2563">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2563">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="cfdd1-2564">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2564">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="cfdd1-2565">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2565">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="cfdd1-2566">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2566">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="cfdd1-2567">対話</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2567">Interactive</span></span>

* <span data-ttu-id="cfdd1-2568">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2568">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="cfdd1-2569">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2569">Increased test coverage</span></span>
* <span data-ttu-id="cfdd1-2570">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2570">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="cfdd1-2571">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2571">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="cfdd1-2572">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2572">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="cfdd1-2573">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2573">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="cfdd1-2574">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2574">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="cfdd1-2575">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2575">Added `--progress` flag</span></span>
* <span data-ttu-id="cfdd1-2576">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2576">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="cfdd1-2577">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2577">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="cfdd1-2578">IoT</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2578">IoT</span></span>

* <span data-ttu-id="cfdd1-2579">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2579">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="cfdd1-2580">(#3934)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2580">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="cfdd1-2581">Key Vault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2581">Key vault</span></span>

* <span data-ttu-id="cfdd1-2582">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2582">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="cfdd1-2583">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2583">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="cfdd1-2584">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2584">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="cfdd1-2585">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2585">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="cfdd1-2586">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2586">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="cfdd1-2587">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2587">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="cfdd1-2588">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2588">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="cfdd1-2589">(#3307)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2589">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="cfdd1-2590">ラボ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2590">Lab</span></span>

* <span data-ttu-id="cfdd1-2591">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2591">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="cfdd1-2592">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2592">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-2593">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2593">Monitor</span></span>

* <span data-ttu-id="cfdd1-2594">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2594">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="cfdd1-2595">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2595">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="cfdd1-2596">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2596">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="cfdd1-2597">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2597">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="cfdd1-2598">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2598">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="cfdd1-2599">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2599">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="cfdd1-2600">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2600">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="cfdd1-2601">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2601">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="cfdd1-2602">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2602">`location` no longer required</span></span>
  * <span data-ttu-id="cfdd1-2603">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2603">Add name and ID support for target</span></span>
  * <span data-ttu-id="cfdd1-2604">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2604">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="cfdd1-2605">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2605">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="cfdd1-2606">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2606">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="cfdd1-2607">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2607">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="cfdd1-2608">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2608">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="cfdd1-2609">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2609">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-2610">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2610">Network</span></span>

* <span data-ttu-id="cfdd1-2611">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2611">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="cfdd1-2612">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2612">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="cfdd1-2613">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2613">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="cfdd1-2614">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2614">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="cfdd1-2615">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2615">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="cfdd1-2616">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2616">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="cfdd1-2617">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2617">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="cfdd1-2618">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2618">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="cfdd1-2619">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2619">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="cfdd1-2620">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2620">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="cfdd1-2621">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2621">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="cfdd1-2622">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2622">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="cfdd1-2623">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2623">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="cfdd1-2624">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2624">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="cfdd1-2625">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2625">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="cfdd1-2626">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2626">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="cfdd1-2627">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2627">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="cfdd1-2628">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2628">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="cfdd1-2629">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2629">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="cfdd1-2630">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2630">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="cfdd1-2631">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2631">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="cfdd1-2632">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2632">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="cfdd1-2633">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2633">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="cfdd1-2634">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2634">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="cfdd1-2635">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2635">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="cfdd1-2636">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2636">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="cfdd1-2637">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2637">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="cfdd1-2638">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2638">Profile</span></span>

* <span data-ttu-id="cfdd1-2639">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2639">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="cfdd1-2640">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2640">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="cfdd1-2641">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2641">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="cfdd1-2642">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2642">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="cfdd1-2643">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2643">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="cfdd1-2644">RDBMS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2644">RDBMS</span></span>

* <span data-ttu-id="cfdd1-2645">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2645">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="cfdd1-2646">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2646">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="cfdd1-2647">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2647">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="cfdd1-2648">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2648">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-2649">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2649">Resource</span></span>

* <span data-ttu-id="cfdd1-2650">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2650">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="cfdd1-2651">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2651">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="cfdd1-2652">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2652">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="cfdd1-2653">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2653">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="cfdd1-2654">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2654">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="cfdd1-2655">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2655">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="cfdd1-2656">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2656">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="cfdd1-2657">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2657">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-2658">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2658">Role</span></span>

* <span data-ttu-id="cfdd1-2659">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2659">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="cfdd1-2660">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2660">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="cfdd1-2661">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2661">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="cfdd1-2662">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2662">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="cfdd1-2663">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2663">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="cfdd1-2664">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2664">Service Fabric</span></span>
* <span data-ttu-id="cfdd1-2665">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2665">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="cfdd1-2666">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2666">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="cfdd1-2667">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2667">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-2668">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2668">SQL</span></span>

* <span data-ttu-id="cfdd1-2669">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2669">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="cfdd1-2670">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2670">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="cfdd1-2671">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2671">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-2672">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2672">Storage</span></span>

* <span data-ttu-id="cfdd1-2673">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2673">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="cfdd1-2674">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2674">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="cfdd1-2675">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2675">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="cfdd1-2676">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2676">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="cfdd1-2677">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2677">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="cfdd1-2678">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2678">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2679">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2679">VM</span></span>

* <span data-ttu-id="cfdd1-2680">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2680">Support configuring nsg</span></span>
* <span data-ttu-id="cfdd1-2681">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2681">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="cfdd1-2682">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2682">Support managed service identities</span></span>
* <span data-ttu-id="cfdd1-2683">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2683">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="cfdd1-2684">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2684">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="cfdd1-2685">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2685">May 10, 2017</span></span>

<span data-ttu-id="cfdd1-2686">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2686">Version 2.0.6</span></span>

* <span data-ttu-id="cfdd1-2687">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2687">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="cfdd1-2688">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2688">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="cfdd1-2689">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2689">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="cfdd1-2690">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2690">Include Cognitive Services module</span></span>
* <span data-ttu-id="cfdd1-2691">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2691">Include Service Fabric module</span></span>
* <span data-ttu-id="cfdd1-2692">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2692">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="cfdd1-2693">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2693">Add support for CDN commands</span></span>
* <span data-ttu-id="cfdd1-2694">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2694">Remove Container module</span></span>
* <span data-ttu-id="cfdd1-2695">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2695">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="cfdd1-2696">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2696">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="cfdd1-2697">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2697">Core</span></span>

* <span data-ttu-id="cfdd1-2698">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2698">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="cfdd1-2699">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2699">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="cfdd1-2700">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2700">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="cfdd1-2701">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2701">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="cfdd1-2702">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2702">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="cfdd1-2703">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2703">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="cfdd1-2704">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2704">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="cfdd1-2705">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2705">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="cfdd1-2706">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2706">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="cfdd1-2707">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2707">core: Improved performance</span></span>
* <span data-ttu-id="cfdd1-2708">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2708">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="cfdd1-2709">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2709">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-2710">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2710">ACS</span></span>

* <span data-ttu-id="cfdd1-2711">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2711">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="cfdd1-2712">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2712">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="cfdd1-2713">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2713">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="cfdd1-2714">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2714">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-2715">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2715">AppService</span></span>

* <span data-ttu-id="cfdd1-2716">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2716">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="cfdd1-2717">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2717">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="cfdd1-2718">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2718">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="cfdd1-2719">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2719">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="cfdd1-2720">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2720">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="cfdd1-2721">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2721">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="cfdd1-2722">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2722">support slot swap with preview</span></span>
* <span data-ttu-id="cfdd1-2723">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2723">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="cfdd1-2724">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2724">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="cfdd1-2725">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2725">CosmosDB</span></span>

* <span data-ttu-id="cfdd1-2726">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2726">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="cfdd1-2727">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2727">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="cfdd1-2728">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2728">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="cfdd1-2729">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2729">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="cfdd1-2730">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2730">Data Lake Analytics</span></span>

* <span data-ttu-id="cfdd1-2731">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2731">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="cfdd1-2732">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2732">Add support for new catalog item type: package.</span></span> <span data-ttu-id="cfdd1-2733">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2733">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="cfdd1-2734">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2734">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="cfdd1-2735">テーブル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2735">Table</span></span>
  * <span data-ttu-id="cfdd1-2736">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2736">Table valued function</span></span>
  * <span data-ttu-id="cfdd1-2737">表示</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2737">View</span></span>
  * <span data-ttu-id="cfdd1-2738">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2738">Table Statistics.</span></span> <span data-ttu-id="cfdd1-2739">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2739">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="cfdd1-2740">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2740">Data Lake Store</span></span>

* <span data-ttu-id="cfdd1-2741">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2741">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="cfdd1-2742">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2742">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="cfdd1-2743">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2743">missed help for access show.</span></span> <span data-ttu-id="cfdd1-2744">追加しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2744">adding it.</span></span> <span data-ttu-id="cfdd1-2745">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2745">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="cfdd1-2746">検索</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2746">Find</span></span>

* <span data-ttu-id="cfdd1-2747">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2747">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="cfdd1-2748">KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2748">KeyVault</span></span>

* <span data-ttu-id="cfdd1-2749">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2749">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="cfdd1-2750">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2750">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="cfdd1-2751">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2751">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="cfdd1-2752">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2752">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="cfdd1-2753">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2753">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="cfdd1-2754">ラボ</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2754">Lab</span></span>

* <span data-ttu-id="cfdd1-2755">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2755">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="cfdd1-2756">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2756">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="cfdd1-2757">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2757">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="cfdd1-2758">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2758">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="cfdd1-2759">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2759">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="cfdd1-2760">監視</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2760">Monitor</span></span>

* <span data-ttu-id="cfdd1-2761">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2761">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="cfdd1-2762">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2762">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="cfdd1-2763">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2763">Network</span></span>

* <span data-ttu-id="cfdd1-2764">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2764">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="cfdd1-2765">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2765">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="cfdd1-2766">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2766">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="cfdd1-2767">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2767">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="cfdd1-2768">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2768">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="cfdd1-2769">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2769">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="cfdd1-2770">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2770">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="cfdd1-2771">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2771">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="cfdd1-2772">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2772">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="cfdd1-2773">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2773">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="cfdd1-2774">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2774">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="cfdd1-2775">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2775">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="cfdd1-2776">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2776">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="cfdd1-2777">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2777">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="cfdd1-2778">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2778">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="cfdd1-2779">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2779">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="cfdd1-2780">プロファイル</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2780">Profile</span></span>

* <span data-ttu-id="cfdd1-2781">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2781">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="cfdd1-2782">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2782">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="cfdd1-2783">Redis</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2783">Redis</span></span>

* <span data-ttu-id="cfdd1-2784">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2784">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="cfdd1-2785">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2785">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="cfdd1-2786">リソース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2786">Resource</span></span>

* <span data-ttu-id="cfdd1-2787">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2787">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="cfdd1-2788">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2788">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="cfdd1-2789">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2789">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="cfdd1-2790">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2790">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="cfdd1-2791">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2791">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="cfdd1-2792">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2792">Add docs for az lock update.</span></span> <span data-ttu-id="cfdd1-2793">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2793">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="cfdd1-2794">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2794">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="cfdd1-2795">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2795">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="cfdd1-2796">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2796">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="cfdd1-2797">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2797">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="cfdd1-2798">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2798">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="cfdd1-2799">Role</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2799">Role</span></span>

* <span data-ttu-id="cfdd1-2800">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2800">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="cfdd1-2801">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2801">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="cfdd1-2802">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2802">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="cfdd1-2803">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2803">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="cfdd1-2804">SQL</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2804">SQL</span></span>

* <span data-ttu-id="cfdd1-2805">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2805">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="cfdd1-2806">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2806">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="cfdd1-2807">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2807">Storage</span></span>

* <span data-ttu-id="cfdd1-2808">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2808">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="cfdd1-2809">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2809">Add support for incremental blob copy</span></span>
* <span data-ttu-id="cfdd1-2810">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2810">Add support for large block blob upload</span></span>
* <span data-ttu-id="cfdd1-2811">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2811">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2812">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2812">VM</span></span>

* <span data-ttu-id="cfdd1-2813">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2813">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="cfdd1-2814">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2814">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="cfdd1-2815">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2815">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="cfdd1-2816">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2816">az vm/vmss disk</span></span>
  3. <span data-ttu-id="cfdd1-2817">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2817">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="cfdd1-2818">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2818">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="cfdd1-2819">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2819">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="cfdd1-2820">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2820">April 3, 2017</span></span>

<span data-ttu-id="cfdd1-2821">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2821">Version 2.0.2</span></span>

<span data-ttu-id="cfdd1-2822">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2822">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="cfdd1-2823">コア</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2823">Core</span></span>

* <span data-ttu-id="cfdd1-2824">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2824">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="cfdd1-2825">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2825">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="cfdd1-2826">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2826">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="cfdd1-2827">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2827">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="cfdd1-2828">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2828">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="cfdd1-2829">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2829">Add prompting for missing template parameters.</span></span> <span data-ttu-id="cfdd1-2830">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2830">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="cfdd1-2831">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2831">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="cfdd1-2832">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2832">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="cfdd1-2833">ACS</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2833">ACS</span></span>

* <span data-ttu-id="cfdd1-2834">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2834">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="cfdd1-2835">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2835">Add support for ssh key password prompting.</span></span> <span data-ttu-id="cfdd1-2836">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2836">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="cfdd1-2837">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2837">Add support for windows clusters.</span></span> <span data-ttu-id="cfdd1-2838">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2838">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="cfdd1-2839">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2839">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="cfdd1-2840">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2840">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="cfdd1-2841">AppService</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2841">AppService</span></span>

* <span data-ttu-id="cfdd1-2842">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2842">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="cfdd1-2843">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2843">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="cfdd1-2844">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2844">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="cfdd1-2845">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2845">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="cfdd1-2846">DataLake</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2846">DataLake</span></span>

* <span data-ttu-id="cfdd1-2847">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2847">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="cfdd1-2848">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2848">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="cfdd1-2849">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2849">DocuemntDB</span></span>

* <span data-ttu-id="cfdd1-2850">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2850">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="cfdd1-2851">VM</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2851">VM</span></span>

* <span data-ttu-id="cfdd1-2852">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2852">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="cfdd1-2853">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2853">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="cfdd1-2854">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2854">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="cfdd1-2855">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2855">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="cfdd1-2856">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2856">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="cfdd1-2857">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2857">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="cfdd1-2858">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2858">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="cfdd1-2859">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2859">February 27, 2017</span></span>

<span data-ttu-id="cfdd1-2860">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2860">Version 2.0.0</span></span>

<span data-ttu-id="cfdd1-2861">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2861">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="cfdd1-2862">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2862">Container Service (acs)</span></span>
- <span data-ttu-id="cfdd1-2863">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2863">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="cfdd1-2864">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2864">Networking</span></span>
- <span data-ttu-id="cfdd1-2865">Storage</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2865">Storage</span></span>

<span data-ttu-id="cfdd1-2866">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2866">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="cfdd1-2867">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2867">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="cfdd1-2868">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2868">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="cfdd1-2869">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2869">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="cfdd1-2870">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2870">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="cfdd1-2871">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2871">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="cfdd1-2872">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2872">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="cfdd1-2873">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2873">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="cfdd1-2874">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="cfdd1-2874">Provide feedback from the command line with the `az feedback` command</span></span>

