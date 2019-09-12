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
ms.openlocfilehash: 03594fc6e7e24fd1b7d2f9c846161a40e8ea7678
ms.sourcegitcommit: f9bfb4b063151434b3a9bff936a73b251666e775
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/10/2019
ms.locfileid: "70878227"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="7c209-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="7c209-103">Azure CLI release notes</span></span>

## <a name="september-5-2019"></a><span data-ttu-id="7c209-104">2019 年 9 月 5 日</span><span class="sxs-lookup"><span data-stu-id="7c209-104">September 5, 2019</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-105">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-105">ACR</span></span>

* <span data-ttu-id="7c209-106">アイテム保持ポリシーを構成するためのコマンド グループ `acr config retention` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-106">Added command group `acr config retention` to configure retention policy</span></span>

### <a name="aks"></a><span data-ttu-id="7c209-107">AKS</span><span class="sxs-lookup"><span data-stu-id="7c209-107">AKS</span></span>

* <span data-ttu-id="7c209-108">次のコマンドを使用した ACR 統合のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="7c209-108">Added support for ACR integration with the following commands:</span></span>
  * <span data-ttu-id="7c209-109">AKS クラスターに ACR をアタッチするための `--attach-acr` パラメーターを `aks [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-109">Added `--attach-acr` parameter to `aks [create|update]` to attach an ACR to an AKS cluster</span></span>
  * <span data-ttu-id="7c209-110">AKS クラスターから ACR をデタッチするための `--detach-acr` パラメーターを `aks update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-110">Added `--detach-acr` parameter to `aks update` to detach the ACR from an AKS cluster</span></span>

### <a name="arm"></a><span data-ttu-id="7c209-111">ARM</span><span class="sxs-lookup"><span data-stu-id="7c209-111">ARM</span></span>

* <span data-ttu-id="7c209-112">API バージョン 2019-05-10 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-112">Updated to use API version 2019-05-10</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-113">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-113">Batch</span></span>

* <span data-ttu-id="7c209-114">`batch pool create` の `--json-file` に新しい JSON 構成設定を追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-114">Added new JSON configuration settings to `--json-file` for `batch pool create`:</span></span>
  * <span data-ttu-id="7c209-115">ファイル システム マウント用の `MountConfigurations` を追加しました (詳細については https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="7c209-115">Added `MountConfigurations` for file system mounts (see https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body for details)</span></span>
  * <span data-ttu-id="7c209-116">プール上のパブリック IP 用に、`NetworkConfiguration` にオプションのプロパティ `publicIPs` を追加しました (詳細については https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="7c209-116">Added optional property `publicIPs` on `NetworkConfiguration` for public IPs on pools (see https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body for details)</span></span>
* <span data-ttu-id="7c209-117">共有イメージ ギャラリーのサポートを `--image` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-117">Added support for shared image galleries to `--image`</span></span>
* <span data-ttu-id="7c209-118">[重大な変更] `batch pool create` の `--start-task-wait-for-success` の既定値を `true` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-118">[BREAKING CHANGE] Changed default value of `--start-task-wait-for-success` on `batch pool create` to be `true`</span></span>
* <span data-ttu-id="7c209-119">[重大な変更] `AutoUserSpecification` の `Scope` の既定値が常に Pool になるように変更しました (以前は Windows ノードでは `Task`、Linux ノードでは `Pool` でした)</span><span class="sxs-lookup"><span data-stu-id="7c209-119">[BREAKING CHANGE] Changed default value for `Scope` on `AutoUserSpecification` to always be Pool (was `Task` on Windows nodes, `Pool` on Linux nodes)</span></span>
  * <span data-ttu-id="7c209-120">この引数は、`--json-file` を使用して JSON 構成からのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="7c209-120">This argument can only be set from a JSON configuration with `--json-file`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="7c209-121">HDInsight</span><span class="sxs-lookup"><span data-stu-id="7c209-121">HDInsight</span></span>

* <span data-ttu-id="7c209-122">GA リリース</span><span class="sxs-lookup"><span data-stu-id="7c209-122">GA release</span></span>
* <span data-ttu-id="7c209-123">[重大な変更] `az hdinsight resize` のパラメーター `--workernode-count/-c` が必須に変更されました。</span><span class="sxs-lookup"><span data-stu-id="7c209-123">[BREAKING CHANGE] Changed parameter `--workernode-count/-c` of `az hdinsight resize` to be required.</span></span>

### <a name="key-vault"></a><span data-ttu-id="7c209-124">Key Vault</span><span class="sxs-lookup"><span data-stu-id="7c209-124">Key Vault</span></span>

* <span data-ttu-id="7c209-125">ネットワーク ルールからサブネットを削除できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-125">Fixed issue where subnets couldn't be deleted from network rules</span></span>
* <span data-ttu-id="7c209-126">重複したサブネットと IP アドレスをネットワーク ルールに追加できる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-126">Fixed issue where duplicated subnets and IP addresses could be added to network rules</span></span>

### <a name="network"></a><span data-ttu-id="7c209-127">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-127">Network</span></span>

* <span data-ttu-id="7c209-128">トラフィック分析間隔の値を設定する `--interval` パラメーターを `network watcher flow-log` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-128">Added `--interval` parameter to `network watcher flow-log` to set traffic analysis interval value</span></span>
* <span data-ttu-id="7c209-129">ゲートウェイ ID を管理するための `network application-gateway identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-129">Added `network application-gateway identity` to manage gateway identity</span></span>
* <span data-ttu-id="7c209-130">Key Vault ID を設定するためのサポートを `network application-gateway ssl-cert` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-130">Added support for setting Key Vault ID to `network application-gateway ssl-cert`</span></span>
* <span data-ttu-id="7c209-131">`network express-route peering peer-connection [show|list]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-131">Added `network express-route peering peer-connection [show|list]`</span></span>

### <a name="policy"></a><span data-ttu-id="7c209-132">ポリシー</span><span class="sxs-lookup"><span data-stu-id="7c209-132">Policy</span></span>

* <span data-ttu-id="7c209-133">API バージョン 2019-01-01 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-133">Updated to use API version 2019-01-01</span></span>

## <a name="august-27-2019"></a><span data-ttu-id="7c209-134">2019 年 8 月 27 日</span><span class="sxs-lookup"><span data-stu-id="7c209-134">August 27, 2019</span></span>

<span data-ttu-id="7c209-135">バージョン 2.0.72</span><span class="sxs-lookup"><span data-stu-id="7c209-135">Version 2.0.72</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-136">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-136">ACR</span></span>

* <span data-ttu-id="7c209-137">[重大な変更] `classic` SKU のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-137">[BREAKING CHNAGE] Removed support for the `classic` SKU</span></span>

### <a name="api-management"></a><span data-ttu-id="7c209-138">API Management</span><span class="sxs-lookup"><span data-stu-id="7c209-138">API Management</span></span>

* <span data-ttu-id="7c209-139">[プレビュー] `apim` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-139">[PREVIEW] Added `apim` command group</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-140">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-140">AppService</span></span>

* <span data-ttu-id="7c209-141">スロットを指定したときの `webapp webjob continuous start` コマンドに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-141">Fixed issue with `webapp webjob continuous start` command when specifying a slot</span></span>
* <span data-ttu-id="7c209-142">`env` フォルダーを検出してデプロイに使用されているファイルから削除するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-142">Changed `webapp up` to detect `env` folder and remove it from the file used for deployment</span></span>

### <a name="keyvault"></a><span data-ttu-id="7c209-143">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c209-143">Keyvault</span></span>

* <span data-ttu-id="7c209-144">`--expires` 引数を無視する `keyvault secret set` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-144">Fixed a bug in `keyvault secret set` that igored the `--expires` argument</span></span>

### <a name="network"></a><span data-ttu-id="7c209-145">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-145">Network</span></span>

* <span data-ttu-id="7c209-146">`--private-ip-address-version` 引数に IPv6 アドレスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-146">Added support for IPv6 addresses to `--private-ip-address-version` arguments</span></span>
* <span data-ttu-id="7c209-147">プライベート エンドポイントの管理用に新しいコマンド `network private-endpoint [create|update|list-types]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-147">Added new commands `network private-endpoint [create|update|list-types]` for private endpoint management</span></span>
* <span data-ttu-id="7c209-148">コマンド グループ `network private-link-service` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-148">Added command group `network private-link-service`</span></span>
* <span data-ttu-id="7c209-149">`--private-endpoint-network-policies` 引数と `--private-link-service-network-policies` 引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-149">Added `--private-endpoint-network-policies` and `--private-link-service-network-policies` arguments to `network vnet subnet update`</span></span>

### <a name="rbac"></a><span data-ttu-id="7c209-150">RBAC</span><span class="sxs-lookup"><span data-stu-id="7c209-150">RBAC</span></span>

* <span data-ttu-id="7c209-151">ホームページが更新されない `ad app update --homepage` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-151">Fixed issue with `ad app update --homepage` where homepage would not be updated</span></span>

### <a name="servicefabric"></a><span data-ttu-id="7c209-152">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7c209-152">ServiceFabric</span></span>

* <span data-ttu-id="7c209-153">キー コンテナーの大文字と小文字が混在する名前のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-153">Added support for mixed-case Key Vault names</span></span>
* <span data-ttu-id="7c209-154">Key Vault で証明書を使用したときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-154">Fixed issue when using certificates in Key Vault</span></span>
* <span data-ttu-id="7c209-155">PFX 証明書ファイルの使用に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-155">Fixed issue with using PFX certificate files</span></span>
* <span data-ttu-id="7c209-156">Key Vault リソースグループが指定されていなかったときの `sf cluster certificate add` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-156">Fixed issue with `sf cluster certificate add` when Key Vault resource group wasn't specified</span></span>
* <span data-ttu-id="7c209-157">`sf cluster set` が動作しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-157">Fixed issue with `sf cluster set` not working</span></span>

### <a name="signalr"></a><span data-ttu-id="7c209-158">SignalR</span><span class="sxs-lookup"><span data-stu-id="7c209-158">SignalR</span></span>

* <span data-ttu-id="7c209-159">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-159">Added new commands:</span></span>
  * <span data-ttu-id="7c209-160">`signalr cors`:SignalR CORS の管理</span><span class="sxs-lookup"><span data-stu-id="7c209-160">`signalr cors`: Manage SignalR CORS</span></span>
  * <span data-ttu-id="7c209-161">`signalr restart`:SignalR Service の再起動</span><span class="sxs-lookup"><span data-stu-id="7c209-161">`signalr restart`: Restart a SignalR service</span></span>
  * <span data-ttu-id="7c209-162">`signalr update`:SignalR Service の更新</span><span class="sxs-lookup"><span data-stu-id="7c209-162">`signalr update`: Update a SignalR service</span></span>
* <span data-ttu-id="7c209-163">`--service-mode` 引数を `signalr create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-163">Added `--service-mode` argument to `signalr create`</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-164">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-164">Storage</span></span>

* <span data-ttu-id="7c209-165">`storage account revoke-delegation-keys` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-165">Added `storage account revoke-delegation-keys` command</span></span>

## <a name="august-13-2019"></a><span data-ttu-id="7c209-166">2019 年 8 月 13 日</span><span class="sxs-lookup"><span data-stu-id="7c209-166">August 13, 2019</span></span>

<span data-ttu-id="7c209-167">バージョン 2.0.71</span><span class="sxs-lookup"><span data-stu-id="7c209-167">Version 2.0.71</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-168">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-168">AppService</span></span>

* <span data-ttu-id="7c209-169">`webapp webjob continuous` コマンドがスロットで失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-169">Fixed issue where `webapp webjob continuous` commands were failing for slots</span></span>

### <a name="botservice"></a><span data-ttu-id="7c209-170">BotService</span><span class="sxs-lookup"><span data-stu-id="7c209-170">BotService</span></span>

* <span data-ttu-id="7c209-171">[重大な変更] v3 SDK ボットの作成のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-171">[BREAKING CHANGE] Removed support for creating v3 SDK bots</span></span>

### <a name="cognitiveservices"></a><span data-ttu-id="7c209-172">CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7c209-172">CognitiveServices</span></span>

* <span data-ttu-id="7c209-173">`cognitiveservices account network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-173">Added `cognitiveservices account network-rule` commands</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="7c209-174">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="7c209-174">Cosmos DB</span></span>

* <span data-ttu-id="7c209-175">複数の書き込み場所を更新するときの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-175">Removed warning when updating multiple write locations</span></span>
* <span data-ttu-id="7c209-176">CosmosDB SQL、MongoDB、Cassandra、Gremlin、およびテーブル リソースとリソースのスループットのための CRUD コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-176">Added CRUD commands for CosmosDB SQL, MongoDB, Cassandra, Gremlin and Table resources and resource's throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="7c209-177">HDInsight</span><span class="sxs-lookup"><span data-stu-id="7c209-177">HDInsight</span></span>

<span data-ttu-id="7c209-178">このリリースには、多数の破壊的変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7c209-178">This release contains a large number of breaking changes.</span></span>

* <span data-ttu-id="7c209-179">[重大な変更] `hdinsight create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-179">[BREAKING CHANGE] Renamed parameters for `hdinsight create`:</span></span>
  * <span data-ttu-id="7c209-180">`--storage-default-container` の名前を `--storage-container` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-180">Renamed `--storage-default-container` to `--storage-container`</span></span>
  * <span data-ttu-id="7c209-181">`--storage-default-filesystem` の名前を `--storage-filesystem` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-181">Renamed `--storage-default-filesystem` to `--storage-filesystem`</span></span>
* <span data-ttu-id="7c209-182">[重大な変更] `application create` の `--name` 引数が、クラスター名の代わりにアプリケーション名を表すように変更されました</span><span class="sxs-lookup"><span data-stu-id="7c209-182">[BREAKING CHANGE] Changed the `--name` argument of `application create` to represent the application name instead of the cluster name</span></span>
* <span data-ttu-id="7c209-183">`--cluster-name` 引数が `application create` に追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="7c209-183">Added `--cluster-name` argument to `application create` to replace old `--name` functionality</span></span>
* <span data-ttu-id="7c209-184">[重大な変更] `application create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-184">[BREAKING CHANGE] Renamed parameters for `application create`:</span></span>
  * <span data-ttu-id="7c209-185">`--application-type` の名前を `--type` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-185">Renamed `--application-type` to `--type`</span></span>
  * <span data-ttu-id="7c209-186">`--marketplace-identifier` の名前を `--marketplace-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-186">Renamed `--marketplace-identifier` to `--marketplace-id`</span></span>
  * <span data-ttu-id="7c209-187">`--https-endpoint-access-mode` の名前を `--access-mode` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-187">Renamed `--https-endpoint-access-mode` to `--access-mode`</span></span>
  * <span data-ttu-id="7c209-188">`--https-endpoint-destination-port` の名前を `--destination-port` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-188">Renamed  `--https-endpoint-destination-port` to `--destination-port`</span></span>
* <span data-ttu-id="7c209-189">[重大な変更] `application create` のパラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-189">[BREAKING CHANGE] Removed parameters for `application create`:</span></span>
  * `--https-endpoint-location`
  * `--https-endpoint-public-port`
  * `--ssh-endpoint-destination-port`
  * `--ssh-endpoint-location`
  * `--ssh-endpoint-public-port`
* <span data-ttu-id="7c209-190">[破壊的変更] `hdinsight resize`の `--target-instance-count` の名前を `--workernode-count` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-190">[BREAKING CHNAGE] Renamed `--target-instance-count` to `--workernode-count` for `hdinsight resize`</span></span>
* <span data-ttu-id="7c209-191">[重大な変更] `hdinsight script-action` グループのすべてのコマンドが、スクリプト アクションの名前として `--name` パラメーターを使用するように変更されました。</span><span class="sxs-lookup"><span data-stu-id="7c209-191">[BREAKING CHANGE] Changed all commands in the `hdinsight script-action` group to use the `--name` parameter as the name of the script action.</span></span>
* <span data-ttu-id="7c209-192">`--cluster-name` 引数がすべての `hdinsight script-action` コマンドに追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="7c209-192">Added `--cluster-name` argument to all `hdinsight script-action` commands to replace old `--name` functionality</span></span>
* <span data-ttu-id="7c209-193">[重大な変更] すべての `hdinsight script-action` コマンドで `--script-execution-id` の名前を `--execution-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-193">[BREAKING CHANGE] Renamed `--script-execution-id` to `--execution-id` for all `hdinsight script-action` commands</span></span>
* <span data-ttu-id="7c209-194">[重大な変更] 名前を `hdinsight script-action show` から `hdinsight script-action show-execution-details` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-194">[BREAKING CHANGE] Renamed `hdinsight script-action show` to `hdinsight script-action show-execution-details`</span></span>
* <span data-ttu-id="7c209-195">[破壊的変更] `hdinsight script-action execute --roles` に対するパラメーターを、コンマ区切りではなくスペース区切りにしました</span><span class="sxs-lookup"><span data-stu-id="7c209-195">[BREAKING CHNAGE] Changed parameters to `hdinsight script-action execute --roles` to be space-separated instead of comma-separated</span></span>
* <span data-ttu-id="7c209-196">[重大な変更] `hdinsight script-action list`の `--persisted` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-196">[BREAKING CHANGE] Removed the `--persisted` parameter of `hdinsight script-action list`</span></span>
* <span data-ttu-id="7c209-197">ローカル JSON ファイルへのパスまたは JSON 文字列を受け入れるように `hdinsight create --cluster-configurations` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-197">Changed the `hdinsight create --cluster-configurations` parameter to accept a path to a local JSON file or a JSON string</span></span>
* <span data-ttu-id="7c209-198">`hdinsight script-action list-execution-history` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-198">Added command `hdinsight script-action list-execution-history`</span></span>
* <span data-ttu-id="7c209-199">Log Analytics ワークスペース ID またはワークスペース名を受け入れるように `hdinsight monitor enable --workspace` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-199">Changed `hdinsight monitor enable --workspace` to accept a Log Analytics workspace ID or workspace name</span></span>
* <span data-ttu-id="7c209-200">`hdinsight monitor enable --primary-key` 引数を追加しました。これは、ワークスペース ID がパラメーターとして指定されている場合に必要です</span><span class="sxs-lookup"><span data-stu-id="7c209-200">Added the `hdinsight monitor enable --primary-key` argument, which is needed if a workspace ID is provided as the parameter</span></span>
* <span data-ttu-id="7c209-201">例をさらに追加し、ヘルプ メッセージの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-201">Added more examples and updated descriptions for help messages</span></span>

### <a name="interactive"></a><span data-ttu-id="7c209-202">Interactive</span><span class="sxs-lookup"><span data-stu-id="7c209-202">Interactive</span></span>

* <span data-ttu-id="7c209-203">読み込みエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-203">Fixed a loading error</span></span>

### <a name="kubernetes"></a><span data-ttu-id="7c209-204">Kubernetes</span><span class="sxs-lookup"><span data-stu-id="7c209-204">Kubernetes</span></span>

* <span data-ttu-id="7c209-205">ダッシュボードのコンテナー ポートで `https` が使用されている場合に `https` を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-205">Changed to use `https` if dashboard container port is using `https`</span></span>

### <a name="network"></a><span data-ttu-id="7c209-206">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-206">Network</span></span>

* <span data-ttu-id="7c209-207">`--yes` 引数を `network dns record-set cname delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-207">Added `--yes` argument `network dns record-set cname delete`</span></span>

### <a name="profile"></a><span data-ttu-id="7c209-208">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-208">Profile</span></span>

* <span data-ttu-id="7c209-209">リソースのアクセス トークンを取得するための `account get-access-token` に `--resource-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-209">Added `--resource-type` argument to `account get-access-token` to get resource access tokens</span></span>

### <a name="servicefabric"></a><span data-ttu-id="7c209-210">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7c209-210">ServiceFabric</span></span>

* <span data-ttu-id="7c209-211">sf cluster create でサポートされているすべての OS バージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-211">Added all supported os version for sf cluster create</span></span>
* <span data-ttu-id="7c209-212">プライマリ証明書の検証のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-212">Fixed primary certificate validation bug</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-213">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-213">Storage</span></span>

* <span data-ttu-id="7c209-214">`storage copy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-214">Added command `storage copy`</span></span>

## <a name="july-30-2019"></a><span data-ttu-id="7c209-215">2019 年 7 月 30 日</span><span class="sxs-lookup"><span data-stu-id="7c209-215">July 30, 2019</span></span>

<span data-ttu-id="7c209-216">バージョン 2.0.70</span><span class="sxs-lookup"><span data-stu-id="7c209-216">Version 2.0.70</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-217">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-217">ACR</span></span>

* <span data-ttu-id="7c209-218">問題 #9952 (`acr pack build` コマンドでの回帰) を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-218">Fixed issue #9952 (a regression in the `acr pack build` command)</span></span>
* <span data-ttu-id="7c209-219">`acr pack build` の既定のビルダー イメージ名を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-219">Removed the default builder image name in `acr pack build`</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-220">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-220">Appservice</span></span>

* <span data-ttu-id="7c209-221">リソースが見つからない場合にメッセージ表示するように `webapp config ssl` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-221">Changed `webapp config ssl` to show a message if a resource is not found</span></span>
* <span data-ttu-id="7c209-222">`functionapp create` がストレージ アカウントの種類 `Standard_RAGRS` を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-222">Fixed issue where `functionapp create` does not accept `Standard_RAGRS` storage account type</span></span>
* <span data-ttu-id="7c209-223">古いバージョンの python を使用して `webapp up` を実行すると失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-223">Fixed an issue where `webapp up` would fail if run using older versions of python</span></span>

### <a name="network"></a><span data-ttu-id="7c209-224">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-224">Network</span></span>

* <span data-ttu-id="7c209-225">`network nic ip-config add` から無効なパラメーター `--ids` を削除しました (#9861 の修正)</span><span class="sxs-lookup"><span data-stu-id="7c209-225">Removed invalid parameter `--ids` from `network nic ip-config add` (fixes #9861)</span></span>
* <span data-ttu-id="7c209-226">#9604 を修正しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-226">Fixes #9604.</span></span> <span data-ttu-id="7c209-227">信頼されたルート証明書へのユーザーの関連付けをサポートするために、`network application-gateway http-settings [create|update]` に `--root-certs` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-227">Added `--root-certs` parameter to `network application-gateway http-settings [create|update]` to support user associate trusted root certificates.</span></span>
* <span data-ttu-id="7c209-228">`network dns record-set ns create` の引数 `--subscription` を修正しました (#9965)</span><span class="sxs-lookup"><span data-stu-id="7c209-228">Fixed arguent `--subscription` for `network dns record-set ns create` (#9965)</span></span>

### <a name="rbac"></a><span data-ttu-id="7c209-229">RBAC</span><span class="sxs-lookup"><span data-stu-id="7c209-229">RBAC</span></span>

* <span data-ttu-id="7c209-230">`user update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-230">Added `user update` command</span></span>
* <span data-ttu-id="7c209-231">[非推奨] ユーザー関連コマンドで `--upn-or-object-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-231">[DEPRECATED] Deprecated `--upn-or-object-id` from user-related commands</span></span>
    * <span data-ttu-id="7c209-232">代替引数の `--id` を使用してください</span><span class="sxs-lookup"><span data-stu-id="7c209-232">Use replacement argument `--id`</span></span>
* <span data-ttu-id="7c209-233">ユーザー関連コマンドに `--id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-233">Added `--id` argument to user-related commands</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-234">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-234">SQL</span></span>

* <span data-ttu-id="7c209-235">マネージド インスタンス キーおよび TDE 保護機能の管理コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-235">Added management commands for managed instance keys and TDE protector</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-236">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-236">Storage</span></span>

* <span data-ttu-id="7c209-237">`storage remove` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-237">Added `storage remove` command</span></span>
* <span data-ttu-id="7c209-238">`storage blob update` での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-238">Fixed an issue with `storage blob update`</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-239">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-239">VM</span></span>

* <span data-ttu-id="7c209-240">ゾーンの詳細を出力するための新しい API バージョンを使用するように `list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-240">Changed `list-skus` to use newer api-version to output zone details</span></span>
* <span data-ttu-id="7c209-241">`vmss create` の `--single-placement-group` の既定値を`false` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-241">Changed default of `--single-placement-group` to `false` for `vmss create`</span></span>
* <span data-ttu-id="7c209-242">`[snapshot|disk] create` において ZRS ストレージ SKU を選択する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-242">Added ability to select ZRS storage SKUs for `[snapshot|disk] create`</span></span>
* <span data-ttu-id="7c209-243">専用ホストをサポートするために、新しいコマンド グループ `vm host` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-243">Added new command group `vm host` to support dedicated hosts</span></span>
* <span data-ttu-id="7c209-244">VM 専用ホストを設定するためのパラメーター `--host` と `--host-group` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-244">Added parameters `--host` and `--host-group` on `vm create` to set VM dedicated host</span></span>

## <a name="july-16-2019"></a><span data-ttu-id="7c209-245">2019 年 7 月 16 日</span><span class="sxs-lookup"><span data-stu-id="7c209-245">July 16, 2019</span></span>

<span data-ttu-id="7c209-246">バージョン 2.0.69</span><span class="sxs-lookup"><span data-stu-id="7c209-246">Version 2.0.69</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-247">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-247">Appservice</span></span>

* <span data-ttu-id="7c209-248">ResourceGroupName または App の名前が無効な場合に適切なエラー メッセージを返すように `webapp identity` コマンドが変更されました</span><span class="sxs-lookup"><span data-stu-id="7c209-248">Changed `webapp identity` commands to return a proper error message if ResourceGroupName or App name are invalid</span></span>
* <span data-ttu-id="7c209-249">ResourceGroup が指定されなかった場合に numberOfSites の正しい値を返すように `webapp list` が修正されました</span><span class="sxs-lookup"><span data-stu-id="7c209-249">Fixed `webapp list` to return the correct value for numberOfSites if no ResourceGroup was provided</span></span>
* <span data-ttu-id="7c209-250">`appservice plan create` と `webapp create` の副作用が修正されました</span><span class="sxs-lookup"><span data-stu-id="7c209-250">Fixed side-effects of `appservice plan create` and `webapp create`</span></span>

### <a name="core"></a><span data-ttu-id="7c209-251">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-251">Core</span></span>

* <span data-ttu-id="7c209-252">`--subscription` が適用不可にもかかわらず表示される問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="7c209-252">Fixed issue where `--subscription` would appear despite being not applicable</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-253">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-253">Batch</span></span>

* <span data-ttu-id="7c209-254">[重大な変更] `batch pool node-agent-skus list` が `batch pool supported-images list` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="7c209-254">[BREAKING CHANGE] Replaced `batch pool node-agent-skus list` with `batch pool supported-images list`</span></span>
* <span data-ttu-id="7c209-255">`batch pool create network` の `--json-file` オプションを使用するときに、トラフィックのソース ポートに基づいてプールへのネットワーク アクセスをブロックするセキュリティ規則のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-255">Added support for security rules blocking network access to a pool based on the source port of the traffic when using the `--json-file` option of `batch pool create network`</span></span>
* <span data-ttu-id="7c209-256">`batch task create`の `--json-file` オプションを使用するときに、コンテナーの作業ディレクトリまたは Batch タスクの作業ディレクトリでタスクを実行するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-256">Added support for executing the task in the container working directory or in the Batch task working directory when using the `--json-file` option of `batch task create`</span></span>
* <span data-ttu-id="7c209-257">`batch pool create`の `--application-package-references` オプションが、既定値でのみ動作するというエラーが修正されました</span><span class="sxs-lookup"><span data-stu-id="7c209-257">Fixed error in `--application-package-references` option of `batch pool create` where it would only work with defaults</span></span>

### <a name="eventhubs"></a><span data-ttu-id="7c209-258">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="7c209-258">Eventhubs</span></span>

* <span data-ttu-id="7c209-259">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-259">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="rdbms"></a><span data-ttu-id="7c209-260">RDBMS</span><span class="sxs-lookup"><span data-stu-id="7c209-260">RDBMS</span></span>

* <span data-ttu-id="7c209-261">レプリカ作成コマンドでレプリカ SKU を指定するためのオプション パラメーターが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-261">Added optional parameter to specify replica SKU for create replica command</span></span>
* <span data-ttu-id="7c209-262">MySQL レプリカの作成で CI テストが失敗する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="7c209-262">Fixed the issue with CI test failure with creating MySQL replica</span></span>

### <a name="relay"></a><span data-ttu-id="7c209-263">リレー</span><span class="sxs-lookup"><span data-stu-id="7c209-263">Relay</span></span>

* <span data-ttu-id="7c209-264">クライアント承認が無効になっているときのハイブリッド接続の問題が修正されました ([#8775](https://github.com/azure/azure-cli/issues/8775))</span><span class="sxs-lookup"><span data-stu-id="7c209-264">Fixed issue with hybrid connection when client authroization disabled [#8775](https://github.com/azure/azure-cli/issues/8775)</span></span>
* <span data-ttu-id="7c209-265">パラメーター `--requires-transport-security` を `relay wcfrelay create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-265">Added parameter `--requires-transport-security` to `relay wcfrelay create`</span></span>

### <a name="servicebus"></a><span data-ttu-id="7c209-266">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7c209-266">Servicebus</span></span>

* <span data-ttu-id="7c209-267">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-267">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-268">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-268">Storage</span></span>

* <span data-ttu-id="7c209-269">ストレージ アカウントの更新で Files AADDS を有効にします</span><span class="sxs-lookup"><span data-stu-id="7c209-269">Enable Files AADDS for storage account update</span></span>
* <span data-ttu-id="7c209-270">修正された問題 `storage blob service-properties update --set`</span><span class="sxs-lookup"><span data-stu-id="7c209-270">Fixed issue `storage blob service-properties update --set`</span></span>

## <a name="july-2-2019"></a><span data-ttu-id="7c209-271">2019 年 7 月 2 日</span><span class="sxs-lookup"><span data-stu-id="7c209-271">July 2, 2019</span></span>

<span data-ttu-id="7c209-272">バージョン 2.0.68</span><span class="sxs-lookup"><span data-stu-id="7c209-272">Version 2.0.68</span></span>

### <a name="core"></a><span data-ttu-id="7c209-273">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-273">Core</span></span>

* <span data-ttu-id="7c209-274">コマンド モジュールが再頒布可能な 1 つの Python コードに統合されました。</span><span class="sxs-lookup"><span data-stu-id="7c209-274">Command modules are now consolidated into a single Python distributable.</span></span> <span data-ttu-id="7c209-275">これにより、PyPI での多くの `azure-cli-` パッケージの直接使用が廃止されます。</span><span class="sxs-lookup"><span data-stu-id="7c209-275">This deprecates direct use of many `azure-cli-` packages on PyPI.</span></span>
  <span data-ttu-id="7c209-276">またこれにより、インストール サイズが削減され、`pip` 経由で直接インストールしたユーザーにのみ影響が出ます。</span><span class="sxs-lookup"><span data-stu-id="7c209-276">This should reduce install size and only affect users who have directly installed via `pip`.</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-277">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-277">ACR</span></span>

* <span data-ttu-id="7c209-278">タスクへのタイマー トリガーのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-278">Added support for Timer Triggers to Task</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-279">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-279">Appservice</span></span>

* <span data-ttu-id="7c209-280">既定でアプリケーション インサイトを有効にするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-280">Changed `functionapp create` to enable application insights by default</span></span>
* <span data-ttu-id="7c209-281">[重大な変更] 非推奨の `functionapp devops-build` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-281">[BREAKING CHANGE] Removed deprecated `functionapp devops-build` command.</span></span>
  *  <span data-ttu-id="7c209-282">代わりに新しいコマンド `az functionapp devops-pipeline` を使用</span><span class="sxs-lookup"><span data-stu-id="7c209-282">Use the new command `az functionapp devops-pipeline` instead</span></span>
* <span data-ttu-id="7c209-283">Linux 従量課金プランの関数アプリのプラン サポートを `functionapp deployment config-zip` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-283">Added Linux Consumption function app plan support to `functionapp deployment config-zip`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="7c209-284">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="7c209-284">Cosmos DB</span></span>

* <span data-ttu-id="7c209-285">ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-285">Added support for disabling TTL</span></span>

### <a name="dls"></a><span data-ttu-id="7c209-286">DLS</span><span class="sxs-lookup"><span data-stu-id="7c209-286">DLS</span></span>

* <span data-ttu-id="7c209-287">ADLS バージョンを更新しました (0.0.45)</span><span class="sxs-lookup"><span data-stu-id="7c209-287">Updated ADLS version (0.0.45)</span></span>

### <a name="feedback"></a><span data-ttu-id="7c209-288">フィードバック</span><span class="sxs-lookup"><span data-stu-id="7c209-288">Feedback</span></span>

* <span data-ttu-id="7c209-289">失敗した拡張機能コマンドを報告するときに、`az feedback` はインデックスからの拡張機能のプロジェクト/リポジトリの url にブラウザーを開こうとするようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-289">When reporting a failed extension command, `az feedback` now attempts to open the browser to the project/repo url of the extension from the index</span></span>

### <a name="hdinsight"></a><span data-ttu-id="7c209-290">HDInsight</span><span class="sxs-lookup"><span data-stu-id="7c209-290">HDInsight</span></span>

* <span data-ttu-id="7c209-291">[重大な変更] `oms` コマンド グループ名を `monitor` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-291">[BREAKING CHANGE] Changed `oms` command group name to `monitor`</span></span>
* <span data-ttu-id="7c209-292">[重大な変更] `--http-password/-p` が必須パラメーターになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-292">[BREAKING CHANGE] Made `--http-password/-p` a required parameter</span></span> 
* <span data-ttu-id="7c209-293">`--cluster-admin-account` および `cluster-users-group-dns` パラメーター入力候補の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-293">Added completers for `--cluster-admin-account` and `cluster-users-group-dns` parameters completer</span></span> 
* <span data-ttu-id="7c209-294">`cluster-users-group-dns` パラメーターを `—esp` が存在するときに必要となるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-294">Changed `cluster-users-group-dns` parameter to be required when `—esp` is present</span></span>
* <span data-ttu-id="7c209-295">既存の引数自動オートコンプリートすべてにタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-295">Added a timeout for all existing argument auto-completers</span></span>
* <span data-ttu-id="7c209-296">リソース名をリソース id に変換する際のタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-296">Added a timeout for transforming resource name to resource id</span></span>
* <span data-ttu-id="7c209-297">任意のリソース グループからリソースを選択するようにオートコンプリートを変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-297">Changed Auto-completers to select resources from any resource group.</span></span> <span data-ttu-id="7c209-298">`-g` で指定されるリソース グループとは別のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="7c209-298">It can be a different resource group than the one specified with `-g`</span></span>
* <span data-ttu-id="7c209-299">`hdinsight application create` コマンドで `--sub-domain-suffix` および `--disable_gateway_auth` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-299">Added support for `--sub-domain-suffix` and `--disable_gateway_auth` parameters in the `hdinsight application create` command</span></span>

### <a name="managed-services"></a><span data-ttu-id="7c209-300">マネージド サービス</span><span class="sxs-lookup"><span data-stu-id="7c209-300">Managed Services</span></span>

* <span data-ttu-id="7c209-301">プレビューにマネージド サービス コマンド モジュールを導入</span><span class="sxs-lookup"><span data-stu-id="7c209-301">Introducing managed service command module in preview</span></span>

### <a name="profile"></a><span data-ttu-id="7c209-302">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-302">Profile</span></span>
* <span data-ttu-id="7c209-303">ログアウト コマンドの `--subscription` 引数を抑制</span><span class="sxs-lookup"><span data-stu-id="7c209-303">Suppress `--subscription` argument for logout command</span></span>

### <a name="rbac"></a><span data-ttu-id="7c209-304">RBAC</span><span class="sxs-lookup"><span data-stu-id="7c209-304">RBAC</span></span>

* <span data-ttu-id="7c209-305">[重大な変更] `create-for-rbac` の `--password` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-305">[BREAKING CHANGE] Removed `--password` argument for `create-for-rbac`</span></span>
* <span data-ttu-id="7c209-306">AAD グラフ サーバー レプリケーションの待機時間によって発生する断続的なエラーを回避するために `--assignee-principal-type` パラメーターを `create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-306">Added `--assignee-principal-type` parameter to `create` command to avoid intermittent failures caused by AAD graph server replication latency</span></span>
* <span data-ttu-id="7c209-307">所有オブジェクトの一覧表示時の `ad signed-in-user` のクラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-307">Fixed a crash in `ad signed-in-user` when listing owned objects</span></span>
* <span data-ttu-id="7c209-308">`ad sp` によってサービス プリンシパルから適切なアプリケーションが検出されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-308">Fixed issue where `ad sp` would not find the right application from a service principal</span></span>

### <a name="rdbms"></a><span data-ttu-id="7c209-309">RDBMS</span><span class="sxs-lookup"><span data-stu-id="7c209-309">RDBMS</span></span>

* <span data-ttu-id="7c209-310">MariaDB のレプリケーション サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-310">Added support for replication for MariaDB</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-311">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-311">SQL</span></span>

* <span data-ttu-id="7c209-312">`sql db create --sample-name` に使用できる値を文書化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-312">Documented allowed values for `sql db create --sample-name`</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-313">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-313">Storage</span></span>

* <span data-ttu-id="7c209-314">`--as-user` を使用した `storage blob generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-314">Added user delegation SAS token support with `--as-user` to `storage blob generate-sas`</span></span> 
* <span data-ttu-id="7c209-315">`--as-user` を使用した `storage container generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-315">Added user delegation SAS token support with `--as-user` to `storage container generate-sas`</span></span> 

### <a name="vm"></a><span data-ttu-id="7c209-316">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-316">VM</span></span>

* <span data-ttu-id="7c209-317">`--no-wait` による実行時に `vmss create` によってエラー メッセージが返されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-317">Fixed bug where `vmss create` returns an error message when run with `--no-wait`</span></span>
* <span data-ttu-id="7c209-318">`vmss create --single-placement-group` のクライアント側の検証を削除しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-318">Removed client-side validation for `vmss create --single-placement-group`.</span></span> <span data-ttu-id="7c209-319">`--single-placement-group` が `true` に設定され、`--instance-count` が 100 より大きいか、可用性ゾーンが指定されていても失敗にはならず、この検証はコンピューティング サービスに任されます</span><span class="sxs-lookup"><span data-stu-id="7c209-319">Does not fail if `--single-placement-group` is set to `true` and`--instance-count` is greater than 100 or availability zones are specified, but leaves this validation to the compute service</span></span>
* <span data-ttu-id="7c209-320">`--latest` と共に使用したときに `[vm|vmss] extension image list` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-320">Fixed bug where `[vm|vmss] extension image list` fails when used with `--latest`</span></span>


## <a name="june-18-2019"></a><span data-ttu-id="7c209-321">2019 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="7c209-321">June 18, 2019</span></span>

<span data-ttu-id="7c209-322">バージョン 2.0.67</span><span class="sxs-lookup"><span data-stu-id="7c209-322">Version 2.0.67</span></span>

### <a name="core"></a><span data-ttu-id="7c209-323">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-323">Core</span></span>

<span data-ttu-id="7c209-324">このリリースでは、新しい [プレビュー] タグが導入され、コマンド グループ、コマンド、または引数がプレビュー状態である場合に、お客様により明確に通知できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="7c209-324">This release introduces a new [Preview] tag to more clearly communicate to customers when a command group, command or argument is in preview status.</span></span> <span data-ttu-id="7c209-325">以前は、これはヘルプ テキストで通知されていたか、コマンド モジュールのバージョン番号によって暗黙的に通知されていました。</span><span class="sxs-lookup"><span data-stu-id="7c209-325">This was previously called out in help text or communicated implicitly by the command module version number.</span></span>
<span data-ttu-id="7c209-326">CLI では、将来、個々のパッケージのバージョン番号が削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="7c209-326">The CLI will be removing version numbers for individual packages in the future.</span></span> <span data-ttu-id="7c209-327">コマンドがプレビュー状態の場合は、そのすべての引数もプレビュー状態です。</span><span class="sxs-lookup"><span data-stu-id="7c209-327">If a command is in preview, all of its arguments are as well.</span></span> <span data-ttu-id="7c209-328">コマンド グループにプレビュー状態のラベルが付いている場合、すべてのコマンドと引数もプレビュー状態と見なされます。</span><span class="sxs-lookup"><span data-stu-id="7c209-328">If a command group is labeled as being in preview, then all commands and arguments are considered to be in preview as well.</span></span>

<span data-ttu-id="7c209-329">この変更の結果、このリリースでは、一部のコマンド グループが "突然" プレビュー状態になったように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="7c209-329">As a result of this change, several command groups may seem to "suddenly" appear to be in a preview status with this release.</span></span> <span data-ttu-id="7c209-330">ほとんどのパッケージがプレビュー状態にあったのですが、このリリースでは一般提供と見なされていることがその真相です</span><span class="sxs-lookup"><span data-stu-id="7c209-330">What actually happened is that most packages were in a preview status, but are being deemed GA with this release</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-331">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-331">ACR</span></span>
* <span data-ttu-id="7c209-332">'acr check-health' コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-332">Added 'acr check-health' command</span></span>
* <span data-ttu-id="7c209-333">AAD トークンおよび外部コマンドの取得に関するエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-333">Improved error handling for AAD tokens and for retrieving external commands</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-334">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-334">ACS</span></span>
* <span data-ttu-id="7c209-335">非推奨の ACS コマンドがヘルプ ビューで非表示になりました</span><span class="sxs-lookup"><span data-stu-id="7c209-335">Deprecated ACS commands are now hidden from help view</span></span>

### <a name="ams"></a><span data-ttu-id="7c209-336">AMS</span><span class="sxs-lookup"><span data-stu-id="7c209-336">AMS</span></span>
* <span data-ttu-id="7c209-337">[重大な変更] archive-window-length および key-frame-interval-duration の ISO 8601 時間文字列を返すように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-337">[BREAKING CHANGE] Changed to return ISO 8601 time strings for archive-window-length and key-frame-interval-duration</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-338">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-338">AppService</span></span>
* <span data-ttu-id="7c209-339">`webapp deleted list` および `webapp deleted restore` に対してロケーション ベースのルーティングを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-339">Added location based routing for `webapp deleted list` and `webapp deleted restore`</span></span>
* <span data-ttu-id="7c209-340">Azure Cloud Shell で Web アプリのログに記録されたターゲット URL ("You can launch the app at...") がクリックできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-340">Fixed issue where webapp up logged target URL ("You can launch the app at...") was not clickable in Azure Cloud Shell</span></span>
* <span data-ttu-id="7c209-341">一部の SKU でのアプリ作成が AlwaysOn エラーで失敗するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-341">Fixed an issue where creating apps with the some SKUs was failing with an AlwaysOn error</span></span>
* <span data-ttu-id="7c209-342">`[appservice|webapp] create` に事前検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-342">Added pre-validation to `[appservice|webapp] create`</span></span>
* <span data-ttu-id="7c209-343">正しい actionHostName を使用するように `[webapp|functionapp] traffic-routing` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-343">Fixed `[webapp|functionapp] traffic-routing` to use the correct actionHostName</span></span>
* <span data-ttu-id="7c209-344">`functionapp` コマンドにスロット サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-344">Added slot support to `functionapp` commands</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-345">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-345">Batch</span></span>
* <span data-ttu-id="7c209-346">共有キー認証の過度のエラー報告による AAD 認証の回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-346">Fixed AAD auth regression caused by over-aggressive error reporting for Shared Key Auth</span></span>

### <a name="batchai"></a><span data-ttu-id="7c209-347">BatchAI</span><span class="sxs-lookup"><span data-stu-id="7c209-347">BatchAI</span></span>
* <span data-ttu-id="7c209-348">BatchAI コマンドが非推奨となり、非表示になりました</span><span class="sxs-lookup"><span data-stu-id="7c209-348">BatchAI commands are now deprecated and hidden</span></span>

### <a name="botservice"></a><span data-ttu-id="7c209-349">BotService</span><span class="sxs-lookup"><span data-stu-id="7c209-349">BotService</span></span>
* <span data-ttu-id="7c209-350">v3 SDK をサポートするコマンドに "廃止されたサポート"/"保守モード" 警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-350">Added "discontinued support"/"maintenance mode" warning messages for commands that support the v3 SDK</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="7c209-351">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="7c209-351">CosmosDB</span></span>
* <span data-ttu-id="7c209-352">[非推奨] `cosmosdb list-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-352">[DEPRECATED] Deprecated the `cosmosdb list-keys` command</span></span>
* <span data-ttu-id="7c209-353">`cosmosdb keys list` コマンドを追加しました。`cosmosdb list-keys` に置き換わるものです</span><span class="sxs-lookup"><span data-stu-id="7c209-353">Added the `cosmosdb keys list` command - replaces `cosmosdb list-keys`</span></span>
* <span data-ttu-id="7c209-354">`cosmsodb create/update`:"isZoneRedundant" プロパティを設定できるように --location の新しいフォーマットを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-354">`cosmsodb create/update`: Added new format for --location to allow setting "isZoneRedundant" property.</span></span> <span data-ttu-id="7c209-355">古いフォーマットを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-355">Deprecated old format</span></span>

### <a name="eventgrid"></a><span data-ttu-id="7c209-356">EventGrid</span><span class="sxs-lookup"><span data-stu-id="7c209-356">EventGrid</span></span>
* <span data-ttu-id="7c209-357">ドメイン CRUD 操作のための `eventgrid domain` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-357">Added `eventgrid domain` commands for domain CRUD operations</span></span>
* <span data-ttu-id="7c209-358">ドメイン トピック CRUD 操作のための `eventgrid domain topic` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-358">Added `eventgrid domain topic` commands for domain topics CRUD operations</span></span>
* <span data-ttu-id="7c209-359">OData 構文を使用して結果をフィルタリングするための `--odata-query` 引数を `eventgrid [topic|event-subscription] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-359">Added `--odata-query` argument to `eventgrid [topic|event-subscription] list` for filtering results using OData syntax</span></span>
* <span data-ttu-id="7c209-360">`event-subscription create/update`:`--endpoint-type` パラメーターの新しい値として servicebusqueue を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-360">`event-subscription create/update`: Added servicebusqueue as new values for the `--endpoint-type` parameter</span></span>
* <span data-ttu-id="7c209-361">[重大な変更] `eventgrid event-subscription [create|update]` での `--included-event-types All` のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-361">[BREAKING CHANGE] Removed support for `--included-event-types All` with `eventgrid event-subscription [create|update]`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="7c209-362">HDInsight</span><span class="sxs-lookup"><span data-stu-id="7c209-362">HDInsight</span></span>
* <span data-ttu-id="7c209-363">`hdinsight create` コマンドでの `--ssh-public-key` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-363">Added support for `--ssh-public-key` parameter in `hdinsight create` command</span></span>

### <a name="iot"></a><span data-ttu-id="7c209-364">IoT</span><span class="sxs-lookup"><span data-stu-id="7c209-364">IoT</span></span>
* <span data-ttu-id="7c209-365">承認ポリシー キーの再生成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-365">Added support to regenerate authorization policy keys</span></span>
* <span data-ttu-id="7c209-366">DigitalTwin リポジトリ プロビジョニング サービスの SDK およびサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-366">Added SDK and support for DigitalTwin Repository Provisioning Service</span></span>

### <a name="network"></a><span data-ttu-id="7c209-367">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-367">Network</span></span>
* <span data-ttu-id="7c209-368">Nat Gateway に対するゾーン サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-368">Added Zone support for Nat Gateway</span></span>
* <span data-ttu-id="7c209-369">`network list-service-tags` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-369">Added command `network list-service-tags`</span></span>
* <span data-ttu-id="7c209-370">ユーザーがワイルドカード A レコードをインポートできない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-370">Fixed issue with `dns zone import` where users could not import wildcard A records</span></span>
* <span data-ttu-id="7c209-371">特定のリージョンでフロー ロギングを有効にできない `watcher flow-log configure` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-371">Fixed issue with `watcher flow-log configure` where flow logging could not be enabled in certain regions</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-372">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-372">Resource</span></span>
* <span data-ttu-id="7c209-373">REST 呼び出しを行うための `az rest` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-373">Added `az rest` command for making REST calls</span></span>
* <span data-ttu-id="7c209-374">リソース グループまたはサブスクリプション レベル`--scope` で `policy assignment list` を使用する場合のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-374">Fixed error when using `policy assignment list` with a resource group or subscription level `--scope`</span></span>

### <a name="servicebus"></a><span data-ttu-id="7c209-375">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7c209-375">ServiceBus</span></span>
* <span data-ttu-id="7c209-376">`servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319) での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-376">Fixed issue with `servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319)</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-377">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-377">SQL</span></span>
* <span data-ttu-id="7c209-378">`--location` を `sql [server|mi] create` のオプションに変更しました - 指定されていない場合、リソース グループの場所を使用します</span><span class="sxs-lookup"><span data-stu-id="7c209-378">Changed `--location` to be optional for `sql [server|mi] create` - uses resource group location if not specified</span></span>
* <span data-ttu-id="7c209-379">`sql db list-editions --available` の "'NoneType' object is not iterable" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-379">Fixed "'NoneType' object is not iterable" error for `sql db list-editions --available`</span></span>

### <a name="sqlvm"></a><span data-ttu-id="7c209-380">SQLVm</span><span class="sxs-lookup"><span data-stu-id="7c209-380">SQLVm</span></span>
* <span data-ttu-id="7c209-381">[破壊的変更] `--license-type` パラメーターを必要とするように `sql vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-381">[BREAKING CHNAGE] Changed `sql vm create` to require `--license-type` parameter</span></span>
* <span data-ttu-id="7c209-382">sql vm の作成または更新時に SQL イメージ SKU を設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-382">Changed to allow setting SQL image SKU when creating or updating a sql vm</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-383">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-383">Storage</span></span>
* <span data-ttu-id="7c209-384">`storage container generate-sas` のアカウント キーが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-384">Fixed issue with missing account key for `storage container generate-sas`</span></span>
* <span data-ttu-id="7c209-385">Linux での `storage blob sync` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-385">Fixed issue with `storage blob sync` on Linux</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-386">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-386">VM</span></span>
* <span data-ttu-id="7c209-387">[プレビュー] VM イメージを構築するための `vm image template` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-387">[PREVIEW] Added `vm image template` commands to build VM images</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="7c209-388">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="7c209-388">June 4, 2019</span></span>

<span data-ttu-id="7c209-389">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="7c209-389">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="7c209-390">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-390">Core</span></span>
* <span data-ttu-id="7c209-391">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-391">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-392">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-392">ACR</span></span>
* <span data-ttu-id="7c209-393">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-393">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-394">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-394">ACS</span></span>
* <span data-ttu-id="7c209-395">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-395">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="7c209-396">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="7c209-396">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-397">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-397">Batch</span></span>
* <span data-ttu-id="7c209-398">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-398">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="7c209-399">IoT</span><span class="sxs-lookup"><span data-stu-id="7c209-399">IoT</span></span>
* <span data-ttu-id="7c209-400">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-400">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="7c209-401">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-401">Network</span></span>
* <span data-ttu-id="7c209-402">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-402">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="7c209-403">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-403">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="7c209-404">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-404">Resource</span></span>
* <span data-ttu-id="7c209-405">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-405">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="7c209-406">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-406">Role</span></span>
* <span data-ttu-id="7c209-407">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-407">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="7c209-408">Compute</span><span class="sxs-lookup"><span data-stu-id="7c209-408">Compute</span></span>
* <span data-ttu-id="7c209-409">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-409">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="7c209-410">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="7c209-410">May 21, 2019</span></span>

<span data-ttu-id="7c209-411">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="7c209-411">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="7c209-412">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-412">Core</span></span>
* <span data-ttu-id="7c209-413">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-413">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="7c209-414">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-414">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="7c209-415">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-415">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-416">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-416">ACR</span></span>
* <span data-ttu-id="7c209-417">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-417">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-418">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-418">ACS</span></span>
* <span data-ttu-id="7c209-419">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-419">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-420">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-420">AppService</span></span>
* <span data-ttu-id="7c209-421">[非推奨] `functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="7c209-421">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="7c209-422">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-422">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="7c209-423">[重大な変更] `--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="7c209-423">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="7c209-424">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-424">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="7c209-425">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-425">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="7c209-426">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-426">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="7c209-427">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-427">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="7c209-428">BotService</span><span class="sxs-lookup"><span data-stu-id="7c209-428">BotService</span></span>
* <span data-ttu-id="7c209-429">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-429">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="7c209-430">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-430">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="7c209-431">消費</span><span class="sxs-lookup"><span data-stu-id="7c209-431">Consumption</span></span>
* <span data-ttu-id="7c209-432">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-432">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="7c209-433">IoT</span><span class="sxs-lookup"><span data-stu-id="7c209-433">IoT</span></span>
* <span data-ttu-id="7c209-434">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-434">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="7c209-435">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-435">Network</span></span>
* [重大な変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="7c209-437">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-437">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="7c209-438">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-438">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="7c209-439">RDBMS</span><span class="sxs-lookup"><span data-stu-id="7c209-439">RDBMS</span></span>
* <span data-ttu-id="7c209-440">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-440">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="7c209-441">RBAC</span><span class="sxs-lookup"><span data-stu-id="7c209-441">RBAC</span></span>
* <span data-ttu-id="7c209-442">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-442">Added support for mangement group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-443">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-443">Storage</span></span>
* <span data-ttu-id="7c209-444">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="7c209-444">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="7c209-445">Compute</span><span class="sxs-lookup"><span data-stu-id="7c209-445">Compute</span></span>
* <span data-ttu-id="7c209-446">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-446">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="7c209-447">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-447">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="7c209-448">__メモ__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="7c209-448">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="7c209-449">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-449">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="7c209-450">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="7c209-450">May 6, 2019</span></span>

<span data-ttu-id="7c209-451">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="7c209-451">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-452">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-452">ACS</span></span>
* <span data-ttu-id="7c209-453">[重大な変更] `--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-453">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="7c209-454">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-454">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="7c209-455">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-455">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="7c209-456">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-456">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-457">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-457">Appservice</span></span>
* <span data-ttu-id="7c209-458">[非推奨] `functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-458">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="7c209-459">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-459">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="7c209-460">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="7c209-460">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="7c209-461">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-461">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="7c209-462">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-462">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="7c209-463">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-463">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="7c209-464">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-464">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="7c209-465">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-465">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="7c209-466">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-466">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="7c209-467">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-467">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-468">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-468">Batch</span></span>
* <span data-ttu-id="7c209-469">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-469">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="7c209-470">Botservice</span><span class="sxs-lookup"><span data-stu-id="7c209-470">Botservice</span></span>
* <span data-ttu-id="7c209-471">[重大な変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="7c209-471">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="7c209-472">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-472">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="7c209-473">[重大な変更] `--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-473">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="7c209-474">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="7c209-474">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="7c209-475">[重大な変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-475">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="7c209-476">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="7c209-476">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="7c209-477">[重大な変更] `bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-477">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="7c209-478">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-478">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="7c209-479">[重大な変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-479">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="7c209-480">[重大な変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-480">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="7c209-481">[重大な変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-481">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="7c209-482">[重大な変更] `Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-482">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="7c209-483">[重大な変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-483">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="7c209-484">[重大な変更] `SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-484">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="7c209-485">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="7c209-485">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="7c209-486">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-486">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="7c209-487">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-487">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="7c209-488">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-488">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="7c209-489">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-489">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="7c209-490">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-490">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="7c209-491">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-491">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="7c209-492">構成</span><span class="sxs-lookup"><span data-stu-id="7c209-492">Configure</span></span>
* <span data-ttu-id="7c209-493">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-493">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="7c209-494">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="7c209-494">Eventhubs</span></span>
* <span data-ttu-id="7c209-495">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-495">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="7c209-496">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-496">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="7c209-497">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-497">Network</span></span>
* <span data-ttu-id="7c209-498">[重大な変更] `vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="7c209-498">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="7c209-499">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="7c209-499">Policy Insights</span></span>
* <span data-ttu-id="7c209-500">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-500">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="7c209-501">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-501">Role</span></span>
* <span data-ttu-id="7c209-502">[非推奨] `create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="7c209-502">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="7c209-503">Service Bus</span><span class="sxs-lookup"><span data-stu-id="7c209-503">Service Bus</span></span>
* <span data-ttu-id="7c209-504">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-504">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="7c209-505">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-505">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="7c209-506">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-506">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-507">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-507">SQL</span></span>
* <span data-ttu-id="7c209-508">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-508">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-509">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-509">VM</span></span>
* <span data-ttu-id="7c209-510">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-510">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="7c209-511">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-511">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="7c209-512">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-512">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="7c209-513">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-513">Added new `ppg` command group for manging Proximity Placement Groups</span></span>
* <span data-ttu-id="7c209-514">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-514">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="7c209-515">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-515">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="7c209-516">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="7c209-516">April 23, 2019</span></span>

<span data-ttu-id="7c209-517">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="7c209-517">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-518">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-518">ACS</span></span>
* <span data-ttu-id="7c209-519">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-519">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="7c209-520">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-520">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="7c209-521">AMS</span><span class="sxs-lookup"><span data-stu-id="7c209-521">AMS</span></span>
* <span data-ttu-id="7c209-522">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-522">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-523">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-523">AppService</span></span>
* <span data-ttu-id="7c209-524">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-524">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="7c209-525">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-525">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="7c209-526">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-526">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="7c209-527">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-527">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="7c209-528">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-528">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="7c209-529">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-529">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="7c209-530">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-530">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="7c209-531">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-531">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="7c209-532">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-532">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="7c209-533">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="7c209-533">Deployment Manager</span></span>
* <span data-ttu-id="7c209-534">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="7c209-534">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="7c209-535">ラボ</span><span class="sxs-lookup"><span data-stu-id="7c209-535">Lab</span></span>
* <span data-ttu-id="7c209-536">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-536">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="7c209-537">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-537">Network</span></span>
* <span data-ttu-id="7c209-538">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-538">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-539">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-539">Resource</span></span>
* <span data-ttu-id="7c209-540">[非推奨] `resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="7c209-540">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="7c209-541">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="7c209-541">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="7c209-542">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-542">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="7c209-543">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-543">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-544">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-544">SQL</span></span>
* <span data-ttu-id="7c209-545">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-545">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="7c209-546">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-546">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="7c209-547">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-547">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="7c209-548">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-548">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-549">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-549">Storage</span></span>
* <span data-ttu-id="7c209-550">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-550">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-551">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-551">VM</span></span>
* <span data-ttu-id="7c209-552">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-552">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="7c209-553">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-553">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="7c209-554">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-554">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="7c209-555">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="7c209-555">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="7c209-556">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-556">Core</span></span>
* <span data-ttu-id="7c209-557">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-557">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-558">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-558">ACR</span></span>
* <span data-ttu-id="7c209-559">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-559">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="7c209-560">AMS</span><span class="sxs-lookup"><span data-stu-id="7c209-560">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="7c209-563">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-563">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="7c209-564">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-564">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-565">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-565">AppService</span></span>
* <span data-ttu-id="7c209-566">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-566">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="7c209-567">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-567">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="7c209-568">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-568">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="7c209-569">[重大な変更] `devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="7c209-569">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="7c209-570">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-570">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="7c209-571">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-571">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="7c209-572">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-572">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="7c209-573">CDN</span><span class="sxs-lookup"><span data-stu-id="7c209-573">CDN</span></span>
* <span data-ttu-id="7c209-574">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-574">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="7c209-575">フィードバック</span><span class="sxs-lookup"><span data-stu-id="7c209-575">Feedback</span></span>
* <span data-ttu-id="7c209-576">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-576">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="7c209-577">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-577">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="7c209-578">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-578">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-579">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-579">Monitor</span></span>
* <span data-ttu-id="7c209-580">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-580">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="7c209-581">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-581">Network</span></span>
* <span data-ttu-id="7c209-582">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-582">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="7c209-583">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-583">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="7c209-584">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-584">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="7c209-585">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-585">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="7c209-586">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="7c209-586">PrivateDNS</span></span>
* <span data-ttu-id="7c209-587">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-587">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-588">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-588">Resource</span></span>
* <span data-ttu-id="7c209-589">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-589">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="7c209-590">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-590">Role</span></span>
* <span data-ttu-id="7c209-591">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-591">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="7c209-592">[重大な変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-592">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-593">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-593">SQL</span></span>
* <span data-ttu-id="7c209-594">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-594">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-595">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-595">Storage</span></span>
* <span data-ttu-id="7c209-596">[重大な変更] `storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-596">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="7c209-597">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-597">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="7c209-598">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-598">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="7c209-599">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-599">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="7c209-600">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="7c209-600">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="7c209-601">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-601">Core</span></span>
* <span data-ttu-id="7c209-602">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-602">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="7c209-603">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-603">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="7c209-604">クラウド</span><span class="sxs-lookup"><span data-stu-id="7c209-604">Cloud</span></span>
* <span data-ttu-id="7c209-605">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-605">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-606">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-606">ACR</span></span>
* <span data-ttu-id="7c209-607">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-607">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="7c209-608">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-608">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="7c209-609">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-609">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="7c209-610">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-610">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-611">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-611">AppService</span></span>
* <span data-ttu-id="7c209-612">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-612">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="7c209-613">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-613">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="7c209-614">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="7c209-614">BOT Service</span></span>
* <span data-ttu-id="7c209-615">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-615">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="7c209-616">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-616">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="7c209-617">[重大な変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-617">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="7c209-618">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-618">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="7c209-619">CDN</span><span class="sxs-lookup"><span data-stu-id="7c209-619">CDN</span></span>
* <span data-ttu-id="7c209-620">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-620">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [重大な変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="7c209-622">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="7c209-622">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="7c209-623">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-623">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="7c209-624">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="7c209-624">Cosmosdb</span></span>
* <span data-ttu-id="7c209-625">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-625">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="7c209-626">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-626">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="7c209-627">Interactive</span><span class="sxs-lookup"><span data-stu-id="7c209-627">Interactive</span></span>
* <span data-ttu-id="7c209-628">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-628">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-629">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-629">Monitor</span></span>
* <span data-ttu-id="7c209-630">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-630">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="7c209-631">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-631">Network</span></span>
* <span data-ttu-id="7c209-632">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-632">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="7c209-633">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-633">Profile</span></span>
* <span data-ttu-id="7c209-634">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-634">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="7c209-635">Postgres</span><span class="sxs-lookup"><span data-stu-id="7c209-635">Postgres</span></span> 
* <span data-ttu-id="7c209-636">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-636">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="7c209-637">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="7c209-637">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-638">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-638">Resource</span></span>
* <span data-ttu-id="7c209-639">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-639">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="7c209-640">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-640">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="7c209-641">Graph</span><span class="sxs-lookup"><span data-stu-id="7c209-641">Graph</span></span>
* <span data-ttu-id="7c209-642">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-642">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="7c209-643">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-643">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="7c209-644">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-644">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="7c209-645">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-645">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="7c209-646">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-646">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-647">storage</span><span class="sxs-lookup"><span data-stu-id="7c209-647">storage</span></span>
* <span data-ttu-id="7c209-648">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-648">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="7c209-649">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-649">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="7c209-650">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-650">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="7c209-651">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-651">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-652">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-652">VM</span></span>
* <span data-ttu-id="7c209-653">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-653">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="7c209-654">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="7c209-654">March 12, 2019</span></span>

<span data-ttu-id="7c209-655">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="7c209-655">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="7c209-656">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-656">Core</span></span>

* <span data-ttu-id="7c209-657">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-657">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-658">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-658">ACR</span></span>

* <span data-ttu-id="7c209-659">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-659">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-660">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-660">ACS</span></span>

* <span data-ttu-id="7c209-661">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-661">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="7c209-662">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-662">AppService</span></span>

* <span data-ttu-id="7c209-663">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-663">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="7c209-664">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-664">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="7c209-665">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-665">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="7c209-666">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-666">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="7c209-667">Botservice</span><span class="sxs-lookup"><span data-stu-id="7c209-667">Botservice</span></span>

* <span data-ttu-id="7c209-668">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-668">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="7c209-669">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-669">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="7c209-670">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-670">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="7c209-671">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-671">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="7c209-672">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-672">Container</span></span>

* <span data-ttu-id="7c209-673">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-673">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="7c209-674">EventHub</span><span class="sxs-lookup"><span data-stu-id="7c209-674">EventHub</span></span>

* <span data-ttu-id="7c209-675">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-675">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="7c209-676">Find</span><span class="sxs-lookup"><span data-stu-id="7c209-676">Find</span></span>

* <span data-ttu-id="7c209-677">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="7c209-677">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="7c209-678">HDInsight</span><span class="sxs-lookup"><span data-stu-id="7c209-678">HDInsight</span></span>

* <span data-ttu-id="7c209-679">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-679">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="7c209-680">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-680">Network</span></span>

* <span data-ttu-id="7c209-681">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-681">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="7c209-682">Rdbms</span><span class="sxs-lookup"><span data-stu-id="7c209-682">Rdbms</span></span>

* <span data-ttu-id="7c209-683">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="7c209-683">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="7c209-684">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-684">Role</span></span>

* <span data-ttu-id="7c209-685">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-685">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="7c209-686">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-686">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="7c209-687">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7c209-687">Service Fabric</span></span>

* <span data-ttu-id="7c209-688">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-688">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="7c209-689">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="7c209-689">February 26, 2019</span></span>

<span data-ttu-id="7c209-690">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="7c209-690">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="7c209-691">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-691">Core</span></span>

* <span data-ttu-id="7c209-692">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-692">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-693">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-693">ACR</span></span>

* <span data-ttu-id="7c209-694">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-694">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="7c209-695">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-695">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-696">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-696">ACS</span></span>

* <span data-ttu-id="7c209-697">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-697">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-698">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-698">AppService</span></span>

* <span data-ttu-id="7c209-699">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-699">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-700">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-700">Batch</span></span>
* <span data-ttu-id="7c209-701">[重大な変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-701">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="7c209-702">[重大な変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-702">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="7c209-703">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-703">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="7c209-704">[重大な変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-704">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="7c209-705">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-705">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="7c209-706">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="7c209-706">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="7c209-707">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="7c209-707">CosmosDB</span></span>

* <span data-ttu-id="7c209-708">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-708">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="7c209-709">Kusto</span><span class="sxs-lookup"><span data-stu-id="7c209-709">Kusto</span></span>

* <span data-ttu-id="7c209-710">[重大な変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-710">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="7c209-711">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-711">Network</span></span>

* <span data-ttu-id="7c209-712">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-712">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="7c209-713">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-713">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="7c209-714">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-714">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="7c209-715">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-715">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="7c209-716">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-716">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="7c209-717">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-717">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="7c209-718">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-718">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-719">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-719">Resource</span></span>

* <span data-ttu-id="7c209-720">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-720">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="7c209-721">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-721">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="7c209-722">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-722">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="7c209-723">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-723">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="7c209-724">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-724">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="7c209-725">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-725">Role</span></span>

* <span data-ttu-id="7c209-726">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-726">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-727">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-727">VM</span></span>

* <span data-ttu-id="7c209-728">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-728">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="7c209-729">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="7c209-729">February 12, 2019</span></span>

<span data-ttu-id="7c209-730">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="7c209-730">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="7c209-731">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-731">Core</span></span>

* <span data-ttu-id="7c209-732">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-732">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="7c209-733">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-733">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-734">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-734">ACR</span></span>
* <span data-ttu-id="7c209-735">[重大な変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-735">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="7c209-736">[重大な変更] `acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-736">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-737">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-737">ACS</span></span>
* <span data-ttu-id="7c209-738">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-738">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="7c209-739">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-739">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="7c209-740">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-740">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="7c209-741">AMS</span><span class="sxs-lookup"><span data-stu-id="7c209-741">AMS</span></span>
* <span data-ttu-id="7c209-742">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-742">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="7c209-743">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-743">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-744">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-744">Appservice</span></span>
* <span data-ttu-id="7c209-745">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-745">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="7c209-746">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-746">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="7c209-747">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-747">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="7c209-748">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-748">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="7c209-749">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-749">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="7c209-750">Botservice</span><span class="sxs-lookup"><span data-stu-id="7c209-750">Botservice</span></span>
* <span data-ttu-id="7c209-751">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-751">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="7c209-752">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-752">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="7c209-753">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-753">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="7c209-754">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-754">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="7c209-755">[非推奨] `--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-755">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="7c209-756">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-756">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="7c209-757">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-757">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="7c209-758">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-758">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="7c209-759">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="7c209-759">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="7c209-760">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-760">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="7c209-761">Key Vault</span><span class="sxs-lookup"><span data-stu-id="7c209-761">Key Vault</span></span>
* <span data-ttu-id="7c209-762">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-762">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-763">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-763">Monitor</span></span>
* <span data-ttu-id="7c209-764">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-764">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="7c209-765">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-765">Network</span></span>
* <span data-ttu-id="7c209-766">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-766">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="7c209-767">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-767">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="7c209-768">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-768">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="7c209-769">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-769">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="7c209-770">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="7c209-770">Policy Insights</span></span>
* <span data-ttu-id="7c209-771">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-771">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="7c209-772">RDBMS</span><span class="sxs-lookup"><span data-stu-id="7c209-772">RDBMS</span></span>
* <span data-ttu-id="7c209-773">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-773">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="7c209-774">Redis</span><span class="sxs-lookup"><span data-stu-id="7c209-774">Redis</span></span>
* <span data-ttu-id="7c209-775">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-775">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="7c209-776">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-776">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="7c209-777">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-777">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="7c209-778">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-778">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="7c209-779">[重大な変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-779">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="7c209-780">[重大な変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="7c209-780">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="7c209-781">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-781">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="7c209-782">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-782">Role</span></span>
* <span data-ttu-id="7c209-783">[重大な変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="7c209-783">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="7c209-784">SQL VM</span><span class="sxs-lookup"><span data-stu-id="7c209-784">SQL VM</span></span>
* <span data-ttu-id="7c209-785">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-785">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-786">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-786">VM</span></span>
* <span data-ttu-id="7c209-787">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-787">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="7c209-788">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-788">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="7c209-789">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-789">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="7c209-790">[重大な変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="7c209-790">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="7c209-791">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="7c209-791">January 31, 2019</span></span>

<span data-ttu-id="7c209-792">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="7c209-792">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="7c209-793">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-793">Core</span></span>

* <span data-ttu-id="7c209-794">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="7c209-794">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="7c209-795">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="7c209-795">January 28, 2019</span></span>

<span data-ttu-id="7c209-796">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="7c209-796">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-797">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-797">ACR</span></span>
* <span data-ttu-id="7c209-798">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-798">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-799">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-799">ACS</span></span>
* <span data-ttu-id="7c209-800">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-800">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="7c209-801">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-801">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="7c209-802">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-802">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="7c209-803">AMS</span><span class="sxs-lookup"><span data-stu-id="7c209-803">AMS</span></span>
* <span data-ttu-id="7c209-804">[重大な変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-804">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="7c209-805">[重大な変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-805">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-806">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-806">Appservice</span></span>
* <span data-ttu-id="7c209-807">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-807">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="7c209-808">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-808">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="7c209-809">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-809">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="7c209-810">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-810">Container</span></span>
* <span data-ttu-id="7c209-811">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-811">Added `container start` command</span></span>
* <span data-ttu-id="7c209-812">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-812">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="7c209-813">EventGrid</span><span class="sxs-lookup"><span data-stu-id="7c209-813">EventGrid</span></span>
* <span data-ttu-id="7c209-814">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-814">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="7c209-815">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-815">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="7c209-816">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-816">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="7c209-817">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-817">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="7c209-818">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="7c209-818">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="7c209-819">HDInsight</span><span class="sxs-lookup"><span data-stu-id="7c209-819">HDInsight</span></span>
* <span data-ttu-id="7c209-820">[重大な変更] `hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-820">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="7c209-821">[重大な変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-821">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="7c209-822">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-822">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="7c209-823">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-823">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="7c209-824">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-824">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="7c209-825">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-825">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="7c209-826">IoT</span><span class="sxs-lookup"><span data-stu-id="7c209-826">IoT</span></span>
* <span data-ttu-id="7c209-827">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-827">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="7c209-828">Kusto</span><span class="sxs-lookup"><span data-stu-id="7c209-828">Kusto</span></span>
* <span data-ttu-id="7c209-829">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="7c209-829">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-830">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-830">Monitor</span></span>
* <span data-ttu-id="7c209-831">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-831">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="7c209-832">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-832">Profile</span></span>
* <span data-ttu-id="7c209-833">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-833">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="7c209-834">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-834">Network</span></span>
* <span data-ttu-id="7c209-835">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-835">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="7c209-836">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-836">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-837">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-837">Resource</span></span>
* <span data-ttu-id="7c209-838">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-838">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="7c209-839">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-839">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="7c209-840">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="7c209-840">SQL Virtual Machine</span></span>
* <span data-ttu-id="7c209-841">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="7c209-841">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-842">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-842">Storage</span></span>
* <span data-ttu-id="7c209-843">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-843">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="7c209-844">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="7c209-844">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-845">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-845">VM</span></span>
* <span data-ttu-id="7c209-846">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-846">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="7c209-847">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-847">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="7c209-848">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="7c209-848">January 15, 2019</span></span>

<span data-ttu-id="7c209-849">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="7c209-849">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-850">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-850">ACR</span></span>
* <span data-ttu-id="7c209-851">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-851">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="7c209-852">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-852">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="7c209-853">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-853">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="7c209-854">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-854">ACS</span></span>
* <span data-ttu-id="7c209-855">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-855">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-856">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-856">Appservice</span></span>
* <span data-ttu-id="7c209-857">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-857">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="7c209-858">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-858">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="7c209-859">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-859">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="7c209-860">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-860">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="7c209-861">Botservice</span><span class="sxs-lookup"><span data-stu-id="7c209-861">Botservice</span></span>
* <span data-ttu-id="7c209-862">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-862">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="7c209-863">構成</span><span class="sxs-lookup"><span data-stu-id="7c209-863">Configure</span></span>
* <span data-ttu-id="7c209-864">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-864">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="7c209-865">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="7c209-865">CosmosDB</span></span>
* <span data-ttu-id="7c209-866">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-866">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="7c209-867">HDInsight</span><span class="sxs-lookup"><span data-stu-id="7c209-867">HDInsight</span></span>
* <span data-ttu-id="7c209-868">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-868">Added commands for managing applications</span></span>
* <span data-ttu-id="7c209-869">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-869">Added commands for managing script actions</span></span>
* <span data-ttu-id="7c209-870">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-870">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="7c209-871">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-871">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="7c209-872">[重大な変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-872">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="7c209-873">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-873">Network</span></span>
* <span data-ttu-id="7c209-874">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-874">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="7c209-875">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-875">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="7c209-876">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-876">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="7c209-877">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-877">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="7c209-878">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-878">Role</span></span>
* <span data-ttu-id="7c209-879">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="7c209-879">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="7c209-880">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="7c209-880">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="7c209-881">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="7c209-881">Security</span></span>
* <span data-ttu-id="7c209-882">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="7c209-882">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-883">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-883">Storage</span></span>
* <span data-ttu-id="7c209-884">[重大な変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-884">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="7c209-885">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="7c209-885">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="7c209-886">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-886">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="7c209-887">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-887">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="7c209-888">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-888">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-889">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-889">VM</span></span>
* <span data-ttu-id="7c209-890">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-890">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="7c209-891">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-891">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="7c209-892">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-892">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="7c209-893">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-893">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="7c209-894">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-894">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="7c209-895">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-895">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="7c209-896">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="7c209-896">December 20, 2018</span></span>

<span data-ttu-id="7c209-897">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="7c209-897">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="7c209-898">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-898">Appservice</span></span>
* <span data-ttu-id="7c209-899">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-899">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="7c209-900">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-900">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="7c209-901">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-901">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="7c209-902">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="7c209-902">IoTCentral</span></span>
* <span data-ttu-id="7c209-903">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-903">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="7c209-904">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-904">Role</span></span>
* <span data-ttu-id="7c209-905">[重大な変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-905">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-906">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-906">SQL</span></span>
* <span data-ttu-id="7c209-907">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-907">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-908">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-908">VM</span></span>
* <span data-ttu-id="7c209-909">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-909">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="7c209-910">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="7c209-910">December 18, 2018</span></span>

<span data-ttu-id="7c209-911">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="7c209-911">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="7c209-912">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-912">ACR</span></span>
* <span data-ttu-id="7c209-913">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-913">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="7c209-914">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="7c209-914">Condensed the table layout for task list</span></span>
* <span data-ttu-id="7c209-915">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-915">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-916">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-916">ACS</span></span>
* <span data-ttu-id="7c209-917">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-917">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="7c209-918">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-918">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="7c209-919">[非推奨] `az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="7c209-919">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="7c209-920">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="7c209-920">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="7c209-921">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-921">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="7c209-922">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-922">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-923">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-923">Appservice</span></span>
* <span data-ttu-id="7c209-924">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-924">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="7c209-925">Botservice</span><span class="sxs-lookup"><span data-stu-id="7c209-925">Botservice</span></span>
* <span data-ttu-id="7c209-926">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-926">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="7c209-927">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-927">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="7c209-928">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-928">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="7c209-929">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="7c209-929">Reduced Kudu network calls</span></span>
* <span data-ttu-id="7c209-930">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-930">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="7c209-931">消費</span><span class="sxs-lookup"><span data-stu-id="7c209-931">Consumption</span></span>
* <span data-ttu-id="7c209-932">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-932">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="7c209-933">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="7c209-933">CosmosDB</span></span>
* <span data-ttu-id="7c209-934">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-934">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="7c209-935">マップ</span><span class="sxs-lookup"><span data-stu-id="7c209-935">Maps</span></span>
* <span data-ttu-id="7c209-936">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-936">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="7c209-937">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-937">Network</span></span>
* <span data-ttu-id="7c209-938">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-938">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="7c209-939">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-939">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-940">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-940">Resource</span></span>
* <span data-ttu-id="7c209-941">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-941">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="7c209-942">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-942">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-943">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-943">Storage</span></span>
*  <span data-ttu-id="7c209-944">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-944">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-945">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-945">VM</span></span>
* <span data-ttu-id="7c209-946">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-946">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="7c209-947">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="7c209-947">December 4, 2018</span></span>

<span data-ttu-id="7c209-948">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="7c209-948">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="7c209-949">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-949">Core</span></span>
* <span data-ttu-id="7c209-950">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-950">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="7c209-951">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-951">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-952">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-952">Appservice</span></span>
* <span data-ttu-id="7c209-953">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-953">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="7c209-954">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-954">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="7c209-955">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-955">Network</span></span>
* <span data-ttu-id="7c209-956">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-956">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="7c209-957">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-957">Role</span></span>
* <span data-ttu-id="7c209-958">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-958">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="7c209-959">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-959">VM</span></span>
* <span data-ttu-id="7c209-960">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-960">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="7c209-961">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-961">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="7c209-962">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-962">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="7c209-963">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-963">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="7c209-964">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="7c209-964">November 20, 2018</span></span>

<span data-ttu-id="7c209-965">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="7c209-965">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="7c209-966">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-966">Core</span></span>
* <span data-ttu-id="7c209-967">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-967">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-968">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-968">ACR</span></span>
* <span data-ttu-id="7c209-969">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-969">Added context token to task step</span></span>
* <span data-ttu-id="7c209-970">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-970">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="7c209-971">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-971">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-972">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-972">Appservice</span></span>
* <span data-ttu-id="7c209-973">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-973">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="7c209-974">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-974">Updated the default `node_version`.</span></span> <span data-ttu-id="7c209-975">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="7c209-975">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="7c209-976">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-976">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="7c209-977">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-977">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="7c209-978">IotCentral</span><span class="sxs-lookup"><span data-stu-id="7c209-978">IotCentral</span></span>
* <span data-ttu-id="7c209-979">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-979">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="7c209-980">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c209-980">KeyVault</span></span>
* <span data-ttu-id="7c209-981">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-981">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="7c209-982">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-982">Network</span></span>
* <span data-ttu-id="7c209-983">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-983">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="7c209-984">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-984">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="7c209-985">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-985">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="7c209-986">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-986">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="7c209-987">Rdbms</span><span class="sxs-lookup"><span data-stu-id="7c209-987">Rdbms</span></span>
* <span data-ttu-id="7c209-988">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-988">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="7c209-989">Rbac</span><span class="sxs-lookup"><span data-stu-id="7c209-989">Rbac</span></span>
* <span data-ttu-id="7c209-990">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-990">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="7c209-991">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-991">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="7c209-992">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-992">Storage</span></span>
* <span data-ttu-id="7c209-993">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-993">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="7c209-994">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-994">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="7c209-995">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-995">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="7c209-996">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="7c209-996">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-997">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-997">VM</span></span>
* <span data-ttu-id="7c209-998">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-998">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="7c209-999">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-999">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="7c209-1000">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="7c209-1000">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="7c209-1001">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1001">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="7c209-1002">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1002">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="7c209-1003">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1003">Added `snapshot wait` command</span></span>
* <span data-ttu-id="7c209-1004">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1004">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="7c209-1005">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1005">November 6, 2018</span></span>

<span data-ttu-id="7c209-1006">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="7c209-1006">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1007">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1007">Core</span></span>
* <span data-ttu-id="7c209-1008">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1008">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-1009">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-1009">ACR</span></span>
* <span data-ttu-id="7c209-1010">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1010">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="7c209-1011">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1011">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1012">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1012">ACS</span></span>
* <span data-ttu-id="7c209-1013">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1013">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="7c209-1014">Advisor</span><span class="sxs-lookup"><span data-stu-id="7c209-1014">Advisor</span></span>
* <span data-ttu-id="7c209-1015">GA リリース</span><span class="sxs-lookup"><span data-stu-id="7c209-1015">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="7c209-1016">AMS</span><span class="sxs-lookup"><span data-stu-id="7c209-1016">AMS</span></span>
* <span data-ttu-id="7c209-1017">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1017">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="7c209-1018">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1018">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="7c209-1019">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1019">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="7c209-1020">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-1020">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="7c209-1021">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1021">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="7c209-1022">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1022">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="7c209-1023">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1023">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="7c209-1024">[重大な変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="7c209-1024">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="7c209-1025">[重大な変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1025">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="7c209-1026">[重大な変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1026">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="7c209-1027">[重大な変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="7c209-1027">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="7c209-1028">[重大な変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1028">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="7c209-1029">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="7c209-1029">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="7c209-1030">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="7c209-1030">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="7c209-1031">[重大な変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1031">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="7c209-1032">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1032">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="7c209-1033">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="7c209-1033">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1034">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-1034">AppService</span></span>
* <span data-ttu-id="7c209-1035">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1035">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="7c209-1036">構成</span><span class="sxs-lookup"><span data-stu-id="7c209-1036">Configure</span></span>
* <span data-ttu-id="7c209-1037">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1037">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="7c209-1038">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-1038">Container</span></span>
* <span data-ttu-id="7c209-1039">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1039">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="7c209-1040">EventHub</span><span class="sxs-lookup"><span data-stu-id="7c209-1040">EventHub</span></span>
* <span data-ttu-id="7c209-1041">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1041">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="7c209-1042">Interactive</span><span class="sxs-lookup"><span data-stu-id="7c209-1042">Interactive</span></span>
* <span data-ttu-id="7c209-1043">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="7c209-1043">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-1044">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-1044">Monitor</span></span>
* <span data-ttu-id="7c209-1045">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-1045">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1046">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1046">Network</span></span>
* <span data-ttu-id="7c209-1047">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1047">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="7c209-1048">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1048">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="7c209-1049">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1049">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="7c209-1050">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-1050">Profile</span></span>
* <span data-ttu-id="7c209-1051">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1051">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="7c209-1052">RDBMS</span><span class="sxs-lookup"><span data-stu-id="7c209-1052">RDBMS</span></span>
* <span data-ttu-id="7c209-1053">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1053">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-1054">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-1054">Resource</span></span>
* <span data-ttu-id="7c209-1055">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1055">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="7c209-1056">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-1056">Role</span></span>
* <span data-ttu-id="7c209-1057">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-1057">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="7c209-1058">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1058">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="7c209-1059">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1059">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1060">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1060">Storage</span></span>
* <span data-ttu-id="7c209-1061">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="7c209-1061">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1062">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1062">VM</span></span>
* <span data-ttu-id="7c209-1063">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1063">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="7c209-1064">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1064">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="7c209-1065">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1065">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="7c209-1066">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1066">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="7c209-1067">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="7c209-1067">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="7c209-1068">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1068">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="7c209-1069">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1069">October 23, 2018</span></span>

<span data-ttu-id="7c209-1070">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="7c209-1070">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1071">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1071">Core</span></span>
* <span data-ttu-id="7c209-1072">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1072">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="7c209-1073">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1073">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-1074">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-1074">ACR</span></span>
* <span data-ttu-id="7c209-1075">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1075">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="7c209-1076">CDN</span><span class="sxs-lookup"><span data-stu-id="7c209-1076">CDN</span></span>
* <span data-ttu-id="7c209-1077">[重大な変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1077">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="7c209-1078">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-1078">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="7c209-1079">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-1079">Container</span></span>
* <span data-ttu-id="7c209-1080">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1080">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="7c209-1081">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1081">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="7c209-1082">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1082">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="7c209-1083">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1083">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="7c209-1084">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1084">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="7c209-1085">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1085">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="7c209-1086">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1086">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="7c209-1087">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="7c209-1087">CosmosDB</span></span>
* <span data-ttu-id="7c209-1088">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1088">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="7c209-1089">Interactive</span><span class="sxs-lookup"><span data-stu-id="7c209-1089">Interactive</span></span>
* <span data-ttu-id="7c209-1090">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1090">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="7c209-1091">IoT Central</span><span class="sxs-lookup"><span data-stu-id="7c209-1091">IoT Central</span></span>
* <span data-ttu-id="7c209-1092">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1092">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="7c209-1093">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="7c209-1093">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-1094">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-1094">Monitor</span></span>
* <span data-ttu-id="7c209-1095">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="7c209-1095">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="7c209-1096">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1096">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="7c209-1097">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1097">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="7c209-1098">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1098">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="7c209-1099">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1099">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="7c209-1100">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1100">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="7c209-1101">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="7c209-1101">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="7c209-1102">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1102">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="7c209-1103">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1103">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="7c209-1104">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1104">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1105">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1105">Network</span></span>
* <span data-ttu-id="7c209-1106">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1106">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="7c209-1107">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1107">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="7c209-1108">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7c209-1108">ServiceBus</span></span>
* <span data-ttu-id="7c209-1109">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1109">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-1110">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-1110">SQL</span></span>
* <span data-ttu-id="7c209-1111">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1111">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1112">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1112">Storage</span></span>
* <span data-ttu-id="7c209-1113">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1113">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="7c209-1114">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1114">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1115">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1115">VM</span></span>
* <span data-ttu-id="7c209-1116">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="7c209-1116">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="7c209-1117">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1117">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="7c209-1118">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1118">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="7c209-1119">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1119">October 16, 2018</span></span>

<span data-ttu-id="7c209-1120">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="7c209-1120">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1121">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1121">VM</span></span>
* <span data-ttu-id="7c209-1122">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1122">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="7c209-1123">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1123">October 9, 2018</span></span>

<span data-ttu-id="7c209-1124">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="7c209-1124">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1125">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1125">Core</span></span>
* <span data-ttu-id="7c209-1126">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1126">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-1127">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-1127">ACR</span></span>
* <span data-ttu-id="7c209-1128">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1128">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1129">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1129">ACS</span></span>
* <span data-ttu-id="7c209-1130">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="7c209-1130">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="7c209-1131">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1131">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="7c209-1132">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1132">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="7c209-1133">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1133">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="7c209-1134">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-1134">Container</span></span>
* <span data-ttu-id="7c209-1135">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1135">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="7c209-1136">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1136">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="7c209-1137">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="7c209-1137">Event Hub</span></span>
* <span data-ttu-id="7c209-1138">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1138">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="7c209-1139">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1139">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="7c209-1140">Extensions</span><span class="sxs-lookup"><span data-stu-id="7c209-1140">Extensions</span></span>
* <span data-ttu-id="7c209-1141">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1141">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="7c209-1142">HDInsight</span><span class="sxs-lookup"><span data-stu-id="7c209-1142">HDInsight</span></span>
* <span data-ttu-id="7c209-1143">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="7c209-1143">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="7c209-1144">IoT</span><span class="sxs-lookup"><span data-stu-id="7c209-1144">IoT</span></span>
* <span data-ttu-id="7c209-1145">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1145">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="7c209-1146">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c209-1146">KeyVault</span></span>
* <span data-ttu-id="7c209-1147">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1147">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1148">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1148">Network</span></span>
* <span data-ttu-id="7c209-1149">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="7c209-1149">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="7c209-1150">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="7c209-1150">See #6052</span></span>
* <span data-ttu-id="7c209-1151">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1151">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="7c209-1152">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="7c209-1152">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="7c209-1153">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1153">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="7c209-1154">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1154">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="7c209-1155">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1155">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="7c209-1156">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1156">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="7c209-1157">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-1157">Role</span></span>
* <span data-ttu-id="7c209-1158">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1158">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="7c209-1159">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1159">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="7c209-1160">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1160">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="7c209-1161">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1161">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="7c209-1162">Service Bus</span><span class="sxs-lookup"><span data-stu-id="7c209-1162">Service Bus</span></span>
* <span data-ttu-id="7c209-1163">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1163">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1164">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1164">VM</span></span>
* <span data-ttu-id="7c209-1165">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1165">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="7c209-1166">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1166">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="7c209-1167">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1167">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="7c209-1168">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1168">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="7c209-1169">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1169">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="7c209-1170">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1170">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="7c209-1171">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1171">September 21, 2018</span></span>

<span data-ttu-id="7c209-1172">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="7c209-1172">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-1173">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-1173">ACR</span></span>
* <span data-ttu-id="7c209-1174">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1174">Added ACR Task commands</span></span>
* <span data-ttu-id="7c209-1175">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1175">Added quick run command</span></span>
* <span data-ttu-id="7c209-1176">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1176">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="7c209-1177">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1177">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="7c209-1178">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1178">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="7c209-1179">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1179">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1180">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1180">ACS</span></span>
* <span data-ttu-id="7c209-1181">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1181">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="7c209-1182">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1182">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1183">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-1183">AppService</span></span>

* <span data-ttu-id="7c209-1184">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1184">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="7c209-1185">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1185">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="7c209-1186">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1186">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="7c209-1187">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1187">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-1188">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-1188">Batch</span></span>
* <span data-ttu-id="7c209-1189">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1189">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="7c209-1190">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1190">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="7c209-1191">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1191">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="7c209-1192">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1192">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="7c209-1193">Batch AI</span><span class="sxs-lookup"><span data-stu-id="7c209-1193">Batch AI</span></span> 
* <span data-ttu-id="7c209-1194">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1194">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="7c209-1195">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="7c209-1195">Cognitive Services</span></span>
* <span data-ttu-id="7c209-1196">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1196">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="7c209-1197">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1197">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="7c209-1198">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1198">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="7c209-1199">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1199">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="7c209-1200">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1200">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="7c209-1201">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1201">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="7c209-1202">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-1202">Container</span></span>
* <span data-ttu-id="7c209-1203">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1203">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="7c209-1204">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1204">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="7c209-1205">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1205">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="7c209-1206">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1206">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="7c209-1207">DataLake</span><span class="sxs-lookup"><span data-stu-id="7c209-1207">Datalake</span></span>
* <span data-ttu-id="7c209-1208">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1208">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="7c209-1209">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="7c209-1209">Interactive Shell</span></span>
* <span data-ttu-id="7c209-1210">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1210">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="7c209-1211">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1211">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="7c209-1212">IoT</span><span class="sxs-lookup"><span data-stu-id="7c209-1212">IoT</span></span>
* <span data-ttu-id="7c209-1213">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1213">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="7c209-1214">Key Vault</span><span class="sxs-lookup"><span data-stu-id="7c209-1214">Key Vault</span></span>
* <span data-ttu-id="7c209-1215">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1215">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1216">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1216">Network</span></span>
* <span data-ttu-id="7c209-1217">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1217">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="7c209-1218">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1218">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="7c209-1219">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1219">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="7c209-1220">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1220">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="7c209-1221">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1221">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="7c209-1222">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1222">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="7c209-1223">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1223">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="7c209-1224">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-1224">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="7c209-1225">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1225">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="7c209-1226">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1226">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="7c209-1227">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1227">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="7c209-1228">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1228">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="7c209-1229">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1229">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="7c209-1230">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="7c209-1230">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="7c209-1231">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1231">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="7c209-1232">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1232">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="7c209-1233">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1233">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="7c209-1234">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1234">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="7c209-1235">RDBMS</span><span class="sxs-lookup"><span data-stu-id="7c209-1235">RDBMS</span></span>
* <span data-ttu-id="7c209-1236">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1236">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="7c209-1237">予約</span><span class="sxs-lookup"><span data-stu-id="7c209-1237">Reservation</span></span>
* <span data-ttu-id="7c209-1238">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1238">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="7c209-1239">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1239">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="7c209-1240">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="7c209-1240">Manage App</span></span>
* <span data-ttu-id="7c209-1241">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1241">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="7c209-1242">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1242">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="7c209-1243">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-1243">Role</span></span>
* <span data-ttu-id="7c209-1244">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1244">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="7c209-1245">SignalR</span><span class="sxs-lookup"><span data-stu-id="7c209-1245">SignalR</span></span>
* <span data-ttu-id="7c209-1246">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="7c209-1246">First release</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1247">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1247">Storage</span></span>
* <span data-ttu-id="7c209-1248">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1248">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="7c209-1249">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1249">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1250">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1250">VM</span></span>
* <span data-ttu-id="7c209-1251">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="7c209-1251">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="7c209-1252">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1252">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="7c209-1253">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1253">August 28, 2018</span></span>

<span data-ttu-id="7c209-1254">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="7c209-1254">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1255">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1255">Core</span></span>

* <span data-ttu-id="7c209-1256">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1256">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="7c209-1257">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1257">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-1258">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-1258">ACR</span></span>

* <span data-ttu-id="7c209-1259">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1259">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="7c209-1260">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1260">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1261">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1261">ACS</span></span>

* <span data-ttu-id="7c209-1262">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1262">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="7c209-1263">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1263">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1264">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-1264">AppService</span></span>

* <span data-ttu-id="7c209-1265">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1265">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="7c209-1266">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1266">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="7c209-1267">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1267">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="7c209-1268">バックアップ</span><span class="sxs-lookup"><span data-stu-id="7c209-1268">Backup</span></span>

* <span data-ttu-id="7c209-1269">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1269">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="7c209-1270">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="7c209-1270">Bot Service</span></span>

* <span data-ttu-id="7c209-1271">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="7c209-1271">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="7c209-1272">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="7c209-1272">Cognitive Services</span></span>

* <span data-ttu-id="7c209-1273">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1273">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="7c209-1274">IoT</span><span class="sxs-lookup"><span data-stu-id="7c209-1274">IoT</span></span>

* <span data-ttu-id="7c209-1275">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1275">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-1276">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-1276">Monitor</span></span>

* <span data-ttu-id="7c209-1277">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1277">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="7c209-1278">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1278">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1279">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1279">Network</span></span>

* <span data-ttu-id="7c209-1280">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1280">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-1281">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-1281">Resource</span></span>

* <span data-ttu-id="7c209-1282">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1282">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1283">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1283">Storage</span></span>

* <span data-ttu-id="7c209-1284">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1284">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1285">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1285">VM</span></span>

* <span data-ttu-id="7c209-1286">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1286">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="7c209-1287">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1287">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="7c209-1288">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1288">Auguest 14, 2018</span></span>

<span data-ttu-id="7c209-1289">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="7c209-1289">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1290">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1290">Core</span></span>

* <span data-ttu-id="7c209-1291">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1291">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="7c209-1292">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1292">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="7c209-1293">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="7c209-1293">Telemetry</span></span>

* <span data-ttu-id="7c209-1294">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1294">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-1295">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-1295">ACR</span></span>

* <span data-ttu-id="7c209-1296">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1296">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="7c209-1297">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1297">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1298">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1298">ACS</span></span>

* <span data-ttu-id="7c209-1299">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1299">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="7c209-1300">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1300">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="7c209-1301">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1301">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="7c209-1302">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1302">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="7c209-1303">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1303">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="7c209-1304">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-1304">AppService</span></span>

* <span data-ttu-id="7c209-1305">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1305">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="7c209-1306">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1306">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="7c209-1307">BatchAI</span><span class="sxs-lookup"><span data-stu-id="7c209-1307">BatchAI</span></span>

* <span data-ttu-id="7c209-1308">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1308">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="7c209-1309">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-1309">Container</span></span>

* <span data-ttu-id="7c209-1310">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1310">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="7c209-1311">IoT</span><span class="sxs-lookup"><span data-stu-id="7c209-1311">IoT</span></span>

* <span data-ttu-id="7c209-1312">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1312">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="7c209-1313">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1313">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="7c209-1314">Iot Central</span><span class="sxs-lookup"><span data-stu-id="7c209-1314">Iot Central</span></span>

* <span data-ttu-id="7c209-1315">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="7c209-1315">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="7c209-1316">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c209-1316">KeyVault</span></span>


* <span data-ttu-id="7c209-1317">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1317">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="7c209-1318">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1318">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="7c209-1319">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1319">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="7c209-1320">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1320">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="7c209-1321">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1321">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="7c209-1322">リレー</span><span class="sxs-lookup"><span data-stu-id="7c209-1322">Relay</span></span>

* <span data-ttu-id="7c209-1323">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="7c209-1323">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-1324">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-1324">Sql</span></span>

* <span data-ttu-id="7c209-1325">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1325">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1326">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1326">Storage</span></span>

* <span data-ttu-id="7c209-1327">[重大な変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="7c209-1327">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="7c209-1328">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1328">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="7c209-1329">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1329">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="7c209-1330">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1330">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="7c209-1331">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1331">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1332">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1332">VM</span></span>

* <span data-ttu-id="7c209-1333">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1333">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="7c209-1334">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="7c209-1334">July 31, 2018</span></span>

<span data-ttu-id="7c209-1335">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="7c209-1335">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-1336">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-1336">ACR</span></span>

* <span data-ttu-id="7c209-1337">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1337">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="7c209-1338">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1338">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1339">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1339">ACS</span></span>

* <span data-ttu-id="7c209-1340">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1340">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-1341">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-1341">Batch</span></span>

* <span data-ttu-id="7c209-1342">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1342">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="7c209-1343">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-1343">Container</span></span>

* <span data-ttu-id="7c209-1344">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1344">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1345">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1345">Network</span></span>

* <span data-ttu-id="7c209-1346">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1346">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="7c209-1347">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-1347">Resource</span></span>

* <span data-ttu-id="7c209-1348">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1348">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="7c209-1349">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1349">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="7c209-1350">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-1350">Role</span></span>

* <span data-ttu-id="7c209-1351">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1351">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="7c209-1352">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1352">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="7c209-1353">Search</span><span class="sxs-lookup"><span data-stu-id="7c209-1353">Search</span></span>

* <span data-ttu-id="7c209-1354">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1354">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="7c209-1355">Service Bus</span><span class="sxs-lookup"><span data-stu-id="7c209-1355">Service Bus</span></span>

* <span data-ttu-id="7c209-1356">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1356">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="7c209-1357">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1357">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="7c209-1358">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="7c209-1358">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="7c209-1359">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="7c209-1359">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1360">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1360">Storage</span></span>

* <span data-ttu-id="7c209-1361">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-1361">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="7c209-1362">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1362">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1363">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1363">VM</span></span>

* <span data-ttu-id="7c209-1364">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-1364">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="7c209-1365">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1365">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="7c209-1366">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1366">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="7c209-1367">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1367">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="7c209-1368">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1368">July 18, 2018</span></span>

<span data-ttu-id="7c209-1369">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="7c209-1369">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1370">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1370">Core</span></span>

* <span data-ttu-id="7c209-1371">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1371">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="7c209-1372">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1372">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="7c209-1373">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1373">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-1374">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-1374">ACR</span></span>

* <span data-ttu-id="7c209-1375">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1375">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="7c209-1376">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1376">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="7c209-1377">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1377">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="7c209-1378">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1378">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1379">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1379">ACS</span></span>

* <span data-ttu-id="7c209-1380">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1380">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1381">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-1381">AppService</span></span>

* <span data-ttu-id="7c209-1382">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1382">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-1383">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-1383">Batch</span></span>

* <span data-ttu-id="7c209-1384">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1384">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="7c209-1385">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1385">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="7c209-1386">Batch AI</span><span class="sxs-lookup"><span data-stu-id="7c209-1386">Batch AI</span></span>

* <span data-ttu-id="7c209-1387">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1387">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="7c209-1388">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-1388">Container</span></span>

* <span data-ttu-id="7c209-1389">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1389">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="7c209-1390">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1390">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1391">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1391">Network</span></span>

* <span data-ttu-id="7c209-1392">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1392">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="7c209-1393">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1393">Added `network nic wait`</span></span>
* <span data-ttu-id="7c209-1394">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1394">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="7c209-1395">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1395">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="7c209-1396">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-1396">Resource</span></span>

* <span data-ttu-id="7c209-1397">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1397">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="7c209-1398">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1398">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="7c209-1399">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1399">Added `deployment wait` command</span></span>
* <span data-ttu-id="7c209-1400">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1400">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-1401">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-1401">SQL</span></span>

* <span data-ttu-id="7c209-1402">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1402">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="7c209-1403">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-1403">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="7c209-1404">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1404">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1405">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1405">Storage</span></span>

* <span data-ttu-id="7c209-1406">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1406">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1407">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1407">VM</span></span>

* <span data-ttu-id="7c209-1408">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1408">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="7c209-1409">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1409">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="7c209-1410">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1410">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="7c209-1411">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1411">July 3, 2018</span></span>

<span data-ttu-id="7c209-1412">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="7c209-1412">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="7c209-1413">AKS</span><span class="sxs-lookup"><span data-stu-id="7c209-1413">AKS</span></span>

* <span data-ttu-id="7c209-1414">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1414">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="7c209-1415">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1415">July 3, 2018</span></span>

<span data-ttu-id="7c209-1416">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="7c209-1416">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1417">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1417">Core</span></span>

* <span data-ttu-id="7c209-1418">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1418">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-1419">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-1419">ACR</span></span>

* <span data-ttu-id="7c209-1420">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1420">Added polling build status</span></span>
* <span data-ttu-id="7c209-1421">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1421">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="7c209-1422">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1422">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1423">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1423">ACS</span></span>

* <span data-ttu-id="7c209-1424">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1424">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="7c209-1425">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1425">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="7c209-1426">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1426">Updated options for `aks browse` command.</span></span> <span data-ttu-id="7c209-1427">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1427">Added `--listen-port` support</span></span>
* <span data-ttu-id="7c209-1428">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1428">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="7c209-1429">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="7c209-1429">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="7c209-1430">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1430">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1431">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-1431">AppService</span></span>

* <span data-ttu-id="7c209-1432">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-1432">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="7c209-1433">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1433">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="7c209-1434">バックアップ</span><span class="sxs-lookup"><span data-stu-id="7c209-1434">Backup</span></span>

* <span data-ttu-id="7c209-1435">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1435">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="7c209-1436">BatchAI</span><span class="sxs-lookup"><span data-stu-id="7c209-1436">BatchAI</span></span>

* <span data-ttu-id="7c209-1437">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1437">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="7c209-1438">クラウド</span><span class="sxs-lookup"><span data-stu-id="7c209-1438">Cloud</span></span>

* <span data-ttu-id="7c209-1439">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1439">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="7c209-1440">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-1440">Container</span></span>

* <span data-ttu-id="7c209-1441">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1441">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="7c209-1442">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1442">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="7c209-1443">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1443">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="7c209-1444">拡張機能</span><span class="sxs-lookup"><span data-stu-id="7c209-1444">Extension</span></span>

* <span data-ttu-id="7c209-1445">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1445">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1446">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1446">Network</span></span>

* <span data-ttu-id="7c209-1447">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1447">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="7c209-1448">Rdbms</span><span class="sxs-lookup"><span data-stu-id="7c209-1448">Rdbms</span></span>

* <span data-ttu-id="7c209-1449">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1449">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-1450">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-1450">Resource</span></span>

* <span data-ttu-id="7c209-1451">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1451">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1452">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1452">VM</span></span>

* <span data-ttu-id="7c209-1453">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-1453">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="7c209-1454">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1454">June 25, 2018</span></span>

<span data-ttu-id="7c209-1455">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="7c209-1455">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="7c209-1456">CLI</span><span class="sxs-lookup"><span data-stu-id="7c209-1456">CLI</span></span>

* <span data-ttu-id="7c209-1457">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1457">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="7c209-1458">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1458">June 19, 2018</span></span>

<span data-ttu-id="7c209-1459">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="7c209-1459">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1460">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1460">Core</span></span>

* <span data-ttu-id="7c209-1461">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1461">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-1462">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-1462">ACR</span></span>

* <span data-ttu-id="7c209-1463">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1463">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="7c209-1464">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1464">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1465">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1465">ACS</span></span>

* <span data-ttu-id="7c209-1466">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1466">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="7c209-1467">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1467">Added `--update` support</span></span>
* <span data-ttu-id="7c209-1468">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1468">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="7c209-1469">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1469">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="7c209-1470">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1470">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="7c209-1471">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1471">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="7c209-1472">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1472">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="7c209-1473">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1473">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1474">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-1474">AppService</span></span>

* <span data-ttu-id="7c209-1475">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1475">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="7c209-1476">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1476">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-1477">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-1477">Batch</span></span>

* <span data-ttu-id="7c209-1478">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1478">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="7c209-1479">Batch AI</span><span class="sxs-lookup"><span data-stu-id="7c209-1479">Batch AI</span></span>

* <span data-ttu-id="7c209-1480">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1480">Added support for workspaces.</span></span> <span data-ttu-id="7c209-1481">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="7c209-1481">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="7c209-1482">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1482">Added support for experiments.</span></span> <span data-ttu-id="7c209-1483">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="7c209-1483">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="7c209-1484">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1484">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="7c209-1485">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1485">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="7c209-1486">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="7c209-1486">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="7c209-1487">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1487">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="7c209-1488">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="7c209-1488">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="7c209-1489">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="7c209-1489">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="7c209-1490">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1490">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="7c209-1491">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="7c209-1491">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="7c209-1492">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1492">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="7c209-1493">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="7c209-1493">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="7c209-1494">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1494">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="7c209-1495">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="7c209-1495">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="7c209-1496">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1496">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="7c209-1497">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1497">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="7c209-1498">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1498">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="7c209-1499">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1499">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="7c209-1500">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1500">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="7c209-1501">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1501">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="7c209-1502">マップ</span><span class="sxs-lookup"><span data-stu-id="7c209-1502">Maps</span></span>

* <span data-ttu-id="7c209-1503">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1503">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1504">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1504">Network</span></span>

* <span data-ttu-id="7c209-1505">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="7c209-1505">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="7c209-1506">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1506">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="7c209-1507">#6502</span><span class="sxs-lookup"><span data-stu-id="7c209-1507">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="7c209-1508">Reservations</span><span class="sxs-lookup"><span data-stu-id="7c209-1508">Reservations</span></span>

* <span data-ttu-id="7c209-1509">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1509">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="7c209-1510">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1510">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="7c209-1511">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1511">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="7c209-1512">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1512">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="7c209-1513">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1513">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="7c209-1514">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1514">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="7c209-1515">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-1515">Role</span></span>

* <span data-ttu-id="7c209-1516">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1516">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-1517">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-1517">SQL</span></span>

* <span data-ttu-id="7c209-1518">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1518">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1519">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1519">Storage</span></span>

* <span data-ttu-id="7c209-1520">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1520">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1521">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1521">VM</span></span>

* <span data-ttu-id="7c209-1522">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1522">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="7c209-1523">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1523">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="7c209-1524">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1524">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="7c209-1525">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1525">June 13, 2018</span></span>

<span data-ttu-id="7c209-1526">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="7c209-1526">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1527">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1527">Core</span></span>

* <span data-ttu-id="7c209-1528">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1528">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="7c209-1529">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1529">June 13, 2018</span></span>

<span data-ttu-id="7c209-1530">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="7c209-1530">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="7c209-1531">AKS</span><span class="sxs-lookup"><span data-stu-id="7c209-1531">AKS</span></span>

* <span data-ttu-id="7c209-1532">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1532">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="7c209-1533">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1533">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="7c209-1534">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1534">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="7c209-1535">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1535">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="7c209-1536">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1536">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1537">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-1537">AppService</span></span>

* <span data-ttu-id="7c209-1538">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1538">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="7c209-1539">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1539">June 5, 2018</span></span>

<span data-ttu-id="7c209-1540">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="7c209-1540">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="7c209-1541">Interactive</span><span class="sxs-lookup"><span data-stu-id="7c209-1541">Interactive</span></span>

* <span data-ttu-id="7c209-1542">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1542">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="7c209-1543">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1543">June 5, 2018</span></span>

<span data-ttu-id="7c209-1544">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="7c209-1544">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1545">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1545">Core</span></span>

* <span data-ttu-id="7c209-1546">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1546">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="7c209-1547">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1547">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-1548">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-1548">ACR</span></span>

* <span data-ttu-id="7c209-1549">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1549">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="7c209-1550">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1550">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="7c209-1551">AKS</span><span class="sxs-lookup"><span data-stu-id="7c209-1551">AKS</span></span>

* <span data-ttu-id="7c209-1552">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1552">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-1553">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-1553">Batch</span></span>

* <span data-ttu-id="7c209-1554">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1554">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="7c209-1555">IoT</span><span class="sxs-lookup"><span data-stu-id="7c209-1555">IOT</span></span>

* <span data-ttu-id="7c209-1556">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1556">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1557">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1557">Network</span></span>

* <span data-ttu-id="7c209-1558">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1558">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="7c209-1559">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="7c209-1559">Policy Insights</span></span>

* <span data-ttu-id="7c209-1560">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="7c209-1560">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="7c209-1561">ARM</span><span class="sxs-lookup"><span data-stu-id="7c209-1561">ARM</span></span>

* <span data-ttu-id="7c209-1562">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1562">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-1563">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-1563">SQL</span></span>

* <span data-ttu-id="7c209-1564">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1564">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="7c209-1565">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1565">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="7c209-1566">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1566">Storage</span></span>

* <span data-ttu-id="7c209-1567">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1567">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1568">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1568">VM</span></span>

* <span data-ttu-id="7c209-1569">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1569">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="7c209-1570">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1570">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="7c209-1571">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1571">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="7c209-1572">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1572">May 22, 2018</span></span>

<span data-ttu-id="7c209-1573">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="7c209-1573">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1574">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1574">Core</span></span>

* <span data-ttu-id="7c209-1575">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1575">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1576">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1576">ACS</span></span>

* <span data-ttu-id="7c209-1577">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1577">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="7c209-1578">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1578">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1579">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-1579">AppService</span></span>

* <span data-ttu-id="7c209-1580">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1580">Improved generic update commands</span></span>
* <span data-ttu-id="7c209-1581">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1581">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="7c209-1582">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-1582">Container</span></span>

* <span data-ttu-id="7c209-1583">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1583">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="7c209-1584">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1584">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="7c209-1585">拡張機能</span><span class="sxs-lookup"><span data-stu-id="7c209-1585">Extension</span></span>

* <span data-ttu-id="7c209-1586">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1586">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="7c209-1587">Interactive</span><span class="sxs-lookup"><span data-stu-id="7c209-1587">Interactive</span></span>

* <span data-ttu-id="7c209-1588">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1588">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="7c209-1589">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1589">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="7c209-1590">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c209-1590">KeyVault</span></span>

* <span data-ttu-id="7c209-1591">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1591">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1592">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1592">Network</span></span>

* <span data-ttu-id="7c209-1593">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1593">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="7c209-1594">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1594">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-1595">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-1595">SQL</span></span>

* <span data-ttu-id="7c209-1596">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1596">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="7c209-1597">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1597">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="7c209-1598">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1598">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="7c209-1599">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1599">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="7c209-1600">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1600">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="7c209-1601">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="7c209-1601">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="7c209-1602">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="7c209-1602">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="7c209-1603">`edition`</span><span class="sxs-lookup"><span data-stu-id="7c209-1603">`edition`.</span></span> <span data-ttu-id="7c209-1604">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="7c209-1604">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="7c209-1605">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="7c209-1605">`elasticPoolName`.</span></span> <span data-ttu-id="7c209-1606">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="7c209-1606">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="7c209-1607">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1607">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="7c209-1608">`edition`</span><span class="sxs-lookup"><span data-stu-id="7c209-1608">`edition`.</span></span> <span data-ttu-id="7c209-1609">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="7c209-1609">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="7c209-1610">`dtu`</span><span class="sxs-lookup"><span data-stu-id="7c209-1610">`dtu`.</span></span> <span data-ttu-id="7c209-1611">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="7c209-1611">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="7c209-1612">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="7c209-1612">`databaseDtuMin`.</span></span> <span data-ttu-id="7c209-1613">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="7c209-1613">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="7c209-1614">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="7c209-1614">`databaseDtuMax`.</span></span> <span data-ttu-id="7c209-1615">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="7c209-1615">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="7c209-1616">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1616">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="7c209-1617">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1617">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1618">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1618">Storage</span></span>

* <span data-ttu-id="7c209-1619">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1619">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="7c209-1620">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1620">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1621">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1621">VM</span></span>

* <span data-ttu-id="7c209-1622">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1622">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="7c209-1623">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="7c209-1623">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="7c209-1624">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1624">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="7c209-1625">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1625">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="7c209-1626">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1626">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="7c209-1627">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1627">May 7, 2018</span></span>

<span data-ttu-id="7c209-1628">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="7c209-1628">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1629">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1629">Core</span></span>

* <span data-ttu-id="7c209-1630">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1630">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="7c209-1631">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1631">Added limited support for positional arguments</span></span>
* <span data-ttu-id="7c209-1632">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1632">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="7c209-1633">#5591</span><span class="sxs-lookup"><span data-stu-id="7c209-1633">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="7c209-1634">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1634">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="7c209-1635">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="7c209-1635">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="7c209-1636">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1636">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="7c209-1637">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1637">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="7c209-1638">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1638">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-1639">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-1639">ACR</span></span>

* <span data-ttu-id="7c209-1640">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1640">Added ACR Build commands</span></span>
* <span data-ttu-id="7c209-1641">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1641">Improved resource not found error messages</span></span>
* <span data-ttu-id="7c209-1642">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1642">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="7c209-1643">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1643">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="7c209-1644">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1644">Improved repository commands error messages</span></span>
* <span data-ttu-id="7c209-1645">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1645">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1646">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1646">ACS</span></span>

* <span data-ttu-id="7c209-1647">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1647">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="7c209-1648">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1648">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="7c209-1649">AMS</span><span class="sxs-lookup"><span data-stu-id="7c209-1649">AMS</span></span>

* <span data-ttu-id="7c209-1650">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="7c209-1650">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1651">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-1651">Appservice</span></span>

* <span data-ttu-id="7c209-1652">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1652">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="7c209-1653">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1653">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="7c209-1654">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1654">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="7c209-1655">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1655">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="7c209-1656">Batch AI</span><span class="sxs-lookup"><span data-stu-id="7c209-1656">Batch AI</span></span>

* <span data-ttu-id="7c209-1657">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1657">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="7c209-1658">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="7c209-1658">Cognitive Services</span></span>

* <span data-ttu-id="7c209-1659">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1659">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="7c209-1660">消費</span><span class="sxs-lookup"><span data-stu-id="7c209-1660">Consumption</span></span>

* <span data-ttu-id="7c209-1661">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1661">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="7c209-1662">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-1662">Container</span></span>

* <span data-ttu-id="7c209-1663">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1663">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="7c209-1664">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="7c209-1664">Cosmos DB</span></span>

* <span data-ttu-id="7c209-1665">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1665">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="7c209-1666">DMS</span><span class="sxs-lookup"><span data-stu-id="7c209-1666">DMS</span></span>

* <span data-ttu-id="7c209-1667">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1667">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="7c209-1668">拡張機能</span><span class="sxs-lookup"><span data-stu-id="7c209-1668">Extension</span></span>

* <span data-ttu-id="7c209-1669">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1669">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="7c209-1670">Interactive</span><span class="sxs-lookup"><span data-stu-id="7c209-1670">Interactive</span></span>

* <span data-ttu-id="7c209-1671">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-1671">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="7c209-1672">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1672">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="7c209-1673">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1673">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="7c209-1674">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1674">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="7c209-1675">ラボ</span><span class="sxs-lookup"><span data-stu-id="7c209-1675">Lab</span></span>

* <span data-ttu-id="7c209-1676">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1676">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1677">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1677">Network</span></span>

* <span data-ttu-id="7c209-1678">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1678">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="7c209-1679">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-1679">Profile</span></span>

* <span data-ttu-id="7c209-1680">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1680">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="7c209-1681">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1681">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="7c209-1682">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1682">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="7c209-1683">Redis</span><span class="sxs-lookup"><span data-stu-id="7c209-1683">Redis</span></span>

* <span data-ttu-id="7c209-1684">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1684">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="7c209-1685">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1685">Deprecated `redis list-all`.</span></span> <span data-ttu-id="7c209-1686">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="7c209-1686">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="7c209-1687">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1687">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="7c209-1688">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1688">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="7c209-1689">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-1689">Role</span></span>

* <span data-ttu-id="7c209-1690">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1690">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1691">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1691">Storage</span></span>

* <span data-ttu-id="7c209-1692">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="7c209-1692">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="7c209-1693">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1693">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="7c209-1694">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="7c209-1694">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="7c209-1695">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="7c209-1695">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="7c209-1696">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1696">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1697">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1697">VM</span></span>

* <span data-ttu-id="7c209-1698">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1698">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="7c209-1699">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1699">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="7c209-1700">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="7c209-1700">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="7c209-1701">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1701">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="7c209-1702">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1702">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="7c209-1703">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1703">Added write accelerator support</span></span>
* <span data-ttu-id="7c209-1704">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1704">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="7c209-1705">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1705">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="7c209-1706">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1706">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="7c209-1707">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1707">April 10, 2018</span></span>

<span data-ttu-id="7c209-1708">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="7c209-1708">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-1709">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-1709">ACR</span></span>

* <span data-ttu-id="7c209-1710">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1710">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1711">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1711">ACS</span></span>

* <span data-ttu-id="7c209-1712">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1712">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1713">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-1713">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="7c209-1715">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1715">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="7c209-1716">BatchAI</span><span class="sxs-lookup"><span data-stu-id="7c209-1716">BatchAI</span></span>

* <span data-ttu-id="7c209-1717">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1717">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="7c209-1718">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="7c209-1718">Job level mounting</span></span>
  - <span data-ttu-id="7c209-1719">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="7c209-1719">Environment variables with secret values</span></span>
  - <span data-ttu-id="7c209-1720">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="7c209-1720">Performance counters settings</span></span>
  - <span data-ttu-id="7c209-1721">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="7c209-1721">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="7c209-1722">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="7c209-1722">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="7c209-1723">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="7c209-1723">Usage and limits reporting</span></span>
  - <span data-ttu-id="7c209-1724">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="7c209-1724">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="7c209-1725">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="7c209-1725">Support for custom images</span></span>
  - <span data-ttu-id="7c209-1726">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1726">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="7c209-1727">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-1727">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="7c209-1728">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="7c209-1728">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="7c209-1729">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="7c209-1729">National clouds are supported</span></span>
* <span data-ttu-id="7c209-1730">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1730">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="7c209-1731">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1731">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="7c209-1732">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1732">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="7c209-1733">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1733">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="7c209-1734">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="7c209-1734">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="7c209-1735">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="7c209-1735">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="7c209-1736">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1736">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="7c209-1737">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1737">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="7c209-1738">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="7c209-1738">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="7c209-1739">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1739">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="7c209-1740">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1740">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="7c209-1741">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1741">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="7c209-1742">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1742">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="7c209-1743">課金</span><span class="sxs-lookup"><span data-stu-id="7c209-1743">Billing</span></span>

* <span data-ttu-id="7c209-1744">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1744">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="7c209-1745">消費</span><span class="sxs-lookup"><span data-stu-id="7c209-1745">Consumption</span></span>

* <span data-ttu-id="7c209-1746">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1746">Added `marketplace` commands</span></span>
* <span data-ttu-id="7c209-1747">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1747">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="7c209-1748">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1748">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="7c209-1749">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1749">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="7c209-1750">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1750">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="7c209-1751">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1751">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="7c209-1752">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-1752">Container</span></span>

* <span data-ttu-id="7c209-1753">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1753">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="7c209-1754">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1754">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="7c209-1755">拡張機能</span><span class="sxs-lookup"><span data-stu-id="7c209-1755">Extension</span></span>

* <span data-ttu-id="7c209-1756">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1756">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="7c209-1757">Interactive</span><span class="sxs-lookup"><span data-stu-id="7c209-1757">Interactive</span></span>

* <span data-ttu-id="7c209-1758">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1758">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="7c209-1759">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1759">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="7c209-1760">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1760">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1761">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1761">Network</span></span>

* <span data-ttu-id="7c209-1762">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1762">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="7c209-1763">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1763">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="7c209-1764">#4910</span><span class="sxs-lookup"><span data-stu-id="7c209-1764">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="7c209-1765">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1765">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="7c209-1766">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="7c209-1766">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="7c209-1767">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1767">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="7c209-1768">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1768">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="7c209-1769">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1769">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="7c209-1770">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-1770">Profile</span></span>

* <span data-ttu-id="7c209-1771">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1771">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="7c209-1772">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1772">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="7c209-1773">RDBMS</span><span class="sxs-lookup"><span data-stu-id="7c209-1773">RDBMS</span></span>

* <span data-ttu-id="7c209-1774">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1774">Added `georestore` command</span></span>
* <span data-ttu-id="7c209-1775">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1775">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-1776">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-1776">Resource</span></span>

* <span data-ttu-id="7c209-1777">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1777">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="7c209-1778">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1778">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-1779">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-1779">SQL</span></span>

* <span data-ttu-id="7c209-1780">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1780">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1781">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1781">Storage</span></span>

* <span data-ttu-id="7c209-1782">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1782">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1783">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1783">VM</span></span>

* <span data-ttu-id="7c209-1784">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1784">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="7c209-1785">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1785">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="7c209-1787">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1787">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="7c209-1788">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1788">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="7c209-1789">#5718</span><span class="sxs-lookup"><span data-stu-id="7c209-1789">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="7c209-1790">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1790">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="7c209-1791">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1791">March 27, 2018</span></span>

<span data-ttu-id="7c209-1792">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="7c209-1792">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1793">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1793">Core</span></span>

* <span data-ttu-id="7c209-1794">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="7c209-1794">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1795">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1795">ACS</span></span>

* <span data-ttu-id="7c209-1796">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1796">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1797">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-1797">Appservice</span></span>

* <span data-ttu-id="7c209-1798">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1798">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="7c209-1799">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1799">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="7c209-1800">バックアップ</span><span class="sxs-lookup"><span data-stu-id="7c209-1800">Backup</span></span>

* <span data-ttu-id="7c209-1801">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1801">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="7c209-1802">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="7c209-1802">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="7c209-1803">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1803">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="7c209-1804">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1804">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="7c209-1805">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-1805">Container</span></span>

* <span data-ttu-id="7c209-1806">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1806">Added `container exec` command.</span></span> <span data-ttu-id="7c209-1807">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="7c209-1807">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="7c209-1808">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="7c209-1808">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="7c209-1809">拡張機能</span><span class="sxs-lookup"><span data-stu-id="7c209-1809">Extension</span></span>

* <span data-ttu-id="7c209-1810">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1810">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="7c209-1811">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1811">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="7c209-1812">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1812">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="7c209-1813">Interactive</span><span class="sxs-lookup"><span data-stu-id="7c209-1813">Interactive</span></span>

* <span data-ttu-id="7c209-1814">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1814">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="7c209-1815">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1815">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="7c209-1816">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="7c209-1816">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="7c209-1817">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1817">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="7c209-1818">ラボ</span><span class="sxs-lookup"><span data-stu-id="7c209-1818">Lab</span></span>

* <span data-ttu-id="7c209-1819">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1819">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-1820">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-1820">Monitor</span></span>

* <span data-ttu-id="7c209-1821">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="7c209-1821">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="7c209-1822">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="7c209-1822">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="7c209-1823">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="7c209-1823">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1824">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1824">Network</span></span>

* <span data-ttu-id="7c209-1825">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1825">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="7c209-1826">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-1826">Profile</span></span>

* <span data-ttu-id="7c209-1827">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1827">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="7c209-1828">RDBMS</span><span class="sxs-lookup"><span data-stu-id="7c209-1828">RDBMS</span></span>

* <span data-ttu-id="7c209-1829">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1829">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-1830">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-1830">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="7c209-1832">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-1832">Role</span></span>

* <span data-ttu-id="7c209-1833">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1833">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="7c209-1834">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1834">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="7c209-1835">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1835">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="7c209-1836">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1836">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="7c209-1837">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1837">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1838">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1838">Storage</span></span>

* <span data-ttu-id="7c209-1839">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1839">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="7c209-1840">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="7c209-1840">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1841">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1841">VM</span></span>

* <span data-ttu-id="7c209-1842">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1842">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="7c209-1843">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1843">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="7c209-1844">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1844">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="7c209-1845">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1845">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="7c209-1846">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1846">March 13, 2018</span></span>

<span data-ttu-id="7c209-1847">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="7c209-1847">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-1848">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-1848">ACR</span></span>

* <span data-ttu-id="7c209-1849">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1849">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="7c209-1850">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1850">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="7c209-1851">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1851">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1852">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1852">ACS</span></span>

* <span data-ttu-id="7c209-1853">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1853">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="7c209-1854">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1854">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="7c209-1855">Advisor</span><span class="sxs-lookup"><span data-stu-id="7c209-1855">Advisor</span></span>

* <span data-ttu-id="7c209-1856">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1856">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="7c209-1857">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1857">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="7c209-1858">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1858">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="7c209-1859">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1859">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="7c209-1860">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1860">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1861">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-1861">Appservice</span></span>

* <span data-ttu-id="7c209-1862">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1862">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="7c209-1863">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1863">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="7c209-1864">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="7c209-1864">Eventhubs</span></span>

* <span data-ttu-id="7c209-1865">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="7c209-1865">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="7c209-1866">拡張機能</span><span class="sxs-lookup"><span data-stu-id="7c209-1866">Extension</span></span>

* <span data-ttu-id="7c209-1867">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1867">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="7c209-1868">Interactive</span><span class="sxs-lookup"><span data-stu-id="7c209-1868">Interactive</span></span>

* <span data-ttu-id="7c209-1869">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="7c209-1869">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="7c209-1870">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="7c209-1870">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="7c209-1871">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="7c209-1871">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="7c209-1872">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1872">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-1873">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-1873">Monitor</span></span>

* <span data-ttu-id="7c209-1874">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1874">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="7c209-1875">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1875">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="7c209-1876">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1876">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="7c209-1877">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1877">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1878">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1878">Network</span></span>

* <span data-ttu-id="7c209-1879">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1879">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="7c209-1880">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1880">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="7c209-1881">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1881">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="7c209-1882">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1882">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="7c209-1883">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-1883">Profile</span></span>

* <span data-ttu-id="7c209-1884">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1884">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="7c209-1885">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1885">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="7c209-1886">RDBMS</span><span class="sxs-lookup"><span data-stu-id="7c209-1886">RDBMS</span></span>

* <span data-ttu-id="7c209-1887">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1887">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="7c209-1888">Service Bus</span><span class="sxs-lookup"><span data-stu-id="7c209-1888">Service Bus</span></span>

* <span data-ttu-id="7c209-1889">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="7c209-1889">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1890">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1890">Storage</span></span>

* <span data-ttu-id="7c209-1891">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-1891">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="7c209-1892">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="7c209-1892">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1893">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1893">VM</span></span>

* <span data-ttu-id="7c209-1894">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1894">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="7c209-1895">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1895">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="7c209-1896">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1896">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="7c209-1897">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1897">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="7c209-1898">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1898">February 27, 2018</span></span>

<span data-ttu-id="7c209-1899">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="7c209-1899">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1900">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1900">Core</span></span>

* <span data-ttu-id="7c209-1901">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="7c209-1901">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="7c209-1902">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1902">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="7c209-1903">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1903">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1904">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1904">ACS</span></span>

* <span data-ttu-id="7c209-1905">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1905">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="7c209-1906">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="7c209-1906">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="7c209-1907">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1907">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="7c209-1908">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1908">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1909">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-1909">Appservice</span></span>

* <span data-ttu-id="7c209-1910">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="7c209-1910">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="7c209-1911">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="7c209-1911">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="7c209-1912">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="7c209-1912">Cognitive Services</span></span>

* <span data-ttu-id="7c209-1913">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1913">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="7c209-1914">消費</span><span class="sxs-lookup"><span data-stu-id="7c209-1914">Consumption</span></span>

* <span data-ttu-id="7c209-1915">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1915">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="7c209-1916">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1916">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="7c209-1917">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-1917">Container</span></span>

* <span data-ttu-id="7c209-1918">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1918">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1919">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1919">Network</span></span>

* <span data-ttu-id="7c209-1920">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="7c209-1920">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-1921">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-1921">Resource</span></span>

* <span data-ttu-id="7c209-1922">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1922">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="7c209-1923">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-1923">Role</span></span>

* <span data-ttu-id="7c209-1924">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1924">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-1925">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-1925">SQL</span></span>

* <span data-ttu-id="7c209-1926">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1926">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1927">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1927">Storage</span></span>

* <span data-ttu-id="7c209-1928">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1928">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1929">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1929">VM</span></span>

* <span data-ttu-id="7c209-1930">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1930">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="7c209-1931">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1931">February 13, 2018</span></span>

<span data-ttu-id="7c209-1932">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="7c209-1932">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1933">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1933">Core</span></span>

* <span data-ttu-id="7c209-1934">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1934">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1935">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1935">ACS</span></span>

* <span data-ttu-id="7c209-1936">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1936">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="7c209-1937">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1937">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="7c209-1938">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1938">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="7c209-1939">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1939">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="7c209-1940">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1940">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="7c209-1941">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1941">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="7c209-1942">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1942">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="7c209-1943">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="7c209-1943">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1944">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-1944">Appservice</span></span>

* <span data-ttu-id="7c209-1945">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1945">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="7c209-1946">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1946">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="7c209-1947">CDN</span><span class="sxs-lookup"><span data-stu-id="7c209-1947">CDN</span></span>

* <span data-ttu-id="7c209-1948">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1948">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="7c209-1949">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-1949">Container</span></span>

* <span data-ttu-id="7c209-1950">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1950">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="7c209-1951">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1951">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="7c209-1952">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="7c209-1952">CosmosDB</span></span>

* <span data-ttu-id="7c209-1953">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1953">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="7c209-1954">拡張機能</span><span class="sxs-lookup"><span data-stu-id="7c209-1954">Extension</span></span>

* <span data-ttu-id="7c209-1955">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1955">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="7c209-1956">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1956">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="7c209-1957">フィードバック</span><span class="sxs-lookup"><span data-stu-id="7c209-1957">Feedback</span></span>

* <span data-ttu-id="7c209-1958">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1958">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="7c209-1959">Interactive</span><span class="sxs-lookup"><span data-stu-id="7c209-1959">Interactive</span></span>

* <span data-ttu-id="7c209-1960">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1960">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="7c209-1961">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1961">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="7c209-1962">IoT</span><span class="sxs-lookup"><span data-stu-id="7c209-1962">IoT</span></span>

* <span data-ttu-id="7c209-1963">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1963">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="7c209-1964">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1964">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="7c209-1965">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1965">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="7c209-1966">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1966">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-1967">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-1967">Monitor</span></span>

* <span data-ttu-id="7c209-1968">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1968">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="7c209-1969">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-1969">Network</span></span>

* <span data-ttu-id="7c209-1970">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1970">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="7c209-1971">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-1971">Profile</span></span>

* <span data-ttu-id="7c209-1972">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-1972">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-1973">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-1973">Resource</span></span>

* <span data-ttu-id="7c209-1974">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1974">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="7c209-1975">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-1975">Role</span></span>

* <span data-ttu-id="7c209-1976">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1976">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-1977">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-1977">SQL</span></span>

* <span data-ttu-id="7c209-1978">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1978">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="7c209-1979">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1979">Added `sql db rename`</span></span>
* <span data-ttu-id="7c209-1980">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1980">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-1981">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-1981">Storage</span></span>

* <span data-ttu-id="7c209-1982">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1982">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-1983">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-1983">VM</span></span>

* <span data-ttu-id="7c209-1984">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1984">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="7c209-1985">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1985">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="7c209-1986">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="7c209-1986">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="7c209-1987">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="7c209-1987">January 31, 2018</span></span>

<span data-ttu-id="7c209-1988">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="7c209-1988">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="7c209-1989">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-1989">Core</span></span>

* <span data-ttu-id="7c209-1990">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1990">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="7c209-1991">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1991">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="7c209-1992">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-1992">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="7c209-1993">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="7c209-1993">Use `--verbose` to see</span></span>
* <span data-ttu-id="7c209-1994">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="7c209-1994">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-1995">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-1995">ACS</span></span>

* <span data-ttu-id="7c209-1996">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1996">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="7c209-1997">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-1997">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-1998">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-1998">Appservice</span></span>

* <span data-ttu-id="7c209-1999">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="7c209-1999">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="7c209-2000">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2000">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="7c209-2001">CDN</span><span class="sxs-lookup"><span data-stu-id="7c209-2001">CDN</span></span>

* <span data-ttu-id="7c209-2002">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2002">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="7c209-2003">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="7c209-2003">CosmosDB</span></span>

* <span data-ttu-id="7c209-2004">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2004">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="7c209-2005">Interactive</span><span class="sxs-lookup"><span data-stu-id="7c209-2005">Interactive</span></span>

* <span data-ttu-id="7c209-2006">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2006">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="7c209-2007">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-2007">Network</span></span>

* <span data-ttu-id="7c209-2008">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2008">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="7c209-2009">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2009">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="7c209-2010">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2010">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="7c209-2011">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2011">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="7c209-2012">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2012">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="7c209-2013">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2013">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="7c209-2014">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2014">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="7c209-2015">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2015">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="7c209-2016">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2016">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="7c209-2017">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2017">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="7c209-2018">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-2018">Profile</span></span>

* <span data-ttu-id="7c209-2019">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2019">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-2020">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-2020">Resource</span></span>

* <span data-ttu-id="7c209-2021">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2021">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-2022">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-2022">Storage</span></span>

* <span data-ttu-id="7c209-2023">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2023">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="7c209-2024">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2024">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="7c209-2025">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2025">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="7c209-2026">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2026">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="7c209-2027">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2027">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-2028">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-2028">VM</span></span>

* <span data-ttu-id="7c209-2029">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2029">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="7c209-2030">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2030">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="7c209-2031">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2031">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="7c209-2032">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2032">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="7c209-2033">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2033">January 17, 2018</span></span>

<span data-ttu-id="7c209-2034">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="7c209-2034">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-2035">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-2035">ACR</span></span>

* <span data-ttu-id="7c209-2036">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2036">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="7c209-2037">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2037">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-2038">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-2038">ACS</span></span>

* <span data-ttu-id="7c209-2039">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2039">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="7c209-2040">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2040">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-2041">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-2041">Appservice</span></span>

* <span data-ttu-id="7c209-2042">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2042">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="7c209-2043">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2043">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="7c209-2044">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2044">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="7c209-2045">バックアップ</span><span class="sxs-lookup"><span data-stu-id="7c209-2045">Backup</span></span>

* <span data-ttu-id="7c209-2046">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2046">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="7c209-2047">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2047">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="7c209-2048">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2048">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="7c209-2049">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2049">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="7c209-2050">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2050">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-2051">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-2051">Batch</span></span>

* <span data-ttu-id="7c209-2052">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2052">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="7c209-2053">クラウド</span><span class="sxs-lookup"><span data-stu-id="7c209-2053">Cloud</span></span>

* <span data-ttu-id="7c209-2054">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2054">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="7c209-2055">消費</span><span class="sxs-lookup"><span data-stu-id="7c209-2055">Consumption</span></span>

* <span data-ttu-id="7c209-2056">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2056">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="7c209-2057">Event Grid</span><span class="sxs-lookup"><span data-stu-id="7c209-2057">Event Grid</span></span>

* <span data-ttu-id="7c209-2058">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2058">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="7c209-2059">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2059">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="7c209-2060">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2060">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="7c209-2061">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="7c209-2061">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="7c209-2062">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2062">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="7c209-2063">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2063">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="7c209-2064">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2064">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="7c209-2065">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2065">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="7c209-2066">Interactive</span><span class="sxs-lookup"><span data-stu-id="7c209-2066">Interactive</span></span>

* <span data-ttu-id="7c209-2067">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2067">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="7c209-2068">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2068">Fixed errors on startup</span></span>
* <span data-ttu-id="7c209-2069">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2069">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="7c209-2070">IoT</span><span class="sxs-lookup"><span data-stu-id="7c209-2070">IoT</span></span>

* <span data-ttu-id="7c209-2071">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2071">Added support for device provisioning service</span></span>
* <span data-ttu-id="7c209-2072">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2072">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="7c209-2073">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2073">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-2074">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-2074">Monitor</span></span>

* <span data-ttu-id="7c209-2075">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2075">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="7c209-2076">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2076">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="7c209-2077">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2077">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="7c209-2078">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-2078">Network</span></span>

* <span data-ttu-id="7c209-2079">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2079">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="7c209-2080">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2080">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="7c209-2081">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-2081">Profile</span></span>

* <span data-ttu-id="7c209-2082">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2082">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="7c209-2083">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-2083">Role</span></span>

* <span data-ttu-id="7c209-2084">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2084">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="7c209-2085">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7c209-2085">Service Fabric</span></span>

* <span data-ttu-id="7c209-2086">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2086">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="7c209-2087">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2087">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-2088">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-2088">VM</span></span>

* <span data-ttu-id="7c209-2089">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="7c209-2089">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="7c209-2090">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2090">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="7c209-2091">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2091">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="7c209-2092">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2092">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="7c209-2093">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2093">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="7c209-2094">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2094">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="7c209-2095">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2095">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="7c209-2096">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2096">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="7c209-2097">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2097">December 19, 2017</span></span>

<span data-ttu-id="7c209-2098">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="7c209-2098">Version 2.0.23</span></span>

* <span data-ttu-id="7c209-2099">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2099">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="7c209-2100">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-2100">Container</span></span>

* <span data-ttu-id="7c209-2101">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2101">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="7c209-2102">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-2102">Network</span></span>

* <span data-ttu-id="7c209-2103">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2103">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="7c209-2104">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2104">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-2105">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-2105">Storage</span></span>

* <span data-ttu-id="7c209-2106">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2106">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-2107">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-2107">VM</span></span>

* <span data-ttu-id="7c209-2108">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2108">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="7c209-2109">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2109">December 5, 2017</span></span>

<span data-ttu-id="7c209-2110">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="7c209-2110">Version 2.0.22</span></span>

* <span data-ttu-id="7c209-2111">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2111">Removed `az component` commands.</span></span> <span data-ttu-id="7c209-2112">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="7c209-2112">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="7c209-2113">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-2113">Core</span></span>
* <span data-ttu-id="7c209-2114">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2114">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="7c209-2115">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2115">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-2116">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-2116">ACS</span></span>

* <span data-ttu-id="7c209-2117">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2117">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="7c209-2118">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2118">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="7c209-2119">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2119">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="7c209-2120">Advisor</span><span class="sxs-lookup"><span data-stu-id="7c209-2120">Advisor</span></span>

* <span data-ttu-id="7c209-2121">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="7c209-2121">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-2122">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-2122">Appservice</span></span>

* <span data-ttu-id="7c209-2123">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2123">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="7c209-2124">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2124">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="7c209-2125">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2125">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="7c209-2126">消費</span><span class="sxs-lookup"><span data-stu-id="7c209-2126">Consumption</span></span>

* <span data-ttu-id="7c209-2127">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2127">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="7c209-2128">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-2128">Container</span></span>

* <span data-ttu-id="7c209-2129">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2129">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-2130">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-2130">Monitor</span></span>

* <span data-ttu-id="7c209-2131">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2131">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-2132">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-2132">Resource</span></span>

* <span data-ttu-id="7c209-2133">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2133">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="7c209-2134">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-2134">Role</span></span>

* <span data-ttu-id="7c209-2135">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2135">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="7c209-2136">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2136">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="7c209-2137">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2137">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-2138">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-2138">SQL</span></span>

* <span data-ttu-id="7c209-2139">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2139">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="7c209-2140">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2140">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-2141">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-2141">VM</span></span>

* <span data-ttu-id="7c209-2142">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2142">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="7c209-2143">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2143">November 14, 2017</span></span>

<span data-ttu-id="7c209-2144">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="7c209-2144">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-2145">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-2145">ACR</span></span>

* <span data-ttu-id="7c209-2146">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2146">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="7c209-2147">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-2147">ACS</span></span>

* <span data-ttu-id="7c209-2148">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2148">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="7c209-2149">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2149">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="7c209-2150">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2150">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="7c209-2151">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2151">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="7c209-2152">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2152">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-2153">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-2153">Appservice</span></span>

* <span data-ttu-id="7c209-2154">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2154">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="7c209-2155">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2155">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="7c209-2156">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2156">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="7c209-2157">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2157">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="7c209-2158">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2158">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="7c209-2159">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="7c209-2159">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-2160">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-2160">Batch</span></span>

* <span data-ttu-id="7c209-2161">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2161">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="7c209-2162">Batchai</span><span class="sxs-lookup"><span data-stu-id="7c209-2162">Batchai</span></span>

* <span data-ttu-id="7c209-2163">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2163">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="7c209-2164">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2164">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="7c209-2165">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2165">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="7c209-2166">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2166">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="7c209-2167">クラウド</span><span class="sxs-lookup"><span data-stu-id="7c209-2167">Cloud</span></span>

* <span data-ttu-id="7c209-2168">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2168">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="7c209-2169">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-2169">Container</span></span>

* <span data-ttu-id="7c209-2170">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2170">Added support to open multiple ports</span></span>
* <span data-ttu-id="7c209-2171">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2171">Added container group restart policy</span></span>
* <span data-ttu-id="7c209-2172">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2172">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="7c209-2173">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2173">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="7c209-2174">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="7c209-2174">Data Lake Analytics</span></span>

* <span data-ttu-id="7c209-2175">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2175">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="7c209-2176">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="7c209-2176">Data Lake Store</span></span>

* <span data-ttu-id="7c209-2177">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2177">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="7c209-2178">拡張機能</span><span class="sxs-lookup"><span data-stu-id="7c209-2178">Extension</span></span>

* <span data-ttu-id="7c209-2179">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2179">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="7c209-2180">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2180">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="7c209-2181">IoT</span><span class="sxs-lookup"><span data-stu-id="7c209-2181">IoT</span></span>

* <span data-ttu-id="7c209-2182">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2182">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-2183">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-2183">Monitor</span></span>

* <span data-ttu-id="7c209-2184">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2184">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="7c209-2185">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-2185">Network</span></span>

* <span data-ttu-id="7c209-2186">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2186">Added support for CAA DNS records</span></span>
* <span data-ttu-id="7c209-2187">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2187">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="7c209-2188">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2188">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="7c209-2189">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2189">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="7c209-2190">Reservations</span><span class="sxs-lookup"><span data-stu-id="7c209-2190">Reservations</span></span>

* <span data-ttu-id="7c209-2191">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="7c209-2191">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-2192">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-2192">Resource</span></span>

* <span data-ttu-id="7c209-2193">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2193">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-2194">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-2194">SQL</span></span>

* <span data-ttu-id="7c209-2195">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2195">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-2196">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-2196">Storage</span></span>

* <span data-ttu-id="7c209-2197">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2197">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="7c209-2198">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2198">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="7c209-2199">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2199">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="7c209-2200">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2200">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="7c209-2201">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2201">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="7c209-2202">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2202">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="7c209-2203">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2203">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-2204">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-2204">VM</span></span>

* <span data-ttu-id="7c209-2205">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2205">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="7c209-2206">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2206">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="7c209-2207">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2207">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="7c209-2208">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2208">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="7c209-2209">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2209">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="7c209-2210">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2210">October 24, 2017</span></span>

<span data-ttu-id="7c209-2211">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="7c209-2211">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="7c209-2212">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-2212">Core</span></span>

* <span data-ttu-id="7c209-2213">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2213">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-2214">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-2214">ACR</span></span>

* <span data-ttu-id="7c209-2215">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2215">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="7c209-2216">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2216">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="7c209-2217">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2217">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-2218">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-2218">ACS</span></span>

* <span data-ttu-id="7c209-2219">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2219">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="7c209-2220">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2220">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-2221">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-2221">Appservice</span></span>

* <span data-ttu-id="7c209-2222">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2222">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="7c209-2223">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="7c209-2223">Component</span></span>

* <span data-ttu-id="7c209-2224">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2224">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-2225">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-2225">Monitor</span></span>

* <span data-ttu-id="7c209-2226">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2226">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-2227">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-2227">Resource</span></span>

* <span data-ttu-id="7c209-2228">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2228">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="7c209-2229">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2229">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-2230">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-2230">VM</span></span>

* <span data-ttu-id="7c209-2231">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2231">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="7c209-2232">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2232">October 9, 2017</span></span>

<span data-ttu-id="7c209-2233">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="7c209-2233">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="7c209-2234">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-2234">Core</span></span>

* <span data-ttu-id="7c209-2235">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2235">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-2236">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-2236">Appservice</span></span>

* <span data-ttu-id="7c209-2237">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2237">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-2238">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-2238">Batch</span></span>

* <span data-ttu-id="7c209-2239">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2239">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="7c209-2240">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2240">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="7c209-2241">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2241">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="7c209-2242">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2242">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="7c209-2243">Batchai</span><span class="sxs-lookup"><span data-stu-id="7c209-2243">Batchai</span></span>

* <span data-ttu-id="7c209-2244">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="7c209-2244">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="7c209-2245">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c209-2245">Keyvault</span></span>

* <span data-ttu-id="7c209-2246">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2246">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="7c209-2247">(#4448)</span><span class="sxs-lookup"><span data-stu-id="7c209-2247">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="7c209-2248">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-2248">Network</span></span>

* <span data-ttu-id="7c209-2249">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2249">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="7c209-2250">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2250">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-2251">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-2251">Resource</span></span>

* <span data-ttu-id="7c209-2252">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2252">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="7c209-2253">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2253">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="7c209-2254">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2254">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="7c209-2255">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2255">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-2256">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-2256">Sql</span></span>

* <span data-ttu-id="7c209-2257">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2257">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="7c209-2258">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2258">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="7c209-2259">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2259">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-2260">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-2260">Storage</span></span>

* <span data-ttu-id="7c209-2261">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2261">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-2262">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-2262">Vm</span></span>

* <span data-ttu-id="7c209-2263">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2263">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="7c209-2264">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2264">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="7c209-2265">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2265">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="7c209-2266">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2266">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="7c209-2267">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2267">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="7c209-2268">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2268">September 22, 2017</span></span>

<span data-ttu-id="7c209-2269">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="7c209-2269">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-2270">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-2270">Resource</span></span>

* <span data-ttu-id="7c209-2271">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2271">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="7c209-2272">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2272">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="7c209-2273">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2273">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="7c209-2274">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2274">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="7c209-2275">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-2275">Network</span></span>

* <span data-ttu-id="7c209-2276">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2276">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="7c209-2277">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2277">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="7c209-2278">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2278">Added `asg` application security group commands</span></span>
* <span data-ttu-id="7c209-2279">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2279">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="7c209-2280">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2280">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="7c209-2281">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2281">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="7c209-2282">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2282">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-2283">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-2283">Storage</span></span>

* <span data-ttu-id="7c209-2284">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2284">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="7c209-2285">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="7c209-2285">Eventgrid</span></span>

* <span data-ttu-id="7c209-2286">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2286">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-2287">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-2287">SQL</span></span>

* <span data-ttu-id="7c209-2288">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2288">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="7c209-2289">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="7c209-2289">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="7c209-2290">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2290">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="7c209-2291">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c209-2291">Keyvault</span></span>

* <span data-ttu-id="7c209-2292">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2292">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-2293">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-2293">VM</span></span>

* <span data-ttu-id="7c209-2294">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2294">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="7c209-2295">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2295">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="7c209-2296">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2296">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="7c209-2297">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2297">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="7c209-2298">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2298">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="7c209-2299">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2299">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-2300">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-2300">ACS</span></span>

* <span data-ttu-id="7c209-2301">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2301">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-2302">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-2302">Appservice</span></span>

* <span data-ttu-id="7c209-2303">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2303">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="7c209-2304">バックアップ</span><span class="sxs-lookup"><span data-stu-id="7c209-2304">Backup</span></span>

* <span data-ttu-id="7c209-2305">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="7c209-2305">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="7c209-2306">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2306">September 11, 2017</span></span>

<span data-ttu-id="7c209-2307">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="7c209-2307">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="7c209-2308">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-2308">Core</span></span>

* <span data-ttu-id="7c209-2309">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2309">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="7c209-2310">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2310">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-2311">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-2311">Acs</span></span>

* <span data-ttu-id="7c209-2312">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2312">Added `acs list-locations` command</span></span>
* <span data-ttu-id="7c209-2313">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2313">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-2314">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-2314">Appservice</span></span>

* <span data-ttu-id="7c209-2315">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2315">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="7c209-2316">CDN</span><span class="sxs-lookup"><span data-stu-id="7c209-2316">CDN</span></span>

* <span data-ttu-id="7c209-2317">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2317">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="7c209-2318">拡張機能</span><span class="sxs-lookup"><span data-stu-id="7c209-2318">Extension</span></span>

* <span data-ttu-id="7c209-2319">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="7c209-2319">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="7c209-2320">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c209-2320">Keyvault</span></span>

* <span data-ttu-id="7c209-2321">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2321">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="7c209-2322">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-2322">Network</span></span>

* <span data-ttu-id="7c209-2323">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2323">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="7c209-2324">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2324">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="7c209-2325">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2325">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="7c209-2326">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2326">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="7c209-2327">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2327">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-2328">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-2328">Resource</span></span>

* <span data-ttu-id="7c209-2329">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="7c209-2329">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="7c209-2330">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="7c209-2330">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="7c209-2331">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="7c209-2331">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="7c209-2332">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2332">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-2333">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-2333">SQL</span></span>

* <span data-ttu-id="7c209-2334">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2334">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-2335">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-2335">VM</span></span>

* <span data-ttu-id="7c209-2336">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="7c209-2336">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="7c209-2337">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="7c209-2337">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="7c209-2338">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2338">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="7c209-2339">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="7c209-2339">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="7c209-2340">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="7c209-2340">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="7c209-2341">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2341">August 31, 2017</span></span>

<span data-ttu-id="7c209-2342">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="7c209-2342">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="7c209-2343">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c209-2343">Keyvault</span></span>

* <span data-ttu-id="7c209-2344">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2344">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="7c209-2345">SF</span><span class="sxs-lookup"><span data-stu-id="7c209-2345">Sf</span></span>

* <span data-ttu-id="7c209-2346">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="7c209-2346">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-2347">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-2347">Storage</span></span>

* <span data-ttu-id="7c209-2348">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2348">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="7c209-2349">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="7c209-2349">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="7c209-2350">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2350">August 28, 2017</span></span>

<span data-ttu-id="7c209-2351">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="7c209-2351">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="7c209-2352">CLI</span><span class="sxs-lookup"><span data-stu-id="7c209-2352">CLI</span></span>

* <span data-ttu-id="7c209-2353">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2353">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-2354">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-2354">ACS</span></span>

* <span data-ttu-id="7c209-2355">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2355">Corrected preview regions</span></span>
* <span data-ttu-id="7c209-2356">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2356">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="7c209-2357">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2357">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-2358">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-2358">Appservice</span></span>

* <span data-ttu-id="7c209-2359">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2359">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="7c209-2360">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2360">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="7c209-2361">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2361">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="7c209-2362">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2362">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="7c209-2363">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="7c209-2363">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="7c209-2364">IoT</span><span class="sxs-lookup"><span data-stu-id="7c209-2364">IoT</span></span>

* <span data-ttu-id="7c209-2365">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2365">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="7c209-2366">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-2366">Network</span></span>

* <span data-ttu-id="7c209-2367">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2367">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="7c209-2368">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2368">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="7c209-2369">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2369">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="7c209-2370">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2370">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="7c209-2371">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2371">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="7c209-2372">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-2372">Profile</span></span>

* <span data-ttu-id="7c209-2373">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2373">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="7c209-2374">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7c209-2374">Service Fabric</span></span>

* <span data-ttu-id="7c209-2375">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="7c209-2375">Preview release</span></span>
* <span data-ttu-id="7c209-2376">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2376">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="7c209-2377">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2377">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="7c209-2378">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2378">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-2379">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-2379">Storage</span></span>

* <span data-ttu-id="7c209-2380">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2380">Enabled setting blob tier</span></span>
* <span data-ttu-id="7c209-2381">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2381">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="7c209-2382">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2382">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="7c209-2383">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2383">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="7c209-2384">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2384">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="7c209-2385">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="7c209-2385">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-2386">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-2386">VM</span></span>

* <span data-ttu-id="7c209-2387">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2387">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="7c209-2388">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2388">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="7c209-2389">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2389">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="7c209-2390">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2390">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="7c209-2391">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2391">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="7c209-2392">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2392">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="7c209-2393">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2393">August 15, 2017</span></span>

<span data-ttu-id="7c209-2394">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="7c209-2394">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-2395">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-2395">ACS</span></span>

* <span data-ttu-id="7c209-2396">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2396">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-2397">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-2397">Appservice</span></span>

* <span data-ttu-id="7c209-2398">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2398">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="7c209-2399">Event Grid</span><span class="sxs-lookup"><span data-stu-id="7c209-2399">Event Grid</span></span>

* <span data-ttu-id="7c209-2400">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2400">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="7c209-2401">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2401">August 11, 2017</span></span>

<span data-ttu-id="7c209-2402">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="7c209-2402">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-2403">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-2403">ACS</span></span>

* <span data-ttu-id="7c209-2404">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2404">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-2405">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-2405">Batch</span></span>

* <span data-ttu-id="7c209-2406">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2406">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="7c209-2407">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2407">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="7c209-2408">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2408">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="7c209-2409">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2409">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="7c209-2410">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2410">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="7c209-2411">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2411">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="7c209-2412">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="7c209-2412">Component</span></span>

* <span data-ttu-id="7c209-2413">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2413">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="7c209-2414">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7c209-2414">Container</span></span>

* <span data-ttu-id="7c209-2415">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2415">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="7c209-2416">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="7c209-2416">Data Lake Store</span></span>

* <span data-ttu-id="7c209-2417">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2417">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="7c209-2418">Event Grid</span><span class="sxs-lookup"><span data-stu-id="7c209-2418">Event Grid</span></span>

* <span data-ttu-id="7c209-2419">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="7c209-2419">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="7c209-2420">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-2420">Network</span></span>

* <span data-ttu-id="7c209-2421">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2421">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="7c209-2422">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2422">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="7c209-2423">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2423">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="7c209-2424">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2424">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="7c209-2425">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-2425">Profile</span></span>

* <span data-ttu-id="7c209-2426">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2426">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-2427">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-2427">Storage</span></span>

* <span data-ttu-id="7c209-2428">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="7c209-2428">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-2429">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-2429">VM</span></span>

* <span data-ttu-id="7c209-2430">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2430">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="7c209-2431">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2431">Exposed `list-skus` command</span></span>
* <span data-ttu-id="7c209-2432">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2432">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="7c209-2433">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="7c209-2433">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="7c209-2434">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2434">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="7c209-2435">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2435">July 28, 2017</span></span>

<span data-ttu-id="7c209-2436">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="7c209-2436">Version 2.0.12</span></span>

* <span data-ttu-id="7c209-2437">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2437">Added container commands</span></span>
* <span data-ttu-id="7c209-2438">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2438">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="7c209-2439">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-2439">Core</span></span>

* <span data-ttu-id="7c209-2440">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="7c209-2440">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="7c209-2441">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2441">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="7c209-2442">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="7c209-2442">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="7c209-2443">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="7c209-2443">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="7c209-2444">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="7c209-2444">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="7c209-2445">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="7c209-2445">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="7c209-2446">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="7c209-2446">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="7c209-2447">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="7c209-2447">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="7c209-2448">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="7c209-2448">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="7c209-2449">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="7c209-2449">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="7c209-2450">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="7c209-2450">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="7c209-2451">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="7c209-2451">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="7c209-2452">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2452">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="7c209-2453">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2453">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="7c209-2454">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2454">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="7c209-2455">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="7c209-2455">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="7c209-2456">ACR</span><span class="sxs-lookup"><span data-stu-id="7c209-2456">ACR</span></span>

* <span data-ttu-id="7c209-2457">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2457">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="7c209-2458">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2458">Support SKU update for managed registries</span></span>
* <span data-ttu-id="7c209-2459">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2459">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="7c209-2460">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2460">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="7c209-2461">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2461">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="7c209-2462">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2462">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-2463">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-2463">ACS</span></span>

* <span data-ttu-id="7c209-2464">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2464">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-2465">Appservice</span><span class="sxs-lookup"><span data-stu-id="7c209-2465">Appservice</span></span>

* <span data-ttu-id="7c209-2466">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2466">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="7c209-2467">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2467">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="7c209-2468">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="7c209-2468">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="7c209-2469">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="7c209-2469">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="7c209-2470">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="7c209-2470">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="7c209-2471">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="7c209-2471">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="7c209-2472">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="7c209-2472">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="7c209-2473">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="7c209-2473">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="7c209-2474">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2474">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="7c209-2475">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="7c209-2475">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="7c209-2476">Batch</span><span class="sxs-lookup"><span data-stu-id="7c209-2476">Batch</span></span>

* <span data-ttu-id="7c209-2477">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2477">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="7c209-2478">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2478">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="7c209-2479">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2479">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="7c209-2480">CDN</span><span class="sxs-lookup"><span data-stu-id="7c209-2480">CDN</span></span>

* <span data-ttu-id="7c209-2481">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2481">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="7c209-2482">クラウド</span><span class="sxs-lookup"><span data-stu-id="7c209-2482">Cloud</span></span>

* <span data-ttu-id="7c209-2483">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2483">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="7c209-2484">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="7c209-2484">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="7c209-2485">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2485">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="7c209-2486">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2486">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="7c209-2487">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2487">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="7c209-2488">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="7c209-2488">CosmosDB</span></span>

* <span data-ttu-id="7c209-2489">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2489">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="7c209-2490">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2490">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="7c209-2491">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="7c209-2491">Data Lake Analytics</span></span>

* <span data-ttu-id="7c209-2492">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2492">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="7c209-2493">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2493">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="7c209-2494">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2494">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="7c209-2495">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="7c209-2495">Data Lake Store</span></span>

* <span data-ttu-id="7c209-2496">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2496">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="7c209-2497">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2497">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="7c209-2498">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2498">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="7c209-2499">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="7c209-2499">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="7c209-2500">対話</span><span class="sxs-lookup"><span data-stu-id="7c209-2500">Interactive</span></span>

* <span data-ttu-id="7c209-2501">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2501">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="7c209-2502">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="7c209-2502">Increased test coverage</span></span>
* <span data-ttu-id="7c209-2503">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2503">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="7c209-2504">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="7c209-2504">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="7c209-2505">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="7c209-2505">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="7c209-2506">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="7c209-2506">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="7c209-2507">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="7c209-2507">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="7c209-2508">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2508">Added `--progress` flag</span></span>
* <span data-ttu-id="7c209-2509">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2509">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="7c209-2510">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="7c209-2510">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="7c209-2511">IoT</span><span class="sxs-lookup"><span data-stu-id="7c209-2511">IoT</span></span>

* <span data-ttu-id="7c209-2512">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2512">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="7c209-2513">(#3934)</span><span class="sxs-lookup"><span data-stu-id="7c209-2513">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="7c209-2514">Key Vault</span><span class="sxs-lookup"><span data-stu-id="7c209-2514">Key vault</span></span>

* <span data-ttu-id="7c209-2515">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2515">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="7c209-2516">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="7c209-2516">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="7c209-2517">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="7c209-2517">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="7c209-2518">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="7c209-2518">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="7c209-2519">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="7c209-2519">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="7c209-2520">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="7c209-2520">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="7c209-2521">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2521">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="7c209-2522">(#3307)</span><span class="sxs-lookup"><span data-stu-id="7c209-2522">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="7c209-2523">ラボ</span><span class="sxs-lookup"><span data-stu-id="7c209-2523">Lab</span></span>

* <span data-ttu-id="7c209-2524">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2524">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="7c209-2525">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2525">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-2526">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-2526">Monitor</span></span>

* <span data-ttu-id="7c209-2527">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="7c209-2527">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="7c209-2528">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2528">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="7c209-2529">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2529">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="7c209-2530">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2530">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="7c209-2531">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2531">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="7c209-2532">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2532">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="7c209-2533">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2533">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="7c209-2534">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="7c209-2534">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="7c209-2535">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2535">`location` no longer required</span></span>
  * <span data-ttu-id="7c209-2536">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="7c209-2536">Add name and ID support for target</span></span>
  * <span data-ttu-id="7c209-2537">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="7c209-2537">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="7c209-2538">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2538">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="7c209-2539">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2539">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="7c209-2540">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="7c209-2540">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="7c209-2541">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2541">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="7c209-2542">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2542">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="7c209-2543">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-2543">Network</span></span>

* <span data-ttu-id="7c209-2544">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2544">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="7c209-2545">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2545">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="7c209-2546">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2546">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="7c209-2547">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2547">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="7c209-2548">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2548">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="7c209-2549">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2549">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="7c209-2550">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2550">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="7c209-2551">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2551">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="7c209-2552">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2552">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="7c209-2553">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2553">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="7c209-2554">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2554">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="7c209-2555">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2555">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="7c209-2556">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2556">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="7c209-2557">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2557">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="7c209-2558">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2558">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="7c209-2559">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2559">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="7c209-2560">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2560">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="7c209-2561">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2561">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="7c209-2562">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2562">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="7c209-2563">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2563">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="7c209-2564">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2564">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="7c209-2565">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2565">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="7c209-2566">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2566">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="7c209-2567">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="7c209-2567">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="7c209-2568">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="7c209-2568">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="7c209-2569">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="7c209-2569">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="7c209-2570">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="7c209-2570">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="7c209-2571">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-2571">Profile</span></span>

* <span data-ttu-id="7c209-2572">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2572">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="7c209-2573">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2573">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="7c209-2574">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="7c209-2574">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="7c209-2575">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2575">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="7c209-2576">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2576">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="7c209-2577">RDBMS</span><span class="sxs-lookup"><span data-stu-id="7c209-2577">RDBMS</span></span>

* <span data-ttu-id="7c209-2578">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="7c209-2578">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="7c209-2579">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="7c209-2579">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="7c209-2580">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="7c209-2580">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="7c209-2581">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="7c209-2581">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-2582">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-2582">Resource</span></span>

* <span data-ttu-id="7c209-2583">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2583">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="7c209-2584">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2584">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="7c209-2585">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2585">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="7c209-2586">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2586">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="7c209-2587">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="7c209-2587">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="7c209-2588">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2588">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="7c209-2589">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="7c209-2589">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="7c209-2590">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2590">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="7c209-2591">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-2591">Role</span></span>

* <span data-ttu-id="7c209-2592">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2592">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="7c209-2593">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="7c209-2593">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="7c209-2594">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="7c209-2594">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="7c209-2595">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="7c209-2595">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="7c209-2596">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2596">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="7c209-2597">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7c209-2597">Service Fabric</span></span>
* <span data-ttu-id="7c209-2598">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="7c209-2598">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="7c209-2599">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="7c209-2599">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="7c209-2600">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="7c209-2600">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-2601">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-2601">SQL</span></span>

* <span data-ttu-id="7c209-2602">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2602">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="7c209-2603">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2603">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="7c209-2604">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2604">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-2605">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-2605">Storage</span></span>

* <span data-ttu-id="7c209-2606">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="7c209-2606">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="7c209-2607">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2607">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="7c209-2608">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="7c209-2608">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="7c209-2609">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="7c209-2609">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="7c209-2610">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="7c209-2610">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="7c209-2611">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="7c209-2611">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-2612">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-2612">VM</span></span>

* <span data-ttu-id="7c209-2613">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2613">Support configuring nsg</span></span>
* <span data-ttu-id="7c209-2614">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2614">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="7c209-2615">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="7c209-2615">Support managed service identities</span></span>
* <span data-ttu-id="7c209-2616">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2616">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="7c209-2617">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="7c209-2617">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="7c209-2618">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2618">May 10, 2017</span></span>

<span data-ttu-id="7c209-2619">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="7c209-2619">Version 2.0.6</span></span>

* <span data-ttu-id="7c209-2620">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2620">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="7c209-2621">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2621">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="7c209-2622">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2622">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="7c209-2623">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2623">Include Cognitive Services module</span></span>
* <span data-ttu-id="7c209-2624">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2624">Include Service Fabric module</span></span>
* <span data-ttu-id="7c209-2625">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="7c209-2625">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="7c209-2626">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2626">Add support for CDN commands</span></span>
* <span data-ttu-id="7c209-2627">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2627">Remove Container module</span></span>
* <span data-ttu-id="7c209-2628">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="7c209-2628">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="7c209-2629">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="7c209-2629">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="7c209-2630">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-2630">Core</span></span>

* <span data-ttu-id="7c209-2631">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="7c209-2631">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="7c209-2632">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="7c209-2632">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="7c209-2633">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="7c209-2633">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="7c209-2634">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="7c209-2634">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="7c209-2635">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="7c209-2635">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="7c209-2636">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="7c209-2636">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="7c209-2637">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="7c209-2637">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="7c209-2638">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="7c209-2638">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="7c209-2639">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="7c209-2639">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="7c209-2640">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="7c209-2640">core: Improved performance</span></span>
* <span data-ttu-id="7c209-2641">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="7c209-2641">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="7c209-2642">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="7c209-2642">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-2643">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-2643">ACS</span></span>

* <span data-ttu-id="7c209-2644">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2644">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="7c209-2645">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2645">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="7c209-2646">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2646">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="7c209-2647">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="7c209-2647">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-2648">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-2648">AppService</span></span>

* <span data-ttu-id="7c209-2649">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2649">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="7c209-2650">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2650">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="7c209-2651">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="7c209-2651">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="7c209-2652">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2652">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="7c209-2653">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2653">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="7c209-2654">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="7c209-2654">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="7c209-2655">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="7c209-2655">support slot swap with preview</span></span>
* <span data-ttu-id="7c209-2656">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="7c209-2656">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="7c209-2657">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="7c209-2657">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="7c209-2658">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="7c209-2658">CosmosDB</span></span>

* <span data-ttu-id="7c209-2659">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2659">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="7c209-2660">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2660">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="7c209-2661">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2661">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="7c209-2662">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2662">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="7c209-2663">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="7c209-2663">Data Lake Analytics</span></span>

* <span data-ttu-id="7c209-2664">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2664">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="7c209-2665">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2665">Add support for new catalog item type: package.</span></span> <span data-ttu-id="7c209-2666">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="7c209-2666">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="7c209-2667">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="7c209-2667">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="7c209-2668">テーブル</span><span class="sxs-lookup"><span data-stu-id="7c209-2668">Table</span></span>
  * <span data-ttu-id="7c209-2669">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="7c209-2669">Table valued function</span></span>
  * <span data-ttu-id="7c209-2670">表示</span><span class="sxs-lookup"><span data-stu-id="7c209-2670">View</span></span>
  * <span data-ttu-id="7c209-2671">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="7c209-2671">Table Statistics.</span></span> <span data-ttu-id="7c209-2672">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="7c209-2672">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="7c209-2673">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="7c209-2673">Data Lake Store</span></span>

* <span data-ttu-id="7c209-2674">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2674">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="7c209-2675">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="7c209-2675">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="7c209-2676">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="7c209-2676">missed help for access show.</span></span> <span data-ttu-id="7c209-2677">追加しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2677">adding it.</span></span> <span data-ttu-id="7c209-2678">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="7c209-2678">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="7c209-2679">検索</span><span class="sxs-lookup"><span data-stu-id="7c209-2679">Find</span></span>

* <span data-ttu-id="7c209-2680">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2680">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="7c209-2681">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c209-2681">KeyVault</span></span>

* <span data-ttu-id="7c209-2682">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2682">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="7c209-2683">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2683">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="7c209-2684">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="7c209-2684">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="7c209-2685">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2685">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="7c209-2686">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="7c209-2686">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="7c209-2687">ラボ</span><span class="sxs-lookup"><span data-stu-id="7c209-2687">Lab</span></span>

* <span data-ttu-id="7c209-2688">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2688">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="7c209-2689">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2689">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="7c209-2690">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2690">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="7c209-2691">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2691">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="7c209-2692">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2692">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="7c209-2693">監視</span><span class="sxs-lookup"><span data-stu-id="7c209-2693">Monitor</span></span>

* <span data-ttu-id="7c209-2694">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="7c209-2694">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="7c209-2695">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="7c209-2695">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="7c209-2696">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-2696">Network</span></span>

* <span data-ttu-id="7c209-2697">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2697">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="7c209-2698">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2698">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="7c209-2699">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2699">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="7c209-2700">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2700">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="7c209-2701">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2701">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="7c209-2702">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2702">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="7c209-2703">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2703">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="7c209-2704">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2704">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="7c209-2705">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2705">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="7c209-2706">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2706">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="7c209-2707">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2707">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="7c209-2708">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2708">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="7c209-2709">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2709">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="7c209-2710">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2710">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="7c209-2711">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="7c209-2711">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="7c209-2712">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2712">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="7c209-2713">プロファイル</span><span class="sxs-lookup"><span data-stu-id="7c209-2713">Profile</span></span>

* <span data-ttu-id="7c209-2714">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="7c209-2714">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="7c209-2715">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="7c209-2715">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="7c209-2716">Redis</span><span class="sxs-lookup"><span data-stu-id="7c209-2716">Redis</span></span>

* <span data-ttu-id="7c209-2717">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2717">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="7c209-2718">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2718">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="7c209-2719">リソース</span><span class="sxs-lookup"><span data-stu-id="7c209-2719">Resource</span></span>

* <span data-ttu-id="7c209-2720">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="7c209-2720">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="7c209-2721">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="7c209-2721">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="7c209-2722">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="7c209-2722">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="7c209-2723">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2723">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="7c209-2724">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="7c209-2724">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="7c209-2725">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2725">Add docs for az lock update.</span></span> <span data-ttu-id="7c209-2726">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="7c209-2726">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="7c209-2727">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="7c209-2727">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="7c209-2728">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="7c209-2728">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="7c209-2729">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="7c209-2729">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="7c209-2730">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="7c209-2730">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="7c209-2731">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="7c209-2731">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="7c209-2732">Role</span><span class="sxs-lookup"><span data-stu-id="7c209-2732">Role</span></span>

* <span data-ttu-id="7c209-2733">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="7c209-2733">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="7c209-2734">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="7c209-2734">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="7c209-2735">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="7c209-2735">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="7c209-2736">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="7c209-2736">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="7c209-2737">SQL</span><span class="sxs-lookup"><span data-stu-id="7c209-2737">SQL</span></span>

* <span data-ttu-id="7c209-2738">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="7c209-2738">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="7c209-2739">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="7c209-2739">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="7c209-2740">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-2740">Storage</span></span>

* <span data-ttu-id="7c209-2741">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="7c209-2741">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="7c209-2742">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2742">Add support for incremental blob copy</span></span>
* <span data-ttu-id="7c209-2743">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2743">Add support for large block blob upload</span></span>
* <span data-ttu-id="7c209-2744">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="7c209-2744">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-2745">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-2745">VM</span></span>

* <span data-ttu-id="7c209-2746">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="7c209-2746">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="7c209-2747">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="7c209-2747">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="7c209-2748">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="7c209-2748">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="7c209-2749">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="7c209-2749">az vm/vmss disk</span></span>
  3. <span data-ttu-id="7c209-2750">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="7c209-2750">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="7c209-2751">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="7c209-2751">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="7c209-2752">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="7c209-2752">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="7c209-2753">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2753">April 3, 2017</span></span>

<span data-ttu-id="7c209-2754">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="7c209-2754">Version 2.0.2</span></span>

<span data-ttu-id="7c209-2755">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="7c209-2755">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="7c209-2756">コア</span><span class="sxs-lookup"><span data-stu-id="7c209-2756">Core</span></span>

* <span data-ttu-id="7c209-2757">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="7c209-2757">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="7c209-2758">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="7c209-2758">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="7c209-2759">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="7c209-2759">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="7c209-2760">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="7c209-2760">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="7c209-2761">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="7c209-2761">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="7c209-2762">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="7c209-2762">Add prompting for missing template parameters.</span></span> <span data-ttu-id="7c209-2763">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="7c209-2763">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="7c209-2764">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="7c209-2764">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="7c209-2765">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="7c209-2765">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="7c209-2766">ACS</span><span class="sxs-lookup"><span data-stu-id="7c209-2766">ACS</span></span>

* <span data-ttu-id="7c209-2767">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="7c209-2767">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="7c209-2768">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="7c209-2768">Add support for ssh key password prompting.</span></span> <span data-ttu-id="7c209-2769">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="7c209-2769">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="7c209-2770">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="7c209-2770">Add support for windows clusters.</span></span> <span data-ttu-id="7c209-2771">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="7c209-2771">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="7c209-2772">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="7c209-2772">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="7c209-2773">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="7c209-2773">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="7c209-2774">AppService</span><span class="sxs-lookup"><span data-stu-id="7c209-2774">AppService</span></span>

* <span data-ttu-id="7c209-2775">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="7c209-2775">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="7c209-2776">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="7c209-2776">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="7c209-2777">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="7c209-2777">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="7c209-2778">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="7c209-2778">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="7c209-2779">DataLake</span><span class="sxs-lookup"><span data-stu-id="7c209-2779">DataLake</span></span>

* <span data-ttu-id="7c209-2780">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="7c209-2780">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="7c209-2781">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="7c209-2781">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="7c209-2782">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="7c209-2782">DocuemntDB</span></span>

* <span data-ttu-id="7c209-2783">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="7c209-2783">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="7c209-2784">VM</span><span class="sxs-lookup"><span data-stu-id="7c209-2784">VM</span></span>

* <span data-ttu-id="7c209-2785">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="7c209-2785">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="7c209-2786">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="7c209-2786">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="7c209-2787">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="7c209-2787">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="7c209-2788">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="7c209-2788">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="7c209-2789">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="7c209-2789">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="7c209-2790">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="7c209-2790">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="7c209-2791">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="7c209-2791">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="7c209-2792">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="7c209-2792">February 27, 2017</span></span>

<span data-ttu-id="7c209-2793">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="7c209-2793">Version 2.0.0</span></span>

<span data-ttu-id="7c209-2794">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="7c209-2794">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="7c209-2795">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="7c209-2795">Container Service (acs)</span></span>
- <span data-ttu-id="7c209-2796">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="7c209-2796">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="7c209-2797">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="7c209-2797">Networking</span></span>
- <span data-ttu-id="7c209-2798">Storage</span><span class="sxs-lookup"><span data-stu-id="7c209-2798">Storage</span></span>

<span data-ttu-id="7c209-2799">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="7c209-2799">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="7c209-2800">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="7c209-2800">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="7c209-2801">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="7c209-2801">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="7c209-2802">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="7c209-2802">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="7c209-2803">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="7c209-2803">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="7c209-2804">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="7c209-2804">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="7c209-2805">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="7c209-2805">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="7c209-2806">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="7c209-2806">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="7c209-2807">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="7c209-2807">Provide feedback from the command line with the `az feedback` command</span></span>

