---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 03/10/2020
ms.topic: article
ms.service: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: ff3a1da2343b96bfd78b20742c2c15707932f3d7
ms.sourcegitcommit: 21bc2a7125b6c38bf1c4def0a0e66e6673de4805
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/10/2020
ms.locfileid: "79037950"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="16653-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="16653-103">Azure CLI release notes</span></span>

## <a name="march-10-2020"></a><span data-ttu-id="16653-104">2020 年 3 月 10 日</span><span class="sxs-lookup"><span data-stu-id="16653-104">March 10, 2020</span></span>

<span data-ttu-id="16653-105">バージョン 2.2.0</span><span class="sxs-lookup"><span data-stu-id="16653-105">Version 2.2.0</span></span>

### <a name="acr"></a><span data-ttu-id="16653-106">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-106">ACR</span></span>

* <span data-ttu-id="16653-107">修正: `az acr login` で誤ってエラーが発生する</span><span class="sxs-lookup"><span data-stu-id="16653-107">Fix: `az acr login` wrongly raise error</span></span>
* <span data-ttu-id="16653-108">新しいコマンド `az acr helm install-cli` を追加</span><span class="sxs-lookup"><span data-stu-id="16653-108">Add new command `az acr helm install-cli`</span></span>
* <span data-ttu-id="16653-109">プライベート リンクと CMK のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="16653-109">Add private link and CMK support</span></span>
* <span data-ttu-id="16653-110">'private-link-resource list' コマンドの追加</span><span class="sxs-lookup"><span data-stu-id="16653-110">add 'private-link-resource list' command</span></span>

### <a name="aks"></a><span data-ttu-id="16653-111">AKS</span><span class="sxs-lookup"><span data-stu-id="16653-111">AKS</span></span>

* <span data-ttu-id="16653-112">クラウド シェルでの aks browse の修正</span><span class="sxs-lookup"><span data-stu-id="16653-112">fix the aks browse in cloud shell</span></span>
* <span data-ttu-id="16653-113">az aks:addon および agentpool NoneType エラーの監視を修正</span><span class="sxs-lookup"><span data-stu-id="16653-113">az aks: Fix monitoring addon and agentpool NoneType errors</span></span>
* <span data-ttu-id="16653-114">Azure Kubernetes クラスターの作成時にノード プールに --nodepool-tags を追加</span><span class="sxs-lookup"><span data-stu-id="16653-114">Add --nodepool-tags to node pool when creating azure kubernetes cluster</span></span>
* <span data-ttu-id="16653-115">クラスターへの nodepool の追加または更新時に --tags を追加</span><span class="sxs-lookup"><span data-stu-id="16653-115">Add --tags when adding or updating a nodepool to cluster</span></span>
* <span data-ttu-id="16653-116">aks create: `--enable-private-cluster` の追加</span><span class="sxs-lookup"><span data-stu-id="16653-116">aks create: add `--enable-private-cluster`</span></span>
* <span data-ttu-id="16653-117">Azure Kubernetes クラスターの作成時に --nodepool-labels を追加</span><span class="sxs-lookup"><span data-stu-id="16653-117">add --nodepool-labels when creating azure kubernetes cluster</span></span>
* <span data-ttu-id="16653-118">Azure Kubernetes クラスターへの新しい nodepool 追加時に --labels を追加</span><span class="sxs-lookup"><span data-stu-id="16653-118">add --labels when adding a new nodepool to azure kubernetes cluster</span></span>
* <span data-ttu-id="16653-119">ダッシュボード URL に欠落していた / を追加</span><span class="sxs-lookup"><span data-stu-id="16653-119">add missing / in the dashboard url</span></span>
* <span data-ttu-id="16653-120">マネージド ID を有効にする aks クラスターの作成のサポート</span><span class="sxs-lookup"><span data-stu-id="16653-120">Support create aks clusters enabling managed identity</span></span>
* <span data-ttu-id="16653-121">az aks:ネットワーク プラグインが "azure" または "kubernet" のいずれかであることを検証</span><span class="sxs-lookup"><span data-stu-id="16653-121">az aks: Validate network plugin to be either "azure" or "kubenet"</span></span>
* <span data-ttu-id="16653-122">az aks:aad セッション キーのサポートの追加</span><span class="sxs-lookup"><span data-stu-id="16653-122">az aks: Add aad session key support</span></span>
* <span data-ttu-id="16653-123">[重大な変更] az aks: omsagent での GF と BF に対する msi 変更のサポート (コンテナー監視)(#1)</span><span class="sxs-lookup"><span data-stu-id="16653-123">[BREAKING CHANGE] az aks: support msi changes for GF and BF for omsagent (Container monitoring)(#1)</span></span>
* <span data-ttu-id="16653-124">az aks use-dev-spaces:Azure Dev Spaces コントローラー上に作成されたエンドポイントをカスタマイズするために、use-dev-spaces コマンドにエンドポイントの種類オプションを追加</span><span class="sxs-lookup"><span data-stu-id="16653-124">az aks use-dev-spaces: Adding endpoint type option to the use-dev-spaces command to customize the endpoint created on an Azure Dev Spaces controller</span></span>

### <a name="appconfig"></a><span data-ttu-id="16653-125">AppConfig</span><span class="sxs-lookup"><span data-stu-id="16653-125">AppConfig</span></span>

* <span data-ttu-id="16653-126">keyvault 参照および機能の追加のための "kv set" を使用したブロック解除</span><span class="sxs-lookup"><span data-stu-id="16653-126">Unblock using "kv set" to add keyvault reference and feature …</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-127">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-127">AppService</span></span>

* <span data-ttu-id="16653-128">az webapp create:--runtime を指定したコマンドの実行時の問題を修正</span><span class="sxs-lookup"><span data-stu-id="16653-128">az webapp create : Fix issue when running the command with --runtime</span></span>
* <span data-ttu-id="16653-129">az functionapp deployment source config-zip:リソース グループまたは関数名が無効であるか存在しない場合のエラー メッセージの追加</span><span class="sxs-lookup"><span data-stu-id="16653-129">az functionapp deployment source config-zip: Add an error message if resource group or function name are invalid/don't exist</span></span>
* <span data-ttu-id="16653-130">functionapp create:`functionapp create` で表示される警告メッセージの修正 (現在、これは`--functions_version` フラグを示しますが、誤ってフラグ名の `-` ではなく `_` を使用します)</span><span class="sxs-lookup"><span data-stu-id="16653-130">functionapp create: Fix the warning message that appears with `functionapp create` today which cites a `--functions_version` flag but erroneously uses a `_` instead of a `-` in the flag name</span></span>
* <span data-ttu-id="16653-131">az functionapp create:Linux 関数アプリに linuxFxVersion とコンテナー イメージ名が設定されていた方法を更新</span><span class="sxs-lookup"><span data-stu-id="16653-131">az functionapp create: Updated the way linuxFxVersion and container image name were being set for linux function apps</span></span>
* <span data-ttu-id="16653-132">az functionapp deployment source config-zip:zip デプロイ中にアプリ設定の変更の競合状態によって発生する問題 (デプロイ時に 5xx エラーが表示される) を修正</span><span class="sxs-lookup"><span data-stu-id="16653-132">az functionapp deployment source config-zip: Fix an issue caused by app settings change racing condition during zip deploy, giving 5xx errors during deployment</span></span>
* <span data-ttu-id="16653-133">#5720946 の修正: az webapp backup で名前の設定に失敗する</span><span class="sxs-lookup"><span data-stu-id="16653-133">Fix #5720946: az webapp backup fails to set name</span></span>

### <a name="arm"></a><span data-ttu-id="16653-134">ARM</span><span class="sxs-lookup"><span data-stu-id="16653-134">ARM</span></span>

* <span data-ttu-id="16653-135">az resource:リソース モジュールの例の改善</span><span class="sxs-lookup"><span data-stu-id="16653-135">az resource: Improve the examples of the resource module</span></span>
* <span data-ttu-id="16653-136">az policy assignment list:管理グループ スコープでのポリシー割り当ての一覧表示をサポート</span><span class="sxs-lookup"><span data-stu-id="16653-136">az policy assignment list: Support listing policy assignments at Management Group scope</span></span>
* <span data-ttu-id="16653-137">リソース グループでのテンプレートのデプロイ用に `az deployment group` と `az deployment operation group` を追加。</span><span class="sxs-lookup"><span data-stu-id="16653-137">Add `az deployment group` and `az deployment operation group` for template deployment at resource groups.</span></span> <span data-ttu-id="16653-138">これは `az group deployment` と `az group deployment operation` の複製です</span><span class="sxs-lookup"><span data-stu-id="16653-138">This is a duplicate of `az group deployment` and `az group deployment operation`</span></span>
* <span data-ttu-id="16653-139">サブスクリプション スコープでのテンプレートのデプロイ用に `az deployment sub` と `az deployment operation sub` を追加。</span><span class="sxs-lookup"><span data-stu-id="16653-139">Add `az deployment sub` and `az deployment operation sub` for template deployment at subscription scope.</span></span> <span data-ttu-id="16653-140">これは `az deployment` と `az deployment operation` の複製です</span><span class="sxs-lookup"><span data-stu-id="16653-140">This is a duplicate of `az deployment` and `az deployment operation`</span></span>
* <span data-ttu-id="16653-141">管理グループでのテンプレートのデプロイ用に `az deployment mg` と `az deployment operation mg` を追加</span><span class="sxs-lookup"><span data-stu-id="16653-141">Add `az deployment mg` and `az deployment operation mg` for template deployment at management groups</span></span>
* <span data-ttu-id="16653-142">テナント スコープでのテンプレートのデプロイ用に `az deployment tenant` と `az deployment operation tenant` を追加</span><span class="sxs-lookup"><span data-stu-id="16653-142">Add `az deployment tenant` and `az deployment operation tenant` for template deployment at tenant scope</span></span>
* <span data-ttu-id="16653-143">az policy assignment create:`--location` パラメーターに対する説明の追加</span><span class="sxs-lookup"><span data-stu-id="16653-143">az policy assignment create: Add a description to the `--location` parameter</span></span>
* <span data-ttu-id="16653-144">az group deployment create:クロス テナントをサポートするためにパラメーター `--aux-tenants` を追加</span><span class="sxs-lookup"><span data-stu-id="16653-144">az group deployment create: Add parameter `--aux-tenants` to support cross tenants</span></span>

### <a name="cdn"></a><span data-ttu-id="16653-145">CDN</span><span class="sxs-lookup"><span data-stu-id="16653-145">CDN</span></span>

* <span data-ttu-id="16653-146">CDN WAF コマンドの追加</span><span class="sxs-lookup"><span data-stu-id="16653-146">Add CDN WAF commands</span></span>

### <a name="compute"></a><span data-ttu-id="16653-147">Compute</span><span class="sxs-lookup"><span data-stu-id="16653-147">Compute</span></span>

* <span data-ttu-id="16653-148">az sig image-version: --data-snapshot-luns の追加</span><span class="sxs-lookup"><span data-stu-id="16653-148">az sig image-version: add --data-snapshot-luns</span></span>
* <span data-ttu-id="16653-149">az ppg show: 近接配置グループ内のすべてのリソースのコロケーションの状態をフェッチできるように、--colocation-status を追加</span><span class="sxs-lookup"><span data-stu-id="16653-149">az ppg show: add --colocation-status to enable fetching the colocation status of all the resources in the proximity placement group</span></span>
* <span data-ttu-id="16653-150">az vmss create/update: 自動修復のサポート</span><span class="sxs-lookup"><span data-stu-id="16653-150">az vmss create/update: support automatic repairs</span></span>
* <span data-ttu-id="16653-151">[重大な変更] az image template: テンプレートの名前を builder に変更</span><span class="sxs-lookup"><span data-stu-id="16653-151">[BREAKING CHANGE] az image template: rename template to builder</span></span>
* <span data-ttu-id="16653-152">az image builder create: --image-template の追加</span><span class="sxs-lookup"><span data-stu-id="16653-152">az image builder create: add --image-template</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="16653-153">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-153">Cosmos DB</span></span>

* <span data-ttu-id="16653-154">SQL ストアド プロシージャ、udf およびトリガーのコマンドレットの追加</span><span class="sxs-lookup"><span data-stu-id="16653-154">Add Sql stored procedure, udf and trigger cmdlets</span></span>
* <span data-ttu-id="16653-155">az cosmosdb create: キー コンテナーの暗号化情報の追加をサポートするために、--key-uri を追加</span><span class="sxs-lookup"><span data-stu-id="16653-155">az cosmosdb create: add --key-uri to support adding key vault encryption information</span></span>

### <a name="keyvault"></a><span data-ttu-id="16653-156">KeyVault</span><span class="sxs-lookup"><span data-stu-id="16653-156">KeyVault</span></span>

* <span data-ttu-id="16653-157">keyvault create: 論理的な削除を既定で有効化</span><span class="sxs-lookup"><span data-stu-id="16653-157">keyvault create: enable soft-delete by default</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-158">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-158">Monitor</span></span>

* <span data-ttu-id="16653-159">az monitor metrics alert create: `--condition` での `~` のサポート</span><span class="sxs-lookup"><span data-stu-id="16653-159">az monitor metrics alert create: support `~` in `--condition`</span></span>

### <a name="network"></a><span data-ttu-id="16653-160">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-160">Network</span></span>

* <span data-ttu-id="16653-161">az network application-gateway rewrite-rule create: URL の構成のサポート</span><span class="sxs-lookup"><span data-stu-id="16653-161">az network application-gateway rewrite-rule create: support url configuration</span></span>
* <span data-ttu-id="16653-162">az network dns zone import: 今後、--zone-name は大文字と小文字を区別する</span><span class="sxs-lookup"><span data-stu-id="16653-162">az network dns zone import: --zone-name will be case insensitive in the future</span></span>
* <span data-ttu-id="16653-163">az network private-endpoint/private-link-service: プレビュー ラベルの削除</span><span class="sxs-lookup"><span data-stu-id="16653-163">az network private-endpoint/private-link-service: remove preview label</span></span>
* <span data-ttu-id="16653-164">az network bastion: Bastion のサポート</span><span class="sxs-lookup"><span data-stu-id="16653-164">az network bastion: support bastion</span></span>
* <span data-ttu-id="16653-165">az network vnet list-available-ips: VNet 内で使用可能な IP の一覧のサポート</span><span class="sxs-lookup"><span data-stu-id="16653-165">az network vnet list-available-ips: support list available ips in a vnet</span></span>
* <span data-ttu-id="16653-166">az network watcher flow-log create/list/delete/update: Watcher フロー ログを管理するために新しいコマンドを追加し、Watcher を明示的に識別するために --location を公開</span><span class="sxs-lookup"><span data-stu-id="16653-166">az network watcher flow-log create/list/delete/update: add new commands to manage watcher flow log and exposing --location to identify watcher explicitly</span></span>
* <span data-ttu-id="16653-167">az network watcher flow-log configure: 非推奨</span><span class="sxs-lookup"><span data-stu-id="16653-167">az network watcher flow-log configure: deprecated</span></span>
* <span data-ttu-id="16653-168">az network watcher flow-log show: ARM 形式の結果 (非推奨の古い形式の出力) を取得するために --location および--name をサポート</span><span class="sxs-lookup"><span data-stu-id="16653-168">az network watcher flow-log show: support --location and --name to get ARM-formatted result, deprecated old formatted output</span></span>

### <a name="policy"></a><span data-ttu-id="16653-169">ポリシー</span><span class="sxs-lookup"><span data-stu-id="16653-169">Policy</span></span>

* <span data-ttu-id="16653-170">az policy assignment create:ポリシー割り当ての自動生成された名前が制限を超えるというバグの修正</span><span class="sxs-lookup"><span data-stu-id="16653-170">az policy assignment create: Fix the bug that automatically generated name of policy assignment exceeds the limit</span></span>

### <a name="rbac"></a><span data-ttu-id="16653-171">RBAC</span><span class="sxs-lookup"><span data-stu-id="16653-171">RBAC</span></span>

* <span data-ttu-id="16653-172">az ad group show: RegEx の問題として扱われる --group 値の修正</span><span class="sxs-lookup"><span data-stu-id="16653-172">az ad group show: fix --group value treated as regex problem</span></span>

### <a name="rdbms"></a><span data-ttu-id="16653-173">RDBMS</span><span class="sxs-lookup"><span data-stu-id="16653-173">RDBMS</span></span>

* <span data-ttu-id="16653-174">azure-mgmt-rdbms SDK のバージョンを 2.0.0 にバージョンアップ</span><span class="sxs-lookup"><span data-stu-id="16653-174">Bump the azure-mgmt-rdbms SDK version to 2.0.0</span></span>
* <span data-ttu-id="16653-175">az postgres private-endpoint-connection: Postgres プライベート エンドポイント接続の管理</span><span class="sxs-lookup"><span data-stu-id="16653-175">az postgres private-endpoint-connection: manage postgres private endpoint connections</span></span>
* <span data-ttu-id="16653-176">az postgres private-link-resource: Postgres プライベート リンク リソースの管理</span><span class="sxs-lookup"><span data-stu-id="16653-176">az postgres private-link-resource: manage postgres private link resources</span></span>
* <span data-ttu-id="16653-177">az mysql private-endpoint-connection: MySQL プライベート エンドポイント接続の管理</span><span class="sxs-lookup"><span data-stu-id="16653-177">az mysql private-endpoint-connection: manage mysql private endpoint connections</span></span>
* <span data-ttu-id="16653-178">az mysql private-link-resource: MySQL プライベート リンク リソースの管理</span><span class="sxs-lookup"><span data-stu-id="16653-178">az mysql private-link-resource: manage mysql private link resources</span></span>
* <span data-ttu-id="16653-179">az mariadb private-endpoint-connection: MariaDB プライベート エンドポイント接続の管理</span><span class="sxs-lookup"><span data-stu-id="16653-179">az mariadb private-endpoint-connection: manage mariadb private endpoint connections</span></span>
* <span data-ttu-id="16653-180">az mariadb private-link-resource: MariaDB プライベート リンク リソースの管理</span><span class="sxs-lookup"><span data-stu-id="16653-180">az mariadb private-link-resource: manage mariadb private link resources</span></span>
* <span data-ttu-id="16653-181">RDBMS プライベート エンドポイント テストを更新中</span><span class="sxs-lookup"><span data-stu-id="16653-181">Updating RDBMS Private Endpoint Tests</span></span>

### <a name="sql"></a><span data-ttu-id="16653-182">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-182">SQL</span></span>

* <span data-ttu-id="16653-183">Sql midb Add: list-deleted、show-deleted、update-retention、show-retention</span><span class="sxs-lookup"><span data-stu-id="16653-183">Sql midb Add: list-deleted, show-deleted, update-retention, show-retention</span></span>
* <span data-ttu-id="16653-184">(sql server create:)オプションの public-network-access 'Enable'/'Disable' フラグを sql server create に追加</span><span class="sxs-lookup"><span data-stu-id="16653-184">(sql server create:) Add optional public-network-access 'Enable'/'Disable' flag to sql server create</span></span>
* <span data-ttu-id="16653-185">(sql server update:) 顧客向けの変更の実施</span><span class="sxs-lookup"><span data-stu-id="16653-185">(sql server update:) make some customer-facing change</span></span>
* <span data-ttu-id="16653-186">MI および SQL DB 用の minimal_tls_version プロパティの追加</span><span class="sxs-lookup"><span data-stu-id="16653-186">Add minimal_tls_version property for MI and SQL DB</span></span>

### <a name="storage"></a><span data-ttu-id="16653-187">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-187">Storage</span></span>

* <span data-ttu-id="16653-188">az storage blob delete-batch:`--dryrun` フラグの誤動作</span><span class="sxs-lookup"><span data-stu-id="16653-188">az storage blob delete-batch: Misbehaving `--dryrun` flag</span></span>
* <span data-ttu-id="16653-189">az storage account network-rule add (バグ修正): 追加操作は、べき等にする必要がある</span><span class="sxs-lookup"><span data-stu-id="16653-189">az storage account network-rule add (bug fix): add operation should be idempotent</span></span>
* <span data-ttu-id="16653-190">az storage account create/update:ルーティングの優先順位のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="16653-190">az storage account create/update: Add Routing Preference support</span></span>
* <span data-ttu-id="16653-191">azure-mgmt-storage のバージョンを 8.0.0 にアップグレード</span><span class="sxs-lookup"><span data-stu-id="16653-191">Upgrade azure-mgmt-storage version to 8.0.0</span></span>
* <span data-ttu-id="16653-192">az storage container immutability create: --allow-protected-append-write パラメーターの追加</span><span class="sxs-lookup"><span data-stu-id="16653-192">az storage container immutability create: add --allow-protected-append-write parameter</span></span>
* <span data-ttu-id="16653-193">az storage account private-link-resource list:ストレージ アカウントのプライベート リンク リソースを一覧表示するためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="16653-193">az storage account private-link-resource list: Add support to list private link resources for storage account</span></span>
* <span data-ttu-id="16653-194">az storage account private-endpoint-connection approve/reject/show/delete:プライベート エンドポイント接続の管理のサポート</span><span class="sxs-lookup"><span data-stu-id="16653-194">az storage account private-endpoint-connection approve/reject/show/delete: Support to manage private endpoint connections</span></span>
* <span data-ttu-id="16653-195">az storage account blob-service-properties update: --enable-restore-policy と --restore-days の追加</span><span class="sxs-lookup"><span data-stu-id="16653-195">az storage account blob-service-properties update: add --enable-restore-policy and --restore-days</span></span>
* <span data-ttu-id="16653-196">az storage blob restore:BLOB 範囲を復元するためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="16653-196">az storage blob restore: Add support to restore blob ranges</span></span>

## <a name="february-18-2020"></a><span data-ttu-id="16653-197">2020 年 2 月 18 日</span><span class="sxs-lookup"><span data-stu-id="16653-197">February 18, 2020</span></span>

<span data-ttu-id="16653-198">バージョン 2.1.0</span><span class="sxs-lookup"><span data-stu-id="16653-198">Version 2.1.0</span></span>

### <a name="acr"></a><span data-ttu-id="16653-199">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-199">ACR</span></span>

* <span data-ttu-id="16653-200">`az acr login` の新しい引数 `--expose-token` を追加</span><span class="sxs-lookup"><span data-stu-id="16653-200">Add a new argument `--expose-token` for `az acr login`</span></span>
* <span data-ttu-id="16653-201">`az acr task identity show -n Name -r Registry -o table` の正しくない出力を修正</span><span class="sxs-lookup"><span data-stu-id="16653-201">Fix the incorrect output of `az acr task identity show -n Name -r Registry -o table`</span></span>
* <span data-ttu-id="16653-202">az acr login:Docker コマンドによって返されたエラーが返された場合は CLIError をスロー</span><span class="sxs-lookup"><span data-stu-id="16653-202">az acr login: Throw a CLIError if there are errors returned by docker command</span></span>

### <a name="acs"></a><span data-ttu-id="16653-203">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-203">ACS</span></span>

* <span data-ttu-id="16653-204">aks create/update: `--vnet-subnet-id` の検証を追加</span><span class="sxs-lookup"><span data-stu-id="16653-204">aks create/update: add `--vnet-subnet-id` validation</span></span>

### <a name="aladdin"></a><span data-ttu-id="16653-205">Aladdin</span><span class="sxs-lookup"><span data-stu-id="16653-205">Aladdin</span></span>

* <span data-ttu-id="16653-206">生成された例をコマンドの _help.py として解析</span><span class="sxs-lookup"><span data-stu-id="16653-206">Parse generated examples into commands' _help.py</span></span>

### <a name="ams"></a><span data-ttu-id="16653-207">AMS</span><span class="sxs-lookup"><span data-stu-id="16653-207">AMS</span></span>

* <span data-ttu-id="16653-208">az ams の一般提供を開始</span><span class="sxs-lookup"><span data-stu-id="16653-208">az ams is GA now</span></span>

### <a name="appconfig"></a><span data-ttu-id="16653-209">AppConfig</span><span class="sxs-lookup"><span data-stu-id="16653-209">AppConfig</span></span>

* <span data-ttu-id="16653-210">サポートされていないキー/ラベル フィルターを除外するようにヘルプ メッセージを変更</span><span class="sxs-lookup"><span data-stu-id="16653-210">Revise help message to exclude unsupported key/label filter</span></span>
* <span data-ttu-id="16653-211">マネージド ID と機能フラグを除くほとんどのコマンドのプレビュー タグを削除</span><span class="sxs-lookup"><span data-stu-id="16653-211">Remove preview tag for most commands excluding managed identity and feature flags</span></span>
* <span data-ttu-id="16653-212">ストアの更新時にカスタマー マネージド キーを追加</span><span class="sxs-lookup"><span data-stu-id="16653-212">Add customer managed key when updating stores</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-213">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-213">AppService</span></span>

* <span data-ttu-id="16653-214">az webapp list-runtimes:list-runtimes のバグを修正</span><span class="sxs-lookup"><span data-stu-id="16653-214">az webapp list-runtimes: Fix the bug for list-runtimes</span></span>
* <span data-ttu-id="16653-215">az webapp | functionapp config ssl create を追加</span><span class="sxs-lookup"><span data-stu-id="16653-215">Add az webapp|functionapp config ssl create</span></span>
* <span data-ttu-id="16653-216">v3 関数アプリおよびノード 12 のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="16653-216">Add support for v3 function apps and node 12</span></span>

### <a name="arm"></a><span data-ttu-id="16653-217">ARM</span><span class="sxs-lookup"><span data-stu-id="16653-217">ARM</span></span>

* <span data-ttu-id="16653-218">az policy assignment create:`--policy` パラメーターが無効な場合のエラー メッセージを修正</span><span class="sxs-lookup"><span data-stu-id="16653-218">az policy assignment create: Fix the error message when the `--policy` parameter is invalid</span></span>
* <span data-ttu-id="16653-219">az group deployment create:サイズの大きな parameters.json ファイルの使用時の "stat: path too long for Windows" エラーを修正</span><span class="sxs-lookup"><span data-stu-id="16653-219">az group deployment create: Fix "stat: path too long for Windows" error when using large parameters.json file</span></span>

### <a name="backup"></a><span data-ttu-id="16653-220">バックアップ</span><span class="sxs-lookup"><span data-stu-id="16653-220">Backup</span></span>

* <span data-ttu-id="16653-221">OLR のアイテム レベルの回復フローを修正</span><span class="sxs-lookup"><span data-stu-id="16653-221">Fix for item level recovery flow in OLR</span></span>
* <span data-ttu-id="16653-222">SQL Database および SAP Database のファイルとしての復元のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="16653-222">Add restore as files support for SQL and SAP Databases</span></span>

### <a name="compute"></a><span data-ttu-id="16653-223">Compute</span><span class="sxs-lookup"><span data-stu-id="16653-223">Compute</span></span>

* <span data-ttu-id="16653-224">vm/vmss/availability-set update: ProximityPlacementGroup を更新できるように --ppg を追加</span><span class="sxs-lookup"><span data-stu-id="16653-224">vm/vmss/availability-set update: add --ppg to allowing updating ProximityPlacementGroup</span></span>
* <span data-ttu-id="16653-225">vmss create: --data-disk-iops および --data-disk-mbps を追加</span><span class="sxs-lookup"><span data-stu-id="16653-225">vmss create: add --data-disk-iops and --data-disk-mbps</span></span>
* <span data-ttu-id="16653-226">az vm host: `vm host` および `vm host group` のプレビュー タグを削除</span><span class="sxs-lookup"><span data-stu-id="16653-226">az vm host: remove preview tag for `vm host` and `vm host group`</span></span>
* <span data-ttu-id="16653-227">[重大な変更] #10728 を修正: `az vm create`: vnet が指定されている場合、サブネットが存在しなければサブネットが自動的に作成される</span><span class="sxs-lookup"><span data-stu-id="16653-227">[BREAKING CHANGE] Fix #10728: `az vm create`: create subnet automatically if vnet is specified and subnet not exists</span></span>
* <span data-ttu-id="16653-228">vm イメージ リストの信頼性を向上</span><span class="sxs-lookup"><span data-stu-id="16653-228">Increase robustness of vm image list</span></span>

### <a name="eventhub"></a><span data-ttu-id="16653-229">Eventhub</span><span class="sxs-lookup"><span data-stu-id="16653-229">Eventhub</span></span>

* <span data-ttu-id="16653-230">2019-03-01-hybrid プロファイルに対する Azure Stack のサポート</span><span class="sxs-lookup"><span data-stu-id="16653-230">Azure Stack support for 2019-03-01-hybrid profile</span></span>

### <a name="keyvault"></a><span data-ttu-id="16653-231">KeyVault</span><span class="sxs-lookup"><span data-stu-id="16653-231">KeyVault</span></span>

* <span data-ttu-id="16653-232">az keyvault key create: パラメーター `--ops` の新しい値 `import` を追加</span><span class="sxs-lookup"><span data-stu-id="16653-232">az keyvault key create: add a new value `import` for parameter `--ops`</span></span>
* <span data-ttu-id="16653-233">az keyvault key list-versions: キー指定のためのパラメーター `--id` をサポート</span><span class="sxs-lookup"><span data-stu-id="16653-233">az keyvault key list-versions: support parameter `--id` for specifying keys</span></span>
* <span data-ttu-id="16653-234">プライベート エンドポイントの接続をサポート</span><span class="sxs-lookup"><span data-stu-id="16653-234">Support private endpoint connections</span></span>

### <a name="network"></a><span data-ttu-id="16653-235">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-235">Network</span></span>

* <span data-ttu-id="16653-236">azure-mgmt-network 9.0.0 にバージョンアップ</span><span class="sxs-lookup"><span data-stu-id="16653-236">Bump to azure-mgmt-network 9.0.0</span></span>
* <span data-ttu-id="16653-237">az network private-link-service update/create: support --enable-proxy-protocol</span><span class="sxs-lookup"><span data-stu-id="16653-237">az network private-link-service update/create: support --enable-proxy-protocol</span></span>
* <span data-ttu-id="16653-238">接続モニター V2 の機能を追加</span><span class="sxs-lookup"><span data-stu-id="16653-238">Add connection Monitor V2 feature</span></span>

### <a name="packaging"></a><span data-ttu-id="16653-239">梱包</span><span class="sxs-lookup"><span data-stu-id="16653-239">Packaging</span></span>

* <span data-ttu-id="16653-240">[重大な変更] Python 2.7 のサポートを終了</span><span class="sxs-lookup"><span data-stu-id="16653-240">[BREAKING CHANGE] Drop support for Python 2.7</span></span>

### <a name="profile"></a><span data-ttu-id="16653-241">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-241">Profile</span></span>

* <span data-ttu-id="16653-242">プレビュー:サブスクリプション アカウントに新しい属性 `homeTenantId` および `managedByTenants` を追加。</span><span class="sxs-lookup"><span data-stu-id="16653-242">Preview: Add new attributes `homeTenantId` and `managedByTenants` to subscription accounts.</span></span> <span data-ttu-id="16653-243">変更を有効にするには、`az login` を再実行してください</span><span class="sxs-lookup"><span data-stu-id="16653-243">Please re-run `az login` for the changes to take effect</span></span>
* <span data-ttu-id="16653-244">az login:1 つのサブスクリプションが複数のテナントからリストされる場合は警告を表示して最初のものに既定で設定。</span><span class="sxs-lookup"><span data-stu-id="16653-244">az login: Show a warning when a subscription is listed from more than one tenants and default to the first one.</span></span> <span data-ttu-id="16653-245">このサブスクリプションにアクセスする際の特定のテナントを選択するには、`az login` に `--tenant` を含めてください</span><span class="sxs-lookup"><span data-stu-id="16653-245">To select a specific tenant when accessing this subscription, please include `--tenant` in `az login`</span></span>

### <a name="role"></a><span data-ttu-id="16653-246">Role</span><span class="sxs-lookup"><span data-stu-id="16653-246">Role</span></span>

* <span data-ttu-id="16653-247">az role assignment create:表示名でサービス プリンシパルにロールを割り当てた場合に HTTP 400 が発生するエラーを修正</span><span class="sxs-lookup"><span data-stu-id="16653-247">az role assignment create: Fix the error that assigning a role to a service principal by display name yields a HTTP 400</span></span>

### <a name="sql"></a><span data-ttu-id="16653-248">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-248">SQL</span></span>

* <span data-ttu-id="16653-249">Update SQL Managed Instance のコマンドレット `az sql mi update` に 2 つのパラメーター tier および family を追加して更新</span><span class="sxs-lookup"><span data-stu-id="16653-249">Update SQL Managed Instance cmdlet `az sql mi update` with two new parameters: tier and family</span></span>

### <a name="storage"></a><span data-ttu-id="16653-250">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-250">Storage</span></span>

* <span data-ttu-id="16653-251">[破壊的変更] `az storage account create`:既定のストレージ アカウントの種類を StorageV2 に変更</span><span class="sxs-lookup"><span data-stu-id="16653-251">[BREAKING CHANGE] `az storage account create`: Change default storage account kind to StorageV2</span></span>

## <a name="february-04-2020"></a><span data-ttu-id="16653-252">2020 年 2 月 4 日</span><span class="sxs-lookup"><span data-stu-id="16653-252">February 04, 2020</span></span>

<span data-ttu-id="16653-253">バージョン 2.0.81</span><span class="sxs-lookup"><span data-stu-id="16653-253">Version 2.0.81</span></span>

### <a name="acs"></a><span data-ttu-id="16653-254">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-254">ACS</span></span>

* <span data-ttu-id="16653-255">Standard Load Balancer でアウトバウンド割当てポートとアイドル タイムアウトを設定するためのサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="16653-255">Add support to set outbound allocated ports and idle timeouts on standard load balancer</span></span>
* <span data-ttu-id="16653-256">API バージョン 2019-11-01 への更新を行います</span><span class="sxs-lookup"><span data-stu-id="16653-256">Update to API Version 2019-11-01</span></span>

### <a name="acr"></a><span data-ttu-id="16653-257">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-257">ACR</span></span>

* <span data-ttu-id="16653-258">[破壊的変更] `az acr delete` でプロンプトが表示されます</span><span class="sxs-lookup"><span data-stu-id="16653-258">[BREAKING CHANGE] `az acr delete` will prompt</span></span>
* <span data-ttu-id="16653-259">[重大な変更] 'az acr task delete' でプロンプトが表示されます</span><span class="sxs-lookup"><span data-stu-id="16653-259">[BREAKING CHANGE] 'az acr task delete' will prompt</span></span>
* <span data-ttu-id="16653-260">taskrun 管理用の新しいコマンド グループ 'az acr taskrun show/list/delete' を追加します</span><span class="sxs-lookup"><span data-stu-id="16653-260">Add a new command group 'az acr taskrun show/list/delete' for taskrun management</span></span>

### <a name="aks"></a><span data-ttu-id="16653-261">AKS</span><span class="sxs-lookup"><span data-stu-id="16653-261">AKS</span></span>

* <span data-ttu-id="16653-262">各クラスターは、分離を向上させるために、個別のサービス プリンシパルを取得します</span><span class="sxs-lookup"><span data-stu-id="16653-262">Each cluster gets a separate service principal to improve isolation</span></span>

### <a name="appconfig"></a><span data-ttu-id="16653-263">AppConfig</span><span class="sxs-lookup"><span data-stu-id="16653-263">AppConfig</span></span>

* <span data-ttu-id="16653-264">appservice との間での keyvault 参照のインポート/エクスポートをサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-264">Support import/export of keyvault references from/to appservice</span></span>
* <span data-ttu-id="16653-265">appconfig から appconfig へのすべてのラベルのインポート/エクスポートをサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-265">Support import/export of all labels from appconfig to appconfig</span></span>
* <span data-ttu-id="16653-266">設定とインポートの前にキーと機能の名前を検証します</span><span class="sxs-lookup"><span data-stu-id="16653-266">Validate key and feature names before setting and importing</span></span>
* <span data-ttu-id="16653-267">構成ストアの SKU 変更を公開します。</span><span class="sxs-lookup"><span data-stu-id="16653-267">Expose sku modification for configuration store.</span></span>
* <span data-ttu-id="16653-268">マネージド ID のコマンド グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="16653-268">Add command group for managed identity.</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-269">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-269">AppService</span></span>

* <span data-ttu-id="16653-270">Azure Stack: 2019-03-01-hybrid のプロファイルの下の surface コマンド</span><span class="sxs-lookup"><span data-stu-id="16653-270">Azure Stack: surface commands under the profile of 2019-03-01-hybrid</span></span>
* <span data-ttu-id="16653-271">functionapp:Linux で Java 関数アプリを作成する機能を追加します</span><span class="sxs-lookup"><span data-stu-id="16653-271">functionapp: Add ability to create Java function apps in Linux</span></span>

### <a name="arm"></a><span data-ttu-id="16653-272">ARM</span><span class="sxs-lookup"><span data-stu-id="16653-272">ARM</span></span>

* <span data-ttu-id="16653-273">問題 #10246 を修正: 渡されたパラメーター `--ids` がリソース グループ ID の場合、`az resource tag` がクラッシュします</span><span class="sxs-lookup"><span data-stu-id="16653-273">Fix issue #10246: `az resource tag` crashes when the parameter `--ids` passed in is resource group ID</span></span>
* <span data-ttu-id="16653-274">問題 #11658 を修正: `az group export` コマンド が `--query` と `--output` パラメーターをサポートしません</span><span class="sxs-lookup"><span data-stu-id="16653-274">Fix issue #11658: `az group export` command does not support `--query` and `--output` parameters</span></span>
* <span data-ttu-id="16653-275">問題 #10279 を修正:検証が失敗した場合、`az group deployment validate` の終了コードは 0 になります</span><span class="sxs-lookup"><span data-stu-id="16653-275">Fix issue #10279: The exit code of `az group deployment validate` is 0 when the verification fails</span></span>
* <span data-ttu-id="16653-276">問題 #9916 を修正:`az resource list` コマンドのタグとその他のフィルター条件間の競合に関するエラー メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="16653-276">Fix issue #9916: Improve the error message of the conflict between tag and other filter conditions for `az resource list` command</span></span>
* <span data-ttu-id="16653-277">コマンド `az group create` の managedBy 情報の追加をサポートする新しいパラメーター `--managed-by` を追加します</span><span class="sxs-lookup"><span data-stu-id="16653-277">Add new parameter `--managed-by` to support adding managedBy information for command `az group create`</span></span>

### <a name="azure-red-hat-openshift"></a><span data-ttu-id="16653-278">Azure Red Hat OpenShift</span><span class="sxs-lookup"><span data-stu-id="16653-278">Azure Red Hat OpenShift</span></span>

* <span data-ttu-id="16653-279">Azure Red Hat OpensShift クラスターで Log Analytics 監視を管理するための `monitor` サブグループを追加します</span><span class="sxs-lookup"><span data-stu-id="16653-279">Add `monitor` subgroup to manage Log Analytics monitoring in Azure Red Hat OpensShift cluster</span></span>

### <a name="botservice"></a><span data-ttu-id="16653-280">BotService</span><span class="sxs-lookup"><span data-stu-id="16653-280">BotService</span></span>

* <span data-ttu-id="16653-281">問題 #11697 を修正: `az bot create` がべき等ではありません</span><span class="sxs-lookup"><span data-stu-id="16653-281">Fix issue #11697: `az bot create` is not idempotent</span></span>
* <span data-ttu-id="16653-282">名前修正テストをライブ モードでのみ実行するように変更します</span><span class="sxs-lookup"><span data-stu-id="16653-282">Change name-correcting tests to run in Live-mode only</span></span>

### <a name="cdn"></a><span data-ttu-id="16653-283">CDN</span><span class="sxs-lookup"><span data-stu-id="16653-283">CDN</span></span>

* <span data-ttu-id="16653-284">rulesEngine 機能のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="16653-284">Add support for rulesEngine feature</span></span>
* <span data-ttu-id="16653-285">規則を管理するための新しいコマンド グループ 'cdn endpoint rule' を追加します</span><span class="sxs-lookup"><span data-stu-id="16653-285">Add new commands group 'cdn endpoint rule' to manage rules</span></span>
* <span data-ttu-id="16653-286">API バージョン 2019-04-15 を使用するように azure-mgmt-cdn バージョンを 4.0.0 に更新します</span><span class="sxs-lookup"><span data-stu-id="16653-286">Update azure-mgmt-cdn version to 4.0.0 to use api version 2019-04-15</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="16653-287">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="16653-287">Deployment Manager</span></span>

* <span data-ttu-id="16653-288">すべてのリソースのリスト操作を追加します。</span><span class="sxs-lookup"><span data-stu-id="16653-288">Add list operation for all resources.</span></span>
* <span data-ttu-id="16653-289">新しい手順の種類に対する手順リソースを強化します。</span><span class="sxs-lookup"><span data-stu-id="16653-289">Enhance step resource for new step type.</span></span>
* <span data-ttu-id="16653-290">バージョン 0.2.0 を使用するように azure-mgmt-deploymentmanager パッケージを更新します。</span><span class="sxs-lookup"><span data-stu-id="16653-290">Update azure-mgmt-deploymentmanager package to use version 0.2.0.</span></span>

### <a name="iot"></a><span data-ttu-id="16653-291">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-291">IoT</span></span>

* <span data-ttu-id="16653-292">'IoT hub Job' コマンドを廃止します。</span><span class="sxs-lookup"><span data-stu-id="16653-292">Deprecate 'IoT hub Job' commands.</span></span>

### <a name="iot-central"></a><span data-ttu-id="16653-293">IoT Central</span><span class="sxs-lookup"><span data-stu-id="16653-293">IoT Central</span></span>

* <span data-ttu-id="16653-294">新しい SKU 名 ST0、ST1、ST2 でのアプリの作成/更新をサポートします。</span><span class="sxs-lookup"><span data-stu-id="16653-294">Support app creation/update with the new sku name ST0, ST1, ST2.</span></span>

### <a name="key-vault"></a><span data-ttu-id="16653-295">Key Vault</span><span class="sxs-lookup"><span data-stu-id="16653-295">Key Vault</span></span>

* <span data-ttu-id="16653-296">キーをダウンロードするための新しいコマンド `az keyvault key download` を追加します。</span><span class="sxs-lookup"><span data-stu-id="16653-296">Add a new command `az keyvault key download` for downloading keys.</span></span>

### <a name="misc"></a><span data-ttu-id="16653-297">その他</span><span class="sxs-lookup"><span data-stu-id="16653-297">Misc</span></span>

* <span data-ttu-id="16653-298">#6371 を修正:Bash でのファイル名と環境変数の補完をサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-298">Fix #6371: Support filename and environment variable completion in Bash</span></span>

### <a name="network"></a><span data-ttu-id="16653-299">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-299">Network</span></span>

* <span data-ttu-id="16653-300">#2092 を修正: az network dns record-add/remove: レコード セットが見つからない場合に警告を追加します。</span><span class="sxs-lookup"><span data-stu-id="16653-300">Fix #2092: az network dns record-set add/remove: add warning when record-set is not found.</span></span> <span data-ttu-id="16653-301">今後、この自動作成を確認するための追加の引数がサポートされる予定です。</span><span class="sxs-lookup"><span data-stu-id="16653-301">In the future, an extra argument will be supported to confirm this auto creation.</span></span>

### <a name="policy"></a><span data-ttu-id="16653-302">ポリシー</span><span class="sxs-lookup"><span data-stu-id="16653-302">Policy</span></span>

* <span data-ttu-id="16653-303">豊富なポリシー メタデータ リソースを取得するための新しいコマンド `az policy metadata` を追加します</span><span class="sxs-lookup"><span data-stu-id="16653-303">Add new command `az policy metadata` to retrieve rich policy metadata resources</span></span>
* <span data-ttu-id="16653-304">`az policy remediation create`:`--resource-discovery-mode` パラメーターを使用して、修復前にコンプライアンスを再評価する必要があるかどうかを指定します</span><span class="sxs-lookup"><span data-stu-id="16653-304">`az policy remediation create`: Specify whether compliance should be re-evaluated prior to remediation with the `--resource-discovery-mode` parameter</span></span>

### <a name="profile"></a><span data-ttu-id="16653-305">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-305">Profile</span></span>

* <span data-ttu-id="16653-306">`az account get-access-token`:サブスクリプションを指定することなく、テナントのトークンを直接取得するための `--tenant` パラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="16653-306">`az account get-access-token`: Add `--tenant` parameter to acquire token for the tenant directly, needless to specify a subscription</span></span>

### <a name="rbac"></a><span data-ttu-id="16653-307">RBAC</span><span class="sxs-lookup"><span data-stu-id="16653-307">RBAC</span></span>

* <span data-ttu-id="16653-308">[重大な変更] #11883 を修正: `az role assignment create`: 空のスコープの場合にエラーが表示されます</span><span class="sxs-lookup"><span data-stu-id="16653-308">[BREAKING CHANGE] Fix #11883: `az role assignment create`: empty scope will prompt error</span></span>

### <a name="security"></a><span data-ttu-id="16653-309">Security</span><span class="sxs-lookup"><span data-stu-id="16653-309">Security</span></span>

* <span data-ttu-id="16653-310">ストレージ アカウントの高度な脅威保護設定を表示および管理するための新しいコマンド `az atp show` と `az atp update` を追加します。</span><span class="sxs-lookup"><span data-stu-id="16653-310">Add new commands `az atp show` and `az atp update` to view and manage advanced threat protection settings for storage accounts.</span></span>

### <a name="sql"></a><span data-ttu-id="16653-311">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-311">SQL</span></span>

* <span data-ttu-id="16653-312">`sql dw create`: `--zone-redundant` と `--read-replica-count` パラメーターを廃止します。</span><span class="sxs-lookup"><span data-stu-id="16653-312">`sql dw create`: deprecate `--zone-redundant` and `--read-replica-count` parameters.</span></span> <span data-ttu-id="16653-313">これらのパラメーターは、DataWarehouse には適用されません。</span><span class="sxs-lookup"><span data-stu-id="16653-313">These parameters do not apply to DataWarehouse.</span></span>
* <span data-ttu-id="16653-314">[破壊的変更] `az sql db create`:"az sql db create --sample-name" に対して使用可能な値としてドキュメントに記載されている "WideWorldImportersStd" と "WideWorldImportersFull" を削除します。</span><span class="sxs-lookup"><span data-stu-id="16653-314">[BREAKING CHANGE] `az sql db create`: Remove "WideWorldImportersStd" and "WideWorldImportersFull" as documented allowed values for "az sql db create --sample-name".</span></span> <span data-ttu-id="16653-315">これらのサンプル データベースを使用すると、常に作成が失敗します。</span><span class="sxs-lookup"><span data-stu-id="16653-315">These sample databases would always cause creation to fail.</span></span>
* <span data-ttu-id="16653-316">SQL データベースの機密性分類を管理するための新しいコマンド `sql db classification show/list/update/delete` と `sql db classification recommendation list/enable/disable` を追加します。</span><span class="sxs-lookup"><span data-stu-id="16653-316">Add New commands `sql db classification show/list/update/delete` and `sql db classification recommendation list/enable/disable` to manage sensitivity classifications for SQL databases.</span></span>
* <span data-ttu-id="16653-317">`az sql db audit-policy`:空の監査アクションとグループの修正</span><span class="sxs-lookup"><span data-stu-id="16653-317">`az sql db audit-policy`: Fix for empty audit actions and groups</span></span>

### <a name="storage"></a><span data-ttu-id="16653-318">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-318">Storage</span></span>

* <span data-ttu-id="16653-319">Azure ファイル共有の管理操作に Microsoft.Storage リソース プロバイダーを使用するための新しいコマンド グループ `az storage share-rm` を追加します。</span><span class="sxs-lookup"><span data-stu-id="16653-319">Add a new command group `az storage share-rm` to use the Microsoft.Storage resource provider for Azure file share management operations.</span></span>
* <span data-ttu-id="16653-320">問題 #11415 を修正: `az storage blob update` のアクセス許可エラー</span><span class="sxs-lookup"><span data-stu-id="16653-320">Fix issue #11415: permission error for `az storage blob update`</span></span>
* <span data-ttu-id="16653-321">Azcopy 10.3.3 を統合し、Win32 をサポートします。</span><span class="sxs-lookup"><span data-stu-id="16653-321">Integrate Azcopy 10.3.3 and support Win32.</span></span>
* <span data-ttu-id="16653-322">`az storage copy`:`--include-path`、`--include-pattern`、`--exclude-path`、および `--exclude-pattern` パラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="16653-322">`az storage copy`: Add `--include-path`, `--include-pattern`, `--exclude-path` and`--exclude-pattern` parameters</span></span>
* <span data-ttu-id="16653-323">`az storage remove`:`--inlcude` および `--exclude` パラメーターを `--include-path`、`--include-pattern`、`--exclude-path`、および `--exclude-pattern` パラメーターに変更します</span><span class="sxs-lookup"><span data-stu-id="16653-323">`az storage remove`: Change `--inlcude` and `--exclude` parameters to `--include-path`, `--include-pattern`, `--exclude-path` and`--exclude-pattern` parameters</span></span>
* <span data-ttu-id="16653-324">`az storage sync`:`--include-pattern`、`--exclude-path`、および `--exclude-pattern` パラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="16653-324">`az storage sync`: Add `--include-pattern`, `--exclude-path` and`--exclude-pattern` parameters</span></span>

### <a name="servicefabric"></a><span data-ttu-id="16653-325">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="16653-325">ServiceFabric</span></span>

* <span data-ttu-id="16653-326">アプリケーションとサービスを管理するための新しいコマンドを追加します。</span><span class="sxs-lookup"><span data-stu-id="16653-326">Add new commands to manage appliaction and services.</span></span>

## <a name="january-13-2020"></a><span data-ttu-id="16653-327">2020 年 1 月 13 日</span><span class="sxs-lookup"><span data-stu-id="16653-327">January 13, 2020</span></span>

<span data-ttu-id="16653-328">バージョン 2.0.80</span><span class="sxs-lookup"><span data-stu-id="16653-328">Version 2.0.80</span></span>

### <a name="compute"></a><span data-ttu-id="16653-329">Compute</span><span class="sxs-lookup"><span data-stu-id="16653-329">Compute</span></span>

* <span data-ttu-id="16653-330">disk update:--disk-encryption-set と --encryption-type を追加します</span><span class="sxs-lookup"><span data-stu-id="16653-330">disk update: Add --disk-encryption-set and --encryption-type</span></span>
* <span data-ttu-id="16653-331">snapshot create/update:--disk-encryption-set と --encryption-type を追加します</span><span class="sxs-lookup"><span data-stu-id="16653-331">snapshot create/update: Add --disk-encryption-set and --encryption-type</span></span>

### <a name="storage"></a><span data-ttu-id="16653-332">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-332">Storage</span></span>

* <span data-ttu-id="16653-333">azure-mgmt-storage のバージョンを 7.1.0 にアップグレードします</span><span class="sxs-lookup"><span data-stu-id="16653-333">Upgrade azure-mgmt-storage version to 7.1.0</span></span>
* <span data-ttu-id="16653-334">`az storage account create`:テーブルとキューの暗号化サービスをサポートするための `--encryption-key-type-for-table` と `--encryption-key-type-for-queue` を追加します</span><span class="sxs-lookup"><span data-stu-id="16653-334">`az storage account create`: Add `--encryption-key-type-for-table` and `--encryption-key-type-for-queue` to support Table and Queue Encryption Service</span></span>

## <a name="january-07-2020"></a><span data-ttu-id="16653-335">2020 年 1 月 7 日</span><span class="sxs-lookup"><span data-stu-id="16653-335">January 07, 2020</span></span>

<span data-ttu-id="16653-336">バージョン 2.0.79</span><span class="sxs-lookup"><span data-stu-id="16653-336">Version 2.0.79</span></span>

### <a name="acr"></a><span data-ttu-id="16653-337">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-337">ACR</span></span>

* <span data-ttu-id="16653-338">[重大な変更] 'acr build'、'acr task create/update'、'acr run'、および 'acr pack' の '--os' パラメーターを削除します。</span><span class="sxs-lookup"><span data-stu-id="16653-338">[BREAKING CHANGE] Remove '--os' parameter for 'acr build', 'acr task create/update', 'acr run', and 'acr pack'.</span></span> <span data-ttu-id="16653-339">代わりに、'--platform' を使用してください。</span><span class="sxs-lookup"><span data-stu-id="16653-339">Use '--platform' instead.</span></span>

### <a name="appconfig"></a><span data-ttu-id="16653-340">AppConfig</span><span class="sxs-lookup"><span data-stu-id="16653-340">AppConfig</span></span>

* <span data-ttu-id="16653-341">機能フラグのインポート/エクスポートのサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="16653-341">Add support for importing/exporting feature flags</span></span>
* <span data-ttu-id="16653-342">keyvault 参照を作成するための新しいコマンド 'az appconfig kv set-keyvault' を追加します</span><span class="sxs-lookup"><span data-stu-id="16653-342">Add new command 'az appconfig kv set-keyvault' for creating keyvault reference</span></span>
* <span data-ttu-id="16653-343">機能フラグをファイルにエクスポートするときに、さまざまな名前付け規則をサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-343">Support various naming conventions when exporting feature flags to file</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-344">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-344">AppService</span></span>

* <span data-ttu-id="16653-345">問題 #7154 を修正:単一引用符ではなく、アクサン グラーブを使用するように、コマンド < > のドキュメントを更新しています</span><span class="sxs-lookup"><span data-stu-id="16653-345">Fix issue #7154: Updating documentation for command <> to use back ticks instead of single quotes</span></span>
* <span data-ttu-id="16653-346">問題 #11287 を修正: webapp up:既定で、up を使用して作成されたアプリを 'SSL 有効' にする必要がある</span><span class="sxs-lookup"><span data-stu-id="16653-346">Fix issue #11287: webapp up: By default make the app created using up 'should be 'SSL enabled'</span></span>
* <span data-ttu-id="16653-347">問題 #11592 を修正:HTML 静的サイトに az webapp up フラグを追加します</span><span class="sxs-lookup"><span data-stu-id="16653-347">Fix issue #11592: Add az webapp up flag for html static sites</span></span>

### <a name="arm"></a><span data-ttu-id="16653-348">ARM</span><span class="sxs-lookup"><span data-stu-id="16653-348">ARM</span></span>

* <span data-ttu-id="16653-349">`az resource tag` を修正:Recovery Services コンテナー タグを更新できない</span><span class="sxs-lookup"><span data-stu-id="16653-349">Fix `az resource tag`: Recovery Services Vault tags cannot be updated</span></span>

### <a name="backup"></a><span data-ttu-id="16653-350">バックアップ</span><span class="sxs-lookup"><span data-stu-id="16653-350">Backup</span></span>

* <span data-ttu-id="16653-351">IaasVM ワークロードの論理的な削除機能を有効にするための新しいコマンド 'backup protection undelete' を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-351">Added new command 'backup protection undelete' to enable soft-delete feature for IaasVM workload</span></span>
* <span data-ttu-id="16653-352">backup-properties コマンドを設定するための新しいパラメーター '--soft-delete-feature-state' を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-352">Added new parameter '--soft-delete-feature-state' to set backup-properties command</span></span>
* <span data-ttu-id="16653-353">IaasVM ワークロードのディスク除外のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-353">Added disk exclusion support for IaasVM workload</span></span>

### <a name="compute"></a><span data-ttu-id="16653-354">Compute</span><span class="sxs-lookup"><span data-stu-id="16653-354">Compute</span></span>

* <span data-ttu-id="16653-355">Azure Stack プロファイルの `vm create` エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="16653-355">Fix `vm create` failure in Azure Stack profile.</span></span>
* <span data-ttu-id="16653-356">vm monitor metrics tail/list-definitions: VM のクエリ メトリックとリスト定義をサポートします。</span><span class="sxs-lookup"><span data-stu-id="16653-356">vm monitor metrics tail/list-definitions: support query metric and list definitions for a vm.</span></span>
* <span data-ttu-id="16653-357">az vm の新しい再適用コマンド アクションを追加します</span><span class="sxs-lookup"><span data-stu-id="16653-357">Add new reapply command action for az vm</span></span>

### <a name="hdinsight"></a><span data-ttu-id="16653-358">HDInsight</span><span class="sxs-lookup"><span data-stu-id="16653-358">HDInsight</span></span>

* <span data-ttu-id="16653-359">Kafka REST プロキシを使用する Kafka クラスターの作成のサポート</span><span class="sxs-lookup"><span data-stu-id="16653-359">Support for creating a Kafka cluster with Kafka Rest Proxy</span></span>
* <span data-ttu-id="16653-360">azure-mgmt-hdinsight を 1.3.0 にアップグレード</span><span class="sxs-lookup"><span data-stu-id="16653-360">Upgrade azure-mgmt-hdinsight to 1.3.0</span></span>

### <a name="misc"></a><span data-ttu-id="16653-361">その他</span><span class="sxs-lookup"><span data-stu-id="16653-361">Misc.</span></span>

* <span data-ttu-id="16653-362">既定の JSON 形式 または --output によって構成された形式で Azure CLI モジュールと拡張機能のバージョンを表示するプレビュー コマンド `az version show` を追加します</span><span class="sxs-lookup"><span data-stu-id="16653-362">Add preview command `az version show` to show the versions of Azure CLI modules and extensions in JSON format by default or format configured by --output</span></span>

### <a name="event-hubs"></a><span data-ttu-id="16653-363">Event Hubs</span><span class="sxs-lookup"><span data-stu-id="16653-363">Event Hubs</span></span>

* <span data-ttu-id="16653-364">[重大な変更] コマンド 'az eventhubs eventhub update' と 'az eventhubs eventhub create' から 'ReceiveDisabled' status オプションを削除します。</span><span class="sxs-lookup"><span data-stu-id="16653-364">[BREAKING CHANGE] Remove 'ReceiveDisabled' status option from command 'az eventhubs eventhub update' and 'az eventhubs eventhub create'.</span></span> <span data-ttu-id="16653-365">このオプションは、イベント ハブ エンティティに対しては無効です。</span><span class="sxs-lookup"><span data-stu-id="16653-365">This option is not valid for Event Hub entities.</span></span>

### <a name="service-bus"></a><span data-ttu-id="16653-366">Service Bus</span><span class="sxs-lookup"><span data-stu-id="16653-366">Service Bus</span></span>

* <span data-ttu-id="16653-367">[重大な変更] コマンド 'az servicebus topic create'、'az servicebus topic update'、'az servicebus queue create'、および 'az servicebus queue update' から 'ReceiveDisabled' status オプションを削除します。</span><span class="sxs-lookup"><span data-stu-id="16653-367">[BREAKING CHANGE] Remove 'ReceiveDisabled' status option from command 'az servicebus topic create', 'az servicebus topic update', 'az servicebus queue create', and 'az servicebus queue update'.</span></span> <span data-ttu-id="16653-368">このオプションは、Service Bus のトピックとキューに対しては無効です。</span><span class="sxs-lookup"><span data-stu-id="16653-368">This option is not valid for Service Bus topics and queues.</span></span>

### <a name="rbac"></a><span data-ttu-id="16653-369">RBAC</span><span class="sxs-lookup"><span data-stu-id="16653-369">RBAC</span></span>

* <span data-ttu-id="16653-370">#11712 を修正: アプリケーションまたはサービス プリンシパルが存在しない場合に `az ad app/sp show` で終了コード 3 が返されない</span><span class="sxs-lookup"><span data-stu-id="16653-370">Fix #11712: `az ad app/sp show` does not return exit code 3 when the application or service principal does not exist</span></span>

### <a name="storage"></a><span data-ttu-id="16653-371">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-371">Storage</span></span>

* <span data-ttu-id="16653-372">`az storage account create`:--enable-hierarchical-namespace パラメーターのプレビュー フラグを削除します</span><span class="sxs-lookup"><span data-stu-id="16653-372">`az storage account create`: Remove preview flag for --enable-hierarchical-namespace parameter</span></span>
* <span data-ttu-id="16653-373">API バージョン 2019-06-01 を使用するために azure-mgmt-storage バージョンを 7.0.0 に更新します</span><span class="sxs-lookup"><span data-stu-id="16653-373">Update azure-mgmt-storage version to 7.0.0 to use api version 2019-06-01</span></span>
* <span data-ttu-id="16653-374">ストレージ アカウント blob-service-properties の削除の保持ポリシーの管理をサポートするために、新しいパラメーター `--enable-delete-retention` と `--delete-retention-days` を追加します。</span><span class="sxs-lookup"><span data-stu-id="16653-374">Add new parameters `--enable-delete-retention` and `--delete-retention-days` to support managing delete retention policy for storage account blob-service-properties.</span></span>

## <a name="december-17-2019"></a><span data-ttu-id="16653-375">2019 年 12 月 17 日</span><span class="sxs-lookup"><span data-stu-id="16653-375">December 17, 2019</span></span>

<span data-ttu-id="16653-376">2.0.78</span><span class="sxs-lookup"><span data-stu-id="16653-376">2.0.78</span></span>

### <a name="acr"></a><span data-ttu-id="16653-377">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-377">ACR</span></span>

* <span data-ttu-id="16653-378">acr task run でのローカル コンテキストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-378">Added support Local context in acr task run</span></span>

### <a name="acs"></a><span data-ttu-id="16653-379">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-379">ACS</span></span>

* <span data-ttu-id="16653-380">[重大な変更] az openshift create: `--workspace-resource-id` の名前を `--workspace-id` に変更します。</span><span class="sxs-lookup"><span data-stu-id="16653-380">[BREAKING CHANGE]az openshift create: rename `--workspace-resource-id` to `--workspace-id`.</span></span>

### <a name="ams"></a><span data-ttu-id="16653-381">AMS</span><span class="sxs-lookup"><span data-stu-id="16653-381">AMS</span></span>

* <span data-ttu-id="16653-382">リソースが見つからない場合に 3 を返すように表示コマンドを更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-382">Updated show commands to return 3 when resource not found</span></span>

### <a name="appconfig"></a><span data-ttu-id="16653-383">AppConfig</span><span class="sxs-lookup"><span data-stu-id="16653-383">AppConfig</span></span>

* <span data-ttu-id="16653-384">要求 URL に api-version を追加するときのバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="16653-384">Fixed bug when appending api-version to request url.</span></span> <span data-ttu-id="16653-385">既存のソリューションは、改ページ位置の自動修正で機能しません。</span><span class="sxs-lookup"><span data-stu-id="16653-385">The existing solution doesn't work with pagination.</span></span>
* <span data-ttu-id="16653-386">英語以外の言語を表示するためのサポートを追加しました。これは、Microsoft のバックエンド サービスがグローバリゼーション向けに unicode をサポートするためです。</span><span class="sxs-lookup"><span data-stu-id="16653-386">Added support for showing languages besides English as our backend service support unicode for globalization.</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-387">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-387">AppService</span></span>

* <span data-ttu-id="16653-388">問題 #11217 を修正: webapp: az webapp config ssl upload はスロット パラメーターをサポートする必要がある</span><span class="sxs-lookup"><span data-stu-id="16653-388">Fixed issue #11217: webapp: az webapp config ssl upload should support slot parameter</span></span>
* <span data-ttu-id="16653-389">問題 #10965 を修正:エラー:名前を空にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="16653-389">Fixed issue #10965: Error: Name cannot be empty.</span></span> <span data-ttu-id="16653-390">ip_address とサブネットによる削除を許可します</span><span class="sxs-lookup"><span data-stu-id="16653-390">Allow remove by ip_address and subnet</span></span>
* <span data-ttu-id="16653-391">Key Vault `az webapp config ssl import` からの証明書のインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-391">Added support for importing certificates from Key Vault `az webapp config ssl import`</span></span>

### <a name="arm"></a><span data-ttu-id="16653-392">ARM</span><span class="sxs-lookup"><span data-stu-id="16653-392">ARM</span></span>

* <span data-ttu-id="16653-393">6\.0.0 を使用するように azure-mgmt-resource パッケージを更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-393">Updated azure-mgmt-resource package to use 6.0.0</span></span>
* <span data-ttu-id="16653-394">新しいパラメーター `--aux-subs` の追加による `az group deployment create` コマンドのクロス テナントのサポート</span><span class="sxs-lookup"><span data-stu-id="16653-394">Cross Tenant Support for `az group deployment create` command by adding new parameter `--aux-subs`</span></span>
* <span data-ttu-id="16653-395">ポリシー セット定義へのメタデータ情報の追加をサポートするために、新しいパラメーター `--metadata` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-395">Added new parameter `--metadata` to support adding metadata information for policy set definitions.</span></span>

### <a name="backup"></a><span data-ttu-id="16653-396">バックアップ</span><span class="sxs-lookup"><span data-stu-id="16653-396">Backup</span></span>

* <span data-ttu-id="16653-397">SQL および SAP Hana ワークロードのバックアップ サポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-397">Added Backup support for SQL and SAP Hana workload.</span></span>

### <a name="botservice"></a><span data-ttu-id="16653-398">BotService</span><span class="sxs-lookup"><span data-stu-id="16653-398">BotService</span></span>

* <span data-ttu-id="16653-399">[重大な変更] プレビューコマンド 'az bot create' から '--version' フラグを削除します。</span><span class="sxs-lookup"><span data-stu-id="16653-399">[Breaking change] Remove '--version' flag from preview command 'az bot create'.</span></span> <span data-ttu-id="16653-400">v4 SDK ボットのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="16653-400">Only v4 SDK bots are supported.</span></span>
* <span data-ttu-id="16653-401">名前を使用できるかどうかのチェックを 'sz bot create' に追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-401">Added name availability check for 'az bot create'.</span></span>
* <span data-ttu-id="16653-402">'az bot update' を使用してボットのアイコン URL を更新するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-402">Added support for updating the icon URL for a bot via 'az bot update'.</span></span>
* <span data-ttu-id="16653-403">'az bot directline update' を使用して Direct Line チャネルを更新するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-403">Added support for updating a Direct Line channel via 'az bot directline update'.</span></span>
* <span data-ttu-id="16653-404">'az bot directline create' に '--enable-enhanced-auth' フラグのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-404">Added '--enable-enhanced-auth' flag support to 'az bot directline create'.</span></span>
* <span data-ttu-id="16653-405">コマンド グループ 'az bot authsetting' は、プレビュー段階ではなく、GA です。</span><span class="sxs-lookup"><span data-stu-id="16653-405">The following command groups are GA and not in preview: 'az bot authsetting'.</span></span>
* <span data-ttu-id="16653-406">'az bot' の次のコマンドは、プレビュー段階ではなく、GA です: 'create'、'prepare-deploy'、'show'、'delete'、'update'。</span><span class="sxs-lookup"><span data-stu-id="16653-406">The following commands in 'az bot' are GA and not in preview: 'create', 'prepare-deploy', 'show', 'delete', 'update'.</span></span>
* <span data-ttu-id="16653-407">'az bot prepare-deploy' が修正され、 '--proj-file-path' 値が小文字に変更されます (例:"Test.csproj" が "test.csproj" に)。</span><span class="sxs-lookup"><span data-stu-id="16653-407">Fixed 'az bot prepare-deploy' changing '--proj-file-path' value to lower case (e.g. "Test.csproj" to "test.csproj").</span></span>

### <a name="compute"></a><span data-ttu-id="16653-408">Compute</span><span class="sxs-lookup"><span data-stu-id="16653-408">Compute</span></span>

* <span data-ttu-id="16653-409">vmss create/update:--scale-in-policy を追加しました。これは、VMSS がスケールインされるときに削除対象として選択される仮想マシンを決定します。</span><span class="sxs-lookup"><span data-stu-id="16653-409">vmss create/update: Added --scale-in-policy, which decides which virtual machines are chosen for removal when a VMSS is scaled-in.</span></span>
* <span data-ttu-id="16653-410">vm/vmss update:--priority を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-410">vm/vmss update: Added --priority.</span></span>
* <span data-ttu-id="16653-411">vm/vmss update:--max-price を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-411">vm/vmss update: Added --max-price.</span></span>
* <span data-ttu-id="16653-412">disk-encryption-set コマンド グループ (create、show、update、delete、list) を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-412">Added disk-encryption-set command group (create, show, update, delete, list).</span></span>
* <span data-ttu-id="16653-413">disk create:--encryption-type と --disk-encryption-set を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-413">disk create: Added --encryption-type and --disk-encryption-set.</span></span>
* <span data-ttu-id="16653-414">vm/vmss create: --os-disk-encryption-set と --data-disk-encryption-sets を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-414">vm/vmss create: Added --os-disk-encryption-set and --data-disk-encryption-sets.</span></span>

### <a name="core"></a><span data-ttu-id="16653-415">コア</span><span class="sxs-lookup"><span data-stu-id="16653-415">Core</span></span>

* <span data-ttu-id="16653-416">Python 3.4 のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-416">Removed support for Python 3.4</span></span>
* <span data-ttu-id="16653-417">複数のコマンドでの HaTS 調査のプラグイン</span><span class="sxs-lookup"><span data-stu-id="16653-417">Plug in HaTS survey in multiple commands</span></span>

### <a name="dls"></a><span data-ttu-id="16653-418">DLS</span><span class="sxs-lookup"><span data-stu-id="16653-418">DLS</span></span>

* <span data-ttu-id="16653-419">ADLS SDK バージョンを更新しました (0.0.48)。</span><span class="sxs-lookup"><span data-stu-id="16653-419">Updated ADLS sdk version (0.0.48).</span></span>

### <a name="install"></a><span data-ttu-id="16653-420">インストール</span><span class="sxs-lookup"><span data-stu-id="16653-420">Install</span></span>

* <span data-ttu-id="16653-421">インストール スクリプトで python 3.8 がサポートされます</span><span class="sxs-lookup"><span data-stu-id="16653-421">Install script support python 3.8</span></span>

### <a name="iot"></a><span data-ttu-id="16653-422">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-422">IOT</span></span>

* <span data-ttu-id="16653-423">[重大な変更] manual-failover から --failover-region パラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="16653-423">[BREAKING CHANGE] Removed --failover-region parameter from manual-failover.</span></span> <span data-ttu-id="16653-424">これで、割り当てられた geo ペアのセカンダリ リージョンにフェールオーバーします。</span><span class="sxs-lookup"><span data-stu-id="16653-424">Now it will failover to assigned geo-paired secondary region.</span></span>

### <a name="key-vault"></a><span data-ttu-id="16653-425">Key Vault</span><span class="sxs-lookup"><span data-stu-id="16653-425">Key Vault</span></span>

* <span data-ttu-id="16653-426">#8095 を修正: `az keyvault storage remove`: ヘルプ メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="16653-426">Fixed #8095: `az keyvault storage remove`: improve the help message</span></span>
* <span data-ttu-id="16653-427">#8921 を修正: `az keyvault key/secret/certificate list/list-deleted/list-versions`: パラメーター `--maxresults` の検証のバグを修正します</span><span class="sxs-lookup"><span data-stu-id="16653-427">Fixed #8921: `az keyvault key/secret/certificate list/list-deleted/list-versions`: fix the validation bug on parameter `--maxresults`</span></span>
* <span data-ttu-id="16653-428">#10512 を修正: `az keyvault set-policy`: `--object-id`、`--spn`、`--upn` のいずれも指定されていない場合のエラー メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="16653-428">Fixed #10512: `az keyvault set-policy`: improve the error message when none of `--object-id`, `--spn` or `--upn` is specified</span></span>
* <span data-ttu-id="16653-429">#10846 を修正: `az keyvault secret show-deleted`: `--id` を指定した場合、`--name/-n` は必要ありません</span><span class="sxs-lookup"><span data-stu-id="16653-429">Fixed #10846: `az keyvault secret show-deleted`: when `--id` is specified, `--name/-n` is not required</span></span>
* <span data-ttu-id="16653-430">#11084 を修正: `az keyvault secret download`: パラメーター `--encoding` のヘルプ メッセージを改善します</span><span class="sxs-lookup"><span data-stu-id="16653-430">Fixed #11084: `az keyvault secret download`: improve the help message of parameter `--encoding`</span></span>

### <a name="network"></a><span data-ttu-id="16653-431">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-431">Network</span></span>

* <span data-ttu-id="16653-432">az network application-gateway probe:作成および更新時にバックエンド サーバーをプローブするためのポートを指定する --port オプションのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-432">az network application-gateway probe: Added support --port option to specify a port for probing backend servers when create and update</span></span>
* <span data-ttu-id="16653-433">az network application-gateway url-path-map create/update: `--waf-policy` のバグ修正</span><span class="sxs-lookup"><span data-stu-id="16653-433">az network application-gateway url-path-map create/update: bug fix for `--waf-policy`</span></span>
* <span data-ttu-id="16653-434">az network application-gateway:`--rewrite-rule-set` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-434">az network application-gateway: Added support `--rewrite-rule-set`</span></span>
* <span data-ttu-id="16653-435">az network list-service-aliases:サービス エンドポイント ポリシーに使用できるサービス別名を一覧表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-435">az network list-service-aliases: Added support list service aliases which can be used for Service Endpoint Policies</span></span>
* <span data-ttu-id="16653-436">az network dns zone import:レコード名での .@ のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-436">az network dns zone import: Added support .@ in record name</span></span>

### <a name="packaging"></a><span data-ttu-id="16653-437">梱包</span><span class="sxs-lookup"><span data-stu-id="16653-437">Packaging</span></span>

* <span data-ttu-id="16653-438">pip インストール用のバック エッジ ビルドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-438">Added back edge builds for pip install</span></span>
* <span data-ttu-id="16653-439">Ubuntu eoan パッケージを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-439">Added Ubuntu eoan package</span></span>

### <a name="policy"></a><span data-ttu-id="16653-440">ポリシー</span><span class="sxs-lookup"><span data-stu-id="16653-440">Policy</span></span>

* <span data-ttu-id="16653-441">ポリシー API バージョン 2019-09-01 のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-441">Added support for Policy API version 2019-09-01.</span></span>
* <span data-ttu-id="16653-442">az policy set-definition:`--definition-groups` パラメーターを使用したポリシー セット定義内のグループ化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-442">az policy set-definition: Added support grouping within policy set definitions with `--definition-groups` parameter</span></span>

### <a name="redis"></a><span data-ttu-id="16653-443">Redis</span><span class="sxs-lookup"><span data-stu-id="16653-443">Redis</span></span>

* <span data-ttu-id="16653-444">`az redis create` コマンドにプレビュー パラメーター `--replicas-per-master` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-444">Added preview param `--replicas-per-master` to `az redis create` command</span></span>
* <span data-ttu-id="16653-445">azure-mgmt-redis を 6.0.0 から 7.0.0rc1 に更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-445">Updated azure-mgmt-redis from 6.0.0 to 7.0.0rc1</span></span>

### <a name="servicefabric"></a><span data-ttu-id="16653-446">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="16653-446">ServiceFabric</span></span>

* <span data-ttu-id="16653-447">#10963 を含む node-type 追加ロジックを修正:持続性レベル Gold で新しいノード タイプを追加すると、常に CLI エラーがスローされる</span><span class="sxs-lookup"><span data-stu-id="16653-447">Fixed in node-type add logic including #10963: Adding new node type with durability level Gold will always throw CLI error</span></span>
* <span data-ttu-id="16653-448">作成テンプレートの ServiceFabricNodeVmExt バージョンを 1.1 に更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-448">Updated ServiceFabricNodeVmExt version to 1.1 in creation template</span></span>

### <a name="sql"></a><span data-ttu-id="16653-449">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-449">SQL</span></span>

* <span data-ttu-id="16653-450">読み取りスケール管理をサポートするために、sql db create および update コマンドに "--read-scale" と "--read-replicas" パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-450">Added "--read-scale" and "--read-replicas" parameters to sql db create and update commands, to support read scale management.</span></span>

### <a name="storage"></a><span data-ttu-id="16653-451">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-451">Storage</span></span>

* <span data-ttu-id="16653-452">GA リリースでの storage account create および update コマンド用の大きいファイルの共有プロパティ</span><span class="sxs-lookup"><span data-stu-id="16653-452">GA Release Large File Shares property for storage account create and update command</span></span>
* <span data-ttu-id="16653-453">GA リリースでのユーザー委任 SAS トークンのサポート</span><span class="sxs-lookup"><span data-stu-id="16653-453">GA Release User Delegation SAS token Support</span></span>
* <span data-ttu-id="16653-454">ストレージ アカウントの Blob service のプロパティを管理するための新しいコマンド `az storage account blob-service-properties show` と `az storage account blob-service-properties update --enable-change-feed` が追加されました。</span><span class="sxs-lookup"><span data-stu-id="16653-454">Added new commands `az storage account blob-service-properties show` and `az storage account blob-service-properties update --enable-change-feed` to manage blob service properties for storage account.</span></span>
* <span data-ttu-id="16653-455">[今後の破壊的変更] `az storage copy`: `*` 文字は URL 内のワイルドカードとしてサポートされなくなりましたが、新しいパラメーターの --include-pattern と --exclude-pattern が `*` ワイルドカードをサポートして追加されます。</span><span class="sxs-lookup"><span data-stu-id="16653-455">[COMING BREAKING CHANGE] `az storage copy`: `*` character is no longer supported as a wildcard in URL, but new parameters --include-pattern and --exclude-pattern will be added with `*` wildcard support.</span></span>
* <span data-ttu-id="16653-456">問題 #11043 を修正:`az storage remove` コマンドでコンテナー/共有全体を削除するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-456">Fixed issue #11043: Added support to remove whole container/share in `az storage remove` command</span></span>

## <a name="november-26-2019"></a><span data-ttu-id="16653-457">2019 年 11 月 26 日</span><span class="sxs-lookup"><span data-stu-id="16653-457">November 26, 2019</span></span>

<span data-ttu-id="16653-458">バージョン 2.0.77</span><span class="sxs-lookup"><span data-stu-id="16653-458">Version 2.0.77</span></span>

### <a name="acr"></a><span data-ttu-id="16653-459">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-459">ACR</span></span>

* <span data-ttu-id="16653-460">acr task create/update からパラメーター `--branch` が非推奨になりました</span><span class="sxs-lookup"><span data-stu-id="16653-460">Deprecated parameter `--branch` from acr task create/update</span></span>

### <a name="azure-red-hat-openshift"></a><span data-ttu-id="16653-461">Azure Red Hat OpenShift</span><span class="sxs-lookup"><span data-stu-id="16653-461">Azure Red Hat OpenShift</span></span>

* <span data-ttu-id="16653-462">監視を使用して Azure Red Hat Openshift クラスターを作成できるように、`--workspace-resource-id` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-462">Added `--workspace-resource-id` flag to allow creation of Azure Red Hat Openshift cluster with monitoring</span></span>
* <span data-ttu-id="16653-463">監視を使用して Azure Red Hat OpenShift クラスターを作成するために `monitor_profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-463">Added `monitor_profile` to create Azure Red Hat OpenShift cluster with monitoring</span></span>

### <a name="aks"></a><span data-ttu-id="16653-464">AKS</span><span class="sxs-lookup"><span data-stu-id="16653-464">AKS</span></span>

* <span data-ttu-id="16653-465">"az aks rotate-certs" を使用したクラスター証明書ローテーション操作のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-465">Added support cluster certificate rotation operation using "az aks rotate-certs".</span></span>

### <a name="appconfig"></a><span data-ttu-id="16653-466">AppConfig</span><span class="sxs-lookup"><span data-stu-id="16653-466">AppConfig</span></span>

* <span data-ttu-id="16653-467">`as az appconfig kv import` の区切り文字に ":" を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-467">Added support for using ":" for `as az appconfig kv import` separator</span></span>
* <span data-ttu-id="16653-468">null ラベルを含む複数のラベルを持つキー値の一覧表示に関する問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="16653-468">Fixed issue for listing key values with multiple labels including null label.</span></span> 
* <span data-ttu-id="16653-469">管理プレーン SKD である azure-mgmt-appconfiguration を バージョン 0.3.0 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="16653-469">Updated management plane sdk, azure-mgmt-appconfiguration, to version 0.3.0.</span></span> 

### <a name="appservice"></a><span data-ttu-id="16653-470">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-470">AppService</span></span>

* <span data-ttu-id="16653-471">問題 #11100 を修正:サービス プランの作成時の az webapp up の AttributeError</span><span class="sxs-lookup"><span data-stu-id="16653-471">Fixed issue #11100: AttributeError for az webapp up when create service plan</span></span>
* <span data-ttu-id="16653-472">az webapp up:サポートされている言語のサイトに作成またはデプロイを強制します。既定値は使用されません。</span><span class="sxs-lookup"><span data-stu-id="16653-472">az webapp up: Forcing the creation or deployment to a site for supported languages, no defaults used.</span></span>
* <span data-ttu-id="16653-473">App Service Environment のサポートを追加しました: az appservice ase show | list | list-addresses | list-plans | create | update | delete</span><span class="sxs-lookup"><span data-stu-id="16653-473">Added support for App Service Environment: az appservice ase show | list | list-addresses | list-plans | create | update | delete</span></span>

### <a name="backup"></a><span data-ttu-id="16653-474">バックアップ</span><span class="sxs-lookup"><span data-stu-id="16653-474">Backup</span></span>

* <span data-ttu-id="16653-475">az backup policy list-associated-items の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="16653-475">Fixed issue in az backup policy list-associated-items.</span></span> <span data-ttu-id="16653-476">省略可能な BackupManagementType パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-476">Added optional BackupManagementType parameter.</span></span>

### <a name="compute"></a><span data-ttu-id="16653-477">Compute</span><span class="sxs-lookup"><span data-stu-id="16653-477">Compute</span></span>

* <span data-ttu-id="16653-478">コンピューティング、ディスク、スナップショットの API バージョンを 2019-07-01 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="16653-478">Upgraded API version of compute, disks, snapshots to 2019-07-01</span></span>
* <span data-ttu-id="16653-479">vmss create: --orchestration-mode の改善</span><span class="sxs-lookup"><span data-stu-id="16653-479">vmss create: Improvement for --orchestration-mode</span></span>
* <span data-ttu-id="16653-480">sig image-definition create: --os-state を追加して、このイメージの下に作成された仮想マシンを "一般化" するか、または "特殊化" するかを指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="16653-480">sig image-definition create: Added --os-state to allow specifying whether the virtual machines created under this image are 'Generalized' or 'Specialized'</span></span>
* <span data-ttu-id="16653-481">sig image-definition create: --hyper-v-generation を追加して、ハイパーバイザーの生成を指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="16653-481">sig image-definition create: Added --hyper-v-generation to allow specifying the hypervisor generation</span></span>
* <span data-ttu-id="16653-482">sig image-version create: --os-snapshot と --data-snapshots のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-482">sig image-version create: Added support --os-snapshot and --data-snapshots</span></span>
* <span data-ttu-id="16653-483">image create: --data-disk-caching を追加して、データ ディスクのキャッシュ設定を指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="16653-483">image create: Added --data-disk-caching to allow specifying caching setting of data disks</span></span>
* <span data-ttu-id="16653-484">Python Compute SDK を 10.0.0 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="16653-484">Upgraded Python Compute SDK to 10.0.0</span></span>
* <span data-ttu-id="16653-485">vm/vmss create: 'Priority' 列挙型プロパティに 'Spot' を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-485">vm/vmss create: Added 'Spot' to 'Priority' enum property</span></span>
* <span data-ttu-id="16653-486">[重大な変更] Swagger と Powershell のコマンドレットとの一貫性を維持するために、VM と VMSS の両方で '--max-billing' パラメーターを '--max-price' に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-486">[Breaking change] Renamed '--max-billing' parameter to '--max-price', for both VM and VMSS, to be consistent with Swagger and Powershell cmdlets</span></span>
* <span data-ttu-id="16653-487">vm monitor log show: リンクされた Log Analytics ワークスペースに対してログのクエリを実行するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-487">vm monitor log show: Added support for querying log over linked log analytics workspace.</span></span>

### <a name="iot"></a><span data-ttu-id="16653-488">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-488">IOT</span></span>

* <span data-ttu-id="16653-489">#2531 の修正: ハブの更新に便利な引数を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-489">Fix #2531: Added convenience arguments for hub update.</span></span>
* <span data-ttu-id="16653-490">#8323 の修正: ストレージ カスタム エンドポイントを作成するために不足しているパラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-490">Fix #8323: Added missing parameters to create storage custom endpoint.</span></span>
* <span data-ttu-id="16653-491">回帰バグの修正: 既定のストレージ エンドポイントをオーバーライドする変更を元に戻しました。</span><span class="sxs-lookup"><span data-stu-id="16653-491">Fix regression bug: Reverted the changes which overrides the default storage endpoint.</span></span>

### <a name="key-vault"></a><span data-ttu-id="16653-492">Key Vault</span><span class="sxs-lookup"><span data-stu-id="16653-492">Key Vault</span></span>

* <span data-ttu-id="16653-493">#11121 を修正しました: `az keyvault certificate list` を使用する場合、`--include-pending` を渡すときに `true` または `false` の値が必須ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="16653-493">Fixed #11121: When using `az keyvault certificate list`, passing `--include-pending` now doesn't require a value of `true` or `false`</span></span>

### <a name="netappfiles"></a><span data-ttu-id="16653-494">NetAppFiles</span><span class="sxs-lookup"><span data-stu-id="16653-494">NetAppFiles</span></span>

* <span data-ttu-id="16653-495">azure-mgmt-netapp を 0.7.0 にアップグレードしました。これには、今後のレプリケーション操作に関連した追加のボリューム プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="16653-495">Upgraded azure-mgmt-netapp to 0.7.0 which includes some additional volume properties associated with upcoming replication operations</span></span>

### <a name="network"></a><span data-ttu-id="16653-496">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-496">Network</span></span>

* <span data-ttu-id="16653-497">application-gateway waf-config: 非推奨になりました</span><span class="sxs-lookup"><span data-stu-id="16653-497">application-gateway waf-config: deprecated</span></span>
* <span data-ttu-id="16653-498">application-gateway waf-policy: 管理されているルール セットと除外ルールを管理するために、サブグループ managed-rules を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-498">application-gateway waf-policy: Added subgroup managed-rules to manage managed rule sets and exclusion rules</span></span>
* <span data-ttu-id="16653-499">application-gateway waf-policy: waf-policy のグローバル構成を管理するために、サブグループ policy-setting を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-499">application-gateway waf-policy: Added subgroup policy-setting to manage global configuration of a waf-policy</span></span>
* <span data-ttu-id="16653-500">[重大な変更] application-gateway waf-policy: subgroup rule を custom-rule に名前変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-500">[BREAKING CHANGE] application-gateway waf-policy: Renamed subgroup rule to custom-rule</span></span>
* <span data-ttu-id="16653-501">application-gateway http-listener: 作成時の --firewall-policy を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-501">application-gateway http-listener: Added --firewall-policy when create</span></span>
* <span data-ttu-id="16653-502">application-gateway url-path-map rule: 作成時の --firewall-policy を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-502">application-gateway url-path-map rule: Added --firewall-policy when create</span></span>

### <a name="packaging"></a><span data-ttu-id="16653-503">梱包</span><span class="sxs-lookup"><span data-stu-id="16653-503">Packaging</span></span>

* <span data-ttu-id="16653-504">az ラッパーを Python で書き直しました</span><span class="sxs-lookup"><span data-stu-id="16653-504">Rewrote the az wrapper in Python</span></span>
* <span data-ttu-id="16653-505">Python 3.8 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-505">Added support for Python 3.8</span></span>
* <span data-ttu-id="16653-506">RPM パッケージで Python 3 に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-506">Changed to Python 3 for RPM package</span></span>

### <a name="profile"></a><span data-ttu-id="16653-507">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-507">Profile</span></span>

* <span data-ttu-id="16653-508">Microsoft アカウントで `az login -u {} -p {}` を実行するときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-508">Polished error when running `az login -u {} -p {}` with Microsoft account</span></span>
* <span data-ttu-id="16653-509">自己署名ルート証明書使用してプロキシの背後で `az login` を実行するときの `SSLError` を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-509">Polished `SSLError` when running `az login` behind a proxy with self-signed root certificate</span></span>
* <span data-ttu-id="16653-510">#10578 を修正: Windows または WSL で同時に複数のインスタンスを起動すると `az login` がハングする</span><span class="sxs-lookup"><span data-stu-id="16653-510">Fixed #10578: `az login` hangs when more than one instances are launched at the same time on Windows or WSL</span></span>
* <span data-ttu-id="16653-511">#11059 を修正: テナントにサブスクリプションがあると `az login --allow-no-subscriptions` が失敗する</span><span class="sxs-lookup"><span data-stu-id="16653-511">Fixed #11059: `az login --allow-no-subscriptions` fails if there are subscriptions in the tenant</span></span>
* <span data-ttu-id="16653-512">#11238 を修正: サブスクリプションの名前を変更した後、MSI を使用してログインすると、同じサブスクリプションが 2 回表示される</span><span class="sxs-lookup"><span data-stu-id="16653-512">Fixed #11238: After renaming a subscription, logging in with MSI will result in the same subscription appearing twice</span></span>

### <a name="rbac"></a><span data-ttu-id="16653-513">RBAC</span><span class="sxs-lookup"><span data-stu-id="16653-513">RBAC</span></span>

* <span data-ttu-id="16653-514">#10996 を修正: `--password` が指定されていないときの `az ad user update` での `--force-change-password-next-login` のエラーを改善</span><span class="sxs-lookup"><span data-stu-id="16653-514">Fixed #10996: Polish error for `--force-change-password-next-login` in `az ad user update` when `--password` is not specified</span></span>

### <a name="redis"></a><span data-ttu-id="16653-515">Redis</span><span class="sxs-lookup"><span data-stu-id="16653-515">Redis</span></span>

* <span data-ttu-id="16653-516">#2902 を修正: Basic SKU キャッシュの更新中、メモリ構成を設定しない</span><span class="sxs-lookup"><span data-stu-id="16653-516">Fixed #2902: Avoid setting memory configs while updating Basic SKU cache</span></span>

### <a name="reservations"></a><span data-ttu-id="16653-517">Reservations</span><span class="sxs-lookup"><span data-stu-id="16653-517">Reservations</span></span>

* <span data-ttu-id="16653-518">SDK バージョンを 0.6.0 にアップグレードしました</span><span class="sxs-lookup"><span data-stu-id="16653-518">Upgraded SDK Version to 0.6.0</span></span>
* <span data-ttu-id="16653-519">Gat-Gatalogs を呼び出した後の billingplan の詳細情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-519">Added billingplan details info after calling Get-Gatalogs</span></span>
* <span data-ttu-id="16653-520">予約の価格を計算するための新しいコマンド `az reservations reservation-order calculate` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-520">Added new command `az reservations reservation-order calculate` to calculate the price for a reservation</span></span>
* <span data-ttu-id="16653-521">新しい予約を購入するための新しいコマンド `az reservations reservation-order purchase` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-521">Added new command `az reservations reservation-order purchase` to purchase a new reservation</span></span>

### <a name="rest"></a><span data-ttu-id="16653-522">REST</span><span class="sxs-lookup"><span data-stu-id="16653-522">Rest</span></span>
* <span data-ttu-id="16653-523">`az rest` を GA に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-523">Changed `az rest` to GA</span></span>

### <a name="sql"></a><span data-ttu-id="16653-524">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-524">SQL</span></span>

* <span data-ttu-id="16653-525">azure-mgmt-sql をバージョン 0.15.0 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="16653-525">Updated azure-mgmt-sql to version 0.15.0.</span></span>

### <a name="storage"></a><span data-ttu-id="16653-526">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-526">Storage</span></span>

* <span data-ttu-id="16653-527">storage account create: Blob service でのファイルシステムのセマンティクスをサポートするために、--enable-hierarchical-namespace を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-527">storage account create: Added --enable-hierarchical-namespace to support filesystem semantics in blob service.</span></span>
* <span data-ttu-id="16653-528">エラー メッセージから関連性のない例外を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-528">Removed unrelated exception from error message</span></span>
* <span data-ttu-id="16653-529">"この操作を実行するのに必要なアクセス許可がありません" という誤ったエラー メッセージが</span><span class="sxs-lookup"><span data-stu-id="16653-529">Fixed issues with incorrect error message "You do not have the required permissions needed to perform this operation."</span></span> <span data-ttu-id="16653-530">ネットワーク ルールまたは AuthenticationFailed によってブロックされた場合に表示される問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="16653-530">when blocked by network rules or AuthenticationFailed.</span></span>

## <a name="november-4-2019"></a><span data-ttu-id="16653-531">2019 年 11 月 4 日</span><span class="sxs-lookup"><span data-stu-id="16653-531">November 4, 2019</span></span>

<span data-ttu-id="16653-532">バージョン 2.0.76</span><span class="sxs-lookup"><span data-stu-id="16653-532">Version 2.0.76</span></span>

### <a name="acr"></a><span data-ttu-id="16653-533">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-533">ACR</span></span>

* <span data-ttu-id="16653-534">コマンド `az acr pack build` にプレビュー パラメーター `--pack-image-tag` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-534">Added a preview parameter `--pack-image-tag` to command `az acr pack build`.</span></span>
* <span data-ttu-id="16653-535">レジストリ作成時の監査を有効にするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-535">Added support for enabling auditing on creating a registry</span></span>
* <span data-ttu-id="16653-536">レジストリ スコープが設定された RBAC のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-536">Added support for Repository-scoped RBAC</span></span>

### <a name="aks"></a><span data-ttu-id="16653-537">AKS</span><span class="sxs-lookup"><span data-stu-id="16653-537">AKS</span></span>

* <span data-ttu-id="16653-538">`az aks create` コマンドに `--enable-cluster-autoscaler`、`--min-count`、および `--max-count` を追加しました。これにより、ノード プールのクラスター オートスケーラーが有効になります。</span><span class="sxs-lookup"><span data-stu-id="16653-538">Added `--enable-cluster-autoscaler`, `--min-count` and `--max-count` to the `az aks create` command, which enables cluster autoscaler for the node pool.</span></span>
* <span data-ttu-id="16653-539">上記のフラグに加えて、`--update-cluster-autoscaler` および `--disable-cluster-autoscaler` を `az aks update` コマンドに追加し、クラスター オートスケーラーを更新できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="16653-539">Added the above flags as well as `--update-cluster-autoscaler` and `--disable-cluster-autoscaler` to the `az aks update` command, allowing updates to cluster autoscaler.</span></span>

### <a name="appconfig"></a><span data-ttu-id="16653-540">AppConfig</span><span class="sxs-lookup"><span data-stu-id="16653-540">AppConfig</span></span>

* <span data-ttu-id="16653-541">App Configuration に格納される機能フラグを管理するために、appconfig feature コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-541">Added appconfig feature command group to manage feature flags stored in an App Configuration.</span></span>
* <span data-ttu-id="16653-542">ファイルに対する appconfig kv export コマンドの軽微なバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="16653-542">Fixed minor bug for appconfig kv export to file command.</span></span> <span data-ttu-id="16653-543">エクスポート中に宛先ファイルの内容を読み取らないようにしました。</span><span class="sxs-lookup"><span data-stu-id="16653-543">Stop reading dest file contents during export.</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-544">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-544">AppService</span></span>

* <span data-ttu-id="16653-545">`az appservice plan create`:appservice plan create に "persitescaling" を設定するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-545">`az appservice plan create`: Added support to set 'persitescaling' on appservice plan create.</span></span>
* <span data-ttu-id="16653-546">webapp config ssl bind 操作がリソースから既存のタグを削除する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-546">Fixed an issue where webapp config ssl bind operation was removing existing tags from the resource</span></span>
* <span data-ttu-id="16653-547">関数アプリのデプロイ時にリモート ビルド アクションをサポートするために、`az functionapp deployment source config-zip` に `--build-remote` フラグを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-547">Added `--build-remote` flag for `az functionapp deployment source config-zip` to support remote build action during function app deployment.</span></span>
* <span data-ttu-id="16653-548">Windows 向けの関数アプリの既定のノードバージョンを 10 に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-548">Changed default node version on function apps to ~10 for Windows</span></span>
* <span data-ttu-id="16653-549">`az functionapp create` に `--runtime-version` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-549">Added `--runtime-version` property to `az functionapp create`</span></span>

### <a name="arm"></a><span data-ttu-id="16653-550">ARM</span><span class="sxs-lookup"><span data-stu-id="16653-550">ARM</span></span>

* <span data-ttu-id="16653-551">`az deployment/group deployment validate`:デプロイ時に、json テンプレートで複数行とコメントをサポートするために `--handle-extended-json-format` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-551">`az deployment/group deployment validate`: Added `--handle-extended-json-format` parameter to support multiline and comments in json template when deployment.</span></span>
* <span data-ttu-id="16653-552">azure-mgmt-resource を 2019-07-01 に引き上げました</span><span class="sxs-lookup"><span data-stu-id="16653-552">Bumped azure-mgmt-resource to 2019-07-01</span></span>

### <a name="backup"></a><span data-ttu-id="16653-553">バックアップ</span><span class="sxs-lookup"><span data-stu-id="16653-553">Backup</span></span>

* <span data-ttu-id="16653-554">AzureFiles のバックアップ サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-554">Added AzureFiles backup support</span></span>

### <a name="compute"></a><span data-ttu-id="16653-555">Compute</span><span class="sxs-lookup"><span data-stu-id="16653-555">Compute</span></span>

* <span data-ttu-id="16653-556">`az vm create`:高速ネットワークと既存の NIC を一緒に指定した場合の警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-556">`az vm create`: Added warning when specifying accelerated networking and an existing NIC together.</span></span>
* <span data-ttu-id="16653-557">`az vm create`:仮想マシンを割り当てる必要がある既存の仮想マシン スケール セットを指定するための `--vmss` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-557">`az vm create`: Added `--vmss` to specify an existing virtual machine scale set that the virtual machine should be assigned to.</span></span>
* <span data-ttu-id="16653-558">`az vm/vmss create`:イメージ エイリアス ファイルのローカル コピーを追加し、制限付きネットワーク環境でそれにアクセスできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="16653-558">`az vm/vmss create`: Added a local copy of image alias file so that it can be accessed in a restricted network environment.</span></span>
* <span data-ttu-id="16653-559">`az vmss create`:スケール セットによる仮想マシンの管理方法を指定するための `--orchestration-mode` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-559">`az vmss create`: Added `--orchestration-mode` to specify how virtual machines are managed by the scale set.</span></span>
* <span data-ttu-id="16653-560">`az vm/vmss update`:Ultra SSD 設定を更新できるように `--ultra-ssd-enabled` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-560">`az vm/vmss update`: Added `--ultra-ssd-enabled` to allow updating ultra SSD setting.</span></span>
* <span data-ttu-id="16653-561">[破壊的変更] `az vm extension set`:ユーザーが `--ids` を使用して、VM に拡張機能を設定できないバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="16653-561">[BREAKING CHANGE] `az vm extension set`: Fixed bug where users could not set an extension on a VM with `--ids`.</span></span>
* <span data-ttu-id="16653-562">Azure Marketplace イメージの使用条件を管理するための新しいコマンド `az vm image terms accept/cancel/show` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-562">Added new commands `az vm image terms accept/cancel/show` to manage Azure Marketplace image terms.</span></span>
* <span data-ttu-id="16653-563">VMAccessForLinux をバージョン 1.5 に更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-563">Updated VMAccessForLinux to version 1.5</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="16653-564">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-564">CosmosDB</span></span>

* <span data-ttu-id="16653-565">[破壊的変更] `az sql container create`:`--partition-key-path` を必須パラメーターに変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-565">[BREAKING CHANGE] `az sql container create`: Changed `--partition-key-path` to required parameter</span></span>
* <span data-ttu-id="16653-566">[破壊的変更] `az gremlin graph create`:`--partition-key-path` を必須パラメーターに変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-566">[BREAKING CHANGE] `az gremlin graph create`: Changed `--partition-key-path` to required parameter</span></span>
* <span data-ttu-id="16653-567">`az sql container create`:`--unique-key-policy` および `--conflict-resolution-policy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-567">`az sql container create`: Added `--unique-key-policy` and `--conflict-resolution-policy`</span></span>
* <span data-ttu-id="16653-568">`az sql container create/update`:既定のスキーマ `--idx` を更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-568">`az sql container create/update`: Updated the `--idx` default schema</span></span>
* <span data-ttu-id="16653-569">`gremlin graph create`:`--conflict-resolution-policy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-569">`gremlin graph create`: Added `--conflict-resolution-policy`</span></span>
* <span data-ttu-id="16653-570">`gremlin graph create/update`:既定のスキーマ `--idx` を更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-570">`gremlin graph create/update`: Updated the `--idx` default schema</span></span>
* <span data-ttu-id="16653-571">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-571">Fixed typo in help message</span></span>
* <span data-ttu-id="16653-572">データベース:非推奨の情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-572">database: Added deprecation information</span></span>
* <span data-ttu-id="16653-573">コレクション:非推奨の情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-573">collection: Added deprecation information</span></span>

### <a name="iot"></a><span data-ttu-id="16653-574">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-574">IoT</span></span>

* <span data-ttu-id="16653-575">新しいルーティング ソースの種類を追加しました: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="16653-575">Added new routing source type: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="16653-576">`az iot hub create` の不十分な機能を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-576">Fixed missing features in `az iot hub create`</span></span>

### <a name="key-vault"></a><span data-ttu-id="16653-577">Key Vault</span><span class="sxs-lookup"><span data-stu-id="16653-577">Key Vault</span></span>

* <span data-ttu-id="16653-578">証明書ファイルが存在しない場合の予期しないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-578">Fixed an unexpected error when certificate file does not exist</span></span>
* <span data-ttu-id="16653-579">`az keyvault recover/purge` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-579">Fixed `az keyvault recover/purge` not working</span></span>

### <a name="netappfiles"></a><span data-ttu-id="16653-580">NetAppFiles</span><span class="sxs-lookup"><span data-stu-id="16653-580">NetAppFiles</span></span>

* <span data-ttu-id="16653-581">API バージョン 2019-07-01 を使用するために azure-mgmt-netapp を 0.6.0 にアップグレードしました。</span><span class="sxs-lookup"><span data-stu-id="16653-581">Upgraded azure-mgmt-netapp to 0.6.0 to use API version 2019-07-01.</span></span> <span data-ttu-id="16653-582">この新しい API バージョンには以下の変更内容が含まれます。</span><span class="sxs-lookup"><span data-stu-id="16653-582">This new API version includes:</span></span>

    - <span data-ttu-id="16653-583">ボリューム作成の `--protocol-types` が "NFSv4" ではなく "NFSv 4.1" を受け入れるようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-583">Volume creation `--protocol-types` accepts now "NFSv4.1" not "NFSv4"</span></span>
    - <span data-ttu-id="16653-584">ボリューム エクスポート ポリシー プロパティの名前が "nfsv4" ではなく "nfsv41" に変更されました</span><span class="sxs-lookup"><span data-stu-id="16653-584">Volume export policy property now named 'nfsv41' not 'nfsv4'</span></span>
    - <span data-ttu-id="16653-585">ボリュームの `--creation-token` の名前が `--file-path` に変更されました</span><span class="sxs-lookup"><span data-stu-id="16653-585">Volume `--creation-token` renamed to `--file-path`</span></span>
    - <span data-ttu-id="16653-586">スナップショット作成日の名前が単に "created" に変更されました</span><span class="sxs-lookup"><span data-stu-id="16653-586">Snapshot creation date now named just 'created'</span></span>

### <a name="network"></a><span data-ttu-id="16653-587">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-587">Network</span></span>

* <span data-ttu-id="16653-588">`az network private-dns link vnet create/update`:テナント間の仮想ネットワーク リンクがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="16653-588">`az network private-dns link vnet create/update`: Support cross-tenant virtual network linking.</span></span>
* <span data-ttu-id="16653-589">[破壊的変更] `az network vnet subnet list`:`--resource-group` と `--vnet-name` を必須に変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-589">[BREAKING CHANGE] `az network vnet subnet list`: Changed `--resource-group` and `--vnet-name` to be required now.</span></span>
* <span data-ttu-id="16653-590">`az network public-ip prefix create`:作成時に IP アドレスのバージョン (IPv4、IPv6) を指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-590">`az network public-ip prefix create`: Added support to specify IP address version (IPv4, IPv6) when creation</span></span>
* <span data-ttu-id="16653-591">azure-mgmt-network を 7.0.0 に、api-version を 2019-09-01 に引き上げました</span><span class="sxs-lookup"><span data-stu-id="16653-591">Bumped azure-mgmt-network to 7.0.0 and api-version to 2019-09-01</span></span>
* <span data-ttu-id="16653-592">`az network vrouter`:新しいサービスの仮想ルーターと仮想ルーター ピアリングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-592">`az network vrouter`: Added support for new service virtual router and virtual router peering</span></span>
* <span data-ttu-id="16653-593">`az network express-route gateway connection`:`--internet-security` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-593">`az network express-route gateway connection`: Added support for `--internet-security`</span></span>

### <a name="profile"></a><span data-ttu-id="16653-594">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-594">Profile</span></span>

* <span data-ttu-id="16653-595">`az account get-access-token --resource-type ms-graph` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-595">Fixed `az account get-access-token --resource-type ms-graph` not working</span></span>
* <span data-ttu-id="16653-596">`az login` からの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-596">Removed warning from `az login`</span></span>

### <a name="rbac"></a><span data-ttu-id="16653-597">RBAC</span><span class="sxs-lookup"><span data-stu-id="16653-597">RBAC</span></span>

* <span data-ttu-id="16653-598">`az ad app update --id {} --display-name {}` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-598">Fixed `az ad app update --id {} --display-name {}` doesn't work</span></span>

### <a name="servicefabric"></a><span data-ttu-id="16653-599">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="16653-599">ServiceFabric</span></span>

* <span data-ttu-id="16653-600">`az sf cluster create`:Service Fabric の Linux と Windows の template.json コンピューティング vmss を標準からマネージド ディスクに変更することによって問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-600">`az sf cluster create`: Fixed an issue by modifying service fabric linux and windows template.json compute vmss from standard to managed disks</span></span>

### <a name="sql"></a><span data-ttu-id="16653-601">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-601">SQL</span></span>

* <span data-ttu-id="16653-602">次の新しい SQL Database オファリングの CRUD 操作をサポートするために、`--compute-model`、`--auto-pause-delay`、および `--min-capacity` パラメーターを追加しました:サーバーレス コンピューティング モデル。</span><span class="sxs-lookup"><span data-stu-id="16653-602">Added `--compute-model`, `--auto-pause-delay`, and `--min-capacity` parameters to support CRUD operations for new SQL Database offering: Serverless compute model.</span></span>

### <a name="storage"></a><span data-ttu-id="16653-603">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-603">Storage</span></span>

* <span data-ttu-id="16653-604">`az storage account create/update`:Azure Files Active Directory Domain Services 認証をサポートするために、--enable-files-adds パラメーターと Azure Active Directory プロパティ引数グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-604">`az storage account create/update`: Added --enable-files-adds parameter and Azure Active Directory Properties Argument group to support Azure Files Active Directory Domain Service Authentication</span></span>
* <span data-ttu-id="16653-605">ストレージ アカウントの Kerberos キーの一覧表示または再生成をサポートするために、`az storage account keys list/renew` を拡張しました。</span><span class="sxs-lookup"><span data-stu-id="16653-605">Expanded `az storage account keys list/renew` to support listing or regenerating Kerberos keys of storage account.</span></span>

## <a name="october-15-2019"></a><span data-ttu-id="16653-606">2019 年 10 月 15 日</span><span class="sxs-lookup"><span data-stu-id="16653-606">October 15, 2019</span></span>

<span data-ttu-id="16653-607">バージョン 2.0.75</span><span class="sxs-lookup"><span data-stu-id="16653-607">Version 2.0.75</span></span>

### <a name="aks"></a><span data-ttu-id="16653-608">AKS</span><span class="sxs-lookup"><span data-stu-id="16653-608">AKS</span></span>

* <span data-ttu-id="16653-609">Kubernetes のバージョンでサポートされている場合、`--load-balancer-sku` の既定値を `standard` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-609">Changed `--load-balancer-sku` default value to `standard` if supported by the kubernetes version</span></span>
* <span data-ttu-id="16653-610">Kubernetes のバージョンでサポートされている場合、`--vm-set-type` の既定値を `virtualmachinescalesets` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-610">Changed `--vm-set-type` default value to `virtualmachinescalesets` if supported by the kubernetes version</span></span>

### <a name="ams"></a><span data-ttu-id="16653-611">AMS</span><span class="sxs-lookup"><span data-stu-id="16653-611">AMS</span></span>

* <span data-ttu-id="16653-612">[重大な変更]`job start` の名前を `job create` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-612">[BREAKING CHANGE] Changed the name of `job start` to `job create`</span></span>
* <span data-ttu-id="16653-613">[重大な変更]`content-key-policy create` の `--ask` パラメーターが UTF8 ではなく 32 文字の 16 進文字列を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-613">[BREAKING CHANGE] Changed the `--ask` parameter of `content-key-policy create` to use a 32-character hex string instead of UTF8</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-614">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-614">AppService</span></span>

* <span data-ttu-id="16653-615">コマンド `webapp config access-restriction show|set|add|remove` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-615">Added commands `webapp config access-restriction show|set|add|remove`</span></span>
* <span data-ttu-id="16653-616">より優れたエラー処理を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-616">Added better error handling to `webapp up`</span></span>
* <span data-ttu-id="16653-617">`Isolated` SKU のサポートを `appservice plan update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-617">Added support for `Isolated` SKU to `appservice plan update`</span></span>

### <a name="arm"></a><span data-ttu-id="16653-618">ARM</span><span class="sxs-lookup"><span data-stu-id="16653-618">ARM</span></span>

* <span data-ttu-id="16653-619">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `deployment create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-619">Added `--handle-extended-json-format` parameter `deployment create` to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="16653-620">Compute</span><span class="sxs-lookup"><span data-stu-id="16653-620">Compute</span></span>

* <span data-ttu-id="16653-621">`--enable-agent` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-621">Added `--enable-agent` parameter to `vm create`</span></span>
* <span data-ttu-id="16653-622">ゾーンを使用するときに標準のパブリック IP SKU を自動的に使用するように `vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-622">Changed `vm create` to use standard public IP SKU automatically when using zones</span></span>
* <span data-ttu-id="16653-623">VM の有効なコンピューター名が指定されていない場合に自動的に作成されるように `vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-623">Changed `vm create` to automatically create a valid computer name for a VM if none is provided</span></span>
* <span data-ttu-id="16653-624">VMSS 内の仮想マシンのカスタム コンピューター名プレフィックスをサポートするために `--computer-name-prefix` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-624">Added `--computer-name-prefix` parameter to `vmss create` to support custom computer name prefix of virtual machines in the VMSS</span></span>
* <span data-ttu-id="16653-625">ログ分析ワークスペースを自動的に有効にする `--workspace` パラメーターを `vm create` に追加します</span><span class="sxs-lookup"><span data-stu-id="16653-625">Add `--workspace` parameter to `vm create` to enable log analytics workspace automatically</span></span>
* <span data-ttu-id="16653-626">ギャラリーの API バージョンが 2019-07-01 に更新されました</span><span class="sxs-lookup"><span data-stu-id="16653-626">Updated galleries API version to 2019-07-01</span></span>

### <a name="core"></a><span data-ttu-id="16653-627">コア</span><span class="sxs-lookup"><span data-stu-id="16653-627">Core</span></span>

* <span data-ttu-id="16653-628">汎用の update コマンドで `--set` パラメーターの構文チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-628">Added syntax check for `--set` parameter in generic update command</span></span>

### <a name="iot"></a><span data-ttu-id="16653-629">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-629">IoT</span></span>

* <span data-ttu-id="16653-630">`iot hub show` で "リソースが見つかりません" のエラーが誤って発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-630">Fixed an issue where `iot hub show` would incorrectly error with "resource not found"</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-631">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-631">Monitor</span></span>

* <span data-ttu-id="16653-632">CRUD のサポートを `monitor log-analytics workspace` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-632">Added support for CRUD to `monitor log-analytics workspace`</span></span>

### <a name="network"></a><span data-ttu-id="16653-633">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-633">Network</span></span>

* <span data-ttu-id="16653-634">クロステナントの仮想リンクのサポートを `network private-dns link vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-634">Added support for cross-tenant virtual linking to `network private-dns link vnet [create|update]`</span></span>
* <span data-ttu-id="16653-635">[重大な変更]`network vnet subnet list` で `--resource-group` および `--vnet-name` パラメーターが必須に変更になりました</span><span class="sxs-lookup"><span data-stu-id="16653-635">[BREAKING CHANGE] Changed `network vnet subnet list` to require `--resource-group` and `--vnet-name` parameters</span></span>

### <a name="sql"></a><span data-ttu-id="16653-636">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-636">SQL</span></span>

* <span data-ttu-id="16653-637">マネージ インスタンスの AAD 管理者の設定をサポートするコマンドを `sql mi ad-admin` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-637">Added commands to `sql mi ad-admin` that support setting an AAD administrator on managed instances</span></span>

### <a name="storage"></a><span data-ttu-id="16653-638">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-638">Storage</span></span>

* <span data-ttu-id="16653-639">サービス間のコピー中にアクセス層を保持する `--preserve-s2s-access-tier` パラメーターを `storage copy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-639">Added `--preserve-s2s-access-tier` parameter `storage copy` to preserve access tier during service to service copy</span></span>
* <span data-ttu-id="16653-640">ストレージ アカウントで大容量ファイルの共有をサポートするために `--enable-large-file-share` パラメーターを `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-640">Added `--enable-large-file-share` parameter to `storage account [create|update]` to support large file shares for storage account</span></span>

## <a name="september-24-2019"></a><span data-ttu-id="16653-641">2019 年 9 月 24 日</span><span class="sxs-lookup"><span data-stu-id="16653-641">September 24, 2019</span></span>

<span data-ttu-id="16653-642">バージョン 2.0.74</span><span class="sxs-lookup"><span data-stu-id="16653-642">Version 2.0.74</span></span>

### <a name="acr"></a><span data-ttu-id="16653-643">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-643">ACR</span></span>

* <span data-ttu-id="16653-644">必須の `--type` パラメーターを `acr config retention update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-644">Added a required `--type` parameter to `acr config retention update`</span></span>
* <span data-ttu-id="16653-645">[重大な変更] `acr config` コマンド グループでパラメーター `--name -n` の名前が `--registry -r ` に変更されました</span><span class="sxs-lookup"><span data-stu-id="16653-645">[BREAKING CHANGE] Renamed parameter `--name -n` changed to `--registry -r ` for `acr config` command group</span></span>

### <a name="aks"></a><span data-ttu-id="16653-646">AKS</span><span class="sxs-lookup"><span data-stu-id="16653-646">AKS</span></span>

* <span data-ttu-id="16653-647">`--load-balancer-sku` パラメーターを `aks create` コマンドに追加しました。これにより、SLB を使用する AKS クラスターを作成できます</span><span class="sxs-lookup"><span data-stu-id="16653-647">Added `--load-balancer-sku` parameter to `aks create` command, which allows for creating AKS cluster with SLB</span></span>
* <span data-ttu-id="16653-648">`--load-balancer-managed-outbound-ip-count`、`--load-balancer-outbound-ips`、`--load-balancer-outbound-ip-prefixes` パラメーターを `aks [create|update]` コマンドに追加しました。これにより、SLB を使用する AKS クラスターのロード バランサー プロファイルを更新できます</span><span class="sxs-lookup"><span data-stu-id="16653-648">Added `--load-balancer-managed-outbound-ip-count`, `--load-balancer-outbound-ips` and `--load-balancer-outbound-ip-prefixes` parameters to `aks [create|update]` commands, which allow for updating load balancer profile of an AKS cluster with SLB</span></span>
* <span data-ttu-id="16653-649">`--vm-set-type` パラメーターを `aks create` コマンドに追加しました。これにより、AKS クラスターの VM の種類 (vmas または vmss) を指定できます</span><span class="sxs-lookup"><span data-stu-id="16653-649">Added `--vm-set-type` parameter to `aks create` command, which allows to specify vm types of an AKS Cluster (vmas or vmss)</span></span>

### <a name="arm"></a><span data-ttu-id="16653-650">ARM</span><span class="sxs-lookup"><span data-stu-id="16653-650">ARM</span></span>

* <span data-ttu-id="16653-651">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `group deployment create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-651">Added `--handle-extended-json-format` parameter to `group deployment create` command to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="16653-652">Compute</span><span class="sxs-lookup"><span data-stu-id="16653-652">Compute</span></span>

* <span data-ttu-id="16653-653">終了のスケジュール化されたイベントを構成しやすくするために `--terminate-notification-time` パラメーターを `vmss [create|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-653">Added `--terminate-notification-time` parameter to `vmss [create|update]` commands to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="16653-654">終了のスケジュール化されたイベントを構成しやすくするために `--enable-terminate-notification` パラメーターを `vmss update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-654">Added `--enable-terminate-notification` parameter to `vmss update` command to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="16653-655">`--priority,` `--eviction-policy,` `--max-billing` パラメーターを `[vm|vmss] create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-655">Added `--priority,` `--eviction-policy,` `--max-billing` parameters to `[vm|vmss] create` commands</span></span>
* <span data-ttu-id="16653-656">`disk create` を変更し、ディスク アップロードの正確なサイズを指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="16653-656">Changed `disk create` to allow specifying the exact size of the disk upload</span></span>
* <span data-ttu-id="16653-657">マネージド ディスクの増分スナップショットのサポートを `snapshot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-657">Added support for incremental snapshots for managed disks to `snapshot create`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="16653-658">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-658">Cosmos DB</span></span>

* <span data-ttu-id="16653-659">キー、読み取り専用キー、または接続文字列を表示する `--type <key-type>` パラメーターを `cosmosdb keys list` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-659">Added `--type <key-type>` parameter to `cosmosdb keys list` command to show key, read only keys or connection strings</span></span>
* <span data-ttu-id="16653-660">`cosmosdb keys regenerate` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-660">Added `cosmosdb keys regenerate` command</span></span>
* <span data-ttu-id="16653-661">[非推奨]`cosmosdb list-connection-strings`、`cosmosdb regenerate-key`、`cosmosdb list-read-only-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-661">[DEPRECATED] Deprecated `cosmosdb list-connection-strings`, `cosmosdb regenerate-key` and `cosmosdb list-read-only-keys` commands</span></span>

### <a name="eventgrid"></a><span data-ttu-id="16653-662">EventGrid</span><span class="sxs-lookup"><span data-stu-id="16653-662">EventGrid</span></span>

* <span data-ttu-id="16653-663">正しいパラメーターを参照するようにエンドポイントのヘルプ テキストを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-663">Fixed the endpoint help text to refer to the right parameter</span></span>

### <a name="key-vault"></a><span data-ttu-id="16653-664">Key Vault</span><span class="sxs-lookup"><span data-stu-id="16653-664">Key Vault</span></span>

* <span data-ttu-id="16653-665">テナントを使用してログインすると (`login -t`)、`keyvault create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-665">Fixed issue where logging in with a tenant (`login -t`) could cause `keyvault create` to fail</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-666">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-666">Monitor</span></span>

* <span data-ttu-id="16653-667">`monitor metrics alert create` の `--condition` 引数で `:` 文字を使用できないという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-667">Fixed issue where `:` character was not allowed in `--condition` argument to `monitor metrics alert create`</span></span>

### <a name="policy"></a><span data-ttu-id="16653-668">ポリシー</span><span class="sxs-lookup"><span data-stu-id="16653-668">Policy</span></span>

* <span data-ttu-id="16653-669">Policy API バージョン 2019-06-01 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-669">Added support for Policy API version 2019-06-01</span></span>
* <span data-ttu-id="16653-670">`policy assignment create` コマンドに `--enforcement-mode` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-670">Added `--enforcement-mode` parameter to `policy assignment create` command</span></span>

### <a name="storage"></a><span data-ttu-id="16653-671">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-671">Storage</span></span>

* <span data-ttu-id="16653-672">`az storage copy` コマンドに `--blob-type` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-672">Added `--blob-type` parameter to `az storage copy` command</span></span>

## <a name="september-10-2019"></a><span data-ttu-id="16653-673">2019 年 9 月 10 日</span><span class="sxs-lookup"><span data-stu-id="16653-673">September 10, 2019</span></span>

### <a name="acr"></a><span data-ttu-id="16653-674">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-674">ACR</span></span>

* <span data-ttu-id="16653-675">アイテム保持ポリシーを構成するためのコマンド グループ `acr config retention` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-675">Added command group `acr config retention` to configure retention policy</span></span>

### <a name="aks"></a><span data-ttu-id="16653-676">AKS</span><span class="sxs-lookup"><span data-stu-id="16653-676">AKS</span></span>

* <span data-ttu-id="16653-677">次のコマンドを使用した ACR 統合のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="16653-677">Added support for ACR integration with the following commands:</span></span>
  * <span data-ttu-id="16653-678">AKS クラスターに ACR をアタッチするための `--attach-acr` パラメーターを `aks [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-678">Added `--attach-acr` parameter to `aks [create|update]` to attach an ACR to an AKS cluster</span></span>
  * <span data-ttu-id="16653-679">AKS クラスターから ACR をデタッチするための `--detach-acr` パラメーターを `aks update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-679">Added `--detach-acr` parameter to `aks update` to detach the ACR from an AKS cluster</span></span>

### <a name="arm"></a><span data-ttu-id="16653-680">ARM</span><span class="sxs-lookup"><span data-stu-id="16653-680">ARM</span></span>

* <span data-ttu-id="16653-681">API バージョン 2019-05-10 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-681">Updated to use API version 2019-05-10</span></span>

### <a name="batch"></a><span data-ttu-id="16653-682">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-682">Batch</span></span>

* <span data-ttu-id="16653-683">`batch pool create` の `--json-file` に新しい JSON 構成設定を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-683">Added new JSON configuration settings to `--json-file` for `batch pool create`:</span></span>
  * <span data-ttu-id="16653-684">ファイル システム マウント用の `MountConfigurations` を追加しました (詳細については https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="16653-684">Added `MountConfigurations` for file system mounts (see https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body for details)</span></span>
  * <span data-ttu-id="16653-685">プール上のパブリック IP 用に、`NetworkConfiguration` にオプションのプロパティ `publicIPs` を追加しました (詳細については https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="16653-685">Added optional property `publicIPs` on `NetworkConfiguration` for public IPs on pools (see https://docs.microsoft.com/rest/api/batchservice/pool/add#request-body for details)</span></span>
* <span data-ttu-id="16653-686">共有イメージ ギャラリーのサポートを `--image` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-686">Added support for shared image galleries to `--image`</span></span>
* <span data-ttu-id="16653-687">[重大な変更]`batch pool create` の `--start-task-wait-for-success` の既定値を `true` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-687">[BREAKING CHANGE] Changed default value of `--start-task-wait-for-success` on `batch pool create` to be `true`</span></span>
* <span data-ttu-id="16653-688">[重大な変更]`AutoUserSpecification` の `Scope` の既定値が常に Pool になるように変更しました (以前は Windows ノードでは `Task`、Linux ノードでは `Pool` でした)</span><span class="sxs-lookup"><span data-stu-id="16653-688">[BREAKING CHANGE] Changed default value for `Scope` on `AutoUserSpecification` to always be Pool (was `Task` on Windows nodes, `Pool` on Linux nodes)</span></span>
  * <span data-ttu-id="16653-689">この引数は、`--json-file` を使用して JSON 構成からのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="16653-689">This argument can only be set from a JSON configuration with `--json-file`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="16653-690">HDInsight</span><span class="sxs-lookup"><span data-stu-id="16653-690">HDInsight</span></span>

* <span data-ttu-id="16653-691">GA リリース</span><span class="sxs-lookup"><span data-stu-id="16653-691">GA release</span></span>
* <span data-ttu-id="16653-692">[重大な変更]`az hdinsight resize` のパラメーター `--workernode-count/-c` が必須に変更されました。</span><span class="sxs-lookup"><span data-stu-id="16653-692">[BREAKING CHANGE] Changed parameter `--workernode-count/-c` of `az hdinsight resize` to be required.</span></span>

### <a name="key-vault"></a><span data-ttu-id="16653-693">Key Vault</span><span class="sxs-lookup"><span data-stu-id="16653-693">Key Vault</span></span>

* <span data-ttu-id="16653-694">ネットワーク ルールからサブネットを削除できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-694">Fixed issue where subnets couldn't be deleted from network rules</span></span>
* <span data-ttu-id="16653-695">重複したサブネットと IP アドレスをネットワーク ルールに追加できる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-695">Fixed issue where duplicated subnets and IP addresses could be added to network rules</span></span>

### <a name="network"></a><span data-ttu-id="16653-696">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-696">Network</span></span>

* <span data-ttu-id="16653-697">トラフィック分析間隔の値を設定する `--interval` パラメーターを `network watcher flow-log` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-697">Added `--interval` parameter to `network watcher flow-log` to set traffic analysis interval value</span></span>
* <span data-ttu-id="16653-698">ゲートウェイ ID を管理するための `network application-gateway identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-698">Added `network application-gateway identity` to manage gateway identity</span></span>
* <span data-ttu-id="16653-699">Key Vault ID を設定するためのサポートを `network application-gateway ssl-cert` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-699">Added support for setting Key Vault ID to `network application-gateway ssl-cert`</span></span>
* <span data-ttu-id="16653-700">`network express-route peering peer-connection [show|list]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-700">Added `network express-route peering peer-connection [show|list]`</span></span>

### <a name="policy"></a><span data-ttu-id="16653-701">ポリシー</span><span class="sxs-lookup"><span data-stu-id="16653-701">Policy</span></span>

* <span data-ttu-id="16653-702">API バージョン 2019-01-01 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-702">Updated to use API version 2019-01-01</span></span>

## <a name="august-27-2019"></a><span data-ttu-id="16653-703">2019 年 8 月 27 日</span><span class="sxs-lookup"><span data-stu-id="16653-703">August 27, 2019</span></span>

<span data-ttu-id="16653-704">バージョン 2.0.72</span><span class="sxs-lookup"><span data-stu-id="16653-704">Version 2.0.72</span></span>

### <a name="acr"></a><span data-ttu-id="16653-705">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-705">ACR</span></span>

* <span data-ttu-id="16653-706">[重大な変更]`classic` SKU のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-706">[BREAKING CHANGE] Removed support for the `classic` SKU</span></span>

### <a name="api-management"></a><span data-ttu-id="16653-707">API Management</span><span class="sxs-lookup"><span data-stu-id="16653-707">API Management</span></span>

* <span data-ttu-id="16653-708">[プレビュー] `apim` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-708">[PREVIEW] Added `apim` command group</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-709">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-709">AppService</span></span>

* <span data-ttu-id="16653-710">スロットを指定したときの `webapp webjob continuous start` コマンドに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-710">Fixed issue with `webapp webjob continuous start` command when specifying a slot</span></span>
* <span data-ttu-id="16653-711">`env` フォルダーを検出してデプロイに使用されているファイルから削除するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-711">Changed `webapp up` to detect `env` folder and remove it from the file used for deployment</span></span>

### <a name="keyvault"></a><span data-ttu-id="16653-712">KeyVault</span><span class="sxs-lookup"><span data-stu-id="16653-712">Keyvault</span></span>

* <span data-ttu-id="16653-713">`--expires` 引数を無視する `keyvault secret set` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-713">Fixed a bug in `keyvault secret set` that igored the `--expires` argument</span></span>

### <a name="network"></a><span data-ttu-id="16653-714">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-714">Network</span></span>

* <span data-ttu-id="16653-715">`--private-ip-address-version` 引数に IPv6 アドレスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-715">Added support for IPv6 addresses to `--private-ip-address-version` arguments</span></span>
* <span data-ttu-id="16653-716">プライベート エンドポイントの管理用に新しいコマンド `network private-endpoint [create|update|list-types]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-716">Added new commands `network private-endpoint [create|update|list-types]` for private endpoint management</span></span>
* <span data-ttu-id="16653-717">コマンド グループ `network private-link-service` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-717">Added command group `network private-link-service`</span></span>
* <span data-ttu-id="16653-718">`--private-endpoint-network-policies` 引数と `--private-link-service-network-policies` 引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-718">Added `--private-endpoint-network-policies` and `--private-link-service-network-policies` arguments to `network vnet subnet update`</span></span>

### <a name="rbac"></a><span data-ttu-id="16653-719">RBAC</span><span class="sxs-lookup"><span data-stu-id="16653-719">RBAC</span></span>

* <span data-ttu-id="16653-720">ホームページが更新されない `ad app update --homepage` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-720">Fixed issue with `ad app update --homepage` where homepage would not be updated</span></span>

### <a name="servicefabric"></a><span data-ttu-id="16653-721">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="16653-721">ServiceFabric</span></span>

* <span data-ttu-id="16653-722">キー コンテナーの大文字と小文字が混在する名前のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-722">Added support for mixed-case Key Vault names</span></span>
* <span data-ttu-id="16653-723">Key Vault で証明書を使用したときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-723">Fixed issue when using certificates in Key Vault</span></span>
* <span data-ttu-id="16653-724">PFX 証明書ファイルの使用に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-724">Fixed issue with using PFX certificate files</span></span>
* <span data-ttu-id="16653-725">Key Vault リソースグループが指定されていなかったときの `sf cluster certificate add` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-725">Fixed issue with `sf cluster certificate add` when Key Vault resource group wasn't specified</span></span>
* <span data-ttu-id="16653-726">`sf cluster set` が動作しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-726">Fixed issue with `sf cluster set` not working</span></span>

### <a name="signalr"></a><span data-ttu-id="16653-727">SignalR</span><span class="sxs-lookup"><span data-stu-id="16653-727">SignalR</span></span>

* <span data-ttu-id="16653-728">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-728">Added new commands:</span></span>
  * <span data-ttu-id="16653-729">`signalr cors`:SignalR CORS の管理</span><span class="sxs-lookup"><span data-stu-id="16653-729">`signalr cors`: Manage SignalR CORS</span></span>
  * <span data-ttu-id="16653-730">`signalr restart`:SignalR Service の再起動</span><span class="sxs-lookup"><span data-stu-id="16653-730">`signalr restart`: Restart a SignalR service</span></span>
  * <span data-ttu-id="16653-731">`signalr update`:SignalR Service の更新</span><span class="sxs-lookup"><span data-stu-id="16653-731">`signalr update`: Update a SignalR service</span></span>
* <span data-ttu-id="16653-732">`--service-mode` 引数を `signalr create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-732">Added `--service-mode` argument to `signalr create`</span></span>

### <a name="storage"></a><span data-ttu-id="16653-733">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-733">Storage</span></span>

* <span data-ttu-id="16653-734">`storage account revoke-delegation-keys` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-734">Added `storage account revoke-delegation-keys` command</span></span>

## <a name="august-13-2019"></a><span data-ttu-id="16653-735">2019 年 8 月 13 日</span><span class="sxs-lookup"><span data-stu-id="16653-735">August 13, 2019</span></span>

<span data-ttu-id="16653-736">バージョン 2.0.71</span><span class="sxs-lookup"><span data-stu-id="16653-736">Version 2.0.71</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-737">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-737">AppService</span></span>

* <span data-ttu-id="16653-738">`webapp webjob continuous` コマンドがスロットで失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-738">Fixed issue where `webapp webjob continuous` commands were failing for slots</span></span>

### <a name="botservice"></a><span data-ttu-id="16653-739">BotService</span><span class="sxs-lookup"><span data-stu-id="16653-739">BotService</span></span>

* <span data-ttu-id="16653-740">[重大な変更] v3 SDK ボットの作成のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-740">[BREAKING CHANGE] Removed support for creating v3 SDK bots</span></span>

### <a name="cognitiveservices"></a><span data-ttu-id="16653-741">CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="16653-741">CognitiveServices</span></span>

* <span data-ttu-id="16653-742">`cognitiveservices account network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-742">Added `cognitiveservices account network-rule` commands</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="16653-743">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-743">Cosmos DB</span></span>

* <span data-ttu-id="16653-744">複数の書き込み場所を更新するときの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-744">Removed warning when updating multiple write locations</span></span>
* <span data-ttu-id="16653-745">CosmosDB SQL、MongoDB、Cassandra、Gremlin、およびテーブル リソースとリソースのスループットのための CRUD コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-745">Added CRUD commands for CosmosDB SQL, MongoDB, Cassandra, Gremlin and Table resources and resource's throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="16653-746">HDInsight</span><span class="sxs-lookup"><span data-stu-id="16653-746">HDInsight</span></span>

<span data-ttu-id="16653-747">このリリースには、多数の破壊的変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="16653-747">This release contains a large number of breaking changes.</span></span>

* <span data-ttu-id="16653-748">[重大な変更]`hdinsight create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-748">[BREAKING CHANGE] Renamed parameters for `hdinsight create`:</span></span>
  * <span data-ttu-id="16653-749">`--storage-default-container` から `--storage-container` への名称変更</span><span class="sxs-lookup"><span data-stu-id="16653-749">Renamed `--storage-default-container` to `--storage-container`</span></span>
  * <span data-ttu-id="16653-750">`--storage-default-filesystem` から `--storage-filesystem` への名称変更</span><span class="sxs-lookup"><span data-stu-id="16653-750">Renamed `--storage-default-filesystem` to `--storage-filesystem`</span></span>
* <span data-ttu-id="16653-751">[重大な変更]`application create` の `--name` 引数が、クラスター名の代わりにアプリケーション名を表すように変更されました</span><span class="sxs-lookup"><span data-stu-id="16653-751">[BREAKING CHANGE] Changed the `--name` argument of `application create` to represent the application name instead of the cluster name</span></span>
* <span data-ttu-id="16653-752">`--cluster-name` 引数が `application create` に追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="16653-752">Added `--cluster-name` argument to `application create` to replace old `--name` functionality</span></span>
* <span data-ttu-id="16653-753">[重大な変更]`application create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-753">[BREAKING CHANGE] Renamed parameters for `application create`:</span></span>
  * <span data-ttu-id="16653-754">`--application-type` から `--type` への名称変更</span><span class="sxs-lookup"><span data-stu-id="16653-754">Renamed `--application-type` to `--type`</span></span>
  * <span data-ttu-id="16653-755">`--marketplace-identifier` から `--marketplace-id` への名称変更</span><span class="sxs-lookup"><span data-stu-id="16653-755">Renamed `--marketplace-identifier` to `--marketplace-id`</span></span>
  * <span data-ttu-id="16653-756">`--https-endpoint-access-mode` から `--access-mode` への名称変更</span><span class="sxs-lookup"><span data-stu-id="16653-756">Renamed `--https-endpoint-access-mode` to `--access-mode`</span></span>
  * <span data-ttu-id="16653-757">`--https-endpoint-destination-port` の名前を `--destination-port` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-757">Renamed  `--https-endpoint-destination-port` to `--destination-port`</span></span>
* <span data-ttu-id="16653-758">[重大な変更]`application create` のパラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="16653-758">[BREAKING CHANGE] Removed parameters for `application create`:</span></span>
  * `--https-endpoint-location`
  * `--https-endpoint-public-port`
  * `--ssh-endpoint-destination-port`
  * `--ssh-endpoint-location`
  * `--ssh-endpoint-public-port`
* <span data-ttu-id="16653-759">[破壊的変更] `hdinsight resize`の `--target-instance-count` の名前を `--workernode-count` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-759">[BREAKING CHNAGE] Renamed `--target-instance-count` to `--workernode-count` for `hdinsight resize`</span></span>
* <span data-ttu-id="16653-760">[重大な変更]`hdinsight script-action` グループのすべてのコマンドが、スクリプト アクションの名前として `--name` パラメーターを使用するように変更されました。</span><span class="sxs-lookup"><span data-stu-id="16653-760">[BREAKING CHANGE] Changed all commands in the `hdinsight script-action` group to use the `--name` parameter as the name of the script action.</span></span>
* <span data-ttu-id="16653-761">`--cluster-name` 引数がすべての `hdinsight script-action` コマンドに追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="16653-761">Added `--cluster-name` argument to all `hdinsight script-action` commands to replace old `--name` functionality</span></span>
* <span data-ttu-id="16653-762">[重大な変更] すべての `hdinsight script-action` コマンドで `--script-execution-id` の名前を `--execution-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-762">[BREAKING CHANGE] Renamed `--script-execution-id` to `--execution-id` for all `hdinsight script-action` commands</span></span>
* <span data-ttu-id="16653-763">[重大な変更] 名前を `hdinsight script-action show` から `hdinsight script-action show-execution-details` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-763">[BREAKING CHANGE] Renamed `hdinsight script-action show` to `hdinsight script-action show-execution-details`</span></span>
* <span data-ttu-id="16653-764">[破壊的変更] `hdinsight script-action execute --roles` に対するパラメーターを、コンマ区切りではなくスペース区切りにしました</span><span class="sxs-lookup"><span data-stu-id="16653-764">[BREAKING CHNAGE] Changed parameters to `hdinsight script-action execute --roles` to be space-separated instead of comma-separated</span></span>
* <span data-ttu-id="16653-765">[重大な変更]`hdinsight script-action list`の `--persisted` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-765">[BREAKING CHANGE] Removed the `--persisted` parameter of `hdinsight script-action list`</span></span>
* <span data-ttu-id="16653-766">ローカル JSON ファイルへのパスまたは JSON 文字列を受け入れるように `hdinsight create --cluster-configurations` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-766">Changed the `hdinsight create --cluster-configurations` parameter to accept a path to a local JSON file or a JSON string</span></span>
* <span data-ttu-id="16653-767">`hdinsight script-action list-execution-history` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-767">Added command `hdinsight script-action list-execution-history`</span></span>
* <span data-ttu-id="16653-768">Log Analytics ワークスペース ID またはワークスペース名を受け入れるように `hdinsight monitor enable --workspace` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-768">Changed `hdinsight monitor enable --workspace` to accept a Log Analytics workspace ID or workspace name</span></span>
* <span data-ttu-id="16653-769">`hdinsight monitor enable --primary-key` 引数を追加しました。これは、ワークスペース ID がパラメーターとして指定されている場合に必要です</span><span class="sxs-lookup"><span data-stu-id="16653-769">Added the `hdinsight monitor enable --primary-key` argument, which is needed if a workspace ID is provided as the parameter</span></span>
* <span data-ttu-id="16653-770">例をさらに追加し、ヘルプ メッセージの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-770">Added more examples and updated descriptions for help messages</span></span>

### <a name="interactive"></a><span data-ttu-id="16653-771">Interactive</span><span class="sxs-lookup"><span data-stu-id="16653-771">Interactive</span></span>

* <span data-ttu-id="16653-772">読み込みエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-772">Fixed a loading error</span></span>

### <a name="kubernetes"></a><span data-ttu-id="16653-773">Kubernetes</span><span class="sxs-lookup"><span data-stu-id="16653-773">Kubernetes</span></span>

* <span data-ttu-id="16653-774">ダッシュボードのコンテナー ポートで `https` が使用されている場合に `https` を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-774">Changed to use `https` if dashboard container port is using `https`</span></span>

### <a name="network"></a><span data-ttu-id="16653-775">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-775">Network</span></span>

* <span data-ttu-id="16653-776">`--yes` 引数を `network dns record-set cname delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-776">Added `--yes` argument `network dns record-set cname delete`</span></span>

### <a name="profile"></a><span data-ttu-id="16653-777">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-777">Profile</span></span>

* <span data-ttu-id="16653-778">リソースのアクセス トークンを取得するための `account get-access-token` に `--resource-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-778">Added `--resource-type` argument to `account get-access-token` to get resource access tokens</span></span>

### <a name="servicefabric"></a><span data-ttu-id="16653-779">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="16653-779">ServiceFabric</span></span>

* <span data-ttu-id="16653-780">sf cluster create でサポートされているすべての OS バージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-780">Added all supported os version for sf cluster create</span></span>
* <span data-ttu-id="16653-781">プライマリ証明書の検証のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-781">Fixed primary certificate validation bug</span></span>

### <a name="storage"></a><span data-ttu-id="16653-782">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-782">Storage</span></span>

* <span data-ttu-id="16653-783">`storage copy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-783">Added command `storage copy`</span></span>

## <a name="july-30-2019"></a><span data-ttu-id="16653-784">2019 年 7 月 30 日</span><span class="sxs-lookup"><span data-stu-id="16653-784">July 30, 2019</span></span>

<span data-ttu-id="16653-785">バージョン 2.0.70</span><span class="sxs-lookup"><span data-stu-id="16653-785">Version 2.0.70</span></span>

### <a name="acr"></a><span data-ttu-id="16653-786">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-786">ACR</span></span>

* <span data-ttu-id="16653-787">問題 #9952 (`acr pack build` コマンドでの回帰) を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-787">Fixed issue #9952 (a regression in the `acr pack build` command)</span></span>
* <span data-ttu-id="16653-788">`acr pack build` の既定のビルダー イメージ名を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-788">Removed the default builder image name in `acr pack build`</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-789">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-789">Appservice</span></span>

* <span data-ttu-id="16653-790">リソースが見つからない場合にメッセージ表示するように `webapp config ssl` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-790">Changed `webapp config ssl` to show a message if a resource is not found</span></span>
* <span data-ttu-id="16653-791">`functionapp create` がストレージ アカウントの種類 `Standard_RAGRS` を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-791">Fixed issue where `functionapp create` does not accept `Standard_RAGRS` storage account type</span></span>
* <span data-ttu-id="16653-792">古いバージョンの python を使用して `webapp up` を実行すると失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-792">Fixed an issue where `webapp up` would fail if run using older versions of python</span></span>

### <a name="network"></a><span data-ttu-id="16653-793">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-793">Network</span></span>

* <span data-ttu-id="16653-794">`network nic ip-config add` から無効なパラメーター `--ids` を削除しました (#9861 の修正)</span><span class="sxs-lookup"><span data-stu-id="16653-794">Removed invalid parameter `--ids` from `network nic ip-config add` (fixes #9861)</span></span>
* <span data-ttu-id="16653-795">#9604 を修正しました。</span><span class="sxs-lookup"><span data-stu-id="16653-795">Fixes #9604.</span></span> <span data-ttu-id="16653-796">信頼されたルート証明書へのユーザーの関連付けをサポートするために、`network application-gateway http-settings [create|update]` に `--root-certs` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-796">Added `--root-certs` parameter to `network application-gateway http-settings [create|update]` to support user associate trusted root certificates.</span></span>
* <span data-ttu-id="16653-797">`network dns record-set ns create` の引数 `--subscription` を修正しました (#9965)</span><span class="sxs-lookup"><span data-stu-id="16653-797">Fixed arguent `--subscription` for `network dns record-set ns create` (#9965)</span></span>

### <a name="rbac"></a><span data-ttu-id="16653-798">RBAC</span><span class="sxs-lookup"><span data-stu-id="16653-798">RBAC</span></span>

* <span data-ttu-id="16653-799">`user update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-799">Added `user update` command</span></span>
* <span data-ttu-id="16653-800">[非推奨] ユーザー関連コマンドで `--upn-or-object-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-800">[DEPRECATED] Deprecated `--upn-or-object-id` from user-related commands</span></span>
    * <span data-ttu-id="16653-801">代替引数の `--id` を使用してください</span><span class="sxs-lookup"><span data-stu-id="16653-801">Use replacement argument `--id`</span></span>
* <span data-ttu-id="16653-802">ユーザー関連コマンドに `--id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-802">Added `--id` argument to user-related commands</span></span>

### <a name="sql"></a><span data-ttu-id="16653-803">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-803">SQL</span></span>

* <span data-ttu-id="16653-804">マネージド インスタンス キーおよび TDE 保護機能の管理コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-804">Added management commands for managed instance keys and TDE protector</span></span>

### <a name="storage"></a><span data-ttu-id="16653-805">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-805">Storage</span></span>

* <span data-ttu-id="16653-806">`storage remove` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-806">Added `storage remove` command</span></span>
* <span data-ttu-id="16653-807">`storage blob update` での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-807">Fixed an issue with `storage blob update`</span></span>

### <a name="vm"></a><span data-ttu-id="16653-808">VM</span><span class="sxs-lookup"><span data-stu-id="16653-808">VM</span></span>

* <span data-ttu-id="16653-809">ゾーンの詳細を出力するための新しい API バージョンを使用するように `list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-809">Changed `list-skus` to use newer api-version to output zone details</span></span>
* <span data-ttu-id="16653-810">`vmss create` の `--single-placement-group` の既定値を`false` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-810">Changed default of `--single-placement-group` to `false` for `vmss create`</span></span>
* <span data-ttu-id="16653-811">`[snapshot|disk] create` において ZRS ストレージ SKU を選択する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-811">Added ability to select ZRS storage SKUs for `[snapshot|disk] create`</span></span>
* <span data-ttu-id="16653-812">専用ホストをサポートするために、新しいコマンド グループ `vm host` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-812">Added new command group `vm host` to support dedicated hosts</span></span>
* <span data-ttu-id="16653-813">VM 専用ホストを設定するためのパラメーター `--host` と `--host-group` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-813">Added parameters `--host` and `--host-group` on `vm create` to set VM dedicated host</span></span>

## <a name="july-16-2019"></a><span data-ttu-id="16653-814">2019 年 7 月 16 日</span><span class="sxs-lookup"><span data-stu-id="16653-814">July 16, 2019</span></span>

<span data-ttu-id="16653-815">バージョン 2.0.69</span><span class="sxs-lookup"><span data-stu-id="16653-815">Version 2.0.69</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-816">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-816">Appservice</span></span>

* <span data-ttu-id="16653-817">ResourceGroupName または App の名前が無効な場合に適切なエラー メッセージを返すように `webapp identity` コマンドが変更されました</span><span class="sxs-lookup"><span data-stu-id="16653-817">Changed `webapp identity` commands to return a proper error message if ResourceGroupName or App name are invalid</span></span>
* <span data-ttu-id="16653-818">ResourceGroup が指定されなかった場合に numberOfSites の正しい値を返すように `webapp list` が修正されました</span><span class="sxs-lookup"><span data-stu-id="16653-818">Fixed `webapp list` to return the correct value for numberOfSites if no ResourceGroup was provided</span></span>
* <span data-ttu-id="16653-819">`appservice plan create` と `webapp create` の副作用が修正されました</span><span class="sxs-lookup"><span data-stu-id="16653-819">Fixed side-effects of `appservice plan create` and `webapp create`</span></span>

### <a name="core"></a><span data-ttu-id="16653-820">コア</span><span class="sxs-lookup"><span data-stu-id="16653-820">Core</span></span>

* <span data-ttu-id="16653-821">`--subscription` が適用不可にもかかわらず表示される問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="16653-821">Fixed issue where `--subscription` would appear despite being not applicable</span></span>

### <a name="batch"></a><span data-ttu-id="16653-822">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-822">Batch</span></span>

* <span data-ttu-id="16653-823">[重大な変更]`batch pool node-agent-skus list` が `batch pool supported-images list` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="16653-823">[BREAKING CHANGE] Replaced `batch pool node-agent-skus list` with `batch pool supported-images list`</span></span>
* <span data-ttu-id="16653-824">`batch pool create network` の `--json-file` オプションを使用するときに、トラフィックのソース ポートに基づいてプールへのネットワーク アクセスをブロックするセキュリティ規則のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-824">Added support for security rules blocking network access to a pool based on the source port of the traffic when using the `--json-file` option of `batch pool create network`</span></span>
* <span data-ttu-id="16653-825">`batch task create`の `--json-file` オプションを使用するときに、コンテナーの作業ディレクトリまたは Batch タスクの作業ディレクトリでタスクを実行するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-825">Added support for executing the task in the container working directory or in the Batch task working directory when using the `--json-file` option of `batch task create`</span></span>
* <span data-ttu-id="16653-826">`batch pool create`の `--application-package-references` オプションが、既定値でのみ動作するというエラーが修正されました</span><span class="sxs-lookup"><span data-stu-id="16653-826">Fixed error in `--application-package-references` option of `batch pool create` where it would only work with defaults</span></span>

### <a name="eventhubs"></a><span data-ttu-id="16653-827">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="16653-827">Eventhubs</span></span>

* <span data-ttu-id="16653-828">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-828">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="rdbms"></a><span data-ttu-id="16653-829">RDBMS</span><span class="sxs-lookup"><span data-stu-id="16653-829">RDBMS</span></span>

* <span data-ttu-id="16653-830">レプリカ作成コマンドでレプリカ SKU を指定するためのオプション パラメーターが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-830">Added optional parameter to specify replica SKU for create replica command</span></span>
* <span data-ttu-id="16653-831">MySQL レプリカの作成で CI テストが失敗する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="16653-831">Fixed the issue with CI test failure with creating MySQL replica</span></span>

### <a name="relay"></a><span data-ttu-id="16653-832">リレー</span><span class="sxs-lookup"><span data-stu-id="16653-832">Relay</span></span>

* <span data-ttu-id="16653-833">クライアント承認が無効になっているときのハイブリッド接続の問題が修正されました ([#8775](https://github.com/azure/azure-cli/issues/8775))</span><span class="sxs-lookup"><span data-stu-id="16653-833">Fixed issue with hybrid connection when client authroization disabled [#8775](https://github.com/azure/azure-cli/issues/8775)</span></span>
* <span data-ttu-id="16653-834">パラメーター `--requires-transport-security` を `relay wcfrelay create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-834">Added parameter `--requires-transport-security` to `relay wcfrelay create`</span></span>

### <a name="servicebus"></a><span data-ttu-id="16653-835">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="16653-835">Servicebus</span></span>

* <span data-ttu-id="16653-836">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-836">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="storage"></a><span data-ttu-id="16653-837">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-837">Storage</span></span>

* <span data-ttu-id="16653-838">ストレージ アカウントの更新で Files AADDS を有効にします</span><span class="sxs-lookup"><span data-stu-id="16653-838">Enable Files AADDS for storage account update</span></span>
* <span data-ttu-id="16653-839">修正された問題 `storage blob service-properties update --set`</span><span class="sxs-lookup"><span data-stu-id="16653-839">Fixed issue `storage blob service-properties update --set`</span></span>

## <a name="july-2-2019"></a><span data-ttu-id="16653-840">2019 年 7 月 2 日</span><span class="sxs-lookup"><span data-stu-id="16653-840">July 2, 2019</span></span>

<span data-ttu-id="16653-841">バージョン 2.0.68</span><span class="sxs-lookup"><span data-stu-id="16653-841">Version 2.0.68</span></span>

### <a name="core"></a><span data-ttu-id="16653-842">コア</span><span class="sxs-lookup"><span data-stu-id="16653-842">Core</span></span>

* <span data-ttu-id="16653-843">コマンド モジュールが再頒布可能な 1 つの Python コードに統合されました。</span><span class="sxs-lookup"><span data-stu-id="16653-843">Command modules are now consolidated into a single Python distributable.</span></span> <span data-ttu-id="16653-844">これにより、PyPI での多くの `azure-cli-` パッケージの直接使用が廃止されます。</span><span class="sxs-lookup"><span data-stu-id="16653-844">This deprecates direct use of many `azure-cli-` packages on PyPI.</span></span>
  <span data-ttu-id="16653-845">またこれにより、インストール サイズが削減され、`pip` 経由で直接インストールしたユーザーにのみ影響が出ます。</span><span class="sxs-lookup"><span data-stu-id="16653-845">This should reduce install size and only affect users who have directly installed via `pip`.</span></span>

### <a name="acr"></a><span data-ttu-id="16653-846">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-846">ACR</span></span>

* <span data-ttu-id="16653-847">タスクへのタイマー トリガーのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-847">Added support for Timer Triggers to Task</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-848">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-848">Appservice</span></span>

* <span data-ttu-id="16653-849">既定でアプリケーション インサイトを有効にするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-849">Changed `functionapp create` to enable application insights by default</span></span>
* <span data-ttu-id="16653-850">[重大な変更] 非推奨の `functionapp devops-build` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="16653-850">[BREAKING CHANGE] Removed deprecated `functionapp devops-build` command.</span></span>
  *  <span data-ttu-id="16653-851">代わりに新しいコマンド `az functionapp devops-pipeline` を使用</span><span class="sxs-lookup"><span data-stu-id="16653-851">Use the new command `az functionapp devops-pipeline` instead</span></span>
* <span data-ttu-id="16653-852">Linux 従量課金プランの関数アプリのプラン サポートを `functionapp deployment config-zip` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-852">Added Linux Consumption function app plan support to `functionapp deployment config-zip`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="16653-853">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-853">Cosmos DB</span></span>

* <span data-ttu-id="16653-854">ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-854">Added support for disabling TTL</span></span>

### <a name="dls"></a><span data-ttu-id="16653-855">DLS</span><span class="sxs-lookup"><span data-stu-id="16653-855">DLS</span></span>

* <span data-ttu-id="16653-856">ADLS バージョンを更新しました (0.0.45)</span><span class="sxs-lookup"><span data-stu-id="16653-856">Updated ADLS version (0.0.45)</span></span>

### <a name="feedback"></a><span data-ttu-id="16653-857">フィードバック</span><span class="sxs-lookup"><span data-stu-id="16653-857">Feedback</span></span>

* <span data-ttu-id="16653-858">失敗した拡張機能コマンドを報告するときに、`az feedback` はインデックスからの拡張機能のプロジェクト/リポジトリの url にブラウザーを開こうとするようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-858">When reporting a failed extension command, `az feedback` now attempts to open the browser to the project/repo url of the extension from the index</span></span>

### <a name="hdinsight"></a><span data-ttu-id="16653-859">HDInsight</span><span class="sxs-lookup"><span data-stu-id="16653-859">HDInsight</span></span>

* <span data-ttu-id="16653-860">[重大な変更]`oms` コマンド グループ名を `monitor` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-860">[BREAKING CHANGE] Changed `oms` command group name to `monitor`</span></span>
* <span data-ttu-id="16653-861">[重大な変更]`--http-password/-p` が必須パラメーターになりました</span><span class="sxs-lookup"><span data-stu-id="16653-861">[BREAKING CHANGE] Made `--http-password/-p` a required parameter</span></span> 
* <span data-ttu-id="16653-862">`--cluster-admin-account` および `cluster-users-group-dns` パラメーター入力候補の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-862">Added completers for `--cluster-admin-account` and `cluster-users-group-dns` parameters completer</span></span> 
* <span data-ttu-id="16653-863">`cluster-users-group-dns` パラメーターを `—esp` が存在するときに必要となるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-863">Changed `cluster-users-group-dns` parameter to be required when `—esp` is present</span></span>
* <span data-ttu-id="16653-864">既存の引数自動オートコンプリートすべてにタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-864">Added a timeout for all existing argument auto-completers</span></span>
* <span data-ttu-id="16653-865">リソース名をリソース id に変換する際のタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-865">Added a timeout for transforming resource name to resource id</span></span>
* <span data-ttu-id="16653-866">任意のリソース グループからリソースを選択するようにオートコンプリートを変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-866">Changed Auto-completers to select resources from any resource group.</span></span> <span data-ttu-id="16653-867">`-g` で指定されるリソース グループとは別のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="16653-867">It can be a different resource group than the one specified with `-g`</span></span>
* <span data-ttu-id="16653-868">`hdinsight application create` コマンドで `--sub-domain-suffix` および `--disable_gateway_auth` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-868">Added support for `--sub-domain-suffix` and `--disable_gateway_auth` parameters in the `hdinsight application create` command</span></span>

### <a name="managed-services"></a><span data-ttu-id="16653-869">マネージド サービス</span><span class="sxs-lookup"><span data-stu-id="16653-869">Managed Services</span></span>

* <span data-ttu-id="16653-870">プレビューにマネージド サービス コマンド モジュールを導入</span><span class="sxs-lookup"><span data-stu-id="16653-870">Introducing managed service command module in preview</span></span>

### <a name="profile"></a><span data-ttu-id="16653-871">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-871">Profile</span></span>
* <span data-ttu-id="16653-872">ログアウト コマンドの `--subscription` 引数を抑制</span><span class="sxs-lookup"><span data-stu-id="16653-872">Suppress `--subscription` argument for logout command</span></span>

### <a name="rbac"></a><span data-ttu-id="16653-873">RBAC</span><span class="sxs-lookup"><span data-stu-id="16653-873">RBAC</span></span>

* <span data-ttu-id="16653-874">[重大な変更]`create-for-rbac` の `--password` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-874">[BREAKING CHANGE] Removed `--password` argument for `create-for-rbac`</span></span>
* <span data-ttu-id="16653-875">AAD グラフ サーバー レプリケーションの待機時間によって発生する断続的なエラーを回避するために `--assignee-principal-type` パラメーターを `create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-875">Added `--assignee-principal-type` parameter to `create` command to avoid intermittent failures caused by AAD graph server replication latency</span></span>
* <span data-ttu-id="16653-876">所有オブジェクトの一覧表示時の `ad signed-in-user` のクラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-876">Fixed a crash in `ad signed-in-user` when listing owned objects</span></span>
* <span data-ttu-id="16653-877">`ad sp` によってサービス プリンシパルから適切なアプリケーションが検出されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-877">Fixed issue where `ad sp` would not find the right application from a service principal</span></span>

### <a name="rdbms"></a><span data-ttu-id="16653-878">RDBMS</span><span class="sxs-lookup"><span data-stu-id="16653-878">RDBMS</span></span>

* <span data-ttu-id="16653-879">MariaDB のレプリケーション サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-879">Added support for replication for MariaDB</span></span>

### <a name="sql"></a><span data-ttu-id="16653-880">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-880">SQL</span></span>

* <span data-ttu-id="16653-881">`sql db create --sample-name` に使用できる値を文書化しました</span><span class="sxs-lookup"><span data-stu-id="16653-881">Documented allowed values for `sql db create --sample-name`</span></span>

### <a name="storage"></a><span data-ttu-id="16653-882">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-882">Storage</span></span>

* <span data-ttu-id="16653-883">`--as-user` を使用した `storage blob generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-883">Added user delegation SAS token support with `--as-user` to `storage blob generate-sas`</span></span> 
* <span data-ttu-id="16653-884">`--as-user` を使用した `storage container generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-884">Added user delegation SAS token support with `--as-user` to `storage container generate-sas`</span></span> 

### <a name="vm"></a><span data-ttu-id="16653-885">VM</span><span class="sxs-lookup"><span data-stu-id="16653-885">VM</span></span>

* <span data-ttu-id="16653-886">`--no-wait` による実行時に `vmss create` によってエラー メッセージが返されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-886">Fixed bug where `vmss create` returns an error message when run with `--no-wait`</span></span>
* <span data-ttu-id="16653-887">`vmss create --single-placement-group` のクライアント側の検証を削除しました。</span><span class="sxs-lookup"><span data-stu-id="16653-887">Removed client-side validation for `vmss create --single-placement-group`.</span></span> <span data-ttu-id="16653-888">`--single-placement-group` が `true` に設定され、`--instance-count` が 100 より大きいか、可用性ゾーンが指定されていても失敗にはならず、この検証はコンピューティング サービスに任されます</span><span class="sxs-lookup"><span data-stu-id="16653-888">Does not fail if `--single-placement-group` is set to `true` and`--instance-count` is greater than 100 or availability zones are specified, but leaves this validation to the compute service</span></span>
* <span data-ttu-id="16653-889">`--latest` と共に使用したときに `[vm|vmss] extension image list` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-889">Fixed bug where `[vm|vmss] extension image list` fails when used with `--latest`</span></span>


## <a name="june-18-2019"></a><span data-ttu-id="16653-890">2019 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="16653-890">June 18, 2019</span></span>

<span data-ttu-id="16653-891">バージョン 2.0.67</span><span class="sxs-lookup"><span data-stu-id="16653-891">Version 2.0.67</span></span>

### <a name="core"></a><span data-ttu-id="16653-892">コア</span><span class="sxs-lookup"><span data-stu-id="16653-892">Core</span></span>

<span data-ttu-id="16653-893">このリリースでは、新しい [プレビュー] タグが導入され、コマンド グループ、コマンド、または引数がプレビュー状態である場合に、お客様により明確に通知できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="16653-893">This release introduces a new [Preview] tag to more clearly communicate to customers when a command group, command or argument is in preview status.</span></span> <span data-ttu-id="16653-894">以前は、これはヘルプ テキストで通知されていたか、コマンド モジュールのバージョン番号によって暗黙的に通知されていました。</span><span class="sxs-lookup"><span data-stu-id="16653-894">This was previously called out in help text or communicated implicitly by the command module version number.</span></span>
<span data-ttu-id="16653-895">CLI では、将来、個々のパッケージのバージョン番号が削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="16653-895">The CLI will be removing version numbers for individual packages in the future.</span></span> <span data-ttu-id="16653-896">コマンドがプレビュー状態の場合は、そのすべての引数もプレビュー状態です。</span><span class="sxs-lookup"><span data-stu-id="16653-896">If a command is in preview, all of its arguments are as well.</span></span> <span data-ttu-id="16653-897">コマンド グループにプレビュー状態のラベルが付いている場合、すべてのコマンドと引数もプレビュー状態と見なされます。</span><span class="sxs-lookup"><span data-stu-id="16653-897">If a command group is labeled as being in preview, then all commands and arguments are considered to be in preview as well.</span></span>

<span data-ttu-id="16653-898">この変更の結果、このリリースでは、一部のコマンド グループが "突然" プレビュー状態になったように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="16653-898">As a result of this change, several command groups may seem to "suddenly" appear to be in a preview status with this release.</span></span> <span data-ttu-id="16653-899">ほとんどのパッケージがプレビュー状態にあったのですが、このリリースでは一般提供と見なされていることがその真相です</span><span class="sxs-lookup"><span data-stu-id="16653-899">What actually happened is that most packages were in a preview status, but are being deemed GA with this release</span></span>

### <a name="acr"></a><span data-ttu-id="16653-900">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-900">ACR</span></span>
* <span data-ttu-id="16653-901">'acr check-health' コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-901">Added 'acr check-health' command</span></span>
* <span data-ttu-id="16653-902">AAD トークンおよび外部コマンドの取得に関するエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-902">Improved error handling for AAD tokens and for retrieving external commands</span></span>

### <a name="acs"></a><span data-ttu-id="16653-903">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-903">ACS</span></span>
* <span data-ttu-id="16653-904">非推奨の ACS コマンドがヘルプ ビューで非表示になりました</span><span class="sxs-lookup"><span data-stu-id="16653-904">Deprecated ACS commands are now hidden from help view</span></span>

### <a name="ams"></a><span data-ttu-id="16653-905">AMS</span><span class="sxs-lookup"><span data-stu-id="16653-905">AMS</span></span>
* <span data-ttu-id="16653-906">[重大な変更] archive-window-length および key-frame-interval-duration の ISO 8601 時間文字列を返すように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-906">[BREAKING CHANGE] Changed to return ISO 8601 time strings for archive-window-length and key-frame-interval-duration</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-907">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-907">AppService</span></span>
* <span data-ttu-id="16653-908">`webapp deleted list` および `webapp deleted restore` に対してロケーション ベースのルーティングを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-908">Added location based routing for `webapp deleted list` and `webapp deleted restore`</span></span>
* <span data-ttu-id="16653-909">Azure Cloud Shell で Web アプリのログに記録されたターゲット URL ("You can launch the app at...") がクリックできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-909">Fixed issue where webapp up logged target URL ("You can launch the app at...") was not clickable in Azure Cloud Shell</span></span>
* <span data-ttu-id="16653-910">一部の SKU でのアプリ作成が AlwaysOn エラーで失敗するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-910">Fixed an issue where creating apps with the some SKUs was failing with an AlwaysOn error</span></span>
* <span data-ttu-id="16653-911">`[appservice|webapp] create` に事前検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-911">Added pre-validation to `[appservice|webapp] create`</span></span>
* <span data-ttu-id="16653-912">正しい actionHostName を使用するように `[webapp|functionapp] traffic-routing` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-912">Fixed `[webapp|functionapp] traffic-routing` to use the correct actionHostName</span></span>
* <span data-ttu-id="16653-913">`functionapp` コマンドにスロット サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-913">Added slot support to `functionapp` commands</span></span>

### <a name="batch"></a><span data-ttu-id="16653-914">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-914">Batch</span></span>
* <span data-ttu-id="16653-915">共有キー認証の過度のエラー報告による AAD 認証の回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-915">Fixed AAD auth regression caused by over-aggressive error reporting for Shared Key Auth</span></span>

### <a name="batchai"></a><span data-ttu-id="16653-916">BatchAI</span><span class="sxs-lookup"><span data-stu-id="16653-916">BatchAI</span></span>
* <span data-ttu-id="16653-917">BatchAI コマンドが非推奨となり、非表示になりました</span><span class="sxs-lookup"><span data-stu-id="16653-917">BatchAI commands are now deprecated and hidden</span></span>

### <a name="botservice"></a><span data-ttu-id="16653-918">BotService</span><span class="sxs-lookup"><span data-stu-id="16653-918">BotService</span></span>
* <span data-ttu-id="16653-919">v3 SDK をサポートするコマンドに "廃止されたサポート"/"保守モード" 警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-919">Added "discontinued support"/"maintenance mode" warning messages for commands that support the v3 SDK</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="16653-920">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-920">CosmosDB</span></span>
* <span data-ttu-id="16653-921">[非推奨]`cosmosdb list-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-921">[DEPRECATED] Deprecated the `cosmosdb list-keys` command</span></span>
* <span data-ttu-id="16653-922">`cosmosdb keys list` コマンドを追加しました。`cosmosdb list-keys` に置き換わるものです</span><span class="sxs-lookup"><span data-stu-id="16653-922">Added the `cosmosdb keys list` command - replaces `cosmosdb list-keys`</span></span>
* <span data-ttu-id="16653-923">`cosmsodb create/update`:"isZoneRedundant" プロパティを設定できるように --location の新しいフォーマットを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-923">`cosmsodb create/update`: Added new format for --location to allow setting "isZoneRedundant" property.</span></span> <span data-ttu-id="16653-924">古いフォーマットを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-924">Deprecated old format</span></span>

### <a name="eventgrid"></a><span data-ttu-id="16653-925">EventGrid</span><span class="sxs-lookup"><span data-stu-id="16653-925">EventGrid</span></span>
* <span data-ttu-id="16653-926">ドメイン CRUD 操作のための `eventgrid domain` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-926">Added `eventgrid domain` commands for domain CRUD operations</span></span>
* <span data-ttu-id="16653-927">ドメイン トピック CRUD 操作のための `eventgrid domain topic` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-927">Added `eventgrid domain topic` commands for domain topics CRUD operations</span></span>
* <span data-ttu-id="16653-928">OData 構文を使用して結果をフィルタリングするための `--odata-query` 引数を `eventgrid [topic|event-subscription] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-928">Added `--odata-query` argument to `eventgrid [topic|event-subscription] list` for filtering results using OData syntax</span></span>
* <span data-ttu-id="16653-929">`event-subscription create/update`:`--endpoint-type` パラメーターの新しい値として servicebusqueue を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-929">`event-subscription create/update`: Added servicebusqueue as new values for the `--endpoint-type` parameter</span></span>
* <span data-ttu-id="16653-930">[重大な変更]`eventgrid event-subscription [create|update]` での `--included-event-types All` のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-930">[BREAKING CHANGE] Removed support for `--included-event-types All` with `eventgrid event-subscription [create|update]`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="16653-931">HDInsight</span><span class="sxs-lookup"><span data-stu-id="16653-931">HDInsight</span></span>
* <span data-ttu-id="16653-932">`hdinsight create` コマンドでの `--ssh-public-key` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-932">Added support for `--ssh-public-key` parameter in `hdinsight create` command</span></span>

### <a name="iot"></a><span data-ttu-id="16653-933">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-933">IoT</span></span>
* <span data-ttu-id="16653-934">承認ポリシー キーの再生成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-934">Added support to regenerate authorization policy keys</span></span>
* <span data-ttu-id="16653-935">DigitalTwin リポジトリ プロビジョニング サービスの SDK およびサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-935">Added SDK and support for DigitalTwin Repository Provisioning Service</span></span>

### <a name="network"></a><span data-ttu-id="16653-936">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-936">Network</span></span>
* <span data-ttu-id="16653-937">Nat Gateway に対するゾーン サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-937">Added Zone support for Nat Gateway</span></span>
* <span data-ttu-id="16653-938">`network list-service-tags` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-938">Added command `network list-service-tags`</span></span>
* <span data-ttu-id="16653-939">ユーザーがワイルドカード A レコードをインポートできない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-939">Fixed issue with `dns zone import` where users could not import wildcard A records</span></span>
* <span data-ttu-id="16653-940">特定のリージョンでフロー ロギングを有効にできない `watcher flow-log configure` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-940">Fixed issue with `watcher flow-log configure` where flow logging could not be enabled in certain regions</span></span>

### <a name="resource"></a><span data-ttu-id="16653-941">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-941">Resource</span></span>
* <span data-ttu-id="16653-942">REST 呼び出しを行うための `az rest` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-942">Added `az rest` command for making REST calls</span></span>
* <span data-ttu-id="16653-943">リソース グループまたはサブスクリプション レベル`--scope` で `policy assignment list` を使用する場合のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-943">Fixed error when using `policy assignment list` with a resource group or subscription level `--scope`</span></span>

### <a name="servicebus"></a><span data-ttu-id="16653-944">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="16653-944">ServiceBus</span></span>
* <span data-ttu-id="16653-945">`servicebus topic create --max-size` での問題 [#9319](https://github.com/azure/azure-cli/issues/9319) を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-945">Fixed issue with `servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319)</span></span>

### <a name="sql"></a><span data-ttu-id="16653-946">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-946">SQL</span></span>
* <span data-ttu-id="16653-947">`--location` を `sql [server|mi] create` のオプションに変更しました - 指定されていない場合、リソース グループの場所を使用します</span><span class="sxs-lookup"><span data-stu-id="16653-947">Changed `--location` to be optional for `sql [server|mi] create` - uses resource group location if not specified</span></span>
* <span data-ttu-id="16653-948">`sql db list-editions --available` の "'NoneType' object is not iterable" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-948">Fixed "'NoneType' object is not iterable" error for `sql db list-editions --available`</span></span>

### <a name="sqlvm"></a><span data-ttu-id="16653-949">SQLVm</span><span class="sxs-lookup"><span data-stu-id="16653-949">SQLVm</span></span>
* <span data-ttu-id="16653-950">[破壊的変更] `--license-type` パラメーターを必要とするように `sql vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-950">[BREAKING CHNAGE] Changed `sql vm create` to require `--license-type` parameter</span></span>
* <span data-ttu-id="16653-951">sql vm の作成または更新時に SQL イメージ SKU を設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-951">Changed to allow setting SQL image SKU when creating or updating a sql vm</span></span>

### <a name="storage"></a><span data-ttu-id="16653-952">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-952">Storage</span></span>
* <span data-ttu-id="16653-953">`storage container generate-sas` のアカウント キーが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-953">Fixed issue with missing account key for `storage container generate-sas`</span></span>
* <span data-ttu-id="16653-954">Linux での `storage blob sync` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-954">Fixed issue with `storage blob sync` on Linux</span></span>

### <a name="vm"></a><span data-ttu-id="16653-955">VM</span><span class="sxs-lookup"><span data-stu-id="16653-955">VM</span></span>
* <span data-ttu-id="16653-956">[プレビュー] VM イメージを構築するための `vm image template` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-956">[PREVIEW] Added `vm image template` commands to build VM images</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="16653-957">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="16653-957">June 4, 2019</span></span>

<span data-ttu-id="16653-958">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="16653-958">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="16653-959">コア</span><span class="sxs-lookup"><span data-stu-id="16653-959">Core</span></span>
* <span data-ttu-id="16653-960">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-960">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="16653-961">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-961">ACR</span></span>
* <span data-ttu-id="16653-962">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-962">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="16653-963">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-963">ACS</span></span>
* <span data-ttu-id="16653-964">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-964">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="16653-965">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="16653-965">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="16653-966">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-966">Batch</span></span>
* <span data-ttu-id="16653-967">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-967">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="16653-968">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-968">IoT</span></span>
* <span data-ttu-id="16653-969">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-969">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="16653-970">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-970">Network</span></span>
* <span data-ttu-id="16653-971">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-971">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="16653-972">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-972">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="16653-973">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-973">Resource</span></span>
* <span data-ttu-id="16653-974">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-974">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="16653-975">Role</span><span class="sxs-lookup"><span data-stu-id="16653-975">Role</span></span>
* <span data-ttu-id="16653-976">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="16653-976">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="16653-977">Compute</span><span class="sxs-lookup"><span data-stu-id="16653-977">Compute</span></span>
* <span data-ttu-id="16653-978">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-978">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="16653-979">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="16653-979">May 21, 2019</span></span>

<span data-ttu-id="16653-980">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="16653-980">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="16653-981">コア</span><span class="sxs-lookup"><span data-stu-id="16653-981">Core</span></span>
* <span data-ttu-id="16653-982">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-982">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="16653-983">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-983">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="16653-984">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-984">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="16653-985">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-985">ACR</span></span>
* <span data-ttu-id="16653-986">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-986">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="16653-987">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-987">ACS</span></span>
* <span data-ttu-id="16653-988">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-988">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-989">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-989">AppService</span></span>
* <span data-ttu-id="16653-990">[非推奨]`functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="16653-990">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="16653-991">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-991">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="16653-992">[重大な変更]`--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="16653-992">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="16653-993">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-993">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="16653-994">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-994">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="16653-995">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-995">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="16653-996">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-996">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="16653-997">BotService</span><span class="sxs-lookup"><span data-stu-id="16653-997">BotService</span></span>
* <span data-ttu-id="16653-998">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-998">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="16653-999">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-999">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="16653-1000">従量課金</span><span class="sxs-lookup"><span data-stu-id="16653-1000">Consumption</span></span>
* <span data-ttu-id="16653-1001">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1001">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="16653-1002">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-1002">IoT</span></span>
* <span data-ttu-id="16653-1003">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1003">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="16653-1004">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1004">Network</span></span>
* [重大な変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="16653-1006">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1006">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="16653-1007">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1007">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="16653-1008">RDBMS</span><span class="sxs-lookup"><span data-stu-id="16653-1008">RDBMS</span></span>
* <span data-ttu-id="16653-1009">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1009">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="16653-1010">RBAC</span><span class="sxs-lookup"><span data-stu-id="16653-1010">RBAC</span></span>
* <span data-ttu-id="16653-1011">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1011">Added support for management group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="16653-1012">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-1012">Storage</span></span>
* <span data-ttu-id="16653-1013">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="16653-1013">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="16653-1014">Compute</span><span class="sxs-lookup"><span data-stu-id="16653-1014">Compute</span></span>
* <span data-ttu-id="16653-1015">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1015">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="16653-1016">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-1016">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="16653-1017">__注__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="16653-1017">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="16653-1018">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1018">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="16653-1019">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="16653-1019">May 6, 2019</span></span>

<span data-ttu-id="16653-1020">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="16653-1020">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1021">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1021">ACS</span></span>
* <span data-ttu-id="16653-1022">[重大な変更]`--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1022">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="16653-1023">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1023">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="16653-1024">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1024">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="16653-1025">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1025">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1026">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-1026">Appservice</span></span>
* <span data-ttu-id="16653-1027">[非推奨]`functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1027">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="16653-1028">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1028">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="16653-1029">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="16653-1029">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="16653-1030">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-1030">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="16653-1031">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1031">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="16653-1032">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1032">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="16653-1033">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1033">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="16653-1034">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1034">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="16653-1035">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1035">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="16653-1036">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1036">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="16653-1037">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-1037">Batch</span></span>
* <span data-ttu-id="16653-1038">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1038">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="16653-1039">Botservice</span><span class="sxs-lookup"><span data-stu-id="16653-1039">Botservice</span></span>
* <span data-ttu-id="16653-1040">[重大な変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="16653-1040">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="16653-1041">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1041">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="16653-1042">[重大な変更]`--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1042">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="16653-1043">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="16653-1043">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="16653-1044">[重大な変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-1044">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="16653-1045">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="16653-1045">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="16653-1046">[重大な変更]`bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1046">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="16653-1047">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1047">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="16653-1048">[重大な変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1048">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="16653-1049">[重大な変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1049">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="16653-1050">[重大な変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1050">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="16653-1051">[重大な変更]`Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1051">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="16653-1052">[重大な変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1052">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="16653-1053">[重大な変更]`SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-1053">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="16653-1054">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="16653-1054">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="16653-1055">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1055">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="16653-1056">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1056">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="16653-1057">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1057">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="16653-1058">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1058">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="16653-1059">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1059">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="16653-1060">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1060">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="16653-1061">構成</span><span class="sxs-lookup"><span data-stu-id="16653-1061">Configure</span></span>
* <span data-ttu-id="16653-1062">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1062">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="16653-1063">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="16653-1063">Eventhubs</span></span>
* <span data-ttu-id="16653-1064">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1064">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="16653-1065">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1065">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="16653-1066">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1066">Network</span></span>
* <span data-ttu-id="16653-1067">[重大な変更]`vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="16653-1067">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="16653-1068">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="16653-1068">Policy Insights</span></span>
* <span data-ttu-id="16653-1069">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1069">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="16653-1070">Role</span><span class="sxs-lookup"><span data-stu-id="16653-1070">Role</span></span>
* <span data-ttu-id="16653-1071">[非推奨]`create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="16653-1071">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="16653-1072">Service Bus</span><span class="sxs-lookup"><span data-stu-id="16653-1072">Service Bus</span></span>
* <span data-ttu-id="16653-1073">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1073">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="16653-1074">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1074">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="16653-1075">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1075">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="16653-1076">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-1076">SQL</span></span>
* <span data-ttu-id="16653-1077">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1077">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1078">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1078">VM</span></span>
* <span data-ttu-id="16653-1079">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1079">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="16653-1080">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1080">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="16653-1081">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1081">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="16653-1082">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1082">Added new `ppg` command group for managing Proximity Placement Groups</span></span>
* <span data-ttu-id="16653-1083">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1083">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="16653-1084">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1084">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="16653-1085">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="16653-1085">April 23, 2019</span></span>

<span data-ttu-id="16653-1086">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="16653-1086">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1087">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1087">ACS</span></span>
* <span data-ttu-id="16653-1088">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1088">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="16653-1089">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1089">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="16653-1090">AMS</span><span class="sxs-lookup"><span data-stu-id="16653-1090">AMS</span></span>
* <span data-ttu-id="16653-1091">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1091">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1092">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-1092">AppService</span></span>
* <span data-ttu-id="16653-1093">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1093">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="16653-1094">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1094">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="16653-1095">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1095">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="16653-1096">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1096">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="16653-1097">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1097">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="16653-1098">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1098">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="16653-1099">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1099">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="16653-1100">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1100">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="16653-1101">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1101">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="16653-1102">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="16653-1102">Deployment Manager</span></span>
* <span data-ttu-id="16653-1103">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="16653-1103">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="16653-1104">ラボ</span><span class="sxs-lookup"><span data-stu-id="16653-1104">Lab</span></span>
* <span data-ttu-id="16653-1105">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1105">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="16653-1106">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1106">Network</span></span>
* <span data-ttu-id="16653-1107">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1107">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="16653-1108">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-1108">Resource</span></span>
* <span data-ttu-id="16653-1109">[非推奨]`resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="16653-1109">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="16653-1110">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="16653-1110">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="16653-1111">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1111">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="16653-1112">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1112">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="16653-1113">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-1113">SQL</span></span>
* <span data-ttu-id="16653-1114">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1114">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="16653-1115">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1115">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="16653-1116">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1116">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="16653-1117">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1117">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="16653-1118">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-1118">Storage</span></span>
* <span data-ttu-id="16653-1119">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1119">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1120">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1120">VM</span></span>
* <span data-ttu-id="16653-1121">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1121">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="16653-1122">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1122">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="16653-1123">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1123">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="16653-1124">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="16653-1124">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="16653-1125">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1125">Core</span></span>
* <span data-ttu-id="16653-1126">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1126">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1127">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1127">ACR</span></span>
* <span data-ttu-id="16653-1128">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-1128">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="16653-1129">AMS</span><span class="sxs-lookup"><span data-stu-id="16653-1129">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="16653-1132">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1132">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="16653-1133">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1133">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1134">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-1134">AppService</span></span>
* <span data-ttu-id="16653-1135">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1135">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="16653-1136">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1136">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="16653-1137">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-1137">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="16653-1138">[重大な変更]`devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="16653-1138">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="16653-1139">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1139">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="16653-1140">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1140">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="16653-1141">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1141">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="16653-1142">CDN</span><span class="sxs-lookup"><span data-stu-id="16653-1142">CDN</span></span>
* <span data-ttu-id="16653-1143">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1143">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="16653-1144">フィードバック</span><span class="sxs-lookup"><span data-stu-id="16653-1144">Feedback</span></span>
* <span data-ttu-id="16653-1145">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1145">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="16653-1146">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1146">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="16653-1147">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1147">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-1148">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-1148">Monitor</span></span>
* <span data-ttu-id="16653-1149">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1149">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="16653-1150">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1150">Network</span></span>
* <span data-ttu-id="16653-1151">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1151">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="16653-1152">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1152">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="16653-1153">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1153">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="16653-1154">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1154">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="16653-1155">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="16653-1155">PrivateDNS</span></span>
* <span data-ttu-id="16653-1156">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1156">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="16653-1157">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-1157">Resource</span></span>
* <span data-ttu-id="16653-1158">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1158">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="16653-1159">Role</span><span class="sxs-lookup"><span data-stu-id="16653-1159">Role</span></span>
* <span data-ttu-id="16653-1160">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1160">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="16653-1161">[重大な変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1161">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="16653-1162">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-1162">SQL</span></span>
* <span data-ttu-id="16653-1163">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-1163">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="16653-1164">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-1164">Storage</span></span>
* <span data-ttu-id="16653-1165">[重大な変更]`storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1165">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="16653-1166">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1166">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="16653-1167">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1167">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="16653-1168">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1168">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="16653-1169">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="16653-1169">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="16653-1170">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1170">Core</span></span>
* <span data-ttu-id="16653-1171">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1171">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="16653-1172">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-1172">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="16653-1173">クラウド</span><span class="sxs-lookup"><span data-stu-id="16653-1173">Cloud</span></span>
* <span data-ttu-id="16653-1174">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1174">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1175">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1175">ACR</span></span>
* <span data-ttu-id="16653-1176">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1176">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="16653-1177">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1177">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="16653-1178">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1178">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="16653-1179">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1179">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1180">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-1180">AppService</span></span>
* <span data-ttu-id="16653-1181">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1181">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="16653-1182">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1182">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="16653-1183">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="16653-1183">BOT Service</span></span>
* <span data-ttu-id="16653-1184">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1184">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="16653-1185">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1185">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="16653-1186">[重大な変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1186">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="16653-1187">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1187">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="16653-1188">CDN</span><span class="sxs-lookup"><span data-stu-id="16653-1188">CDN</span></span>
* <span data-ttu-id="16653-1189">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1189">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [重大な変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="16653-1191">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="16653-1191">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="16653-1192">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-1192">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="16653-1193">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="16653-1193">Cosmosdb</span></span>
* <span data-ttu-id="16653-1194">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1194">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="16653-1195">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1195">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="16653-1196">Interactive</span><span class="sxs-lookup"><span data-stu-id="16653-1196">Interactive</span></span>
* <span data-ttu-id="16653-1197">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1197">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-1198">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-1198">Monitor</span></span>
* <span data-ttu-id="16653-1199">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1199">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="16653-1200">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1200">Network</span></span>
* <span data-ttu-id="16653-1201">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1201">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="16653-1202">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-1202">Profile</span></span>
* <span data-ttu-id="16653-1203">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1203">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="16653-1204">Postgres</span><span class="sxs-lookup"><span data-stu-id="16653-1204">Postgres</span></span> 
* <span data-ttu-id="16653-1205">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1205">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="16653-1206">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="16653-1206">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="16653-1207">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-1207">Resource</span></span>
* <span data-ttu-id="16653-1208">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="16653-1208">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="16653-1209">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1209">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="16653-1210">グラフ</span><span class="sxs-lookup"><span data-stu-id="16653-1210">Graph</span></span>
* <span data-ttu-id="16653-1211">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1211">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="16653-1212">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1212">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="16653-1213">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1213">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="16653-1214">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1214">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="16653-1215">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1215">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="16653-1216">storage</span><span class="sxs-lookup"><span data-stu-id="16653-1216">storage</span></span>
* <span data-ttu-id="16653-1217">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1217">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="16653-1218">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1218">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="16653-1219">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1219">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="16653-1220">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1220">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1221">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1221">VM</span></span>
* <span data-ttu-id="16653-1222">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1222">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="16653-1223">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="16653-1223">March 12, 2019</span></span>

<span data-ttu-id="16653-1224">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="16653-1224">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="16653-1225">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1225">Core</span></span>

* <span data-ttu-id="16653-1226">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1226">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1227">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1227">ACR</span></span>

* <span data-ttu-id="16653-1228">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1228">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1229">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1229">ACS</span></span>

* <span data-ttu-id="16653-1230">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1230">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="16653-1231">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-1231">AppService</span></span>

* <span data-ttu-id="16653-1232">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1232">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="16653-1233">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1233">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="16653-1234">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1234">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="16653-1235">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-1235">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="16653-1236">Botservice</span><span class="sxs-lookup"><span data-stu-id="16653-1236">Botservice</span></span>

* <span data-ttu-id="16653-1237">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1237">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="16653-1238">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1238">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="16653-1239">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1239">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="16653-1240">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1240">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="16653-1241">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-1241">Container</span></span>

* <span data-ttu-id="16653-1242">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1242">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="16653-1243">EventHub</span><span class="sxs-lookup"><span data-stu-id="16653-1243">EventHub</span></span>

* <span data-ttu-id="16653-1244">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1244">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="16653-1245">Find</span><span class="sxs-lookup"><span data-stu-id="16653-1245">Find</span></span>

* <span data-ttu-id="16653-1246">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="16653-1246">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="16653-1247">HDInsight</span><span class="sxs-lookup"><span data-stu-id="16653-1247">HDInsight</span></span>

* <span data-ttu-id="16653-1248">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1248">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="16653-1249">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1249">Network</span></span>

* <span data-ttu-id="16653-1250">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1250">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="16653-1251">Rdbms</span><span class="sxs-lookup"><span data-stu-id="16653-1251">Rdbms</span></span>

* <span data-ttu-id="16653-1252">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="16653-1252">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="16653-1253">Role</span><span class="sxs-lookup"><span data-stu-id="16653-1253">Role</span></span>

* <span data-ttu-id="16653-1254">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1254">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="16653-1255">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1255">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="16653-1256">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="16653-1256">Service Fabric</span></span>

* <span data-ttu-id="16653-1257">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1257">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="16653-1258">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="16653-1258">February 26, 2019</span></span>

<span data-ttu-id="16653-1259">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="16653-1259">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="16653-1260">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1260">Core</span></span>

* <span data-ttu-id="16653-1261">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1261">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1262">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1262">ACR</span></span>

* <span data-ttu-id="16653-1263">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1263">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="16653-1264">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-1264">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1265">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1265">ACS</span></span>

* <span data-ttu-id="16653-1266">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1266">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1267">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-1267">AppService</span></span>

* <span data-ttu-id="16653-1268">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1268">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="16653-1269">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-1269">Batch</span></span>
* <span data-ttu-id="16653-1270">[重大な変更]`batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1270">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="16653-1271">[重大な変更]`Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1271">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="16653-1272">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1272">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="16653-1273">[重大な変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1273">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="16653-1274">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1274">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="16653-1275">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="16653-1275">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="16653-1276">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-1276">CosmosDB</span></span>

* <span data-ttu-id="16653-1277">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1277">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="16653-1278">Kusto</span><span class="sxs-lookup"><span data-stu-id="16653-1278">Kusto</span></span>

* <span data-ttu-id="16653-1279">[重大な変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1279">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="16653-1280">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1280">Network</span></span>

* <span data-ttu-id="16653-1281">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1281">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="16653-1282">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1282">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="16653-1283">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1283">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="16653-1284">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1284">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="16653-1285">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1285">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="16653-1286">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1286">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="16653-1287">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1287">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="16653-1288">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-1288">Resource</span></span>

* <span data-ttu-id="16653-1289">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1289">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="16653-1290">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1290">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="16653-1291">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1291">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="16653-1292">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1292">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="16653-1293">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1293">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="16653-1294">Role</span><span class="sxs-lookup"><span data-stu-id="16653-1294">Role</span></span>

* <span data-ttu-id="16653-1295">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1295">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1296">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1296">VM</span></span>

* <span data-ttu-id="16653-1297">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1297">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="16653-1298">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="16653-1298">February 12, 2019</span></span>

<span data-ttu-id="16653-1299">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="16653-1299">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="16653-1300">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1300">Core</span></span>

* <span data-ttu-id="16653-1301">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-1301">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="16653-1302">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1302">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1303">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1303">ACR</span></span>
* <span data-ttu-id="16653-1304">[重大な変更]`acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1304">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="16653-1305">[重大な変更]`acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1305">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1306">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1306">ACS</span></span>
* <span data-ttu-id="16653-1307">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1307">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="16653-1308">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1308">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="16653-1309">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1309">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="16653-1310">AMS</span><span class="sxs-lookup"><span data-stu-id="16653-1310">AMS</span></span>
* <span data-ttu-id="16653-1311">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1311">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="16653-1312">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1312">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1313">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-1313">Appservice</span></span>
* <span data-ttu-id="16653-1314">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1314">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="16653-1315">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-1315">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="16653-1316">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="16653-1316">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="16653-1317">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1317">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="16653-1318">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1318">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="16653-1319">Botservice</span><span class="sxs-lookup"><span data-stu-id="16653-1319">Botservice</span></span>
* <span data-ttu-id="16653-1320">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="16653-1320">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="16653-1321">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1321">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="16653-1322">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1322">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="16653-1323">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1323">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="16653-1324">[非推奨]`--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1324">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="16653-1325">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1325">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="16653-1326">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1326">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="16653-1327">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1327">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="16653-1328">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="16653-1328">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="16653-1329">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-1329">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="16653-1330">Key Vault</span><span class="sxs-lookup"><span data-stu-id="16653-1330">Key Vault</span></span>
* <span data-ttu-id="16653-1331">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1331">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-1332">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-1332">Monitor</span></span>
* <span data-ttu-id="16653-1333">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1333">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="16653-1334">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1334">Network</span></span>
* <span data-ttu-id="16653-1335">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1335">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="16653-1336">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1336">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="16653-1337">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1337">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="16653-1338">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1338">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="16653-1339">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="16653-1339">Policy Insights</span></span>
* <span data-ttu-id="16653-1340">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1340">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="16653-1341">RDBMS</span><span class="sxs-lookup"><span data-stu-id="16653-1341">RDBMS</span></span>
* <span data-ttu-id="16653-1342">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="16653-1342">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="16653-1343">Redis</span><span class="sxs-lookup"><span data-stu-id="16653-1343">Redis</span></span>
* <span data-ttu-id="16653-1344">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1344">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="16653-1345">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1345">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="16653-1346">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1346">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="16653-1347">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1347">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="16653-1348">[重大な変更]`redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1348">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="16653-1349">[重大な変更]`redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="16653-1349">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="16653-1350">[非推奨]`redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1350">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="16653-1351">Role</span><span class="sxs-lookup"><span data-stu-id="16653-1351">Role</span></span>
* <span data-ttu-id="16653-1352">[重大な変更]`az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="16653-1352">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="16653-1353">SQL VM</span><span class="sxs-lookup"><span data-stu-id="16653-1353">SQL VM</span></span>
* <span data-ttu-id="16653-1354">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1354">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1355">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1355">VM</span></span>
* <span data-ttu-id="16653-1356">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1356">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="16653-1357">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1357">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="16653-1358">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1358">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="16653-1359">[重大な変更]`az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="16653-1359">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="16653-1360">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="16653-1360">January 31, 2019</span></span>

<span data-ttu-id="16653-1361">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="16653-1361">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="16653-1362">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1362">Core</span></span>

* <span data-ttu-id="16653-1363">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="16653-1363">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="16653-1364">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="16653-1364">January 28, 2019</span></span>

<span data-ttu-id="16653-1365">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="16653-1365">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1366">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1366">ACR</span></span>
* <span data-ttu-id="16653-1367">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1367">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1368">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1368">ACS</span></span>
* <span data-ttu-id="16653-1369">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1369">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="16653-1370">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1370">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="16653-1371">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1371">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="16653-1372">AMS</span><span class="sxs-lookup"><span data-stu-id="16653-1372">AMS</span></span>
* <span data-ttu-id="16653-1373">[重大な変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1373">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="16653-1374">[重大な変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1374">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1375">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-1375">Appservice</span></span>
* <span data-ttu-id="16653-1376">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1376">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="16653-1377">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1377">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="16653-1378">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1378">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="16653-1379">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-1379">Container</span></span>
* <span data-ttu-id="16653-1380">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1380">Added `container start` command</span></span>
* <span data-ttu-id="16653-1381">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1381">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="16653-1382">EventGrid</span><span class="sxs-lookup"><span data-stu-id="16653-1382">EventGrid</span></span>
* <span data-ttu-id="16653-1383">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1383">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="16653-1384">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1384">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="16653-1385">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1385">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="16653-1386">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1386">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="16653-1387">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="16653-1387">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="16653-1388">HDInsight</span><span class="sxs-lookup"><span data-stu-id="16653-1388">HDInsight</span></span>
* <span data-ttu-id="16653-1389">[重大な変更]`hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1389">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="16653-1390">[重大な変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1390">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="16653-1391">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1391">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="16653-1392">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-1392">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="16653-1393">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1393">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="16653-1394">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1394">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="16653-1395">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-1395">IoT</span></span>
* <span data-ttu-id="16653-1396">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1396">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="16653-1397">Kusto</span><span class="sxs-lookup"><span data-stu-id="16653-1397">Kusto</span></span>
* <span data-ttu-id="16653-1398">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="16653-1398">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-1399">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-1399">Monitor</span></span>
* <span data-ttu-id="16653-1400">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1400">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="16653-1401">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-1401">Profile</span></span>
* <span data-ttu-id="16653-1402">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1402">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="16653-1403">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1403">Network</span></span>
* <span data-ttu-id="16653-1404">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1404">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="16653-1405">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1405">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="16653-1406">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-1406">Resource</span></span>
* <span data-ttu-id="16653-1407">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1407">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="16653-1408">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1408">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="16653-1409">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="16653-1409">SQL Virtual Machine</span></span>
* <span data-ttu-id="16653-1410">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="16653-1410">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="16653-1411">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-1411">Storage</span></span>
* <span data-ttu-id="16653-1412">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1412">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="16653-1413">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="16653-1413">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1414">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1414">VM</span></span>
* <span data-ttu-id="16653-1415">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1415">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="16653-1416">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1416">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="16653-1417">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="16653-1417">January 15, 2019</span></span>

<span data-ttu-id="16653-1418">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="16653-1418">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1419">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1419">ACR</span></span>
* <span data-ttu-id="16653-1420">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1420">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="16653-1421">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1421">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="16653-1422">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1422">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="16653-1423">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1423">ACS</span></span>
* <span data-ttu-id="16653-1424">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1424">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1425">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-1425">Appservice</span></span>
* <span data-ttu-id="16653-1426">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1426">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="16653-1427">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1427">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="16653-1428">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1428">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="16653-1429">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1429">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="16653-1430">Botservice</span><span class="sxs-lookup"><span data-stu-id="16653-1430">Botservice</span></span>
* <span data-ttu-id="16653-1431">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1431">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="16653-1432">構成</span><span class="sxs-lookup"><span data-stu-id="16653-1432">Configure</span></span>
* <span data-ttu-id="16653-1433">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1433">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="16653-1434">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-1434">CosmosDB</span></span>
* <span data-ttu-id="16653-1435">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1435">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="16653-1436">HDInsight</span><span class="sxs-lookup"><span data-stu-id="16653-1436">HDInsight</span></span>
* <span data-ttu-id="16653-1437">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1437">Added commands for managing applications</span></span>
* <span data-ttu-id="16653-1438">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1438">Added commands for managing script actions</span></span>
* <span data-ttu-id="16653-1439">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1439">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="16653-1440">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1440">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="16653-1441">[重大な変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1441">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="16653-1442">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1442">Network</span></span>
* <span data-ttu-id="16653-1443">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1443">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="16653-1444">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1444">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="16653-1445">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1445">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="16653-1446">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1446">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="16653-1447">Role</span><span class="sxs-lookup"><span data-stu-id="16653-1447">Role</span></span>
* <span data-ttu-id="16653-1448">[非推奨]`create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="16653-1448">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="16653-1449">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="16653-1449">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="16653-1450">Security</span><span class="sxs-lookup"><span data-stu-id="16653-1450">Security</span></span>
* <span data-ttu-id="16653-1451">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="16653-1451">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="16653-1452">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-1452">Storage</span></span>
* <span data-ttu-id="16653-1453">[重大な変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-1453">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="16653-1454">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="16653-1454">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="16653-1455">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1455">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="16653-1456">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1456">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="16653-1457">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1457">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1458">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1458">VM</span></span>
* <span data-ttu-id="16653-1459">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1459">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="16653-1460">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1460">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="16653-1461">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1461">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="16653-1462">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1462">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="16653-1463">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1463">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="16653-1464">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1464">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="16653-1465">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="16653-1465">December 20, 2018</span></span>

<span data-ttu-id="16653-1466">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="16653-1466">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="16653-1467">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-1467">Appservice</span></span>
* <span data-ttu-id="16653-1468">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1468">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="16653-1469">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1469">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="16653-1470">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1470">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="16653-1471">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="16653-1471">IoTCentral</span></span>
* <span data-ttu-id="16653-1472">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1472">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="16653-1473">Role</span><span class="sxs-lookup"><span data-stu-id="16653-1473">Role</span></span>
* <span data-ttu-id="16653-1474">[重大な変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1474">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="16653-1475">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-1475">SQL</span></span>
* <span data-ttu-id="16653-1476">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1476">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1477">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1477">VM</span></span>
* <span data-ttu-id="16653-1478">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1478">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="16653-1479">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="16653-1479">December 18, 2018</span></span>

<span data-ttu-id="16653-1480">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="16653-1480">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="16653-1481">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1481">ACR</span></span>
* <span data-ttu-id="16653-1482">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1482">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="16653-1483">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="16653-1483">Condensed the table layout for task list</span></span>
* <span data-ttu-id="16653-1484">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1484">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1485">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1485">ACS</span></span>
* <span data-ttu-id="16653-1486">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1486">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="16653-1487">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1487">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="16653-1488">[非推奨]`az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="16653-1488">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="16653-1489">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="16653-1489">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="16653-1490">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1490">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="16653-1491">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1491">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1492">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-1492">Appservice</span></span>
* <span data-ttu-id="16653-1493">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1493">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="16653-1494">Botservice</span><span class="sxs-lookup"><span data-stu-id="16653-1494">Botservice</span></span>
* <span data-ttu-id="16653-1495">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1495">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="16653-1496">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1496">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="16653-1497">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1497">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="16653-1498">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="16653-1498">Reduced Kudu network calls</span></span>
* <span data-ttu-id="16653-1499">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-1499">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="16653-1500">従量課金</span><span class="sxs-lookup"><span data-stu-id="16653-1500">Consumption</span></span>
* <span data-ttu-id="16653-1501">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1501">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="16653-1502">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-1502">CosmosDB</span></span>
* <span data-ttu-id="16653-1503">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1503">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="16653-1504">マップ</span><span class="sxs-lookup"><span data-stu-id="16653-1504">Maps</span></span>
* <span data-ttu-id="16653-1505">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1505">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="16653-1506">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1506">Network</span></span>
* <span data-ttu-id="16653-1507">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1507">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="16653-1508">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1508">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="16653-1509">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-1509">Resource</span></span>
* <span data-ttu-id="16653-1510">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1510">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="16653-1511">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1511">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="16653-1512">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-1512">Storage</span></span>
*  <span data-ttu-id="16653-1513">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1513">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1514">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1514">VM</span></span>
* <span data-ttu-id="16653-1515">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1515">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="16653-1516">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="16653-1516">December 4, 2018</span></span>

<span data-ttu-id="16653-1517">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="16653-1517">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="16653-1518">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1518">Core</span></span>
* <span data-ttu-id="16653-1519">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1519">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="16653-1520">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1520">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1521">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-1521">Appservice</span></span>
* <span data-ttu-id="16653-1522">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1522">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="16653-1523">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1523">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="16653-1524">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1524">Network</span></span>
* <span data-ttu-id="16653-1525">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1525">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="16653-1526">Role</span><span class="sxs-lookup"><span data-stu-id="16653-1526">Role</span></span>
* <span data-ttu-id="16653-1527">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1527">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="16653-1528">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1528">VM</span></span>
* <span data-ttu-id="16653-1529">[非推奨]`vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1529">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="16653-1530">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1530">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="16653-1531">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1531">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="16653-1532">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1532">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="16653-1533">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="16653-1533">November 20, 2018</span></span>

<span data-ttu-id="16653-1534">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="16653-1534">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="16653-1535">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1535">Core</span></span>
* <span data-ttu-id="16653-1536">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1536">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1537">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1537">ACR</span></span>
* <span data-ttu-id="16653-1538">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1538">Added context token to task step</span></span>
* <span data-ttu-id="16653-1539">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1539">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="16653-1540">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-1540">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1541">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-1541">Appservice</span></span>
* <span data-ttu-id="16653-1542">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1542">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="16653-1543">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="16653-1543">Updated the default `node_version`.</span></span> <span data-ttu-id="16653-1544">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="16653-1544">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="16653-1545">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1545">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="16653-1546">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1546">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="16653-1547">IotCentral</span><span class="sxs-lookup"><span data-stu-id="16653-1547">IotCentral</span></span>
* <span data-ttu-id="16653-1548">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1548">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="16653-1549">KeyVault</span><span class="sxs-lookup"><span data-stu-id="16653-1549">KeyVault</span></span>
* <span data-ttu-id="16653-1550">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1550">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="16653-1551">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1551">Network</span></span>
* <span data-ttu-id="16653-1552">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1552">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="16653-1553">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1553">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="16653-1554">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1554">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="16653-1555">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1555">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="16653-1556">Rdbms</span><span class="sxs-lookup"><span data-stu-id="16653-1556">Rdbms</span></span>
* <span data-ttu-id="16653-1557">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1557">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="16653-1558">Rbac</span><span class="sxs-lookup"><span data-stu-id="16653-1558">Rbac</span></span>
* <span data-ttu-id="16653-1559">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1559">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="16653-1560">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1560">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="16653-1561">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-1561">Storage</span></span>
* <span data-ttu-id="16653-1562">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-1562">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="16653-1563">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1563">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="16653-1564">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1564">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="16653-1565">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="16653-1565">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1566">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1566">VM</span></span>
* <span data-ttu-id="16653-1567">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1567">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="16653-1568">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1568">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="16653-1569">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="16653-1569">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="16653-1570">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1570">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="16653-1571">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1571">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="16653-1572">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1572">Added `snapshot wait` command</span></span>
* <span data-ttu-id="16653-1573">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1573">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="16653-1574">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="16653-1574">November 6, 2018</span></span>

<span data-ttu-id="16653-1575">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="16653-1575">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="16653-1576">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1576">Core</span></span>
* <span data-ttu-id="16653-1577">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1577">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1578">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1578">ACR</span></span>
* <span data-ttu-id="16653-1579">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1579">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="16653-1580">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1580">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1581">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1581">ACS</span></span>
* <span data-ttu-id="16653-1582">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1582">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="16653-1583">Advisor</span><span class="sxs-lookup"><span data-stu-id="16653-1583">Advisor</span></span>
* <span data-ttu-id="16653-1584">GA リリース</span><span class="sxs-lookup"><span data-stu-id="16653-1584">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="16653-1585">AMS</span><span class="sxs-lookup"><span data-stu-id="16653-1585">AMS</span></span>
* <span data-ttu-id="16653-1586">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1586">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="16653-1587">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1587">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="16653-1588">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1588">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="16653-1589">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-1589">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="16653-1590">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1590">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="16653-1591">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1591">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="16653-1592">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1592">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="16653-1593">[重大な変更]`ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="16653-1593">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="16653-1594">[重大な変更]`ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-1594">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="16653-1595">[重大な変更]`ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1595">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="16653-1596">[重大な変更]`ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="16653-1596">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="16653-1597">[重大な変更]`ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="16653-1597">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="16653-1598">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="16653-1598">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="16653-1599">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="16653-1599">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="16653-1600">[重大な変更]`ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-1600">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="16653-1601">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="16653-1601">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="16653-1602">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="16653-1602">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1603">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-1603">AppService</span></span>
* <span data-ttu-id="16653-1604">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1604">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="16653-1605">構成</span><span class="sxs-lookup"><span data-stu-id="16653-1605">Configure</span></span>
* <span data-ttu-id="16653-1606">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1606">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="16653-1607">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-1607">Container</span></span>
* <span data-ttu-id="16653-1608">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1608">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="16653-1609">EventHub</span><span class="sxs-lookup"><span data-stu-id="16653-1609">EventHub</span></span>
* <span data-ttu-id="16653-1610">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1610">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="16653-1611">Interactive</span><span class="sxs-lookup"><span data-stu-id="16653-1611">Interactive</span></span>
* <span data-ttu-id="16653-1612">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="16653-1612">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-1613">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-1613">Monitor</span></span>
* <span data-ttu-id="16653-1614">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-1614">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="16653-1615">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1615">Network</span></span>
* <span data-ttu-id="16653-1616">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1616">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="16653-1617">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1617">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="16653-1618">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1618">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="16653-1619">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-1619">Profile</span></span>
* <span data-ttu-id="16653-1620">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1620">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="16653-1621">RDBMS</span><span class="sxs-lookup"><span data-stu-id="16653-1621">RDBMS</span></span>
* <span data-ttu-id="16653-1622">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1622">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="16653-1623">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-1623">Resource</span></span>
* <span data-ttu-id="16653-1624">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1624">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="16653-1625">Role</span><span class="sxs-lookup"><span data-stu-id="16653-1625">Role</span></span>
* <span data-ttu-id="16653-1626">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-1626">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="16653-1627">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1627">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="16653-1628">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1628">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="16653-1629">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-1629">Storage</span></span>
* <span data-ttu-id="16653-1630">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="16653-1630">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1631">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1631">VM</span></span>
* <span data-ttu-id="16653-1632">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1632">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="16653-1633">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1633">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="16653-1634">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1634">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="16653-1635">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-1635">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="16653-1636">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="16653-1636">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="16653-1637">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-1637">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="16653-1638">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="16653-1638">October 23, 2018</span></span>

<span data-ttu-id="16653-1639">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="16653-1639">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="16653-1640">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1640">Core</span></span>
* <span data-ttu-id="16653-1641">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1641">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="16653-1642">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1642">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1643">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1643">ACR</span></span>
* <span data-ttu-id="16653-1644">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1644">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="16653-1645">CDN</span><span class="sxs-lookup"><span data-stu-id="16653-1645">CDN</span></span>
* <span data-ttu-id="16653-1646">[重大な変更]`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="16653-1646">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="16653-1647">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-1647">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="16653-1648">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-1648">Container</span></span>
* <span data-ttu-id="16653-1649">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1649">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="16653-1650">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1650">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="16653-1651">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1651">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="16653-1652">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1652">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="16653-1653">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1653">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="16653-1654">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1654">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="16653-1655">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1655">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="16653-1656">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-1656">CosmosDB</span></span>
* <span data-ttu-id="16653-1657">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1657">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="16653-1658">Interactive</span><span class="sxs-lookup"><span data-stu-id="16653-1658">Interactive</span></span>
* <span data-ttu-id="16653-1659">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1659">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="16653-1660">IoT Central</span><span class="sxs-lookup"><span data-stu-id="16653-1660">IoT Central</span></span>
* <span data-ttu-id="16653-1661">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1661">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="16653-1662">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="16653-1662">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-1663">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-1663">Monitor</span></span>
* <span data-ttu-id="16653-1664">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="16653-1664">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="16653-1665">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1665">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="16653-1666">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1666">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="16653-1667">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-1667">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="16653-1668">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1668">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="16653-1669">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1669">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="16653-1670">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="16653-1670">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="16653-1671">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1671">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="16653-1672">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-1672">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="16653-1673">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-1673">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="16653-1674">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1674">Network</span></span>
* <span data-ttu-id="16653-1675">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1675">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="16653-1676">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1676">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="16653-1677">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="16653-1677">ServiceBus</span></span>
* <span data-ttu-id="16653-1678">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1678">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="16653-1679">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-1679">SQL</span></span>
* <span data-ttu-id="16653-1680">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1680">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="16653-1681">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-1681">Storage</span></span>
* <span data-ttu-id="16653-1682">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1682">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="16653-1683">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1683">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1684">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1684">VM</span></span>
* <span data-ttu-id="16653-1685">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="16653-1685">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="16653-1686">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-1686">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="16653-1687">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1687">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="16653-1688">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="16653-1688">October 16, 2018</span></span>

<span data-ttu-id="16653-1689">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="16653-1689">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1690">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1690">VM</span></span>
* <span data-ttu-id="16653-1691">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1691">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="16653-1692">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="16653-1692">October 9, 2018</span></span>

<span data-ttu-id="16653-1693">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="16653-1693">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="16653-1694">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1694">Core</span></span>
* <span data-ttu-id="16653-1695">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-1695">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1696">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1696">ACR</span></span>
* <span data-ttu-id="16653-1697">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1697">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1698">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1698">ACS</span></span>
* <span data-ttu-id="16653-1699">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="16653-1699">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="16653-1700">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1700">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="16653-1701">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1701">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="16653-1702">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-1702">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="16653-1703">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-1703">Container</span></span>
* <span data-ttu-id="16653-1704">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1704">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="16653-1705">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1705">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="16653-1706">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="16653-1706">Event Hub</span></span>
* <span data-ttu-id="16653-1707">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1707">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="16653-1708">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1708">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="16653-1709">拡張機能</span><span class="sxs-lookup"><span data-stu-id="16653-1709">Extensions</span></span>
* <span data-ttu-id="16653-1710">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1710">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="16653-1711">HDInsight</span><span class="sxs-lookup"><span data-stu-id="16653-1711">HDInsight</span></span>
* <span data-ttu-id="16653-1712">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="16653-1712">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="16653-1713">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-1713">IoT</span></span>
* <span data-ttu-id="16653-1714">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1714">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="16653-1715">KeyVault</span><span class="sxs-lookup"><span data-stu-id="16653-1715">KeyVault</span></span>
* <span data-ttu-id="16653-1716">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1716">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="16653-1717">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1717">Network</span></span>
* <span data-ttu-id="16653-1718">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="16653-1718">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="16653-1719">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="16653-1719">See #6052</span></span>
* <span data-ttu-id="16653-1720">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1720">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="16653-1721">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="16653-1721">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="16653-1722">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1722">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="16653-1723">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1723">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="16653-1724">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1724">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="16653-1725">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1725">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="16653-1726">Role</span><span class="sxs-lookup"><span data-stu-id="16653-1726">Role</span></span>
* <span data-ttu-id="16653-1727">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1727">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="16653-1728">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1728">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="16653-1729">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1729">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="16653-1730">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1730">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="16653-1731">Service Bus</span><span class="sxs-lookup"><span data-stu-id="16653-1731">Service Bus</span></span>
* <span data-ttu-id="16653-1732">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1732">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1733">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1733">VM</span></span>
* <span data-ttu-id="16653-1734">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1734">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="16653-1735">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1735">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="16653-1736">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1736">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="16653-1737">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1737">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="16653-1738">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1738">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="16653-1739">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1739">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="16653-1740">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="16653-1740">September 21, 2018</span></span>

<span data-ttu-id="16653-1741">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="16653-1741">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1742">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1742">ACR</span></span>
* <span data-ttu-id="16653-1743">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1743">Added ACR Task commands</span></span>
* <span data-ttu-id="16653-1744">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1744">Added quick run command</span></span>
* <span data-ttu-id="16653-1745">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1745">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="16653-1746">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1746">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="16653-1747">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1747">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="16653-1748">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1748">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1749">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1749">ACS</span></span>
* <span data-ttu-id="16653-1750">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1750">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="16653-1751">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1751">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1752">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-1752">AppService</span></span>

* <span data-ttu-id="16653-1753">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1753">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="16653-1754">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1754">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="16653-1755">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1755">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="16653-1756">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1756">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="16653-1757">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-1757">Batch</span></span>
* <span data-ttu-id="16653-1758">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1758">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="16653-1759">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-1759">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="16653-1760">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1760">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="16653-1761">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1761">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="16653-1762">Batch AI</span><span class="sxs-lookup"><span data-stu-id="16653-1762">Batch AI</span></span> 
* <span data-ttu-id="16653-1763">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1763">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="16653-1764">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="16653-1764">Cognitive Services</span></span>
* <span data-ttu-id="16653-1765">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1765">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="16653-1766">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1766">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="16653-1767">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1767">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="16653-1768">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1768">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="16653-1769">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1769">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="16653-1770">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1770">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="16653-1771">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-1771">Container</span></span>
* <span data-ttu-id="16653-1772">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1772">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="16653-1773">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1773">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="16653-1774">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1774">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="16653-1775">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1775">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="16653-1776">DataLake</span><span class="sxs-lookup"><span data-stu-id="16653-1776">Datalake</span></span>
* <span data-ttu-id="16653-1777">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1777">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="16653-1778">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="16653-1778">Interactive Shell</span></span>
* <span data-ttu-id="16653-1779">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1779">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="16653-1780">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1780">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="16653-1781">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-1781">IoT</span></span>
* <span data-ttu-id="16653-1782">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1782">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="16653-1783">Key Vault</span><span class="sxs-lookup"><span data-stu-id="16653-1783">Key Vault</span></span>
* <span data-ttu-id="16653-1784">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1784">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="16653-1785">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1785">Network</span></span>
* <span data-ttu-id="16653-1786">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1786">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="16653-1787">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1787">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="16653-1788">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1788">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="16653-1789">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1789">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="16653-1790">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1790">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="16653-1791">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1791">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="16653-1792">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="16653-1792">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="16653-1793">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-1793">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="16653-1794">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1794">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="16653-1795">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1795">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="16653-1796">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1796">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="16653-1797">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1797">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="16653-1798">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1798">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="16653-1799">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="16653-1799">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="16653-1800">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1800">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="16653-1801">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1801">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="16653-1802">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1802">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="16653-1803">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1803">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="16653-1804">RDBMS</span><span class="sxs-lookup"><span data-stu-id="16653-1804">RDBMS</span></span>
* <span data-ttu-id="16653-1805">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1805">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="16653-1806">予約</span><span class="sxs-lookup"><span data-stu-id="16653-1806">Reservation</span></span>
* <span data-ttu-id="16653-1807">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1807">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="16653-1808">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1808">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="16653-1809">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="16653-1809">Manage App</span></span>
* <span data-ttu-id="16653-1810">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1810">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="16653-1811">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1811">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="16653-1812">Role</span><span class="sxs-lookup"><span data-stu-id="16653-1812">Role</span></span>
* <span data-ttu-id="16653-1813">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1813">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="16653-1814">SignalR</span><span class="sxs-lookup"><span data-stu-id="16653-1814">SignalR</span></span>
* <span data-ttu-id="16653-1815">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="16653-1815">First release</span></span>

### <a name="storage"></a><span data-ttu-id="16653-1816">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-1816">Storage</span></span>
* <span data-ttu-id="16653-1817">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1817">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="16653-1818">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1818">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1819">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1819">VM</span></span>
* <span data-ttu-id="16653-1820">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="16653-1820">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="16653-1821">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1821">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="16653-1822">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="16653-1822">August 28, 2018</span></span>

<span data-ttu-id="16653-1823">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="16653-1823">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="16653-1824">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1824">Core</span></span>

* <span data-ttu-id="16653-1825">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1825">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="16653-1826">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1826">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1827">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1827">ACR</span></span>

* <span data-ttu-id="16653-1828">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1828">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="16653-1829">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1829">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1830">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1830">ACS</span></span>

* <span data-ttu-id="16653-1831">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1831">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="16653-1832">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1832">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1833">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-1833">AppService</span></span>

* <span data-ttu-id="16653-1834">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1834">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="16653-1835">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1835">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="16653-1836">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1836">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="16653-1837">バックアップ</span><span class="sxs-lookup"><span data-stu-id="16653-1837">Backup</span></span>

* <span data-ttu-id="16653-1838">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1838">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="16653-1839">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="16653-1839">Bot Service</span></span>

* <span data-ttu-id="16653-1840">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="16653-1840">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="16653-1841">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="16653-1841">Cognitive Services</span></span>

* <span data-ttu-id="16653-1842">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1842">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="16653-1843">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-1843">IoT</span></span>

* <span data-ttu-id="16653-1844">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1844">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-1845">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-1845">Monitor</span></span>

* <span data-ttu-id="16653-1846">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1846">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="16653-1847">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1847">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="16653-1848">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1848">Network</span></span>

* <span data-ttu-id="16653-1849">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1849">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="16653-1850">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-1850">Resource</span></span>

* <span data-ttu-id="16653-1851">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1851">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="16653-1852">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-1852">Storage</span></span>

* <span data-ttu-id="16653-1853">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1853">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1854">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1854">VM</span></span>

* <span data-ttu-id="16653-1855">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1855">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="16653-1856">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1856">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="16653-1857">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="16653-1857">Auguest 14, 2018</span></span>

<span data-ttu-id="16653-1858">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="16653-1858">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="16653-1859">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1859">Core</span></span>

* <span data-ttu-id="16653-1860">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1860">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="16653-1861">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1861">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="16653-1862">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="16653-1862">Telemetry</span></span>

* <span data-ttu-id="16653-1863">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-1863">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1864">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1864">ACR</span></span>

* <span data-ttu-id="16653-1865">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1865">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="16653-1866">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1866">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1867">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1867">ACS</span></span>

* <span data-ttu-id="16653-1868">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1868">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="16653-1869">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1869">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="16653-1870">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1870">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="16653-1871">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1871">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="16653-1872">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1872">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="16653-1873">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-1873">AppService</span></span>

* <span data-ttu-id="16653-1874">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1874">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="16653-1875">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1875">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="16653-1876">BatchAI</span><span class="sxs-lookup"><span data-stu-id="16653-1876">BatchAI</span></span>

* <span data-ttu-id="16653-1877">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-1877">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="16653-1878">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-1878">Container</span></span>

* <span data-ttu-id="16653-1879">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1879">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="16653-1880">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-1880">IoT</span></span>

* <span data-ttu-id="16653-1881">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1881">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="16653-1882">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-1882">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="16653-1883">Iot Central</span><span class="sxs-lookup"><span data-stu-id="16653-1883">Iot Central</span></span>

* <span data-ttu-id="16653-1884">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="16653-1884">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="16653-1885">KeyVault</span><span class="sxs-lookup"><span data-stu-id="16653-1885">KeyVault</span></span>


* <span data-ttu-id="16653-1886">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1886">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="16653-1887">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1887">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="16653-1888">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1888">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="16653-1889">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1889">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="16653-1890">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1890">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="16653-1891">リレー</span><span class="sxs-lookup"><span data-stu-id="16653-1891">Relay</span></span>

* <span data-ttu-id="16653-1892">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="16653-1892">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="16653-1893">Sql</span><span class="sxs-lookup"><span data-stu-id="16653-1893">Sql</span></span>

* <span data-ttu-id="16653-1894">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1894">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="16653-1895">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-1895">Storage</span></span>

* <span data-ttu-id="16653-1896">[重大な変更]`--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="16653-1896">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="16653-1897">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1897">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="16653-1898">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="16653-1898">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="16653-1899">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1899">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="16653-1900">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1900">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1901">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1901">VM</span></span>

* <span data-ttu-id="16653-1902">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1902">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="16653-1903">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="16653-1903">July 31, 2018</span></span>

<span data-ttu-id="16653-1904">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="16653-1904">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1905">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1905">ACR</span></span>

* <span data-ttu-id="16653-1906">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1906">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="16653-1907">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1907">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1908">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1908">ACS</span></span>

* <span data-ttu-id="16653-1909">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1909">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="16653-1910">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-1910">Batch</span></span>

* <span data-ttu-id="16653-1911">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1911">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="16653-1912">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-1912">Container</span></span>

* <span data-ttu-id="16653-1913">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1913">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="16653-1914">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1914">Network</span></span>

* <span data-ttu-id="16653-1915">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1915">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="16653-1916">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-1916">Resource</span></span>

* <span data-ttu-id="16653-1917">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1917">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="16653-1918">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1918">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="16653-1919">Role</span><span class="sxs-lookup"><span data-stu-id="16653-1919">Role</span></span>

* <span data-ttu-id="16653-1920">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1920">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="16653-1921">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1921">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="16653-1922">検索</span><span class="sxs-lookup"><span data-stu-id="16653-1922">Search</span></span>

* <span data-ttu-id="16653-1923">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1923">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="16653-1924">Service Bus</span><span class="sxs-lookup"><span data-stu-id="16653-1924">Service Bus</span></span>

* <span data-ttu-id="16653-1925">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1925">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="16653-1926">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1926">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="16653-1927">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="16653-1927">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="16653-1928">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="16653-1928">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="16653-1929">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-1929">Storage</span></span>

* <span data-ttu-id="16653-1930">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-1930">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="16653-1931">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="16653-1931">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1932">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1932">VM</span></span>

* <span data-ttu-id="16653-1933">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-1933">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="16653-1934">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1934">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="16653-1935">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1935">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="16653-1936">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1936">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="16653-1937">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="16653-1937">July 18, 2018</span></span>

<span data-ttu-id="16653-1938">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="16653-1938">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="16653-1939">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1939">Core</span></span>

* <span data-ttu-id="16653-1940">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1940">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="16653-1941">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1941">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="16653-1942">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1942">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1943">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1943">ACR</span></span>

* <span data-ttu-id="16653-1944">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-1944">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="16653-1945">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1945">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="16653-1946">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1946">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="16653-1947">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1947">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1948">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1948">ACS</span></span>

* <span data-ttu-id="16653-1949">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1949">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-1950">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-1950">AppService</span></span>

* <span data-ttu-id="16653-1951">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1951">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="16653-1952">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-1952">Batch</span></span>

* <span data-ttu-id="16653-1953">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1953">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="16653-1954">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1954">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="16653-1955">Batch AI</span><span class="sxs-lookup"><span data-stu-id="16653-1955">Batch AI</span></span>

* <span data-ttu-id="16653-1956">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1956">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="16653-1957">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-1957">Container</span></span>

* <span data-ttu-id="16653-1958">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-1958">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="16653-1959">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1959">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="16653-1960">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-1960">Network</span></span>

* <span data-ttu-id="16653-1961">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1961">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="16653-1962">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1962">Added `network nic wait`</span></span>
* <span data-ttu-id="16653-1963">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1963">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="16653-1964">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1964">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="16653-1965">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-1965">Resource</span></span>

* <span data-ttu-id="16653-1966">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1966">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="16653-1967">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1967">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="16653-1968">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1968">Added `deployment wait` command</span></span>
* <span data-ttu-id="16653-1969">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1969">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="16653-1970">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-1970">SQL</span></span>

* <span data-ttu-id="16653-1971">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-1971">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="16653-1972">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-1972">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="16653-1973">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="16653-1973">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="16653-1974">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-1974">Storage</span></span>

* <span data-ttu-id="16653-1975">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1975">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="16653-1976">VM</span><span class="sxs-lookup"><span data-stu-id="16653-1976">VM</span></span>

* <span data-ttu-id="16653-1977">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1977">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="16653-1978">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1978">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="16653-1979">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1979">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="16653-1980">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="16653-1980">July 3, 2018</span></span>

<span data-ttu-id="16653-1981">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="16653-1981">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="16653-1982">AKS</span><span class="sxs-lookup"><span data-stu-id="16653-1982">AKS</span></span>

* <span data-ttu-id="16653-1983">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-1983">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="16653-1984">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="16653-1984">July 3, 2018</span></span>

<span data-ttu-id="16653-1985">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="16653-1985">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="16653-1986">コア</span><span class="sxs-lookup"><span data-stu-id="16653-1986">Core</span></span>

* <span data-ttu-id="16653-1987">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1987">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="16653-1988">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-1988">ACR</span></span>

* <span data-ttu-id="16653-1989">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1989">Added polling build status</span></span>
* <span data-ttu-id="16653-1990">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1990">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="16653-1991">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1991">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="16653-1992">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-1992">ACS</span></span>

* <span data-ttu-id="16653-1993">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1993">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="16653-1994">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-1994">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="16653-1995">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="16653-1995">Updated options for `aks browse` command.</span></span> <span data-ttu-id="16653-1996">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1996">Added `--listen-port` support</span></span>
* <span data-ttu-id="16653-1997">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="16653-1997">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="16653-1998">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="16653-1998">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="16653-1999">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-1999">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2000">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-2000">AppService</span></span>

* <span data-ttu-id="16653-2001">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-2001">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="16653-2002">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2002">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="16653-2003">バックアップ</span><span class="sxs-lookup"><span data-stu-id="16653-2003">Backup</span></span>

* <span data-ttu-id="16653-2004">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-2004">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="16653-2005">BatchAI</span><span class="sxs-lookup"><span data-stu-id="16653-2005">BatchAI</span></span>

* <span data-ttu-id="16653-2006">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2006">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="16653-2007">クラウド</span><span class="sxs-lookup"><span data-stu-id="16653-2007">Cloud</span></span>

* <span data-ttu-id="16653-2008">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2008">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="16653-2009">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-2009">Container</span></span>

* <span data-ttu-id="16653-2010">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2010">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="16653-2011">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2011">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="16653-2012">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2012">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="16653-2013">拡張機能</span><span class="sxs-lookup"><span data-stu-id="16653-2013">Extension</span></span>

* <span data-ttu-id="16653-2014">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2014">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="16653-2015">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2015">Network</span></span>

* <span data-ttu-id="16653-2016">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2016">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="16653-2017">Rdbms</span><span class="sxs-lookup"><span data-stu-id="16653-2017">Rdbms</span></span>

* <span data-ttu-id="16653-2018">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2018">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="16653-2019">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-2019">Resource</span></span>

* <span data-ttu-id="16653-2020">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2020">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2021">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2021">VM</span></span>

* <span data-ttu-id="16653-2022">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-2022">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="16653-2023">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="16653-2023">June 25, 2018</span></span>

<span data-ttu-id="16653-2024">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="16653-2024">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="16653-2025">CLI</span><span class="sxs-lookup"><span data-stu-id="16653-2025">CLI</span></span>

* <span data-ttu-id="16653-2026">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-2026">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="16653-2027">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="16653-2027">June 19, 2018</span></span>

<span data-ttu-id="16653-2028">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="16653-2028">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="16653-2029">コア</span><span class="sxs-lookup"><span data-stu-id="16653-2029">Core</span></span>

* <span data-ttu-id="16653-2030">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2030">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="16653-2031">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-2031">ACR</span></span>

* <span data-ttu-id="16653-2032">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2032">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="16653-2033">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2033">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2034">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2034">ACS</span></span>

* <span data-ttu-id="16653-2035">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2035">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="16653-2036">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2036">Added `--update` support</span></span>
* <span data-ttu-id="16653-2037">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2037">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="16653-2038">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="16653-2038">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="16653-2039">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2039">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="16653-2040">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2040">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="16653-2041">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2041">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="16653-2042">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2042">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2043">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-2043">AppService</span></span>

* <span data-ttu-id="16653-2044">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2044">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="16653-2045">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2045">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="16653-2046">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-2046">Batch</span></span>

* <span data-ttu-id="16653-2047">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2047">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="16653-2048">Batch AI</span><span class="sxs-lookup"><span data-stu-id="16653-2048">Batch AI</span></span>

* <span data-ttu-id="16653-2049">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2049">Added support for workspaces.</span></span> <span data-ttu-id="16653-2050">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="16653-2050">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="16653-2051">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2051">Added support for experiments.</span></span> <span data-ttu-id="16653-2052">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="16653-2052">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="16653-2053">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2053">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="16653-2054">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2054">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="16653-2055">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="16653-2055">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="16653-2056">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2056">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="16653-2057">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="16653-2057">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="16653-2058">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="16653-2058">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="16653-2059">[重大な変更]`--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2059">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="16653-2060">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="16653-2060">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="16653-2061">[重大な変更]`--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2061">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="16653-2062">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="16653-2062">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="16653-2063">[重大な変更]`location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2063">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="16653-2064">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="16653-2064">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="16653-2065">[重大な変更]`--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2065">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="16653-2066">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2066">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="16653-2067">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2067">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="16653-2068">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2068">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="16653-2069">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2069">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="16653-2070">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2070">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="16653-2071">マップ</span><span class="sxs-lookup"><span data-stu-id="16653-2071">Maps</span></span>

* <span data-ttu-id="16653-2072">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2072">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="16653-2073">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2073">Network</span></span>

* <span data-ttu-id="16653-2074">`https` のサポートを `network lb probe create` に追加しました ([#6571](https://github.com/Azure/azure-cli/issues/6571))</span><span class="sxs-lookup"><span data-stu-id="16653-2074">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="16653-2075">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2075">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="16653-2076">#6502</span><span class="sxs-lookup"><span data-stu-id="16653-2076">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="16653-2077">Reservations</span><span class="sxs-lookup"><span data-stu-id="16653-2077">Reservations</span></span>

* <span data-ttu-id="16653-2078">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2078">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="16653-2079">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2079">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="16653-2080">[重大な変更]`kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2080">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="16653-2081">[重大な変更]`Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2081">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="16653-2082">[重大な変更]`Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2082">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="16653-2083">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2083">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="16653-2084">Role</span><span class="sxs-lookup"><span data-stu-id="16653-2084">Role</span></span>

* <span data-ttu-id="16653-2085">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2085">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="16653-2086">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-2086">SQL</span></span>

* <span data-ttu-id="16653-2087">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2087">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2088">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2088">Storage</span></span>

* <span data-ttu-id="16653-2089">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="16653-2089">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2090">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2090">VM</span></span>

* <span data-ttu-id="16653-2091">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2091">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="16653-2092">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2092">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="16653-2093">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2093">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="16653-2094">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="16653-2094">June 13, 2018</span></span>

<span data-ttu-id="16653-2095">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="16653-2095">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="16653-2096">コア</span><span class="sxs-lookup"><span data-stu-id="16653-2096">Core</span></span>

* <span data-ttu-id="16653-2097">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2097">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="16653-2098">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="16653-2098">June 13, 2018</span></span>

<span data-ttu-id="16653-2099">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="16653-2099">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="16653-2100">AKS</span><span class="sxs-lookup"><span data-stu-id="16653-2100">AKS</span></span>

* <span data-ttu-id="16653-2101">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2101">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="16653-2102">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2102">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="16653-2103">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2103">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="16653-2104">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2104">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="16653-2105">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2105">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2106">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-2106">AppService</span></span>

* <span data-ttu-id="16653-2107">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2107">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="16653-2108">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="16653-2108">June 5, 2018</span></span>

<span data-ttu-id="16653-2109">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="16653-2109">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="16653-2110">Interactive</span><span class="sxs-lookup"><span data-stu-id="16653-2110">Interactive</span></span>

* <span data-ttu-id="16653-2111">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2111">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="16653-2112">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="16653-2112">June 5, 2018</span></span>

<span data-ttu-id="16653-2113">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="16653-2113">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="16653-2114">コア</span><span class="sxs-lookup"><span data-stu-id="16653-2114">Core</span></span>

* <span data-ttu-id="16653-2115">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2115">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="16653-2116">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="16653-2116">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="16653-2117">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-2117">ACR</span></span>

* <span data-ttu-id="16653-2118">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2118">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="16653-2119">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2119">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="16653-2120">AKS</span><span class="sxs-lookup"><span data-stu-id="16653-2120">AKS</span></span>

* <span data-ttu-id="16653-2121">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2121">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="16653-2122">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-2122">Batch</span></span>

* <span data-ttu-id="16653-2123">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2123">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="16653-2124">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-2124">IOT</span></span>

* <span data-ttu-id="16653-2125">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2125">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="16653-2126">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2126">Network</span></span>

* <span data-ttu-id="16653-2127">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="16653-2127">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="16653-2128">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="16653-2128">Policy Insights</span></span>

* <span data-ttu-id="16653-2129">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="16653-2129">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="16653-2130">ARM</span><span class="sxs-lookup"><span data-stu-id="16653-2130">ARM</span></span>

* <span data-ttu-id="16653-2131">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2131">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="16653-2132">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-2132">SQL</span></span>

* <span data-ttu-id="16653-2133">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2133">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="16653-2134">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2134">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="16653-2135">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2135">Storage</span></span>

* <span data-ttu-id="16653-2136">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2136">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2137">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2137">VM</span></span>

* <span data-ttu-id="16653-2138">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2138">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="16653-2139">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2139">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="16653-2140">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2140">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="16653-2141">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="16653-2141">May 22, 2018</span></span>

<span data-ttu-id="16653-2142">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="16653-2142">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="16653-2143">コア</span><span class="sxs-lookup"><span data-stu-id="16653-2143">Core</span></span>

* <span data-ttu-id="16653-2144">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2144">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2145">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2145">ACS</span></span>

* <span data-ttu-id="16653-2146">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2146">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="16653-2147">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2147">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2148">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-2148">AppService</span></span>

* <span data-ttu-id="16653-2149">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="16653-2149">Improved generic update commands</span></span>
* <span data-ttu-id="16653-2150">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2150">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="16653-2151">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-2151">Container</span></span>

* <span data-ttu-id="16653-2152">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2152">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="16653-2153">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2153">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="16653-2154">拡張機能</span><span class="sxs-lookup"><span data-stu-id="16653-2154">Extension</span></span>

* <span data-ttu-id="16653-2155">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="16653-2155">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="16653-2156">Interactive</span><span class="sxs-lookup"><span data-stu-id="16653-2156">Interactive</span></span>

* <span data-ttu-id="16653-2157">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2157">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="16653-2158">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="16653-2158">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="16653-2159">KeyVault</span><span class="sxs-lookup"><span data-stu-id="16653-2159">KeyVault</span></span>

* <span data-ttu-id="16653-2160">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2160">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="16653-2161">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2161">Network</span></span>

* <span data-ttu-id="16653-2162">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2162">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="16653-2163">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2163">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="16653-2164">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-2164">SQL</span></span>

* <span data-ttu-id="16653-2165">[重大な変更]`db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2165">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="16653-2166">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2166">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="16653-2167">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2167">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="16653-2168">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2168">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="16653-2169">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2169">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="16653-2170">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="16653-2170">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="16653-2171">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="16653-2171">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="16653-2172">`edition`</span><span class="sxs-lookup"><span data-stu-id="16653-2172">`edition`.</span></span> <span data-ttu-id="16653-2173">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="16653-2173">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="16653-2174">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="16653-2174">`elasticPoolName`.</span></span> <span data-ttu-id="16653-2175">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="16653-2175">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="16653-2176">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2176">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="16653-2177">`edition`</span><span class="sxs-lookup"><span data-stu-id="16653-2177">`edition`.</span></span> <span data-ttu-id="16653-2178">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="16653-2178">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="16653-2179">`dtu`</span><span class="sxs-lookup"><span data-stu-id="16653-2179">`dtu`.</span></span> <span data-ttu-id="16653-2180">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="16653-2180">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="16653-2181">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="16653-2181">`databaseDtuMin`.</span></span> <span data-ttu-id="16653-2182">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="16653-2182">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="16653-2183">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="16653-2183">`databaseDtuMax`.</span></span> <span data-ttu-id="16653-2184">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="16653-2184">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="16653-2185">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2185">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="16653-2186">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2186">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2187">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2187">Storage</span></span>

* <span data-ttu-id="16653-2188">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2188">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="16653-2189">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2189">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2190">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2190">VM</span></span>

* <span data-ttu-id="16653-2191">[重大な変更]`--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2191">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="16653-2192">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="16653-2192">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="16653-2193">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2193">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="16653-2194">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2194">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="16653-2195">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2195">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="16653-2196">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="16653-2196">May 7, 2018</span></span>

<span data-ttu-id="16653-2197">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="16653-2197">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="16653-2198">コア</span><span class="sxs-lookup"><span data-stu-id="16653-2198">Core</span></span>

* <span data-ttu-id="16653-2199">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2199">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="16653-2200">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2200">Added limited support for positional arguments</span></span>
* <span data-ttu-id="16653-2201">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2201">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="16653-2202">#5591</span><span class="sxs-lookup"><span data-stu-id="16653-2202">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="16653-2203">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2203">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="16653-2204">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="16653-2204">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="16653-2205">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2205">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="16653-2206">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2206">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="16653-2207">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2207">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="16653-2208">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-2208">ACR</span></span>

* <span data-ttu-id="16653-2209">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2209">Added ACR Build commands</span></span>
* <span data-ttu-id="16653-2210">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2210">Improved resource not found error messages</span></span>
* <span data-ttu-id="16653-2211">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2211">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="16653-2212">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2212">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="16653-2213">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2213">Improved repository commands error messages</span></span>
* <span data-ttu-id="16653-2214">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-2214">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2215">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2215">ACS</span></span>

* <span data-ttu-id="16653-2216">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2216">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="16653-2217">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2217">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="16653-2218">AMS</span><span class="sxs-lookup"><span data-stu-id="16653-2218">AMS</span></span>

* <span data-ttu-id="16653-2219">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="16653-2219">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2220">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2220">Appservice</span></span>

* <span data-ttu-id="16653-2221">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2221">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="16653-2222">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2222">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="16653-2223">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2223">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="16653-2224">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2224">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="16653-2225">Batch AI</span><span class="sxs-lookup"><span data-stu-id="16653-2225">Batch AI</span></span>

* <span data-ttu-id="16653-2226">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2226">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="16653-2227">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="16653-2227">Cognitive Services</span></span>

* <span data-ttu-id="16653-2228">`cognitiveservices account create` の例の誤りを修正しました ([#5603](https://github.com/Azure/azure-cli/issues/5603))</span><span class="sxs-lookup"><span data-stu-id="16653-2228">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="16653-2229">従量課金</span><span class="sxs-lookup"><span data-stu-id="16653-2229">Consumption</span></span>

* <span data-ttu-id="16653-2230">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2230">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="16653-2231">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-2231">Container</span></span>

* <span data-ttu-id="16653-2232">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2232">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="16653-2233">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-2233">Cosmos DB</span></span>

* <span data-ttu-id="16653-2234">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="16653-2234">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="16653-2235">DMS</span><span class="sxs-lookup"><span data-stu-id="16653-2235">DMS</span></span>

* <span data-ttu-id="16653-2236">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2236">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="16653-2237">拡張機能</span><span class="sxs-lookup"><span data-stu-id="16653-2237">Extension</span></span>

* <span data-ttu-id="16653-2238">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2238">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="16653-2239">Interactive</span><span class="sxs-lookup"><span data-stu-id="16653-2239">Interactive</span></span>

* <span data-ttu-id="16653-2240">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-2240">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="16653-2241">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="16653-2241">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="16653-2242">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2242">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="16653-2243">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2243">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="16653-2244">ラボ</span><span class="sxs-lookup"><span data-stu-id="16653-2244">Lab</span></span>

* <span data-ttu-id="16653-2245">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2245">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="16653-2246">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2246">Network</span></span>

* <span data-ttu-id="16653-2247">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2247">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="16653-2248">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-2248">Profile</span></span>

* <span data-ttu-id="16653-2249">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2249">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="16653-2250">[重大な変更]`--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2250">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="16653-2251">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2251">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="16653-2252">Redis</span><span class="sxs-lookup"><span data-stu-id="16653-2252">Redis</span></span>

* <span data-ttu-id="16653-2253">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2253">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="16653-2254">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="16653-2254">Deprecated `redis list-all`.</span></span> <span data-ttu-id="16653-2255">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="16653-2255">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="16653-2256">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2256">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="16653-2257">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2257">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="16653-2258">Role</span><span class="sxs-lookup"><span data-stu-id="16653-2258">Role</span></span>

* <span data-ttu-id="16653-2259">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2259">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2260">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2260">Storage</span></span>

* <span data-ttu-id="16653-2261">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="16653-2261">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="16653-2262">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="16653-2262">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="16653-2263">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="16653-2263">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="16653-2264">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="16653-2264">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="16653-2265">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2265">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2266">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2266">VM</span></span>

* <span data-ttu-id="16653-2267">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2267">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="16653-2268">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2268">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="16653-2269">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="16653-2269">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="16653-2270">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2270">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="16653-2271">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2271">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="16653-2272">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2272">Added write accelerator support</span></span>
* <span data-ttu-id="16653-2273">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2273">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="16653-2274">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2274">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="16653-2275">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2275">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="16653-2276">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="16653-2276">April 10, 2018</span></span>

<span data-ttu-id="16653-2277">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="16653-2277">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="16653-2278">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-2278">ACR</span></span>

* <span data-ttu-id="16653-2279">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2279">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2280">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2280">ACS</span></span>

* <span data-ttu-id="16653-2281">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2281">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2282">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2282">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="16653-2284">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2284">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="16653-2285">BatchAI</span><span class="sxs-lookup"><span data-stu-id="16653-2285">BatchAI</span></span>

* <span data-ttu-id="16653-2286">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2286">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="16653-2287">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="16653-2287">Job level mounting</span></span>
  - <span data-ttu-id="16653-2288">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="16653-2288">Environment variables with secret values</span></span>
  - <span data-ttu-id="16653-2289">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="16653-2289">Performance counters settings</span></span>
  - <span data-ttu-id="16653-2290">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="16653-2290">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="16653-2291">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="16653-2291">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="16653-2292">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="16653-2292">Usage and limits reporting</span></span>
  - <span data-ttu-id="16653-2293">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="16653-2293">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="16653-2294">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="16653-2294">Support for custom images</span></span>
  - <span data-ttu-id="16653-2295">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2295">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="16653-2296">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="16653-2296">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="16653-2297">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="16653-2297">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="16653-2298">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="16653-2298">National clouds are supported</span></span>
* <span data-ttu-id="16653-2299">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2299">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="16653-2300">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2300">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="16653-2301">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2301">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="16653-2302">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2302">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="16653-2303">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="16653-2303">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="16653-2304">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="16653-2304">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="16653-2305">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2305">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="16653-2306">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2306">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="16653-2307">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="16653-2307">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="16653-2308">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2308">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="16653-2309">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="16653-2309">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="16653-2310">[重大な変更]`job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="16653-2310">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="16653-2311">[重大な変更]`cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2311">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="16653-2312">課金</span><span class="sxs-lookup"><span data-stu-id="16653-2312">Billing</span></span>

* <span data-ttu-id="16653-2313">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2313">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="16653-2314">従量課金</span><span class="sxs-lookup"><span data-stu-id="16653-2314">Consumption</span></span>

* <span data-ttu-id="16653-2315">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2315">Added `marketplace` commands</span></span>
* <span data-ttu-id="16653-2316">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2316">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="16653-2317">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2317">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="16653-2318">[重大な変更]`reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2318">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="16653-2319">[重大な変更]`reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2319">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="16653-2320">[重大な変更]`pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2320">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="16653-2321">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-2321">Container</span></span>

* <span data-ttu-id="16653-2322">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2322">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="16653-2323">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2323">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="16653-2324">拡張機能</span><span class="sxs-lookup"><span data-stu-id="16653-2324">Extension</span></span>

* <span data-ttu-id="16653-2325">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2325">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="16653-2326">Interactive</span><span class="sxs-lookup"><span data-stu-id="16653-2326">Interactive</span></span>

* <span data-ttu-id="16653-2327">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2327">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="16653-2328">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2328">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="16653-2329">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2329">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="16653-2330">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2330">Network</span></span>

* <span data-ttu-id="16653-2331">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2331">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="16653-2332">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2332">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="16653-2333">#4910</span><span class="sxs-lookup"><span data-stu-id="16653-2333">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="16653-2334">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2334">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="16653-2335">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="16653-2335">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="16653-2336">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2336">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="16653-2337">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2337">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="16653-2338">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2338">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="16653-2339">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-2339">Profile</span></span>

* <span data-ttu-id="16653-2340">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2340">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="16653-2341">[重大な変更]`--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2341">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="16653-2342">RDBMS</span><span class="sxs-lookup"><span data-stu-id="16653-2342">RDBMS</span></span>

* <span data-ttu-id="16653-2343">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2343">Added `georestore` command</span></span>
* <span data-ttu-id="16653-2344">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2344">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="16653-2345">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-2345">Resource</span></span>

* <span data-ttu-id="16653-2346">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2346">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="16653-2347">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2347">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="16653-2348">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-2348">SQL</span></span>

* <span data-ttu-id="16653-2349">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2349">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2350">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2350">Storage</span></span>

* <span data-ttu-id="16653-2351">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2351">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2352">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2352">VM</span></span>

* <span data-ttu-id="16653-2353">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2353">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="16653-2354">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2354">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="16653-2356">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2356">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="16653-2357">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2357">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="16653-2358">#5718</span><span class="sxs-lookup"><span data-stu-id="16653-2358">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="16653-2359">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2359">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="16653-2360">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="16653-2360">March 27, 2018</span></span>

<span data-ttu-id="16653-2361">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="16653-2361">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="16653-2362">コア</span><span class="sxs-lookup"><span data-stu-id="16653-2362">Core</span></span>

* <span data-ttu-id="16653-2363">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="16653-2363">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2364">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2364">ACS</span></span>

* <span data-ttu-id="16653-2365">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2365">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2366">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2366">Appservice</span></span>

* <span data-ttu-id="16653-2367">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2367">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="16653-2368">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2368">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="16653-2369">バックアップ</span><span class="sxs-lookup"><span data-stu-id="16653-2369">Backup</span></span>

* <span data-ttu-id="16653-2370">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2370">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="16653-2371">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="16653-2371">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="16653-2372">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2372">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="16653-2373">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2373">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="16653-2374">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-2374">Container</span></span>

* <span data-ttu-id="16653-2375">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2375">Added `container exec` command.</span></span> <span data-ttu-id="16653-2376">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="16653-2376">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="16653-2377">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="16653-2377">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="16653-2378">拡張機能</span><span class="sxs-lookup"><span data-stu-id="16653-2378">Extension</span></span>

* <span data-ttu-id="16653-2379">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2379">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="16653-2380">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2380">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="16653-2381">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2381">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="16653-2382">Interactive</span><span class="sxs-lookup"><span data-stu-id="16653-2382">Interactive</span></span>

* <span data-ttu-id="16653-2383">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2383">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="16653-2384">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2384">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="16653-2385">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="16653-2385">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="16653-2386">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="16653-2386">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="16653-2387">ラボ</span><span class="sxs-lookup"><span data-stu-id="16653-2387">Lab</span></span>

* <span data-ttu-id="16653-2388">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2388">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-2389">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-2389">Monitor</span></span>

* <span data-ttu-id="16653-2390">`--top`、`--orderby`、および `--namespace` のサポートを `metrics list` に追加しました ([#5785](https://github.com/Azure/azure-cli/issues/5785))</span><span class="sxs-lookup"><span data-stu-id="16653-2390">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="16653-2391">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="16653-2391">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="16653-2392">`--namespace` のサポートを `metrics list-definitions` に追加しました ([#5785](https://github.com/Azure/azure-cli/issues/5785))</span><span class="sxs-lookup"><span data-stu-id="16653-2392">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="16653-2393">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2393">Network</span></span>

* <span data-ttu-id="16653-2394">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2394">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="16653-2395">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-2395">Profile</span></span>

* <span data-ttu-id="16653-2396">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2396">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="16653-2397">RDBMS</span><span class="sxs-lookup"><span data-stu-id="16653-2397">RDBMS</span></span>

* <span data-ttu-id="16653-2398">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2398">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="16653-2399">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-2399">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="16653-2401">Role</span><span class="sxs-lookup"><span data-stu-id="16653-2401">Role</span></span>

* <span data-ttu-id="16653-2402">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2402">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="16653-2403">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2403">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="16653-2404">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2404">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="16653-2405">[重大な変更]`az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2405">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="16653-2406">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2406">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2407">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2407">Storage</span></span>

* <span data-ttu-id="16653-2408">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2408">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="16653-2409">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="16653-2409">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2410">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2410">VM</span></span>

* <span data-ttu-id="16653-2411">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2411">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="16653-2412">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2412">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="16653-2413">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2413">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="16653-2414">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2414">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="16653-2415">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="16653-2415">March 13, 2018</span></span>

<span data-ttu-id="16653-2416">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="16653-2416">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="16653-2417">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-2417">ACR</span></span>

* <span data-ttu-id="16653-2418">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2418">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="16653-2419">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2419">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="16653-2420">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2420">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2421">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2421">ACS</span></span>

* <span data-ttu-id="16653-2422">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2422">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="16653-2423">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2423">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="16653-2424">Advisor</span><span class="sxs-lookup"><span data-stu-id="16653-2424">Advisor</span></span>

* <span data-ttu-id="16653-2425">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2425">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="16653-2426">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2426">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="16653-2427">[重大な変更]`advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2427">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="16653-2428">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2428">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="16653-2429">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2429">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2430">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2430">Appservice</span></span>

* <span data-ttu-id="16653-2431">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2431">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="16653-2432">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2432">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="16653-2433">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="16653-2433">Eventhubs</span></span>

* <span data-ttu-id="16653-2434">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="16653-2434">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="16653-2435">拡張機能</span><span class="sxs-lookup"><span data-stu-id="16653-2435">Extension</span></span>

* <span data-ttu-id="16653-2436">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2436">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="16653-2437">Interactive</span><span class="sxs-lookup"><span data-stu-id="16653-2437">Interactive</span></span>

* <span data-ttu-id="16653-2438">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="16653-2438">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="16653-2439">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="16653-2439">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="16653-2440">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="16653-2440">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="16653-2441">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2441">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-2442">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-2442">Monitor</span></span>

* <span data-ttu-id="16653-2443">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2443">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="16653-2444">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2444">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="16653-2445">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2445">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="16653-2446">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2446">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="16653-2447">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2447">Network</span></span>

* <span data-ttu-id="16653-2448">[重大な変更]`route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2448">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="16653-2449">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2449">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="16653-2450">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2450">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="16653-2451">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2451">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="16653-2452">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-2452">Profile</span></span>

* <span data-ttu-id="16653-2453">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2453">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="16653-2454">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2454">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="16653-2455">RDBMS</span><span class="sxs-lookup"><span data-stu-id="16653-2455">RDBMS</span></span>

* <span data-ttu-id="16653-2456">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2456">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="16653-2457">Service Bus</span><span class="sxs-lookup"><span data-stu-id="16653-2457">Service Bus</span></span>

* <span data-ttu-id="16653-2458">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="16653-2458">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2459">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2459">Storage</span></span>

* <span data-ttu-id="16653-2460">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-2460">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="16653-2461">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="16653-2461">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2462">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2462">VM</span></span>

* <span data-ttu-id="16653-2463">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2463">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="16653-2464">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2464">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="16653-2465">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2465">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="16653-2466">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2466">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="16653-2467">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="16653-2467">February 27, 2018</span></span>

<span data-ttu-id="16653-2468">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="16653-2468">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="16653-2469">コア</span><span class="sxs-lookup"><span data-stu-id="16653-2469">Core</span></span>

* <span data-ttu-id="16653-2470">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="16653-2470">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="16653-2471">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2471">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="16653-2472">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2472">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2473">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2473">ACS</span></span>

* <span data-ttu-id="16653-2474">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2474">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="16653-2475">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="16653-2475">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="16653-2476">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2476">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="16653-2477">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2477">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2478">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2478">Appservice</span></span>

* <span data-ttu-id="16653-2479">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="16653-2479">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="16653-2480">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="16653-2480">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="16653-2481">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="16653-2481">Cognitive Services</span></span>

* <span data-ttu-id="16653-2482">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-2482">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="16653-2483">従量課金</span><span class="sxs-lookup"><span data-stu-id="16653-2483">Consumption</span></span>

* <span data-ttu-id="16653-2484">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2484">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="16653-2485">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-2485">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="16653-2486">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-2486">Container</span></span>

* <span data-ttu-id="16653-2487">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2487">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="16653-2488">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2488">Network</span></span>

* <span data-ttu-id="16653-2489">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="16653-2489">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="16653-2490">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-2490">Resource</span></span>

* <span data-ttu-id="16653-2491">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2491">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="16653-2492">Role</span><span class="sxs-lookup"><span data-stu-id="16653-2492">Role</span></span>

* <span data-ttu-id="16653-2493">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2493">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="16653-2494">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-2494">SQL</span></span>

* <span data-ttu-id="16653-2495">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2495">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2496">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2496">Storage</span></span>

* <span data-ttu-id="16653-2497">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2497">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2498">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2498">VM</span></span>

* <span data-ttu-id="16653-2499">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2499">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="16653-2500">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="16653-2500">February 13, 2018</span></span>

<span data-ttu-id="16653-2501">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="16653-2501">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="16653-2502">コア</span><span class="sxs-lookup"><span data-stu-id="16653-2502">Core</span></span>

* <span data-ttu-id="16653-2503">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2503">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2504">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2504">ACS</span></span>

* <span data-ttu-id="16653-2505">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2505">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="16653-2506">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2506">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="16653-2507">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2507">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="16653-2508">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-2508">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="16653-2509">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2509">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="16653-2510">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="16653-2510">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="16653-2511">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2511">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="16653-2512">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="16653-2512">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2513">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2513">Appservice</span></span>

* <span data-ttu-id="16653-2514">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2514">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="16653-2515">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2515">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="16653-2516">CDN</span><span class="sxs-lookup"><span data-stu-id="16653-2516">CDN</span></span>

* <span data-ttu-id="16653-2517">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2517">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="16653-2518">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-2518">Container</span></span>

* <span data-ttu-id="16653-2519">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2519">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="16653-2520">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2520">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="16653-2521">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-2521">CosmosDB</span></span>

* <span data-ttu-id="16653-2522">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2522">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="16653-2523">拡張機能</span><span class="sxs-lookup"><span data-stu-id="16653-2523">Extension</span></span>

* <span data-ttu-id="16653-2524">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2524">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="16653-2525">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2525">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="16653-2526">フィードバック</span><span class="sxs-lookup"><span data-stu-id="16653-2526">Feedback</span></span>

* <span data-ttu-id="16653-2527">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2527">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="16653-2528">Interactive</span><span class="sxs-lookup"><span data-stu-id="16653-2528">Interactive</span></span>

* <span data-ttu-id="16653-2529">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2529">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="16653-2530">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2530">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="16653-2531">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-2531">IoT</span></span>

* <span data-ttu-id="16653-2532">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2532">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="16653-2533">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2533">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="16653-2534">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2534">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="16653-2535">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2535">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-2536">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-2536">Monitor</span></span>

* <span data-ttu-id="16653-2537">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2537">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="16653-2538">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2538">Network</span></span>

* <span data-ttu-id="16653-2539">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2539">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="16653-2540">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-2540">Profile</span></span>

* <span data-ttu-id="16653-2541">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2541">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="16653-2542">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-2542">Resource</span></span>

* <span data-ttu-id="16653-2543">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2543">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="16653-2544">Role</span><span class="sxs-lookup"><span data-stu-id="16653-2544">Role</span></span>

* <span data-ttu-id="16653-2545">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2545">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="16653-2546">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-2546">SQL</span></span>

* <span data-ttu-id="16653-2547">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2547">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="16653-2548">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2548">Added `sql db rename`</span></span>
* <span data-ttu-id="16653-2549">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2549">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2550">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2550">Storage</span></span>

* <span data-ttu-id="16653-2551">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2551">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2552">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2552">VM</span></span>

* <span data-ttu-id="16653-2553">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2553">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="16653-2554">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2554">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="16653-2555">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="16653-2555">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="16653-2556">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="16653-2556">January 31, 2018</span></span>

<span data-ttu-id="16653-2557">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="16653-2557">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="16653-2558">コア</span><span class="sxs-lookup"><span data-stu-id="16653-2558">Core</span></span>

* <span data-ttu-id="16653-2559">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2559">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="16653-2560">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2560">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="16653-2561">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2561">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="16653-2562">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="16653-2562">Use `--verbose` to see</span></span>
* <span data-ttu-id="16653-2563">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="16653-2563">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2564">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2564">ACS</span></span>

* <span data-ttu-id="16653-2565">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="16653-2565">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="16653-2566">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="16653-2566">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2567">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2567">Appservice</span></span>

* <span data-ttu-id="16653-2568">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="16653-2568">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="16653-2569">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2569">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="16653-2570">CDN</span><span class="sxs-lookup"><span data-stu-id="16653-2570">CDN</span></span>

* <span data-ttu-id="16653-2571">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2571">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="16653-2572">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-2572">CosmosDB</span></span>

* <span data-ttu-id="16653-2573">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2573">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="16653-2574">Interactive</span><span class="sxs-lookup"><span data-stu-id="16653-2574">Interactive</span></span>

* <span data-ttu-id="16653-2575">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2575">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="16653-2576">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2576">Network</span></span>

* <span data-ttu-id="16653-2577">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2577">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="16653-2578">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2578">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="16653-2579">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2579">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="16653-2580">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2580">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="16653-2581">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2581">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="16653-2582">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2582">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="16653-2583">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2583">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="16653-2584">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2584">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="16653-2585">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2585">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="16653-2586">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="16653-2586">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="16653-2587">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-2587">Profile</span></span>

* <span data-ttu-id="16653-2588">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2588">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="16653-2589">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-2589">Resource</span></span>

* <span data-ttu-id="16653-2590">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2590">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2591">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2591">Storage</span></span>

* <span data-ttu-id="16653-2592">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2592">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="16653-2593">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2593">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="16653-2594">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2594">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="16653-2595">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2595">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="16653-2596">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2596">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2597">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2597">VM</span></span>

* <span data-ttu-id="16653-2598">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2598">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="16653-2599">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2599">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="16653-2600">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2600">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="16653-2601">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2601">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="16653-2602">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="16653-2602">January 17, 2018</span></span>

<span data-ttu-id="16653-2603">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="16653-2603">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="16653-2604">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-2604">ACR</span></span>

* <span data-ttu-id="16653-2605">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2605">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="16653-2606">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2606">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2607">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2607">ACS</span></span>

* <span data-ttu-id="16653-2608">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2608">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="16653-2609">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2609">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2610">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2610">Appservice</span></span>

* <span data-ttu-id="16653-2611">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2611">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="16653-2612">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2612">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="16653-2613">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2613">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="16653-2614">バックアップ</span><span class="sxs-lookup"><span data-stu-id="16653-2614">Backup</span></span>

* <span data-ttu-id="16653-2615">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2615">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="16653-2616">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2616">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="16653-2617">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2617">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="16653-2618">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2618">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="16653-2619">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2619">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="16653-2620">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-2620">Batch</span></span>

* <span data-ttu-id="16653-2621">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2621">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="16653-2622">クラウド</span><span class="sxs-lookup"><span data-stu-id="16653-2622">Cloud</span></span>

* <span data-ttu-id="16653-2623">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2623">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="16653-2624">従量課金</span><span class="sxs-lookup"><span data-stu-id="16653-2624">Consumption</span></span>

* <span data-ttu-id="16653-2625">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2625">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="16653-2626">Event Grid</span><span class="sxs-lookup"><span data-stu-id="16653-2626">Event Grid</span></span>

* <span data-ttu-id="16653-2627">[重大な変更]`az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="16653-2627">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="16653-2628">[重大な変更]`az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="16653-2628">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="16653-2629">[重大な変更]`eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2629">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="16653-2630">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="16653-2630">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="16653-2631">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2631">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="16653-2632">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2632">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="16653-2633">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2633">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="16653-2634">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2634">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="16653-2635">Interactive</span><span class="sxs-lookup"><span data-stu-id="16653-2635">Interactive</span></span>

* <span data-ttu-id="16653-2636">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="16653-2636">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="16653-2637">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2637">Fixed errors on startup</span></span>
* <span data-ttu-id="16653-2638">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2638">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="16653-2639">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-2639">IoT</span></span>

* <span data-ttu-id="16653-2640">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2640">Added support for device provisioning service</span></span>
* <span data-ttu-id="16653-2641">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2641">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="16653-2642">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2642">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-2643">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-2643">Monitor</span></span>

* <span data-ttu-id="16653-2644">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2644">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="16653-2645">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="16653-2645">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="16653-2646">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2646">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="16653-2647">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2647">Network</span></span>

* <span data-ttu-id="16653-2648">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2648">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="16653-2649">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2649">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="16653-2650">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-2650">Profile</span></span>

* <span data-ttu-id="16653-2651">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2651">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="16653-2652">Role</span><span class="sxs-lookup"><span data-stu-id="16653-2652">Role</span></span>

* <span data-ttu-id="16653-2653">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2653">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="16653-2654">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="16653-2654">Service Fabric</span></span>

* <span data-ttu-id="16653-2655">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2655">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="16653-2656">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2656">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2657">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2657">VM</span></span>

* <span data-ttu-id="16653-2658">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="16653-2658">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="16653-2659">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2659">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="16653-2660">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2660">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="16653-2661">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2661">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="16653-2662">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2662">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="16653-2663">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2663">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="16653-2664">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2664">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="16653-2665">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2665">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="16653-2666">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="16653-2666">December 19, 2017</span></span>

<span data-ttu-id="16653-2667">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="16653-2667">Version 2.0.23</span></span>

* <span data-ttu-id="16653-2668">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2668">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="16653-2669">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-2669">Container</span></span>

* <span data-ttu-id="16653-2670">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2670">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="16653-2671">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2671">Network</span></span>

* <span data-ttu-id="16653-2672">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2672">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="16653-2673">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2673">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2674">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2674">Storage</span></span>

* <span data-ttu-id="16653-2675">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2675">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2676">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2676">VM</span></span>

* <span data-ttu-id="16653-2677">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2677">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="16653-2678">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="16653-2678">December 5, 2017</span></span>

<span data-ttu-id="16653-2679">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="16653-2679">Version 2.0.22</span></span>

* <span data-ttu-id="16653-2680">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2680">Removed `az component` commands.</span></span> <span data-ttu-id="16653-2681">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="16653-2681">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="16653-2682">コア</span><span class="sxs-lookup"><span data-stu-id="16653-2682">Core</span></span>
* <span data-ttu-id="16653-2683">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2683">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="16653-2684">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2684">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2685">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2685">ACS</span></span>

* <span data-ttu-id="16653-2686">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2686">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="16653-2687">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2687">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="16653-2688">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2688">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="16653-2689">Advisor</span><span class="sxs-lookup"><span data-stu-id="16653-2689">Advisor</span></span>

* <span data-ttu-id="16653-2690">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="16653-2690">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2691">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2691">Appservice</span></span>

* <span data-ttu-id="16653-2692">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2692">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="16653-2693">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2693">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="16653-2694">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2694">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="16653-2695">従量課金</span><span class="sxs-lookup"><span data-stu-id="16653-2695">Consumption</span></span>

* <span data-ttu-id="16653-2696">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2696">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="16653-2697">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-2697">Container</span></span>

* <span data-ttu-id="16653-2698">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2698">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-2699">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-2699">Monitor</span></span>

* <span data-ttu-id="16653-2700">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2700">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="16653-2701">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-2701">Resource</span></span>

* <span data-ttu-id="16653-2702">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2702">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="16653-2703">Role</span><span class="sxs-lookup"><span data-stu-id="16653-2703">Role</span></span>

* <span data-ttu-id="16653-2704">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2704">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="16653-2705">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="16653-2705">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="16653-2706">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2706">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="16653-2707">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-2707">SQL</span></span>

* <span data-ttu-id="16653-2708">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2708">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="16653-2709">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2709">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2710">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2710">VM</span></span>

* <span data-ttu-id="16653-2711">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2711">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="16653-2712">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="16653-2712">November 14, 2017</span></span>

<span data-ttu-id="16653-2713">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="16653-2713">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="16653-2714">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-2714">ACR</span></span>

* <span data-ttu-id="16653-2715">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2715">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="16653-2716">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2716">ACS</span></span>

* <span data-ttu-id="16653-2717">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2717">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="16653-2718">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2718">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="16653-2719">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2719">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="16653-2720">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2720">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="16653-2721">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2721">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2722">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2722">Appservice</span></span>

* <span data-ttu-id="16653-2723">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2723">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="16653-2724">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2724">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="16653-2725">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2725">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="16653-2726">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-2726">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="16653-2727">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2727">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="16653-2728">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="16653-2728">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="16653-2729">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-2729">Batch</span></span>

* <span data-ttu-id="16653-2730">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2730">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="16653-2731">Batchai</span><span class="sxs-lookup"><span data-stu-id="16653-2731">Batchai</span></span>

* <span data-ttu-id="16653-2732">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2732">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="16653-2733">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2733">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="16653-2734">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2734">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="16653-2735">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2735">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="16653-2736">クラウド</span><span class="sxs-lookup"><span data-stu-id="16653-2736">Cloud</span></span>

* <span data-ttu-id="16653-2737">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2737">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="16653-2738">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-2738">Container</span></span>

* <span data-ttu-id="16653-2739">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2739">Added support to open multiple ports</span></span>
* <span data-ttu-id="16653-2740">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2740">Added container group restart policy</span></span>
* <span data-ttu-id="16653-2741">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2741">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="16653-2742">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-2742">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="16653-2743">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="16653-2743">Data Lake Analytics</span></span>

* <span data-ttu-id="16653-2744">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2744">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="16653-2745">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="16653-2745">Data Lake Store</span></span>

* <span data-ttu-id="16653-2746">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2746">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="16653-2747">拡張機能</span><span class="sxs-lookup"><span data-stu-id="16653-2747">Extension</span></span>

* <span data-ttu-id="16653-2748">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2748">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="16653-2749">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2749">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="16653-2750">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-2750">IoT</span></span>

* <span data-ttu-id="16653-2751">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2751">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-2752">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-2752">Monitor</span></span>

* <span data-ttu-id="16653-2753">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2753">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="16653-2754">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2754">Network</span></span>

* <span data-ttu-id="16653-2755">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2755">Added support for CAA DNS records</span></span>
* <span data-ttu-id="16653-2756">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2756">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="16653-2757">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2757">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="16653-2758">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2758">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="16653-2759">Reservations</span><span class="sxs-lookup"><span data-stu-id="16653-2759">Reservations</span></span>

* <span data-ttu-id="16653-2760">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="16653-2760">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="16653-2761">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-2761">Resource</span></span>

* <span data-ttu-id="16653-2762">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2762">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="16653-2763">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-2763">SQL</span></span>

* <span data-ttu-id="16653-2764">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2764">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2765">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2765">Storage</span></span>

* <span data-ttu-id="16653-2766">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2766">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="16653-2767">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2767">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="16653-2768">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2768">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="16653-2769">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2769">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="16653-2770">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2770">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="16653-2771">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2771">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="16653-2772">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2772">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2773">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2773">VM</span></span>

* <span data-ttu-id="16653-2774">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2774">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="16653-2775">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2775">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="16653-2776">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2776">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="16653-2777">`vm format-secret` から `vm secret format` への名称変更</span><span class="sxs-lookup"><span data-stu-id="16653-2777">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="16653-2778">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2778">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="16653-2779">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="16653-2779">October 24, 2017</span></span>

<span data-ttu-id="16653-2780">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="16653-2780">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="16653-2781">コア</span><span class="sxs-lookup"><span data-stu-id="16653-2781">Core</span></span>

* <span data-ttu-id="16653-2782">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-2782">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="16653-2783">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-2783">ACR</span></span>

* <span data-ttu-id="16653-2784">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-2784">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="16653-2785">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2785">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="16653-2786">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2786">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2787">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2787">ACS</span></span>

* <span data-ttu-id="16653-2788">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2788">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="16653-2789">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2789">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2790">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2790">Appservice</span></span>

* <span data-ttu-id="16653-2791">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2791">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="16653-2792">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="16653-2792">Component</span></span>

* <span data-ttu-id="16653-2793">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2793">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-2794">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-2794">Monitor</span></span>

* <span data-ttu-id="16653-2795">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2795">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="16653-2796">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-2796">Resource</span></span>

* <span data-ttu-id="16653-2797">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2797">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="16653-2798">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2798">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2799">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2799">VM</span></span>

* <span data-ttu-id="16653-2800">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2800">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="16653-2801">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="16653-2801">October 9, 2017</span></span>

<span data-ttu-id="16653-2802">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="16653-2802">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="16653-2803">コア</span><span class="sxs-lookup"><span data-stu-id="16653-2803">Core</span></span>

* <span data-ttu-id="16653-2804">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2804">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2805">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2805">Appservice</span></span>

* <span data-ttu-id="16653-2806">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2806">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="16653-2807">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-2807">Batch</span></span>

* <span data-ttu-id="16653-2808">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-2808">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="16653-2809">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-2809">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="16653-2810">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2810">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="16653-2811">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2811">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="16653-2812">Batchai</span><span class="sxs-lookup"><span data-stu-id="16653-2812">Batchai</span></span>

* <span data-ttu-id="16653-2813">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="16653-2813">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="16653-2814">KeyVault</span><span class="sxs-lookup"><span data-stu-id="16653-2814">Keyvault</span></span>

* <span data-ttu-id="16653-2815">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2815">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="16653-2816">(#4448)</span><span class="sxs-lookup"><span data-stu-id="16653-2816">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="16653-2817">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2817">Network</span></span>

* <span data-ttu-id="16653-2818">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2818">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="16653-2819">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-2819">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="16653-2820">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-2820">Resource</span></span>

* <span data-ttu-id="16653-2821">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2821">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="16653-2822">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2822">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="16653-2823">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2823">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="16653-2824">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2824">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="16653-2825">Sql</span><span class="sxs-lookup"><span data-stu-id="16653-2825">Sql</span></span>

* <span data-ttu-id="16653-2826">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2826">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="16653-2827">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="16653-2827">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="16653-2828">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="16653-2828">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2829">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2829">Storage</span></span>

* <span data-ttu-id="16653-2830">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2830">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2831">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2831">Vm</span></span>

* <span data-ttu-id="16653-2832">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2832">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="16653-2833">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2833">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="16653-2834">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2834">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="16653-2835">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2835">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="16653-2836">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2836">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="16653-2837">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="16653-2837">September 22, 2017</span></span>

<span data-ttu-id="16653-2838">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="16653-2838">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="16653-2839">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-2839">Resource</span></span>

* <span data-ttu-id="16653-2840">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2840">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="16653-2841">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2841">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="16653-2842">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2842">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="16653-2843">[重大な変更]`managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2843">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="16653-2844">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2844">Network</span></span>

* <span data-ttu-id="16653-2845">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2845">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="16653-2846">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2846">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="16653-2847">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2847">Added `asg` application security group commands</span></span>
* <span data-ttu-id="16653-2848">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2848">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="16653-2849">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2849">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="16653-2850">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2850">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="16653-2851">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2851">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2852">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2852">Storage</span></span>

* <span data-ttu-id="16653-2853">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2853">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="16653-2854">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="16653-2854">Eventgrid</span></span>

* <span data-ttu-id="16653-2855">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-2855">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="16653-2856">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-2856">SQL</span></span>

* <span data-ttu-id="16653-2857">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2857">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="16653-2858">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="16653-2858">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="16653-2859">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2859">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="16653-2860">KeyVault</span><span class="sxs-lookup"><span data-stu-id="16653-2860">Keyvault</span></span>

* <span data-ttu-id="16653-2861">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2861">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2862">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2862">VM</span></span>

* <span data-ttu-id="16653-2863">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2863">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="16653-2864">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2864">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="16653-2865">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2865">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="16653-2866">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2866">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="16653-2867">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2867">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="16653-2868">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2868">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2869">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2869">ACS</span></span>

* <span data-ttu-id="16653-2870">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2870">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2871">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2871">Appservice</span></span>

* <span data-ttu-id="16653-2872">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2872">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="16653-2873">バックアップ</span><span class="sxs-lookup"><span data-stu-id="16653-2873">Backup</span></span>

* <span data-ttu-id="16653-2874">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="16653-2874">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="16653-2875">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="16653-2875">September 11, 2017</span></span>

<span data-ttu-id="16653-2876">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="16653-2876">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="16653-2877">コア</span><span class="sxs-lookup"><span data-stu-id="16653-2877">Core</span></span>

* <span data-ttu-id="16653-2878">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2878">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="16653-2879">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2879">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2880">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2880">Acs</span></span>

* <span data-ttu-id="16653-2881">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2881">Added `acs list-locations` command</span></span>
* <span data-ttu-id="16653-2882">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="16653-2882">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2883">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2883">Appservice</span></span>

* <span data-ttu-id="16653-2884">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2884">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="16653-2885">CDN</span><span class="sxs-lookup"><span data-stu-id="16653-2885">CDN</span></span>

* <span data-ttu-id="16653-2886">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2886">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="16653-2887">拡張機能</span><span class="sxs-lookup"><span data-stu-id="16653-2887">Extension</span></span>

* <span data-ttu-id="16653-2888">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="16653-2888">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="16653-2889">KeyVault</span><span class="sxs-lookup"><span data-stu-id="16653-2889">Keyvault</span></span>

* <span data-ttu-id="16653-2890">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2890">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="16653-2891">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2891">Network</span></span>

* <span data-ttu-id="16653-2892">`vnet list-private-access-services` から `vnet list-endpoint-services` への名称変更</span><span class="sxs-lookup"><span data-stu-id="16653-2892">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="16653-2893">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2893">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="16653-2894">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2894">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="16653-2895">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2895">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="16653-2896">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2896">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="16653-2897">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-2897">Resource</span></span>

* <span data-ttu-id="16653-2898">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="16653-2898">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="16653-2899">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="16653-2899">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="16653-2900">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="16653-2900">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="16653-2901">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="16653-2901">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="16653-2902">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-2902">SQL</span></span>

* <span data-ttu-id="16653-2903">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2903">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2904">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2904">VM</span></span>

* <span data-ttu-id="16653-2905">固定:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="16653-2905">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="16653-2906">固定:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="16653-2906">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="16653-2907">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2907">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="16653-2908">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="16653-2908">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="16653-2909">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="16653-2909">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="16653-2910">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="16653-2910">August 31, 2017</span></span>

<span data-ttu-id="16653-2911">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="16653-2911">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="16653-2912">KeyVault</span><span class="sxs-lookup"><span data-stu-id="16653-2912">Keyvault</span></span>

* <span data-ttu-id="16653-2913">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2913">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="16653-2914">SF</span><span class="sxs-lookup"><span data-stu-id="16653-2914">Sf</span></span>

* <span data-ttu-id="16653-2915">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="16653-2915">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2916">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2916">Storage</span></span>

* <span data-ttu-id="16653-2917">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2917">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="16653-2918">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="16653-2918">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="16653-2919">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="16653-2919">August 28, 2017</span></span>

<span data-ttu-id="16653-2920">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="16653-2920">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="16653-2921">CLI</span><span class="sxs-lookup"><span data-stu-id="16653-2921">CLI</span></span>

* <span data-ttu-id="16653-2922">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2922">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2923">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2923">ACS</span></span>

* <span data-ttu-id="16653-2924">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2924">Corrected preview regions</span></span>
* <span data-ttu-id="16653-2925">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2925">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="16653-2926">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="16653-2926">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2927">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2927">Appservice</span></span>

* <span data-ttu-id="16653-2928">[重大な変更]`az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2928">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="16653-2929">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2929">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="16653-2930">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="16653-2930">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="16653-2931">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="16653-2931">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="16653-2932">固定:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="16653-2932">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="16653-2933">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-2933">IoT</span></span>

* <span data-ttu-id="16653-2934">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="16653-2934">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="16653-2935">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2935">Network</span></span>

* <span data-ttu-id="16653-2936">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2936">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="16653-2937">[重大な変更]`vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2937">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="16653-2938">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2938">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="16653-2939">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2939">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="16653-2940">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2940">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="16653-2941">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-2941">Profile</span></span>

* <span data-ttu-id="16653-2942">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="16653-2942">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="16653-2943">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="16653-2943">Service Fabric</span></span>

* <span data-ttu-id="16653-2944">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="16653-2944">Preview release</span></span>
* <span data-ttu-id="16653-2945">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="16653-2945">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="16653-2946">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2946">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="16653-2947">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2947">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2948">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2948">Storage</span></span>

* <span data-ttu-id="16653-2949">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2949">Enabled setting blob tier</span></span>
* <span data-ttu-id="16653-2950">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2950">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="16653-2951">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2951">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="16653-2952">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2952">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="16653-2953">[重大な変更]`az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-2953">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="16653-2954">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="16653-2954">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2955">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2955">VM</span></span>

* <span data-ttu-id="16653-2956">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2956">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="16653-2957">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-2957">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="16653-2958">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-2958">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="16653-2959">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2959">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="16653-2960">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2960">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="16653-2961">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2961">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="16653-2962">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="16653-2962">August 15, 2017</span></span>

<span data-ttu-id="16653-2963">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="16653-2963">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2964">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2964">ACS</span></span>

* <span data-ttu-id="16653-2965">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2965">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-2966">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-2966">Appservice</span></span>

* <span data-ttu-id="16653-2967">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2967">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="16653-2968">Event Grid</span><span class="sxs-lookup"><span data-stu-id="16653-2968">Event Grid</span></span>

* <span data-ttu-id="16653-2969">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2969">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="16653-2970">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="16653-2970">August 11, 2017</span></span>

<span data-ttu-id="16653-2971">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="16653-2971">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="16653-2972">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-2972">ACS</span></span>

* <span data-ttu-id="16653-2973">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2973">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="16653-2974">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-2974">Batch</span></span>

* <span data-ttu-id="16653-2975">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="16653-2975">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="16653-2976">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2976">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="16653-2977">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2977">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="16653-2978">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-2978">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="16653-2979">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-2979">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="16653-2980">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2980">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="16653-2981">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="16653-2981">Component</span></span>

* <span data-ttu-id="16653-2982">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2982">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="16653-2983">コンテナー</span><span class="sxs-lookup"><span data-stu-id="16653-2983">Container</span></span>

* <span data-ttu-id="16653-2984">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2984">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="16653-2985">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="16653-2985">Data Lake Store</span></span>

* <span data-ttu-id="16653-2986">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="16653-2986">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="16653-2987">Event Grid</span><span class="sxs-lookup"><span data-stu-id="16653-2987">Event Grid</span></span>

* <span data-ttu-id="16653-2988">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="16653-2988">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="16653-2989">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-2989">Network</span></span>

* <span data-ttu-id="16653-2990">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2990">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="16653-2991">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2991">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="16653-2992">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2992">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="16653-2993">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-2993">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="16653-2994">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-2994">Profile</span></span>

* <span data-ttu-id="16653-2995">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-2995">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="16653-2996">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-2996">Storage</span></span>

* <span data-ttu-id="16653-2997">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="16653-2997">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="16653-2998">VM</span><span class="sxs-lookup"><span data-stu-id="16653-2998">VM</span></span>

* <span data-ttu-id="16653-2999">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="16653-2999">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="16653-3000">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="16653-3000">Exposed `list-skus` command</span></span>
* <span data-ttu-id="16653-3001">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-3001">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="16653-3002">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="16653-3002">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="16653-3003">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-3003">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="16653-3004">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="16653-3004">July 28, 2017</span></span>

<span data-ttu-id="16653-3005">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="16653-3005">Version 2.0.12</span></span>

* <span data-ttu-id="16653-3006">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3006">Added container commands</span></span>
* <span data-ttu-id="16653-3007">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3007">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="16653-3008">コア</span><span class="sxs-lookup"><span data-stu-id="16653-3008">Core</span></span>

* <span data-ttu-id="16653-3009">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="16653-3009">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="16653-3010">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3010">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="16653-3011">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="16653-3011">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="16653-3012">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="16653-3012">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="16653-3013">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="16653-3013">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="16653-3014">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="16653-3014">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="16653-3015">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="16653-3015">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="16653-3016">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="16653-3016">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="16653-3017">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="16653-3017">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="16653-3018">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="16653-3018">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="16653-3019">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="16653-3019">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="16653-3020">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="16653-3020">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="16653-3021">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="16653-3021">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="16653-3022">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="16653-3022">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="16653-3023">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-3023">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="16653-3024">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="16653-3024">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="16653-3025">ACR</span><span class="sxs-lookup"><span data-stu-id="16653-3025">ACR</span></span>

* <span data-ttu-id="16653-3026">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3026">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="16653-3027">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-3027">Support SKU update for managed registries</span></span>
* <span data-ttu-id="16653-3028">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3028">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="16653-3029">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3029">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="16653-3030">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3030">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="16653-3031">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3031">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="16653-3032">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-3032">ACS</span></span>

* <span data-ttu-id="16653-3033">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-3033">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-3034">Appservice</span><span class="sxs-lookup"><span data-stu-id="16653-3034">Appservice</span></span>

* <span data-ttu-id="16653-3035">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3035">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="16653-3036">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-3036">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="16653-3037">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="16653-3037">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="16653-3038">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="16653-3038">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="16653-3039">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="16653-3039">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="16653-3040">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="16653-3040">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="16653-3041">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="16653-3041">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="16653-3042">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="16653-3042">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="16653-3043">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="16653-3043">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="16653-3044">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="16653-3044">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="16653-3045">Batch</span><span class="sxs-lookup"><span data-stu-id="16653-3045">Batch</span></span>

* <span data-ttu-id="16653-3046">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="16653-3046">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="16653-3047">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-3047">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="16653-3048">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3048">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="16653-3049">CDN</span><span class="sxs-lookup"><span data-stu-id="16653-3049">CDN</span></span>

* <span data-ttu-id="16653-3050">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-3050">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="16653-3051">クラウド</span><span class="sxs-lookup"><span data-stu-id="16653-3051">Cloud</span></span>

* <span data-ttu-id="16653-3052">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="16653-3052">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="16653-3053">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="16653-3053">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="16653-3054">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-3054">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="16653-3055">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="16653-3055">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="16653-3056">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="16653-3056">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="16653-3057">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-3057">CosmosDB</span></span>

* <span data-ttu-id="16653-3058">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3058">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="16653-3059">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3059">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="16653-3060">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="16653-3060">Data Lake Analytics</span></span>

* <span data-ttu-id="16653-3061">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3061">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="16653-3062">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3062">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="16653-3063">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3063">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="16653-3064">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="16653-3064">Data Lake Store</span></span>

* <span data-ttu-id="16653-3065">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3065">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="16653-3066">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="16653-3066">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="16653-3067">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-3067">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="16653-3068">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="16653-3068">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="16653-3069">Interactive</span><span class="sxs-lookup"><span data-stu-id="16653-3069">Interactive</span></span>

* <span data-ttu-id="16653-3070">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="16653-3070">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="16653-3071">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="16653-3071">Increased test coverage</span></span>
* <span data-ttu-id="16653-3072">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="16653-3072">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="16653-3073">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="16653-3073">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="16653-3074">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="16653-3074">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="16653-3075">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="16653-3075">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="16653-3076">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="16653-3076">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="16653-3077">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3077">Added `--progress` flag</span></span>
* <span data-ttu-id="16653-3078">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-3078">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="16653-3079">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="16653-3079">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="16653-3080">IoT</span><span class="sxs-lookup"><span data-stu-id="16653-3080">IoT</span></span>

* <span data-ttu-id="16653-3081">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="16653-3081">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="16653-3082">(#3934)</span><span class="sxs-lookup"><span data-stu-id="16653-3082">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="16653-3083">Key Vault</span><span class="sxs-lookup"><span data-stu-id="16653-3083">Key vault</span></span>

* <span data-ttu-id="16653-3084">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="16653-3084">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="16653-3085">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="16653-3085">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="16653-3086">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="16653-3086">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="16653-3087">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="16653-3087">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="16653-3088">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="16653-3088">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="16653-3089">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="16653-3089">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="16653-3090">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="16653-3090">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="16653-3091">(#3307)</span><span class="sxs-lookup"><span data-stu-id="16653-3091">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="16653-3092">ラボ</span><span class="sxs-lookup"><span data-stu-id="16653-3092">Lab</span></span>

* <span data-ttu-id="16653-3093">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3093">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="16653-3094">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3094">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-3095">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-3095">Monitor</span></span>

* <span data-ttu-id="16653-3096">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="16653-3096">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="16653-3097">`monitor alert-rule-incidents list` から `monitor alert list-incidents` への名称変更</span><span class="sxs-lookup"><span data-stu-id="16653-3097">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="16653-3098">`monitor alert-rule-incidents show` から `monitor alert show-incident` への名称変更</span><span class="sxs-lookup"><span data-stu-id="16653-3098">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="16653-3099">`monitor metric-defintions list` から `monitor metrics list-definitions` への名称変更</span><span class="sxs-lookup"><span data-stu-id="16653-3099">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="16653-3100">`monitor alert-rules` から `monitor alert` への名称変更</span><span class="sxs-lookup"><span data-stu-id="16653-3100">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="16653-3101">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="16653-3101">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="16653-3102">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="16653-3102">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="16653-3103">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="16653-3103">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="16653-3104">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="16653-3104">`location` no longer required</span></span>
  * <span data-ttu-id="16653-3105">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="16653-3105">Add name and ID support for target</span></span>
  * <span data-ttu-id="16653-3106">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="16653-3106">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="16653-3107">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="16653-3107">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="16653-3108">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3108">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="16653-3109">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="16653-3109">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="16653-3110">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-3110">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="16653-3111">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3111">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="16653-3112">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-3112">Network</span></span>

* <span data-ttu-id="16653-3113">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3113">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="16653-3114">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3114">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="16653-3115">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3115">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="16653-3116">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3116">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="16653-3117">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3117">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="16653-3118">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3118">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="16653-3119">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3119">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="16653-3120">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3120">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="16653-3121">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3121">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="16653-3122">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3122">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="16653-3123">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3123">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="16653-3124">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3124">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="16653-3125">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3125">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="16653-3126">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3126">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="16653-3127">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3127">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="16653-3128">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-3128">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="16653-3129">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3129">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="16653-3130">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3130">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="16653-3131">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3131">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="16653-3132">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3132">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="16653-3133">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3133">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="16653-3134">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3134">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="16653-3135">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-3135">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="16653-3136">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="16653-3136">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="16653-3137">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="16653-3137">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="16653-3138">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="16653-3138">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="16653-3139">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="16653-3139">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="16653-3140">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-3140">Profile</span></span>

* <span data-ttu-id="16653-3141">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-3141">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="16653-3142">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-3142">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="16653-3143">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="16653-3143">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="16653-3144">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3144">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="16653-3145">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-3145">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="16653-3146">RDBMS</span><span class="sxs-lookup"><span data-stu-id="16653-3146">RDBMS</span></span>

* <span data-ttu-id="16653-3147">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="16653-3147">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="16653-3148">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="16653-3148">Fixed `%s` not processed because of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="16653-3149">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="16653-3149">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="16653-3150">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="16653-3150">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="16653-3151">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-3151">Resource</span></span>

* <span data-ttu-id="16653-3152">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-3152">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="16653-3153">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="16653-3153">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="16653-3154">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3154">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="16653-3155">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-3155">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="16653-3156">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="16653-3156">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="16653-3157">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3157">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="16653-3158">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="16653-3158">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="16653-3159">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3159">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="16653-3160">Role</span><span class="sxs-lookup"><span data-stu-id="16653-3160">Role</span></span>

* <span data-ttu-id="16653-3161">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-3161">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="16653-3162">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="16653-3162">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="16653-3163">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="16653-3163">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="16653-3164">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="16653-3164">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="16653-3165">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3165">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="16653-3166">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="16653-3166">Service Fabric</span></span>
* <span data-ttu-id="16653-3167">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="16653-3167">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="16653-3168">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="16653-3168">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="16653-3169">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="16653-3169">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="16653-3170">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-3170">SQL</span></span>

* <span data-ttu-id="16653-3171">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-3171">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="16653-3172">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="16653-3172">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="16653-3173">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3173">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="16653-3174">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-3174">Storage</span></span>

* <span data-ttu-id="16653-3175">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="16653-3175">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="16653-3176">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="16653-3176">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="16653-3177">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="16653-3177">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="16653-3178">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="16653-3178">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="16653-3179">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="16653-3179">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="16653-3180">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="16653-3180">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="16653-3181">VM</span><span class="sxs-lookup"><span data-stu-id="16653-3181">VM</span></span>

* <span data-ttu-id="16653-3182">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-3182">Support configuring nsg</span></span>
* <span data-ttu-id="16653-3183">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3183">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="16653-3184">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="16653-3184">Support managed service identities</span></span>
* <span data-ttu-id="16653-3185">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3185">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="16653-3186">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="16653-3186">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="16653-3187">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="16653-3187">May 10, 2017</span></span>

<span data-ttu-id="16653-3188">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="16653-3188">Version 2.0.6</span></span>

* <span data-ttu-id="16653-3189">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="16653-3189">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="16653-3190">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3190">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="16653-3191">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3191">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="16653-3192">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3192">Include Cognitive Services module</span></span>
* <span data-ttu-id="16653-3193">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3193">Include Service Fabric module</span></span>
* <span data-ttu-id="16653-3194">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="16653-3194">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="16653-3195">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3195">Add support for CDN commands</span></span>
* <span data-ttu-id="16653-3196">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="16653-3196">Remove Container module</span></span>
* <span data-ttu-id="16653-3197">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="16653-3197">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="16653-3198">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="16653-3198">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="16653-3199">コア</span><span class="sxs-lookup"><span data-stu-id="16653-3199">Core</span></span>

* <span data-ttu-id="16653-3200">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="16653-3200">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="16653-3201">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="16653-3201">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="16653-3202">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="16653-3202">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="16653-3203">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="16653-3203">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="16653-3204">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="16653-3204">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="16653-3205">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="16653-3205">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="16653-3206">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="16653-3206">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="16653-3207">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="16653-3207">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="16653-3208">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="16653-3208">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="16653-3209">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="16653-3209">core: Improved performance</span></span>
* <span data-ttu-id="16653-3210">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="16653-3210">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="16653-3211">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="16653-3211">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="16653-3212">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-3212">ACS</span></span>

* <span data-ttu-id="16653-3213">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="16653-3213">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="16653-3214">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="16653-3214">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="16653-3215">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="16653-3215">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="16653-3216">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="16653-3216">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-3217">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-3217">AppService</span></span>

* <span data-ttu-id="16653-3218">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3218">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="16653-3219">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3219">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="16653-3220">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="16653-3220">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="16653-3221">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="16653-3221">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="16653-3222">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="16653-3222">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="16653-3223">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="16653-3223">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="16653-3224">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="16653-3224">support slot swap with preview</span></span>
* <span data-ttu-id="16653-3225">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="16653-3225">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="16653-3226">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="16653-3226">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="16653-3227">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="16653-3227">CosmosDB</span></span>

* <span data-ttu-id="16653-3228">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="16653-3228">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="16653-3229">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3229">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="16653-3230">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3230">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="16653-3231">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3231">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="16653-3232">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="16653-3232">Data Lake Analytics</span></span>

* <span data-ttu-id="16653-3233">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="16653-3233">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="16653-3234">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="16653-3234">Add support for new catalog item type: package.</span></span> <span data-ttu-id="16653-3235">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="16653-3235">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="16653-3236">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="16653-3236">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="16653-3237">テーブル</span><span class="sxs-lookup"><span data-stu-id="16653-3237">Table</span></span>
  * <span data-ttu-id="16653-3238">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="16653-3238">Table valued function</span></span>
  * <span data-ttu-id="16653-3239">表示</span><span class="sxs-lookup"><span data-stu-id="16653-3239">View</span></span>
  * <span data-ttu-id="16653-3240">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="16653-3240">Table Statistics.</span></span> <span data-ttu-id="16653-3241">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="16653-3241">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="16653-3242">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="16653-3242">Data Lake Store</span></span>

* <span data-ttu-id="16653-3243">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="16653-3243">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="16653-3244">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="16653-3244">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="16653-3245">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="16653-3245">missed help for access show.</span></span> <span data-ttu-id="16653-3246">追加しました</span><span class="sxs-lookup"><span data-stu-id="16653-3246">adding it.</span></span> <span data-ttu-id="16653-3247">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="16653-3247">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="16653-3248">Find</span><span class="sxs-lookup"><span data-stu-id="16653-3248">Find</span></span>

* <span data-ttu-id="16653-3249">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="16653-3249">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="16653-3250">KeyVault</span><span class="sxs-lookup"><span data-stu-id="16653-3250">KeyVault</span></span>

* <span data-ttu-id="16653-3251">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="16653-3251">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="16653-3252">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="16653-3252">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="16653-3253">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="16653-3253">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="16653-3254">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="16653-3254">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="16653-3255">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="16653-3255">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="16653-3256">ラボ</span><span class="sxs-lookup"><span data-stu-id="16653-3256">Lab</span></span>

* <span data-ttu-id="16653-3257">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3257">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="16653-3258">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3258">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="16653-3259">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3259">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="16653-3260">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3260">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="16653-3261">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3261">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="16653-3262">モニター</span><span class="sxs-lookup"><span data-stu-id="16653-3262">Monitor</span></span>

* <span data-ttu-id="16653-3263">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="16653-3263">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="16653-3264">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="16653-3264">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="16653-3265">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-3265">Network</span></span>

* <span data-ttu-id="16653-3266">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3266">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="16653-3267">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3267">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="16653-3268">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3268">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="16653-3269">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3269">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="16653-3270">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3270">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="16653-3271">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3271">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="16653-3272">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3272">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="16653-3273">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3273">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="16653-3274">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="16653-3274">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="16653-3275">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3275">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="16653-3276">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="16653-3276">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="16653-3277">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="16653-3277">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="16653-3278">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="16653-3278">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="16653-3279">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="16653-3279">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="16653-3280">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="16653-3280">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="16653-3281">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3281">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="16653-3282">プロファイル</span><span class="sxs-lookup"><span data-stu-id="16653-3282">Profile</span></span>

* <span data-ttu-id="16653-3283">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="16653-3283">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="16653-3284">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="16653-3284">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="16653-3285">Redis</span><span class="sxs-lookup"><span data-stu-id="16653-3285">Redis</span></span>

* <span data-ttu-id="16653-3286">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3286">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="16653-3287">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="16653-3287">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="16653-3288">リソース</span><span class="sxs-lookup"><span data-stu-id="16653-3288">Resource</span></span>

* <span data-ttu-id="16653-3289">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="16653-3289">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="16653-3290">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="16653-3290">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="16653-3291">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="16653-3291">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="16653-3292">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="16653-3292">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="16653-3293">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="16653-3293">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="16653-3294">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3294">Add docs for az lock update.</span></span> <span data-ttu-id="16653-3295">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="16653-3295">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="16653-3296">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="16653-3296">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="16653-3297">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="16653-3297">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="16653-3298">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="16653-3298">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="16653-3299">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="16653-3299">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="16653-3300">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="16653-3300">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="16653-3301">Role</span><span class="sxs-lookup"><span data-stu-id="16653-3301">Role</span></span>

* <span data-ttu-id="16653-3302">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="16653-3302">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="16653-3303">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="16653-3303">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="16653-3304">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="16653-3304">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="16653-3305">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="16653-3305">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="16653-3306">SQL</span><span class="sxs-lookup"><span data-stu-id="16653-3306">SQL</span></span>

* <span data-ttu-id="16653-3307">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="16653-3307">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="16653-3308">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="16653-3308">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="16653-3309">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-3309">Storage</span></span>

* <span data-ttu-id="16653-3310">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="16653-3310">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="16653-3311">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3311">Add support for incremental blob copy</span></span>
* <span data-ttu-id="16653-3312">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="16653-3312">Add support for large block blob upload</span></span>
* <span data-ttu-id="16653-3313">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="16653-3313">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="16653-3314">VM</span><span class="sxs-lookup"><span data-stu-id="16653-3314">VM</span></span>

* <span data-ttu-id="16653-3315">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="16653-3315">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="16653-3316">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="16653-3316">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="16653-3317">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="16653-3317">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="16653-3318">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="16653-3318">az vm/vmss disk</span></span>
  3. <span data-ttu-id="16653-3319">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="16653-3319">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="16653-3320">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="16653-3320">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="16653-3321">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="16653-3321">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="16653-3322">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="16653-3322">April 3, 2017</span></span>

<span data-ttu-id="16653-3323">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="16653-3323">Version 2.0.2</span></span>

<span data-ttu-id="16653-3324">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="16653-3324">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="16653-3325">コア</span><span class="sxs-lookup"><span data-stu-id="16653-3325">Core</span></span>

* <span data-ttu-id="16653-3326">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="16653-3326">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="16653-3327">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="16653-3327">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="16653-3328">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="16653-3328">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="16653-3329">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="16653-3329">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="16653-3330">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="16653-3330">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="16653-3331">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="16653-3331">Add prompting for missing template parameters.</span></span> <span data-ttu-id="16653-3332">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="16653-3332">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="16653-3333">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="16653-3333">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="16653-3334">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="16653-3334">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="16653-3335">ACS</span><span class="sxs-lookup"><span data-stu-id="16653-3335">ACS</span></span>

* <span data-ttu-id="16653-3336">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="16653-3336">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="16653-3337">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="16653-3337">Add support for ssh key password prompting.</span></span> <span data-ttu-id="16653-3338">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="16653-3338">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="16653-3339">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="16653-3339">Add support for windows clusters.</span></span> <span data-ttu-id="16653-3340">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="16653-3340">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="16653-3341">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="16653-3341">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="16653-3342">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="16653-3342">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="16653-3343">AppService</span><span class="sxs-lookup"><span data-stu-id="16653-3343">AppService</span></span>

* <span data-ttu-id="16653-3344">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="16653-3344">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="16653-3345">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="16653-3345">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="16653-3346">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="16653-3346">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="16653-3347">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="16653-3347">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="16653-3348">DataLake</span><span class="sxs-lookup"><span data-stu-id="16653-3348">DataLake</span></span>

* <span data-ttu-id="16653-3349">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="16653-3349">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="16653-3350">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="16653-3350">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="16653-3351">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="16653-3351">DocuemntDB</span></span>

* <span data-ttu-id="16653-3352">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="16653-3352">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="16653-3353">VM</span><span class="sxs-lookup"><span data-stu-id="16653-3353">VM</span></span>

* <span data-ttu-id="16653-3354">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="16653-3354">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="16653-3355">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="16653-3355">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="16653-3356">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="16653-3356">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="16653-3357">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="16653-3357">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="16653-3358">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="16653-3358">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="16653-3359">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="16653-3359">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="16653-3360">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="16653-3360">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="16653-3361">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="16653-3361">February 27, 2017</span></span>

<span data-ttu-id="16653-3362">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="16653-3362">Version 2.0.0</span></span>

<span data-ttu-id="16653-3363">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="16653-3363">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="16653-3364">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="16653-3364">Container Service (acs)</span></span>
- <span data-ttu-id="16653-3365">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="16653-3365">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="16653-3366">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="16653-3366">Networking</span></span>
- <span data-ttu-id="16653-3367">ストレージ</span><span class="sxs-lookup"><span data-stu-id="16653-3367">Storage</span></span>

<span data-ttu-id="16653-3368">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="16653-3368">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="16653-3369">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="16653-3369">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="16653-3370">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="16653-3370">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="16653-3371">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="16653-3371">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="16653-3372">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="16653-3372">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="16653-3373">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="16653-3373">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="16653-3374">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="16653-3374">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="16653-3375">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="16653-3375">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="16653-3376">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="16653-3376">Provide feedback from the command line with the `az feedback` command</span></span>

