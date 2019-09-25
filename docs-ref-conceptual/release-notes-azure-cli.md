---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/05/2019
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 1f829ba3d9ecdb158e96512bde5bcf1565cc205c
ms.sourcegitcommit: 5b9b4446c08b94256ced7f63c145b493ba8b50df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "71217417"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="78af3-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="78af3-103">Azure CLI release notes</span></span>

## <a name="september-24-2019"></a><span data-ttu-id="78af3-104">2019 年 9 月 24 日</span><span class="sxs-lookup"><span data-stu-id="78af3-104">September 24, 2019</span></span>

<span data-ttu-id="78af3-105">バージョン 2.0.74</span><span class="sxs-lookup"><span data-stu-id="78af3-105">Version 2.0.74</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-106">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-106">ACR</span></span>

* <span data-ttu-id="78af3-107">必須の `--type` パラメーターを `acr config retention update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-107">Added a required `--type` parameter to `acr config retention update`</span></span>
* <span data-ttu-id="78af3-108">[破壊的変更] `acr config` コマンド グループでパラメーター `--name -n` の名前が `--registry -r ` に変更されました</span><span class="sxs-lookup"><span data-stu-id="78af3-108">[BREAKING CHNAGE] Renamed parameter `--name -n` changed to `--registry -r ` for `acr config` command group</span></span>

### <a name="aks"></a><span data-ttu-id="78af3-109">AKS</span><span class="sxs-lookup"><span data-stu-id="78af3-109">AKS</span></span>

* <span data-ttu-id="78af3-110">`--load-balancer-sku` パラメーターを `aks create` コマンドに追加しました。これにより、SLB を使用する AKS クラスターを作成できます</span><span class="sxs-lookup"><span data-stu-id="78af3-110">Added `--load-balancer-sku` parameter to `aks create` command, which allows for creating AKS cluster with SLB</span></span>
* <span data-ttu-id="78af3-111">`--load-balancer-managed-outbound-ip-count`、`--load-balancer-outbound-ips`、`--load-balancer-outbound-ip-prefixes` パラメーターを `aks [create|update]` コマンドに追加しました。これにより、SLB を使用する AKS クラスターのロード バランサー プロファイルを更新できます</span><span class="sxs-lookup"><span data-stu-id="78af3-111">Added `--load-balancer-managed-outbound-ip-count`, `--load-balancer-outbound-ips` and `--load-balancer-outbound-ip-prefixes` parameters to `aks [create|update]` commands, which allow for updating load balancer profile of an AKS cluster with SLB</span></span>
* <span data-ttu-id="78af3-112">`--vm-set-type` パラメーターを `aks create` コマンドに追加しました。これにより、AKS クラスターの VM の種類 (vmas または vmss) を指定できます</span><span class="sxs-lookup"><span data-stu-id="78af3-112">Added `--vm-set-type` parameter to `aks create` command, which allows to specify vm types of an AKS Cluster (vmas or vmss)</span></span>

### <a name="arm"></a><span data-ttu-id="78af3-113">ARM</span><span class="sxs-lookup"><span data-stu-id="78af3-113">ARM</span></span>

* <span data-ttu-id="78af3-114">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `group deployment create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-114">Added `--handle-extended-json-format` parameter to `group deployment create` command to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="78af3-115">Compute</span><span class="sxs-lookup"><span data-stu-id="78af3-115">Compute</span></span>

* <span data-ttu-id="78af3-116">終了のスケジュール化されたイベントを構成しやすくするために `--terminate-notification-time` パラメーターを `vmss [create|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-116">Added `--terminate-notification-time` parameter to `vmss [create|update]` commands to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="78af3-117">終了のスケジュール化されたイベントを構成しやすくするために `--enable-terminate-notification` パラメーターを `vmss update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-117">Added `--enable-terminate-notification` parameter to `vmss update` command to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="78af3-118">`--priority,` `--eviction-policy,` `--max-billing` パラメーターを `[vm|vmss] create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-118">Added `--priority,` `--eviction-policy,` `--max-billing` parameters to `[vm|vmss] create` commands</span></span>
* <span data-ttu-id="78af3-119">`disk create` を変更し、ディスク アップロードの正確なサイズを指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="78af3-119">Changed `disk create` to allow specifying the exact size of the disk upload</span></span>
* <span data-ttu-id="78af3-120">マネージド ディスクの増分スナップショットのサポートを `snapshot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-120">Added support for incremental snapshots for managed disks to `snapshot create`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="78af3-121">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="78af3-121">Cosmos DB</span></span>

* <span data-ttu-id="78af3-122">キー、読み取り専用キー、または接続文字列を表示する `--type <key-type>` パラメーターを `cosmosdb keys list` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-122">Added `--type <key-type>` parameter to `cosmosdb keys list` command to show key, read only keys or connection strings</span></span>
* <span data-ttu-id="78af3-123">`cosmosdb keys regenerate` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-123">Added `cosmosdb keys regenerate` command</span></span>
* <span data-ttu-id="78af3-124">[非推奨] `cosmosdb list-connection-strings`、`cosmosdb regenerate-key`、`cosmosdb list-read-only-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-124">[DEPRECATED] Deprecated `cosmosdb list-connection-strings`, `cosmosdb regenerate-key` and `cosmosdb list-read-only-keys` commands</span></span>

### <a name="eventgrid"></a><span data-ttu-id="78af3-125">EventGrid</span><span class="sxs-lookup"><span data-stu-id="78af3-125">EventGrid</span></span>

* <span data-ttu-id="78af3-126">正しいパラメーターを参照するようにエンドポイントのヘルプ テキストを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-126">Fixed the endpoint help text to refer to the right parameter</span></span>

### <a name="key-vault"></a><span data-ttu-id="78af3-127">Key Vault</span><span class="sxs-lookup"><span data-stu-id="78af3-127">Key Vault</span></span>

* <span data-ttu-id="78af3-128">テナントを使用してログインすると (`login -t`)、`keyvault create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-128">Fixed issue where logging in with a tenant (`login -t`) could cause `keyvault create` to fail</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-129">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-129">Monitor</span></span>

* <span data-ttu-id="78af3-130">`monitor metrics alert create` の `--condition` 引数で `:` 文字を使用できないという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-130">Fixed issue where `:` character was not allowed in `--condition` argument to `monitor metrics alert create`</span></span>

### <a name="policy"></a><span data-ttu-id="78af3-131">ポリシー</span><span class="sxs-lookup"><span data-stu-id="78af3-131">Policy</span></span>

* <span data-ttu-id="78af3-132">Policy API バージョン 2019-06-01 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-132">Added support for Policy API version 2019-06-01</span></span>
* <span data-ttu-id="78af3-133">`policy assignment create` コマンドに `--enforcement-mode` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-133">Added `--enforcement-mode` parameter to `policy assignment create` command</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-134">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-134">Storage</span></span>

* <span data-ttu-id="78af3-135">`az storage copy` コマンドに `--blob-type` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-135">Added `--blob-type` parameter to `az storage copy` command</span></span>

## <a name="september-10-2019"></a><span data-ttu-id="78af3-136">2019 年 9 月 10 日</span><span class="sxs-lookup"><span data-stu-id="78af3-136">September 10, 2019</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-137">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-137">ACR</span></span>

* <span data-ttu-id="78af3-138">アイテム保持ポリシーを構成するためのコマンド グループ `acr config retention` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-138">Added command group `acr config retention` to configure retention policy</span></span>

### <a name="aks"></a><span data-ttu-id="78af3-139">AKS</span><span class="sxs-lookup"><span data-stu-id="78af3-139">AKS</span></span>

* <span data-ttu-id="78af3-140">次のコマンドを使用した ACR 統合のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="78af3-140">Added support for ACR integration with the following commands:</span></span>
  * <span data-ttu-id="78af3-141">AKS クラスターに ACR をアタッチするための `--attach-acr` パラメーターを `aks [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-141">Added `--attach-acr` parameter to `aks [create|update]` to attach an ACR to an AKS cluster</span></span>
  * <span data-ttu-id="78af3-142">AKS クラスターから ACR をデタッチするための `--detach-acr` パラメーターを `aks update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-142">Added `--detach-acr` parameter to `aks update` to detach the ACR from an AKS cluster</span></span>

### <a name="arm"></a><span data-ttu-id="78af3-143">ARM</span><span class="sxs-lookup"><span data-stu-id="78af3-143">ARM</span></span>

* <span data-ttu-id="78af3-144">API バージョン 2019-05-10 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-144">Updated to use API version 2019-05-10</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-145">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-145">Batch</span></span>

* <span data-ttu-id="78af3-146">`batch pool create` の `--json-file` に新しい JSON 構成設定を追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-146">Added new JSON configuration settings to `--json-file` for `batch pool create`:</span></span>
  * <span data-ttu-id="78af3-147">ファイル システム マウント用の `MountConfigurations` を追加しました (詳細については https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="78af3-147">Added `MountConfigurations` for file system mounts (see https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body for details)</span></span>
  * <span data-ttu-id="78af3-148">プール上のパブリック IP 用に、`NetworkConfiguration` にオプションのプロパティ `publicIPs` を追加しました (詳細については https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="78af3-148">Added optional property `publicIPs` on `NetworkConfiguration` for public IPs on pools (see https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body for details)</span></span>
* <span data-ttu-id="78af3-149">共有イメージ ギャラリーのサポートを `--image` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-149">Added support for shared image galleries to `--image`</span></span>
* <span data-ttu-id="78af3-150">[重大な変更] `batch pool create` の `--start-task-wait-for-success` の既定値を `true` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-150">[BREAKING CHANGE] Changed default value of `--start-task-wait-for-success` on `batch pool create` to be `true`</span></span>
* <span data-ttu-id="78af3-151">[重大な変更] `AutoUserSpecification` の `Scope` の既定値が常に Pool になるように変更しました (以前は Windows ノードでは `Task`、Linux ノードでは `Pool` でした)</span><span class="sxs-lookup"><span data-stu-id="78af3-151">[BREAKING CHANGE] Changed default value for `Scope` on `AutoUserSpecification` to always be Pool (was `Task` on Windows nodes, `Pool` on Linux nodes)</span></span>
  * <span data-ttu-id="78af3-152">この引数は、`--json-file` を使用して JSON 構成からのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="78af3-152">This argument can only be set from a JSON configuration with `--json-file`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="78af3-153">HDInsight</span><span class="sxs-lookup"><span data-stu-id="78af3-153">HDInsight</span></span>

* <span data-ttu-id="78af3-154">GA リリース</span><span class="sxs-lookup"><span data-stu-id="78af3-154">GA release</span></span>
* <span data-ttu-id="78af3-155">[重大な変更] `az hdinsight resize` のパラメーター `--workernode-count/-c` が必須に変更されました。</span><span class="sxs-lookup"><span data-stu-id="78af3-155">[BREAKING CHANGE] Changed parameter `--workernode-count/-c` of `az hdinsight resize` to be required.</span></span>

### <a name="key-vault"></a><span data-ttu-id="78af3-156">Key Vault</span><span class="sxs-lookup"><span data-stu-id="78af3-156">Key Vault</span></span>

* <span data-ttu-id="78af3-157">ネットワーク ルールからサブネットを削除できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-157">Fixed issue where subnets couldn't be deleted from network rules</span></span>
* <span data-ttu-id="78af3-158">重複したサブネットと IP アドレスをネットワーク ルールに追加できる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-158">Fixed issue where duplicated subnets and IP addresses could be added to network rules</span></span>

### <a name="network"></a><span data-ttu-id="78af3-159">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-159">Network</span></span>

* <span data-ttu-id="78af3-160">トラフィック分析間隔の値を設定する `--interval` パラメーターを `network watcher flow-log` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-160">Added `--interval` parameter to `network watcher flow-log` to set traffic analysis interval value</span></span>
* <span data-ttu-id="78af3-161">ゲートウェイ ID を管理するための `network application-gateway identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-161">Added `network application-gateway identity` to manage gateway identity</span></span>
* <span data-ttu-id="78af3-162">Key Vault ID を設定するためのサポートを `network application-gateway ssl-cert` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-162">Added support for setting Key Vault ID to `network application-gateway ssl-cert`</span></span>
* <span data-ttu-id="78af3-163">`network express-route peering peer-connection [show|list]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-163">Added `network express-route peering peer-connection [show|list]`</span></span>

### <a name="policy"></a><span data-ttu-id="78af3-164">ポリシー</span><span class="sxs-lookup"><span data-stu-id="78af3-164">Policy</span></span>

* <span data-ttu-id="78af3-165">API バージョン 2019-01-01 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-165">Updated to use API version 2019-01-01</span></span>

## <a name="august-27-2019"></a><span data-ttu-id="78af3-166">2019 年 8 月 27 日</span><span class="sxs-lookup"><span data-stu-id="78af3-166">August 27, 2019</span></span>

<span data-ttu-id="78af3-167">バージョン 2.0.72</span><span class="sxs-lookup"><span data-stu-id="78af3-167">Version 2.0.72</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-168">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-168">ACR</span></span>

* <span data-ttu-id="78af3-169">[重大な変更] `classic` SKU のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-169">[BREAKING CHANGE] Removed support for the `classic` SKU</span></span>

### <a name="api-management"></a><span data-ttu-id="78af3-170">API Management</span><span class="sxs-lookup"><span data-stu-id="78af3-170">API Management</span></span>

* <span data-ttu-id="78af3-171">[プレビュー] `apim` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-171">[PREVIEW] Added `apim` command group</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-172">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-172">AppService</span></span>

* <span data-ttu-id="78af3-173">スロットを指定したときの `webapp webjob continuous start` コマンドに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-173">Fixed issue with `webapp webjob continuous start` command when specifying a slot</span></span>
* <span data-ttu-id="78af3-174">`env` フォルダーを検出してデプロイに使用されているファイルから削除するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-174">Changed `webapp up` to detect `env` folder and remove it from the file used for deployment</span></span>

### <a name="keyvault"></a><span data-ttu-id="78af3-175">KeyVault</span><span class="sxs-lookup"><span data-stu-id="78af3-175">Keyvault</span></span>

* <span data-ttu-id="78af3-176">`--expires` 引数を無視する `keyvault secret set` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-176">Fixed a bug in `keyvault secret set` that igored the `--expires` argument</span></span>

### <a name="network"></a><span data-ttu-id="78af3-177">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-177">Network</span></span>

* <span data-ttu-id="78af3-178">`--private-ip-address-version` 引数に IPv6 アドレスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-178">Added support for IPv6 addresses to `--private-ip-address-version` arguments</span></span>
* <span data-ttu-id="78af3-179">プライベート エンドポイントの管理用に新しいコマンド `network private-endpoint [create|update|list-types]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-179">Added new commands `network private-endpoint [create|update|list-types]` for private endpoint management</span></span>
* <span data-ttu-id="78af3-180">コマンド グループ `network private-link-service` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-180">Added command group `network private-link-service`</span></span>
* <span data-ttu-id="78af3-181">`--private-endpoint-network-policies` 引数と `--private-link-service-network-policies` 引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-181">Added `--private-endpoint-network-policies` and `--private-link-service-network-policies` arguments to `network vnet subnet update`</span></span>

### <a name="rbac"></a><span data-ttu-id="78af3-182">RBAC</span><span class="sxs-lookup"><span data-stu-id="78af3-182">RBAC</span></span>

* <span data-ttu-id="78af3-183">ホームページが更新されない `ad app update --homepage` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-183">Fixed issue with `ad app update --homepage` where homepage would not be updated</span></span>

### <a name="servicefabric"></a><span data-ttu-id="78af3-184">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="78af3-184">ServiceFabric</span></span>

* <span data-ttu-id="78af3-185">キー コンテナーの大文字と小文字が混在する名前のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-185">Added support for mixed-case Key Vault names</span></span>
* <span data-ttu-id="78af3-186">Key Vault で証明書を使用したときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-186">Fixed issue when using certificates in Key Vault</span></span>
* <span data-ttu-id="78af3-187">PFX 証明書ファイルの使用に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-187">Fixed issue with using PFX certificate files</span></span>
* <span data-ttu-id="78af3-188">Key Vault リソースグループが指定されていなかったときの `sf cluster certificate add` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-188">Fixed issue with `sf cluster certificate add` when Key Vault resource group wasn't specified</span></span>
* <span data-ttu-id="78af3-189">`sf cluster set` が動作しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-189">Fixed issue with `sf cluster set` not working</span></span>

### <a name="signalr"></a><span data-ttu-id="78af3-190">SignalR</span><span class="sxs-lookup"><span data-stu-id="78af3-190">SignalR</span></span>

* <span data-ttu-id="78af3-191">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-191">Added new commands:</span></span>
  * <span data-ttu-id="78af3-192">`signalr cors`:SignalR CORS の管理</span><span class="sxs-lookup"><span data-stu-id="78af3-192">`signalr cors`: Manage SignalR CORS</span></span>
  * <span data-ttu-id="78af3-193">`signalr restart`:SignalR Service の再起動</span><span class="sxs-lookup"><span data-stu-id="78af3-193">`signalr restart`: Restart a SignalR service</span></span>
  * <span data-ttu-id="78af3-194">`signalr update`:SignalR Service の更新</span><span class="sxs-lookup"><span data-stu-id="78af3-194">`signalr update`: Update a SignalR service</span></span>
* <span data-ttu-id="78af3-195">`--service-mode` 引数を `signalr create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-195">Added `--service-mode` argument to `signalr create`</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-196">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-196">Storage</span></span>

* <span data-ttu-id="78af3-197">`storage account revoke-delegation-keys` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-197">Added `storage account revoke-delegation-keys` command</span></span>

## <a name="august-13-2019"></a><span data-ttu-id="78af3-198">2019 年 8 月 13 日</span><span class="sxs-lookup"><span data-stu-id="78af3-198">August 13, 2019</span></span>

<span data-ttu-id="78af3-199">バージョン 2.0.71</span><span class="sxs-lookup"><span data-stu-id="78af3-199">Version 2.0.71</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-200">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-200">AppService</span></span>

* <span data-ttu-id="78af3-201">`webapp webjob continuous` コマンドがスロットで失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-201">Fixed issue where `webapp webjob continuous` commands were failing for slots</span></span>

### <a name="botservice"></a><span data-ttu-id="78af3-202">BotService</span><span class="sxs-lookup"><span data-stu-id="78af3-202">BotService</span></span>

* <span data-ttu-id="78af3-203">[重大な変更] v3 SDK ボットの作成のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-203">[BREAKING CHANGE] Removed support for creating v3 SDK bots</span></span>

### <a name="cognitiveservices"></a><span data-ttu-id="78af3-204">CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="78af3-204">CognitiveServices</span></span>

* <span data-ttu-id="78af3-205">`cognitiveservices account network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-205">Added `cognitiveservices account network-rule` commands</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="78af3-206">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="78af3-206">Cosmos DB</span></span>

* <span data-ttu-id="78af3-207">複数の書き込み場所を更新するときの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-207">Removed warning when updating multiple write locations</span></span>
* <span data-ttu-id="78af3-208">CosmosDB SQL、MongoDB、Cassandra、Gremlin、およびテーブル リソースとリソースのスループットのための CRUD コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-208">Added CRUD commands for CosmosDB SQL, MongoDB, Cassandra, Gremlin and Table resources and resource's throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="78af3-209">HDInsight</span><span class="sxs-lookup"><span data-stu-id="78af3-209">HDInsight</span></span>

<span data-ttu-id="78af3-210">このリリースには、多数の破壊的変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="78af3-210">This release contains a large number of breaking changes.</span></span>

* <span data-ttu-id="78af3-211">[重大な変更] `hdinsight create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-211">[BREAKING CHANGE] Renamed parameters for `hdinsight create`:</span></span>
  * <span data-ttu-id="78af3-212">`--storage-default-container` の名前を `--storage-container` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-212">Renamed `--storage-default-container` to `--storage-container`</span></span>
  * <span data-ttu-id="78af3-213">`--storage-default-filesystem` の名前を `--storage-filesystem` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-213">Renamed `--storage-default-filesystem` to `--storage-filesystem`</span></span>
* <span data-ttu-id="78af3-214">[重大な変更] `application create` の `--name` 引数が、クラスター名の代わりにアプリケーション名を表すように変更されました</span><span class="sxs-lookup"><span data-stu-id="78af3-214">[BREAKING CHANGE] Changed the `--name` argument of `application create` to represent the application name instead of the cluster name</span></span>
* <span data-ttu-id="78af3-215">`--cluster-name` 引数が `application create` に追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="78af3-215">Added `--cluster-name` argument to `application create` to replace old `--name` functionality</span></span>
* <span data-ttu-id="78af3-216">[重大な変更] `application create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-216">[BREAKING CHANGE] Renamed parameters for `application create`:</span></span>
  * <span data-ttu-id="78af3-217">`--application-type` の名前を `--type` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-217">Renamed `--application-type` to `--type`</span></span>
  * <span data-ttu-id="78af3-218">`--marketplace-identifier` の名前を `--marketplace-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-218">Renamed `--marketplace-identifier` to `--marketplace-id`</span></span>
  * <span data-ttu-id="78af3-219">`--https-endpoint-access-mode` の名前を `--access-mode` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-219">Renamed `--https-endpoint-access-mode` to `--access-mode`</span></span>
  * <span data-ttu-id="78af3-220">`--https-endpoint-destination-port` の名前を `--destination-port` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-220">Renamed  `--https-endpoint-destination-port` to `--destination-port`</span></span>
* <span data-ttu-id="78af3-221">[重大な変更] `application create` のパラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-221">[BREAKING CHANGE] Removed parameters for `application create`:</span></span>
  * `--https-endpoint-location`
  * `--https-endpoint-public-port`
  * `--ssh-endpoint-destination-port`
  * `--ssh-endpoint-location`
  * `--ssh-endpoint-public-port`
* <span data-ttu-id="78af3-222">[破壊的変更] `hdinsight resize`の `--target-instance-count` の名前を `--workernode-count` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-222">[BREAKING CHNAGE] Renamed `--target-instance-count` to `--workernode-count` for `hdinsight resize`</span></span>
* <span data-ttu-id="78af3-223">[重大な変更] `hdinsight script-action` グループのすべてのコマンドが、スクリプト アクションの名前として `--name` パラメーターを使用するように変更されました。</span><span class="sxs-lookup"><span data-stu-id="78af3-223">[BREAKING CHANGE] Changed all commands in the `hdinsight script-action` group to use the `--name` parameter as the name of the script action.</span></span>
* <span data-ttu-id="78af3-224">`--cluster-name` 引数がすべての `hdinsight script-action` コマンドに追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="78af3-224">Added `--cluster-name` argument to all `hdinsight script-action` commands to replace old `--name` functionality</span></span>
* <span data-ttu-id="78af3-225">[重大な変更] すべての `hdinsight script-action` コマンドで `--script-execution-id` の名前を `--execution-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-225">[BREAKING CHANGE] Renamed `--script-execution-id` to `--execution-id` for all `hdinsight script-action` commands</span></span>
* <span data-ttu-id="78af3-226">[重大な変更] 名前を `hdinsight script-action show` から `hdinsight script-action show-execution-details` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-226">[BREAKING CHANGE] Renamed `hdinsight script-action show` to `hdinsight script-action show-execution-details`</span></span>
* <span data-ttu-id="78af3-227">[破壊的変更] `hdinsight script-action execute --roles` に対するパラメーターを、コンマ区切りではなくスペース区切りにしました</span><span class="sxs-lookup"><span data-stu-id="78af3-227">[BREAKING CHNAGE] Changed parameters to `hdinsight script-action execute --roles` to be space-separated instead of comma-separated</span></span>
* <span data-ttu-id="78af3-228">[重大な変更] `hdinsight script-action list`の `--persisted` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-228">[BREAKING CHANGE] Removed the `--persisted` parameter of `hdinsight script-action list`</span></span>
* <span data-ttu-id="78af3-229">ローカル JSON ファイルへのパスまたは JSON 文字列を受け入れるように `hdinsight create --cluster-configurations` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-229">Changed the `hdinsight create --cluster-configurations` parameter to accept a path to a local JSON file or a JSON string</span></span>
* <span data-ttu-id="78af3-230">`hdinsight script-action list-execution-history` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-230">Added command `hdinsight script-action list-execution-history`</span></span>
* <span data-ttu-id="78af3-231">Log Analytics ワークスペース ID またはワークスペース名を受け入れるように `hdinsight monitor enable --workspace` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-231">Changed `hdinsight monitor enable --workspace` to accept a Log Analytics workspace ID or workspace name</span></span>
* <span data-ttu-id="78af3-232">`hdinsight monitor enable --primary-key` 引数を追加しました。これは、ワークスペース ID がパラメーターとして指定されている場合に必要です</span><span class="sxs-lookup"><span data-stu-id="78af3-232">Added the `hdinsight monitor enable --primary-key` argument, which is needed if a workspace ID is provided as the parameter</span></span>
* <span data-ttu-id="78af3-233">例をさらに追加し、ヘルプ メッセージの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-233">Added more examples and updated descriptions for help messages</span></span>

### <a name="interactive"></a><span data-ttu-id="78af3-234">Interactive</span><span class="sxs-lookup"><span data-stu-id="78af3-234">Interactive</span></span>

* <span data-ttu-id="78af3-235">読み込みエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-235">Fixed a loading error</span></span>

### <a name="kubernetes"></a><span data-ttu-id="78af3-236">Kubernetes</span><span class="sxs-lookup"><span data-stu-id="78af3-236">Kubernetes</span></span>

* <span data-ttu-id="78af3-237">ダッシュボードのコンテナー ポートで `https` が使用されている場合に `https` を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-237">Changed to use `https` if dashboard container port is using `https`</span></span>

### <a name="network"></a><span data-ttu-id="78af3-238">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-238">Network</span></span>

* <span data-ttu-id="78af3-239">`--yes` 引数を `network dns record-set cname delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-239">Added `--yes` argument `network dns record-set cname delete`</span></span>

### <a name="profile"></a><span data-ttu-id="78af3-240">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-240">Profile</span></span>

* <span data-ttu-id="78af3-241">リソースのアクセス トークンを取得するための `account get-access-token` に `--resource-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-241">Added `--resource-type` argument to `account get-access-token` to get resource access tokens</span></span>

### <a name="servicefabric"></a><span data-ttu-id="78af3-242">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="78af3-242">ServiceFabric</span></span>

* <span data-ttu-id="78af3-243">sf cluster create でサポートされているすべての OS バージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-243">Added all supported os version for sf cluster create</span></span>
* <span data-ttu-id="78af3-244">プライマリ証明書の検証のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-244">Fixed primary certificate validation bug</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-245">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-245">Storage</span></span>

* <span data-ttu-id="78af3-246">`storage copy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-246">Added command `storage copy`</span></span>

## <a name="july-30-2019"></a><span data-ttu-id="78af3-247">2019 年 7 月 30 日</span><span class="sxs-lookup"><span data-stu-id="78af3-247">July 30, 2019</span></span>

<span data-ttu-id="78af3-248">バージョン 2.0.70</span><span class="sxs-lookup"><span data-stu-id="78af3-248">Version 2.0.70</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-249">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-249">ACR</span></span>

* <span data-ttu-id="78af3-250">問題 #9952 (`acr pack build` コマンドでの回帰) を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-250">Fixed issue #9952 (a regression in the `acr pack build` command)</span></span>
* <span data-ttu-id="78af3-251">`acr pack build` の既定のビルダー イメージ名を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-251">Removed the default builder image name in `acr pack build`</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-252">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-252">Appservice</span></span>

* <span data-ttu-id="78af3-253">リソースが見つからない場合にメッセージ表示するように `webapp config ssl` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-253">Changed `webapp config ssl` to show a message if a resource is not found</span></span>
* <span data-ttu-id="78af3-254">`functionapp create` がストレージ アカウントの種類 `Standard_RAGRS` を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-254">Fixed issue where `functionapp create` does not accept `Standard_RAGRS` storage account type</span></span>
* <span data-ttu-id="78af3-255">古いバージョンの python を使用して `webapp up` を実行すると失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-255">Fixed an issue where `webapp up` would fail if run using older versions of python</span></span>

### <a name="network"></a><span data-ttu-id="78af3-256">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-256">Network</span></span>

* <span data-ttu-id="78af3-257">`network nic ip-config add` から無効なパラメーター `--ids` を削除しました (#9861 の修正)</span><span class="sxs-lookup"><span data-stu-id="78af3-257">Removed invalid parameter `--ids` from `network nic ip-config add` (fixes #9861)</span></span>
* <span data-ttu-id="78af3-258">#9604 を修正しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-258">Fixes #9604.</span></span> <span data-ttu-id="78af3-259">信頼されたルート証明書へのユーザーの関連付けをサポートするために、`network application-gateway http-settings [create|update]` に `--root-certs` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-259">Added `--root-certs` parameter to `network application-gateway http-settings [create|update]` to support user associate trusted root certificates.</span></span>
* <span data-ttu-id="78af3-260">`network dns record-set ns create` の引数 `--subscription` を修正しました (#9965)</span><span class="sxs-lookup"><span data-stu-id="78af3-260">Fixed arguent `--subscription` for `network dns record-set ns create` (#9965)</span></span>

### <a name="rbac"></a><span data-ttu-id="78af3-261">RBAC</span><span class="sxs-lookup"><span data-stu-id="78af3-261">RBAC</span></span>

* <span data-ttu-id="78af3-262">`user update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-262">Added `user update` command</span></span>
* <span data-ttu-id="78af3-263">[非推奨] ユーザー関連コマンドで `--upn-or-object-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-263">[DEPRECATED] Deprecated `--upn-or-object-id` from user-related commands</span></span>
    * <span data-ttu-id="78af3-264">代替引数の `--id` を使用してください</span><span class="sxs-lookup"><span data-stu-id="78af3-264">Use replacement argument `--id`</span></span>
* <span data-ttu-id="78af3-265">ユーザー関連コマンドに `--id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-265">Added `--id` argument to user-related commands</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-266">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-266">SQL</span></span>

* <span data-ttu-id="78af3-267">マネージド インスタンス キーおよび TDE 保護機能の管理コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-267">Added management commands for managed instance keys and TDE protector</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-268">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-268">Storage</span></span>

* <span data-ttu-id="78af3-269">`storage remove` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-269">Added `storage remove` command</span></span>
* <span data-ttu-id="78af3-270">`storage blob update` での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-270">Fixed an issue with `storage blob update`</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-271">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-271">VM</span></span>

* <span data-ttu-id="78af3-272">ゾーンの詳細を出力するための新しい API バージョンを使用するように `list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-272">Changed `list-skus` to use newer api-version to output zone details</span></span>
* <span data-ttu-id="78af3-273">`vmss create` の `--single-placement-group` の既定値を`false` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-273">Changed default of `--single-placement-group` to `false` for `vmss create`</span></span>
* <span data-ttu-id="78af3-274">`[snapshot|disk] create` において ZRS ストレージ SKU を選択する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-274">Added ability to select ZRS storage SKUs for `[snapshot|disk] create`</span></span>
* <span data-ttu-id="78af3-275">専用ホストをサポートするために、新しいコマンド グループ `vm host` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-275">Added new command group `vm host` to support dedicated hosts</span></span>
* <span data-ttu-id="78af3-276">VM 専用ホストを設定するためのパラメーター `--host` と `--host-group` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-276">Added parameters `--host` and `--host-group` on `vm create` to set VM dedicated host</span></span>

## <a name="july-16-2019"></a><span data-ttu-id="78af3-277">2019 年 7 月 16 日</span><span class="sxs-lookup"><span data-stu-id="78af3-277">July 16, 2019</span></span>

<span data-ttu-id="78af3-278">バージョン 2.0.69</span><span class="sxs-lookup"><span data-stu-id="78af3-278">Version 2.0.69</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-279">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-279">Appservice</span></span>

* <span data-ttu-id="78af3-280">ResourceGroupName または App の名前が無効な場合に適切なエラー メッセージを返すように `webapp identity` コマンドが変更されました</span><span class="sxs-lookup"><span data-stu-id="78af3-280">Changed `webapp identity` commands to return a proper error message if ResourceGroupName or App name are invalid</span></span>
* <span data-ttu-id="78af3-281">ResourceGroup が指定されなかった場合に numberOfSites の正しい値を返すように `webapp list` が修正されました</span><span class="sxs-lookup"><span data-stu-id="78af3-281">Fixed `webapp list` to return the correct value for numberOfSites if no ResourceGroup was provided</span></span>
* <span data-ttu-id="78af3-282">`appservice plan create` と `webapp create` の副作用が修正されました</span><span class="sxs-lookup"><span data-stu-id="78af3-282">Fixed side-effects of `appservice plan create` and `webapp create`</span></span>

### <a name="core"></a><span data-ttu-id="78af3-283">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-283">Core</span></span>

* <span data-ttu-id="78af3-284">`--subscription` が適用不可にもかかわらず表示される問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="78af3-284">Fixed issue where `--subscription` would appear despite being not applicable</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-285">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-285">Batch</span></span>

* <span data-ttu-id="78af3-286">[重大な変更] `batch pool node-agent-skus list` が `batch pool supported-images list` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="78af3-286">[BREAKING CHANGE] Replaced `batch pool node-agent-skus list` with `batch pool supported-images list`</span></span>
* <span data-ttu-id="78af3-287">`batch pool create network` の `--json-file` オプションを使用するときに、トラフィックのソース ポートに基づいてプールへのネットワーク アクセスをブロックするセキュリティ規則のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-287">Added support for security rules blocking network access to a pool based on the source port of the traffic when using the `--json-file` option of `batch pool create network`</span></span>
* <span data-ttu-id="78af3-288">`batch task create`の `--json-file` オプションを使用するときに、コンテナーの作業ディレクトリまたは Batch タスクの作業ディレクトリでタスクを実行するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-288">Added support for executing the task in the container working directory or in the Batch task working directory when using the `--json-file` option of `batch task create`</span></span>
* <span data-ttu-id="78af3-289">`batch pool create`の `--application-package-references` オプションが、既定値でのみ動作するというエラーが修正されました</span><span class="sxs-lookup"><span data-stu-id="78af3-289">Fixed error in `--application-package-references` option of `batch pool create` where it would only work with defaults</span></span>

### <a name="eventhubs"></a><span data-ttu-id="78af3-290">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="78af3-290">Eventhubs</span></span>

* <span data-ttu-id="78af3-291">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-291">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="rdbms"></a><span data-ttu-id="78af3-292">RDBMS</span><span class="sxs-lookup"><span data-stu-id="78af3-292">RDBMS</span></span>

* <span data-ttu-id="78af3-293">レプリカ作成コマンドでレプリカ SKU を指定するためのオプション パラメーターが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-293">Added optional parameter to specify replica SKU for create replica command</span></span>
* <span data-ttu-id="78af3-294">MySQL レプリカの作成で CI テストが失敗する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="78af3-294">Fixed the issue with CI test failure with creating MySQL replica</span></span>

### <a name="relay"></a><span data-ttu-id="78af3-295">リレー</span><span class="sxs-lookup"><span data-stu-id="78af3-295">Relay</span></span>

* <span data-ttu-id="78af3-296">クライアント承認が無効になっているときのハイブリッド接続の問題が修正されました ([#8775](https://github.com/azure/azure-cli/issues/8775))</span><span class="sxs-lookup"><span data-stu-id="78af3-296">Fixed issue with hybrid connection when client authroization disabled [#8775](https://github.com/azure/azure-cli/issues/8775)</span></span>
* <span data-ttu-id="78af3-297">パラメーター `--requires-transport-security` を `relay wcfrelay create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-297">Added parameter `--requires-transport-security` to `relay wcfrelay create`</span></span>

### <a name="servicebus"></a><span data-ttu-id="78af3-298">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="78af3-298">Servicebus</span></span>

* <span data-ttu-id="78af3-299">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-299">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-300">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-300">Storage</span></span>

* <span data-ttu-id="78af3-301">ストレージ アカウントの更新で Files AADDS を有効にします</span><span class="sxs-lookup"><span data-stu-id="78af3-301">Enable Files AADDS for storage account update</span></span>
* <span data-ttu-id="78af3-302">修正された問題 `storage blob service-properties update --set`</span><span class="sxs-lookup"><span data-stu-id="78af3-302">Fixed issue `storage blob service-properties update --set`</span></span>

## <a name="july-2-2019"></a><span data-ttu-id="78af3-303">2019 年 7 月 2 日</span><span class="sxs-lookup"><span data-stu-id="78af3-303">July 2, 2019</span></span>

<span data-ttu-id="78af3-304">バージョン 2.0.68</span><span class="sxs-lookup"><span data-stu-id="78af3-304">Version 2.0.68</span></span>

### <a name="core"></a><span data-ttu-id="78af3-305">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-305">Core</span></span>

* <span data-ttu-id="78af3-306">コマンド モジュールが再頒布可能な 1 つの Python コードに統合されました。</span><span class="sxs-lookup"><span data-stu-id="78af3-306">Command modules are now consolidated into a single Python distributable.</span></span> <span data-ttu-id="78af3-307">これにより、PyPI での多くの `azure-cli-` パッケージの直接使用が廃止されます。</span><span class="sxs-lookup"><span data-stu-id="78af3-307">This deprecates direct use of many `azure-cli-` packages on PyPI.</span></span>
  <span data-ttu-id="78af3-308">またこれにより、インストール サイズが削減され、`pip` 経由で直接インストールしたユーザーにのみ影響が出ます。</span><span class="sxs-lookup"><span data-stu-id="78af3-308">This should reduce install size and only affect users who have directly installed via `pip`.</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-309">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-309">ACR</span></span>

* <span data-ttu-id="78af3-310">タスクへのタイマー トリガーのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-310">Added support for Timer Triggers to Task</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-311">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-311">Appservice</span></span>

* <span data-ttu-id="78af3-312">既定でアプリケーション インサイトを有効にするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-312">Changed `functionapp create` to enable application insights by default</span></span>
* <span data-ttu-id="78af3-313">[重大な変更] 非推奨の `functionapp devops-build` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-313">[BREAKING CHANGE] Removed deprecated `functionapp devops-build` command.</span></span>
  *  <span data-ttu-id="78af3-314">代わりに新しいコマンド `az functionapp devops-pipeline` を使用</span><span class="sxs-lookup"><span data-stu-id="78af3-314">Use the new command `az functionapp devops-pipeline` instead</span></span>
* <span data-ttu-id="78af3-315">Linux 従量課金プランの関数アプリのプラン サポートを `functionapp deployment config-zip` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-315">Added Linux Consumption function app plan support to `functionapp deployment config-zip`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="78af3-316">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="78af3-316">Cosmos DB</span></span>

* <span data-ttu-id="78af3-317">ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-317">Added support for disabling TTL</span></span>

### <a name="dls"></a><span data-ttu-id="78af3-318">DLS</span><span class="sxs-lookup"><span data-stu-id="78af3-318">DLS</span></span>

* <span data-ttu-id="78af3-319">ADLS バージョンを更新しました (0.0.45)</span><span class="sxs-lookup"><span data-stu-id="78af3-319">Updated ADLS version (0.0.45)</span></span>

### <a name="feedback"></a><span data-ttu-id="78af3-320">フィードバック</span><span class="sxs-lookup"><span data-stu-id="78af3-320">Feedback</span></span>

* <span data-ttu-id="78af3-321">失敗した拡張機能コマンドを報告するときに、`az feedback` はインデックスからの拡張機能のプロジェクト/リポジトリの url にブラウザーを開こうとするようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-321">When reporting a failed extension command, `az feedback` now attempts to open the browser to the project/repo url of the extension from the index</span></span>

### <a name="hdinsight"></a><span data-ttu-id="78af3-322">HDInsight</span><span class="sxs-lookup"><span data-stu-id="78af3-322">HDInsight</span></span>

* <span data-ttu-id="78af3-323">[重大な変更] `oms` コマンド グループ名を `monitor` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-323">[BREAKING CHANGE] Changed `oms` command group name to `monitor`</span></span>
* <span data-ttu-id="78af3-324">[重大な変更] `--http-password/-p` が必須パラメーターになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-324">[BREAKING CHANGE] Made `--http-password/-p` a required parameter</span></span> 
* <span data-ttu-id="78af3-325">`--cluster-admin-account` および `cluster-users-group-dns` パラメーター入力候補の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-325">Added completers for `--cluster-admin-account` and `cluster-users-group-dns` parameters completer</span></span> 
* <span data-ttu-id="78af3-326">`cluster-users-group-dns` パラメーターを `—esp` が存在するときに必要となるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-326">Changed `cluster-users-group-dns` parameter to be required when `—esp` is present</span></span>
* <span data-ttu-id="78af3-327">既存の引数自動オートコンプリートすべてにタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-327">Added a timeout for all existing argument auto-completers</span></span>
* <span data-ttu-id="78af3-328">リソース名をリソース id に変換する際のタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-328">Added a timeout for transforming resource name to resource id</span></span>
* <span data-ttu-id="78af3-329">任意のリソース グループからリソースを選択するようにオートコンプリートを変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-329">Changed Auto-completers to select resources from any resource group.</span></span> <span data-ttu-id="78af3-330">`-g` で指定されるリソース グループとは別のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="78af3-330">It can be a different resource group than the one specified with `-g`</span></span>
* <span data-ttu-id="78af3-331">`hdinsight application create` コマンドで `--sub-domain-suffix` および `--disable_gateway_auth` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-331">Added support for `--sub-domain-suffix` and `--disable_gateway_auth` parameters in the `hdinsight application create` command</span></span>

### <a name="managed-services"></a><span data-ttu-id="78af3-332">マネージド サービス</span><span class="sxs-lookup"><span data-stu-id="78af3-332">Managed Services</span></span>

* <span data-ttu-id="78af3-333">プレビューにマネージド サービス コマンド モジュールを導入</span><span class="sxs-lookup"><span data-stu-id="78af3-333">Introducing managed service command module in preview</span></span>

### <a name="profile"></a><span data-ttu-id="78af3-334">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-334">Profile</span></span>
* <span data-ttu-id="78af3-335">ログアウト コマンドの `--subscription` 引数を抑制</span><span class="sxs-lookup"><span data-stu-id="78af3-335">Suppress `--subscription` argument for logout command</span></span>

### <a name="rbac"></a><span data-ttu-id="78af3-336">RBAC</span><span class="sxs-lookup"><span data-stu-id="78af3-336">RBAC</span></span>

* <span data-ttu-id="78af3-337">[重大な変更] `create-for-rbac` の `--password` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-337">[BREAKING CHANGE] Removed `--password` argument for `create-for-rbac`</span></span>
* <span data-ttu-id="78af3-338">AAD グラフ サーバー レプリケーションの待機時間によって発生する断続的なエラーを回避するために `--assignee-principal-type` パラメーターを `create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-338">Added `--assignee-principal-type` parameter to `create` command to avoid intermittent failures caused by AAD graph server replication latency</span></span>
* <span data-ttu-id="78af3-339">所有オブジェクトの一覧表示時の `ad signed-in-user` のクラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-339">Fixed a crash in `ad signed-in-user` when listing owned objects</span></span>
* <span data-ttu-id="78af3-340">`ad sp` によってサービス プリンシパルから適切なアプリケーションが検出されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-340">Fixed issue where `ad sp` would not find the right application from a service principal</span></span>

### <a name="rdbms"></a><span data-ttu-id="78af3-341">RDBMS</span><span class="sxs-lookup"><span data-stu-id="78af3-341">RDBMS</span></span>

* <span data-ttu-id="78af3-342">MariaDB のレプリケーション サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-342">Added support for replication for MariaDB</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-343">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-343">SQL</span></span>

* <span data-ttu-id="78af3-344">`sql db create --sample-name` に使用できる値を文書化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-344">Documented allowed values for `sql db create --sample-name`</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-345">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-345">Storage</span></span>

* <span data-ttu-id="78af3-346">`--as-user` を使用した `storage blob generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-346">Added user delegation SAS token support with `--as-user` to `storage blob generate-sas`</span></span> 
* <span data-ttu-id="78af3-347">`--as-user` を使用した `storage container generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-347">Added user delegation SAS token support with `--as-user` to `storage container generate-sas`</span></span> 

### <a name="vm"></a><span data-ttu-id="78af3-348">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-348">VM</span></span>

* <span data-ttu-id="78af3-349">`--no-wait` による実行時に `vmss create` によってエラー メッセージが返されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-349">Fixed bug where `vmss create` returns an error message when run with `--no-wait`</span></span>
* <span data-ttu-id="78af3-350">`vmss create --single-placement-group` のクライアント側の検証を削除しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-350">Removed client-side validation for `vmss create --single-placement-group`.</span></span> <span data-ttu-id="78af3-351">`--single-placement-group` が `true` に設定され、`--instance-count` が 100 より大きいか、可用性ゾーンが指定されていても失敗にはならず、この検証はコンピューティング サービスに任されます</span><span class="sxs-lookup"><span data-stu-id="78af3-351">Does not fail if `--single-placement-group` is set to `true` and`--instance-count` is greater than 100 or availability zones are specified, but leaves this validation to the compute service</span></span>
* <span data-ttu-id="78af3-352">`--latest` と共に使用したときに `[vm|vmss] extension image list` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-352">Fixed bug where `[vm|vmss] extension image list` fails when used with `--latest`</span></span>


## <a name="june-18-2019"></a><span data-ttu-id="78af3-353">2019 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="78af3-353">June 18, 2019</span></span>

<span data-ttu-id="78af3-354">バージョン 2.0.67</span><span class="sxs-lookup"><span data-stu-id="78af3-354">Version 2.0.67</span></span>

### <a name="core"></a><span data-ttu-id="78af3-355">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-355">Core</span></span>

<span data-ttu-id="78af3-356">このリリースでは、新しい [プレビュー] タグが導入され、コマンド グループ、コマンド、または引数がプレビュー状態である場合に、お客様により明確に通知できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="78af3-356">This release introduces a new [Preview] tag to more clearly communicate to customers when a command group, command or argument is in preview status.</span></span> <span data-ttu-id="78af3-357">以前は、これはヘルプ テキストで通知されていたか、コマンド モジュールのバージョン番号によって暗黙的に通知されていました。</span><span class="sxs-lookup"><span data-stu-id="78af3-357">This was previously called out in help text or communicated implicitly by the command module version number.</span></span>
<span data-ttu-id="78af3-358">CLI では、将来、個々のパッケージのバージョン番号が削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="78af3-358">The CLI will be removing version numbers for individual packages in the future.</span></span> <span data-ttu-id="78af3-359">コマンドがプレビュー状態の場合は、そのすべての引数もプレビュー状態です。</span><span class="sxs-lookup"><span data-stu-id="78af3-359">If a command is in preview, all of its arguments are as well.</span></span> <span data-ttu-id="78af3-360">コマンド グループにプレビュー状態のラベルが付いている場合、すべてのコマンドと引数もプレビュー状態と見なされます。</span><span class="sxs-lookup"><span data-stu-id="78af3-360">If a command group is labeled as being in preview, then all commands and arguments are considered to be in preview as well.</span></span>

<span data-ttu-id="78af3-361">この変更の結果、このリリースでは、一部のコマンド グループが "突然" プレビュー状態になったように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="78af3-361">As a result of this change, several command groups may seem to "suddenly" appear to be in a preview status with this release.</span></span> <span data-ttu-id="78af3-362">ほとんどのパッケージがプレビュー状態にあったのですが、このリリースでは一般提供と見なされていることがその真相です</span><span class="sxs-lookup"><span data-stu-id="78af3-362">What actually happened is that most packages were in a preview status, but are being deemed GA with this release</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-363">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-363">ACR</span></span>
* <span data-ttu-id="78af3-364">'acr check-health' コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-364">Added 'acr check-health' command</span></span>
* <span data-ttu-id="78af3-365">AAD トークンおよび外部コマンドの取得に関するエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-365">Improved error handling for AAD tokens and for retrieving external commands</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-366">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-366">ACS</span></span>
* <span data-ttu-id="78af3-367">非推奨の ACS コマンドがヘルプ ビューで非表示になりました</span><span class="sxs-lookup"><span data-stu-id="78af3-367">Deprecated ACS commands are now hidden from help view</span></span>

### <a name="ams"></a><span data-ttu-id="78af3-368">AMS</span><span class="sxs-lookup"><span data-stu-id="78af3-368">AMS</span></span>
* <span data-ttu-id="78af3-369">[重大な変更] archive-window-length および key-frame-interval-duration の ISO 8601 時間文字列を返すように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-369">[BREAKING CHANGE] Changed to return ISO 8601 time strings for archive-window-length and key-frame-interval-duration</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-370">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-370">AppService</span></span>
* <span data-ttu-id="78af3-371">`webapp deleted list` および `webapp deleted restore` に対してロケーション ベースのルーティングを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-371">Added location based routing for `webapp deleted list` and `webapp deleted restore`</span></span>
* <span data-ttu-id="78af3-372">Azure Cloud Shell で Web アプリのログに記録されたターゲット URL ("You can launch the app at...") がクリックできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-372">Fixed issue where webapp up logged target URL ("You can launch the app at...") was not clickable in Azure Cloud Shell</span></span>
* <span data-ttu-id="78af3-373">一部の SKU でのアプリ作成が AlwaysOn エラーで失敗するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-373">Fixed an issue where creating apps with the some SKUs was failing with an AlwaysOn error</span></span>
* <span data-ttu-id="78af3-374">`[appservice|webapp] create` に事前検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-374">Added pre-validation to `[appservice|webapp] create`</span></span>
* <span data-ttu-id="78af3-375">正しい actionHostName を使用するように `[webapp|functionapp] traffic-routing` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-375">Fixed `[webapp|functionapp] traffic-routing` to use the correct actionHostName</span></span>
* <span data-ttu-id="78af3-376">`functionapp` コマンドにスロット サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-376">Added slot support to `functionapp` commands</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-377">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-377">Batch</span></span>
* <span data-ttu-id="78af3-378">共有キー認証の過度のエラー報告による AAD 認証の回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-378">Fixed AAD auth regression caused by over-aggressive error reporting for Shared Key Auth</span></span>

### <a name="batchai"></a><span data-ttu-id="78af3-379">BatchAI</span><span class="sxs-lookup"><span data-stu-id="78af3-379">BatchAI</span></span>
* <span data-ttu-id="78af3-380">BatchAI コマンドが非推奨となり、非表示になりました</span><span class="sxs-lookup"><span data-stu-id="78af3-380">BatchAI commands are now deprecated and hidden</span></span>

### <a name="botservice"></a><span data-ttu-id="78af3-381">BotService</span><span class="sxs-lookup"><span data-stu-id="78af3-381">BotService</span></span>
* <span data-ttu-id="78af3-382">v3 SDK をサポートするコマンドに "廃止されたサポート"/"保守モード" 警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-382">Added "discontinued support"/"maintenance mode" warning messages for commands that support the v3 SDK</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="78af3-383">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="78af3-383">CosmosDB</span></span>
* <span data-ttu-id="78af3-384">[非推奨] `cosmosdb list-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-384">[DEPRECATED] Deprecated the `cosmosdb list-keys` command</span></span>
* <span data-ttu-id="78af3-385">`cosmosdb keys list` コマンドを追加しました。`cosmosdb list-keys` に置き換わるものです</span><span class="sxs-lookup"><span data-stu-id="78af3-385">Added the `cosmosdb keys list` command - replaces `cosmosdb list-keys`</span></span>
* <span data-ttu-id="78af3-386">`cosmsodb create/update`:"isZoneRedundant" プロパティを設定できるように --location の新しいフォーマットを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-386">`cosmsodb create/update`: Added new format for --location to allow setting "isZoneRedundant" property.</span></span> <span data-ttu-id="78af3-387">古いフォーマットを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-387">Deprecated old format</span></span>

### <a name="eventgrid"></a><span data-ttu-id="78af3-388">EventGrid</span><span class="sxs-lookup"><span data-stu-id="78af3-388">EventGrid</span></span>
* <span data-ttu-id="78af3-389">ドメイン CRUD 操作のための `eventgrid domain` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-389">Added `eventgrid domain` commands for domain CRUD operations</span></span>
* <span data-ttu-id="78af3-390">ドメイン トピック CRUD 操作のための `eventgrid domain topic` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-390">Added `eventgrid domain topic` commands for domain topics CRUD operations</span></span>
* <span data-ttu-id="78af3-391">OData 構文を使用して結果をフィルタリングするための `--odata-query` 引数を `eventgrid [topic|event-subscription] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-391">Added `--odata-query` argument to `eventgrid [topic|event-subscription] list` for filtering results using OData syntax</span></span>
* <span data-ttu-id="78af3-392">`event-subscription create/update`:`--endpoint-type` パラメーターの新しい値として servicebusqueue を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-392">`event-subscription create/update`: Added servicebusqueue as new values for the `--endpoint-type` parameter</span></span>
* <span data-ttu-id="78af3-393">[重大な変更] `eventgrid event-subscription [create|update]` での `--included-event-types All` のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-393">[BREAKING CHANGE] Removed support for `--included-event-types All` with `eventgrid event-subscription [create|update]`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="78af3-394">HDInsight</span><span class="sxs-lookup"><span data-stu-id="78af3-394">HDInsight</span></span>
* <span data-ttu-id="78af3-395">`hdinsight create` コマンドでの `--ssh-public-key` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-395">Added support for `--ssh-public-key` parameter in `hdinsight create` command</span></span>

### <a name="iot"></a><span data-ttu-id="78af3-396">IoT</span><span class="sxs-lookup"><span data-stu-id="78af3-396">IoT</span></span>
* <span data-ttu-id="78af3-397">承認ポリシー キーの再生成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-397">Added support to regenerate authorization policy keys</span></span>
* <span data-ttu-id="78af3-398">DigitalTwin リポジトリ プロビジョニング サービスの SDK およびサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-398">Added SDK and support for DigitalTwin Repository Provisioning Service</span></span>

### <a name="network"></a><span data-ttu-id="78af3-399">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-399">Network</span></span>
* <span data-ttu-id="78af3-400">Nat Gateway に対するゾーン サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-400">Added Zone support for Nat Gateway</span></span>
* <span data-ttu-id="78af3-401">`network list-service-tags` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-401">Added command `network list-service-tags`</span></span>
* <span data-ttu-id="78af3-402">ユーザーがワイルドカード A レコードをインポートできない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-402">Fixed issue with `dns zone import` where users could not import wildcard A records</span></span>
* <span data-ttu-id="78af3-403">特定のリージョンでフロー ロギングを有効にできない `watcher flow-log configure` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-403">Fixed issue with `watcher flow-log configure` where flow logging could not be enabled in certain regions</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-404">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-404">Resource</span></span>
* <span data-ttu-id="78af3-405">REST 呼び出しを行うための `az rest` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-405">Added `az rest` command for making REST calls</span></span>
* <span data-ttu-id="78af3-406">リソース グループまたはサブスクリプション レベル`--scope` で `policy assignment list` を使用する場合のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-406">Fixed error when using `policy assignment list` with a resource group or subscription level `--scope`</span></span>

### <a name="servicebus"></a><span data-ttu-id="78af3-407">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="78af3-407">ServiceBus</span></span>
* <span data-ttu-id="78af3-408">`servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319) での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-408">Fixed issue with `servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319)</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-409">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-409">SQL</span></span>
* <span data-ttu-id="78af3-410">`--location` を `sql [server|mi] create` のオプションに変更しました - 指定されていない場合、リソース グループの場所を使用します</span><span class="sxs-lookup"><span data-stu-id="78af3-410">Changed `--location` to be optional for `sql [server|mi] create` - uses resource group location if not specified</span></span>
* <span data-ttu-id="78af3-411">`sql db list-editions --available` の "'NoneType' object is not iterable" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-411">Fixed "'NoneType' object is not iterable" error for `sql db list-editions --available`</span></span>

### <a name="sqlvm"></a><span data-ttu-id="78af3-412">SQLVm</span><span class="sxs-lookup"><span data-stu-id="78af3-412">SQLVm</span></span>
* <span data-ttu-id="78af3-413">[破壊的変更] `--license-type` パラメーターを必要とするように `sql vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-413">[BREAKING CHNAGE] Changed `sql vm create` to require `--license-type` parameter</span></span>
* <span data-ttu-id="78af3-414">sql vm の作成または更新時に SQL イメージ SKU を設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-414">Changed to allow setting SQL image SKU when creating or updating a sql vm</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-415">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-415">Storage</span></span>
* <span data-ttu-id="78af3-416">`storage container generate-sas` のアカウント キーが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-416">Fixed issue with missing account key for `storage container generate-sas`</span></span>
* <span data-ttu-id="78af3-417">Linux での `storage blob sync` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-417">Fixed issue with `storage blob sync` on Linux</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-418">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-418">VM</span></span>
* <span data-ttu-id="78af3-419">[プレビュー] VM イメージを構築するための `vm image template` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-419">[PREVIEW] Added `vm image template` commands to build VM images</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="78af3-420">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="78af3-420">June 4, 2019</span></span>

<span data-ttu-id="78af3-421">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="78af3-421">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="78af3-422">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-422">Core</span></span>
* <span data-ttu-id="78af3-423">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-423">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-424">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-424">ACR</span></span>
* <span data-ttu-id="78af3-425">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-425">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-426">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-426">ACS</span></span>
* <span data-ttu-id="78af3-427">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-427">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="78af3-428">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="78af3-428">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-429">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-429">Batch</span></span>
* <span data-ttu-id="78af3-430">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-430">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="78af3-431">IoT</span><span class="sxs-lookup"><span data-stu-id="78af3-431">IoT</span></span>
* <span data-ttu-id="78af3-432">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-432">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="78af3-433">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-433">Network</span></span>
* <span data-ttu-id="78af3-434">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-434">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="78af3-435">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-435">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="78af3-436">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-436">Resource</span></span>
* <span data-ttu-id="78af3-437">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-437">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="78af3-438">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-438">Role</span></span>
* <span data-ttu-id="78af3-439">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-439">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="78af3-440">Compute</span><span class="sxs-lookup"><span data-stu-id="78af3-440">Compute</span></span>
* <span data-ttu-id="78af3-441">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-441">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="78af3-442">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="78af3-442">May 21, 2019</span></span>

<span data-ttu-id="78af3-443">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="78af3-443">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="78af3-444">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-444">Core</span></span>
* <span data-ttu-id="78af3-445">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-445">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="78af3-446">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-446">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="78af3-447">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-447">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-448">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-448">ACR</span></span>
* <span data-ttu-id="78af3-449">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-449">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-450">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-450">ACS</span></span>
* <span data-ttu-id="78af3-451">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-451">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-452">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-452">AppService</span></span>
* <span data-ttu-id="78af3-453">[非推奨] `functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="78af3-453">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="78af3-454">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-454">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="78af3-455">[重大な変更] `--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="78af3-455">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="78af3-456">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-456">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="78af3-457">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-457">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="78af3-458">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-458">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="78af3-459">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-459">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="78af3-460">BotService</span><span class="sxs-lookup"><span data-stu-id="78af3-460">BotService</span></span>
* <span data-ttu-id="78af3-461">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-461">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="78af3-462">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-462">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="78af3-463">消費</span><span class="sxs-lookup"><span data-stu-id="78af3-463">Consumption</span></span>
* <span data-ttu-id="78af3-464">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-464">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="78af3-465">IoT</span><span class="sxs-lookup"><span data-stu-id="78af3-465">IoT</span></span>
* <span data-ttu-id="78af3-466">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-466">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="78af3-467">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-467">Network</span></span>
* [重大な変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="78af3-469">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-469">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="78af3-470">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-470">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="78af3-471">RDBMS</span><span class="sxs-lookup"><span data-stu-id="78af3-471">RDBMS</span></span>
* <span data-ttu-id="78af3-472">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-472">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="78af3-473">RBAC</span><span class="sxs-lookup"><span data-stu-id="78af3-473">RBAC</span></span>
* <span data-ttu-id="78af3-474">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-474">Added support for mangement group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-475">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-475">Storage</span></span>
* <span data-ttu-id="78af3-476">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="78af3-476">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="78af3-477">Compute</span><span class="sxs-lookup"><span data-stu-id="78af3-477">Compute</span></span>
* <span data-ttu-id="78af3-478">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-478">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="78af3-479">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-479">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="78af3-480">__メモ__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="78af3-480">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="78af3-481">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-481">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="78af3-482">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="78af3-482">May 6, 2019</span></span>

<span data-ttu-id="78af3-483">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="78af3-483">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-484">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-484">ACS</span></span>
* <span data-ttu-id="78af3-485">[重大な変更] `--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-485">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="78af3-486">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-486">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="78af3-487">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-487">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="78af3-488">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-488">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-489">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-489">Appservice</span></span>
* <span data-ttu-id="78af3-490">[非推奨] `functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-490">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="78af3-491">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-491">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="78af3-492">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="78af3-492">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="78af3-493">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-493">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="78af3-494">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-494">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="78af3-495">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-495">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="78af3-496">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-496">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="78af3-497">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-497">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="78af3-498">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-498">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="78af3-499">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-499">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-500">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-500">Batch</span></span>
* <span data-ttu-id="78af3-501">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-501">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="78af3-502">Botservice</span><span class="sxs-lookup"><span data-stu-id="78af3-502">Botservice</span></span>
* <span data-ttu-id="78af3-503">[重大な変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="78af3-503">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="78af3-504">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-504">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="78af3-505">[重大な変更] `--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-505">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="78af3-506">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="78af3-506">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="78af3-507">[重大な変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-507">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="78af3-508">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="78af3-508">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="78af3-509">[重大な変更] `bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-509">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="78af3-510">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-510">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="78af3-511">[重大な変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-511">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="78af3-512">[重大な変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-512">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="78af3-513">[重大な変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-513">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="78af3-514">[重大な変更] `Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-514">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="78af3-515">[重大な変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-515">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="78af3-516">[重大な変更] `SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-516">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="78af3-517">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="78af3-517">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="78af3-518">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-518">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="78af3-519">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-519">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="78af3-520">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-520">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="78af3-521">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-521">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="78af3-522">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-522">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="78af3-523">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-523">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="78af3-524">構成</span><span class="sxs-lookup"><span data-stu-id="78af3-524">Configure</span></span>
* <span data-ttu-id="78af3-525">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-525">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="78af3-526">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="78af3-526">Eventhubs</span></span>
* <span data-ttu-id="78af3-527">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-527">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="78af3-528">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-528">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="78af3-529">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-529">Network</span></span>
* <span data-ttu-id="78af3-530">[重大な変更] `vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="78af3-530">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="78af3-531">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="78af3-531">Policy Insights</span></span>
* <span data-ttu-id="78af3-532">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-532">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="78af3-533">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-533">Role</span></span>
* <span data-ttu-id="78af3-534">[非推奨] `create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="78af3-534">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="78af3-535">Service Bus</span><span class="sxs-lookup"><span data-stu-id="78af3-535">Service Bus</span></span>
* <span data-ttu-id="78af3-536">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-536">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="78af3-537">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-537">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="78af3-538">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-538">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-539">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-539">SQL</span></span>
* <span data-ttu-id="78af3-540">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-540">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-541">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-541">VM</span></span>
* <span data-ttu-id="78af3-542">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-542">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="78af3-543">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-543">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="78af3-544">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-544">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="78af3-545">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-545">Added new `ppg` command group for manging Proximity Placement Groups</span></span>
* <span data-ttu-id="78af3-546">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-546">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="78af3-547">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-547">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="78af3-548">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="78af3-548">April 23, 2019</span></span>

<span data-ttu-id="78af3-549">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="78af3-549">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-550">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-550">ACS</span></span>
* <span data-ttu-id="78af3-551">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-551">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="78af3-552">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-552">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="78af3-553">AMS</span><span class="sxs-lookup"><span data-stu-id="78af3-553">AMS</span></span>
* <span data-ttu-id="78af3-554">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-554">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-555">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-555">AppService</span></span>
* <span data-ttu-id="78af3-556">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-556">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="78af3-557">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-557">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="78af3-558">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-558">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="78af3-559">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-559">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="78af3-560">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-560">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="78af3-561">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-561">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="78af3-562">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-562">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="78af3-563">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-563">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="78af3-564">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-564">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="78af3-565">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="78af3-565">Deployment Manager</span></span>
* <span data-ttu-id="78af3-566">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="78af3-566">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="78af3-567">ラボ</span><span class="sxs-lookup"><span data-stu-id="78af3-567">Lab</span></span>
* <span data-ttu-id="78af3-568">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-568">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="78af3-569">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-569">Network</span></span>
* <span data-ttu-id="78af3-570">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-570">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-571">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-571">Resource</span></span>
* <span data-ttu-id="78af3-572">[非推奨] `resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="78af3-572">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="78af3-573">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="78af3-573">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="78af3-574">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-574">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="78af3-575">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-575">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-576">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-576">SQL</span></span>
* <span data-ttu-id="78af3-577">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-577">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="78af3-578">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-578">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="78af3-579">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-579">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="78af3-580">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-580">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-581">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-581">Storage</span></span>
* <span data-ttu-id="78af3-582">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-582">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-583">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-583">VM</span></span>
* <span data-ttu-id="78af3-584">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-584">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="78af3-585">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-585">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="78af3-586">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-586">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="78af3-587">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="78af3-587">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="78af3-588">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-588">Core</span></span>
* <span data-ttu-id="78af3-589">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-589">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-590">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-590">ACR</span></span>
* <span data-ttu-id="78af3-591">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-591">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="78af3-592">AMS</span><span class="sxs-lookup"><span data-stu-id="78af3-592">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="78af3-595">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-595">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="78af3-596">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-596">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-597">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-597">AppService</span></span>
* <span data-ttu-id="78af3-598">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-598">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="78af3-599">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-599">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="78af3-600">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-600">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="78af3-601">[重大な変更] `devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="78af3-601">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="78af3-602">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-602">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="78af3-603">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-603">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="78af3-604">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-604">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="78af3-605">CDN</span><span class="sxs-lookup"><span data-stu-id="78af3-605">CDN</span></span>
* <span data-ttu-id="78af3-606">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-606">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="78af3-607">フィードバック</span><span class="sxs-lookup"><span data-stu-id="78af3-607">Feedback</span></span>
* <span data-ttu-id="78af3-608">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-608">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="78af3-609">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-609">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="78af3-610">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-610">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-611">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-611">Monitor</span></span>
* <span data-ttu-id="78af3-612">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-612">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="78af3-613">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-613">Network</span></span>
* <span data-ttu-id="78af3-614">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-614">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="78af3-615">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-615">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="78af3-616">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-616">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="78af3-617">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-617">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="78af3-618">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="78af3-618">PrivateDNS</span></span>
* <span data-ttu-id="78af3-619">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-619">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-620">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-620">Resource</span></span>
* <span data-ttu-id="78af3-621">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-621">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="78af3-622">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-622">Role</span></span>
* <span data-ttu-id="78af3-623">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-623">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="78af3-624">[重大な変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-624">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-625">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-625">SQL</span></span>
* <span data-ttu-id="78af3-626">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-626">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-627">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-627">Storage</span></span>
* <span data-ttu-id="78af3-628">[重大な変更] `storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-628">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="78af3-629">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-629">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="78af3-630">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-630">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="78af3-631">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-631">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="78af3-632">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="78af3-632">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="78af3-633">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-633">Core</span></span>
* <span data-ttu-id="78af3-634">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-634">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="78af3-635">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-635">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="78af3-636">クラウド</span><span class="sxs-lookup"><span data-stu-id="78af3-636">Cloud</span></span>
* <span data-ttu-id="78af3-637">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-637">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-638">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-638">ACR</span></span>
* <span data-ttu-id="78af3-639">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-639">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="78af3-640">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-640">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="78af3-641">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-641">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="78af3-642">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-642">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-643">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-643">AppService</span></span>
* <span data-ttu-id="78af3-644">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-644">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="78af3-645">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-645">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="78af3-646">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="78af3-646">BOT Service</span></span>
* <span data-ttu-id="78af3-647">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-647">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="78af3-648">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-648">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="78af3-649">[重大な変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-649">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="78af3-650">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-650">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="78af3-651">CDN</span><span class="sxs-lookup"><span data-stu-id="78af3-651">CDN</span></span>
* <span data-ttu-id="78af3-652">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-652">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [重大な変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="78af3-654">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="78af3-654">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="78af3-655">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-655">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="78af3-656">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="78af3-656">Cosmosdb</span></span>
* <span data-ttu-id="78af3-657">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-657">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="78af3-658">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-658">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="78af3-659">Interactive</span><span class="sxs-lookup"><span data-stu-id="78af3-659">Interactive</span></span>
* <span data-ttu-id="78af3-660">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-660">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-661">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-661">Monitor</span></span>
* <span data-ttu-id="78af3-662">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-662">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="78af3-663">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-663">Network</span></span>
* <span data-ttu-id="78af3-664">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-664">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="78af3-665">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-665">Profile</span></span>
* <span data-ttu-id="78af3-666">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-666">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="78af3-667">Postgres</span><span class="sxs-lookup"><span data-stu-id="78af3-667">Postgres</span></span> 
* <span data-ttu-id="78af3-668">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-668">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="78af3-669">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="78af3-669">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-670">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-670">Resource</span></span>
* <span data-ttu-id="78af3-671">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-671">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="78af3-672">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-672">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="78af3-673">Graph</span><span class="sxs-lookup"><span data-stu-id="78af3-673">Graph</span></span>
* <span data-ttu-id="78af3-674">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-674">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="78af3-675">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-675">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="78af3-676">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-676">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="78af3-677">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-677">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="78af3-678">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-678">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-679">storage</span><span class="sxs-lookup"><span data-stu-id="78af3-679">storage</span></span>
* <span data-ttu-id="78af3-680">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-680">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="78af3-681">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-681">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="78af3-682">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-682">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="78af3-683">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-683">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-684">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-684">VM</span></span>
* <span data-ttu-id="78af3-685">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-685">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="78af3-686">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="78af3-686">March 12, 2019</span></span>

<span data-ttu-id="78af3-687">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="78af3-687">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="78af3-688">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-688">Core</span></span>

* <span data-ttu-id="78af3-689">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-689">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-690">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-690">ACR</span></span>

* <span data-ttu-id="78af3-691">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-691">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-692">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-692">ACS</span></span>

* <span data-ttu-id="78af3-693">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-693">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="78af3-694">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-694">AppService</span></span>

* <span data-ttu-id="78af3-695">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-695">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="78af3-696">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-696">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="78af3-697">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-697">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="78af3-698">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-698">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="78af3-699">Botservice</span><span class="sxs-lookup"><span data-stu-id="78af3-699">Botservice</span></span>

* <span data-ttu-id="78af3-700">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-700">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="78af3-701">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-701">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="78af3-702">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-702">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="78af3-703">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-703">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="78af3-704">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-704">Container</span></span>

* <span data-ttu-id="78af3-705">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-705">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="78af3-706">EventHub</span><span class="sxs-lookup"><span data-stu-id="78af3-706">EventHub</span></span>

* <span data-ttu-id="78af3-707">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-707">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="78af3-708">Find</span><span class="sxs-lookup"><span data-stu-id="78af3-708">Find</span></span>

* <span data-ttu-id="78af3-709">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="78af3-709">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="78af3-710">HDInsight</span><span class="sxs-lookup"><span data-stu-id="78af3-710">HDInsight</span></span>

* <span data-ttu-id="78af3-711">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-711">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="78af3-712">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-712">Network</span></span>

* <span data-ttu-id="78af3-713">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-713">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="78af3-714">Rdbms</span><span class="sxs-lookup"><span data-stu-id="78af3-714">Rdbms</span></span>

* <span data-ttu-id="78af3-715">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="78af3-715">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="78af3-716">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-716">Role</span></span>

* <span data-ttu-id="78af3-717">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-717">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="78af3-718">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-718">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="78af3-719">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="78af3-719">Service Fabric</span></span>

* <span data-ttu-id="78af3-720">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-720">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="78af3-721">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="78af3-721">February 26, 2019</span></span>

<span data-ttu-id="78af3-722">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="78af3-722">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="78af3-723">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-723">Core</span></span>

* <span data-ttu-id="78af3-724">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-724">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-725">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-725">ACR</span></span>

* <span data-ttu-id="78af3-726">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-726">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="78af3-727">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-727">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-728">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-728">ACS</span></span>

* <span data-ttu-id="78af3-729">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-729">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-730">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-730">AppService</span></span>

* <span data-ttu-id="78af3-731">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-731">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-732">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-732">Batch</span></span>
* <span data-ttu-id="78af3-733">[重大な変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-733">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="78af3-734">[重大な変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-734">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="78af3-735">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-735">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="78af3-736">[重大な変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-736">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="78af3-737">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-737">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="78af3-738">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="78af3-738">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="78af3-739">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="78af3-739">CosmosDB</span></span>

* <span data-ttu-id="78af3-740">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-740">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="78af3-741">Kusto</span><span class="sxs-lookup"><span data-stu-id="78af3-741">Kusto</span></span>

* <span data-ttu-id="78af3-742">[重大な変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-742">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="78af3-743">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-743">Network</span></span>

* <span data-ttu-id="78af3-744">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-744">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="78af3-745">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-745">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="78af3-746">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-746">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="78af3-747">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-747">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="78af3-748">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-748">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="78af3-749">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-749">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="78af3-750">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-750">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-751">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-751">Resource</span></span>

* <span data-ttu-id="78af3-752">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-752">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="78af3-753">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-753">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="78af3-754">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-754">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="78af3-755">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-755">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="78af3-756">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-756">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="78af3-757">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-757">Role</span></span>

* <span data-ttu-id="78af3-758">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-758">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-759">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-759">VM</span></span>

* <span data-ttu-id="78af3-760">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-760">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="78af3-761">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="78af3-761">February 12, 2019</span></span>

<span data-ttu-id="78af3-762">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="78af3-762">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="78af3-763">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-763">Core</span></span>

* <span data-ttu-id="78af3-764">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-764">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="78af3-765">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-765">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-766">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-766">ACR</span></span>
* <span data-ttu-id="78af3-767">[重大な変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-767">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="78af3-768">[重大な変更] `acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-768">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-769">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-769">ACS</span></span>
* <span data-ttu-id="78af3-770">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-770">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="78af3-771">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-771">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="78af3-772">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-772">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="78af3-773">AMS</span><span class="sxs-lookup"><span data-stu-id="78af3-773">AMS</span></span>
* <span data-ttu-id="78af3-774">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-774">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="78af3-775">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-775">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-776">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-776">Appservice</span></span>
* <span data-ttu-id="78af3-777">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-777">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="78af3-778">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-778">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="78af3-779">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-779">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="78af3-780">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-780">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="78af3-781">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-781">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="78af3-782">Botservice</span><span class="sxs-lookup"><span data-stu-id="78af3-782">Botservice</span></span>
* <span data-ttu-id="78af3-783">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-783">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="78af3-784">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-784">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="78af3-785">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-785">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="78af3-786">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-786">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="78af3-787">[非推奨] `--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-787">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="78af3-788">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-788">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="78af3-789">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-789">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="78af3-790">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-790">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="78af3-791">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="78af3-791">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="78af3-792">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-792">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="78af3-793">Key Vault</span><span class="sxs-lookup"><span data-stu-id="78af3-793">Key Vault</span></span>
* <span data-ttu-id="78af3-794">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-794">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-795">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-795">Monitor</span></span>
* <span data-ttu-id="78af3-796">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-796">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="78af3-797">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-797">Network</span></span>
* <span data-ttu-id="78af3-798">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-798">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="78af3-799">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-799">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="78af3-800">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-800">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="78af3-801">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-801">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="78af3-802">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="78af3-802">Policy Insights</span></span>
* <span data-ttu-id="78af3-803">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-803">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="78af3-804">RDBMS</span><span class="sxs-lookup"><span data-stu-id="78af3-804">RDBMS</span></span>
* <span data-ttu-id="78af3-805">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-805">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="78af3-806">Redis</span><span class="sxs-lookup"><span data-stu-id="78af3-806">Redis</span></span>
* <span data-ttu-id="78af3-807">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-807">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="78af3-808">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-808">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="78af3-809">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-809">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="78af3-810">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-810">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="78af3-811">[重大な変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-811">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="78af3-812">[重大な変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="78af3-812">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="78af3-813">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-813">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="78af3-814">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-814">Role</span></span>
* <span data-ttu-id="78af3-815">[重大な変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="78af3-815">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="78af3-816">SQL VM</span><span class="sxs-lookup"><span data-stu-id="78af3-816">SQL VM</span></span>
* <span data-ttu-id="78af3-817">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-817">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-818">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-818">VM</span></span>
* <span data-ttu-id="78af3-819">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-819">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="78af3-820">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-820">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="78af3-821">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-821">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="78af3-822">[重大な変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="78af3-822">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="78af3-823">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="78af3-823">January 31, 2019</span></span>

<span data-ttu-id="78af3-824">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="78af3-824">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="78af3-825">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-825">Core</span></span>

* <span data-ttu-id="78af3-826">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="78af3-826">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="78af3-827">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="78af3-827">January 28, 2019</span></span>

<span data-ttu-id="78af3-828">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="78af3-828">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-829">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-829">ACR</span></span>
* <span data-ttu-id="78af3-830">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-830">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-831">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-831">ACS</span></span>
* <span data-ttu-id="78af3-832">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-832">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="78af3-833">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-833">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="78af3-834">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-834">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="78af3-835">AMS</span><span class="sxs-lookup"><span data-stu-id="78af3-835">AMS</span></span>
* <span data-ttu-id="78af3-836">[重大な変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-836">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="78af3-837">[重大な変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-837">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-838">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-838">Appservice</span></span>
* <span data-ttu-id="78af3-839">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-839">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="78af3-840">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-840">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="78af3-841">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-841">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="78af3-842">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-842">Container</span></span>
* <span data-ttu-id="78af3-843">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-843">Added `container start` command</span></span>
* <span data-ttu-id="78af3-844">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-844">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="78af3-845">EventGrid</span><span class="sxs-lookup"><span data-stu-id="78af3-845">EventGrid</span></span>
* <span data-ttu-id="78af3-846">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-846">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="78af3-847">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-847">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="78af3-848">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-848">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="78af3-849">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-849">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="78af3-850">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="78af3-850">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="78af3-851">HDInsight</span><span class="sxs-lookup"><span data-stu-id="78af3-851">HDInsight</span></span>
* <span data-ttu-id="78af3-852">[重大な変更] `hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-852">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="78af3-853">[重大な変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-853">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="78af3-854">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-854">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="78af3-855">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-855">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="78af3-856">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-856">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="78af3-857">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-857">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="78af3-858">IoT</span><span class="sxs-lookup"><span data-stu-id="78af3-858">IoT</span></span>
* <span data-ttu-id="78af3-859">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-859">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="78af3-860">Kusto</span><span class="sxs-lookup"><span data-stu-id="78af3-860">Kusto</span></span>
* <span data-ttu-id="78af3-861">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="78af3-861">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-862">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-862">Monitor</span></span>
* <span data-ttu-id="78af3-863">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-863">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="78af3-864">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-864">Profile</span></span>
* <span data-ttu-id="78af3-865">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-865">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="78af3-866">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-866">Network</span></span>
* <span data-ttu-id="78af3-867">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-867">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="78af3-868">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-868">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-869">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-869">Resource</span></span>
* <span data-ttu-id="78af3-870">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-870">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="78af3-871">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-871">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="78af3-872">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="78af3-872">SQL Virtual Machine</span></span>
* <span data-ttu-id="78af3-873">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="78af3-873">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-874">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-874">Storage</span></span>
* <span data-ttu-id="78af3-875">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-875">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="78af3-876">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="78af3-876">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-877">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-877">VM</span></span>
* <span data-ttu-id="78af3-878">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-878">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="78af3-879">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-879">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="78af3-880">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="78af3-880">January 15, 2019</span></span>

<span data-ttu-id="78af3-881">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="78af3-881">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-882">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-882">ACR</span></span>
* <span data-ttu-id="78af3-883">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-883">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="78af3-884">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-884">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="78af3-885">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-885">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="78af3-886">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-886">ACS</span></span>
* <span data-ttu-id="78af3-887">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-887">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-888">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-888">Appservice</span></span>
* <span data-ttu-id="78af3-889">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-889">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="78af3-890">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-890">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="78af3-891">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-891">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="78af3-892">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-892">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="78af3-893">Botservice</span><span class="sxs-lookup"><span data-stu-id="78af3-893">Botservice</span></span>
* <span data-ttu-id="78af3-894">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-894">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="78af3-895">構成</span><span class="sxs-lookup"><span data-stu-id="78af3-895">Configure</span></span>
* <span data-ttu-id="78af3-896">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-896">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="78af3-897">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="78af3-897">CosmosDB</span></span>
* <span data-ttu-id="78af3-898">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-898">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="78af3-899">HDInsight</span><span class="sxs-lookup"><span data-stu-id="78af3-899">HDInsight</span></span>
* <span data-ttu-id="78af3-900">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-900">Added commands for managing applications</span></span>
* <span data-ttu-id="78af3-901">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-901">Added commands for managing script actions</span></span>
* <span data-ttu-id="78af3-902">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-902">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="78af3-903">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-903">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="78af3-904">[重大な変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-904">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="78af3-905">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-905">Network</span></span>
* <span data-ttu-id="78af3-906">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-906">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="78af3-907">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-907">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="78af3-908">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-908">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="78af3-909">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-909">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="78af3-910">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-910">Role</span></span>
* <span data-ttu-id="78af3-911">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="78af3-911">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="78af3-912">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="78af3-912">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="78af3-913">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="78af3-913">Security</span></span>
* <span data-ttu-id="78af3-914">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="78af3-914">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-915">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-915">Storage</span></span>
* <span data-ttu-id="78af3-916">[重大な変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-916">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="78af3-917">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="78af3-917">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="78af3-918">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-918">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="78af3-919">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-919">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="78af3-920">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-920">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-921">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-921">VM</span></span>
* <span data-ttu-id="78af3-922">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-922">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="78af3-923">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-923">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="78af3-924">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-924">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="78af3-925">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-925">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="78af3-926">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-926">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="78af3-927">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-927">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="78af3-928">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="78af3-928">December 20, 2018</span></span>

<span data-ttu-id="78af3-929">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="78af3-929">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="78af3-930">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-930">Appservice</span></span>
* <span data-ttu-id="78af3-931">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-931">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="78af3-932">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-932">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="78af3-933">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-933">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="78af3-934">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="78af3-934">IoTCentral</span></span>
* <span data-ttu-id="78af3-935">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-935">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="78af3-936">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-936">Role</span></span>
* <span data-ttu-id="78af3-937">[重大な変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-937">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-938">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-938">SQL</span></span>
* <span data-ttu-id="78af3-939">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-939">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-940">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-940">VM</span></span>
* <span data-ttu-id="78af3-941">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-941">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="78af3-942">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="78af3-942">December 18, 2018</span></span>

<span data-ttu-id="78af3-943">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="78af3-943">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="78af3-944">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-944">ACR</span></span>
* <span data-ttu-id="78af3-945">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-945">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="78af3-946">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="78af3-946">Condensed the table layout for task list</span></span>
* <span data-ttu-id="78af3-947">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-947">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-948">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-948">ACS</span></span>
* <span data-ttu-id="78af3-949">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-949">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="78af3-950">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-950">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="78af3-951">[非推奨] `az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="78af3-951">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="78af3-952">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="78af3-952">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="78af3-953">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-953">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="78af3-954">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-954">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-955">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-955">Appservice</span></span>
* <span data-ttu-id="78af3-956">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-956">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="78af3-957">Botservice</span><span class="sxs-lookup"><span data-stu-id="78af3-957">Botservice</span></span>
* <span data-ttu-id="78af3-958">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-958">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="78af3-959">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-959">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="78af3-960">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-960">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="78af3-961">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="78af3-961">Reduced Kudu network calls</span></span>
* <span data-ttu-id="78af3-962">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-962">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="78af3-963">消費</span><span class="sxs-lookup"><span data-stu-id="78af3-963">Consumption</span></span>
* <span data-ttu-id="78af3-964">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-964">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="78af3-965">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="78af3-965">CosmosDB</span></span>
* <span data-ttu-id="78af3-966">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-966">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="78af3-967">マップ</span><span class="sxs-lookup"><span data-stu-id="78af3-967">Maps</span></span>
* <span data-ttu-id="78af3-968">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-968">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="78af3-969">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-969">Network</span></span>
* <span data-ttu-id="78af3-970">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-970">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="78af3-971">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-971">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-972">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-972">Resource</span></span>
* <span data-ttu-id="78af3-973">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-973">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="78af3-974">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-974">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-975">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-975">Storage</span></span>
*  <span data-ttu-id="78af3-976">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-976">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-977">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-977">VM</span></span>
* <span data-ttu-id="78af3-978">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-978">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="78af3-979">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="78af3-979">December 4, 2018</span></span>

<span data-ttu-id="78af3-980">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="78af3-980">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="78af3-981">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-981">Core</span></span>
* <span data-ttu-id="78af3-982">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-982">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="78af3-983">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-983">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-984">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-984">Appservice</span></span>
* <span data-ttu-id="78af3-985">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-985">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="78af3-986">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-986">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="78af3-987">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-987">Network</span></span>
* <span data-ttu-id="78af3-988">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-988">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="78af3-989">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-989">Role</span></span>
* <span data-ttu-id="78af3-990">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-990">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="78af3-991">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-991">VM</span></span>
* <span data-ttu-id="78af3-992">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-992">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="78af3-993">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-993">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="78af3-994">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-994">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="78af3-995">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-995">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="78af3-996">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="78af3-996">November 20, 2018</span></span>

<span data-ttu-id="78af3-997">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="78af3-997">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="78af3-998">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-998">Core</span></span>
* <span data-ttu-id="78af3-999">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-999">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1000">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1000">ACR</span></span>
* <span data-ttu-id="78af3-1001">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1001">Added context token to task step</span></span>
* <span data-ttu-id="78af3-1002">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1002">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="78af3-1003">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1003">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1004">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-1004">Appservice</span></span>
* <span data-ttu-id="78af3-1005">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1005">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="78af3-1006">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1006">Updated the default `node_version`.</span></span> <span data-ttu-id="78af3-1007">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="78af3-1007">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="78af3-1008">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1008">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="78af3-1009">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1009">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="78af3-1010">IotCentral</span><span class="sxs-lookup"><span data-stu-id="78af3-1010">IotCentral</span></span>
* <span data-ttu-id="78af3-1011">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1011">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="78af3-1012">KeyVault</span><span class="sxs-lookup"><span data-stu-id="78af3-1012">KeyVault</span></span>
* <span data-ttu-id="78af3-1013">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1013">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1014">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1014">Network</span></span>
* <span data-ttu-id="78af3-1015">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1015">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="78af3-1016">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1016">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="78af3-1017">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1017">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="78af3-1018">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1018">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="78af3-1019">Rdbms</span><span class="sxs-lookup"><span data-stu-id="78af3-1019">Rdbms</span></span>
* <span data-ttu-id="78af3-1020">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1020">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="78af3-1021">Rbac</span><span class="sxs-lookup"><span data-stu-id="78af3-1021">Rbac</span></span>
* <span data-ttu-id="78af3-1022">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1022">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="78af3-1023">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1023">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="78af3-1024">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1024">Storage</span></span>
* <span data-ttu-id="78af3-1025">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1025">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="78af3-1026">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1026">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="78af3-1027">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1027">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="78af3-1028">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="78af3-1028">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1029">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1029">VM</span></span>
* <span data-ttu-id="78af3-1030">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1030">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="78af3-1031">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1031">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="78af3-1032">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="78af3-1032">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="78af3-1033">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1033">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="78af3-1034">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1034">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="78af3-1035">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1035">Added `snapshot wait` command</span></span>
* <span data-ttu-id="78af3-1036">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1036">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="78af3-1037">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1037">November 6, 2018</span></span>

<span data-ttu-id="78af3-1038">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="78af3-1038">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1039">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1039">Core</span></span>
* <span data-ttu-id="78af3-1040">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1040">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1041">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1041">ACR</span></span>
* <span data-ttu-id="78af3-1042">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1042">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="78af3-1043">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1043">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1044">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1044">ACS</span></span>
* <span data-ttu-id="78af3-1045">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1045">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="78af3-1046">Advisor</span><span class="sxs-lookup"><span data-stu-id="78af3-1046">Advisor</span></span>
* <span data-ttu-id="78af3-1047">GA リリース</span><span class="sxs-lookup"><span data-stu-id="78af3-1047">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="78af3-1048">AMS</span><span class="sxs-lookup"><span data-stu-id="78af3-1048">AMS</span></span>
* <span data-ttu-id="78af3-1049">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1049">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="78af3-1050">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1050">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="78af3-1051">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1051">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="78af3-1052">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-1052">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="78af3-1053">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1053">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="78af3-1054">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1054">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="78af3-1055">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1055">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="78af3-1056">[重大な変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="78af3-1056">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="78af3-1057">[重大な変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1057">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="78af3-1058">[重大な変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1058">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="78af3-1059">[重大な変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="78af3-1059">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="78af3-1060">[重大な変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1060">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="78af3-1061">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="78af3-1061">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="78af3-1062">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="78af3-1062">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="78af3-1063">[重大な変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1063">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="78af3-1064">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1064">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="78af3-1065">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="78af3-1065">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1066">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-1066">AppService</span></span>
* <span data-ttu-id="78af3-1067">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1067">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="78af3-1068">構成</span><span class="sxs-lookup"><span data-stu-id="78af3-1068">Configure</span></span>
* <span data-ttu-id="78af3-1069">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1069">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="78af3-1070">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-1070">Container</span></span>
* <span data-ttu-id="78af3-1071">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1071">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="78af3-1072">EventHub</span><span class="sxs-lookup"><span data-stu-id="78af3-1072">EventHub</span></span>
* <span data-ttu-id="78af3-1073">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1073">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="78af3-1074">Interactive</span><span class="sxs-lookup"><span data-stu-id="78af3-1074">Interactive</span></span>
* <span data-ttu-id="78af3-1075">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="78af3-1075">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-1076">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-1076">Monitor</span></span>
* <span data-ttu-id="78af3-1077">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-1077">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1078">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1078">Network</span></span>
* <span data-ttu-id="78af3-1079">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1079">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="78af3-1080">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1080">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="78af3-1081">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1081">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="78af3-1082">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-1082">Profile</span></span>
* <span data-ttu-id="78af3-1083">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1083">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="78af3-1084">RDBMS</span><span class="sxs-lookup"><span data-stu-id="78af3-1084">RDBMS</span></span>
* <span data-ttu-id="78af3-1085">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1085">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-1086">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-1086">Resource</span></span>
* <span data-ttu-id="78af3-1087">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1087">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="78af3-1088">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-1088">Role</span></span>
* <span data-ttu-id="78af3-1089">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-1089">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="78af3-1090">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1090">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="78af3-1091">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1091">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-1092">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1092">Storage</span></span>
* <span data-ttu-id="78af3-1093">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="78af3-1093">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1094">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1094">VM</span></span>
* <span data-ttu-id="78af3-1095">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1095">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="78af3-1096">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1096">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="78af3-1097">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1097">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="78af3-1098">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1098">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="78af3-1099">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="78af3-1099">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="78af3-1100">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1100">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="78af3-1101">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1101">October 23, 2018</span></span>

<span data-ttu-id="78af3-1102">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="78af3-1102">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1103">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1103">Core</span></span>
* <span data-ttu-id="78af3-1104">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1104">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="78af3-1105">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1105">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1106">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1106">ACR</span></span>
* <span data-ttu-id="78af3-1107">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1107">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="78af3-1108">CDN</span><span class="sxs-lookup"><span data-stu-id="78af3-1108">CDN</span></span>
* <span data-ttu-id="78af3-1109">[重大な変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1109">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="78af3-1110">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-1110">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="78af3-1111">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-1111">Container</span></span>
* <span data-ttu-id="78af3-1112">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1112">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="78af3-1113">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1113">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="78af3-1114">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1114">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="78af3-1115">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1115">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="78af3-1116">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1116">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="78af3-1117">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1117">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="78af3-1118">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1118">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="78af3-1119">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="78af3-1119">CosmosDB</span></span>
* <span data-ttu-id="78af3-1120">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1120">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="78af3-1121">Interactive</span><span class="sxs-lookup"><span data-stu-id="78af3-1121">Interactive</span></span>
* <span data-ttu-id="78af3-1122">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1122">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="78af3-1123">IoT Central</span><span class="sxs-lookup"><span data-stu-id="78af3-1123">IoT Central</span></span>
* <span data-ttu-id="78af3-1124">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1124">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="78af3-1125">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="78af3-1125">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-1126">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-1126">Monitor</span></span>
* <span data-ttu-id="78af3-1127">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="78af3-1127">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="78af3-1128">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1128">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="78af3-1129">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1129">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="78af3-1130">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1130">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="78af3-1131">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1131">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="78af3-1132">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1132">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="78af3-1133">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="78af3-1133">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="78af3-1134">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1134">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="78af3-1135">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1135">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="78af3-1136">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1136">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1137">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1137">Network</span></span>
* <span data-ttu-id="78af3-1138">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1138">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="78af3-1139">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1139">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="78af3-1140">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="78af3-1140">ServiceBus</span></span>
* <span data-ttu-id="78af3-1141">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1141">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-1142">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-1142">SQL</span></span>
* <span data-ttu-id="78af3-1143">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1143">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-1144">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1144">Storage</span></span>
* <span data-ttu-id="78af3-1145">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1145">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="78af3-1146">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1146">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1147">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1147">VM</span></span>
* <span data-ttu-id="78af3-1148">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="78af3-1148">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="78af3-1149">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1149">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="78af3-1150">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1150">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="78af3-1151">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1151">October 16, 2018</span></span>

<span data-ttu-id="78af3-1152">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="78af3-1152">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1153">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1153">VM</span></span>
* <span data-ttu-id="78af3-1154">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1154">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="78af3-1155">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1155">October 9, 2018</span></span>

<span data-ttu-id="78af3-1156">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="78af3-1156">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1157">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1157">Core</span></span>
* <span data-ttu-id="78af3-1158">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1158">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1159">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1159">ACR</span></span>
* <span data-ttu-id="78af3-1160">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1160">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1161">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1161">ACS</span></span>
* <span data-ttu-id="78af3-1162">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="78af3-1162">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="78af3-1163">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1163">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="78af3-1164">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1164">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="78af3-1165">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1165">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="78af3-1166">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-1166">Container</span></span>
* <span data-ttu-id="78af3-1167">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1167">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="78af3-1168">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1168">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="78af3-1169">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="78af3-1169">Event Hub</span></span>
* <span data-ttu-id="78af3-1170">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1170">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="78af3-1171">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1171">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="78af3-1172">Extensions</span><span class="sxs-lookup"><span data-stu-id="78af3-1172">Extensions</span></span>
* <span data-ttu-id="78af3-1173">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1173">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="78af3-1174">HDInsight</span><span class="sxs-lookup"><span data-stu-id="78af3-1174">HDInsight</span></span>
* <span data-ttu-id="78af3-1175">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="78af3-1175">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="78af3-1176">IoT</span><span class="sxs-lookup"><span data-stu-id="78af3-1176">IoT</span></span>
* <span data-ttu-id="78af3-1177">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1177">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="78af3-1178">KeyVault</span><span class="sxs-lookup"><span data-stu-id="78af3-1178">KeyVault</span></span>
* <span data-ttu-id="78af3-1179">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1179">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1180">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1180">Network</span></span>
* <span data-ttu-id="78af3-1181">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="78af3-1181">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="78af3-1182">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="78af3-1182">See #6052</span></span>
* <span data-ttu-id="78af3-1183">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1183">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="78af3-1184">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="78af3-1184">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="78af3-1185">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1185">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="78af3-1186">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1186">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="78af3-1187">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1187">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="78af3-1188">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1188">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="78af3-1189">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-1189">Role</span></span>
* <span data-ttu-id="78af3-1190">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1190">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="78af3-1191">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1191">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="78af3-1192">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1192">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="78af3-1193">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1193">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="78af3-1194">Service Bus</span><span class="sxs-lookup"><span data-stu-id="78af3-1194">Service Bus</span></span>
* <span data-ttu-id="78af3-1195">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1195">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1196">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1196">VM</span></span>
* <span data-ttu-id="78af3-1197">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1197">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="78af3-1198">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1198">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="78af3-1199">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1199">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="78af3-1200">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1200">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="78af3-1201">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1201">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="78af3-1202">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1202">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="78af3-1203">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1203">September 21, 2018</span></span>

<span data-ttu-id="78af3-1204">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="78af3-1204">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1205">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1205">ACR</span></span>
* <span data-ttu-id="78af3-1206">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1206">Added ACR Task commands</span></span>
* <span data-ttu-id="78af3-1207">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1207">Added quick run command</span></span>
* <span data-ttu-id="78af3-1208">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1208">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="78af3-1209">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1209">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="78af3-1210">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1210">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="78af3-1211">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1211">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1212">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1212">ACS</span></span>
* <span data-ttu-id="78af3-1213">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1213">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="78af3-1214">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1214">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1215">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-1215">AppService</span></span>

* <span data-ttu-id="78af3-1216">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1216">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="78af3-1217">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1217">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="78af3-1218">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1218">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="78af3-1219">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1219">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-1220">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-1220">Batch</span></span>
* <span data-ttu-id="78af3-1221">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1221">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="78af3-1222">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1222">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="78af3-1223">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1223">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="78af3-1224">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1224">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="78af3-1225">Batch AI</span><span class="sxs-lookup"><span data-stu-id="78af3-1225">Batch AI</span></span> 
* <span data-ttu-id="78af3-1226">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1226">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="78af3-1227">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="78af3-1227">Cognitive Services</span></span>
* <span data-ttu-id="78af3-1228">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1228">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="78af3-1229">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1229">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="78af3-1230">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1230">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="78af3-1231">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1231">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="78af3-1232">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1232">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="78af3-1233">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1233">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="78af3-1234">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-1234">Container</span></span>
* <span data-ttu-id="78af3-1235">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1235">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="78af3-1236">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1236">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="78af3-1237">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1237">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="78af3-1238">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1238">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="78af3-1239">DataLake</span><span class="sxs-lookup"><span data-stu-id="78af3-1239">Datalake</span></span>
* <span data-ttu-id="78af3-1240">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1240">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="78af3-1241">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="78af3-1241">Interactive Shell</span></span>
* <span data-ttu-id="78af3-1242">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1242">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="78af3-1243">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1243">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="78af3-1244">IoT</span><span class="sxs-lookup"><span data-stu-id="78af3-1244">IoT</span></span>
* <span data-ttu-id="78af3-1245">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1245">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="78af3-1246">Key Vault</span><span class="sxs-lookup"><span data-stu-id="78af3-1246">Key Vault</span></span>
* <span data-ttu-id="78af3-1247">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1247">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1248">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1248">Network</span></span>
* <span data-ttu-id="78af3-1249">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1249">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="78af3-1250">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1250">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="78af3-1251">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1251">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="78af3-1252">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1252">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="78af3-1253">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1253">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="78af3-1254">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1254">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="78af3-1255">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1255">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="78af3-1256">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-1256">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="78af3-1257">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1257">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="78af3-1258">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1258">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="78af3-1259">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1259">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="78af3-1260">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1260">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="78af3-1261">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1261">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="78af3-1262">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="78af3-1262">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="78af3-1263">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1263">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="78af3-1264">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1264">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="78af3-1265">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1265">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="78af3-1266">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1266">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="78af3-1267">RDBMS</span><span class="sxs-lookup"><span data-stu-id="78af3-1267">RDBMS</span></span>
* <span data-ttu-id="78af3-1268">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1268">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="78af3-1269">予約</span><span class="sxs-lookup"><span data-stu-id="78af3-1269">Reservation</span></span>
* <span data-ttu-id="78af3-1270">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1270">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="78af3-1271">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1271">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="78af3-1272">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="78af3-1272">Manage App</span></span>
* <span data-ttu-id="78af3-1273">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1273">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="78af3-1274">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1274">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="78af3-1275">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-1275">Role</span></span>
* <span data-ttu-id="78af3-1276">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1276">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="78af3-1277">SignalR</span><span class="sxs-lookup"><span data-stu-id="78af3-1277">SignalR</span></span>
* <span data-ttu-id="78af3-1278">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="78af3-1278">First release</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-1279">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1279">Storage</span></span>
* <span data-ttu-id="78af3-1280">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1280">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="78af3-1281">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1281">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1282">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1282">VM</span></span>
* <span data-ttu-id="78af3-1283">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="78af3-1283">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="78af3-1284">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1284">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="78af3-1285">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1285">August 28, 2018</span></span>

<span data-ttu-id="78af3-1286">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="78af3-1286">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1287">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1287">Core</span></span>

* <span data-ttu-id="78af3-1288">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1288">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="78af3-1289">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1289">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1290">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1290">ACR</span></span>

* <span data-ttu-id="78af3-1291">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1291">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="78af3-1292">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1292">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1293">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1293">ACS</span></span>

* <span data-ttu-id="78af3-1294">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1294">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="78af3-1295">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1295">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1296">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-1296">AppService</span></span>

* <span data-ttu-id="78af3-1297">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1297">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="78af3-1298">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1298">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="78af3-1299">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1299">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="78af3-1300">バックアップ</span><span class="sxs-lookup"><span data-stu-id="78af3-1300">Backup</span></span>

* <span data-ttu-id="78af3-1301">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1301">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="78af3-1302">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="78af3-1302">Bot Service</span></span>

* <span data-ttu-id="78af3-1303">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="78af3-1303">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="78af3-1304">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="78af3-1304">Cognitive Services</span></span>

* <span data-ttu-id="78af3-1305">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1305">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="78af3-1306">IoT</span><span class="sxs-lookup"><span data-stu-id="78af3-1306">IoT</span></span>

* <span data-ttu-id="78af3-1307">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1307">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-1308">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-1308">Monitor</span></span>

* <span data-ttu-id="78af3-1309">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1309">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="78af3-1310">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1310">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1311">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1311">Network</span></span>

* <span data-ttu-id="78af3-1312">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1312">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-1313">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-1313">Resource</span></span>

* <span data-ttu-id="78af3-1314">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1314">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-1315">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1315">Storage</span></span>

* <span data-ttu-id="78af3-1316">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1316">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1317">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1317">VM</span></span>

* <span data-ttu-id="78af3-1318">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1318">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="78af3-1319">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1319">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="78af3-1320">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1320">Auguest 14, 2018</span></span>

<span data-ttu-id="78af3-1321">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="78af3-1321">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1322">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1322">Core</span></span>

* <span data-ttu-id="78af3-1323">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1323">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="78af3-1324">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1324">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="78af3-1325">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="78af3-1325">Telemetry</span></span>

* <span data-ttu-id="78af3-1326">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1326">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1327">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1327">ACR</span></span>

* <span data-ttu-id="78af3-1328">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1328">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="78af3-1329">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1329">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1330">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1330">ACS</span></span>

* <span data-ttu-id="78af3-1331">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1331">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="78af3-1332">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1332">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="78af3-1333">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1333">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="78af3-1334">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1334">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="78af3-1335">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1335">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="78af3-1336">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-1336">AppService</span></span>

* <span data-ttu-id="78af3-1337">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1337">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="78af3-1338">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1338">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="78af3-1339">BatchAI</span><span class="sxs-lookup"><span data-stu-id="78af3-1339">BatchAI</span></span>

* <span data-ttu-id="78af3-1340">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1340">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="78af3-1341">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-1341">Container</span></span>

* <span data-ttu-id="78af3-1342">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1342">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="78af3-1343">IoT</span><span class="sxs-lookup"><span data-stu-id="78af3-1343">IoT</span></span>

* <span data-ttu-id="78af3-1344">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1344">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="78af3-1345">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1345">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="78af3-1346">Iot Central</span><span class="sxs-lookup"><span data-stu-id="78af3-1346">Iot Central</span></span>

* <span data-ttu-id="78af3-1347">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="78af3-1347">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="78af3-1348">KeyVault</span><span class="sxs-lookup"><span data-stu-id="78af3-1348">KeyVault</span></span>


* <span data-ttu-id="78af3-1349">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1349">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="78af3-1350">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1350">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="78af3-1351">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1351">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="78af3-1352">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1352">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="78af3-1353">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1353">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="78af3-1354">リレー</span><span class="sxs-lookup"><span data-stu-id="78af3-1354">Relay</span></span>

* <span data-ttu-id="78af3-1355">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="78af3-1355">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-1356">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-1356">Sql</span></span>

* <span data-ttu-id="78af3-1357">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1357">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-1358">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1358">Storage</span></span>

* <span data-ttu-id="78af3-1359">[重大な変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="78af3-1359">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="78af3-1360">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1360">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="78af3-1361">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1361">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="78af3-1362">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1362">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="78af3-1363">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1363">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1364">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1364">VM</span></span>

* <span data-ttu-id="78af3-1365">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1365">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="78af3-1366">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="78af3-1366">July 31, 2018</span></span>

<span data-ttu-id="78af3-1367">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="78af3-1367">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1368">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1368">ACR</span></span>

* <span data-ttu-id="78af3-1369">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1369">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="78af3-1370">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1370">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1371">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1371">ACS</span></span>

* <span data-ttu-id="78af3-1372">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1372">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-1373">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-1373">Batch</span></span>

* <span data-ttu-id="78af3-1374">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1374">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="78af3-1375">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-1375">Container</span></span>

* <span data-ttu-id="78af3-1376">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1376">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1377">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1377">Network</span></span>

* <span data-ttu-id="78af3-1378">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1378">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="78af3-1379">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-1379">Resource</span></span>

* <span data-ttu-id="78af3-1380">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1380">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="78af3-1381">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1381">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="78af3-1382">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-1382">Role</span></span>

* <span data-ttu-id="78af3-1383">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1383">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="78af3-1384">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1384">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="78af3-1385">Search</span><span class="sxs-lookup"><span data-stu-id="78af3-1385">Search</span></span>

* <span data-ttu-id="78af3-1386">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1386">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="78af3-1387">Service Bus</span><span class="sxs-lookup"><span data-stu-id="78af3-1387">Service Bus</span></span>

* <span data-ttu-id="78af3-1388">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1388">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="78af3-1389">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1389">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="78af3-1390">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="78af3-1390">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="78af3-1391">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="78af3-1391">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-1392">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1392">Storage</span></span>

* <span data-ttu-id="78af3-1393">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-1393">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="78af3-1394">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1394">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1395">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1395">VM</span></span>

* <span data-ttu-id="78af3-1396">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-1396">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="78af3-1397">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1397">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="78af3-1398">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1398">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="78af3-1399">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1399">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="78af3-1400">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1400">July 18, 2018</span></span>

<span data-ttu-id="78af3-1401">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="78af3-1401">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1402">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1402">Core</span></span>

* <span data-ttu-id="78af3-1403">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1403">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="78af3-1404">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1404">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="78af3-1405">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1405">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1406">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1406">ACR</span></span>

* <span data-ttu-id="78af3-1407">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1407">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="78af3-1408">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1408">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="78af3-1409">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1409">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="78af3-1410">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1410">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1411">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1411">ACS</span></span>

* <span data-ttu-id="78af3-1412">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1412">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1413">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-1413">AppService</span></span>

* <span data-ttu-id="78af3-1414">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1414">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-1415">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-1415">Batch</span></span>

* <span data-ttu-id="78af3-1416">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1416">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="78af3-1417">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1417">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="78af3-1418">Batch AI</span><span class="sxs-lookup"><span data-stu-id="78af3-1418">Batch AI</span></span>

* <span data-ttu-id="78af3-1419">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1419">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="78af3-1420">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-1420">Container</span></span>

* <span data-ttu-id="78af3-1421">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1421">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="78af3-1422">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1422">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1423">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1423">Network</span></span>

* <span data-ttu-id="78af3-1424">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1424">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="78af3-1425">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1425">Added `network nic wait`</span></span>
* <span data-ttu-id="78af3-1426">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1426">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="78af3-1427">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1427">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="78af3-1428">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-1428">Resource</span></span>

* <span data-ttu-id="78af3-1429">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1429">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="78af3-1430">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1430">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="78af3-1431">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1431">Added `deployment wait` command</span></span>
* <span data-ttu-id="78af3-1432">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1432">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-1433">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-1433">SQL</span></span>

* <span data-ttu-id="78af3-1434">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1434">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="78af3-1435">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-1435">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="78af3-1436">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1436">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-1437">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1437">Storage</span></span>

* <span data-ttu-id="78af3-1438">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1438">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1439">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1439">VM</span></span>

* <span data-ttu-id="78af3-1440">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1440">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="78af3-1441">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1441">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="78af3-1442">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1442">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="78af3-1443">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1443">July 3, 2018</span></span>

<span data-ttu-id="78af3-1444">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="78af3-1444">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="78af3-1445">AKS</span><span class="sxs-lookup"><span data-stu-id="78af3-1445">AKS</span></span>

* <span data-ttu-id="78af3-1446">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1446">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="78af3-1447">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1447">July 3, 2018</span></span>

<span data-ttu-id="78af3-1448">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="78af3-1448">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1449">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1449">Core</span></span>

* <span data-ttu-id="78af3-1450">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1450">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1451">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1451">ACR</span></span>

* <span data-ttu-id="78af3-1452">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1452">Added polling build status</span></span>
* <span data-ttu-id="78af3-1453">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1453">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="78af3-1454">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1454">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1455">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1455">ACS</span></span>

* <span data-ttu-id="78af3-1456">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1456">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="78af3-1457">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1457">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="78af3-1458">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1458">Updated options for `aks browse` command.</span></span> <span data-ttu-id="78af3-1459">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1459">Added `--listen-port` support</span></span>
* <span data-ttu-id="78af3-1460">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1460">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="78af3-1461">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="78af3-1461">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="78af3-1462">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1462">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1463">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-1463">AppService</span></span>

* <span data-ttu-id="78af3-1464">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-1464">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="78af3-1465">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1465">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="78af3-1466">バックアップ</span><span class="sxs-lookup"><span data-stu-id="78af3-1466">Backup</span></span>

* <span data-ttu-id="78af3-1467">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1467">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="78af3-1468">BatchAI</span><span class="sxs-lookup"><span data-stu-id="78af3-1468">BatchAI</span></span>

* <span data-ttu-id="78af3-1469">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1469">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="78af3-1470">クラウド</span><span class="sxs-lookup"><span data-stu-id="78af3-1470">Cloud</span></span>

* <span data-ttu-id="78af3-1471">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1471">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="78af3-1472">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-1472">Container</span></span>

* <span data-ttu-id="78af3-1473">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1473">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="78af3-1474">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1474">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="78af3-1475">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1475">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="78af3-1476">拡張機能</span><span class="sxs-lookup"><span data-stu-id="78af3-1476">Extension</span></span>

* <span data-ttu-id="78af3-1477">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1477">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1478">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1478">Network</span></span>

* <span data-ttu-id="78af3-1479">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1479">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="78af3-1480">Rdbms</span><span class="sxs-lookup"><span data-stu-id="78af3-1480">Rdbms</span></span>

* <span data-ttu-id="78af3-1481">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1481">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-1482">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-1482">Resource</span></span>

* <span data-ttu-id="78af3-1483">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1483">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1484">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1484">VM</span></span>

* <span data-ttu-id="78af3-1485">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-1485">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="78af3-1486">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1486">June 25, 2018</span></span>

<span data-ttu-id="78af3-1487">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="78af3-1487">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="78af3-1488">CLI</span><span class="sxs-lookup"><span data-stu-id="78af3-1488">CLI</span></span>

* <span data-ttu-id="78af3-1489">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1489">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="78af3-1490">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1490">June 19, 2018</span></span>

<span data-ttu-id="78af3-1491">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="78af3-1491">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1492">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1492">Core</span></span>

* <span data-ttu-id="78af3-1493">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1493">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1494">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1494">ACR</span></span>

* <span data-ttu-id="78af3-1495">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1495">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="78af3-1496">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1496">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1497">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1497">ACS</span></span>

* <span data-ttu-id="78af3-1498">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1498">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="78af3-1499">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1499">Added `--update` support</span></span>
* <span data-ttu-id="78af3-1500">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1500">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="78af3-1501">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1501">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="78af3-1502">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1502">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="78af3-1503">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1503">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="78af3-1504">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1504">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="78af3-1505">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1505">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1506">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-1506">AppService</span></span>

* <span data-ttu-id="78af3-1507">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1507">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="78af3-1508">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1508">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-1509">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-1509">Batch</span></span>

* <span data-ttu-id="78af3-1510">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1510">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="78af3-1511">Batch AI</span><span class="sxs-lookup"><span data-stu-id="78af3-1511">Batch AI</span></span>

* <span data-ttu-id="78af3-1512">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1512">Added support for workspaces.</span></span> <span data-ttu-id="78af3-1513">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="78af3-1513">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="78af3-1514">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1514">Added support for experiments.</span></span> <span data-ttu-id="78af3-1515">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="78af3-1515">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="78af3-1516">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1516">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="78af3-1517">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1517">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="78af3-1518">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="78af3-1518">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="78af3-1519">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1519">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="78af3-1520">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="78af3-1520">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="78af3-1521">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="78af3-1521">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="78af3-1522">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1522">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="78af3-1523">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="78af3-1523">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="78af3-1524">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1524">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="78af3-1525">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="78af3-1525">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="78af3-1526">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1526">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="78af3-1527">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="78af3-1527">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="78af3-1528">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1528">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="78af3-1529">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1529">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="78af3-1530">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1530">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="78af3-1531">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1531">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="78af3-1532">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1532">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="78af3-1533">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1533">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="78af3-1534">マップ</span><span class="sxs-lookup"><span data-stu-id="78af3-1534">Maps</span></span>

* <span data-ttu-id="78af3-1535">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1535">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1536">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1536">Network</span></span>

* <span data-ttu-id="78af3-1537">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="78af3-1537">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="78af3-1538">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1538">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="78af3-1539">#6502</span><span class="sxs-lookup"><span data-stu-id="78af3-1539">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="78af3-1540">Reservations</span><span class="sxs-lookup"><span data-stu-id="78af3-1540">Reservations</span></span>

* <span data-ttu-id="78af3-1541">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1541">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="78af3-1542">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1542">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="78af3-1543">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1543">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="78af3-1544">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1544">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="78af3-1545">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1545">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="78af3-1546">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1546">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="78af3-1547">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-1547">Role</span></span>

* <span data-ttu-id="78af3-1548">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1548">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-1549">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-1549">SQL</span></span>

* <span data-ttu-id="78af3-1550">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1550">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-1551">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1551">Storage</span></span>

* <span data-ttu-id="78af3-1552">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1552">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1553">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1553">VM</span></span>

* <span data-ttu-id="78af3-1554">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1554">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="78af3-1555">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1555">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="78af3-1556">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1556">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="78af3-1557">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1557">June 13, 2018</span></span>

<span data-ttu-id="78af3-1558">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="78af3-1558">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1559">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1559">Core</span></span>

* <span data-ttu-id="78af3-1560">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1560">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="78af3-1561">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1561">June 13, 2018</span></span>

<span data-ttu-id="78af3-1562">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="78af3-1562">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="78af3-1563">AKS</span><span class="sxs-lookup"><span data-stu-id="78af3-1563">AKS</span></span>

* <span data-ttu-id="78af3-1564">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1564">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="78af3-1565">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1565">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="78af3-1566">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1566">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="78af3-1567">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1567">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="78af3-1568">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1568">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1569">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-1569">AppService</span></span>

* <span data-ttu-id="78af3-1570">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1570">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="78af3-1571">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1571">June 5, 2018</span></span>

<span data-ttu-id="78af3-1572">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="78af3-1572">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="78af3-1573">Interactive</span><span class="sxs-lookup"><span data-stu-id="78af3-1573">Interactive</span></span>

* <span data-ttu-id="78af3-1574">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1574">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="78af3-1575">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1575">June 5, 2018</span></span>

<span data-ttu-id="78af3-1576">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="78af3-1576">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1577">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1577">Core</span></span>

* <span data-ttu-id="78af3-1578">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1578">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="78af3-1579">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1579">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1580">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1580">ACR</span></span>

* <span data-ttu-id="78af3-1581">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1581">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="78af3-1582">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1582">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="78af3-1583">AKS</span><span class="sxs-lookup"><span data-stu-id="78af3-1583">AKS</span></span>

* <span data-ttu-id="78af3-1584">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1584">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-1585">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-1585">Batch</span></span>

* <span data-ttu-id="78af3-1586">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1586">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="78af3-1587">IoT</span><span class="sxs-lookup"><span data-stu-id="78af3-1587">IOT</span></span>

* <span data-ttu-id="78af3-1588">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1588">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1589">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1589">Network</span></span>

* <span data-ttu-id="78af3-1590">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1590">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="78af3-1591">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="78af3-1591">Policy Insights</span></span>

* <span data-ttu-id="78af3-1592">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="78af3-1592">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="78af3-1593">ARM</span><span class="sxs-lookup"><span data-stu-id="78af3-1593">ARM</span></span>

* <span data-ttu-id="78af3-1594">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1594">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-1595">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-1595">SQL</span></span>

* <span data-ttu-id="78af3-1596">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1596">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="78af3-1597">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1597">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="78af3-1598">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1598">Storage</span></span>

* <span data-ttu-id="78af3-1599">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1599">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1600">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1600">VM</span></span>

* <span data-ttu-id="78af3-1601">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1601">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="78af3-1602">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1602">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="78af3-1603">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1603">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="78af3-1604">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1604">May 22, 2018</span></span>

<span data-ttu-id="78af3-1605">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="78af3-1605">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1606">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1606">Core</span></span>

* <span data-ttu-id="78af3-1607">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1607">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1608">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1608">ACS</span></span>

* <span data-ttu-id="78af3-1609">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1609">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="78af3-1610">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1610">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1611">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-1611">AppService</span></span>

* <span data-ttu-id="78af3-1612">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1612">Improved generic update commands</span></span>
* <span data-ttu-id="78af3-1613">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1613">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="78af3-1614">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-1614">Container</span></span>

* <span data-ttu-id="78af3-1615">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1615">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="78af3-1616">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1616">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="78af3-1617">拡張機能</span><span class="sxs-lookup"><span data-stu-id="78af3-1617">Extension</span></span>

* <span data-ttu-id="78af3-1618">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1618">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="78af3-1619">Interactive</span><span class="sxs-lookup"><span data-stu-id="78af3-1619">Interactive</span></span>

* <span data-ttu-id="78af3-1620">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1620">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="78af3-1621">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1621">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="78af3-1622">KeyVault</span><span class="sxs-lookup"><span data-stu-id="78af3-1622">KeyVault</span></span>

* <span data-ttu-id="78af3-1623">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1623">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1624">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1624">Network</span></span>

* <span data-ttu-id="78af3-1625">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1625">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="78af3-1626">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1626">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-1627">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-1627">SQL</span></span>

* <span data-ttu-id="78af3-1628">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1628">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="78af3-1629">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1629">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="78af3-1630">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1630">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="78af3-1631">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1631">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="78af3-1632">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1632">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="78af3-1633">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="78af3-1633">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="78af3-1634">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="78af3-1634">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="78af3-1635">`edition`</span><span class="sxs-lookup"><span data-stu-id="78af3-1635">`edition`.</span></span> <span data-ttu-id="78af3-1636">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="78af3-1636">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="78af3-1637">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="78af3-1637">`elasticPoolName`.</span></span> <span data-ttu-id="78af3-1638">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="78af3-1638">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="78af3-1639">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1639">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="78af3-1640">`edition`</span><span class="sxs-lookup"><span data-stu-id="78af3-1640">`edition`.</span></span> <span data-ttu-id="78af3-1641">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="78af3-1641">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="78af3-1642">`dtu`</span><span class="sxs-lookup"><span data-stu-id="78af3-1642">`dtu`.</span></span> <span data-ttu-id="78af3-1643">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="78af3-1643">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="78af3-1644">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="78af3-1644">`databaseDtuMin`.</span></span> <span data-ttu-id="78af3-1645">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="78af3-1645">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="78af3-1646">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="78af3-1646">`databaseDtuMax`.</span></span> <span data-ttu-id="78af3-1647">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="78af3-1647">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="78af3-1648">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1648">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="78af3-1649">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1649">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-1650">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1650">Storage</span></span>

* <span data-ttu-id="78af3-1651">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1651">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="78af3-1652">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1652">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1653">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1653">VM</span></span>

* <span data-ttu-id="78af3-1654">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1654">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="78af3-1655">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="78af3-1655">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="78af3-1656">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1656">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="78af3-1657">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1657">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="78af3-1658">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1658">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="78af3-1659">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1659">May 7, 2018</span></span>

<span data-ttu-id="78af3-1660">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="78af3-1660">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1661">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1661">Core</span></span>

* <span data-ttu-id="78af3-1662">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1662">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="78af3-1663">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1663">Added limited support for positional arguments</span></span>
* <span data-ttu-id="78af3-1664">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1664">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="78af3-1665">#5591</span><span class="sxs-lookup"><span data-stu-id="78af3-1665">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="78af3-1666">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1666">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="78af3-1667">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="78af3-1667">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="78af3-1668">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1668">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="78af3-1669">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1669">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="78af3-1670">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1670">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1671">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1671">ACR</span></span>

* <span data-ttu-id="78af3-1672">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1672">Added ACR Build commands</span></span>
* <span data-ttu-id="78af3-1673">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1673">Improved resource not found error messages</span></span>
* <span data-ttu-id="78af3-1674">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1674">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="78af3-1675">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1675">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="78af3-1676">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1676">Improved repository commands error messages</span></span>
* <span data-ttu-id="78af3-1677">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1677">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1678">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1678">ACS</span></span>

* <span data-ttu-id="78af3-1679">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1679">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="78af3-1680">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1680">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="78af3-1681">AMS</span><span class="sxs-lookup"><span data-stu-id="78af3-1681">AMS</span></span>

* <span data-ttu-id="78af3-1682">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="78af3-1682">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1683">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-1683">Appservice</span></span>

* <span data-ttu-id="78af3-1684">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1684">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="78af3-1685">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1685">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="78af3-1686">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1686">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="78af3-1687">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1687">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="78af3-1688">Batch AI</span><span class="sxs-lookup"><span data-stu-id="78af3-1688">Batch AI</span></span>

* <span data-ttu-id="78af3-1689">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1689">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="78af3-1690">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="78af3-1690">Cognitive Services</span></span>

* <span data-ttu-id="78af3-1691">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1691">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="78af3-1692">消費</span><span class="sxs-lookup"><span data-stu-id="78af3-1692">Consumption</span></span>

* <span data-ttu-id="78af3-1693">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1693">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="78af3-1694">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-1694">Container</span></span>

* <span data-ttu-id="78af3-1695">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1695">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="78af3-1696">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="78af3-1696">Cosmos DB</span></span>

* <span data-ttu-id="78af3-1697">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1697">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="78af3-1698">DMS</span><span class="sxs-lookup"><span data-stu-id="78af3-1698">DMS</span></span>

* <span data-ttu-id="78af3-1699">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1699">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="78af3-1700">拡張機能</span><span class="sxs-lookup"><span data-stu-id="78af3-1700">Extension</span></span>

* <span data-ttu-id="78af3-1701">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1701">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="78af3-1702">Interactive</span><span class="sxs-lookup"><span data-stu-id="78af3-1702">Interactive</span></span>

* <span data-ttu-id="78af3-1703">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-1703">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="78af3-1704">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1704">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="78af3-1705">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1705">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="78af3-1706">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1706">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="78af3-1707">ラボ</span><span class="sxs-lookup"><span data-stu-id="78af3-1707">Lab</span></span>

* <span data-ttu-id="78af3-1708">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1708">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1709">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1709">Network</span></span>

* <span data-ttu-id="78af3-1710">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1710">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="78af3-1711">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-1711">Profile</span></span>

* <span data-ttu-id="78af3-1712">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1712">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="78af3-1713">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1713">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="78af3-1714">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1714">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="78af3-1715">Redis</span><span class="sxs-lookup"><span data-stu-id="78af3-1715">Redis</span></span>

* <span data-ttu-id="78af3-1716">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1716">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="78af3-1717">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1717">Deprecated `redis list-all`.</span></span> <span data-ttu-id="78af3-1718">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="78af3-1718">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="78af3-1719">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1719">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="78af3-1720">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1720">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="78af3-1721">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-1721">Role</span></span>

* <span data-ttu-id="78af3-1722">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1722">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-1723">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1723">Storage</span></span>

* <span data-ttu-id="78af3-1724">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="78af3-1724">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="78af3-1725">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1725">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="78af3-1726">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="78af3-1726">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="78af3-1727">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="78af3-1727">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="78af3-1728">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1728">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1729">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1729">VM</span></span>

* <span data-ttu-id="78af3-1730">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1730">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="78af3-1731">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1731">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="78af3-1732">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="78af3-1732">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="78af3-1733">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1733">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="78af3-1734">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1734">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="78af3-1735">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1735">Added write accelerator support</span></span>
* <span data-ttu-id="78af3-1736">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1736">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="78af3-1737">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1737">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="78af3-1738">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1738">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="78af3-1739">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1739">April 10, 2018</span></span>

<span data-ttu-id="78af3-1740">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="78af3-1740">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1741">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1741">ACR</span></span>

* <span data-ttu-id="78af3-1742">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1742">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1743">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1743">ACS</span></span>

* <span data-ttu-id="78af3-1744">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1744">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1745">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-1745">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="78af3-1747">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1747">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="78af3-1748">BatchAI</span><span class="sxs-lookup"><span data-stu-id="78af3-1748">BatchAI</span></span>

* <span data-ttu-id="78af3-1749">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1749">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="78af3-1750">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="78af3-1750">Job level mounting</span></span>
  - <span data-ttu-id="78af3-1751">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="78af3-1751">Environment variables with secret values</span></span>
  - <span data-ttu-id="78af3-1752">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="78af3-1752">Performance counters settings</span></span>
  - <span data-ttu-id="78af3-1753">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="78af3-1753">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="78af3-1754">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="78af3-1754">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="78af3-1755">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="78af3-1755">Usage and limits reporting</span></span>
  - <span data-ttu-id="78af3-1756">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="78af3-1756">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="78af3-1757">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="78af3-1757">Support for custom images</span></span>
  - <span data-ttu-id="78af3-1758">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1758">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="78af3-1759">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-1759">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="78af3-1760">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="78af3-1760">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="78af3-1761">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="78af3-1761">National clouds are supported</span></span>
* <span data-ttu-id="78af3-1762">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1762">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="78af3-1763">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1763">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="78af3-1764">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1764">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="78af3-1765">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1765">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="78af3-1766">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="78af3-1766">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="78af3-1767">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="78af3-1767">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="78af3-1768">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1768">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="78af3-1769">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1769">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="78af3-1770">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="78af3-1770">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="78af3-1771">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1771">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="78af3-1772">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1772">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="78af3-1773">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1773">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="78af3-1774">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1774">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="78af3-1775">課金</span><span class="sxs-lookup"><span data-stu-id="78af3-1775">Billing</span></span>

* <span data-ttu-id="78af3-1776">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1776">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="78af3-1777">消費</span><span class="sxs-lookup"><span data-stu-id="78af3-1777">Consumption</span></span>

* <span data-ttu-id="78af3-1778">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1778">Added `marketplace` commands</span></span>
* <span data-ttu-id="78af3-1779">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1779">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="78af3-1780">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1780">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="78af3-1781">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1781">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="78af3-1782">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1782">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="78af3-1783">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1783">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="78af3-1784">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-1784">Container</span></span>

* <span data-ttu-id="78af3-1785">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1785">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="78af3-1786">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1786">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="78af3-1787">拡張機能</span><span class="sxs-lookup"><span data-stu-id="78af3-1787">Extension</span></span>

* <span data-ttu-id="78af3-1788">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1788">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="78af3-1789">Interactive</span><span class="sxs-lookup"><span data-stu-id="78af3-1789">Interactive</span></span>

* <span data-ttu-id="78af3-1790">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1790">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="78af3-1791">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1791">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="78af3-1792">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1792">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1793">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1793">Network</span></span>

* <span data-ttu-id="78af3-1794">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1794">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="78af3-1795">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1795">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="78af3-1796">#4910</span><span class="sxs-lookup"><span data-stu-id="78af3-1796">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="78af3-1797">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1797">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="78af3-1798">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="78af3-1798">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="78af3-1799">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1799">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="78af3-1800">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1800">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="78af3-1801">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1801">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="78af3-1802">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-1802">Profile</span></span>

* <span data-ttu-id="78af3-1803">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1803">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="78af3-1804">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1804">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="78af3-1805">RDBMS</span><span class="sxs-lookup"><span data-stu-id="78af3-1805">RDBMS</span></span>

* <span data-ttu-id="78af3-1806">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1806">Added `georestore` command</span></span>
* <span data-ttu-id="78af3-1807">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1807">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-1808">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-1808">Resource</span></span>

* <span data-ttu-id="78af3-1809">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1809">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="78af3-1810">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1810">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-1811">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-1811">SQL</span></span>

* <span data-ttu-id="78af3-1812">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1812">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-1813">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1813">Storage</span></span>

* <span data-ttu-id="78af3-1814">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1814">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1815">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1815">VM</span></span>

* <span data-ttu-id="78af3-1816">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1816">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="78af3-1817">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1817">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="78af3-1819">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1819">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="78af3-1820">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1820">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="78af3-1821">#5718</span><span class="sxs-lookup"><span data-stu-id="78af3-1821">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="78af3-1822">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1822">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="78af3-1823">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1823">March 27, 2018</span></span>

<span data-ttu-id="78af3-1824">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="78af3-1824">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1825">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1825">Core</span></span>

* <span data-ttu-id="78af3-1826">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="78af3-1826">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1827">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1827">ACS</span></span>

* <span data-ttu-id="78af3-1828">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1828">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1829">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-1829">Appservice</span></span>

* <span data-ttu-id="78af3-1830">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1830">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="78af3-1831">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1831">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="78af3-1832">バックアップ</span><span class="sxs-lookup"><span data-stu-id="78af3-1832">Backup</span></span>

* <span data-ttu-id="78af3-1833">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1833">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="78af3-1834">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="78af3-1834">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="78af3-1835">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1835">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="78af3-1836">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1836">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="78af3-1837">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-1837">Container</span></span>

* <span data-ttu-id="78af3-1838">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1838">Added `container exec` command.</span></span> <span data-ttu-id="78af3-1839">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="78af3-1839">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="78af3-1840">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="78af3-1840">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="78af3-1841">拡張機能</span><span class="sxs-lookup"><span data-stu-id="78af3-1841">Extension</span></span>

* <span data-ttu-id="78af3-1842">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1842">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="78af3-1843">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1843">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="78af3-1844">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1844">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="78af3-1845">Interactive</span><span class="sxs-lookup"><span data-stu-id="78af3-1845">Interactive</span></span>

* <span data-ttu-id="78af3-1846">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1846">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="78af3-1847">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1847">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="78af3-1848">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="78af3-1848">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="78af3-1849">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1849">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="78af3-1850">ラボ</span><span class="sxs-lookup"><span data-stu-id="78af3-1850">Lab</span></span>

* <span data-ttu-id="78af3-1851">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1851">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-1852">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-1852">Monitor</span></span>

* <span data-ttu-id="78af3-1853">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="78af3-1853">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="78af3-1854">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="78af3-1854">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="78af3-1855">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="78af3-1855">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1856">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1856">Network</span></span>

* <span data-ttu-id="78af3-1857">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1857">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="78af3-1858">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-1858">Profile</span></span>

* <span data-ttu-id="78af3-1859">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1859">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="78af3-1860">RDBMS</span><span class="sxs-lookup"><span data-stu-id="78af3-1860">RDBMS</span></span>

* <span data-ttu-id="78af3-1861">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1861">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-1862">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-1862">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="78af3-1864">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-1864">Role</span></span>

* <span data-ttu-id="78af3-1865">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1865">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="78af3-1866">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1866">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="78af3-1867">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1867">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="78af3-1868">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1868">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="78af3-1869">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1869">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-1870">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1870">Storage</span></span>

* <span data-ttu-id="78af3-1871">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1871">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="78af3-1872">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="78af3-1872">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1873">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1873">VM</span></span>

* <span data-ttu-id="78af3-1874">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1874">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="78af3-1875">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1875">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="78af3-1876">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1876">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="78af3-1877">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1877">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="78af3-1878">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1878">March 13, 2018</span></span>

<span data-ttu-id="78af3-1879">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="78af3-1879">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-1880">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-1880">ACR</span></span>

* <span data-ttu-id="78af3-1881">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1881">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="78af3-1882">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1882">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="78af3-1883">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1883">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1884">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1884">ACS</span></span>

* <span data-ttu-id="78af3-1885">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1885">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="78af3-1886">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1886">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="78af3-1887">Advisor</span><span class="sxs-lookup"><span data-stu-id="78af3-1887">Advisor</span></span>

* <span data-ttu-id="78af3-1888">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1888">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="78af3-1889">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1889">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="78af3-1890">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1890">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="78af3-1891">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1891">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="78af3-1892">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1892">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1893">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-1893">Appservice</span></span>

* <span data-ttu-id="78af3-1894">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1894">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="78af3-1895">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1895">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="78af3-1896">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="78af3-1896">Eventhubs</span></span>

* <span data-ttu-id="78af3-1897">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="78af3-1897">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="78af3-1898">拡張機能</span><span class="sxs-lookup"><span data-stu-id="78af3-1898">Extension</span></span>

* <span data-ttu-id="78af3-1899">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1899">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="78af3-1900">Interactive</span><span class="sxs-lookup"><span data-stu-id="78af3-1900">Interactive</span></span>

* <span data-ttu-id="78af3-1901">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="78af3-1901">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="78af3-1902">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="78af3-1902">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="78af3-1903">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="78af3-1903">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="78af3-1904">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1904">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-1905">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-1905">Monitor</span></span>

* <span data-ttu-id="78af3-1906">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1906">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="78af3-1907">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1907">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="78af3-1908">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1908">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="78af3-1909">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1909">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1910">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1910">Network</span></span>

* <span data-ttu-id="78af3-1911">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1911">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="78af3-1912">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-1912">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="78af3-1913">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1913">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="78af3-1914">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1914">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="78af3-1915">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-1915">Profile</span></span>

* <span data-ttu-id="78af3-1916">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1916">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="78af3-1917">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1917">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="78af3-1918">RDBMS</span><span class="sxs-lookup"><span data-stu-id="78af3-1918">RDBMS</span></span>

* <span data-ttu-id="78af3-1919">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1919">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="78af3-1920">Service Bus</span><span class="sxs-lookup"><span data-stu-id="78af3-1920">Service Bus</span></span>

* <span data-ttu-id="78af3-1921">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="78af3-1921">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-1922">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1922">Storage</span></span>

* <span data-ttu-id="78af3-1923">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-1923">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="78af3-1924">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="78af3-1924">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1925">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1925">VM</span></span>

* <span data-ttu-id="78af3-1926">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1926">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="78af3-1927">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1927">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="78af3-1928">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1928">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="78af3-1929">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1929">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="78af3-1930">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1930">February 27, 2018</span></span>

<span data-ttu-id="78af3-1931">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="78af3-1931">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1932">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1932">Core</span></span>

* <span data-ttu-id="78af3-1933">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="78af3-1933">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="78af3-1934">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1934">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="78af3-1935">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1935">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1936">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1936">ACS</span></span>

* <span data-ttu-id="78af3-1937">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1937">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="78af3-1938">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="78af3-1938">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="78af3-1939">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1939">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="78af3-1940">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1940">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1941">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-1941">Appservice</span></span>

* <span data-ttu-id="78af3-1942">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="78af3-1942">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="78af3-1943">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="78af3-1943">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="78af3-1944">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="78af3-1944">Cognitive Services</span></span>

* <span data-ttu-id="78af3-1945">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1945">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="78af3-1946">消費</span><span class="sxs-lookup"><span data-stu-id="78af3-1946">Consumption</span></span>

* <span data-ttu-id="78af3-1947">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1947">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="78af3-1948">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1948">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="78af3-1949">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-1949">Container</span></span>

* <span data-ttu-id="78af3-1950">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1950">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="78af3-1951">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-1951">Network</span></span>

* <span data-ttu-id="78af3-1952">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="78af3-1952">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-1953">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-1953">Resource</span></span>

* <span data-ttu-id="78af3-1954">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1954">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="78af3-1955">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-1955">Role</span></span>

* <span data-ttu-id="78af3-1956">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1956">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-1957">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-1957">SQL</span></span>

* <span data-ttu-id="78af3-1958">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1958">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-1959">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-1959">Storage</span></span>

* <span data-ttu-id="78af3-1960">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-1960">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-1961">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-1961">VM</span></span>

* <span data-ttu-id="78af3-1962">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1962">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="78af3-1963">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="78af3-1963">February 13, 2018</span></span>

<span data-ttu-id="78af3-1964">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="78af3-1964">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="78af3-1965">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-1965">Core</span></span>

* <span data-ttu-id="78af3-1966">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1966">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-1967">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-1967">ACS</span></span>

* <span data-ttu-id="78af3-1968">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1968">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="78af3-1969">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1969">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="78af3-1970">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1970">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="78af3-1971">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1971">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="78af3-1972">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1972">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="78af3-1973">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1973">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="78af3-1974">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1974">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="78af3-1975">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="78af3-1975">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-1976">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-1976">Appservice</span></span>

* <span data-ttu-id="78af3-1977">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1977">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="78af3-1978">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1978">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="78af3-1979">CDN</span><span class="sxs-lookup"><span data-stu-id="78af3-1979">CDN</span></span>

* <span data-ttu-id="78af3-1980">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1980">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="78af3-1981">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-1981">Container</span></span>

* <span data-ttu-id="78af3-1982">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1982">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="78af3-1983">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1983">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="78af3-1984">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="78af3-1984">CosmosDB</span></span>

* <span data-ttu-id="78af3-1985">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1985">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="78af3-1986">拡張機能</span><span class="sxs-lookup"><span data-stu-id="78af3-1986">Extension</span></span>

* <span data-ttu-id="78af3-1987">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1987">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="78af3-1988">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1988">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="78af3-1989">フィードバック</span><span class="sxs-lookup"><span data-stu-id="78af3-1989">Feedback</span></span>

* <span data-ttu-id="78af3-1990">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1990">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="78af3-1991">Interactive</span><span class="sxs-lookup"><span data-stu-id="78af3-1991">Interactive</span></span>

* <span data-ttu-id="78af3-1992">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1992">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="78af3-1993">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1993">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="78af3-1994">IoT</span><span class="sxs-lookup"><span data-stu-id="78af3-1994">IoT</span></span>

* <span data-ttu-id="78af3-1995">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1995">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="78af3-1996">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1996">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="78af3-1997">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1997">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="78af3-1998">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-1998">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-1999">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-1999">Monitor</span></span>

* <span data-ttu-id="78af3-2000">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2000">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="78af3-2001">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-2001">Network</span></span>

* <span data-ttu-id="78af3-2002">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2002">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="78af3-2003">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-2003">Profile</span></span>

* <span data-ttu-id="78af3-2004">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2004">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-2005">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-2005">Resource</span></span>

* <span data-ttu-id="78af3-2006">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2006">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="78af3-2007">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-2007">Role</span></span>

* <span data-ttu-id="78af3-2008">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2008">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-2009">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-2009">SQL</span></span>

* <span data-ttu-id="78af3-2010">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2010">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="78af3-2011">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2011">Added `sql db rename`</span></span>
* <span data-ttu-id="78af3-2012">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2012">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-2013">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-2013">Storage</span></span>

* <span data-ttu-id="78af3-2014">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2014">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2015">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2015">VM</span></span>

* <span data-ttu-id="78af3-2016">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2016">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="78af3-2017">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2017">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="78af3-2018">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="78af3-2018">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="78af3-2019">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2019">January 31, 2018</span></span>

<span data-ttu-id="78af3-2020">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="78af3-2020">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="78af3-2021">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-2021">Core</span></span>

* <span data-ttu-id="78af3-2022">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2022">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="78af3-2023">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2023">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="78af3-2024">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2024">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="78af3-2025">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="78af3-2025">Use `--verbose` to see</span></span>
* <span data-ttu-id="78af3-2026">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="78af3-2026">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-2027">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-2027">ACS</span></span>

* <span data-ttu-id="78af3-2028">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2028">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="78af3-2029">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2029">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-2030">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-2030">Appservice</span></span>

* <span data-ttu-id="78af3-2031">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="78af3-2031">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="78af3-2032">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2032">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="78af3-2033">CDN</span><span class="sxs-lookup"><span data-stu-id="78af3-2033">CDN</span></span>

* <span data-ttu-id="78af3-2034">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2034">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="78af3-2035">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="78af3-2035">CosmosDB</span></span>

* <span data-ttu-id="78af3-2036">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2036">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="78af3-2037">Interactive</span><span class="sxs-lookup"><span data-stu-id="78af3-2037">Interactive</span></span>

* <span data-ttu-id="78af3-2038">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2038">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="78af3-2039">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-2039">Network</span></span>

* <span data-ttu-id="78af3-2040">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2040">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="78af3-2041">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2041">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="78af3-2042">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2042">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="78af3-2043">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2043">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="78af3-2044">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2044">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="78af3-2045">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2045">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="78af3-2046">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2046">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="78af3-2047">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2047">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="78af3-2048">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2048">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="78af3-2049">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2049">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="78af3-2050">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-2050">Profile</span></span>

* <span data-ttu-id="78af3-2051">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2051">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-2052">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-2052">Resource</span></span>

* <span data-ttu-id="78af3-2053">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2053">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-2054">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-2054">Storage</span></span>

* <span data-ttu-id="78af3-2055">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2055">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="78af3-2056">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2056">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="78af3-2057">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2057">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="78af3-2058">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2058">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="78af3-2059">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2059">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2060">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2060">VM</span></span>

* <span data-ttu-id="78af3-2061">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2061">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="78af3-2062">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2062">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="78af3-2063">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2063">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="78af3-2064">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2064">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="78af3-2065">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2065">January 17, 2018</span></span>

<span data-ttu-id="78af3-2066">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="78af3-2066">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-2067">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-2067">ACR</span></span>

* <span data-ttu-id="78af3-2068">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2068">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="78af3-2069">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2069">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-2070">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-2070">ACS</span></span>

* <span data-ttu-id="78af3-2071">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2071">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="78af3-2072">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2072">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-2073">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-2073">Appservice</span></span>

* <span data-ttu-id="78af3-2074">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2074">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="78af3-2075">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2075">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="78af3-2076">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2076">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="78af3-2077">バックアップ</span><span class="sxs-lookup"><span data-stu-id="78af3-2077">Backup</span></span>

* <span data-ttu-id="78af3-2078">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2078">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="78af3-2079">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2079">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="78af3-2080">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2080">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="78af3-2081">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2081">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="78af3-2082">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2082">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-2083">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-2083">Batch</span></span>

* <span data-ttu-id="78af3-2084">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2084">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="78af3-2085">クラウド</span><span class="sxs-lookup"><span data-stu-id="78af3-2085">Cloud</span></span>

* <span data-ttu-id="78af3-2086">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2086">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="78af3-2087">消費</span><span class="sxs-lookup"><span data-stu-id="78af3-2087">Consumption</span></span>

* <span data-ttu-id="78af3-2088">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2088">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="78af3-2089">Event Grid</span><span class="sxs-lookup"><span data-stu-id="78af3-2089">Event Grid</span></span>

* <span data-ttu-id="78af3-2090">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2090">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="78af3-2091">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2091">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="78af3-2092">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2092">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="78af3-2093">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="78af3-2093">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="78af3-2094">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2094">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="78af3-2095">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2095">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="78af3-2096">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2096">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="78af3-2097">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2097">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="78af3-2098">Interactive</span><span class="sxs-lookup"><span data-stu-id="78af3-2098">Interactive</span></span>

* <span data-ttu-id="78af3-2099">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2099">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="78af3-2100">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2100">Fixed errors on startup</span></span>
* <span data-ttu-id="78af3-2101">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2101">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="78af3-2102">IoT</span><span class="sxs-lookup"><span data-stu-id="78af3-2102">IoT</span></span>

* <span data-ttu-id="78af3-2103">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2103">Added support for device provisioning service</span></span>
* <span data-ttu-id="78af3-2104">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2104">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="78af3-2105">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2105">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-2106">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-2106">Monitor</span></span>

* <span data-ttu-id="78af3-2107">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2107">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="78af3-2108">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2108">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="78af3-2109">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2109">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="78af3-2110">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-2110">Network</span></span>

* <span data-ttu-id="78af3-2111">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2111">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="78af3-2112">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2112">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="78af3-2113">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-2113">Profile</span></span>

* <span data-ttu-id="78af3-2114">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2114">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="78af3-2115">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-2115">Role</span></span>

* <span data-ttu-id="78af3-2116">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2116">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="78af3-2117">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="78af3-2117">Service Fabric</span></span>

* <span data-ttu-id="78af3-2118">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2118">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="78af3-2119">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2119">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2120">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2120">VM</span></span>

* <span data-ttu-id="78af3-2121">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="78af3-2121">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="78af3-2122">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2122">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="78af3-2123">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2123">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="78af3-2124">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2124">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="78af3-2125">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2125">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="78af3-2126">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2126">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="78af3-2127">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2127">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="78af3-2128">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2128">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="78af3-2129">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2129">December 19, 2017</span></span>

<span data-ttu-id="78af3-2130">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="78af3-2130">Version 2.0.23</span></span>

* <span data-ttu-id="78af3-2131">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2131">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="78af3-2132">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-2132">Container</span></span>

* <span data-ttu-id="78af3-2133">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2133">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="78af3-2134">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-2134">Network</span></span>

* <span data-ttu-id="78af3-2135">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2135">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="78af3-2136">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2136">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-2137">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-2137">Storage</span></span>

* <span data-ttu-id="78af3-2138">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2138">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2139">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2139">VM</span></span>

* <span data-ttu-id="78af3-2140">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2140">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="78af3-2141">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2141">December 5, 2017</span></span>

<span data-ttu-id="78af3-2142">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="78af3-2142">Version 2.0.22</span></span>

* <span data-ttu-id="78af3-2143">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2143">Removed `az component` commands.</span></span> <span data-ttu-id="78af3-2144">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="78af3-2144">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="78af3-2145">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-2145">Core</span></span>
* <span data-ttu-id="78af3-2146">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2146">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="78af3-2147">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2147">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-2148">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-2148">ACS</span></span>

* <span data-ttu-id="78af3-2149">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2149">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="78af3-2150">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2150">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="78af3-2151">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2151">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="78af3-2152">Advisor</span><span class="sxs-lookup"><span data-stu-id="78af3-2152">Advisor</span></span>

* <span data-ttu-id="78af3-2153">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="78af3-2153">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-2154">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-2154">Appservice</span></span>

* <span data-ttu-id="78af3-2155">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2155">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="78af3-2156">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2156">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="78af3-2157">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2157">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="78af3-2158">消費</span><span class="sxs-lookup"><span data-stu-id="78af3-2158">Consumption</span></span>

* <span data-ttu-id="78af3-2159">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2159">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="78af3-2160">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-2160">Container</span></span>

* <span data-ttu-id="78af3-2161">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2161">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-2162">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-2162">Monitor</span></span>

* <span data-ttu-id="78af3-2163">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2163">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-2164">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-2164">Resource</span></span>

* <span data-ttu-id="78af3-2165">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2165">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="78af3-2166">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-2166">Role</span></span>

* <span data-ttu-id="78af3-2167">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2167">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="78af3-2168">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2168">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="78af3-2169">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2169">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-2170">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-2170">SQL</span></span>

* <span data-ttu-id="78af3-2171">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2171">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="78af3-2172">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2172">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2173">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2173">VM</span></span>

* <span data-ttu-id="78af3-2174">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2174">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="78af3-2175">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2175">November 14, 2017</span></span>

<span data-ttu-id="78af3-2176">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="78af3-2176">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-2177">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-2177">ACR</span></span>

* <span data-ttu-id="78af3-2178">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2178">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="78af3-2179">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-2179">ACS</span></span>

* <span data-ttu-id="78af3-2180">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2180">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="78af3-2181">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2181">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="78af3-2182">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2182">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="78af3-2183">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2183">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="78af3-2184">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2184">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-2185">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-2185">Appservice</span></span>

* <span data-ttu-id="78af3-2186">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2186">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="78af3-2187">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2187">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="78af3-2188">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2188">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="78af3-2189">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2189">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="78af3-2190">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2190">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="78af3-2191">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="78af3-2191">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-2192">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-2192">Batch</span></span>

* <span data-ttu-id="78af3-2193">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2193">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="78af3-2194">Batchai</span><span class="sxs-lookup"><span data-stu-id="78af3-2194">Batchai</span></span>

* <span data-ttu-id="78af3-2195">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2195">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="78af3-2196">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2196">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="78af3-2197">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2197">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="78af3-2198">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2198">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="78af3-2199">クラウド</span><span class="sxs-lookup"><span data-stu-id="78af3-2199">Cloud</span></span>

* <span data-ttu-id="78af3-2200">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2200">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="78af3-2201">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-2201">Container</span></span>

* <span data-ttu-id="78af3-2202">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2202">Added support to open multiple ports</span></span>
* <span data-ttu-id="78af3-2203">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2203">Added container group restart policy</span></span>
* <span data-ttu-id="78af3-2204">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2204">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="78af3-2205">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2205">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="78af3-2206">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="78af3-2206">Data Lake Analytics</span></span>

* <span data-ttu-id="78af3-2207">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2207">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="78af3-2208">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="78af3-2208">Data Lake Store</span></span>

* <span data-ttu-id="78af3-2209">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2209">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="78af3-2210">拡張機能</span><span class="sxs-lookup"><span data-stu-id="78af3-2210">Extension</span></span>

* <span data-ttu-id="78af3-2211">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2211">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="78af3-2212">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2212">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="78af3-2213">IoT</span><span class="sxs-lookup"><span data-stu-id="78af3-2213">IoT</span></span>

* <span data-ttu-id="78af3-2214">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2214">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-2215">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-2215">Monitor</span></span>

* <span data-ttu-id="78af3-2216">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2216">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="78af3-2217">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-2217">Network</span></span>

* <span data-ttu-id="78af3-2218">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2218">Added support for CAA DNS records</span></span>
* <span data-ttu-id="78af3-2219">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2219">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="78af3-2220">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2220">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="78af3-2221">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2221">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="78af3-2222">Reservations</span><span class="sxs-lookup"><span data-stu-id="78af3-2222">Reservations</span></span>

* <span data-ttu-id="78af3-2223">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="78af3-2223">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-2224">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-2224">Resource</span></span>

* <span data-ttu-id="78af3-2225">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2225">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-2226">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-2226">SQL</span></span>

* <span data-ttu-id="78af3-2227">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2227">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-2228">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-2228">Storage</span></span>

* <span data-ttu-id="78af3-2229">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2229">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="78af3-2230">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2230">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="78af3-2231">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2231">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="78af3-2232">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2232">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="78af3-2233">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2233">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="78af3-2234">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2234">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="78af3-2235">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2235">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2236">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2236">VM</span></span>

* <span data-ttu-id="78af3-2237">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2237">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="78af3-2238">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2238">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="78af3-2239">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2239">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="78af3-2240">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2240">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="78af3-2241">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2241">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="78af3-2242">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2242">October 24, 2017</span></span>

<span data-ttu-id="78af3-2243">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="78af3-2243">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="78af3-2244">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-2244">Core</span></span>

* <span data-ttu-id="78af3-2245">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2245">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-2246">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-2246">ACR</span></span>

* <span data-ttu-id="78af3-2247">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2247">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="78af3-2248">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2248">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="78af3-2249">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2249">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-2250">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-2250">ACS</span></span>

* <span data-ttu-id="78af3-2251">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2251">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="78af3-2252">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2252">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-2253">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-2253">Appservice</span></span>

* <span data-ttu-id="78af3-2254">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2254">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="78af3-2255">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="78af3-2255">Component</span></span>

* <span data-ttu-id="78af3-2256">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2256">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-2257">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-2257">Monitor</span></span>

* <span data-ttu-id="78af3-2258">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2258">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-2259">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-2259">Resource</span></span>

* <span data-ttu-id="78af3-2260">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2260">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="78af3-2261">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2261">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2262">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2262">VM</span></span>

* <span data-ttu-id="78af3-2263">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2263">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="78af3-2264">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2264">October 9, 2017</span></span>

<span data-ttu-id="78af3-2265">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="78af3-2265">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="78af3-2266">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-2266">Core</span></span>

* <span data-ttu-id="78af3-2267">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2267">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-2268">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-2268">Appservice</span></span>

* <span data-ttu-id="78af3-2269">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2269">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-2270">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-2270">Batch</span></span>

* <span data-ttu-id="78af3-2271">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2271">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="78af3-2272">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2272">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="78af3-2273">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2273">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="78af3-2274">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2274">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="78af3-2275">Batchai</span><span class="sxs-lookup"><span data-stu-id="78af3-2275">Batchai</span></span>

* <span data-ttu-id="78af3-2276">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="78af3-2276">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="78af3-2277">KeyVault</span><span class="sxs-lookup"><span data-stu-id="78af3-2277">Keyvault</span></span>

* <span data-ttu-id="78af3-2278">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2278">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="78af3-2279">(#4448)</span><span class="sxs-lookup"><span data-stu-id="78af3-2279">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="78af3-2280">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-2280">Network</span></span>

* <span data-ttu-id="78af3-2281">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2281">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="78af3-2282">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2282">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-2283">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-2283">Resource</span></span>

* <span data-ttu-id="78af3-2284">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2284">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="78af3-2285">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2285">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="78af3-2286">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2286">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="78af3-2287">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2287">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-2288">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-2288">Sql</span></span>

* <span data-ttu-id="78af3-2289">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2289">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="78af3-2290">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2290">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="78af3-2291">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2291">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-2292">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-2292">Storage</span></span>

* <span data-ttu-id="78af3-2293">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2293">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2294">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2294">Vm</span></span>

* <span data-ttu-id="78af3-2295">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2295">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="78af3-2296">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2296">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="78af3-2297">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2297">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="78af3-2298">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2298">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="78af3-2299">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2299">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="78af3-2300">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2300">September 22, 2017</span></span>

<span data-ttu-id="78af3-2301">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="78af3-2301">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-2302">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-2302">Resource</span></span>

* <span data-ttu-id="78af3-2303">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2303">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="78af3-2304">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2304">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="78af3-2305">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2305">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="78af3-2306">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2306">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="78af3-2307">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-2307">Network</span></span>

* <span data-ttu-id="78af3-2308">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2308">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="78af3-2309">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2309">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="78af3-2310">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2310">Added `asg` application security group commands</span></span>
* <span data-ttu-id="78af3-2311">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2311">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="78af3-2312">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2312">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="78af3-2313">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2313">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="78af3-2314">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2314">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-2315">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-2315">Storage</span></span>

* <span data-ttu-id="78af3-2316">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2316">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="78af3-2317">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="78af3-2317">Eventgrid</span></span>

* <span data-ttu-id="78af3-2318">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2318">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-2319">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-2319">SQL</span></span>

* <span data-ttu-id="78af3-2320">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2320">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="78af3-2321">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="78af3-2321">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="78af3-2322">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2322">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="78af3-2323">KeyVault</span><span class="sxs-lookup"><span data-stu-id="78af3-2323">Keyvault</span></span>

* <span data-ttu-id="78af3-2324">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2324">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2325">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2325">VM</span></span>

* <span data-ttu-id="78af3-2326">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2326">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="78af3-2327">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2327">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="78af3-2328">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2328">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="78af3-2329">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2329">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="78af3-2330">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2330">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="78af3-2331">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2331">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-2332">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-2332">ACS</span></span>

* <span data-ttu-id="78af3-2333">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2333">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-2334">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-2334">Appservice</span></span>

* <span data-ttu-id="78af3-2335">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2335">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="78af3-2336">バックアップ</span><span class="sxs-lookup"><span data-stu-id="78af3-2336">Backup</span></span>

* <span data-ttu-id="78af3-2337">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="78af3-2337">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="78af3-2338">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2338">September 11, 2017</span></span>

<span data-ttu-id="78af3-2339">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="78af3-2339">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="78af3-2340">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-2340">Core</span></span>

* <span data-ttu-id="78af3-2341">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2341">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="78af3-2342">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2342">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-2343">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-2343">Acs</span></span>

* <span data-ttu-id="78af3-2344">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2344">Added `acs list-locations` command</span></span>
* <span data-ttu-id="78af3-2345">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2345">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-2346">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-2346">Appservice</span></span>

* <span data-ttu-id="78af3-2347">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2347">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="78af3-2348">CDN</span><span class="sxs-lookup"><span data-stu-id="78af3-2348">CDN</span></span>

* <span data-ttu-id="78af3-2349">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2349">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="78af3-2350">拡張機能</span><span class="sxs-lookup"><span data-stu-id="78af3-2350">Extension</span></span>

* <span data-ttu-id="78af3-2351">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="78af3-2351">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="78af3-2352">KeyVault</span><span class="sxs-lookup"><span data-stu-id="78af3-2352">Keyvault</span></span>

* <span data-ttu-id="78af3-2353">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2353">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="78af3-2354">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-2354">Network</span></span>

* <span data-ttu-id="78af3-2355">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2355">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="78af3-2356">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2356">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="78af3-2357">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2357">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="78af3-2358">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2358">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="78af3-2359">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2359">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-2360">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-2360">Resource</span></span>

* <span data-ttu-id="78af3-2361">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="78af3-2361">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="78af3-2362">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="78af3-2362">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="78af3-2363">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="78af3-2363">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="78af3-2364">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2364">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-2365">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-2365">SQL</span></span>

* <span data-ttu-id="78af3-2366">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2366">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2367">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2367">VM</span></span>

* <span data-ttu-id="78af3-2368">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="78af3-2368">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="78af3-2369">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="78af3-2369">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="78af3-2370">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2370">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="78af3-2371">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="78af3-2371">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="78af3-2372">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="78af3-2372">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="78af3-2373">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2373">August 31, 2017</span></span>

<span data-ttu-id="78af3-2374">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="78af3-2374">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="78af3-2375">KeyVault</span><span class="sxs-lookup"><span data-stu-id="78af3-2375">Keyvault</span></span>

* <span data-ttu-id="78af3-2376">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2376">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="78af3-2377">SF</span><span class="sxs-lookup"><span data-stu-id="78af3-2377">Sf</span></span>

* <span data-ttu-id="78af3-2378">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="78af3-2378">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-2379">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-2379">Storage</span></span>

* <span data-ttu-id="78af3-2380">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2380">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="78af3-2381">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="78af3-2381">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="78af3-2382">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2382">August 28, 2017</span></span>

<span data-ttu-id="78af3-2383">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="78af3-2383">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="78af3-2384">CLI</span><span class="sxs-lookup"><span data-stu-id="78af3-2384">CLI</span></span>

* <span data-ttu-id="78af3-2385">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2385">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-2386">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-2386">ACS</span></span>

* <span data-ttu-id="78af3-2387">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2387">Corrected preview regions</span></span>
* <span data-ttu-id="78af3-2388">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2388">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="78af3-2389">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2389">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-2390">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-2390">Appservice</span></span>

* <span data-ttu-id="78af3-2391">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2391">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="78af3-2392">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2392">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="78af3-2393">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2393">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="78af3-2394">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2394">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="78af3-2395">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="78af3-2395">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="78af3-2396">IoT</span><span class="sxs-lookup"><span data-stu-id="78af3-2396">IoT</span></span>

* <span data-ttu-id="78af3-2397">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2397">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="78af3-2398">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-2398">Network</span></span>

* <span data-ttu-id="78af3-2399">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2399">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="78af3-2400">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2400">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="78af3-2401">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2401">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="78af3-2402">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2402">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="78af3-2403">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2403">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="78af3-2404">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-2404">Profile</span></span>

* <span data-ttu-id="78af3-2405">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2405">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="78af3-2406">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="78af3-2406">Service Fabric</span></span>

* <span data-ttu-id="78af3-2407">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="78af3-2407">Preview release</span></span>
* <span data-ttu-id="78af3-2408">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2408">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="78af3-2409">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2409">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="78af3-2410">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2410">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-2411">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-2411">Storage</span></span>

* <span data-ttu-id="78af3-2412">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2412">Enabled setting blob tier</span></span>
* <span data-ttu-id="78af3-2413">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2413">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="78af3-2414">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2414">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="78af3-2415">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2415">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="78af3-2416">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2416">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="78af3-2417">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="78af3-2417">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2418">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2418">VM</span></span>

* <span data-ttu-id="78af3-2419">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2419">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="78af3-2420">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2420">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="78af3-2421">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2421">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="78af3-2422">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2422">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="78af3-2423">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2423">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="78af3-2424">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2424">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="78af3-2425">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2425">August 15, 2017</span></span>

<span data-ttu-id="78af3-2426">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="78af3-2426">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-2427">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-2427">ACS</span></span>

* <span data-ttu-id="78af3-2428">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2428">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-2429">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-2429">Appservice</span></span>

* <span data-ttu-id="78af3-2430">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2430">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="78af3-2431">Event Grid</span><span class="sxs-lookup"><span data-stu-id="78af3-2431">Event Grid</span></span>

* <span data-ttu-id="78af3-2432">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2432">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="78af3-2433">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2433">August 11, 2017</span></span>

<span data-ttu-id="78af3-2434">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="78af3-2434">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-2435">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-2435">ACS</span></span>

* <span data-ttu-id="78af3-2436">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2436">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-2437">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-2437">Batch</span></span>

* <span data-ttu-id="78af3-2438">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2438">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="78af3-2439">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2439">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="78af3-2440">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2440">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="78af3-2441">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2441">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="78af3-2442">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2442">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="78af3-2443">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2443">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="78af3-2444">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="78af3-2444">Component</span></span>

* <span data-ttu-id="78af3-2445">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2445">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="78af3-2446">コンテナー</span><span class="sxs-lookup"><span data-stu-id="78af3-2446">Container</span></span>

* <span data-ttu-id="78af3-2447">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2447">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="78af3-2448">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="78af3-2448">Data Lake Store</span></span>

* <span data-ttu-id="78af3-2449">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2449">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="78af3-2450">Event Grid</span><span class="sxs-lookup"><span data-stu-id="78af3-2450">Event Grid</span></span>

* <span data-ttu-id="78af3-2451">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="78af3-2451">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="78af3-2452">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-2452">Network</span></span>

* <span data-ttu-id="78af3-2453">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2453">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="78af3-2454">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2454">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="78af3-2455">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2455">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="78af3-2456">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2456">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="78af3-2457">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-2457">Profile</span></span>

* <span data-ttu-id="78af3-2458">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2458">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-2459">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-2459">Storage</span></span>

* <span data-ttu-id="78af3-2460">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="78af3-2460">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2461">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2461">VM</span></span>

* <span data-ttu-id="78af3-2462">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2462">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="78af3-2463">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2463">Exposed `list-skus` command</span></span>
* <span data-ttu-id="78af3-2464">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2464">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="78af3-2465">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="78af3-2465">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="78af3-2466">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2466">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="78af3-2467">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2467">July 28, 2017</span></span>

<span data-ttu-id="78af3-2468">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="78af3-2468">Version 2.0.12</span></span>

* <span data-ttu-id="78af3-2469">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2469">Added container commands</span></span>
* <span data-ttu-id="78af3-2470">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2470">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="78af3-2471">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-2471">Core</span></span>

* <span data-ttu-id="78af3-2472">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="78af3-2472">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="78af3-2473">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2473">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="78af3-2474">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="78af3-2474">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="78af3-2475">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="78af3-2475">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="78af3-2476">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="78af3-2476">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="78af3-2477">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="78af3-2477">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="78af3-2478">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="78af3-2478">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="78af3-2479">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="78af3-2479">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="78af3-2480">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="78af3-2480">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="78af3-2481">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="78af3-2481">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="78af3-2482">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="78af3-2482">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="78af3-2483">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="78af3-2483">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="78af3-2484">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2484">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="78af3-2485">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2485">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="78af3-2486">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2486">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="78af3-2487">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="78af3-2487">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="78af3-2488">ACR</span><span class="sxs-lookup"><span data-stu-id="78af3-2488">ACR</span></span>

* <span data-ttu-id="78af3-2489">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2489">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="78af3-2490">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2490">Support SKU update for managed registries</span></span>
* <span data-ttu-id="78af3-2491">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2491">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="78af3-2492">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2492">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="78af3-2493">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2493">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="78af3-2494">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2494">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-2495">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-2495">ACS</span></span>

* <span data-ttu-id="78af3-2496">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2496">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-2497">Appservice</span><span class="sxs-lookup"><span data-stu-id="78af3-2497">Appservice</span></span>

* <span data-ttu-id="78af3-2498">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2498">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="78af3-2499">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2499">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="78af3-2500">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="78af3-2500">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="78af3-2501">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="78af3-2501">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="78af3-2502">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="78af3-2502">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="78af3-2503">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="78af3-2503">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="78af3-2504">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="78af3-2504">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="78af3-2505">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="78af3-2505">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="78af3-2506">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2506">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="78af3-2507">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="78af3-2507">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="78af3-2508">Batch</span><span class="sxs-lookup"><span data-stu-id="78af3-2508">Batch</span></span>

* <span data-ttu-id="78af3-2509">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2509">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="78af3-2510">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2510">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="78af3-2511">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2511">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="78af3-2512">CDN</span><span class="sxs-lookup"><span data-stu-id="78af3-2512">CDN</span></span>

* <span data-ttu-id="78af3-2513">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2513">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="78af3-2514">クラウド</span><span class="sxs-lookup"><span data-stu-id="78af3-2514">Cloud</span></span>

* <span data-ttu-id="78af3-2515">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2515">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="78af3-2516">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="78af3-2516">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="78af3-2517">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2517">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="78af3-2518">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2518">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="78af3-2519">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2519">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="78af3-2520">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="78af3-2520">CosmosDB</span></span>

* <span data-ttu-id="78af3-2521">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2521">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="78af3-2522">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2522">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="78af3-2523">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="78af3-2523">Data Lake Analytics</span></span>

* <span data-ttu-id="78af3-2524">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2524">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="78af3-2525">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2525">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="78af3-2526">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2526">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="78af3-2527">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="78af3-2527">Data Lake Store</span></span>

* <span data-ttu-id="78af3-2528">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2528">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="78af3-2529">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2529">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="78af3-2530">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2530">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="78af3-2531">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="78af3-2531">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="78af3-2532">対話</span><span class="sxs-lookup"><span data-stu-id="78af3-2532">Interactive</span></span>

* <span data-ttu-id="78af3-2533">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2533">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="78af3-2534">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="78af3-2534">Increased test coverage</span></span>
* <span data-ttu-id="78af3-2535">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2535">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="78af3-2536">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="78af3-2536">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="78af3-2537">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="78af3-2537">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="78af3-2538">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="78af3-2538">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="78af3-2539">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="78af3-2539">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="78af3-2540">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2540">Added `--progress` flag</span></span>
* <span data-ttu-id="78af3-2541">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2541">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="78af3-2542">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="78af3-2542">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="78af3-2543">IoT</span><span class="sxs-lookup"><span data-stu-id="78af3-2543">IoT</span></span>

* <span data-ttu-id="78af3-2544">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2544">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="78af3-2545">(#3934)</span><span class="sxs-lookup"><span data-stu-id="78af3-2545">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="78af3-2546">Key Vault</span><span class="sxs-lookup"><span data-stu-id="78af3-2546">Key vault</span></span>

* <span data-ttu-id="78af3-2547">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2547">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="78af3-2548">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="78af3-2548">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="78af3-2549">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="78af3-2549">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="78af3-2550">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="78af3-2550">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="78af3-2551">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="78af3-2551">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="78af3-2552">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="78af3-2552">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="78af3-2553">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2553">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="78af3-2554">(#3307)</span><span class="sxs-lookup"><span data-stu-id="78af3-2554">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="78af3-2555">ラボ</span><span class="sxs-lookup"><span data-stu-id="78af3-2555">Lab</span></span>

* <span data-ttu-id="78af3-2556">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2556">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="78af3-2557">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2557">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-2558">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-2558">Monitor</span></span>

* <span data-ttu-id="78af3-2559">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="78af3-2559">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="78af3-2560">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2560">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="78af3-2561">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2561">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="78af3-2562">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2562">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="78af3-2563">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2563">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="78af3-2564">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2564">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="78af3-2565">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2565">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="78af3-2566">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="78af3-2566">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="78af3-2567">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2567">`location` no longer required</span></span>
  * <span data-ttu-id="78af3-2568">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="78af3-2568">Add name and ID support for target</span></span>
  * <span data-ttu-id="78af3-2569">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="78af3-2569">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="78af3-2570">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2570">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="78af3-2571">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2571">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="78af3-2572">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="78af3-2572">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="78af3-2573">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2573">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="78af3-2574">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2574">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="78af3-2575">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-2575">Network</span></span>

* <span data-ttu-id="78af3-2576">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2576">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="78af3-2577">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2577">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="78af3-2578">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2578">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="78af3-2579">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2579">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="78af3-2580">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2580">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="78af3-2581">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2581">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="78af3-2582">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2582">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="78af3-2583">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2583">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="78af3-2584">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2584">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="78af3-2585">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2585">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="78af3-2586">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2586">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="78af3-2587">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2587">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="78af3-2588">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2588">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="78af3-2589">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2589">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="78af3-2590">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2590">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="78af3-2591">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2591">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="78af3-2592">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2592">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="78af3-2593">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2593">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="78af3-2594">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2594">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="78af3-2595">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2595">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="78af3-2596">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2596">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="78af3-2597">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2597">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="78af3-2598">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2598">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="78af3-2599">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="78af3-2599">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="78af3-2600">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="78af3-2600">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="78af3-2601">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="78af3-2601">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="78af3-2602">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="78af3-2602">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="78af3-2603">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-2603">Profile</span></span>

* <span data-ttu-id="78af3-2604">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2604">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="78af3-2605">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2605">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="78af3-2606">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="78af3-2606">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="78af3-2607">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2607">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="78af3-2608">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2608">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="78af3-2609">RDBMS</span><span class="sxs-lookup"><span data-stu-id="78af3-2609">RDBMS</span></span>

* <span data-ttu-id="78af3-2610">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="78af3-2610">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="78af3-2611">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="78af3-2611">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="78af3-2612">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="78af3-2612">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="78af3-2613">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="78af3-2613">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-2614">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-2614">Resource</span></span>

* <span data-ttu-id="78af3-2615">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2615">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="78af3-2616">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2616">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="78af3-2617">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2617">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="78af3-2618">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2618">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="78af3-2619">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="78af3-2619">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="78af3-2620">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2620">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="78af3-2621">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="78af3-2621">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="78af3-2622">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2622">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="78af3-2623">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-2623">Role</span></span>

* <span data-ttu-id="78af3-2624">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2624">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="78af3-2625">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="78af3-2625">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="78af3-2626">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="78af3-2626">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="78af3-2627">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="78af3-2627">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="78af3-2628">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2628">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="78af3-2629">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="78af3-2629">Service Fabric</span></span>
* <span data-ttu-id="78af3-2630">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="78af3-2630">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="78af3-2631">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="78af3-2631">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="78af3-2632">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="78af3-2632">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-2633">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-2633">SQL</span></span>

* <span data-ttu-id="78af3-2634">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2634">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="78af3-2635">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2635">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="78af3-2636">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2636">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-2637">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-2637">Storage</span></span>

* <span data-ttu-id="78af3-2638">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="78af3-2638">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="78af3-2639">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2639">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="78af3-2640">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="78af3-2640">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="78af3-2641">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="78af3-2641">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="78af3-2642">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="78af3-2642">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="78af3-2643">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="78af3-2643">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2644">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2644">VM</span></span>

* <span data-ttu-id="78af3-2645">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2645">Support configuring nsg</span></span>
* <span data-ttu-id="78af3-2646">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2646">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="78af3-2647">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="78af3-2647">Support managed service identities</span></span>
* <span data-ttu-id="78af3-2648">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2648">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="78af3-2649">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="78af3-2649">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="78af3-2650">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2650">May 10, 2017</span></span>

<span data-ttu-id="78af3-2651">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="78af3-2651">Version 2.0.6</span></span>

* <span data-ttu-id="78af3-2652">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2652">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="78af3-2653">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2653">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="78af3-2654">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2654">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="78af3-2655">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2655">Include Cognitive Services module</span></span>
* <span data-ttu-id="78af3-2656">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2656">Include Service Fabric module</span></span>
* <span data-ttu-id="78af3-2657">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="78af3-2657">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="78af3-2658">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2658">Add support for CDN commands</span></span>
* <span data-ttu-id="78af3-2659">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2659">Remove Container module</span></span>
* <span data-ttu-id="78af3-2660">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="78af3-2660">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="78af3-2661">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="78af3-2661">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="78af3-2662">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-2662">Core</span></span>

* <span data-ttu-id="78af3-2663">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="78af3-2663">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="78af3-2664">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="78af3-2664">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="78af3-2665">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="78af3-2665">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="78af3-2666">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="78af3-2666">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="78af3-2667">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="78af3-2667">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="78af3-2668">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="78af3-2668">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="78af3-2669">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="78af3-2669">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="78af3-2670">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="78af3-2670">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="78af3-2671">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="78af3-2671">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="78af3-2672">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="78af3-2672">core: Improved performance</span></span>
* <span data-ttu-id="78af3-2673">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="78af3-2673">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="78af3-2674">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="78af3-2674">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-2675">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-2675">ACS</span></span>

* <span data-ttu-id="78af3-2676">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2676">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="78af3-2677">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2677">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="78af3-2678">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2678">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="78af3-2679">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="78af3-2679">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-2680">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-2680">AppService</span></span>

* <span data-ttu-id="78af3-2681">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2681">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="78af3-2682">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2682">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="78af3-2683">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="78af3-2683">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="78af3-2684">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2684">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="78af3-2685">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2685">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="78af3-2686">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="78af3-2686">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="78af3-2687">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="78af3-2687">support slot swap with preview</span></span>
* <span data-ttu-id="78af3-2688">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="78af3-2688">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="78af3-2689">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="78af3-2689">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="78af3-2690">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="78af3-2690">CosmosDB</span></span>

* <span data-ttu-id="78af3-2691">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2691">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="78af3-2692">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2692">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="78af3-2693">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2693">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="78af3-2694">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2694">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="78af3-2695">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="78af3-2695">Data Lake Analytics</span></span>

* <span data-ttu-id="78af3-2696">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2696">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="78af3-2697">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2697">Add support for new catalog item type: package.</span></span> <span data-ttu-id="78af3-2698">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="78af3-2698">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="78af3-2699">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="78af3-2699">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="78af3-2700">テーブル</span><span class="sxs-lookup"><span data-stu-id="78af3-2700">Table</span></span>
  * <span data-ttu-id="78af3-2701">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="78af3-2701">Table valued function</span></span>
  * <span data-ttu-id="78af3-2702">表示</span><span class="sxs-lookup"><span data-stu-id="78af3-2702">View</span></span>
  * <span data-ttu-id="78af3-2703">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="78af3-2703">Table Statistics.</span></span> <span data-ttu-id="78af3-2704">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="78af3-2704">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="78af3-2705">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="78af3-2705">Data Lake Store</span></span>

* <span data-ttu-id="78af3-2706">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2706">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="78af3-2707">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="78af3-2707">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="78af3-2708">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="78af3-2708">missed help for access show.</span></span> <span data-ttu-id="78af3-2709">追加しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2709">adding it.</span></span> <span data-ttu-id="78af3-2710">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="78af3-2710">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="78af3-2711">検索</span><span class="sxs-lookup"><span data-stu-id="78af3-2711">Find</span></span>

* <span data-ttu-id="78af3-2712">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2712">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="78af3-2713">KeyVault</span><span class="sxs-lookup"><span data-stu-id="78af3-2713">KeyVault</span></span>

* <span data-ttu-id="78af3-2714">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2714">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="78af3-2715">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2715">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="78af3-2716">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="78af3-2716">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="78af3-2717">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2717">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="78af3-2718">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="78af3-2718">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="78af3-2719">ラボ</span><span class="sxs-lookup"><span data-stu-id="78af3-2719">Lab</span></span>

* <span data-ttu-id="78af3-2720">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2720">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="78af3-2721">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2721">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="78af3-2722">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2722">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="78af3-2723">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2723">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="78af3-2724">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2724">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="78af3-2725">監視</span><span class="sxs-lookup"><span data-stu-id="78af3-2725">Monitor</span></span>

* <span data-ttu-id="78af3-2726">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="78af3-2726">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="78af3-2727">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="78af3-2727">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="78af3-2728">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-2728">Network</span></span>

* <span data-ttu-id="78af3-2729">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2729">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="78af3-2730">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2730">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="78af3-2731">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2731">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="78af3-2732">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2732">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="78af3-2733">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2733">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="78af3-2734">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2734">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="78af3-2735">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2735">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="78af3-2736">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2736">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="78af3-2737">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2737">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="78af3-2738">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2738">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="78af3-2739">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2739">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="78af3-2740">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2740">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="78af3-2741">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2741">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="78af3-2742">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2742">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="78af3-2743">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="78af3-2743">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="78af3-2744">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2744">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="78af3-2745">プロファイル</span><span class="sxs-lookup"><span data-stu-id="78af3-2745">Profile</span></span>

* <span data-ttu-id="78af3-2746">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="78af3-2746">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="78af3-2747">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="78af3-2747">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="78af3-2748">Redis</span><span class="sxs-lookup"><span data-stu-id="78af3-2748">Redis</span></span>

* <span data-ttu-id="78af3-2749">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2749">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="78af3-2750">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2750">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="78af3-2751">リソース</span><span class="sxs-lookup"><span data-stu-id="78af3-2751">Resource</span></span>

* <span data-ttu-id="78af3-2752">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="78af3-2752">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="78af3-2753">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="78af3-2753">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="78af3-2754">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="78af3-2754">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="78af3-2755">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2755">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="78af3-2756">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="78af3-2756">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="78af3-2757">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2757">Add docs for az lock update.</span></span> <span data-ttu-id="78af3-2758">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="78af3-2758">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="78af3-2759">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="78af3-2759">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="78af3-2760">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="78af3-2760">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="78af3-2761">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="78af3-2761">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="78af3-2762">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="78af3-2762">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="78af3-2763">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="78af3-2763">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="78af3-2764">Role</span><span class="sxs-lookup"><span data-stu-id="78af3-2764">Role</span></span>

* <span data-ttu-id="78af3-2765">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="78af3-2765">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="78af3-2766">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="78af3-2766">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="78af3-2767">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="78af3-2767">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="78af3-2768">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="78af3-2768">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="78af3-2769">SQL</span><span class="sxs-lookup"><span data-stu-id="78af3-2769">SQL</span></span>

* <span data-ttu-id="78af3-2770">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="78af3-2770">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="78af3-2771">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="78af3-2771">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="78af3-2772">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-2772">Storage</span></span>

* <span data-ttu-id="78af3-2773">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="78af3-2773">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="78af3-2774">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2774">Add support for incremental blob copy</span></span>
* <span data-ttu-id="78af3-2775">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2775">Add support for large block blob upload</span></span>
* <span data-ttu-id="78af3-2776">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="78af3-2776">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2777">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2777">VM</span></span>

* <span data-ttu-id="78af3-2778">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="78af3-2778">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="78af3-2779">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="78af3-2779">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="78af3-2780">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="78af3-2780">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="78af3-2781">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="78af3-2781">az vm/vmss disk</span></span>
  3. <span data-ttu-id="78af3-2782">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="78af3-2782">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="78af3-2783">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="78af3-2783">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="78af3-2784">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="78af3-2784">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="78af3-2785">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2785">April 3, 2017</span></span>

<span data-ttu-id="78af3-2786">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="78af3-2786">Version 2.0.2</span></span>

<span data-ttu-id="78af3-2787">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="78af3-2787">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="78af3-2788">コア</span><span class="sxs-lookup"><span data-stu-id="78af3-2788">Core</span></span>

* <span data-ttu-id="78af3-2789">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="78af3-2789">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="78af3-2790">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="78af3-2790">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="78af3-2791">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="78af3-2791">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="78af3-2792">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="78af3-2792">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="78af3-2793">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="78af3-2793">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="78af3-2794">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="78af3-2794">Add prompting for missing template parameters.</span></span> <span data-ttu-id="78af3-2795">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="78af3-2795">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="78af3-2796">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="78af3-2796">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="78af3-2797">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="78af3-2797">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="78af3-2798">ACS</span><span class="sxs-lookup"><span data-stu-id="78af3-2798">ACS</span></span>

* <span data-ttu-id="78af3-2799">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="78af3-2799">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="78af3-2800">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="78af3-2800">Add support for ssh key password prompting.</span></span> <span data-ttu-id="78af3-2801">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="78af3-2801">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="78af3-2802">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="78af3-2802">Add support for windows clusters.</span></span> <span data-ttu-id="78af3-2803">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="78af3-2803">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="78af3-2804">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="78af3-2804">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="78af3-2805">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="78af3-2805">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="78af3-2806">AppService</span><span class="sxs-lookup"><span data-stu-id="78af3-2806">AppService</span></span>

* <span data-ttu-id="78af3-2807">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="78af3-2807">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="78af3-2808">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="78af3-2808">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="78af3-2809">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="78af3-2809">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="78af3-2810">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="78af3-2810">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="78af3-2811">DataLake</span><span class="sxs-lookup"><span data-stu-id="78af3-2811">DataLake</span></span>

* <span data-ttu-id="78af3-2812">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="78af3-2812">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="78af3-2813">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="78af3-2813">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="78af3-2814">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="78af3-2814">DocuemntDB</span></span>

* <span data-ttu-id="78af3-2815">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="78af3-2815">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="78af3-2816">VM</span><span class="sxs-lookup"><span data-stu-id="78af3-2816">VM</span></span>

* <span data-ttu-id="78af3-2817">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="78af3-2817">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="78af3-2818">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="78af3-2818">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="78af3-2819">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="78af3-2819">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="78af3-2820">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="78af3-2820">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="78af3-2821">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="78af3-2821">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="78af3-2822">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="78af3-2822">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="78af3-2823">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="78af3-2823">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="78af3-2824">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="78af3-2824">February 27, 2017</span></span>

<span data-ttu-id="78af3-2825">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="78af3-2825">Version 2.0.0</span></span>

<span data-ttu-id="78af3-2826">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="78af3-2826">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="78af3-2827">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="78af3-2827">Container Service (acs)</span></span>
- <span data-ttu-id="78af3-2828">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="78af3-2828">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="78af3-2829">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="78af3-2829">Networking</span></span>
- <span data-ttu-id="78af3-2830">Storage</span><span class="sxs-lookup"><span data-stu-id="78af3-2830">Storage</span></span>

<span data-ttu-id="78af3-2831">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="78af3-2831">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="78af3-2832">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="78af3-2832">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="78af3-2833">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="78af3-2833">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="78af3-2834">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="78af3-2834">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="78af3-2835">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="78af3-2835">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="78af3-2836">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="78af3-2836">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="78af3-2837">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="78af3-2837">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="78af3-2838">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="78af3-2838">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="78af3-2839">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="78af3-2839">Provide feedback from the command line with the `az feedback` command</span></span>

