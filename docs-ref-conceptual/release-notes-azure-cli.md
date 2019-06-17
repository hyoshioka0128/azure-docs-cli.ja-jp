---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 06/05/2019
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: b79d76480c3e6619427d6a7e3960f53b691889cc
ms.sourcegitcommit: 6aca5a788b9731e6cbeeb497c83a9197ebb7d36e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/06/2019
ms.locfileid: "66750238"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="71cfe-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="71cfe-103">Azure CLI release notes</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="71cfe-104">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-104">June 4, 2019</span></span>

<span data-ttu-id="71cfe-105">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="71cfe-105">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-106">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-106">Core</span></span>
* <span data-ttu-id="71cfe-107">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-107">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-108">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-108">ACR</span></span>
* <span data-ttu-id="71cfe-109">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-109">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-110">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-110">ACS</span></span>
* <span data-ttu-id="71cfe-111">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-111">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="71cfe-112">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-112">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="71cfe-113">Batch</span><span class="sxs-lookup"><span data-stu-id="71cfe-113">Batch</span></span>
* <span data-ttu-id="71cfe-114">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-114">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="71cfe-115">IoT</span><span class="sxs-lookup"><span data-stu-id="71cfe-115">IoT</span></span>
* <span data-ttu-id="71cfe-116">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-116">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-117">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-117">Network</span></span>
* <span data-ttu-id="71cfe-118">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-118">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="71cfe-119">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-119">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="71cfe-120">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-120">Resource</span></span>
* <span data-ttu-id="71cfe-121">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-121">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-122">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-122">Role</span></span>
* <span data-ttu-id="71cfe-123">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-123">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="71cfe-124">Compute</span><span class="sxs-lookup"><span data-stu-id="71cfe-124">Compute</span></span>
* <span data-ttu-id="71cfe-125">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-125">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="71cfe-126">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-126">May 21, 2019</span></span>

<span data-ttu-id="71cfe-127">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="71cfe-127">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-128">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-128">Core</span></span>
* <span data-ttu-id="71cfe-129">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-129">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="71cfe-130">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-130">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="71cfe-131">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-131">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-132">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-132">ACR</span></span>
* <span data-ttu-id="71cfe-133">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-133">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-134">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-134">ACS</span></span>
* <span data-ttu-id="71cfe-135">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-135">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-136">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-136">AppService</span></span>
* <span data-ttu-id="71cfe-137">[非推奨] `functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-137">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="71cfe-138">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-138">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="71cfe-139">[破壊的変更] `--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="71cfe-139">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="71cfe-140">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-140">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="71cfe-141">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-141">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="71cfe-142">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-142">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="71cfe-143">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-143">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="71cfe-144">BotService</span><span class="sxs-lookup"><span data-stu-id="71cfe-144">BotService</span></span>
* <span data-ttu-id="71cfe-145">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-145">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="71cfe-146">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-146">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="71cfe-147">消費</span><span class="sxs-lookup"><span data-stu-id="71cfe-147">Consumption</span></span>
* <span data-ttu-id="71cfe-148">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-148">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="71cfe-149">IoT</span><span class="sxs-lookup"><span data-stu-id="71cfe-149">IoT</span></span>
* <span data-ttu-id="71cfe-150">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-150">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-151">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-151">Network</span></span>
* [破壊的変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="71cfe-153">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-153">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="71cfe-154">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-154">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="71cfe-155">RDBMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-155">RDBMS</span></span>
* <span data-ttu-id="71cfe-156">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-156">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="71cfe-157">RBAC</span><span class="sxs-lookup"><span data-stu-id="71cfe-157">RBAC</span></span>
* <span data-ttu-id="71cfe-158">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-158">Added support for mangement group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-159">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-159">Storage</span></span>
* <span data-ttu-id="71cfe-160">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="71cfe-160">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="71cfe-161">Compute</span><span class="sxs-lookup"><span data-stu-id="71cfe-161">Compute</span></span>
* <span data-ttu-id="71cfe-162">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-162">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="71cfe-163">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-163">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="71cfe-164">__メモ__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-164">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="71cfe-165">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-165">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="71cfe-166">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-166">May 6, 2019</span></span>

<span data-ttu-id="71cfe-167">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="71cfe-167">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-168">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-168">ACS</span></span>
* <span data-ttu-id="71cfe-169">[破壊的変更] `--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-169">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="71cfe-170">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-170">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="71cfe-171">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-171">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="71cfe-172">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-172">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-173">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-173">Appservice</span></span>
* <span data-ttu-id="71cfe-174">[非推奨] `functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-174">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="71cfe-175">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-175">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="71cfe-176">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-176">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="71cfe-177">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-177">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="71cfe-178">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-178">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="71cfe-179">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-179">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="71cfe-180">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-180">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="71cfe-181">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-181">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="71cfe-182">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-182">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="71cfe-183">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-183">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="71cfe-184">Batch</span><span class="sxs-lookup"><span data-stu-id="71cfe-184">Batch</span></span>
* <span data-ttu-id="71cfe-185">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-185">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="71cfe-186">Botservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-186">Botservice</span></span>
* <span data-ttu-id="71cfe-187">[破壊的変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="71cfe-187">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="71cfe-188">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-188">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="71cfe-189">[破壊的変更] `--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-189">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="71cfe-190">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="71cfe-190">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="71cfe-191">[破壊的変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-191">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="71cfe-192">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-192">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="71cfe-193">[破壊的変更] `bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-193">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="71cfe-194">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-194">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="71cfe-195">[破壊的変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-195">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="71cfe-196">[破壊的変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-196">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="71cfe-197">[破壊的変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-197">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="71cfe-198">[破壊的変更] `Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-198">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="71cfe-199">[破壊的変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-199">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="71cfe-200">[破壊的変更] `SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-200">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="71cfe-201">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="71cfe-201">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="71cfe-202">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-202">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="71cfe-203">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-203">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="71cfe-204">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-204">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="71cfe-205">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-205">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="71cfe-206">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-206">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="71cfe-207">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-207">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="71cfe-208">構成</span><span class="sxs-lookup"><span data-stu-id="71cfe-208">Configure</span></span>
* <span data-ttu-id="71cfe-209">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-209">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="71cfe-210">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="71cfe-210">Eventhubs</span></span>
* <span data-ttu-id="71cfe-211">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-211">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="71cfe-212">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-212">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-213">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-213">Network</span></span>
* <span data-ttu-id="71cfe-214">[破壊的変更] `vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="71cfe-214">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="71cfe-215">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="71cfe-215">Policy Insights</span></span>
* <span data-ttu-id="71cfe-216">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-216">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-217">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-217">Role</span></span>
* <span data-ttu-id="71cfe-218">[非推奨] `create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-218">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="71cfe-219">Service Bus</span><span class="sxs-lookup"><span data-stu-id="71cfe-219">Service Bus</span></span>
* <span data-ttu-id="71cfe-220">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-220">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="71cfe-221">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-221">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="71cfe-222">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-222">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-223">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-223">SQL</span></span>
* <span data-ttu-id="71cfe-224">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-224">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-225">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-225">VM</span></span>
* <span data-ttu-id="71cfe-226">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-226">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="71cfe-227">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-227">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="71cfe-228">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-228">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="71cfe-229">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-229">Added new `ppg` command group for manging Proximity Placement Groups</span></span>
* <span data-ttu-id="71cfe-230">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-230">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="71cfe-231">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-231">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="71cfe-232">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-232">April 23, 2019</span></span>

<span data-ttu-id="71cfe-233">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="71cfe-233">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-234">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-234">ACS</span></span>
* <span data-ttu-id="71cfe-235">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-235">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="71cfe-236">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-236">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="71cfe-237">AMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-237">AMS</span></span>
* <span data-ttu-id="71cfe-238">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-238">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-239">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-239">AppService</span></span>
* <span data-ttu-id="71cfe-240">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-240">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="71cfe-241">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-241">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="71cfe-242">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-242">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="71cfe-243">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-243">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="71cfe-244">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-244">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="71cfe-245">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-245">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="71cfe-246">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-246">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="71cfe-247">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-247">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="71cfe-248">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-248">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="71cfe-249">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="71cfe-249">Deployment Manager</span></span>
* <span data-ttu-id="71cfe-250">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="71cfe-250">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="71cfe-251">ラボ</span><span class="sxs-lookup"><span data-stu-id="71cfe-251">Lab</span></span>
* <span data-ttu-id="71cfe-252">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-252">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-253">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-253">Network</span></span>
* <span data-ttu-id="71cfe-254">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-254">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-255">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-255">Resource</span></span>
* <span data-ttu-id="71cfe-256">[非推奨] `resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-256">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="71cfe-257">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="71cfe-257">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="71cfe-258">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-258">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="71cfe-259">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-259">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-260">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-260">SQL</span></span>
* <span data-ttu-id="71cfe-261">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-261">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="71cfe-262">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-262">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="71cfe-263">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-263">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="71cfe-264">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-264">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-265">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-265">Storage</span></span>
* <span data-ttu-id="71cfe-266">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-266">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-267">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-267">VM</span></span>
* <span data-ttu-id="71cfe-268">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-268">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="71cfe-269">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-269">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="71cfe-270">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-270">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="71cfe-271">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-271">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-272">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-272">Core</span></span>
* <span data-ttu-id="71cfe-273">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-273">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-274">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-274">ACR</span></span>
* <span data-ttu-id="71cfe-275">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-275">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="71cfe-276">AMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-276">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="71cfe-279">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-279">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="71cfe-280">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-280">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-281">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-281">AppService</span></span>
* <span data-ttu-id="71cfe-282">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-282">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="71cfe-283">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-283">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="71cfe-284">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-284">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="71cfe-285">[破壊的変更] `devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-285">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="71cfe-286">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-286">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="71cfe-287">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-287">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="71cfe-288">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-288">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="71cfe-289">CDN</span><span class="sxs-lookup"><span data-stu-id="71cfe-289">CDN</span></span>
* <span data-ttu-id="71cfe-290">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-290">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="71cfe-291">フィードバック</span><span class="sxs-lookup"><span data-stu-id="71cfe-291">Feedback</span></span>
* <span data-ttu-id="71cfe-292">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-292">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="71cfe-293">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-293">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="71cfe-294">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-294">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-295">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-295">Monitor</span></span>
* <span data-ttu-id="71cfe-296">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-296">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="71cfe-297">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-297">Network</span></span>
* <span data-ttu-id="71cfe-298">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-298">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="71cfe-299">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-299">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="71cfe-300">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-300">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="71cfe-301">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-301">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="71cfe-302">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="71cfe-302">PrivateDNS</span></span>
* <span data-ttu-id="71cfe-303">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-303">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-304">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-304">Resource</span></span>
* <span data-ttu-id="71cfe-305">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-305">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-306">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-306">Role</span></span>
* <span data-ttu-id="71cfe-307">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-307">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="71cfe-308">[破壊的変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-308">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-309">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-309">SQL</span></span>
* <span data-ttu-id="71cfe-310">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-310">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-311">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-311">Storage</span></span>
* <span data-ttu-id="71cfe-312">[破壊的変更] `storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-312">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="71cfe-313">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-313">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="71cfe-314">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-314">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="71cfe-315">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-315">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="71cfe-316">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-316">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="71cfe-317">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-317">Core</span></span>
* <span data-ttu-id="71cfe-318">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-318">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="71cfe-319">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-319">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="71cfe-320">クラウド</span><span class="sxs-lookup"><span data-stu-id="71cfe-320">Cloud</span></span>
* <span data-ttu-id="71cfe-321">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-321">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-322">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-322">ACR</span></span>
* <span data-ttu-id="71cfe-323">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-323">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="71cfe-324">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-324">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="71cfe-325">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-325">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="71cfe-326">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-326">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-327">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-327">AppService</span></span>
* <span data-ttu-id="71cfe-328">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-328">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="71cfe-329">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-329">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="71cfe-330">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="71cfe-330">BOT Service</span></span>
* <span data-ttu-id="71cfe-331">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-331">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="71cfe-332">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-332">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="71cfe-333">[破壊的変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-333">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="71cfe-334">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-334">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="71cfe-335">CDN</span><span class="sxs-lookup"><span data-stu-id="71cfe-335">CDN</span></span>
* <span data-ttu-id="71cfe-336">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-336">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [破壊的変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="71cfe-338">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-338">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="71cfe-339">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-339">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="71cfe-340">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="71cfe-340">Cosmosdb</span></span>
* <span data-ttu-id="71cfe-341">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-341">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="71cfe-342">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-342">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="71cfe-343">Interactive</span><span class="sxs-lookup"><span data-stu-id="71cfe-343">Interactive</span></span>
* <span data-ttu-id="71cfe-344">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-344">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-345">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-345">Monitor</span></span>
* <span data-ttu-id="71cfe-346">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-346">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-347">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-347">Network</span></span>
* <span data-ttu-id="71cfe-348">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-348">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="71cfe-349">プロファイル</span><span class="sxs-lookup"><span data-stu-id="71cfe-349">Profile</span></span>
* <span data-ttu-id="71cfe-350">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-350">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="71cfe-351">Postgres</span><span class="sxs-lookup"><span data-stu-id="71cfe-351">Postgres</span></span> 
* <span data-ttu-id="71cfe-352">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-352">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="71cfe-353">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="71cfe-353">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-354">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-354">Resource</span></span>
* <span data-ttu-id="71cfe-355">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-355">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="71cfe-356">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-356">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="71cfe-357">Graph</span><span class="sxs-lookup"><span data-stu-id="71cfe-357">Graph</span></span>
* <span data-ttu-id="71cfe-358">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-358">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="71cfe-359">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-359">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="71cfe-360">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-360">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="71cfe-361">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-361">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="71cfe-362">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-362">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-363">storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-363">storage</span></span>
* <span data-ttu-id="71cfe-364">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-364">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="71cfe-365">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-365">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="71cfe-366">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-366">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="71cfe-367">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-367">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-368">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-368">VM</span></span>
* <span data-ttu-id="71cfe-369">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-369">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="71cfe-370">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-370">March 12, 2019</span></span>

<span data-ttu-id="71cfe-371">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="71cfe-371">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-372">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-372">Core</span></span>

* <span data-ttu-id="71cfe-373">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-373">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-374">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-374">ACR</span></span>

* <span data-ttu-id="71cfe-375">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-375">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-376">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-376">ACS</span></span>

* <span data-ttu-id="71cfe-377">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-377">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="71cfe-378">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-378">AppService</span></span>

* <span data-ttu-id="71cfe-379">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-379">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="71cfe-380">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-380">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="71cfe-381">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-381">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="71cfe-382">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-382">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="71cfe-383">Botservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-383">Botservice</span></span>

* <span data-ttu-id="71cfe-384">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-384">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="71cfe-385">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-385">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="71cfe-386">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-386">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="71cfe-387">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-387">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-388">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-388">Container</span></span>

* <span data-ttu-id="71cfe-389">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-389">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="71cfe-390">EventHub</span><span class="sxs-lookup"><span data-stu-id="71cfe-390">EventHub</span></span>

* <span data-ttu-id="71cfe-391">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-391">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="71cfe-392">Find</span><span class="sxs-lookup"><span data-stu-id="71cfe-392">Find</span></span>

* <span data-ttu-id="71cfe-393">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="71cfe-393">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="71cfe-394">HDInsight</span><span class="sxs-lookup"><span data-stu-id="71cfe-394">HDInsight</span></span>

* <span data-ttu-id="71cfe-395">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-395">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-396">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-396">Network</span></span>

* <span data-ttu-id="71cfe-397">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-397">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="71cfe-398">Rdbms</span><span class="sxs-lookup"><span data-stu-id="71cfe-398">Rdbms</span></span>

* <span data-ttu-id="71cfe-399">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="71cfe-399">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-400">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-400">Role</span></span>

* <span data-ttu-id="71cfe-401">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-401">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="71cfe-402">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-402">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="71cfe-403">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="71cfe-403">Service Fabric</span></span>

* <span data-ttu-id="71cfe-404">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-404">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="71cfe-405">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-405">February 26, 2019</span></span>

<span data-ttu-id="71cfe-406">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="71cfe-406">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-407">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-407">Core</span></span>

* <span data-ttu-id="71cfe-408">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-408">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-409">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-409">ACR</span></span>

* <span data-ttu-id="71cfe-410">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-410">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="71cfe-411">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-411">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-412">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-412">ACS</span></span>

* <span data-ttu-id="71cfe-413">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-413">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-414">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-414">AppService</span></span>

* <span data-ttu-id="71cfe-415">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-415">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="71cfe-416">Batch</span><span class="sxs-lookup"><span data-stu-id="71cfe-416">Batch</span></span>
* <span data-ttu-id="71cfe-417">[破壊的変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-417">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="71cfe-418">[破壊的変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-418">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="71cfe-419">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-419">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="71cfe-420">[破壊的変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-420">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="71cfe-421">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-421">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="71cfe-422">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="71cfe-422">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="71cfe-423">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="71cfe-423">CosmosDB</span></span>

* <span data-ttu-id="71cfe-424">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-424">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="71cfe-425">Kusto</span><span class="sxs-lookup"><span data-stu-id="71cfe-425">Kusto</span></span>

* <span data-ttu-id="71cfe-426">[破壊的変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-426">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-427">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-427">Network</span></span>

* <span data-ttu-id="71cfe-428">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-428">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="71cfe-429">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-429">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="71cfe-430">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-430">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="71cfe-431">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-431">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="71cfe-432">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-432">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="71cfe-433">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-433">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="71cfe-434">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-434">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-435">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-435">Resource</span></span>

* <span data-ttu-id="71cfe-436">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-436">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="71cfe-437">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-437">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="71cfe-438">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-438">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="71cfe-439">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-439">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="71cfe-440">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-440">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-441">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-441">Role</span></span>

* <span data-ttu-id="71cfe-442">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-442">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-443">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-443">VM</span></span>

* <span data-ttu-id="71cfe-444">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-444">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="71cfe-445">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-445">February 12, 2019</span></span>

<span data-ttu-id="71cfe-446">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="71cfe-446">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-447">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-447">Core</span></span>

* <span data-ttu-id="71cfe-448">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-448">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="71cfe-449">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-449">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-450">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-450">ACR</span></span>
* <span data-ttu-id="71cfe-451">[破壊的変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-451">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="71cfe-452">[破壊的変更] `acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-452">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-453">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-453">ACS</span></span>
* <span data-ttu-id="71cfe-454">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-454">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="71cfe-455">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-455">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="71cfe-456">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-456">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="71cfe-457">AMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-457">AMS</span></span>
* <span data-ttu-id="71cfe-458">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-458">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="71cfe-459">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-459">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-460">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-460">Appservice</span></span>
* <span data-ttu-id="71cfe-461">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-461">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="71cfe-462">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-462">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="71cfe-463">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-463">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="71cfe-464">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-464">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="71cfe-465">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-465">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="71cfe-466">Botservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-466">Botservice</span></span>
* <span data-ttu-id="71cfe-467">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-467">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="71cfe-468">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-468">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="71cfe-469">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-469">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="71cfe-470">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-470">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="71cfe-471">[非推奨] `--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-471">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="71cfe-472">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-472">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="71cfe-473">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-473">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="71cfe-474">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-474">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="71cfe-475">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="71cfe-475">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="71cfe-476">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-476">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="71cfe-477">Key Vault</span><span class="sxs-lookup"><span data-stu-id="71cfe-477">Key Vault</span></span>
* <span data-ttu-id="71cfe-478">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-478">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-479">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-479">Monitor</span></span>
* <span data-ttu-id="71cfe-480">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-480">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-481">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-481">Network</span></span>
* <span data-ttu-id="71cfe-482">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-482">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="71cfe-483">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-483">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="71cfe-484">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-484">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="71cfe-485">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-485">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="71cfe-486">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="71cfe-486">Policy Insights</span></span>
* <span data-ttu-id="71cfe-487">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-487">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="71cfe-488">RDBMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-488">RDBMS</span></span>
* <span data-ttu-id="71cfe-489">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-489">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="71cfe-490">Redis</span><span class="sxs-lookup"><span data-stu-id="71cfe-490">Redis</span></span>
* <span data-ttu-id="71cfe-491">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-491">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="71cfe-492">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-492">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="71cfe-493">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-493">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="71cfe-494">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-494">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="71cfe-495">[破壊的変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-495">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="71cfe-496">[破壊的変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-496">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="71cfe-497">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-497">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-498">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-498">Role</span></span>
* <span data-ttu-id="71cfe-499">[破壊的変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-499">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="71cfe-500">SQL VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-500">SQL VM</span></span>
* <span data-ttu-id="71cfe-501">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-501">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-502">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-502">VM</span></span>
* <span data-ttu-id="71cfe-503">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-503">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="71cfe-504">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-504">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="71cfe-505">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-505">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="71cfe-506">[破壊的変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-506">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="71cfe-507">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-507">January 31, 2019</span></span>

<span data-ttu-id="71cfe-508">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="71cfe-508">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-509">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-509">Core</span></span>

* <span data-ttu-id="71cfe-510">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="71cfe-510">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="71cfe-511">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-511">January 28, 2019</span></span>

<span data-ttu-id="71cfe-512">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="71cfe-512">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-513">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-513">ACR</span></span>
* <span data-ttu-id="71cfe-514">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-514">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-515">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-515">ACS</span></span>
* <span data-ttu-id="71cfe-516">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-516">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="71cfe-517">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-517">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="71cfe-518">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-518">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="71cfe-519">AMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-519">AMS</span></span>
* <span data-ttu-id="71cfe-520">[破壊的変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-520">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="71cfe-521">[破壊的変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-521">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-522">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-522">Appservice</span></span>
* <span data-ttu-id="71cfe-523">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-523">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="71cfe-524">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-524">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="71cfe-525">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-525">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-526">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-526">Container</span></span>
* <span data-ttu-id="71cfe-527">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-527">Added `container start` command</span></span>
* <span data-ttu-id="71cfe-528">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-528">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="71cfe-529">EventGrid</span><span class="sxs-lookup"><span data-stu-id="71cfe-529">EventGrid</span></span>
* <span data-ttu-id="71cfe-530">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-530">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="71cfe-531">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-531">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="71cfe-532">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-532">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="71cfe-533">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-533">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="71cfe-534">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-534">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="71cfe-535">HDInsight</span><span class="sxs-lookup"><span data-stu-id="71cfe-535">HDInsight</span></span>
* <span data-ttu-id="71cfe-536">[破壊的変更] `hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-536">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="71cfe-537">[破壊的変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-537">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="71cfe-538">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-538">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="71cfe-539">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-539">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="71cfe-540">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-540">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="71cfe-541">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-541">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="71cfe-542">IoT</span><span class="sxs-lookup"><span data-stu-id="71cfe-542">IoT</span></span>
* <span data-ttu-id="71cfe-543">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-543">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="71cfe-544">Kusto</span><span class="sxs-lookup"><span data-stu-id="71cfe-544">Kusto</span></span>
* <span data-ttu-id="71cfe-545">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-545">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-546">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-546">Monitor</span></span>
* <span data-ttu-id="71cfe-547">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-547">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="71cfe-548">プロファイル</span><span class="sxs-lookup"><span data-stu-id="71cfe-548">Profile</span></span>
* <span data-ttu-id="71cfe-549">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-549">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-550">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-550">Network</span></span>
* <span data-ttu-id="71cfe-551">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-551">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="71cfe-552">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-552">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-553">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-553">Resource</span></span>
* <span data-ttu-id="71cfe-554">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-554">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="71cfe-555">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-555">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="71cfe-556">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="71cfe-556">SQL Virtual Machine</span></span>
* <span data-ttu-id="71cfe-557">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-557">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-558">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-558">Storage</span></span>
* <span data-ttu-id="71cfe-559">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-559">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="71cfe-560">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="71cfe-560">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-561">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-561">VM</span></span>
* <span data-ttu-id="71cfe-562">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-562">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="71cfe-563">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-563">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="71cfe-564">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-564">January 15, 2019</span></span>

<span data-ttu-id="71cfe-565">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="71cfe-565">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-566">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-566">ACR</span></span>
* <span data-ttu-id="71cfe-567">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-567">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="71cfe-568">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-568">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="71cfe-569">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-569">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="71cfe-570">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-570">ACS</span></span>
* <span data-ttu-id="71cfe-571">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-571">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-572">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-572">Appservice</span></span>
* <span data-ttu-id="71cfe-573">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-573">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="71cfe-574">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-574">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="71cfe-575">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-575">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="71cfe-576">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-576">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="71cfe-577">Botservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-577">Botservice</span></span>
* <span data-ttu-id="71cfe-578">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-578">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="71cfe-579">構成</span><span class="sxs-lookup"><span data-stu-id="71cfe-579">Configure</span></span>
* <span data-ttu-id="71cfe-580">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-580">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="71cfe-581">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="71cfe-581">CosmosDB</span></span>
* <span data-ttu-id="71cfe-582">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-582">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="71cfe-583">HDInsight</span><span class="sxs-lookup"><span data-stu-id="71cfe-583">HDInsight</span></span>
* <span data-ttu-id="71cfe-584">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-584">Added commands for managing applications</span></span>
* <span data-ttu-id="71cfe-585">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-585">Added commands for managing script actions</span></span>
* <span data-ttu-id="71cfe-586">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-586">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="71cfe-587">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-587">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="71cfe-588">[破壊的変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-588">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-589">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-589">Network</span></span>
* <span data-ttu-id="71cfe-590">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-590">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="71cfe-591">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-591">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="71cfe-592">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-592">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="71cfe-593">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-593">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-594">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-594">Role</span></span>
* <span data-ttu-id="71cfe-595">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-595">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="71cfe-596">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="71cfe-596">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="71cfe-597">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="71cfe-597">Security</span></span>
* <span data-ttu-id="71cfe-598">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-598">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-599">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-599">Storage</span></span>
* <span data-ttu-id="71cfe-600">[破壊的変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-600">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="71cfe-601">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="71cfe-601">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="71cfe-602">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-602">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="71cfe-603">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-603">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="71cfe-604">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-604">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-605">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-605">VM</span></span>
* <span data-ttu-id="71cfe-606">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-606">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="71cfe-607">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-607">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="71cfe-608">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-608">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="71cfe-609">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-609">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="71cfe-610">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-610">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="71cfe-611">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-611">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="71cfe-612">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-612">December 20, 2018</span></span>

<span data-ttu-id="71cfe-613">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="71cfe-613">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="71cfe-614">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-614">Appservice</span></span>
* <span data-ttu-id="71cfe-615">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-615">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="71cfe-616">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-616">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="71cfe-617">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-617">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="71cfe-618">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="71cfe-618">IoTCentral</span></span>
* <span data-ttu-id="71cfe-619">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-619">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-620">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-620">Role</span></span>
* <span data-ttu-id="71cfe-621">[破壊的変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-621">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-622">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-622">SQL</span></span>
* <span data-ttu-id="71cfe-623">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-623">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-624">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-624">VM</span></span>
* <span data-ttu-id="71cfe-625">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-625">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="71cfe-626">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-626">December 18, 2018</span></span>

<span data-ttu-id="71cfe-627">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="71cfe-627">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="71cfe-628">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-628">ACR</span></span>
* <span data-ttu-id="71cfe-629">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-629">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="71cfe-630">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-630">Condensed the table layout for task list</span></span>
* <span data-ttu-id="71cfe-631">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-631">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-632">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-632">ACS</span></span>
* <span data-ttu-id="71cfe-633">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-633">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="71cfe-634">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-634">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="71cfe-635">[非推奨] `az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-635">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="71cfe-636">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="71cfe-636">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="71cfe-637">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-637">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="71cfe-638">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-638">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-639">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-639">Appservice</span></span>
* <span data-ttu-id="71cfe-640">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-640">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="71cfe-641">Botservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-641">Botservice</span></span>
* <span data-ttu-id="71cfe-642">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-642">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="71cfe-643">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-643">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="71cfe-644">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-644">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="71cfe-645">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-645">Reduced Kudu network calls</span></span>
* <span data-ttu-id="71cfe-646">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-646">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="71cfe-647">消費</span><span class="sxs-lookup"><span data-stu-id="71cfe-647">Consumption</span></span>
* <span data-ttu-id="71cfe-648">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-648">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="71cfe-649">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="71cfe-649">CosmosDB</span></span>
* <span data-ttu-id="71cfe-650">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-650">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="71cfe-651">マップ</span><span class="sxs-lookup"><span data-stu-id="71cfe-651">Maps</span></span>
* <span data-ttu-id="71cfe-652">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-652">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-653">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-653">Network</span></span>
* <span data-ttu-id="71cfe-654">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-654">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="71cfe-655">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-655">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-656">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-656">Resource</span></span>
* <span data-ttu-id="71cfe-657">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-657">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="71cfe-658">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-658">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-659">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-659">Storage</span></span>
*  <span data-ttu-id="71cfe-660">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-660">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-661">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-661">VM</span></span>
* <span data-ttu-id="71cfe-662">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-662">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="71cfe-663">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-663">December 4, 2018</span></span>

<span data-ttu-id="71cfe-664">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="71cfe-664">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="71cfe-665">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-665">Core</span></span>
* <span data-ttu-id="71cfe-666">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-666">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="71cfe-667">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-667">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-668">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-668">Appservice</span></span>
* <span data-ttu-id="71cfe-669">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-669">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="71cfe-670">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-670">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-671">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-671">Network</span></span>
* <span data-ttu-id="71cfe-672">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-672">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-673">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-673">Role</span></span>
* <span data-ttu-id="71cfe-674">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-674">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="71cfe-675">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-675">VM</span></span>
* <span data-ttu-id="71cfe-676">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-676">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="71cfe-677">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-677">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="71cfe-678">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-678">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="71cfe-679">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-679">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="71cfe-680">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-680">November 20, 2018</span></span>

<span data-ttu-id="71cfe-681">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="71cfe-681">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="71cfe-682">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-682">Core</span></span>
* <span data-ttu-id="71cfe-683">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-683">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-684">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-684">ACR</span></span>
* <span data-ttu-id="71cfe-685">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-685">Added context token to task step</span></span>
* <span data-ttu-id="71cfe-686">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-686">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="71cfe-687">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-687">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-688">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-688">Appservice</span></span>
* <span data-ttu-id="71cfe-689">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-689">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="71cfe-690">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-690">Updated the default `node_version`.</span></span> <span data-ttu-id="71cfe-691">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-691">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="71cfe-692">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-692">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="71cfe-693">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-693">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="71cfe-694">IotCentral</span><span class="sxs-lookup"><span data-stu-id="71cfe-694">IotCentral</span></span>
* <span data-ttu-id="71cfe-695">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-695">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="71cfe-696">KeyVault</span><span class="sxs-lookup"><span data-stu-id="71cfe-696">KeyVault</span></span>
* <span data-ttu-id="71cfe-697">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-697">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-698">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-698">Network</span></span>
* <span data-ttu-id="71cfe-699">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-699">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="71cfe-700">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-700">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="71cfe-701">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-701">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="71cfe-702">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-702">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="71cfe-703">Rdbms</span><span class="sxs-lookup"><span data-stu-id="71cfe-703">Rdbms</span></span>
* <span data-ttu-id="71cfe-704">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-704">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="71cfe-705">Rbac</span><span class="sxs-lookup"><span data-stu-id="71cfe-705">Rbac</span></span>
* <span data-ttu-id="71cfe-706">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-706">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="71cfe-707">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-707">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="71cfe-708">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-708">Storage</span></span>
* <span data-ttu-id="71cfe-709">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-709">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="71cfe-710">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-710">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="71cfe-711">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-711">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="71cfe-712">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-712">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-713">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-713">VM</span></span>
* <span data-ttu-id="71cfe-714">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-714">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="71cfe-715">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-715">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="71cfe-716">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="71cfe-716">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="71cfe-717">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-717">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="71cfe-718">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-718">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="71cfe-719">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-719">Added `snapshot wait` command</span></span>
* <span data-ttu-id="71cfe-720">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-720">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="71cfe-721">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-721">November 6, 2018</span></span>

<span data-ttu-id="71cfe-722">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="71cfe-722">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-723">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-723">Core</span></span>
* <span data-ttu-id="71cfe-724">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-724">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-725">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-725">ACR</span></span>
* <span data-ttu-id="71cfe-726">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-726">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="71cfe-727">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-727">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-728">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-728">ACS</span></span>
* <span data-ttu-id="71cfe-729">[破壊的変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-729">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="71cfe-730">Advisor</span><span class="sxs-lookup"><span data-stu-id="71cfe-730">Advisor</span></span>
* <span data-ttu-id="71cfe-731">GA リリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-731">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="71cfe-732">AMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-732">AMS</span></span>
* <span data-ttu-id="71cfe-733">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-733">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="71cfe-734">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-734">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="71cfe-735">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-735">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="71cfe-736">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-736">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="71cfe-737">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-737">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="71cfe-738">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-738">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="71cfe-739">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-739">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="71cfe-740">[破壊的変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="71cfe-740">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="71cfe-741">[破壊的変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-741">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="71cfe-742">[破壊的変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-742">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="71cfe-743">[破壊的変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="71cfe-743">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="71cfe-744">[破壊的変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-744">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="71cfe-745">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="71cfe-745">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="71cfe-746">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="71cfe-746">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="71cfe-747">[破壊的変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-747">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="71cfe-748">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-748">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="71cfe-749">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="71cfe-749">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-750">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-750">AppService</span></span>
* <span data-ttu-id="71cfe-751">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-751">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="71cfe-752">構成</span><span class="sxs-lookup"><span data-stu-id="71cfe-752">Configure</span></span>
* <span data-ttu-id="71cfe-753">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-753">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-754">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-754">Container</span></span>
* <span data-ttu-id="71cfe-755">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-755">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="71cfe-756">EventHub</span><span class="sxs-lookup"><span data-stu-id="71cfe-756">EventHub</span></span>
* <span data-ttu-id="71cfe-757">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-757">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="71cfe-758">Interactive</span><span class="sxs-lookup"><span data-stu-id="71cfe-758">Interactive</span></span>
* <span data-ttu-id="71cfe-759">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="71cfe-759">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-760">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-760">Monitor</span></span>
* <span data-ttu-id="71cfe-761">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-761">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-762">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-762">Network</span></span>
* <span data-ttu-id="71cfe-763">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-763">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="71cfe-764">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-764">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="71cfe-765">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-765">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="71cfe-766">プロファイル</span><span class="sxs-lookup"><span data-stu-id="71cfe-766">Profile</span></span>
* <span data-ttu-id="71cfe-767">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-767">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="71cfe-768">RDBMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-768">RDBMS</span></span>
* <span data-ttu-id="71cfe-769">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-769">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-770">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-770">Resource</span></span>
* <span data-ttu-id="71cfe-771">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-771">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-772">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-772">Role</span></span>
* <span data-ttu-id="71cfe-773">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-773">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="71cfe-774">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-774">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="71cfe-775">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-775">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-776">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-776">Storage</span></span>
* <span data-ttu-id="71cfe-777">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="71cfe-777">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-778">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-778">VM</span></span>
* <span data-ttu-id="71cfe-779">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-779">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="71cfe-780">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-780">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="71cfe-781">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-781">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="71cfe-782">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-782">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="71cfe-783">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="71cfe-783">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="71cfe-784">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-784">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="71cfe-785">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-785">October 23, 2018</span></span>

<span data-ttu-id="71cfe-786">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="71cfe-786">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-787">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-787">Core</span></span>
* <span data-ttu-id="71cfe-788">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-788">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="71cfe-789">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-789">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-790">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-790">ACR</span></span>
* <span data-ttu-id="71cfe-791">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-791">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="71cfe-792">CDN</span><span class="sxs-lookup"><span data-stu-id="71cfe-792">CDN</span></span>
* <span data-ttu-id="71cfe-793">[破壊的変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-793">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="71cfe-794">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-794">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-795">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-795">Container</span></span>
* <span data-ttu-id="71cfe-796">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-796">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="71cfe-797">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-797">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="71cfe-798">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-798">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="71cfe-799">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-799">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="71cfe-800">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-800">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="71cfe-801">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-801">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="71cfe-802">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-802">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="71cfe-803">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="71cfe-803">CosmosDB</span></span>
* <span data-ttu-id="71cfe-804">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-804">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="71cfe-805">Interactive</span><span class="sxs-lookup"><span data-stu-id="71cfe-805">Interactive</span></span>
* <span data-ttu-id="71cfe-806">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-806">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="71cfe-807">IoT Central</span><span class="sxs-lookup"><span data-stu-id="71cfe-807">IoT Central</span></span>
* <span data-ttu-id="71cfe-808">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-808">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="71cfe-809">[破壊的変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="71cfe-809">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-810">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-810">Monitor</span></span>
* <span data-ttu-id="71cfe-811">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="71cfe-811">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="71cfe-812">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-812">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="71cfe-813">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-813">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="71cfe-814">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-814">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="71cfe-815">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-815">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="71cfe-816">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-816">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="71cfe-817">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="71cfe-817">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="71cfe-818">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-818">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="71cfe-819">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-819">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="71cfe-820">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-820">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-821">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-821">Network</span></span>
* <span data-ttu-id="71cfe-822">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-822">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="71cfe-823">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-823">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="71cfe-824">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71cfe-824">ServiceBus</span></span>
* <span data-ttu-id="71cfe-825">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-825">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-826">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-826">SQL</span></span>
* <span data-ttu-id="71cfe-827">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-827">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-828">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-828">Storage</span></span>
* <span data-ttu-id="71cfe-829">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-829">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="71cfe-830">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-830">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-831">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-831">VM</span></span>
* <span data-ttu-id="71cfe-832">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-832">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="71cfe-833">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-833">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="71cfe-834">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-834">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="71cfe-835">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-835">October 16, 2018</span></span>

<span data-ttu-id="71cfe-836">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="71cfe-836">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-837">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-837">VM</span></span>
* <span data-ttu-id="71cfe-838">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-838">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="71cfe-839">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-839">October 9, 2018</span></span>

<span data-ttu-id="71cfe-840">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="71cfe-840">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-841">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-841">Core</span></span>
* <span data-ttu-id="71cfe-842">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-842">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-843">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-843">ACR</span></span>
* <span data-ttu-id="71cfe-844">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-844">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-845">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-845">ACS</span></span>
* <span data-ttu-id="71cfe-846">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="71cfe-846">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="71cfe-847">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-847">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="71cfe-848">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-848">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="71cfe-849">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-849">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-850">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-850">Container</span></span>
* <span data-ttu-id="71cfe-851">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-851">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="71cfe-852">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-852">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="71cfe-853">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="71cfe-853">Event Hub</span></span>
* <span data-ttu-id="71cfe-854">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-854">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="71cfe-855">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-855">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="71cfe-856">Extensions</span><span class="sxs-lookup"><span data-stu-id="71cfe-856">Extensions</span></span>
* <span data-ttu-id="71cfe-857">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-857">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="71cfe-858">HDInsight</span><span class="sxs-lookup"><span data-stu-id="71cfe-858">HDInsight</span></span>
* <span data-ttu-id="71cfe-859">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-859">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="71cfe-860">IoT</span><span class="sxs-lookup"><span data-stu-id="71cfe-860">IoT</span></span>
* <span data-ttu-id="71cfe-861">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-861">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="71cfe-862">KeyVault</span><span class="sxs-lookup"><span data-stu-id="71cfe-862">KeyVault</span></span>
* <span data-ttu-id="71cfe-863">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-863">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-864">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-864">Network</span></span>
* <span data-ttu-id="71cfe-865">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="71cfe-865">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="71cfe-866">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="71cfe-866">See #6052</span></span>
* <span data-ttu-id="71cfe-867">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-867">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="71cfe-868">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="71cfe-868">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="71cfe-869">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-869">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="71cfe-870">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-870">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="71cfe-871">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-871">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="71cfe-872">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-872">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-873">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-873">Role</span></span>
* <span data-ttu-id="71cfe-874">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-874">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="71cfe-875">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-875">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="71cfe-876">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-876">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="71cfe-877">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-877">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="71cfe-878">Service Bus</span><span class="sxs-lookup"><span data-stu-id="71cfe-878">Service Bus</span></span>
* <span data-ttu-id="71cfe-879">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-879">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-880">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-880">VM</span></span>
* <span data-ttu-id="71cfe-881">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-881">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="71cfe-882">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-882">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="71cfe-883">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-883">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="71cfe-884">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-884">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="71cfe-885">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-885">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="71cfe-886">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-886">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="71cfe-887">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-887">September 21, 2018</span></span>

<span data-ttu-id="71cfe-888">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="71cfe-888">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-889">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-889">ACR</span></span>
* <span data-ttu-id="71cfe-890">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-890">Added ACR Task commands</span></span>
* <span data-ttu-id="71cfe-891">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-891">Added quick run command</span></span>
* <span data-ttu-id="71cfe-892">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-892">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="71cfe-893">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-893">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="71cfe-894">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-894">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="71cfe-895">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-895">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-896">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-896">ACS</span></span>
* <span data-ttu-id="71cfe-897">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-897">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="71cfe-898">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-898">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-899">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-899">AppService</span></span>

* <span data-ttu-id="71cfe-900">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-900">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="71cfe-901">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-901">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="71cfe-902">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-902">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="71cfe-903">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-903">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="71cfe-904">Batch</span><span class="sxs-lookup"><span data-stu-id="71cfe-904">Batch</span></span>
* <span data-ttu-id="71cfe-905">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-905">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="71cfe-906">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-906">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="71cfe-907">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-907">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="71cfe-908">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-908">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="71cfe-909">Batch AI</span><span class="sxs-lookup"><span data-stu-id="71cfe-909">Batch AI</span></span> 
* <span data-ttu-id="71cfe-910">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-910">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="71cfe-911">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="71cfe-911">Cognitive Services</span></span>
* <span data-ttu-id="71cfe-912">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-912">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="71cfe-913">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-913">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="71cfe-914">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-914">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="71cfe-915">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-915">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="71cfe-916">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-916">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="71cfe-917">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-917">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-918">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-918">Container</span></span>
* <span data-ttu-id="71cfe-919">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-919">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="71cfe-920">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-920">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="71cfe-921">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-921">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="71cfe-922">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-922">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="71cfe-923">DataLake</span><span class="sxs-lookup"><span data-stu-id="71cfe-923">Datalake</span></span>
* <span data-ttu-id="71cfe-924">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-924">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="71cfe-925">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="71cfe-925">Interactive Shell</span></span>
* <span data-ttu-id="71cfe-926">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-926">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="71cfe-927">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-927">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="71cfe-928">IoT</span><span class="sxs-lookup"><span data-stu-id="71cfe-928">IoT</span></span>
* <span data-ttu-id="71cfe-929">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-929">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="71cfe-930">Key Vault</span><span class="sxs-lookup"><span data-stu-id="71cfe-930">Key Vault</span></span>
* <span data-ttu-id="71cfe-931">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-931">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-932">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-932">Network</span></span>
* <span data-ttu-id="71cfe-933">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-933">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="71cfe-934">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-934">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="71cfe-935">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-935">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="71cfe-936">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-936">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="71cfe-937">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-937">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="71cfe-938">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-938">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="71cfe-939">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-939">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="71cfe-940">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-940">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="71cfe-941">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-941">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="71cfe-942">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-942">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="71cfe-943">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-943">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="71cfe-944">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-944">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="71cfe-945">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-945">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="71cfe-946">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="71cfe-946">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="71cfe-947">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-947">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="71cfe-948">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-948">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="71cfe-949">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-949">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="71cfe-950">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-950">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="71cfe-951">RDBMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-951">RDBMS</span></span>
* <span data-ttu-id="71cfe-952">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-952">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="71cfe-953">予約</span><span class="sxs-lookup"><span data-stu-id="71cfe-953">Reservation</span></span>
* <span data-ttu-id="71cfe-954">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-954">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="71cfe-955">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-955">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="71cfe-956">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="71cfe-956">Manage App</span></span>
* <span data-ttu-id="71cfe-957">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-957">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="71cfe-958">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-958">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-959">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-959">Role</span></span>
* <span data-ttu-id="71cfe-960">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-960">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="71cfe-961">SignalR</span><span class="sxs-lookup"><span data-stu-id="71cfe-961">SignalR</span></span>
* <span data-ttu-id="71cfe-962">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-962">First release</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-963">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-963">Storage</span></span>
* <span data-ttu-id="71cfe-964">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-964">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="71cfe-965">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-965">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-966">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-966">VM</span></span>
* <span data-ttu-id="71cfe-967">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="71cfe-967">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="71cfe-968">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-968">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="71cfe-969">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-969">August 28, 2018</span></span>

<span data-ttu-id="71cfe-970">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="71cfe-970">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-971">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-971">Core</span></span>

* <span data-ttu-id="71cfe-972">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-972">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="71cfe-973">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-973">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-974">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-974">ACR</span></span>

* <span data-ttu-id="71cfe-975">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-975">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="71cfe-976">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-976">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-977">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-977">ACS</span></span>

* <span data-ttu-id="71cfe-978">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-978">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="71cfe-979">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-979">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-980">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-980">AppService</span></span>

* <span data-ttu-id="71cfe-981">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-981">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="71cfe-982">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-982">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="71cfe-983">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-983">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="71cfe-984">バックアップ</span><span class="sxs-lookup"><span data-stu-id="71cfe-984">Backup</span></span>

* <span data-ttu-id="71cfe-985">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-985">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="71cfe-986">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="71cfe-986">Bot Service</span></span>

* <span data-ttu-id="71cfe-987">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-987">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="71cfe-988">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="71cfe-988">Cognitive Services</span></span>

* <span data-ttu-id="71cfe-989">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-989">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="71cfe-990">IoT</span><span class="sxs-lookup"><span data-stu-id="71cfe-990">IoT</span></span>

* <span data-ttu-id="71cfe-991">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-991">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-992">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-992">Monitor</span></span>

* <span data-ttu-id="71cfe-993">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-993">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="71cfe-994">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-994">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-995">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-995">Network</span></span>

* <span data-ttu-id="71cfe-996">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-996">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-997">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-997">Resource</span></span>

* <span data-ttu-id="71cfe-998">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-998">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-999">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-999">Storage</span></span>

* <span data-ttu-id="71cfe-1000">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1000">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1001">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1001">VM</span></span>

* <span data-ttu-id="71cfe-1002">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1002">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="71cfe-1003">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1003">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="71cfe-1004">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1004">Auguest 14, 2018</span></span>

<span data-ttu-id="71cfe-1005">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="71cfe-1005">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1006">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1006">Core</span></span>

* <span data-ttu-id="71cfe-1007">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1007">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="71cfe-1008">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1008">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="71cfe-1009">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="71cfe-1009">Telemetry</span></span>

* <span data-ttu-id="71cfe-1010">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1010">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-1011">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-1011">ACR</span></span>

* <span data-ttu-id="71cfe-1012">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1012">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="71cfe-1013">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1013">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1014">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1014">ACS</span></span>

* <span data-ttu-id="71cfe-1015">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1015">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="71cfe-1016">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1016">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="71cfe-1017">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1017">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="71cfe-1018">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1018">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="71cfe-1019">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1019">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="71cfe-1020">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-1020">AppService</span></span>

* <span data-ttu-id="71cfe-1021">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1021">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="71cfe-1022">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1022">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="71cfe-1023">BatchAI</span><span class="sxs-lookup"><span data-stu-id="71cfe-1023">BatchAI</span></span>

* <span data-ttu-id="71cfe-1024">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1024">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="71cfe-1025">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-1025">Container</span></span>

* <span data-ttu-id="71cfe-1026">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1026">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="71cfe-1027">IoT</span><span class="sxs-lookup"><span data-stu-id="71cfe-1027">IoT</span></span>

* <span data-ttu-id="71cfe-1028">[破壊的変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1028">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="71cfe-1029">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1029">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="71cfe-1030">Iot Central</span><span class="sxs-lookup"><span data-stu-id="71cfe-1030">Iot Central</span></span>

* <span data-ttu-id="71cfe-1031">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-1031">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="71cfe-1032">KeyVault</span><span class="sxs-lookup"><span data-stu-id="71cfe-1032">KeyVault</span></span>


* <span data-ttu-id="71cfe-1033">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1033">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="71cfe-1034">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1034">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="71cfe-1035">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1035">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="71cfe-1036">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1036">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="71cfe-1037">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1037">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="71cfe-1038">リレー</span><span class="sxs-lookup"><span data-stu-id="71cfe-1038">Relay</span></span>

* <span data-ttu-id="71cfe-1039">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-1039">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-1040">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-1040">Sql</span></span>

* <span data-ttu-id="71cfe-1041">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1041">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1042">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1042">Storage</span></span>

* <span data-ttu-id="71cfe-1043">[破壊的変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-1043">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="71cfe-1044">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1044">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="71cfe-1045">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1045">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="71cfe-1046">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1046">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="71cfe-1047">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1047">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1048">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1048">VM</span></span>

* <span data-ttu-id="71cfe-1049">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1049">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="71cfe-1050">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1050">July 31, 2018</span></span>

<span data-ttu-id="71cfe-1051">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="71cfe-1051">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-1052">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-1052">ACR</span></span>

* <span data-ttu-id="71cfe-1053">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1053">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="71cfe-1054">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1054">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1055">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1055">ACS</span></span>

* <span data-ttu-id="71cfe-1056">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1056">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="71cfe-1057">Batch</span><span class="sxs-lookup"><span data-stu-id="71cfe-1057">Batch</span></span>

* <span data-ttu-id="71cfe-1058">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1058">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-1059">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-1059">Container</span></span>

* <span data-ttu-id="71cfe-1060">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1060">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1061">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1061">Network</span></span>

* <span data-ttu-id="71cfe-1062">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1062">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="71cfe-1063">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-1063">Resource</span></span>

* <span data-ttu-id="71cfe-1064">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1064">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="71cfe-1065">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1065">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-1066">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-1066">Role</span></span>

* <span data-ttu-id="71cfe-1067">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1067">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="71cfe-1068">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1068">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="71cfe-1069">Search</span><span class="sxs-lookup"><span data-stu-id="71cfe-1069">Search</span></span>

* <span data-ttu-id="71cfe-1070">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1070">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="71cfe-1071">Service Bus</span><span class="sxs-lookup"><span data-stu-id="71cfe-1071">Service Bus</span></span>

* <span data-ttu-id="71cfe-1072">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1072">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="71cfe-1073">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1073">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="71cfe-1074">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="71cfe-1074">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="71cfe-1075">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="71cfe-1075">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1076">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1076">Storage</span></span>

* <span data-ttu-id="71cfe-1077">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1077">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="71cfe-1078">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1078">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1079">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1079">VM</span></span>

* <span data-ttu-id="71cfe-1080">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1080">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="71cfe-1081">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1081">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="71cfe-1082">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1082">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="71cfe-1083">[破壊的変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1083">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="71cfe-1084">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1084">July 18, 2018</span></span>

<span data-ttu-id="71cfe-1085">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="71cfe-1085">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1086">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1086">Core</span></span>

* <span data-ttu-id="71cfe-1087">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1087">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="71cfe-1088">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1088">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="71cfe-1089">[破壊的変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1089">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-1090">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-1090">ACR</span></span>

* <span data-ttu-id="71cfe-1091">[破壊的変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1091">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="71cfe-1092">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1092">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="71cfe-1093">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1093">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="71cfe-1094">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1094">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1095">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1095">ACS</span></span>

* <span data-ttu-id="71cfe-1096">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1096">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1097">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-1097">AppService</span></span>

* <span data-ttu-id="71cfe-1098">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1098">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="71cfe-1099">Batch</span><span class="sxs-lookup"><span data-stu-id="71cfe-1099">Batch</span></span>

* <span data-ttu-id="71cfe-1100">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1100">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="71cfe-1101">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1101">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="71cfe-1102">Batch AI</span><span class="sxs-lookup"><span data-stu-id="71cfe-1102">Batch AI</span></span>

* <span data-ttu-id="71cfe-1103">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1103">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-1104">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-1104">Container</span></span>

* <span data-ttu-id="71cfe-1105">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1105">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="71cfe-1106">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1106">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1107">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1107">Network</span></span>

* <span data-ttu-id="71cfe-1108">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1108">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="71cfe-1109">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1109">Added `network nic wait`</span></span>
* <span data-ttu-id="71cfe-1110">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1110">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="71cfe-1111">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1111">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="71cfe-1112">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-1112">Resource</span></span>

* <span data-ttu-id="71cfe-1113">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1113">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="71cfe-1114">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1114">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="71cfe-1115">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1115">Added `deployment wait` command</span></span>
* <span data-ttu-id="71cfe-1116">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1116">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-1117">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-1117">SQL</span></span>

* <span data-ttu-id="71cfe-1118">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1118">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="71cfe-1119">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1119">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="71cfe-1120">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1120">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1121">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1121">Storage</span></span>

* <span data-ttu-id="71cfe-1122">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1122">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1123">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1123">VM</span></span>

* <span data-ttu-id="71cfe-1124">[破壊的変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1124">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="71cfe-1125">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1125">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="71cfe-1126">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1126">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="71cfe-1127">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1127">July 3, 2018</span></span>

<span data-ttu-id="71cfe-1128">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="71cfe-1128">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="71cfe-1129">AKS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1129">AKS</span></span>

* <span data-ttu-id="71cfe-1130">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1130">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="71cfe-1131">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1131">July 3, 2018</span></span>

<span data-ttu-id="71cfe-1132">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="71cfe-1132">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1133">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1133">Core</span></span>

* <span data-ttu-id="71cfe-1134">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1134">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-1135">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-1135">ACR</span></span>

* <span data-ttu-id="71cfe-1136">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1136">Added polling build status</span></span>
* <span data-ttu-id="71cfe-1137">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1137">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="71cfe-1138">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1138">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1139">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1139">ACS</span></span>

* <span data-ttu-id="71cfe-1140">[破壊的変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1140">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="71cfe-1141">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1141">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="71cfe-1142">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1142">Updated options for `aks browse` command.</span></span> <span data-ttu-id="71cfe-1143">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1143">Added `--listen-port` support</span></span>
* <span data-ttu-id="71cfe-1144">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1144">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="71cfe-1145">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1145">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="71cfe-1146">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1146">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1147">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-1147">AppService</span></span>

* <span data-ttu-id="71cfe-1148">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1148">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="71cfe-1149">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1149">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="71cfe-1150">バックアップ</span><span class="sxs-lookup"><span data-stu-id="71cfe-1150">Backup</span></span>

* <span data-ttu-id="71cfe-1151">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1151">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="71cfe-1152">BatchAI</span><span class="sxs-lookup"><span data-stu-id="71cfe-1152">BatchAI</span></span>

* <span data-ttu-id="71cfe-1153">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1153">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="71cfe-1154">クラウド</span><span class="sxs-lookup"><span data-stu-id="71cfe-1154">Cloud</span></span>

* <span data-ttu-id="71cfe-1155">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1155">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-1156">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-1156">Container</span></span>

* <span data-ttu-id="71cfe-1157">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1157">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="71cfe-1158">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1158">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="71cfe-1159">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1159">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="71cfe-1160">拡張機能</span><span class="sxs-lookup"><span data-stu-id="71cfe-1160">Extension</span></span>

* <span data-ttu-id="71cfe-1161">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1161">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1162">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1162">Network</span></span>

* <span data-ttu-id="71cfe-1163">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1163">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="71cfe-1164">Rdbms</span><span class="sxs-lookup"><span data-stu-id="71cfe-1164">Rdbms</span></span>

* <span data-ttu-id="71cfe-1165">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1165">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-1166">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-1166">Resource</span></span>

* <span data-ttu-id="71cfe-1167">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1167">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1168">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1168">VM</span></span>

* <span data-ttu-id="71cfe-1169">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1169">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="71cfe-1170">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1170">June 25, 2018</span></span>

<span data-ttu-id="71cfe-1171">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="71cfe-1171">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="71cfe-1172">CLI</span><span class="sxs-lookup"><span data-stu-id="71cfe-1172">CLI</span></span>

* <span data-ttu-id="71cfe-1173">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1173">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="71cfe-1174">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1174">June 19, 2018</span></span>

<span data-ttu-id="71cfe-1175">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="71cfe-1175">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1176">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1176">Core</span></span>

* <span data-ttu-id="71cfe-1177">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1177">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-1178">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-1178">ACR</span></span>

* <span data-ttu-id="71cfe-1179">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1179">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="71cfe-1180">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1180">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1181">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1181">ACS</span></span>

* <span data-ttu-id="71cfe-1182">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1182">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="71cfe-1183">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1183">Added `--update` support</span></span>
* <span data-ttu-id="71cfe-1184">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1184">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="71cfe-1185">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1185">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="71cfe-1186">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1186">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="71cfe-1187">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1187">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="71cfe-1188">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1188">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="71cfe-1189">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1189">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1190">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-1190">AppService</span></span>

* <span data-ttu-id="71cfe-1191">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1191">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="71cfe-1192">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1192">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="71cfe-1193">Batch</span><span class="sxs-lookup"><span data-stu-id="71cfe-1193">Batch</span></span>

* <span data-ttu-id="71cfe-1194">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1194">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="71cfe-1195">Batch AI</span><span class="sxs-lookup"><span data-stu-id="71cfe-1195">Batch AI</span></span>

* <span data-ttu-id="71cfe-1196">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1196">Added support for workspaces.</span></span> <span data-ttu-id="71cfe-1197">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="71cfe-1197">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="71cfe-1198">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1198">Added support for experiments.</span></span> <span data-ttu-id="71cfe-1199">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="71cfe-1199">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="71cfe-1200">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1200">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="71cfe-1201">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1201">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="71cfe-1202">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1202">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="71cfe-1203">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1203">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="71cfe-1204">[破壊的変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="71cfe-1204">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="71cfe-1205">[破壊的変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="71cfe-1205">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="71cfe-1206">[破壊的変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1206">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="71cfe-1207">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1207">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="71cfe-1208">[破壊的変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1208">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="71cfe-1209">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1209">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="71cfe-1210">[破壊的変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1210">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="71cfe-1211">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1211">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="71cfe-1212">[破壊的変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1212">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="71cfe-1213">[破壊的変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1213">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="71cfe-1214">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1214">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="71cfe-1215">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1215">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="71cfe-1216">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1216">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="71cfe-1217">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1217">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="71cfe-1218">マップ</span><span class="sxs-lookup"><span data-stu-id="71cfe-1218">Maps</span></span>

* <span data-ttu-id="71cfe-1219">[破壊的変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1219">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1220">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1220">Network</span></span>

* <span data-ttu-id="71cfe-1221">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="71cfe-1221">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="71cfe-1222">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1222">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="71cfe-1223">#6502</span><span class="sxs-lookup"><span data-stu-id="71cfe-1223">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="71cfe-1224">Reservations</span><span class="sxs-lookup"><span data-stu-id="71cfe-1224">Reservations</span></span>

* <span data-ttu-id="71cfe-1225">[破壊的変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1225">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="71cfe-1226">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1226">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="71cfe-1227">[破壊的変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1227">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="71cfe-1228">[破壊的変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1228">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="71cfe-1229">[破壊的変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1229">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="71cfe-1230">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1230">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-1231">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-1231">Role</span></span>

* <span data-ttu-id="71cfe-1232">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1232">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-1233">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-1233">SQL</span></span>

* <span data-ttu-id="71cfe-1234">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1234">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1235">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1235">Storage</span></span>

* <span data-ttu-id="71cfe-1236">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1236">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1237">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1237">VM</span></span>

* <span data-ttu-id="71cfe-1238">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1238">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="71cfe-1239">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1239">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="71cfe-1240">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1240">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="71cfe-1241">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1241">June 13, 2018</span></span>

<span data-ttu-id="71cfe-1242">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="71cfe-1242">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1243">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1243">Core</span></span>

* <span data-ttu-id="71cfe-1244">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1244">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="71cfe-1245">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1245">June 13, 2018</span></span>

<span data-ttu-id="71cfe-1246">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="71cfe-1246">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="71cfe-1247">AKS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1247">AKS</span></span>

* <span data-ttu-id="71cfe-1248">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1248">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="71cfe-1249">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1249">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="71cfe-1250">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1250">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="71cfe-1251">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1251">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="71cfe-1252">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1252">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1253">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-1253">AppService</span></span>

* <span data-ttu-id="71cfe-1254">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1254">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="71cfe-1255">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1255">June 5, 2018</span></span>

<span data-ttu-id="71cfe-1256">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="71cfe-1256">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="71cfe-1257">Interactive</span><span class="sxs-lookup"><span data-stu-id="71cfe-1257">Interactive</span></span>

* <span data-ttu-id="71cfe-1258">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1258">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="71cfe-1259">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1259">June 5, 2018</span></span>

<span data-ttu-id="71cfe-1260">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="71cfe-1260">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1261">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1261">Core</span></span>

* <span data-ttu-id="71cfe-1262">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1262">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="71cfe-1263">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1263">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-1264">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-1264">ACR</span></span>

* <span data-ttu-id="71cfe-1265">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1265">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="71cfe-1266">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1266">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="71cfe-1267">AKS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1267">AKS</span></span>

* <span data-ttu-id="71cfe-1268">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1268">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="71cfe-1269">Batch</span><span class="sxs-lookup"><span data-stu-id="71cfe-1269">Batch</span></span>

* <span data-ttu-id="71cfe-1270">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1270">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="71cfe-1271">IoT</span><span class="sxs-lookup"><span data-stu-id="71cfe-1271">IOT</span></span>

* <span data-ttu-id="71cfe-1272">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1272">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1273">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1273">Network</span></span>

* <span data-ttu-id="71cfe-1274">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1274">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="71cfe-1275">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="71cfe-1275">Policy Insights</span></span>

* <span data-ttu-id="71cfe-1276">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-1276">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="71cfe-1277">ARM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1277">ARM</span></span>

* <span data-ttu-id="71cfe-1278">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1278">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-1279">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-1279">SQL</span></span>

* <span data-ttu-id="71cfe-1280">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1280">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="71cfe-1281">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1281">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="71cfe-1282">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1282">Storage</span></span>

* <span data-ttu-id="71cfe-1283">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1283">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1284">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1284">VM</span></span>

* <span data-ttu-id="71cfe-1285">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1285">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="71cfe-1286">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1286">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="71cfe-1287">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1287">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="71cfe-1288">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1288">May 22, 2018</span></span>

<span data-ttu-id="71cfe-1289">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="71cfe-1289">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1290">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1290">Core</span></span>

* <span data-ttu-id="71cfe-1291">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1291">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1292">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1292">ACS</span></span>

* <span data-ttu-id="71cfe-1293">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1293">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="71cfe-1294">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1294">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1295">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-1295">AppService</span></span>

* <span data-ttu-id="71cfe-1296">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1296">Improved generic update commands</span></span>
* <span data-ttu-id="71cfe-1297">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1297">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-1298">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-1298">Container</span></span>

* <span data-ttu-id="71cfe-1299">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1299">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="71cfe-1300">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1300">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="71cfe-1301">拡張機能</span><span class="sxs-lookup"><span data-stu-id="71cfe-1301">Extension</span></span>

* <span data-ttu-id="71cfe-1302">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1302">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="71cfe-1303">Interactive</span><span class="sxs-lookup"><span data-stu-id="71cfe-1303">Interactive</span></span>

* <span data-ttu-id="71cfe-1304">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1304">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="71cfe-1305">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1305">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="71cfe-1306">KeyVault</span><span class="sxs-lookup"><span data-stu-id="71cfe-1306">KeyVault</span></span>

* <span data-ttu-id="71cfe-1307">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1307">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1308">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1308">Network</span></span>

* <span data-ttu-id="71cfe-1309">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1309">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="71cfe-1310">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1310">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-1311">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-1311">SQL</span></span>

* <span data-ttu-id="71cfe-1312">[破壊的変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1312">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="71cfe-1313">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1313">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="71cfe-1314">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1314">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="71cfe-1315">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1315">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="71cfe-1316">[破壊的変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1316">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="71cfe-1317">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="71cfe-1317">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="71cfe-1318">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1318">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="71cfe-1319">`edition`</span><span class="sxs-lookup"><span data-stu-id="71cfe-1319">`edition`.</span></span> <span data-ttu-id="71cfe-1320">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1320">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="71cfe-1321">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="71cfe-1321">`elasticPoolName`.</span></span> <span data-ttu-id="71cfe-1322">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1322">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="71cfe-1323">[破壊的変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1323">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="71cfe-1324">`edition`</span><span class="sxs-lookup"><span data-stu-id="71cfe-1324">`edition`.</span></span> <span data-ttu-id="71cfe-1325">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1325">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="71cfe-1326">`dtu`</span><span class="sxs-lookup"><span data-stu-id="71cfe-1326">`dtu`.</span></span> <span data-ttu-id="71cfe-1327">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1327">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="71cfe-1328">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="71cfe-1328">`databaseDtuMin`.</span></span> <span data-ttu-id="71cfe-1329">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1329">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="71cfe-1330">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="71cfe-1330">`databaseDtuMax`.</span></span> <span data-ttu-id="71cfe-1331">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1331">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="71cfe-1332">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1332">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="71cfe-1333">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1333">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1334">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1334">Storage</span></span>

* <span data-ttu-id="71cfe-1335">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1335">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="71cfe-1336">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1336">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1337">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1337">VM</span></span>

* <span data-ttu-id="71cfe-1338">[破壊的変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1338">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="71cfe-1339">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="71cfe-1339">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="71cfe-1340">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1340">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="71cfe-1341">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1341">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="71cfe-1342">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1342">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="71cfe-1343">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1343">May 7, 2018</span></span>

<span data-ttu-id="71cfe-1344">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="71cfe-1344">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1345">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1345">Core</span></span>

* <span data-ttu-id="71cfe-1346">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1346">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="71cfe-1347">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1347">Added limited support for positional arguments</span></span>
* <span data-ttu-id="71cfe-1348">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1348">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="71cfe-1349">#5591</span><span class="sxs-lookup"><span data-stu-id="71cfe-1349">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="71cfe-1350">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1350">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="71cfe-1351">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="71cfe-1351">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="71cfe-1352">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1352">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="71cfe-1353">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1353">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="71cfe-1354">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1354">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-1355">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-1355">ACR</span></span>

* <span data-ttu-id="71cfe-1356">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1356">Added ACR Build commands</span></span>
* <span data-ttu-id="71cfe-1357">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1357">Improved resource not found error messages</span></span>
* <span data-ttu-id="71cfe-1358">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1358">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="71cfe-1359">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1359">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="71cfe-1360">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1360">Improved repository commands error messages</span></span>
* <span data-ttu-id="71cfe-1361">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1361">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1362">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1362">ACS</span></span>

* <span data-ttu-id="71cfe-1363">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1363">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="71cfe-1364">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1364">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="71cfe-1365">AMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1365">AMS</span></span>

* <span data-ttu-id="71cfe-1366">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="71cfe-1366">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1367">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-1367">Appservice</span></span>

* <span data-ttu-id="71cfe-1368">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1368">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="71cfe-1369">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1369">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="71cfe-1370">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1370">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="71cfe-1371">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1371">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="71cfe-1372">Batch AI</span><span class="sxs-lookup"><span data-stu-id="71cfe-1372">Batch AI</span></span>

* <span data-ttu-id="71cfe-1373">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1373">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="71cfe-1374">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="71cfe-1374">Cognitive Services</span></span>

* <span data-ttu-id="71cfe-1375">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1375">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="71cfe-1376">消費</span><span class="sxs-lookup"><span data-stu-id="71cfe-1376">Consumption</span></span>

* <span data-ttu-id="71cfe-1377">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1377">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-1378">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-1378">Container</span></span>

* <span data-ttu-id="71cfe-1379">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1379">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="71cfe-1380">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="71cfe-1380">Cosmos DB</span></span>

* <span data-ttu-id="71cfe-1381">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1381">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="71cfe-1382">DMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1382">DMS</span></span>

* <span data-ttu-id="71cfe-1383">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1383">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="71cfe-1384">拡張機能</span><span class="sxs-lookup"><span data-stu-id="71cfe-1384">Extension</span></span>

* <span data-ttu-id="71cfe-1385">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1385">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="71cfe-1386">Interactive</span><span class="sxs-lookup"><span data-stu-id="71cfe-1386">Interactive</span></span>

* <span data-ttu-id="71cfe-1387">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1387">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="71cfe-1388">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1388">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="71cfe-1389">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1389">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="71cfe-1390">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1390">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="71cfe-1391">ラボ</span><span class="sxs-lookup"><span data-stu-id="71cfe-1391">Lab</span></span>

* <span data-ttu-id="71cfe-1392">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1392">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1393">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1393">Network</span></span>

* <span data-ttu-id="71cfe-1394">[破壊的変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1394">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="71cfe-1395">プロファイル</span><span class="sxs-lookup"><span data-stu-id="71cfe-1395">Profile</span></span>

* <span data-ttu-id="71cfe-1396">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1396">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="71cfe-1397">[破壊的変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1397">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="71cfe-1398">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1398">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="71cfe-1399">Redis</span><span class="sxs-lookup"><span data-stu-id="71cfe-1399">Redis</span></span>

* <span data-ttu-id="71cfe-1400">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1400">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="71cfe-1401">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1401">Deprecated `redis list-all`.</span></span> <span data-ttu-id="71cfe-1402">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1402">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="71cfe-1403">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1403">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="71cfe-1404">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1404">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-1405">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-1405">Role</span></span>

* <span data-ttu-id="71cfe-1406">[破壊的変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1406">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1407">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1407">Storage</span></span>

* <span data-ttu-id="71cfe-1408">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="71cfe-1408">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="71cfe-1409">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1409">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="71cfe-1410">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="71cfe-1410">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="71cfe-1411">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="71cfe-1411">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="71cfe-1412">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1412">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1413">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1413">VM</span></span>

* <span data-ttu-id="71cfe-1414">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1414">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="71cfe-1415">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1415">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="71cfe-1416">[破壊的変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="71cfe-1416">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="71cfe-1417">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1417">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="71cfe-1418">[破壊的変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1418">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="71cfe-1419">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1419">Added write accelerator support</span></span>
* <span data-ttu-id="71cfe-1420">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1420">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="71cfe-1421">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1421">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="71cfe-1422">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1422">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="71cfe-1423">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1423">April 10, 2018</span></span>

<span data-ttu-id="71cfe-1424">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="71cfe-1424">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-1425">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-1425">ACR</span></span>

* <span data-ttu-id="71cfe-1426">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1426">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1427">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1427">ACS</span></span>

* <span data-ttu-id="71cfe-1428">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1428">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1429">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-1429">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="71cfe-1431">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1431">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="71cfe-1432">BatchAI</span><span class="sxs-lookup"><span data-stu-id="71cfe-1432">BatchAI</span></span>

* <span data-ttu-id="71cfe-1433">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1433">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="71cfe-1434">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="71cfe-1434">Job level mounting</span></span>
  - <span data-ttu-id="71cfe-1435">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="71cfe-1435">Environment variables with secret values</span></span>
  - <span data-ttu-id="71cfe-1436">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="71cfe-1436">Performance counters settings</span></span>
  - <span data-ttu-id="71cfe-1437">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="71cfe-1437">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="71cfe-1438">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="71cfe-1438">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="71cfe-1439">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="71cfe-1439">Usage and limits reporting</span></span>
  - <span data-ttu-id="71cfe-1440">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="71cfe-1440">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="71cfe-1441">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="71cfe-1441">Support for custom images</span></span>
  - <span data-ttu-id="71cfe-1442">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1442">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="71cfe-1443">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-1443">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="71cfe-1444">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1444">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="71cfe-1445">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="71cfe-1445">National clouds are supported</span></span>
* <span data-ttu-id="71cfe-1446">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1446">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="71cfe-1447">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1447">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="71cfe-1448">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1448">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="71cfe-1449">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1449">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="71cfe-1450">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="71cfe-1450">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="71cfe-1451">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="71cfe-1451">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="71cfe-1452">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1452">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="71cfe-1453">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1453">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="71cfe-1454">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="71cfe-1454">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="71cfe-1455">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1455">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="71cfe-1456">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1456">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="71cfe-1457">[破壊的変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1457">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="71cfe-1458">[破壊的変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1458">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="71cfe-1459">課金</span><span class="sxs-lookup"><span data-stu-id="71cfe-1459">Billing</span></span>

* <span data-ttu-id="71cfe-1460">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1460">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="71cfe-1461">消費</span><span class="sxs-lookup"><span data-stu-id="71cfe-1461">Consumption</span></span>

* <span data-ttu-id="71cfe-1462">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1462">Added `marketplace` commands</span></span>
* <span data-ttu-id="71cfe-1463">[破壊的変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1463">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="71cfe-1464">[破壊的変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1464">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="71cfe-1465">[破壊的変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1465">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="71cfe-1466">[破壊的変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1466">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="71cfe-1467">[破壊的変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1467">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-1468">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-1468">Container</span></span>

* <span data-ttu-id="71cfe-1469">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1469">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="71cfe-1470">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1470">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="71cfe-1471">拡張機能</span><span class="sxs-lookup"><span data-stu-id="71cfe-1471">Extension</span></span>

* <span data-ttu-id="71cfe-1472">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1472">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="71cfe-1473">Interactive</span><span class="sxs-lookup"><span data-stu-id="71cfe-1473">Interactive</span></span>

* <span data-ttu-id="71cfe-1474">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1474">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="71cfe-1475">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1475">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="71cfe-1476">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1476">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1477">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1477">Network</span></span>

* <span data-ttu-id="71cfe-1478">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1478">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="71cfe-1479">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1479">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="71cfe-1480">#4910</span><span class="sxs-lookup"><span data-stu-id="71cfe-1480">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="71cfe-1481">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1481">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="71cfe-1482">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1482">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="71cfe-1483">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1483">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="71cfe-1484">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1484">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="71cfe-1485">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1485">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="71cfe-1486">プロファイル</span><span class="sxs-lookup"><span data-stu-id="71cfe-1486">Profile</span></span>

* <span data-ttu-id="71cfe-1487">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1487">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="71cfe-1488">[破壊的変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1488">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="71cfe-1489">RDBMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1489">RDBMS</span></span>

* <span data-ttu-id="71cfe-1490">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1490">Added `georestore` command</span></span>
* <span data-ttu-id="71cfe-1491">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1491">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-1492">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-1492">Resource</span></span>

* <span data-ttu-id="71cfe-1493">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1493">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="71cfe-1494">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1494">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-1495">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-1495">SQL</span></span>

* <span data-ttu-id="71cfe-1496">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1496">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1497">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1497">Storage</span></span>

* <span data-ttu-id="71cfe-1498">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1498">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1499">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1499">VM</span></span>

* <span data-ttu-id="71cfe-1500">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1500">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="71cfe-1501">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1501">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="71cfe-1503">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1503">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="71cfe-1504">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1504">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="71cfe-1505">#5718</span><span class="sxs-lookup"><span data-stu-id="71cfe-1505">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="71cfe-1506">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1506">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="71cfe-1507">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1507">March 27, 2018</span></span>

<span data-ttu-id="71cfe-1508">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="71cfe-1508">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1509">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1509">Core</span></span>

* <span data-ttu-id="71cfe-1510">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1510">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1511">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1511">ACS</span></span>

* <span data-ttu-id="71cfe-1512">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1512">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1513">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-1513">Appservice</span></span>

* <span data-ttu-id="71cfe-1514">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1514">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="71cfe-1515">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1515">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="71cfe-1516">バックアップ</span><span class="sxs-lookup"><span data-stu-id="71cfe-1516">Backup</span></span>

* <span data-ttu-id="71cfe-1517">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1517">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="71cfe-1518">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="71cfe-1518">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="71cfe-1519">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1519">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="71cfe-1520">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1520">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-1521">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-1521">Container</span></span>

* <span data-ttu-id="71cfe-1522">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1522">Added `container exec` command.</span></span> <span data-ttu-id="71cfe-1523">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1523">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="71cfe-1524">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-1524">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="71cfe-1525">拡張機能</span><span class="sxs-lookup"><span data-stu-id="71cfe-1525">Extension</span></span>

* <span data-ttu-id="71cfe-1526">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1526">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="71cfe-1527">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1527">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="71cfe-1528">[破壊的変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1528">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="71cfe-1529">Interactive</span><span class="sxs-lookup"><span data-stu-id="71cfe-1529">Interactive</span></span>

* <span data-ttu-id="71cfe-1530">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1530">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="71cfe-1531">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1531">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="71cfe-1532">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1532">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="71cfe-1533">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1533">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="71cfe-1534">ラボ</span><span class="sxs-lookup"><span data-stu-id="71cfe-1534">Lab</span></span>

* <span data-ttu-id="71cfe-1535">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1535">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-1536">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-1536">Monitor</span></span>

* <span data-ttu-id="71cfe-1537">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="71cfe-1537">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="71cfe-1538">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="71cfe-1538">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="71cfe-1539">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="71cfe-1539">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1540">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1540">Network</span></span>

* <span data-ttu-id="71cfe-1541">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1541">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="71cfe-1542">プロファイル</span><span class="sxs-lookup"><span data-stu-id="71cfe-1542">Profile</span></span>

* <span data-ttu-id="71cfe-1543">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1543">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="71cfe-1544">RDBMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1544">RDBMS</span></span>

* <span data-ttu-id="71cfe-1545">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1545">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-1546">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-1546">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="71cfe-1548">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-1548">Role</span></span>

* <span data-ttu-id="71cfe-1549">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1549">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="71cfe-1550">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1550">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="71cfe-1551">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1551">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="71cfe-1552">[破壊的変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1552">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="71cfe-1553">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1553">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1554">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1554">Storage</span></span>

* <span data-ttu-id="71cfe-1555">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1555">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="71cfe-1556">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="71cfe-1556">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1557">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1557">VM</span></span>

* <span data-ttu-id="71cfe-1558">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1558">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="71cfe-1559">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1559">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="71cfe-1560">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1560">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="71cfe-1561">[破壊的変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1561">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="71cfe-1562">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1562">March 13, 2018</span></span>

<span data-ttu-id="71cfe-1563">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="71cfe-1563">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-1564">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-1564">ACR</span></span>

* <span data-ttu-id="71cfe-1565">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1565">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="71cfe-1566">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1566">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="71cfe-1567">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1567">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1568">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1568">ACS</span></span>

* <span data-ttu-id="71cfe-1569">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1569">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="71cfe-1570">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1570">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="71cfe-1571">Advisor</span><span class="sxs-lookup"><span data-stu-id="71cfe-1571">Advisor</span></span>

* <span data-ttu-id="71cfe-1572">[破壊的変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1572">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="71cfe-1573">[破壊的変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1573">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="71cfe-1574">[破壊的変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1574">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="71cfe-1575">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1575">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="71cfe-1576">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1576">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1577">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-1577">Appservice</span></span>

* <span data-ttu-id="71cfe-1578">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1578">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="71cfe-1579">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1579">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="71cfe-1580">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="71cfe-1580">Eventhubs</span></span>

* <span data-ttu-id="71cfe-1581">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-1581">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="71cfe-1582">拡張機能</span><span class="sxs-lookup"><span data-stu-id="71cfe-1582">Extension</span></span>

* <span data-ttu-id="71cfe-1583">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1583">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="71cfe-1584">Interactive</span><span class="sxs-lookup"><span data-stu-id="71cfe-1584">Interactive</span></span>

* <span data-ttu-id="71cfe-1585">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-1585">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="71cfe-1586">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="71cfe-1586">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="71cfe-1587">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="71cfe-1587">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="71cfe-1588">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1588">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-1589">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-1589">Monitor</span></span>

* <span data-ttu-id="71cfe-1590">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1590">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="71cfe-1591">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1591">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="71cfe-1592">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1592">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="71cfe-1593">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1593">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1594">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1594">Network</span></span>

* <span data-ttu-id="71cfe-1595">[破壊的変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1595">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="71cfe-1596">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1596">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="71cfe-1597">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1597">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="71cfe-1598">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1598">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="71cfe-1599">プロファイル</span><span class="sxs-lookup"><span data-stu-id="71cfe-1599">Profile</span></span>

* <span data-ttu-id="71cfe-1600">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1600">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="71cfe-1601">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1601">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="71cfe-1602">RDBMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1602">RDBMS</span></span>

* <span data-ttu-id="71cfe-1603">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1603">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="71cfe-1604">Service Bus</span><span class="sxs-lookup"><span data-stu-id="71cfe-1604">Service Bus</span></span>

* <span data-ttu-id="71cfe-1605">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-1605">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1606">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1606">Storage</span></span>

* <span data-ttu-id="71cfe-1607">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1607">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="71cfe-1608">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1608">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1609">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1609">VM</span></span>

* <span data-ttu-id="71cfe-1610">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1610">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="71cfe-1611">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1611">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="71cfe-1612">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1612">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="71cfe-1613">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1613">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="71cfe-1614">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1614">February 27, 2018</span></span>

<span data-ttu-id="71cfe-1615">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="71cfe-1615">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1616">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1616">Core</span></span>

* <span data-ttu-id="71cfe-1617">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="71cfe-1617">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="71cfe-1618">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1618">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="71cfe-1619">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1619">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1620">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1620">ACS</span></span>

* <span data-ttu-id="71cfe-1621">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1621">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="71cfe-1622">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="71cfe-1622">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="71cfe-1623">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1623">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="71cfe-1624">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1624">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1625">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-1625">Appservice</span></span>

* <span data-ttu-id="71cfe-1626">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="71cfe-1626">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="71cfe-1627">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="71cfe-1627">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="71cfe-1628">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="71cfe-1628">Cognitive Services</span></span>

* <span data-ttu-id="71cfe-1629">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1629">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="71cfe-1630">消費</span><span class="sxs-lookup"><span data-stu-id="71cfe-1630">Consumption</span></span>

* <span data-ttu-id="71cfe-1631">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1631">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="71cfe-1632">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1632">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-1633">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-1633">Container</span></span>

* <span data-ttu-id="71cfe-1634">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1634">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1635">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1635">Network</span></span>

* <span data-ttu-id="71cfe-1636">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="71cfe-1636">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-1637">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-1637">Resource</span></span>

* <span data-ttu-id="71cfe-1638">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1638">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-1639">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-1639">Role</span></span>

* <span data-ttu-id="71cfe-1640">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1640">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-1641">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-1641">SQL</span></span>

* <span data-ttu-id="71cfe-1642">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1642">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1643">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1643">Storage</span></span>

* <span data-ttu-id="71cfe-1644">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1644">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1645">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1645">VM</span></span>

* <span data-ttu-id="71cfe-1646">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1646">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="71cfe-1647">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1647">February 13, 2018</span></span>

<span data-ttu-id="71cfe-1648">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="71cfe-1648">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1649">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1649">Core</span></span>

* <span data-ttu-id="71cfe-1650">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1650">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1651">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1651">ACS</span></span>

* <span data-ttu-id="71cfe-1652">[破壊的変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1652">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="71cfe-1653">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1653">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="71cfe-1654">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1654">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="71cfe-1655">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1655">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="71cfe-1656">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1656">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="71cfe-1657">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1657">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="71cfe-1658">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1658">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="71cfe-1659">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="71cfe-1659">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1660">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-1660">Appservice</span></span>

* <span data-ttu-id="71cfe-1661">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1661">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="71cfe-1662">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1662">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="71cfe-1663">CDN</span><span class="sxs-lookup"><span data-stu-id="71cfe-1663">CDN</span></span>

* <span data-ttu-id="71cfe-1664">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1664">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-1665">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-1665">Container</span></span>

* <span data-ttu-id="71cfe-1666">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1666">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="71cfe-1667">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1667">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="71cfe-1668">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="71cfe-1668">CosmosDB</span></span>

* <span data-ttu-id="71cfe-1669">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1669">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="71cfe-1670">拡張機能</span><span class="sxs-lookup"><span data-stu-id="71cfe-1670">Extension</span></span>

* <span data-ttu-id="71cfe-1671">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1671">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="71cfe-1672">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1672">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="71cfe-1673">フィードバック</span><span class="sxs-lookup"><span data-stu-id="71cfe-1673">Feedback</span></span>

* <span data-ttu-id="71cfe-1674">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1674">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="71cfe-1675">Interactive</span><span class="sxs-lookup"><span data-stu-id="71cfe-1675">Interactive</span></span>

* <span data-ttu-id="71cfe-1676">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1676">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="71cfe-1677">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1677">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="71cfe-1678">IoT</span><span class="sxs-lookup"><span data-stu-id="71cfe-1678">IoT</span></span>

* <span data-ttu-id="71cfe-1679">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1679">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="71cfe-1680">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1680">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="71cfe-1681">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1681">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="71cfe-1682">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1682">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-1683">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-1683">Monitor</span></span>

* <span data-ttu-id="71cfe-1684">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1684">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1685">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1685">Network</span></span>

* <span data-ttu-id="71cfe-1686">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1686">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="71cfe-1687">プロファイル</span><span class="sxs-lookup"><span data-stu-id="71cfe-1687">Profile</span></span>

* <span data-ttu-id="71cfe-1688">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1688">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-1689">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-1689">Resource</span></span>

* <span data-ttu-id="71cfe-1690">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1690">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-1691">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-1691">Role</span></span>

* <span data-ttu-id="71cfe-1692">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1692">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-1693">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-1693">SQL</span></span>

* <span data-ttu-id="71cfe-1694">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1694">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="71cfe-1695">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1695">Added `sql db rename`</span></span>
* <span data-ttu-id="71cfe-1696">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1696">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1697">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1697">Storage</span></span>

* <span data-ttu-id="71cfe-1698">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1698">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1699">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1699">VM</span></span>

* <span data-ttu-id="71cfe-1700">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1700">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="71cfe-1701">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1701">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="71cfe-1702">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="71cfe-1702">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="71cfe-1703">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1703">January 31, 2018</span></span>

<span data-ttu-id="71cfe-1704">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="71cfe-1704">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1705">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1705">Core</span></span>

* <span data-ttu-id="71cfe-1706">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1706">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="71cfe-1707">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1707">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="71cfe-1708">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1708">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="71cfe-1709">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1709">Use `--verbose` to see</span></span>
* <span data-ttu-id="71cfe-1710">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="71cfe-1710">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1711">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1711">ACS</span></span>

* <span data-ttu-id="71cfe-1712">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1712">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="71cfe-1713">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1713">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1714">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-1714">Appservice</span></span>

* <span data-ttu-id="71cfe-1715">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="71cfe-1715">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="71cfe-1716">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1716">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="71cfe-1717">CDN</span><span class="sxs-lookup"><span data-stu-id="71cfe-1717">CDN</span></span>

* <span data-ttu-id="71cfe-1718">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1718">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="71cfe-1719">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="71cfe-1719">CosmosDB</span></span>

* <span data-ttu-id="71cfe-1720">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1720">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="71cfe-1721">Interactive</span><span class="sxs-lookup"><span data-stu-id="71cfe-1721">Interactive</span></span>

* <span data-ttu-id="71cfe-1722">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1722">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1723">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1723">Network</span></span>

* <span data-ttu-id="71cfe-1724">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1724">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="71cfe-1725">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1725">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="71cfe-1726">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1726">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="71cfe-1727">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1727">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="71cfe-1728">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1728">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="71cfe-1729">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1729">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="71cfe-1730">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1730">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="71cfe-1731">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1731">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="71cfe-1732">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1732">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="71cfe-1733">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1733">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="71cfe-1734">プロファイル</span><span class="sxs-lookup"><span data-stu-id="71cfe-1734">Profile</span></span>

* <span data-ttu-id="71cfe-1735">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1735">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-1736">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-1736">Resource</span></span>

* <span data-ttu-id="71cfe-1737">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1737">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1738">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1738">Storage</span></span>

* <span data-ttu-id="71cfe-1739">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1739">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="71cfe-1740">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1740">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="71cfe-1741">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1741">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="71cfe-1742">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1742">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="71cfe-1743">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1743">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1744">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1744">VM</span></span>

* <span data-ttu-id="71cfe-1745">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1745">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="71cfe-1746">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1746">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="71cfe-1747">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1747">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="71cfe-1748">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1748">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="71cfe-1749">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1749">January 17, 2018</span></span>

<span data-ttu-id="71cfe-1750">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="71cfe-1750">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-1751">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-1751">ACR</span></span>

* <span data-ttu-id="71cfe-1752">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1752">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="71cfe-1753">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1753">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1754">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1754">ACS</span></span>

* <span data-ttu-id="71cfe-1755">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1755">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="71cfe-1756">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1756">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1757">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-1757">Appservice</span></span>

* <span data-ttu-id="71cfe-1758">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1758">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="71cfe-1759">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1759">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="71cfe-1760">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1760">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="71cfe-1761">バックアップ</span><span class="sxs-lookup"><span data-stu-id="71cfe-1761">Backup</span></span>

* <span data-ttu-id="71cfe-1762">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1762">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="71cfe-1763">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1763">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="71cfe-1764">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1764">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="71cfe-1765">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1765">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="71cfe-1766">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1766">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="71cfe-1767">Batch</span><span class="sxs-lookup"><span data-stu-id="71cfe-1767">Batch</span></span>

* <span data-ttu-id="71cfe-1768">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1768">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="71cfe-1769">クラウド</span><span class="sxs-lookup"><span data-stu-id="71cfe-1769">Cloud</span></span>

* <span data-ttu-id="71cfe-1770">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1770">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="71cfe-1771">消費</span><span class="sxs-lookup"><span data-stu-id="71cfe-1771">Consumption</span></span>

* <span data-ttu-id="71cfe-1772">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1772">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="71cfe-1773">Event Grid</span><span class="sxs-lookup"><span data-stu-id="71cfe-1773">Event Grid</span></span>

* <span data-ttu-id="71cfe-1774">[破壊的変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1774">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="71cfe-1775">[破壊的変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1775">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="71cfe-1776">[破壊的変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1776">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="71cfe-1777">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="71cfe-1777">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="71cfe-1778">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1778">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="71cfe-1779">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1779">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="71cfe-1780">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1780">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="71cfe-1781">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1781">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="71cfe-1782">Interactive</span><span class="sxs-lookup"><span data-stu-id="71cfe-1782">Interactive</span></span>

* <span data-ttu-id="71cfe-1783">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1783">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="71cfe-1784">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1784">Fixed errors on startup</span></span>
* <span data-ttu-id="71cfe-1785">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1785">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="71cfe-1786">IoT</span><span class="sxs-lookup"><span data-stu-id="71cfe-1786">IoT</span></span>

* <span data-ttu-id="71cfe-1787">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1787">Added support for device provisioning service</span></span>
* <span data-ttu-id="71cfe-1788">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1788">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="71cfe-1789">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1789">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-1790">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-1790">Monitor</span></span>

* <span data-ttu-id="71cfe-1791">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1791">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="71cfe-1792">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1792">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="71cfe-1793">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1793">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1794">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1794">Network</span></span>

* <span data-ttu-id="71cfe-1795">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1795">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="71cfe-1796">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1796">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="71cfe-1797">プロファイル</span><span class="sxs-lookup"><span data-stu-id="71cfe-1797">Profile</span></span>

* <span data-ttu-id="71cfe-1798">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1798">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-1799">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-1799">Role</span></span>

* <span data-ttu-id="71cfe-1800">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1800">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="71cfe-1801">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="71cfe-1801">Service Fabric</span></span>

* <span data-ttu-id="71cfe-1802">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1802">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="71cfe-1803">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1803">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1804">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1804">VM</span></span>

* <span data-ttu-id="71cfe-1805">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="71cfe-1805">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="71cfe-1806">[破壊的変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1806">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="71cfe-1807">[破壊的変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1807">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="71cfe-1808">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1808">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="71cfe-1809">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1809">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="71cfe-1810">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1810">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="71cfe-1811">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1811">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="71cfe-1812">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1812">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="71cfe-1813">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1813">December 19, 2017</span></span>

<span data-ttu-id="71cfe-1814">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="71cfe-1814">Version 2.0.23</span></span>

* <span data-ttu-id="71cfe-1815">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1815">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-1816">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-1816">Container</span></span>

* <span data-ttu-id="71cfe-1817">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1817">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1818">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1818">Network</span></span>

* <span data-ttu-id="71cfe-1819">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1819">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="71cfe-1820">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1820">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1821">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1821">Storage</span></span>

* <span data-ttu-id="71cfe-1822">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1822">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1823">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1823">VM</span></span>

* <span data-ttu-id="71cfe-1824">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1824">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="71cfe-1825">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1825">December 5, 2017</span></span>

<span data-ttu-id="71cfe-1826">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="71cfe-1826">Version 2.0.22</span></span>

* <span data-ttu-id="71cfe-1827">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1827">Removed `az component` commands.</span></span> <span data-ttu-id="71cfe-1828">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="71cfe-1828">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1829">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1829">Core</span></span>
* <span data-ttu-id="71cfe-1830">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1830">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="71cfe-1831">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1831">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1832">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1832">ACS</span></span>

* <span data-ttu-id="71cfe-1833">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1833">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="71cfe-1834">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1834">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="71cfe-1835">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1835">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="71cfe-1836">Advisor</span><span class="sxs-lookup"><span data-stu-id="71cfe-1836">Advisor</span></span>

* <span data-ttu-id="71cfe-1837">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-1837">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1838">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-1838">Appservice</span></span>

* <span data-ttu-id="71cfe-1839">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1839">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="71cfe-1840">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1840">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="71cfe-1841">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1841">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="71cfe-1842">消費</span><span class="sxs-lookup"><span data-stu-id="71cfe-1842">Consumption</span></span>

* <span data-ttu-id="71cfe-1843">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1843">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-1844">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-1844">Container</span></span>

* <span data-ttu-id="71cfe-1845">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1845">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-1846">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-1846">Monitor</span></span>

* <span data-ttu-id="71cfe-1847">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1847">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-1848">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-1848">Resource</span></span>

* <span data-ttu-id="71cfe-1849">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1849">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-1850">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-1850">Role</span></span>

* <span data-ttu-id="71cfe-1851">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1851">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="71cfe-1852">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1852">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="71cfe-1853">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1853">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-1854">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-1854">SQL</span></span>

* <span data-ttu-id="71cfe-1855">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1855">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="71cfe-1856">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1856">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1857">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1857">VM</span></span>

* <span data-ttu-id="71cfe-1858">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1858">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="71cfe-1859">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1859">November 14, 2017</span></span>

<span data-ttu-id="71cfe-1860">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="71cfe-1860">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-1861">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-1861">ACR</span></span>

* <span data-ttu-id="71cfe-1862">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1862">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="71cfe-1863">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1863">ACS</span></span>

* <span data-ttu-id="71cfe-1864">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1864">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="71cfe-1865">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1865">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="71cfe-1866">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1866">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="71cfe-1867">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1867">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="71cfe-1868">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1868">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1869">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-1869">Appservice</span></span>

* <span data-ttu-id="71cfe-1870">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1870">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="71cfe-1871">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1871">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="71cfe-1872">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1872">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="71cfe-1873">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1873">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="71cfe-1874">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1874">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="71cfe-1875">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="71cfe-1875">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="71cfe-1876">Batch</span><span class="sxs-lookup"><span data-stu-id="71cfe-1876">Batch</span></span>

* <span data-ttu-id="71cfe-1877">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1877">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="71cfe-1878">Batchai</span><span class="sxs-lookup"><span data-stu-id="71cfe-1878">Batchai</span></span>

* <span data-ttu-id="71cfe-1879">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1879">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="71cfe-1880">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1880">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="71cfe-1881">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1881">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="71cfe-1882">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1882">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="71cfe-1883">クラウド</span><span class="sxs-lookup"><span data-stu-id="71cfe-1883">Cloud</span></span>

* <span data-ttu-id="71cfe-1884">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1884">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-1885">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-1885">Container</span></span>

* <span data-ttu-id="71cfe-1886">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1886">Added support to open multiple ports</span></span>
* <span data-ttu-id="71cfe-1887">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1887">Added container group restart policy</span></span>
* <span data-ttu-id="71cfe-1888">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1888">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="71cfe-1889">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1889">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="71cfe-1890">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="71cfe-1890">Data Lake Analytics</span></span>

* <span data-ttu-id="71cfe-1891">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1891">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="71cfe-1892">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="71cfe-1892">Data Lake Store</span></span>

* <span data-ttu-id="71cfe-1893">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1893">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="71cfe-1894">拡張機能</span><span class="sxs-lookup"><span data-stu-id="71cfe-1894">Extension</span></span>

* <span data-ttu-id="71cfe-1895">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1895">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="71cfe-1896">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1896">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="71cfe-1897">IoT</span><span class="sxs-lookup"><span data-stu-id="71cfe-1897">IoT</span></span>

* <span data-ttu-id="71cfe-1898">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1898">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-1899">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-1899">Monitor</span></span>

* <span data-ttu-id="71cfe-1900">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1900">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1901">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1901">Network</span></span>

* <span data-ttu-id="71cfe-1902">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1902">Added support for CAA DNS records</span></span>
* <span data-ttu-id="71cfe-1903">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1903">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="71cfe-1904">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1904">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="71cfe-1905">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1905">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="71cfe-1906">Reservations</span><span class="sxs-lookup"><span data-stu-id="71cfe-1906">Reservations</span></span>

* <span data-ttu-id="71cfe-1907">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-1907">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-1908">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-1908">Resource</span></span>

* <span data-ttu-id="71cfe-1909">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1909">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-1910">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-1910">SQL</span></span>

* <span data-ttu-id="71cfe-1911">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1911">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1912">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1912">Storage</span></span>

* <span data-ttu-id="71cfe-1913">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1913">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="71cfe-1914">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1914">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="71cfe-1915">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1915">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="71cfe-1916">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1916">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="71cfe-1917">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1917">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="71cfe-1918">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1918">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="71cfe-1919">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1919">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1920">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1920">VM</span></span>

* <span data-ttu-id="71cfe-1921">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1921">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="71cfe-1922">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1922">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="71cfe-1923">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1923">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="71cfe-1924">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1924">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="71cfe-1925">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1925">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="71cfe-1926">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1926">October 24, 2017</span></span>

<span data-ttu-id="71cfe-1927">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="71cfe-1927">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1928">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1928">Core</span></span>

* <span data-ttu-id="71cfe-1929">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1929">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-1930">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-1930">ACR</span></span>

* <span data-ttu-id="71cfe-1931">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1931">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="71cfe-1932">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1932">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="71cfe-1933">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1933">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-1934">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-1934">ACS</span></span>

* <span data-ttu-id="71cfe-1935">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1935">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="71cfe-1936">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1936">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1937">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-1937">Appservice</span></span>

* <span data-ttu-id="71cfe-1938">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1938">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="71cfe-1939">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="71cfe-1939">Component</span></span>

* <span data-ttu-id="71cfe-1940">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1940">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-1941">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-1941">Monitor</span></span>

* <span data-ttu-id="71cfe-1942">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1942">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-1943">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-1943">Resource</span></span>

* <span data-ttu-id="71cfe-1944">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1944">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="71cfe-1945">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1945">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1946">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1946">VM</span></span>

* <span data-ttu-id="71cfe-1947">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1947">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="71cfe-1948">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1948">October 9, 2017</span></span>

<span data-ttu-id="71cfe-1949">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="71cfe-1949">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-1950">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-1950">Core</span></span>

* <span data-ttu-id="71cfe-1951">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1951">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-1952">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-1952">Appservice</span></span>

* <span data-ttu-id="71cfe-1953">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1953">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="71cfe-1954">Batch</span><span class="sxs-lookup"><span data-stu-id="71cfe-1954">Batch</span></span>

* <span data-ttu-id="71cfe-1955">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1955">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="71cfe-1956">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1956">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="71cfe-1957">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1957">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="71cfe-1958">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1958">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="71cfe-1959">Batchai</span><span class="sxs-lookup"><span data-stu-id="71cfe-1959">Batchai</span></span>

* <span data-ttu-id="71cfe-1960">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-1960">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="71cfe-1961">KeyVault</span><span class="sxs-lookup"><span data-stu-id="71cfe-1961">Keyvault</span></span>

* <span data-ttu-id="71cfe-1962">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1962">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="71cfe-1963">(#4448)</span><span class="sxs-lookup"><span data-stu-id="71cfe-1963">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="71cfe-1964">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1964">Network</span></span>

* <span data-ttu-id="71cfe-1965">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1965">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="71cfe-1966">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1966">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-1967">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-1967">Resource</span></span>

* <span data-ttu-id="71cfe-1968">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1968">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="71cfe-1969">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1969">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="71cfe-1970">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1970">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="71cfe-1971">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1971">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-1972">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-1972">Sql</span></span>

* <span data-ttu-id="71cfe-1973">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1973">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="71cfe-1974">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1974">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="71cfe-1975">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-1975">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1976">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1976">Storage</span></span>

* <span data-ttu-id="71cfe-1977">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1977">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-1978">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-1978">Vm</span></span>

* <span data-ttu-id="71cfe-1979">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1979">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="71cfe-1980">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1980">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="71cfe-1981">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1981">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="71cfe-1982">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1982">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="71cfe-1983">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1983">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="71cfe-1984">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-1984">September 22, 2017</span></span>

<span data-ttu-id="71cfe-1985">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="71cfe-1985">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-1986">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-1986">Resource</span></span>

* <span data-ttu-id="71cfe-1987">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1987">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="71cfe-1988">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1988">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="71cfe-1989">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1989">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="71cfe-1990">[破壊的変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1990">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-1991">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-1991">Network</span></span>

* <span data-ttu-id="71cfe-1992">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1992">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="71cfe-1993">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1993">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="71cfe-1994">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1994">Added `asg` application security group commands</span></span>
* <span data-ttu-id="71cfe-1995">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1995">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="71cfe-1996">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1996">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="71cfe-1997">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1997">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="71cfe-1998">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-1998">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-1999">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-1999">Storage</span></span>

* <span data-ttu-id="71cfe-2000">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2000">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="71cfe-2001">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="71cfe-2001">Eventgrid</span></span>

* <span data-ttu-id="71cfe-2002">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2002">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-2003">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-2003">SQL</span></span>

* <span data-ttu-id="71cfe-2004">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2004">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="71cfe-2005">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-2005">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="71cfe-2006">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2006">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="71cfe-2007">KeyVault</span><span class="sxs-lookup"><span data-stu-id="71cfe-2007">Keyvault</span></span>

* <span data-ttu-id="71cfe-2008">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2008">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-2009">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-2009">VM</span></span>

* <span data-ttu-id="71cfe-2010">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2010">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="71cfe-2011">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2011">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="71cfe-2012">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2012">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="71cfe-2013">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2013">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="71cfe-2014">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2014">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="71cfe-2015">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2015">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-2016">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-2016">ACS</span></span>

* <span data-ttu-id="71cfe-2017">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2017">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-2018">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-2018">Appservice</span></span>

* <span data-ttu-id="71cfe-2019">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2019">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="71cfe-2020">バックアップ</span><span class="sxs-lookup"><span data-stu-id="71cfe-2020">Backup</span></span>

* <span data-ttu-id="71cfe-2021">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-2021">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="71cfe-2022">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-2022">September 11, 2017</span></span>

<span data-ttu-id="71cfe-2023">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="71cfe-2023">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="71cfe-2024">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-2024">Core</span></span>

* <span data-ttu-id="71cfe-2025">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2025">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="71cfe-2026">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2026">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-2027">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-2027">Acs</span></span>

* <span data-ttu-id="71cfe-2028">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2028">Added `acs list-locations` command</span></span>
* <span data-ttu-id="71cfe-2029">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2029">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-2030">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-2030">Appservice</span></span>

* <span data-ttu-id="71cfe-2031">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2031">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="71cfe-2032">CDN</span><span class="sxs-lookup"><span data-stu-id="71cfe-2032">CDN</span></span>

* <span data-ttu-id="71cfe-2033">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2033">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="71cfe-2034">拡張機能</span><span class="sxs-lookup"><span data-stu-id="71cfe-2034">Extension</span></span>

* <span data-ttu-id="71cfe-2035">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-2035">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="71cfe-2036">KeyVault</span><span class="sxs-lookup"><span data-stu-id="71cfe-2036">Keyvault</span></span>

* <span data-ttu-id="71cfe-2037">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2037">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-2038">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-2038">Network</span></span>

* <span data-ttu-id="71cfe-2039">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2039">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="71cfe-2040">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2040">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="71cfe-2041">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2041">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="71cfe-2042">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2042">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="71cfe-2043">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2043">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-2044">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-2044">Resource</span></span>

* <span data-ttu-id="71cfe-2045">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2045">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="71cfe-2046">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2046">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="71cfe-2047">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2047">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="71cfe-2048">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2048">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-2049">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-2049">SQL</span></span>

* <span data-ttu-id="71cfe-2050">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2050">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-2051">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-2051">VM</span></span>

* <span data-ttu-id="71cfe-2052">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="71cfe-2052">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="71cfe-2053">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="71cfe-2053">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="71cfe-2054">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2054">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="71cfe-2055">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="71cfe-2055">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="71cfe-2056">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="71cfe-2056">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="71cfe-2057">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-2057">August 31, 2017</span></span>

<span data-ttu-id="71cfe-2058">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="71cfe-2058">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="71cfe-2059">KeyVault</span><span class="sxs-lookup"><span data-stu-id="71cfe-2059">Keyvault</span></span>

* <span data-ttu-id="71cfe-2060">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2060">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="71cfe-2061">SF</span><span class="sxs-lookup"><span data-stu-id="71cfe-2061">Sf</span></span>

* <span data-ttu-id="71cfe-2062">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-2062">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-2063">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-2063">Storage</span></span>

* <span data-ttu-id="71cfe-2064">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2064">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="71cfe-2065">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2065">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="71cfe-2066">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-2066">August 28, 2017</span></span>

<span data-ttu-id="71cfe-2067">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="71cfe-2067">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="71cfe-2068">CLI</span><span class="sxs-lookup"><span data-stu-id="71cfe-2068">CLI</span></span>

* <span data-ttu-id="71cfe-2069">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2069">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-2070">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-2070">ACS</span></span>

* <span data-ttu-id="71cfe-2071">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2071">Corrected preview regions</span></span>
* <span data-ttu-id="71cfe-2072">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2072">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="71cfe-2073">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2073">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-2074">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-2074">Appservice</span></span>

* <span data-ttu-id="71cfe-2075">[破壊的変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2075">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="71cfe-2076">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2076">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="71cfe-2077">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2077">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="71cfe-2078">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2078">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="71cfe-2079">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="71cfe-2079">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="71cfe-2080">IoT</span><span class="sxs-lookup"><span data-stu-id="71cfe-2080">IoT</span></span>

* <span data-ttu-id="71cfe-2081">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2081">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-2082">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-2082">Network</span></span>

* <span data-ttu-id="71cfe-2083">[破壊的変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2083">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="71cfe-2084">[破壊的変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2084">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="71cfe-2085">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2085">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="71cfe-2086">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2086">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="71cfe-2087">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2087">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="71cfe-2088">プロファイル</span><span class="sxs-lookup"><span data-stu-id="71cfe-2088">Profile</span></span>

* <span data-ttu-id="71cfe-2089">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2089">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="71cfe-2090">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="71cfe-2090">Service Fabric</span></span>

* <span data-ttu-id="71cfe-2091">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-2091">Preview release</span></span>
* <span data-ttu-id="71cfe-2092">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2092">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="71cfe-2093">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2093">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="71cfe-2094">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2094">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-2095">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-2095">Storage</span></span>

* <span data-ttu-id="71cfe-2096">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2096">Enabled setting blob tier</span></span>
* <span data-ttu-id="71cfe-2097">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2097">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="71cfe-2098">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2098">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="71cfe-2099">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2099">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="71cfe-2100">[破壊的変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2100">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="71cfe-2101">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="71cfe-2101">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-2102">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-2102">VM</span></span>

* <span data-ttu-id="71cfe-2103">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2103">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="71cfe-2104">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2104">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="71cfe-2105">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2105">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="71cfe-2106">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2106">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="71cfe-2107">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2107">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="71cfe-2108">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2108">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="71cfe-2109">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-2109">August 15, 2017</span></span>

<span data-ttu-id="71cfe-2110">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="71cfe-2110">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-2111">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-2111">ACS</span></span>

* <span data-ttu-id="71cfe-2112">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2112">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-2113">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-2113">Appservice</span></span>

* <span data-ttu-id="71cfe-2114">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2114">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="71cfe-2115">Event Grid</span><span class="sxs-lookup"><span data-stu-id="71cfe-2115">Event Grid</span></span>

* <span data-ttu-id="71cfe-2116">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2116">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="71cfe-2117">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-2117">August 11, 2017</span></span>

<span data-ttu-id="71cfe-2118">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="71cfe-2118">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-2119">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-2119">ACS</span></span>

* <span data-ttu-id="71cfe-2120">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2120">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="71cfe-2121">Batch</span><span class="sxs-lookup"><span data-stu-id="71cfe-2121">Batch</span></span>

* <span data-ttu-id="71cfe-2122">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2122">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="71cfe-2123">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2123">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="71cfe-2124">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2124">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="71cfe-2125">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2125">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="71cfe-2126">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2126">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="71cfe-2127">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2127">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="71cfe-2128">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="71cfe-2128">Component</span></span>

* <span data-ttu-id="71cfe-2129">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2129">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="71cfe-2130">コンテナー</span><span class="sxs-lookup"><span data-stu-id="71cfe-2130">Container</span></span>

* <span data-ttu-id="71cfe-2131">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2131">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="71cfe-2132">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="71cfe-2132">Data Lake Store</span></span>

* <span data-ttu-id="71cfe-2133">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2133">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="71cfe-2134">Event Grid</span><span class="sxs-lookup"><span data-stu-id="71cfe-2134">Event Grid</span></span>

* <span data-ttu-id="71cfe-2135">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-2135">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-2136">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-2136">Network</span></span>

* <span data-ttu-id="71cfe-2137">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2137">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="71cfe-2138">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2138">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="71cfe-2139">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2139">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="71cfe-2140">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2140">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="71cfe-2141">プロファイル</span><span class="sxs-lookup"><span data-stu-id="71cfe-2141">Profile</span></span>

* <span data-ttu-id="71cfe-2142">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2142">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-2143">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-2143">Storage</span></span>

* <span data-ttu-id="71cfe-2144">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2144">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-2145">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-2145">VM</span></span>

* <span data-ttu-id="71cfe-2146">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2146">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="71cfe-2147">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2147">Exposed `list-skus` command</span></span>
* <span data-ttu-id="71cfe-2148">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2148">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="71cfe-2149">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2149">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="71cfe-2150">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2150">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="71cfe-2151">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-2151">July 28, 2017</span></span>

<span data-ttu-id="71cfe-2152">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="71cfe-2152">Version 2.0.12</span></span>

* <span data-ttu-id="71cfe-2153">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2153">Added container commands</span></span>
* <span data-ttu-id="71cfe-2154">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2154">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="71cfe-2155">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-2155">Core</span></span>

* <span data-ttu-id="71cfe-2156">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2156">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="71cfe-2157">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2157">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="71cfe-2158">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2158">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="71cfe-2159">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2159">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="71cfe-2160">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2160">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="71cfe-2161">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2161">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="71cfe-2162">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2162">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="71cfe-2163">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2163">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="71cfe-2164">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2164">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="71cfe-2165">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2165">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="71cfe-2166">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2166">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="71cfe-2167">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2167">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="71cfe-2168">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2168">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="71cfe-2169">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2169">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="71cfe-2170">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2170">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="71cfe-2171">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2171">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="71cfe-2172">ACR</span><span class="sxs-lookup"><span data-stu-id="71cfe-2172">ACR</span></span>

* <span data-ttu-id="71cfe-2173">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2173">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="71cfe-2174">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2174">Support SKU update for managed registries</span></span>
* <span data-ttu-id="71cfe-2175">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2175">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="71cfe-2176">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2176">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="71cfe-2177">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2177">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="71cfe-2178">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2178">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-2179">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-2179">ACS</span></span>

* <span data-ttu-id="71cfe-2180">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2180">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-2181">Appservice</span><span class="sxs-lookup"><span data-stu-id="71cfe-2181">Appservice</span></span>

* <span data-ttu-id="71cfe-2182">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2182">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="71cfe-2183">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2183">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="71cfe-2184">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2184">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="71cfe-2185">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2185">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="71cfe-2186">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2186">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="71cfe-2187">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2187">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="71cfe-2188">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2188">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="71cfe-2189">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2189">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="71cfe-2190">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2190">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="71cfe-2191">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="71cfe-2191">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="71cfe-2192">Batch</span><span class="sxs-lookup"><span data-stu-id="71cfe-2192">Batch</span></span>

* <span data-ttu-id="71cfe-2193">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2193">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="71cfe-2194">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2194">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="71cfe-2195">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2195">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="71cfe-2196">CDN</span><span class="sxs-lookup"><span data-stu-id="71cfe-2196">CDN</span></span>

* <span data-ttu-id="71cfe-2197">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2197">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="71cfe-2198">クラウド</span><span class="sxs-lookup"><span data-stu-id="71cfe-2198">Cloud</span></span>

* <span data-ttu-id="71cfe-2199">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2199">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="71cfe-2200">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="71cfe-2200">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="71cfe-2201">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2201">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="71cfe-2202">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2202">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="71cfe-2203">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2203">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="71cfe-2204">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="71cfe-2204">CosmosDB</span></span>

* <span data-ttu-id="71cfe-2205">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2205">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="71cfe-2206">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2206">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="71cfe-2207">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="71cfe-2207">Data Lake Analytics</span></span>

* <span data-ttu-id="71cfe-2208">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2208">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="71cfe-2209">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2209">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="71cfe-2210">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2210">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="71cfe-2211">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="71cfe-2211">Data Lake Store</span></span>

* <span data-ttu-id="71cfe-2212">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2212">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="71cfe-2213">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2213">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="71cfe-2214">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2214">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="71cfe-2215">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-2215">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="71cfe-2216">対話</span><span class="sxs-lookup"><span data-stu-id="71cfe-2216">Interactive</span></span>

* <span data-ttu-id="71cfe-2217">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2217">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="71cfe-2218">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2218">Increased test coverage</span></span>
* <span data-ttu-id="71cfe-2219">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2219">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="71cfe-2220">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2220">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="71cfe-2221">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2221">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="71cfe-2222">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2222">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="71cfe-2223">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2223">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="71cfe-2224">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2224">Added `--progress` flag</span></span>
* <span data-ttu-id="71cfe-2225">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2225">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="71cfe-2226">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2226">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="71cfe-2227">IoT</span><span class="sxs-lookup"><span data-stu-id="71cfe-2227">IoT</span></span>

* <span data-ttu-id="71cfe-2228">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2228">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="71cfe-2229">(#3934)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2229">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="71cfe-2230">Key Vault</span><span class="sxs-lookup"><span data-stu-id="71cfe-2230">Key vault</span></span>

* <span data-ttu-id="71cfe-2231">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2231">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="71cfe-2232">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="71cfe-2232">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="71cfe-2233">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="71cfe-2233">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="71cfe-2234">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="71cfe-2234">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="71cfe-2235">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="71cfe-2235">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="71cfe-2236">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2236">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="71cfe-2237">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2237">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="71cfe-2238">(#3307)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2238">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="71cfe-2239">ラボ</span><span class="sxs-lookup"><span data-stu-id="71cfe-2239">Lab</span></span>

* <span data-ttu-id="71cfe-2240">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2240">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="71cfe-2241">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2241">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-2242">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-2242">Monitor</span></span>

* <span data-ttu-id="71cfe-2243">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2243">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="71cfe-2244">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2244">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="71cfe-2245">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2245">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="71cfe-2246">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2246">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="71cfe-2247">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2247">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="71cfe-2248">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2248">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="71cfe-2249">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2249">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="71cfe-2250">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2250">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="71cfe-2251">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2251">`location` no longer required</span></span>
  * <span data-ttu-id="71cfe-2252">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2252">Add name and ID support for target</span></span>
  * <span data-ttu-id="71cfe-2253">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2253">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="71cfe-2254">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2254">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="71cfe-2255">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2255">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="71cfe-2256">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2256">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="71cfe-2257">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2257">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="71cfe-2258">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2258">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-2259">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-2259">Network</span></span>

* <span data-ttu-id="71cfe-2260">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2260">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="71cfe-2261">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2261">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="71cfe-2262">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2262">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="71cfe-2263">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2263">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="71cfe-2264">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2264">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="71cfe-2265">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2265">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="71cfe-2266">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2266">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="71cfe-2267">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2267">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="71cfe-2268">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2268">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="71cfe-2269">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2269">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="71cfe-2270">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2270">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="71cfe-2271">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2271">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="71cfe-2272">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2272">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="71cfe-2273">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2273">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="71cfe-2274">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2274">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="71cfe-2275">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2275">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="71cfe-2276">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2276">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="71cfe-2277">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2277">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="71cfe-2278">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2278">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="71cfe-2279">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2279">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="71cfe-2280">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2280">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="71cfe-2281">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2281">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="71cfe-2282">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2282">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="71cfe-2283">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2283">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="71cfe-2284">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2284">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="71cfe-2285">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2285">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="71cfe-2286">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2286">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="71cfe-2287">プロファイル</span><span class="sxs-lookup"><span data-stu-id="71cfe-2287">Profile</span></span>

* <span data-ttu-id="71cfe-2288">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2288">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="71cfe-2289">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2289">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="71cfe-2290">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2290">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="71cfe-2291">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2291">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="71cfe-2292">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2292">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="71cfe-2293">RDBMS</span><span class="sxs-lookup"><span data-stu-id="71cfe-2293">RDBMS</span></span>

* <span data-ttu-id="71cfe-2294">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2294">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="71cfe-2295">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2295">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="71cfe-2296">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2296">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="71cfe-2297">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2297">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-2298">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-2298">Resource</span></span>

* <span data-ttu-id="71cfe-2299">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2299">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="71cfe-2300">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2300">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="71cfe-2301">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2301">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="71cfe-2302">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2302">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="71cfe-2303">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2303">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="71cfe-2304">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2304">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="71cfe-2305">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2305">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="71cfe-2306">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2306">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-2307">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-2307">Role</span></span>

* <span data-ttu-id="71cfe-2308">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2308">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="71cfe-2309">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2309">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="71cfe-2310">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="71cfe-2310">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="71cfe-2311">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2311">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="71cfe-2312">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2312">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="71cfe-2313">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="71cfe-2313">Service Fabric</span></span>
* <span data-ttu-id="71cfe-2314">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2314">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="71cfe-2315">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2315">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="71cfe-2316">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2316">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-2317">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-2317">SQL</span></span>

* <span data-ttu-id="71cfe-2318">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2318">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="71cfe-2319">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2319">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="71cfe-2320">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2320">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-2321">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-2321">Storage</span></span>

* <span data-ttu-id="71cfe-2322">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2322">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="71cfe-2323">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2323">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="71cfe-2324">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2324">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="71cfe-2325">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2325">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="71cfe-2326">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2326">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="71cfe-2327">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2327">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-2328">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-2328">VM</span></span>

* <span data-ttu-id="71cfe-2329">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2329">Support configuring nsg</span></span>
* <span data-ttu-id="71cfe-2330">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2330">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="71cfe-2331">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="71cfe-2331">Support managed service identities</span></span>
* <span data-ttu-id="71cfe-2332">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2332">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="71cfe-2333">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2333">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="71cfe-2334">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-2334">May 10, 2017</span></span>

<span data-ttu-id="71cfe-2335">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="71cfe-2335">Version 2.0.6</span></span>

* <span data-ttu-id="71cfe-2336">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2336">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="71cfe-2337">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2337">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="71cfe-2338">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2338">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="71cfe-2339">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2339">Include Cognitive Services module</span></span>
* <span data-ttu-id="71cfe-2340">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2340">Include Service Fabric module</span></span>
* <span data-ttu-id="71cfe-2341">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2341">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="71cfe-2342">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2342">Add support for CDN commands</span></span>
* <span data-ttu-id="71cfe-2343">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2343">Remove Container module</span></span>
* <span data-ttu-id="71cfe-2344">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2344">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="71cfe-2345">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2345">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="71cfe-2346">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-2346">Core</span></span>

* <span data-ttu-id="71cfe-2347">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-2347">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="71cfe-2348">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2348">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="71cfe-2349">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2349">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="71cfe-2350">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2350">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="71cfe-2351">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2351">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="71cfe-2352">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2352">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="71cfe-2353">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2353">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="71cfe-2354">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2354">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="71cfe-2355">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2355">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="71cfe-2356">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="71cfe-2356">core: Improved performance</span></span>
* <span data-ttu-id="71cfe-2357">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="71cfe-2357">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="71cfe-2358">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-2358">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-2359">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-2359">ACS</span></span>

* <span data-ttu-id="71cfe-2360">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2360">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="71cfe-2361">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2361">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="71cfe-2362">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2362">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="71cfe-2363">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2363">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-2364">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-2364">AppService</span></span>

* <span data-ttu-id="71cfe-2365">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2365">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="71cfe-2366">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2366">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="71cfe-2367">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2367">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="71cfe-2368">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2368">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="71cfe-2369">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2369">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="71cfe-2370">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2370">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="71cfe-2371">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="71cfe-2371">support slot swap with preview</span></span>
* <span data-ttu-id="71cfe-2372">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2372">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="71cfe-2373">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2373">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="71cfe-2374">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="71cfe-2374">CosmosDB</span></span>

* <span data-ttu-id="71cfe-2375">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2375">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="71cfe-2376">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2376">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="71cfe-2377">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2377">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="71cfe-2378">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2378">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="71cfe-2379">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="71cfe-2379">Data Lake Analytics</span></span>

* <span data-ttu-id="71cfe-2380">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2380">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="71cfe-2381">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2381">Add support for new catalog item type: package.</span></span> <span data-ttu-id="71cfe-2382">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="71cfe-2382">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="71cfe-2383">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2383">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="71cfe-2384">テーブル</span><span class="sxs-lookup"><span data-stu-id="71cfe-2384">Table</span></span>
  * <span data-ttu-id="71cfe-2385">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="71cfe-2385">Table valued function</span></span>
  * <span data-ttu-id="71cfe-2386">表示</span><span class="sxs-lookup"><span data-stu-id="71cfe-2386">View</span></span>
  * <span data-ttu-id="71cfe-2387">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2387">Table Statistics.</span></span> <span data-ttu-id="71cfe-2388">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="71cfe-2388">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="71cfe-2389">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="71cfe-2389">Data Lake Store</span></span>

* <span data-ttu-id="71cfe-2390">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2390">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="71cfe-2391">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2391">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="71cfe-2392">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="71cfe-2392">missed help for access show.</span></span> <span data-ttu-id="71cfe-2393">追加しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2393">adding it.</span></span> <span data-ttu-id="71cfe-2394">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2394">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="71cfe-2395">検索</span><span class="sxs-lookup"><span data-stu-id="71cfe-2395">Find</span></span>

* <span data-ttu-id="71cfe-2396">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2396">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="71cfe-2397">KeyVault</span><span class="sxs-lookup"><span data-stu-id="71cfe-2397">KeyVault</span></span>

* <span data-ttu-id="71cfe-2398">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2398">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="71cfe-2399">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2399">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="71cfe-2400">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="71cfe-2400">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="71cfe-2401">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2401">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="71cfe-2402">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2402">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="71cfe-2403">ラボ</span><span class="sxs-lookup"><span data-stu-id="71cfe-2403">Lab</span></span>

* <span data-ttu-id="71cfe-2404">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2404">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="71cfe-2405">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2405">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="71cfe-2406">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2406">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="71cfe-2407">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2407">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="71cfe-2408">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2408">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="71cfe-2409">監視</span><span class="sxs-lookup"><span data-stu-id="71cfe-2409">Monitor</span></span>

* <span data-ttu-id="71cfe-2410">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2410">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="71cfe-2411">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2411">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="71cfe-2412">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-2412">Network</span></span>

* <span data-ttu-id="71cfe-2413">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2413">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="71cfe-2414">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2414">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="71cfe-2415">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2415">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="71cfe-2416">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2416">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="71cfe-2417">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2417">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="71cfe-2418">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2418">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="71cfe-2419">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2419">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="71cfe-2420">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2420">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="71cfe-2421">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2421">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="71cfe-2422">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2422">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="71cfe-2423">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2423">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="71cfe-2424">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2424">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="71cfe-2425">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2425">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="71cfe-2426">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2426">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="71cfe-2427">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2427">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="71cfe-2428">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2428">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="71cfe-2429">プロファイル</span><span class="sxs-lookup"><span data-stu-id="71cfe-2429">Profile</span></span>

* <span data-ttu-id="71cfe-2430">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2430">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="71cfe-2431">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2431">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="71cfe-2432">Redis</span><span class="sxs-lookup"><span data-stu-id="71cfe-2432">Redis</span></span>

* <span data-ttu-id="71cfe-2433">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2433">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="71cfe-2434">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2434">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="71cfe-2435">Resource</span><span class="sxs-lookup"><span data-stu-id="71cfe-2435">Resource</span></span>

* <span data-ttu-id="71cfe-2436">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2436">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="71cfe-2437">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2437">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="71cfe-2438">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2438">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="71cfe-2439">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2439">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="71cfe-2440">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2440">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="71cfe-2441">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2441">Add docs for az lock update.</span></span> <span data-ttu-id="71cfe-2442">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2442">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="71cfe-2443">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-2443">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="71cfe-2444">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2444">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="71cfe-2445">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2445">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="71cfe-2446">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2446">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="71cfe-2447">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2447">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="71cfe-2448">Role</span><span class="sxs-lookup"><span data-stu-id="71cfe-2448">Role</span></span>

* <span data-ttu-id="71cfe-2449">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2449">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="71cfe-2450">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2450">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="71cfe-2451">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2451">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="71cfe-2452">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-2452">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="71cfe-2453">SQL</span><span class="sxs-lookup"><span data-stu-id="71cfe-2453">SQL</span></span>

* <span data-ttu-id="71cfe-2454">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2454">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="71cfe-2455">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2455">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="71cfe-2456">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-2456">Storage</span></span>

* <span data-ttu-id="71cfe-2457">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="71cfe-2457">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="71cfe-2458">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2458">Add support for incremental blob copy</span></span>
* <span data-ttu-id="71cfe-2459">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2459">Add support for large block blob upload</span></span>
* <span data-ttu-id="71cfe-2460">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="71cfe-2460">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-2461">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-2461">VM</span></span>

* <span data-ttu-id="71cfe-2462">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2462">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="71cfe-2463">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2463">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="71cfe-2464">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="71cfe-2464">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="71cfe-2465">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="71cfe-2465">az vm/vmss disk</span></span>
  3. <span data-ttu-id="71cfe-2466">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2466">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="71cfe-2467">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="71cfe-2467">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="71cfe-2468">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2468">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="71cfe-2469">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-2469">April 3, 2017</span></span>

<span data-ttu-id="71cfe-2470">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="71cfe-2470">Version 2.0.2</span></span>

<span data-ttu-id="71cfe-2471">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="71cfe-2471">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="71cfe-2472">コア</span><span class="sxs-lookup"><span data-stu-id="71cfe-2472">Core</span></span>

* <span data-ttu-id="71cfe-2473">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="71cfe-2473">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="71cfe-2474">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2474">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="71cfe-2475">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2475">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="71cfe-2476">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2476">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="71cfe-2477">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2477">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="71cfe-2478">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="71cfe-2478">Add prompting for missing template parameters.</span></span> <span data-ttu-id="71cfe-2479">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2479">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="71cfe-2480">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="71cfe-2480">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="71cfe-2481">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="71cfe-2481">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="71cfe-2482">ACS</span><span class="sxs-lookup"><span data-stu-id="71cfe-2482">ACS</span></span>

* <span data-ttu-id="71cfe-2483">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2483">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="71cfe-2484">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="71cfe-2484">Add support for ssh key password prompting.</span></span> <span data-ttu-id="71cfe-2485">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2485">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="71cfe-2486">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="71cfe-2486">Add support for windows clusters.</span></span> <span data-ttu-id="71cfe-2487">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2487">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="71cfe-2488">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="71cfe-2488">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="71cfe-2489">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2489">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="71cfe-2490">AppService</span><span class="sxs-lookup"><span data-stu-id="71cfe-2490">AppService</span></span>

* <span data-ttu-id="71cfe-2491">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2491">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="71cfe-2492">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2492">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="71cfe-2493">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2493">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="71cfe-2494">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2494">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="71cfe-2495">DataLake</span><span class="sxs-lookup"><span data-stu-id="71cfe-2495">DataLake</span></span>

* <span data-ttu-id="71cfe-2496">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-2496">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="71cfe-2497">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="71cfe-2497">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="71cfe-2498">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="71cfe-2498">DocuemntDB</span></span>

* <span data-ttu-id="71cfe-2499">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2499">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="71cfe-2500">VM</span><span class="sxs-lookup"><span data-stu-id="71cfe-2500">VM</span></span>

* <span data-ttu-id="71cfe-2501">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2501">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="71cfe-2502">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2502">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="71cfe-2503">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2503">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="71cfe-2504">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2504">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="71cfe-2505">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2505">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="71cfe-2506">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2506">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="71cfe-2507">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="71cfe-2507">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="71cfe-2508">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="71cfe-2508">February 27, 2017</span></span>

<span data-ttu-id="71cfe-2509">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="71cfe-2509">Version 2.0.0</span></span>

<span data-ttu-id="71cfe-2510">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2510">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="71cfe-2511">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2511">Container Service (acs)</span></span>
- <span data-ttu-id="71cfe-2512">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="71cfe-2512">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="71cfe-2513">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="71cfe-2513">Networking</span></span>
- <span data-ttu-id="71cfe-2514">Storage</span><span class="sxs-lookup"><span data-stu-id="71cfe-2514">Storage</span></span>

<span data-ttu-id="71cfe-2515">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2515">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="71cfe-2516">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="71cfe-2516">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="71cfe-2517">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2517">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="71cfe-2518">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="71cfe-2518">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="71cfe-2519">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="71cfe-2519">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="71cfe-2520">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2520">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="71cfe-2521">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="71cfe-2521">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="71cfe-2522">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="71cfe-2522">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="71cfe-2523">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="71cfe-2523">Provide feedback from the command line with the `az feedback` command</span></span>

