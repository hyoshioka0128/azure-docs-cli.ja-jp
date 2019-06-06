---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/21/2019
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 5b4bcde8c4a66ccc378abc00468cbdb423f07fa4
ms.sourcegitcommit: 3fe3502ec5af89939155285bb5e741b08af604cd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/24/2019
ms.locfileid: "66197791"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="c1102-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="c1102-103">Azure CLI release notes</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="c1102-104">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="c1102-104">May 21, 2019</span></span>

<span data-ttu-id="c1102-105">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="c1102-105">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="c1102-106">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-106">Core</span></span>
* <span data-ttu-id="c1102-107">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-107">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="c1102-108">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-108">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="c1102-109">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-109">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-110">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-110">ACR</span></span>
* <span data-ttu-id="c1102-111">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-111">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-112">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-112">ACS</span></span>
* <span data-ttu-id="c1102-113">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-113">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-114">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-114">AppService</span></span>
* <span data-ttu-id="c1102-115">[非推奨] `functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="c1102-115">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="c1102-116">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-116">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="c1102-117">[破壊的変更] `--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="c1102-117">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="c1102-118">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-118">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="c1102-119">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-119">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="c1102-120">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-120">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="c1102-121">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-121">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="c1102-122">BotService</span><span class="sxs-lookup"><span data-stu-id="c1102-122">BotService</span></span>
* <span data-ttu-id="c1102-123">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-123">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="c1102-124">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-124">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="c1102-125">消費</span><span class="sxs-lookup"><span data-stu-id="c1102-125">Consumption</span></span>
* <span data-ttu-id="c1102-126">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-126">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="c1102-127">IoT</span><span class="sxs-lookup"><span data-stu-id="c1102-127">IoT</span></span>
* <span data-ttu-id="c1102-128">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-128">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="c1102-129">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-129">Network</span></span>
* [破壊的変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="c1102-131">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-131">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="c1102-132">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-132">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="c1102-133">RDBMS</span><span class="sxs-lookup"><span data-stu-id="c1102-133">RDBMS</span></span>
* <span data-ttu-id="c1102-134">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-134">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="c1102-135">RBAC</span><span class="sxs-lookup"><span data-stu-id="c1102-135">RBAC</span></span>
* <span data-ttu-id="c1102-136">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-136">Added support for mangement group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-137">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-137">Storage</span></span>
* <span data-ttu-id="c1102-138">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="c1102-138">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="c1102-139">Compute</span><span class="sxs-lookup"><span data-stu-id="c1102-139">Compute</span></span>
* <span data-ttu-id="c1102-140">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-140">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="c1102-141">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-141">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="c1102-142">__メモ__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="c1102-142">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="c1102-143">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-143">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="c1102-144">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="c1102-144">May 6, 2019</span></span>

<span data-ttu-id="c1102-145">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="c1102-145">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-146">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-146">ACS</span></span>
* <span data-ttu-id="c1102-147">[破壊的変更] `--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-147">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="c1102-148">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-148">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="c1102-149">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-149">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="c1102-150">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-150">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-151">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-151">Appservice</span></span>
* <span data-ttu-id="c1102-152">[非推奨] `functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-152">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="c1102-153">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-153">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="c1102-154">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="c1102-154">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="c1102-155">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-155">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="c1102-156">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-156">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="c1102-157">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-157">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="c1102-158">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-158">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="c1102-159">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-159">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="c1102-160">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-160">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="c1102-161">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-161">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="c1102-162">Batch</span><span class="sxs-lookup"><span data-stu-id="c1102-162">Batch</span></span>
* <span data-ttu-id="c1102-163">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-163">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="c1102-164">Botservice</span><span class="sxs-lookup"><span data-stu-id="c1102-164">Botservice</span></span>
* <span data-ttu-id="c1102-165">[破壊的変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="c1102-165">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="c1102-166">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-166">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="c1102-167">[破壊的変更] `--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-167">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="c1102-168">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="c1102-168">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="c1102-169">[破壊的変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-169">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="c1102-170">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="c1102-170">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="c1102-171">[破壊的変更] `bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-171">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="c1102-172">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-172">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="c1102-173">[破壊的変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-173">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="c1102-174">[破壊的変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-174">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="c1102-175">[破壊的変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-175">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="c1102-176">[破壊的変更] `Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-176">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="c1102-177">[破壊的変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-177">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="c1102-178">[破壊的変更] `SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-178">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="c1102-179">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="c1102-179">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="c1102-180">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-180">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="c1102-181">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-181">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="c1102-182">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-182">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="c1102-183">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-183">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="c1102-184">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-184">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="c1102-185">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-185">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="c1102-186">構成</span><span class="sxs-lookup"><span data-stu-id="c1102-186">Configure</span></span>
* <span data-ttu-id="c1102-187">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-187">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="c1102-188">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="c1102-188">Eventhubs</span></span>
* <span data-ttu-id="c1102-189">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-189">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="c1102-190">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-190">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="c1102-191">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-191">Network</span></span>
* <span data-ttu-id="c1102-192">[破壊的変更] `vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="c1102-192">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="c1102-193">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="c1102-193">Policy Insights</span></span>
* <span data-ttu-id="c1102-194">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-194">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="c1102-195">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-195">Role</span></span>
* <span data-ttu-id="c1102-196">[非推奨] `create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="c1102-196">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="c1102-197">Service Bus</span><span class="sxs-lookup"><span data-stu-id="c1102-197">Service Bus</span></span>
* <span data-ttu-id="c1102-198">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-198">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="c1102-199">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-199">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="c1102-200">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-200">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-201">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-201">SQL</span></span>
* <span data-ttu-id="c1102-202">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-202">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-203">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-203">VM</span></span>
* <span data-ttu-id="c1102-204">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-204">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="c1102-205">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-205">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="c1102-206">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-206">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="c1102-207">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-207">Added new `ppg` command group for manging Proximity Placement Groups</span></span>
* <span data-ttu-id="c1102-208">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-208">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="c1102-209">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-209">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="c1102-210">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="c1102-210">April 23, 2019</span></span>

<span data-ttu-id="c1102-211">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="c1102-211">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-212">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-212">ACS</span></span>
* <span data-ttu-id="c1102-213">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-213">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="c1102-214">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-214">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="c1102-215">AMS</span><span class="sxs-lookup"><span data-stu-id="c1102-215">AMS</span></span>
* <span data-ttu-id="c1102-216">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-216">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-217">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-217">AppService</span></span>
* <span data-ttu-id="c1102-218">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-218">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="c1102-219">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-219">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="c1102-220">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-220">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="c1102-221">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-221">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="c1102-222">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-222">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="c1102-223">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-223">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="c1102-224">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-224">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="c1102-225">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-225">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="c1102-226">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-226">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="c1102-227">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="c1102-227">Deployment Manager</span></span>
* <span data-ttu-id="c1102-228">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="c1102-228">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="c1102-229">ラボ</span><span class="sxs-lookup"><span data-stu-id="c1102-229">Lab</span></span>
* <span data-ttu-id="c1102-230">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-230">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="c1102-231">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-231">Network</span></span>
* <span data-ttu-id="c1102-232">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-232">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-233">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-233">Resource</span></span>
* <span data-ttu-id="c1102-234">[非推奨] `resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="c1102-234">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="c1102-235">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="c1102-235">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="c1102-236">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-236">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="c1102-237">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-237">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-238">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-238">SQL</span></span>
* <span data-ttu-id="c1102-239">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-239">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="c1102-240">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-240">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="c1102-241">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-241">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="c1102-242">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-242">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-243">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-243">Storage</span></span>
* <span data-ttu-id="c1102-244">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-244">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-245">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-245">VM</span></span>
* <span data-ttu-id="c1102-246">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-246">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="c1102-247">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-247">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="c1102-248">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-248">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="c1102-249">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="c1102-249">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="c1102-250">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-250">Core</span></span>
* <span data-ttu-id="c1102-251">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-251">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-252">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-252">ACR</span></span>
* <span data-ttu-id="c1102-253">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-253">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="c1102-254">AMS</span><span class="sxs-lookup"><span data-stu-id="c1102-254">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="c1102-257">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-257">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="c1102-258">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-258">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-259">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-259">AppService</span></span>
* <span data-ttu-id="c1102-260">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-260">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="c1102-261">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-261">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="c1102-262">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-262">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="c1102-263">[破壊的変更] `devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="c1102-263">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="c1102-264">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-264">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="c1102-265">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-265">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="c1102-266">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-266">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="c1102-267">CDN</span><span class="sxs-lookup"><span data-stu-id="c1102-267">CDN</span></span>
* <span data-ttu-id="c1102-268">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-268">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="c1102-269">フィードバック</span><span class="sxs-lookup"><span data-stu-id="c1102-269">Feedback</span></span>
* <span data-ttu-id="c1102-270">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-270">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="c1102-271">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-271">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="c1102-272">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-272">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-273">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-273">Monitor</span></span>
* <span data-ttu-id="c1102-274">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-274">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="c1102-275">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-275">Network</span></span>
* <span data-ttu-id="c1102-276">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-276">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="c1102-277">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-277">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="c1102-278">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-278">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="c1102-279">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-279">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="c1102-280">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="c1102-280">PrivateDNS</span></span>
* <span data-ttu-id="c1102-281">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-281">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-282">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-282">Resource</span></span>
* <span data-ttu-id="c1102-283">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-283">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="c1102-284">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-284">Role</span></span>
* <span data-ttu-id="c1102-285">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-285">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="c1102-286">[破壊的変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-286">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-287">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-287">SQL</span></span>
* <span data-ttu-id="c1102-288">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-288">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-289">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-289">Storage</span></span>
* <span data-ttu-id="c1102-290">[破壊的変更] `storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-290">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="c1102-291">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-291">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="c1102-292">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-292">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="c1102-293">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-293">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="c1102-294">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="c1102-294">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="c1102-295">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-295">Core</span></span>
* <span data-ttu-id="c1102-296">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-296">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="c1102-297">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-297">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="c1102-298">クラウド</span><span class="sxs-lookup"><span data-stu-id="c1102-298">Cloud</span></span>
* <span data-ttu-id="c1102-299">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-299">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-300">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-300">ACR</span></span>
* <span data-ttu-id="c1102-301">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-301">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="c1102-302">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-302">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="c1102-303">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-303">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="c1102-304">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-304">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-305">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-305">AppService</span></span>
* <span data-ttu-id="c1102-306">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-306">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="c1102-307">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-307">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="c1102-308">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="c1102-308">BOT Service</span></span>
* <span data-ttu-id="c1102-309">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-309">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="c1102-310">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-310">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="c1102-311">[破壊的変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-311">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="c1102-312">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-312">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="c1102-313">CDN</span><span class="sxs-lookup"><span data-stu-id="c1102-313">CDN</span></span>
* <span data-ttu-id="c1102-314">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-314">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [破壊的変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="c1102-316">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="c1102-316">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="c1102-317">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-317">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="c1102-318">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="c1102-318">Cosmosdb</span></span>
* <span data-ttu-id="c1102-319">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-319">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="c1102-320">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-320">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="c1102-321">Interactive</span><span class="sxs-lookup"><span data-stu-id="c1102-321">Interactive</span></span>
* <span data-ttu-id="c1102-322">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-322">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-323">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-323">Monitor</span></span>
* <span data-ttu-id="c1102-324">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-324">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="c1102-325">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-325">Network</span></span>
* <span data-ttu-id="c1102-326">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-326">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="c1102-327">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c1102-327">Profile</span></span>
* <span data-ttu-id="c1102-328">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-328">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="c1102-329">Postgres</span><span class="sxs-lookup"><span data-stu-id="c1102-329">Postgres</span></span> 
* <span data-ttu-id="c1102-330">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-330">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="c1102-331">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="c1102-331">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-332">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-332">Resource</span></span>
* <span data-ttu-id="c1102-333">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-333">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="c1102-334">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-334">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="c1102-335">Graph</span><span class="sxs-lookup"><span data-stu-id="c1102-335">Graph</span></span>
* <span data-ttu-id="c1102-336">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-336">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="c1102-337">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-337">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="c1102-338">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-338">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="c1102-339">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-339">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="c1102-340">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-340">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-341">storage</span><span class="sxs-lookup"><span data-stu-id="c1102-341">storage</span></span>
* <span data-ttu-id="c1102-342">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-342">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="c1102-343">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-343">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="c1102-344">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-344">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="c1102-345">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-345">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-346">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-346">VM</span></span>
* <span data-ttu-id="c1102-347">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-347">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="c1102-348">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="c1102-348">March 12, 2019</span></span>

<span data-ttu-id="c1102-349">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="c1102-349">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="c1102-350">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-350">Core</span></span>

* <span data-ttu-id="c1102-351">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-351">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-352">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-352">ACR</span></span>

* <span data-ttu-id="c1102-353">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-353">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-354">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-354">ACS</span></span>

* <span data-ttu-id="c1102-355">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-355">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="c1102-356">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-356">AppService</span></span>

* <span data-ttu-id="c1102-357">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-357">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="c1102-358">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-358">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="c1102-359">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-359">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="c1102-360">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-360">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="c1102-361">Botservice</span><span class="sxs-lookup"><span data-stu-id="c1102-361">Botservice</span></span>

* <span data-ttu-id="c1102-362">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-362">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="c1102-363">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-363">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="c1102-364">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-364">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="c1102-365">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-365">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="c1102-366">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-366">Container</span></span>

* <span data-ttu-id="c1102-367">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-367">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="c1102-368">EventHub</span><span class="sxs-lookup"><span data-stu-id="c1102-368">EventHub</span></span>

* <span data-ttu-id="c1102-369">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-369">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="c1102-370">Find</span><span class="sxs-lookup"><span data-stu-id="c1102-370">Find</span></span>

* <span data-ttu-id="c1102-371">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="c1102-371">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="c1102-372">HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1102-372">HDInsight</span></span>

* <span data-ttu-id="c1102-373">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-373">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="c1102-374">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-374">Network</span></span>

* <span data-ttu-id="c1102-375">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-375">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="c1102-376">Rdbms</span><span class="sxs-lookup"><span data-stu-id="c1102-376">Rdbms</span></span>

* <span data-ttu-id="c1102-377">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="c1102-377">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="c1102-378">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-378">Role</span></span>

* <span data-ttu-id="c1102-379">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-379">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="c1102-380">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-380">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="c1102-381">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="c1102-381">Service Fabric</span></span>

* <span data-ttu-id="c1102-382">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-382">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="c1102-383">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="c1102-383">February 26, 2019</span></span>

<span data-ttu-id="c1102-384">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="c1102-384">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="c1102-385">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-385">Core</span></span>

* <span data-ttu-id="c1102-386">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-386">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-387">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-387">ACR</span></span>

* <span data-ttu-id="c1102-388">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-388">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="c1102-389">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-389">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-390">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-390">ACS</span></span>

* <span data-ttu-id="c1102-391">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-391">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-392">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-392">AppService</span></span>

* <span data-ttu-id="c1102-393">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-393">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="c1102-394">Batch</span><span class="sxs-lookup"><span data-stu-id="c1102-394">Batch</span></span>
* <span data-ttu-id="c1102-395">[破壊的変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-395">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="c1102-396">[破壊的変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-396">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="c1102-397">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-397">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="c1102-398">[破壊的変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-398">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="c1102-399">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-399">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="c1102-400">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="c1102-400">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="c1102-401">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="c1102-401">CosmosDB</span></span>

* <span data-ttu-id="c1102-402">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-402">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="c1102-403">Kusto</span><span class="sxs-lookup"><span data-stu-id="c1102-403">Kusto</span></span>

* <span data-ttu-id="c1102-404">[破壊的変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-404">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="c1102-405">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-405">Network</span></span>

* <span data-ttu-id="c1102-406">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-406">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="c1102-407">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-407">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="c1102-408">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-408">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="c1102-409">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-409">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="c1102-410">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-410">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="c1102-411">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-411">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="c1102-412">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-412">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-413">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-413">Resource</span></span>

* <span data-ttu-id="c1102-414">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-414">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="c1102-415">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-415">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="c1102-416">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-416">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="c1102-417">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-417">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="c1102-418">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-418">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="c1102-419">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-419">Role</span></span>

* <span data-ttu-id="c1102-420">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-420">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-421">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-421">VM</span></span>

* <span data-ttu-id="c1102-422">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-422">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="c1102-423">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="c1102-423">February 12, 2019</span></span>

<span data-ttu-id="c1102-424">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="c1102-424">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="c1102-425">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-425">Core</span></span>

* <span data-ttu-id="c1102-426">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-426">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="c1102-427">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-427">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-428">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-428">ACR</span></span>
* <span data-ttu-id="c1102-429">[破壊的変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-429">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="c1102-430">[破壊的変更] `acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-430">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-431">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-431">ACS</span></span>
* <span data-ttu-id="c1102-432">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-432">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="c1102-433">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-433">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="c1102-434">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-434">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="c1102-435">AMS</span><span class="sxs-lookup"><span data-stu-id="c1102-435">AMS</span></span>
* <span data-ttu-id="c1102-436">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-436">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="c1102-437">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-437">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-438">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-438">Appservice</span></span>
* <span data-ttu-id="c1102-439">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-439">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="c1102-440">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-440">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="c1102-441">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-441">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="c1102-442">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-442">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="c1102-443">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-443">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="c1102-444">Botservice</span><span class="sxs-lookup"><span data-stu-id="c1102-444">Botservice</span></span>
* <span data-ttu-id="c1102-445">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-445">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="c1102-446">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-446">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="c1102-447">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-447">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="c1102-448">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-448">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="c1102-449">[非推奨] `--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-449">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="c1102-450">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-450">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="c1102-451">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-451">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="c1102-452">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-452">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="c1102-453">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="c1102-453">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="c1102-454">8.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-454">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="c1102-455">Key Vault</span><span class="sxs-lookup"><span data-stu-id="c1102-455">Key Vault</span></span>
* <span data-ttu-id="c1102-456">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-456">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-457">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-457">Monitor</span></span>
* <span data-ttu-id="c1102-458">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-458">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="c1102-459">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-459">Network</span></span>
* <span data-ttu-id="c1102-460">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-460">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="c1102-461">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-461">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="c1102-462">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-462">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="c1102-463">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-463">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="c1102-464">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="c1102-464">Policy Insights</span></span>
* <span data-ttu-id="c1102-465">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-465">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="c1102-466">RDBMS</span><span class="sxs-lookup"><span data-stu-id="c1102-466">RDBMS</span></span>
* <span data-ttu-id="c1102-467">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-467">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="c1102-468">Redis</span><span class="sxs-lookup"><span data-stu-id="c1102-468">Redis</span></span>
* <span data-ttu-id="c1102-469">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-469">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="c1102-470">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-470">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="c1102-471">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-471">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="c1102-472">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-472">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="c1102-473">[破壊的変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-473">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="c1102-474">[破壊的変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="c1102-474">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="c1102-475">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-475">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="c1102-476">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-476">Role</span></span>
* <span data-ttu-id="c1102-477">[破壊的変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="c1102-477">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="c1102-478">SQL VM</span><span class="sxs-lookup"><span data-stu-id="c1102-478">SQL VM</span></span>
* <span data-ttu-id="c1102-479">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-479">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-480">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-480">VM</span></span>
* <span data-ttu-id="c1102-481">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-481">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="c1102-482">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-482">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="c1102-483">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-483">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="c1102-484">[破壊的変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="c1102-484">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="c1102-485">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c1102-485">January 31, 2019</span></span>

<span data-ttu-id="c1102-486">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="c1102-486">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="c1102-487">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-487">Core</span></span>

* <span data-ttu-id="c1102-488">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="c1102-488">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="c1102-489">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="c1102-489">January 28, 2019</span></span>

<span data-ttu-id="c1102-490">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="c1102-490">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-491">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-491">ACR</span></span>
* <span data-ttu-id="c1102-492">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-492">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-493">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-493">ACS</span></span>
* <span data-ttu-id="c1102-494">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-494">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="c1102-495">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-495">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="c1102-496">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-496">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="c1102-497">AMS</span><span class="sxs-lookup"><span data-stu-id="c1102-497">AMS</span></span>
* <span data-ttu-id="c1102-498">[破壊的変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-498">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="c1102-499">[破壊的変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-499">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-500">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-500">Appservice</span></span>
* <span data-ttu-id="c1102-501">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-501">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="c1102-502">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-502">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="c1102-503">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-503">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="c1102-504">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-504">Container</span></span>
* <span data-ttu-id="c1102-505">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-505">Added `container start` command</span></span>
* <span data-ttu-id="c1102-506">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-506">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="c1102-507">EventGrid</span><span class="sxs-lookup"><span data-stu-id="c1102-507">EventGrid</span></span>
* <span data-ttu-id="c1102-508">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-508">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="c1102-509">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-509">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="c1102-510">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-510">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="c1102-511">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-511">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="c1102-512">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="c1102-512">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="c1102-513">HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1102-513">HDInsight</span></span>
* <span data-ttu-id="c1102-514">[破壊的変更] `hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-514">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="c1102-515">[破壊的変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-515">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="c1102-516">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-516">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="c1102-517">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-517">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="c1102-518">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-518">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="c1102-519">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-519">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="c1102-520">IoT</span><span class="sxs-lookup"><span data-stu-id="c1102-520">IoT</span></span>
* <span data-ttu-id="c1102-521">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-521">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="c1102-522">Kusto</span><span class="sxs-lookup"><span data-stu-id="c1102-522">Kusto</span></span>
* <span data-ttu-id="c1102-523">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="c1102-523">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-524">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-524">Monitor</span></span>
* <span data-ttu-id="c1102-525">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-525">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="c1102-526">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c1102-526">Profile</span></span>
* <span data-ttu-id="c1102-527">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-527">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="c1102-528">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-528">Network</span></span>
* <span data-ttu-id="c1102-529">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-529">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="c1102-530">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-530">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-531">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-531">Resource</span></span>
* <span data-ttu-id="c1102-532">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-532">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="c1102-533">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-533">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="c1102-534">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="c1102-534">SQL Virtual Machine</span></span>
* <span data-ttu-id="c1102-535">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="c1102-535">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-536">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-536">Storage</span></span>
* <span data-ttu-id="c1102-537">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-537">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="c1102-538">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="c1102-538">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-539">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-539">VM</span></span>
* <span data-ttu-id="c1102-540">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-540">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="c1102-541">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-541">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="c1102-542">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="c1102-542">January 15, 2019</span></span>

<span data-ttu-id="c1102-543">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="c1102-543">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-544">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-544">ACR</span></span>
* <span data-ttu-id="c1102-545">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-545">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="c1102-546">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-546">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="c1102-547">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-547">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="c1102-548">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-548">ACS</span></span>
* <span data-ttu-id="c1102-549">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-549">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-550">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-550">Appservice</span></span>
* <span data-ttu-id="c1102-551">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-551">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="c1102-552">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-552">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="c1102-553">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-553">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="c1102-554">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-554">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="c1102-555">Botservice</span><span class="sxs-lookup"><span data-stu-id="c1102-555">Botservice</span></span>
* <span data-ttu-id="c1102-556">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-556">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="c1102-557">構成</span><span class="sxs-lookup"><span data-stu-id="c1102-557">Configure</span></span>
* <span data-ttu-id="c1102-558">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-558">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="c1102-559">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="c1102-559">CosmosDB</span></span>
* <span data-ttu-id="c1102-560">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-560">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="c1102-561">HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1102-561">HDInsight</span></span>
* <span data-ttu-id="c1102-562">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-562">Added commands for managing applications</span></span>
* <span data-ttu-id="c1102-563">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-563">Added commands for managing script actions</span></span>
* <span data-ttu-id="c1102-564">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-564">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="c1102-565">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-565">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="c1102-566">[破壊的変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-566">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="c1102-567">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-567">Network</span></span>
* <span data-ttu-id="c1102-568">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-568">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="c1102-569">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-569">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="c1102-570">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-570">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="c1102-571">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-571">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="c1102-572">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-572">Role</span></span>
* <span data-ttu-id="c1102-573">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="c1102-573">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="c1102-574">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="c1102-574">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="c1102-575">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="c1102-575">Security</span></span>
* <span data-ttu-id="c1102-576">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c1102-576">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-577">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-577">Storage</span></span>
* <span data-ttu-id="c1102-578">[破壊的変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-578">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="c1102-579">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="c1102-579">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="c1102-580">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-580">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="c1102-581">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-581">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="c1102-582">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-582">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-583">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-583">VM</span></span>
* <span data-ttu-id="c1102-584">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-584">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="c1102-585">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-585">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="c1102-586">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-586">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="c1102-587">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-587">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="c1102-588">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-588">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="c1102-589">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-589">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="c1102-590">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="c1102-590">December 20, 2018</span></span>

<span data-ttu-id="c1102-591">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="c1102-591">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="c1102-592">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-592">Appservice</span></span>
* <span data-ttu-id="c1102-593">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-593">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="c1102-594">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-594">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="c1102-595">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-595">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="c1102-596">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="c1102-596">IoTCentral</span></span>
* <span data-ttu-id="c1102-597">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-597">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="c1102-598">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-598">Role</span></span>
* <span data-ttu-id="c1102-599">[破壊的変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-599">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-600">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-600">SQL</span></span>
* <span data-ttu-id="c1102-601">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-601">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-602">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-602">VM</span></span>
* <span data-ttu-id="c1102-603">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-603">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="c1102-604">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="c1102-604">December 18, 2018</span></span>

<span data-ttu-id="c1102-605">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="c1102-605">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="c1102-606">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-606">ACR</span></span>
* <span data-ttu-id="c1102-607">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-607">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="c1102-608">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="c1102-608">Condensed the table layout for task list</span></span>
* <span data-ttu-id="c1102-609">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-609">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-610">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-610">ACS</span></span>
* <span data-ttu-id="c1102-611">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-611">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="c1102-612">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-612">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="c1102-613">[非推奨] `az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="c1102-613">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="c1102-614">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="c1102-614">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="c1102-615">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-615">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="c1102-616">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-616">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-617">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-617">Appservice</span></span>
* <span data-ttu-id="c1102-618">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-618">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="c1102-619">Botservice</span><span class="sxs-lookup"><span data-stu-id="c1102-619">Botservice</span></span>
* <span data-ttu-id="c1102-620">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-620">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="c1102-621">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-621">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="c1102-622">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-622">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="c1102-623">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="c1102-623">Reduced Kudu network calls</span></span>
* <span data-ttu-id="c1102-624">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-624">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="c1102-625">消費</span><span class="sxs-lookup"><span data-stu-id="c1102-625">Consumption</span></span>
* <span data-ttu-id="c1102-626">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-626">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="c1102-627">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="c1102-627">CosmosDB</span></span>
* <span data-ttu-id="c1102-628">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-628">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="c1102-629">マップ</span><span class="sxs-lookup"><span data-stu-id="c1102-629">Maps</span></span>
* <span data-ttu-id="c1102-630">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-630">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="c1102-631">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-631">Network</span></span>
* <span data-ttu-id="c1102-632">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-632">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="c1102-633">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-633">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-634">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-634">Resource</span></span>
* <span data-ttu-id="c1102-635">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-635">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="c1102-636">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-636">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-637">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-637">Storage</span></span>
*  <span data-ttu-id="c1102-638">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-638">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-639">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-639">VM</span></span>
* <span data-ttu-id="c1102-640">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-640">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="c1102-641">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="c1102-641">December 4, 2018</span></span>

<span data-ttu-id="c1102-642">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="c1102-642">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="c1102-643">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-643">Core</span></span>
* <span data-ttu-id="c1102-644">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-644">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="c1102-645">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-645">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-646">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-646">Appservice</span></span>
* <span data-ttu-id="c1102-647">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-647">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="c1102-648">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-648">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="c1102-649">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-649">Network</span></span>
* <span data-ttu-id="c1102-650">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-650">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="c1102-651">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-651">Role</span></span>
* <span data-ttu-id="c1102-652">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-652">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="c1102-653">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-653">VM</span></span>
* <span data-ttu-id="c1102-654">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-654">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="c1102-655">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-655">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="c1102-656">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-656">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="c1102-657">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-657">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="c1102-658">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="c1102-658">November 20, 2018</span></span>

<span data-ttu-id="c1102-659">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="c1102-659">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="c1102-660">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-660">Core</span></span>
* <span data-ttu-id="c1102-661">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-661">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-662">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-662">ACR</span></span>
* <span data-ttu-id="c1102-663">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-663">Added context token to task step</span></span>
* <span data-ttu-id="c1102-664">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-664">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="c1102-665">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-665">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-666">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-666">Appservice</span></span>
* <span data-ttu-id="c1102-667">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-667">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="c1102-668">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-668">Updated the default `node_version`.</span></span> <span data-ttu-id="c1102-669">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="c1102-669">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="c1102-670">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-670">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="c1102-671">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-671">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="c1102-672">IotCentral</span><span class="sxs-lookup"><span data-stu-id="c1102-672">IotCentral</span></span>
* <span data-ttu-id="c1102-673">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-673">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="c1102-674">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1102-674">KeyVault</span></span>
* <span data-ttu-id="c1102-675">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-675">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="c1102-676">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-676">Network</span></span>
* <span data-ttu-id="c1102-677">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-677">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="c1102-678">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-678">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="c1102-679">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-679">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="c1102-680">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-680">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="c1102-681">Rdbms</span><span class="sxs-lookup"><span data-stu-id="c1102-681">Rdbms</span></span>
* <span data-ttu-id="c1102-682">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-682">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="c1102-683">Rbac</span><span class="sxs-lookup"><span data-stu-id="c1102-683">Rbac</span></span>
* <span data-ttu-id="c1102-684">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-684">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="c1102-685">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-685">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="c1102-686">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-686">Storage</span></span>
* <span data-ttu-id="c1102-687">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-687">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="c1102-688">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-688">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="c1102-689">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-689">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="c1102-690">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="c1102-690">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-691">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-691">VM</span></span>
* <span data-ttu-id="c1102-692">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-692">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="c1102-693">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-693">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="c1102-694">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="c1102-694">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="c1102-695">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-695">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="c1102-696">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-696">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="c1102-697">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-697">Added `snapshot wait` command</span></span>
* <span data-ttu-id="c1102-698">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-698">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="c1102-699">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="c1102-699">November 6, 2018</span></span>

<span data-ttu-id="c1102-700">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="c1102-700">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="c1102-701">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-701">Core</span></span>
* <span data-ttu-id="c1102-702">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-702">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-703">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-703">ACR</span></span>
* <span data-ttu-id="c1102-704">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-704">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="c1102-705">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-705">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-706">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-706">ACS</span></span>
* <span data-ttu-id="c1102-707">[破壊的変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-707">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="c1102-708">Advisor</span><span class="sxs-lookup"><span data-stu-id="c1102-708">Advisor</span></span>
* <span data-ttu-id="c1102-709">GA リリース</span><span class="sxs-lookup"><span data-stu-id="c1102-709">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="c1102-710">AMS</span><span class="sxs-lookup"><span data-stu-id="c1102-710">AMS</span></span>
* <span data-ttu-id="c1102-711">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-711">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="c1102-712">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-712">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="c1102-713">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-713">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="c1102-714">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-714">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="c1102-715">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-715">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="c1102-716">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-716">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="c1102-717">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-717">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="c1102-718">[破壊的変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="c1102-718">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="c1102-719">[破壊的変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-719">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="c1102-720">[破壊的変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-720">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="c1102-721">[破壊的変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="c1102-721">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="c1102-722">[破壊的変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="c1102-722">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="c1102-723">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="c1102-723">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="c1102-724">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="c1102-724">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="c1102-725">[破壊的変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-725">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="c1102-726">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="c1102-726">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="c1102-727">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="c1102-727">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-728">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-728">AppService</span></span>
* <span data-ttu-id="c1102-729">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-729">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="c1102-730">構成</span><span class="sxs-lookup"><span data-stu-id="c1102-730">Configure</span></span>
* <span data-ttu-id="c1102-731">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-731">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="c1102-732">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-732">Container</span></span>
* <span data-ttu-id="c1102-733">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-733">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="c1102-734">EventHub</span><span class="sxs-lookup"><span data-stu-id="c1102-734">EventHub</span></span>
* <span data-ttu-id="c1102-735">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-735">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="c1102-736">Interactive</span><span class="sxs-lookup"><span data-stu-id="c1102-736">Interactive</span></span>
* <span data-ttu-id="c1102-737">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="c1102-737">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-738">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-738">Monitor</span></span>
* <span data-ttu-id="c1102-739">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-739">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="c1102-740">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-740">Network</span></span>
* <span data-ttu-id="c1102-741">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-741">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="c1102-742">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-742">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="c1102-743">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-743">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="c1102-744">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c1102-744">Profile</span></span>
* <span data-ttu-id="c1102-745">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-745">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="c1102-746">RDBMS</span><span class="sxs-lookup"><span data-stu-id="c1102-746">RDBMS</span></span>
* <span data-ttu-id="c1102-747">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-747">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-748">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-748">Resource</span></span>
* <span data-ttu-id="c1102-749">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-749">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="c1102-750">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-750">Role</span></span>
* <span data-ttu-id="c1102-751">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-751">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="c1102-752">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-752">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="c1102-753">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-753">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-754">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-754">Storage</span></span>
* <span data-ttu-id="c1102-755">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="c1102-755">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-756">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-756">VM</span></span>
* <span data-ttu-id="c1102-757">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-757">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="c1102-758">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-758">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="c1102-759">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-759">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="c1102-760">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-760">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="c1102-761">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="c1102-761">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="c1102-762">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-762">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="c1102-763">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="c1102-763">October 23, 2018</span></span>

<span data-ttu-id="c1102-764">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="c1102-764">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="c1102-765">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-765">Core</span></span>
* <span data-ttu-id="c1102-766">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-766">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="c1102-767">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-767">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-768">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-768">ACR</span></span>
* <span data-ttu-id="c1102-769">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-769">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="c1102-770">CDN</span><span class="sxs-lookup"><span data-stu-id="c1102-770">CDN</span></span>
* <span data-ttu-id="c1102-771">[破壊的変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="c1102-771">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="c1102-772">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-772">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="c1102-773">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-773">Container</span></span>
* <span data-ttu-id="c1102-774">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-774">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="c1102-775">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-775">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="c1102-776">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-776">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="c1102-777">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-777">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="c1102-778">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-778">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="c1102-779">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-779">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="c1102-780">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-780">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="c1102-781">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="c1102-781">CosmosDB</span></span>
* <span data-ttu-id="c1102-782">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-782">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="c1102-783">Interactive</span><span class="sxs-lookup"><span data-stu-id="c1102-783">Interactive</span></span>
* <span data-ttu-id="c1102-784">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-784">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="c1102-785">IoT Central</span><span class="sxs-lookup"><span data-stu-id="c1102-785">IoT Central</span></span>
* <span data-ttu-id="c1102-786">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-786">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="c1102-787">[破壊的変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="c1102-787">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-788">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-788">Monitor</span></span>
* <span data-ttu-id="c1102-789">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="c1102-789">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="c1102-790">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-790">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="c1102-791">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-791">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="c1102-792">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-792">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="c1102-793">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-793">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="c1102-794">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-794">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="c1102-795">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="c1102-795">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="c1102-796">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-796">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="c1102-797">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-797">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="c1102-798">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-798">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="c1102-799">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-799">Network</span></span>
* <span data-ttu-id="c1102-800">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-800">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="c1102-801">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-801">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="c1102-802">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1102-802">ServiceBus</span></span>
* <span data-ttu-id="c1102-803">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-803">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-804">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-804">SQL</span></span>
* <span data-ttu-id="c1102-805">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-805">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-806">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-806">Storage</span></span>
* <span data-ttu-id="c1102-807">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-807">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="c1102-808">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-808">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-809">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-809">VM</span></span>
* <span data-ttu-id="c1102-810">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="c1102-810">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="c1102-811">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-811">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="c1102-812">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-812">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="c1102-813">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="c1102-813">October 16, 2018</span></span>

<span data-ttu-id="c1102-814">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="c1102-814">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-815">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-815">VM</span></span>
* <span data-ttu-id="c1102-816">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-816">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="c1102-817">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="c1102-817">October 9, 2018</span></span>

<span data-ttu-id="c1102-818">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="c1102-818">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="c1102-819">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-819">Core</span></span>
* <span data-ttu-id="c1102-820">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-820">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-821">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-821">ACR</span></span>
* <span data-ttu-id="c1102-822">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-822">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-823">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-823">ACS</span></span>
* <span data-ttu-id="c1102-824">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="c1102-824">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="c1102-825">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-825">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="c1102-826">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-826">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="c1102-827">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-827">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="c1102-828">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-828">Container</span></span>
* <span data-ttu-id="c1102-829">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-829">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="c1102-830">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-830">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="c1102-831">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="c1102-831">Event Hub</span></span>
* <span data-ttu-id="c1102-832">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-832">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="c1102-833">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-833">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="c1102-834">Extensions</span><span class="sxs-lookup"><span data-stu-id="c1102-834">Extensions</span></span>
* <span data-ttu-id="c1102-835">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-835">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="c1102-836">HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1102-836">HDInsight</span></span>
* <span data-ttu-id="c1102-837">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c1102-837">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="c1102-838">IoT</span><span class="sxs-lookup"><span data-stu-id="c1102-838">IoT</span></span>
* <span data-ttu-id="c1102-839">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-839">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="c1102-840">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1102-840">KeyVault</span></span>
* <span data-ttu-id="c1102-841">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-841">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="c1102-842">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-842">Network</span></span>
* <span data-ttu-id="c1102-843">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="c1102-843">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="c1102-844">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="c1102-844">See #6052</span></span>
* <span data-ttu-id="c1102-845">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-845">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="c1102-846">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="c1102-846">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="c1102-847">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-847">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="c1102-848">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-848">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="c1102-849">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-849">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="c1102-850">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-850">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="c1102-851">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-851">Role</span></span>
* <span data-ttu-id="c1102-852">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-852">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="c1102-853">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-853">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="c1102-854">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-854">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="c1102-855">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-855">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="c1102-856">Service Bus</span><span class="sxs-lookup"><span data-stu-id="c1102-856">Service Bus</span></span>
* <span data-ttu-id="c1102-857">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-857">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-858">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-858">VM</span></span>
* <span data-ttu-id="c1102-859">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-859">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="c1102-860">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-860">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="c1102-861">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-861">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="c1102-862">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-862">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="c1102-863">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-863">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="c1102-864">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-864">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="c1102-865">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="c1102-865">September 21, 2018</span></span>

<span data-ttu-id="c1102-866">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="c1102-866">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-867">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-867">ACR</span></span>
* <span data-ttu-id="c1102-868">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-868">Added ACR Task commands</span></span>
* <span data-ttu-id="c1102-869">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-869">Added quick run command</span></span>
* <span data-ttu-id="c1102-870">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-870">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="c1102-871">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-871">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="c1102-872">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-872">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="c1102-873">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-873">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-874">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-874">ACS</span></span>
* <span data-ttu-id="c1102-875">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-875">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="c1102-876">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-876">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-877">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-877">AppService</span></span>

* <span data-ttu-id="c1102-878">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-878">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="c1102-879">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-879">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="c1102-880">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-880">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="c1102-881">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-881">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="c1102-882">Batch</span><span class="sxs-lookup"><span data-stu-id="c1102-882">Batch</span></span>
* <span data-ttu-id="c1102-883">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-883">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="c1102-884">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-884">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="c1102-885">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-885">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="c1102-886">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-886">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="c1102-887">Batch AI</span><span class="sxs-lookup"><span data-stu-id="c1102-887">Batch AI</span></span> 
* <span data-ttu-id="c1102-888">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-888">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="c1102-889">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="c1102-889">Cognitive Services</span></span>
* <span data-ttu-id="c1102-890">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-890">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="c1102-891">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-891">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="c1102-892">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-892">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="c1102-893">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-893">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="c1102-894">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-894">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="c1102-895">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-895">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="c1102-896">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-896">Container</span></span>
* <span data-ttu-id="c1102-897">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-897">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="c1102-898">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-898">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="c1102-899">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-899">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="c1102-900">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-900">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="c1102-901">DataLake</span><span class="sxs-lookup"><span data-stu-id="c1102-901">Datalake</span></span>
* <span data-ttu-id="c1102-902">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-902">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="c1102-903">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="c1102-903">Interactive Shell</span></span>
* <span data-ttu-id="c1102-904">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-904">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="c1102-905">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-905">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="c1102-906">IoT</span><span class="sxs-lookup"><span data-stu-id="c1102-906">IoT</span></span>
* <span data-ttu-id="c1102-907">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-907">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="c1102-908">Key Vault</span><span class="sxs-lookup"><span data-stu-id="c1102-908">Key Vault</span></span>
* <span data-ttu-id="c1102-909">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-909">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="c1102-910">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-910">Network</span></span>
* <span data-ttu-id="c1102-911">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-911">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="c1102-912">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-912">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="c1102-913">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-913">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="c1102-914">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-914">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="c1102-915">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-915">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="c1102-916">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-916">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="c1102-917">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="c1102-917">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="c1102-918">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-918">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="c1102-919">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-919">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="c1102-920">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-920">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="c1102-921">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-921">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="c1102-922">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-922">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="c1102-923">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-923">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="c1102-924">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="c1102-924">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="c1102-925">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-925">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="c1102-926">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-926">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="c1102-927">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-927">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="c1102-928">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-928">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="c1102-929">RDBMS</span><span class="sxs-lookup"><span data-stu-id="c1102-929">RDBMS</span></span>
* <span data-ttu-id="c1102-930">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-930">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="c1102-931">予約</span><span class="sxs-lookup"><span data-stu-id="c1102-931">Reservation</span></span>
* <span data-ttu-id="c1102-932">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-932">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="c1102-933">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-933">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="c1102-934">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="c1102-934">Manage App</span></span>
* <span data-ttu-id="c1102-935">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-935">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="c1102-936">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-936">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="c1102-937">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-937">Role</span></span>
* <span data-ttu-id="c1102-938">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-938">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="c1102-939">SignalR</span><span class="sxs-lookup"><span data-stu-id="c1102-939">SignalR</span></span>
* <span data-ttu-id="c1102-940">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c1102-940">First release</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-941">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-941">Storage</span></span>
* <span data-ttu-id="c1102-942">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-942">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="c1102-943">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-943">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-944">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-944">VM</span></span>
* <span data-ttu-id="c1102-945">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="c1102-945">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="c1102-946">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-946">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="c1102-947">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="c1102-947">August 28, 2018</span></span>

<span data-ttu-id="c1102-948">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="c1102-948">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="c1102-949">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-949">Core</span></span>

* <span data-ttu-id="c1102-950">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-950">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="c1102-951">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-951">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-952">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-952">ACR</span></span>

* <span data-ttu-id="c1102-953">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-953">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="c1102-954">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-954">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-955">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-955">ACS</span></span>

* <span data-ttu-id="c1102-956">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-956">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="c1102-957">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-957">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-958">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-958">AppService</span></span>

* <span data-ttu-id="c1102-959">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-959">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="c1102-960">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-960">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="c1102-961">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-961">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="c1102-962">バックアップ</span><span class="sxs-lookup"><span data-stu-id="c1102-962">Backup</span></span>

* <span data-ttu-id="c1102-963">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-963">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="c1102-964">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="c1102-964">Bot Service</span></span>

* <span data-ttu-id="c1102-965">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="c1102-965">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="c1102-966">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="c1102-966">Cognitive Services</span></span>

* <span data-ttu-id="c1102-967">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-967">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="c1102-968">IoT</span><span class="sxs-lookup"><span data-stu-id="c1102-968">IoT</span></span>

* <span data-ttu-id="c1102-969">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-969">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-970">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-970">Monitor</span></span>

* <span data-ttu-id="c1102-971">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-971">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="c1102-972">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-972">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="c1102-973">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-973">Network</span></span>

* <span data-ttu-id="c1102-974">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-974">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-975">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-975">Resource</span></span>

* <span data-ttu-id="c1102-976">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-976">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-977">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-977">Storage</span></span>

* <span data-ttu-id="c1102-978">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-978">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-979">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-979">VM</span></span>

* <span data-ttu-id="c1102-980">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-980">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="c1102-981">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-981">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="c1102-982">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="c1102-982">Auguest 14, 2018</span></span>

<span data-ttu-id="c1102-983">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="c1102-983">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="c1102-984">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-984">Core</span></span>

* <span data-ttu-id="c1102-985">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-985">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="c1102-986">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-986">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="c1102-987">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="c1102-987">Telemetry</span></span>

* <span data-ttu-id="c1102-988">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-988">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-989">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-989">ACR</span></span>

* <span data-ttu-id="c1102-990">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-990">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="c1102-991">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-991">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-992">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-992">ACS</span></span>

* <span data-ttu-id="c1102-993">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-993">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="c1102-994">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-994">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="c1102-995">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-995">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="c1102-996">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-996">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="c1102-997">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-997">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="c1102-998">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-998">AppService</span></span>

* <span data-ttu-id="c1102-999">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-999">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="c1102-1000">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1000">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="c1102-1001">BatchAI</span><span class="sxs-lookup"><span data-stu-id="c1102-1001">BatchAI</span></span>

* <span data-ttu-id="c1102-1002">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1002">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="c1102-1003">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-1003">Container</span></span>

* <span data-ttu-id="c1102-1004">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1004">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="c1102-1005">IoT</span><span class="sxs-lookup"><span data-stu-id="c1102-1005">IoT</span></span>

* <span data-ttu-id="c1102-1006">[破壊的変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1006">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="c1102-1007">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1007">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="c1102-1008">Iot Central</span><span class="sxs-lookup"><span data-stu-id="c1102-1008">Iot Central</span></span>

* <span data-ttu-id="c1102-1009">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c1102-1009">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="c1102-1010">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1102-1010">KeyVault</span></span>


* <span data-ttu-id="c1102-1011">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1011">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="c1102-1012">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1012">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="c1102-1013">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1013">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="c1102-1014">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1014">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="c1102-1015">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1015">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="c1102-1016">リレー</span><span class="sxs-lookup"><span data-stu-id="c1102-1016">Relay</span></span>

* <span data-ttu-id="c1102-1017">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c1102-1017">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-1018">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-1018">Sql</span></span>

* <span data-ttu-id="c1102-1019">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1019">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1020">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1020">Storage</span></span>

* <span data-ttu-id="c1102-1021">[破壊的変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="c1102-1021">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="c1102-1022">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1022">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="c1102-1023">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1023">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="c1102-1024">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1024">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="c1102-1025">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1025">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1026">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1026">VM</span></span>

* <span data-ttu-id="c1102-1027">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1027">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="c1102-1028">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="c1102-1028">July 31, 2018</span></span>

<span data-ttu-id="c1102-1029">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="c1102-1029">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-1030">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-1030">ACR</span></span>

* <span data-ttu-id="c1102-1031">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1031">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="c1102-1032">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1032">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1033">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1033">ACS</span></span>

* <span data-ttu-id="c1102-1034">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1034">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="c1102-1035">Batch</span><span class="sxs-lookup"><span data-stu-id="c1102-1035">Batch</span></span>

* <span data-ttu-id="c1102-1036">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1036">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="c1102-1037">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-1037">Container</span></span>

* <span data-ttu-id="c1102-1038">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1038">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1039">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1039">Network</span></span>

* <span data-ttu-id="c1102-1040">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1040">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="c1102-1041">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-1041">Resource</span></span>

* <span data-ttu-id="c1102-1042">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1042">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="c1102-1043">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1043">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="c1102-1044">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-1044">Role</span></span>

* <span data-ttu-id="c1102-1045">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1045">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="c1102-1046">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1046">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="c1102-1047">Search</span><span class="sxs-lookup"><span data-stu-id="c1102-1047">Search</span></span>

* <span data-ttu-id="c1102-1048">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1048">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="c1102-1049">Service Bus</span><span class="sxs-lookup"><span data-stu-id="c1102-1049">Service Bus</span></span>

* <span data-ttu-id="c1102-1050">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1050">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="c1102-1051">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1051">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="c1102-1052">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="c1102-1052">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="c1102-1053">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="c1102-1053">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1054">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1054">Storage</span></span>

* <span data-ttu-id="c1102-1055">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-1055">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="c1102-1056">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1056">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1057">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1057">VM</span></span>

* <span data-ttu-id="c1102-1058">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-1058">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="c1102-1059">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1059">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="c1102-1060">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1060">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="c1102-1061">[破壊的変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1061">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="c1102-1062">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1062">July 18, 2018</span></span>

<span data-ttu-id="c1102-1063">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="c1102-1063">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="c1102-1064">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-1064">Core</span></span>

* <span data-ttu-id="c1102-1065">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1065">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="c1102-1066">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1066">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="c1102-1067">[破壊的変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1067">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-1068">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-1068">ACR</span></span>

* <span data-ttu-id="c1102-1069">[破壊的変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1069">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="c1102-1070">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1070">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="c1102-1071">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1071">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="c1102-1072">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1072">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1073">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1073">ACS</span></span>

* <span data-ttu-id="c1102-1074">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1074">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1075">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-1075">AppService</span></span>

* <span data-ttu-id="c1102-1076">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1076">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="c1102-1077">Batch</span><span class="sxs-lookup"><span data-stu-id="c1102-1077">Batch</span></span>

* <span data-ttu-id="c1102-1078">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1078">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="c1102-1079">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1079">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="c1102-1080">Batch AI</span><span class="sxs-lookup"><span data-stu-id="c1102-1080">Batch AI</span></span>

* <span data-ttu-id="c1102-1081">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1081">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="c1102-1082">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-1082">Container</span></span>

* <span data-ttu-id="c1102-1083">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1083">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="c1102-1084">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1084">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1085">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1085">Network</span></span>

* <span data-ttu-id="c1102-1086">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1086">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="c1102-1087">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1087">Added `network nic wait`</span></span>
* <span data-ttu-id="c1102-1088">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1088">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="c1102-1089">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1089">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="c1102-1090">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-1090">Resource</span></span>

* <span data-ttu-id="c1102-1091">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1091">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="c1102-1092">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1092">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="c1102-1093">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1093">Added `deployment wait` command</span></span>
* <span data-ttu-id="c1102-1094">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1094">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-1095">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-1095">SQL</span></span>

* <span data-ttu-id="c1102-1096">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1096">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="c1102-1097">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-1097">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="c1102-1098">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1098">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1099">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1099">Storage</span></span>

* <span data-ttu-id="c1102-1100">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1100">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1101">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1101">VM</span></span>

* <span data-ttu-id="c1102-1102">[破壊的変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1102">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="c1102-1103">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1103">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="c1102-1104">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1104">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="c1102-1105">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1105">July 3, 2018</span></span>

<span data-ttu-id="c1102-1106">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="c1102-1106">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="c1102-1107">AKS</span><span class="sxs-lookup"><span data-stu-id="c1102-1107">AKS</span></span>

* <span data-ttu-id="c1102-1108">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1108">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="c1102-1109">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1109">July 3, 2018</span></span>

<span data-ttu-id="c1102-1110">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="c1102-1110">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="c1102-1111">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-1111">Core</span></span>

* <span data-ttu-id="c1102-1112">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1112">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-1113">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-1113">ACR</span></span>

* <span data-ttu-id="c1102-1114">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1114">Added polling build status</span></span>
* <span data-ttu-id="c1102-1115">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1115">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="c1102-1116">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1116">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1117">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1117">ACS</span></span>

* <span data-ttu-id="c1102-1118">[破壊的変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1118">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="c1102-1119">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1119">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="c1102-1120">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1120">Updated options for `aks browse` command.</span></span> <span data-ttu-id="c1102-1121">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1121">Added `--listen-port` support</span></span>
* <span data-ttu-id="c1102-1122">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1122">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="c1102-1123">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="c1102-1123">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="c1102-1124">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1124">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1125">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-1125">AppService</span></span>

* <span data-ttu-id="c1102-1126">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-1126">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="c1102-1127">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1127">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="c1102-1128">バックアップ</span><span class="sxs-lookup"><span data-stu-id="c1102-1128">Backup</span></span>

* <span data-ttu-id="c1102-1129">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1129">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="c1102-1130">BatchAI</span><span class="sxs-lookup"><span data-stu-id="c1102-1130">BatchAI</span></span>

* <span data-ttu-id="c1102-1131">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1131">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="c1102-1132">クラウド</span><span class="sxs-lookup"><span data-stu-id="c1102-1132">Cloud</span></span>

* <span data-ttu-id="c1102-1133">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1133">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="c1102-1134">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-1134">Container</span></span>

* <span data-ttu-id="c1102-1135">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1135">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="c1102-1136">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1136">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="c1102-1137">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1137">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="c1102-1138">拡張機能</span><span class="sxs-lookup"><span data-stu-id="c1102-1138">Extension</span></span>

* <span data-ttu-id="c1102-1139">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1139">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1140">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1140">Network</span></span>

* <span data-ttu-id="c1102-1141">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1141">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="c1102-1142">Rdbms</span><span class="sxs-lookup"><span data-stu-id="c1102-1142">Rdbms</span></span>

* <span data-ttu-id="c1102-1143">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1143">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-1144">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-1144">Resource</span></span>

* <span data-ttu-id="c1102-1145">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1145">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1146">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1146">VM</span></span>

* <span data-ttu-id="c1102-1147">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-1147">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="c1102-1148">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1148">June 25, 2018</span></span>

<span data-ttu-id="c1102-1149">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="c1102-1149">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="c1102-1150">CLI</span><span class="sxs-lookup"><span data-stu-id="c1102-1150">CLI</span></span>

* <span data-ttu-id="c1102-1151">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1151">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="c1102-1152">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1152">June 19, 2018</span></span>

<span data-ttu-id="c1102-1153">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="c1102-1153">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="c1102-1154">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-1154">Core</span></span>

* <span data-ttu-id="c1102-1155">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1155">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-1156">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-1156">ACR</span></span>

* <span data-ttu-id="c1102-1157">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1157">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="c1102-1158">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1158">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1159">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1159">ACS</span></span>

* <span data-ttu-id="c1102-1160">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1160">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="c1102-1161">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1161">Added `--update` support</span></span>
* <span data-ttu-id="c1102-1162">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1162">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="c1102-1163">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1163">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="c1102-1164">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1164">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="c1102-1165">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1165">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="c1102-1166">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1166">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="c1102-1167">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1167">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1168">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-1168">AppService</span></span>

* <span data-ttu-id="c1102-1169">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1169">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="c1102-1170">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1170">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="c1102-1171">Batch</span><span class="sxs-lookup"><span data-stu-id="c1102-1171">Batch</span></span>

* <span data-ttu-id="c1102-1172">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1172">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="c1102-1173">Batch AI</span><span class="sxs-lookup"><span data-stu-id="c1102-1173">Batch AI</span></span>

* <span data-ttu-id="c1102-1174">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1174">Added support for workspaces.</span></span> <span data-ttu-id="c1102-1175">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="c1102-1175">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="c1102-1176">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1176">Added support for experiments.</span></span> <span data-ttu-id="c1102-1177">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="c1102-1177">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="c1102-1178">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1178">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="c1102-1179">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1179">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="c1102-1180">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="c1102-1180">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="c1102-1181">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1181">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="c1102-1182">[破壊的変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="c1102-1182">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="c1102-1183">[破壊的変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="c1102-1183">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="c1102-1184">[破壊的変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1184">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="c1102-1185">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="c1102-1185">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="c1102-1186">[破壊的変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1186">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="c1102-1187">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="c1102-1187">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="c1102-1188">[破壊的変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1188">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="c1102-1189">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="c1102-1189">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="c1102-1190">[破壊的変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1190">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="c1102-1191">[破壊的変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1191">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="c1102-1192">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1192">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="c1102-1193">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1193">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="c1102-1194">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1194">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="c1102-1195">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1195">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="c1102-1196">マップ</span><span class="sxs-lookup"><span data-stu-id="c1102-1196">Maps</span></span>

* <span data-ttu-id="c1102-1197">[破壊的変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1197">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1198">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1198">Network</span></span>

* <span data-ttu-id="c1102-1199">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="c1102-1199">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="c1102-1200">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1200">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="c1102-1201">#6502</span><span class="sxs-lookup"><span data-stu-id="c1102-1201">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="c1102-1202">Reservations</span><span class="sxs-lookup"><span data-stu-id="c1102-1202">Reservations</span></span>

* <span data-ttu-id="c1102-1203">[破壊的変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1203">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="c1102-1204">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1204">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="c1102-1205">[破壊的変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1205">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="c1102-1206">[破壊的変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1206">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="c1102-1207">[破壊的変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1207">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="c1102-1208">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1208">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="c1102-1209">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-1209">Role</span></span>

* <span data-ttu-id="c1102-1210">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1210">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-1211">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-1211">SQL</span></span>

* <span data-ttu-id="c1102-1212">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1212">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1213">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1213">Storage</span></span>

* <span data-ttu-id="c1102-1214">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1214">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1215">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1215">VM</span></span>

* <span data-ttu-id="c1102-1216">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1216">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="c1102-1217">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1217">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="c1102-1218">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1218">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="c1102-1219">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1219">June 13, 2018</span></span>

<span data-ttu-id="c1102-1220">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="c1102-1220">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="c1102-1221">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-1221">Core</span></span>

* <span data-ttu-id="c1102-1222">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1222">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="c1102-1223">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1223">June 13, 2018</span></span>

<span data-ttu-id="c1102-1224">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="c1102-1224">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="c1102-1225">AKS</span><span class="sxs-lookup"><span data-stu-id="c1102-1225">AKS</span></span>

* <span data-ttu-id="c1102-1226">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1226">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="c1102-1227">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1227">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="c1102-1228">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1228">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="c1102-1229">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1229">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="c1102-1230">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1230">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1231">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-1231">AppService</span></span>

* <span data-ttu-id="c1102-1232">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1232">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="c1102-1233">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1233">June 5, 2018</span></span>

<span data-ttu-id="c1102-1234">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="c1102-1234">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="c1102-1235">Interactive</span><span class="sxs-lookup"><span data-stu-id="c1102-1235">Interactive</span></span>

* <span data-ttu-id="c1102-1236">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1236">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="c1102-1237">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1237">June 5, 2018</span></span>

<span data-ttu-id="c1102-1238">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="c1102-1238">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="c1102-1239">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-1239">Core</span></span>

* <span data-ttu-id="c1102-1240">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1240">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="c1102-1241">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1241">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-1242">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-1242">ACR</span></span>

* <span data-ttu-id="c1102-1243">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1243">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="c1102-1244">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1244">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="c1102-1245">AKS</span><span class="sxs-lookup"><span data-stu-id="c1102-1245">AKS</span></span>

* <span data-ttu-id="c1102-1246">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1246">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="c1102-1247">Batch</span><span class="sxs-lookup"><span data-stu-id="c1102-1247">Batch</span></span>

* <span data-ttu-id="c1102-1248">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1248">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="c1102-1249">IoT</span><span class="sxs-lookup"><span data-stu-id="c1102-1249">IOT</span></span>

* <span data-ttu-id="c1102-1250">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1250">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1251">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1251">Network</span></span>

* <span data-ttu-id="c1102-1252">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1252">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="c1102-1253">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="c1102-1253">Policy Insights</span></span>

* <span data-ttu-id="c1102-1254">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c1102-1254">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="c1102-1255">ARM</span><span class="sxs-lookup"><span data-stu-id="c1102-1255">ARM</span></span>

* <span data-ttu-id="c1102-1256">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1256">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-1257">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-1257">SQL</span></span>

* <span data-ttu-id="c1102-1258">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1258">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="c1102-1259">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1259">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="c1102-1260">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1260">Storage</span></span>

* <span data-ttu-id="c1102-1261">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1261">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1262">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1262">VM</span></span>

* <span data-ttu-id="c1102-1263">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1263">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="c1102-1264">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1264">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="c1102-1265">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1265">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="c1102-1266">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1266">May 22, 2018</span></span>

<span data-ttu-id="c1102-1267">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="c1102-1267">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="c1102-1268">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-1268">Core</span></span>

* <span data-ttu-id="c1102-1269">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1269">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1270">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1270">ACS</span></span>

* <span data-ttu-id="c1102-1271">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1271">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="c1102-1272">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1272">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1273">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-1273">AppService</span></span>

* <span data-ttu-id="c1102-1274">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1274">Improved generic update commands</span></span>
* <span data-ttu-id="c1102-1275">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1275">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="c1102-1276">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-1276">Container</span></span>

* <span data-ttu-id="c1102-1277">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1277">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="c1102-1278">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1278">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="c1102-1279">拡張機能</span><span class="sxs-lookup"><span data-stu-id="c1102-1279">Extension</span></span>

* <span data-ttu-id="c1102-1280">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1280">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="c1102-1281">Interactive</span><span class="sxs-lookup"><span data-stu-id="c1102-1281">Interactive</span></span>

* <span data-ttu-id="c1102-1282">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1282">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="c1102-1283">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1283">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="c1102-1284">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1102-1284">KeyVault</span></span>

* <span data-ttu-id="c1102-1285">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1285">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1286">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1286">Network</span></span>

* <span data-ttu-id="c1102-1287">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1287">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="c1102-1288">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1288">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-1289">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-1289">SQL</span></span>

* <span data-ttu-id="c1102-1290">[破壊的変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1290">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="c1102-1291">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1291">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="c1102-1292">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1292">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="c1102-1293">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1293">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="c1102-1294">[破壊的変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1294">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="c1102-1295">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="c1102-1295">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="c1102-1296">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="c1102-1296">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="c1102-1297">`edition`</span><span class="sxs-lookup"><span data-stu-id="c1102-1297">`edition`.</span></span> <span data-ttu-id="c1102-1298">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="c1102-1298">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="c1102-1299">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="c1102-1299">`elasticPoolName`.</span></span> <span data-ttu-id="c1102-1300">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="c1102-1300">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="c1102-1301">[破壊的変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1301">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="c1102-1302">`edition`</span><span class="sxs-lookup"><span data-stu-id="c1102-1302">`edition`.</span></span> <span data-ttu-id="c1102-1303">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="c1102-1303">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="c1102-1304">`dtu`</span><span class="sxs-lookup"><span data-stu-id="c1102-1304">`dtu`.</span></span> <span data-ttu-id="c1102-1305">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="c1102-1305">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="c1102-1306">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="c1102-1306">`databaseDtuMin`.</span></span> <span data-ttu-id="c1102-1307">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="c1102-1307">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="c1102-1308">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="c1102-1308">`databaseDtuMax`.</span></span> <span data-ttu-id="c1102-1309">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="c1102-1309">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="c1102-1310">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1310">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="c1102-1311">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1311">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1312">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1312">Storage</span></span>

* <span data-ttu-id="c1102-1313">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1313">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="c1102-1314">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1314">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1315">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1315">VM</span></span>

* <span data-ttu-id="c1102-1316">[破壊的変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1316">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="c1102-1317">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="c1102-1317">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="c1102-1318">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1318">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="c1102-1319">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1319">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="c1102-1320">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1320">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="c1102-1321">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1321">May 7, 2018</span></span>

<span data-ttu-id="c1102-1322">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="c1102-1322">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="c1102-1323">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-1323">Core</span></span>

* <span data-ttu-id="c1102-1324">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1324">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="c1102-1325">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1325">Added limited support for positional arguments</span></span>
* <span data-ttu-id="c1102-1326">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1326">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="c1102-1327">#5591</span><span class="sxs-lookup"><span data-stu-id="c1102-1327">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="c1102-1328">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1328">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="c1102-1329">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="c1102-1329">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="c1102-1330">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1330">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="c1102-1331">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1331">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="c1102-1332">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1332">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-1333">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-1333">ACR</span></span>

* <span data-ttu-id="c1102-1334">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1334">Added ACR Build commands</span></span>
* <span data-ttu-id="c1102-1335">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1335">Improved resource not found error messages</span></span>
* <span data-ttu-id="c1102-1336">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1336">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="c1102-1337">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1337">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="c1102-1338">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1338">Improved repository commands error messages</span></span>
* <span data-ttu-id="c1102-1339">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1339">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1340">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1340">ACS</span></span>

* <span data-ttu-id="c1102-1341">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1341">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="c1102-1342">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1342">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="c1102-1343">AMS</span><span class="sxs-lookup"><span data-stu-id="c1102-1343">AMS</span></span>

* <span data-ttu-id="c1102-1344">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="c1102-1344">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1345">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-1345">Appservice</span></span>

* <span data-ttu-id="c1102-1346">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1346">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="c1102-1347">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1347">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="c1102-1348">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1348">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="c1102-1349">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1349">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="c1102-1350">Batch AI</span><span class="sxs-lookup"><span data-stu-id="c1102-1350">Batch AI</span></span>

* <span data-ttu-id="c1102-1351">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1351">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="c1102-1352">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="c1102-1352">Cognitive Services</span></span>

* <span data-ttu-id="c1102-1353">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1353">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="c1102-1354">消費</span><span class="sxs-lookup"><span data-stu-id="c1102-1354">Consumption</span></span>

* <span data-ttu-id="c1102-1355">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1355">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="c1102-1356">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-1356">Container</span></span>

* <span data-ttu-id="c1102-1357">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1357">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="c1102-1358">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="c1102-1358">Cosmos DB</span></span>

* <span data-ttu-id="c1102-1359">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1359">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="c1102-1360">DMS</span><span class="sxs-lookup"><span data-stu-id="c1102-1360">DMS</span></span>

* <span data-ttu-id="c1102-1361">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1361">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="c1102-1362">拡張機能</span><span class="sxs-lookup"><span data-stu-id="c1102-1362">Extension</span></span>

* <span data-ttu-id="c1102-1363">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1363">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="c1102-1364">Interactive</span><span class="sxs-lookup"><span data-stu-id="c1102-1364">Interactive</span></span>

* <span data-ttu-id="c1102-1365">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-1365">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="c1102-1366">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1366">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="c1102-1367">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1367">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="c1102-1368">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1368">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="c1102-1369">ラボ</span><span class="sxs-lookup"><span data-stu-id="c1102-1369">Lab</span></span>

* <span data-ttu-id="c1102-1370">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1370">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1371">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1371">Network</span></span>

* <span data-ttu-id="c1102-1372">[破壊的変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1372">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="c1102-1373">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c1102-1373">Profile</span></span>

* <span data-ttu-id="c1102-1374">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1374">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="c1102-1375">[破壊的変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1375">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="c1102-1376">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1376">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="c1102-1377">Redis</span><span class="sxs-lookup"><span data-stu-id="c1102-1377">Redis</span></span>

* <span data-ttu-id="c1102-1378">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1378">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="c1102-1379">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1379">Deprecated `redis list-all`.</span></span> <span data-ttu-id="c1102-1380">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="c1102-1380">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="c1102-1381">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1381">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="c1102-1382">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1382">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="c1102-1383">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-1383">Role</span></span>

* <span data-ttu-id="c1102-1384">[破壊的変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1384">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1385">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1385">Storage</span></span>

* <span data-ttu-id="c1102-1386">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="c1102-1386">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="c1102-1387">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1387">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="c1102-1388">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="c1102-1388">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="c1102-1389">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="c1102-1389">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="c1102-1390">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1390">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1391">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1391">VM</span></span>

* <span data-ttu-id="c1102-1392">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1392">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="c1102-1393">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1393">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="c1102-1394">[破壊的変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="c1102-1394">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="c1102-1395">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1395">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="c1102-1396">[破壊的変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1396">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="c1102-1397">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1397">Added write accelerator support</span></span>
* <span data-ttu-id="c1102-1398">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1398">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="c1102-1399">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1399">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="c1102-1400">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1400">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="c1102-1401">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1401">April 10, 2018</span></span>

<span data-ttu-id="c1102-1402">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="c1102-1402">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-1403">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-1403">ACR</span></span>

* <span data-ttu-id="c1102-1404">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1404">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1405">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1405">ACS</span></span>

* <span data-ttu-id="c1102-1406">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1406">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1407">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-1407">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="c1102-1409">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1409">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="c1102-1410">BatchAI</span><span class="sxs-lookup"><span data-stu-id="c1102-1410">BatchAI</span></span>

* <span data-ttu-id="c1102-1411">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1411">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="c1102-1412">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="c1102-1412">Job level mounting</span></span>
  - <span data-ttu-id="c1102-1413">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="c1102-1413">Environment variables with secret values</span></span>
  - <span data-ttu-id="c1102-1414">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="c1102-1414">Performance counters settings</span></span>
  - <span data-ttu-id="c1102-1415">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="c1102-1415">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="c1102-1416">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="c1102-1416">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="c1102-1417">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="c1102-1417">Usage and limits reporting</span></span>
  - <span data-ttu-id="c1102-1418">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="c1102-1418">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="c1102-1419">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="c1102-1419">Support for custom images</span></span>
  - <span data-ttu-id="c1102-1420">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1420">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="c1102-1421">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-1421">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="c1102-1422">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="c1102-1422">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="c1102-1423">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="c1102-1423">National clouds are supported</span></span>
* <span data-ttu-id="c1102-1424">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1424">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="c1102-1425">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1425">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="c1102-1426">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1426">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="c1102-1427">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1427">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="c1102-1428">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="c1102-1428">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="c1102-1429">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="c1102-1429">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="c1102-1430">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1430">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="c1102-1431">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1431">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="c1102-1432">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="c1102-1432">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="c1102-1433">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1433">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="c1102-1434">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1434">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="c1102-1435">[破壊的変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1435">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="c1102-1436">[破壊的変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1436">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="c1102-1437">課金</span><span class="sxs-lookup"><span data-stu-id="c1102-1437">Billing</span></span>

* <span data-ttu-id="c1102-1438">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1438">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="c1102-1439">消費</span><span class="sxs-lookup"><span data-stu-id="c1102-1439">Consumption</span></span>

* <span data-ttu-id="c1102-1440">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1440">Added `marketplace` commands</span></span>
* <span data-ttu-id="c1102-1441">[破壊的変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1441">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="c1102-1442">[破壊的変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1442">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="c1102-1443">[破壊的変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1443">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="c1102-1444">[破壊的変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1444">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="c1102-1445">[破壊的変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1445">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="c1102-1446">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-1446">Container</span></span>

* <span data-ttu-id="c1102-1447">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1447">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="c1102-1448">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1448">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="c1102-1449">拡張機能</span><span class="sxs-lookup"><span data-stu-id="c1102-1449">Extension</span></span>

* <span data-ttu-id="c1102-1450">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1450">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="c1102-1451">Interactive</span><span class="sxs-lookup"><span data-stu-id="c1102-1451">Interactive</span></span>

* <span data-ttu-id="c1102-1452">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1452">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="c1102-1453">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1453">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="c1102-1454">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1454">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1455">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1455">Network</span></span>

* <span data-ttu-id="c1102-1456">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1456">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="c1102-1457">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1457">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="c1102-1458">#4910</span><span class="sxs-lookup"><span data-stu-id="c1102-1458">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="c1102-1459">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1459">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="c1102-1460">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="c1102-1460">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="c1102-1461">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1461">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="c1102-1462">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1462">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="c1102-1463">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1463">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="c1102-1464">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c1102-1464">Profile</span></span>

* <span data-ttu-id="c1102-1465">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1465">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="c1102-1466">[破壊的変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1466">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="c1102-1467">RDBMS</span><span class="sxs-lookup"><span data-stu-id="c1102-1467">RDBMS</span></span>

* <span data-ttu-id="c1102-1468">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1468">Added `georestore` command</span></span>
* <span data-ttu-id="c1102-1469">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1469">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-1470">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-1470">Resource</span></span>

* <span data-ttu-id="c1102-1471">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1471">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="c1102-1472">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1472">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-1473">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-1473">SQL</span></span>

* <span data-ttu-id="c1102-1474">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1474">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1475">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1475">Storage</span></span>

* <span data-ttu-id="c1102-1476">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1476">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1477">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1477">VM</span></span>

* <span data-ttu-id="c1102-1478">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1478">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="c1102-1479">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1479">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="c1102-1481">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1481">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="c1102-1482">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1482">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="c1102-1483">#5718</span><span class="sxs-lookup"><span data-stu-id="c1102-1483">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="c1102-1484">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1484">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="c1102-1485">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1485">March 27, 2018</span></span>

<span data-ttu-id="c1102-1486">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="c1102-1486">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="c1102-1487">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-1487">Core</span></span>

* <span data-ttu-id="c1102-1488">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="c1102-1488">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1489">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1489">ACS</span></span>

* <span data-ttu-id="c1102-1490">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1490">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1491">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-1491">Appservice</span></span>

* <span data-ttu-id="c1102-1492">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1492">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="c1102-1493">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1493">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="c1102-1494">バックアップ</span><span class="sxs-lookup"><span data-stu-id="c1102-1494">Backup</span></span>

* <span data-ttu-id="c1102-1495">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1495">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="c1102-1496">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="c1102-1496">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="c1102-1497">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1497">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="c1102-1498">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1498">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="c1102-1499">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-1499">Container</span></span>

* <span data-ttu-id="c1102-1500">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1500">Added `container exec` command.</span></span> <span data-ttu-id="c1102-1501">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="c1102-1501">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="c1102-1502">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="c1102-1502">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="c1102-1503">拡張機能</span><span class="sxs-lookup"><span data-stu-id="c1102-1503">Extension</span></span>

* <span data-ttu-id="c1102-1504">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1504">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="c1102-1505">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1505">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="c1102-1506">[破壊的変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1506">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="c1102-1507">Interactive</span><span class="sxs-lookup"><span data-stu-id="c1102-1507">Interactive</span></span>

* <span data-ttu-id="c1102-1508">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1508">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="c1102-1509">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1509">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="c1102-1510">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="c1102-1510">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="c1102-1511">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1511">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="c1102-1512">ラボ</span><span class="sxs-lookup"><span data-stu-id="c1102-1512">Lab</span></span>

* <span data-ttu-id="c1102-1513">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1513">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-1514">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-1514">Monitor</span></span>

* <span data-ttu-id="c1102-1515">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="c1102-1515">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="c1102-1516">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="c1102-1516">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="c1102-1517">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="c1102-1517">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1518">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1518">Network</span></span>

* <span data-ttu-id="c1102-1519">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1519">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="c1102-1520">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c1102-1520">Profile</span></span>

* <span data-ttu-id="c1102-1521">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1521">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="c1102-1522">RDBMS</span><span class="sxs-lookup"><span data-stu-id="c1102-1522">RDBMS</span></span>

* <span data-ttu-id="c1102-1523">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1523">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-1524">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-1524">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="c1102-1526">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-1526">Role</span></span>

* <span data-ttu-id="c1102-1527">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1527">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="c1102-1528">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1528">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="c1102-1529">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1529">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="c1102-1530">[破壊的変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1530">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="c1102-1531">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1531">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1532">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1532">Storage</span></span>

* <span data-ttu-id="c1102-1533">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1533">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="c1102-1534">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="c1102-1534">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1535">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1535">VM</span></span>

* <span data-ttu-id="c1102-1536">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1536">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="c1102-1537">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1537">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="c1102-1538">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1538">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="c1102-1539">[破壊的変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1539">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="c1102-1540">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1540">March 13, 2018</span></span>

<span data-ttu-id="c1102-1541">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="c1102-1541">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-1542">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-1542">ACR</span></span>

* <span data-ttu-id="c1102-1543">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1543">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="c1102-1544">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1544">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="c1102-1545">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1545">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1546">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1546">ACS</span></span>

* <span data-ttu-id="c1102-1547">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1547">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="c1102-1548">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1548">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="c1102-1549">Advisor</span><span class="sxs-lookup"><span data-stu-id="c1102-1549">Advisor</span></span>

* <span data-ttu-id="c1102-1550">[破壊的変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1550">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="c1102-1551">[破壊的変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1551">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="c1102-1552">[破壊的変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1552">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="c1102-1553">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1553">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="c1102-1554">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1554">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1555">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-1555">Appservice</span></span>

* <span data-ttu-id="c1102-1556">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1556">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="c1102-1557">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1557">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="c1102-1558">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="c1102-1558">Eventhubs</span></span>

* <span data-ttu-id="c1102-1559">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c1102-1559">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="c1102-1560">拡張機能</span><span class="sxs-lookup"><span data-stu-id="c1102-1560">Extension</span></span>

* <span data-ttu-id="c1102-1561">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1561">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="c1102-1562">Interactive</span><span class="sxs-lookup"><span data-stu-id="c1102-1562">Interactive</span></span>

* <span data-ttu-id="c1102-1563">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="c1102-1563">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="c1102-1564">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="c1102-1564">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="c1102-1565">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="c1102-1565">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="c1102-1566">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1566">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-1567">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-1567">Monitor</span></span>

* <span data-ttu-id="c1102-1568">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1568">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="c1102-1569">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1569">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="c1102-1570">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1570">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="c1102-1571">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1571">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1572">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1572">Network</span></span>

* <span data-ttu-id="c1102-1573">[破壊的変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1573">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="c1102-1574">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1574">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="c1102-1575">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1575">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="c1102-1576">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1576">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="c1102-1577">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c1102-1577">Profile</span></span>

* <span data-ttu-id="c1102-1578">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1578">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="c1102-1579">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1579">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="c1102-1580">RDBMS</span><span class="sxs-lookup"><span data-stu-id="c1102-1580">RDBMS</span></span>

* <span data-ttu-id="c1102-1581">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1581">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="c1102-1582">Service Bus</span><span class="sxs-lookup"><span data-stu-id="c1102-1582">Service Bus</span></span>

* <span data-ttu-id="c1102-1583">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c1102-1583">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1584">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1584">Storage</span></span>

* <span data-ttu-id="c1102-1585">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-1585">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="c1102-1586">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="c1102-1586">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1587">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1587">VM</span></span>

* <span data-ttu-id="c1102-1588">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1588">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="c1102-1589">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1589">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="c1102-1590">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1590">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="c1102-1591">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1591">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="c1102-1592">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1592">February 27, 2018</span></span>

<span data-ttu-id="c1102-1593">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="c1102-1593">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="c1102-1594">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-1594">Core</span></span>

* <span data-ttu-id="c1102-1595">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="c1102-1595">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="c1102-1596">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1596">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="c1102-1597">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1597">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1598">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1598">ACS</span></span>

* <span data-ttu-id="c1102-1599">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1599">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="c1102-1600">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="c1102-1600">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="c1102-1601">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1601">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="c1102-1602">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1602">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1603">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-1603">Appservice</span></span>

* <span data-ttu-id="c1102-1604">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="c1102-1604">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="c1102-1605">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="c1102-1605">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="c1102-1606">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="c1102-1606">Cognitive Services</span></span>

* <span data-ttu-id="c1102-1607">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1607">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="c1102-1608">消費</span><span class="sxs-lookup"><span data-stu-id="c1102-1608">Consumption</span></span>

* <span data-ttu-id="c1102-1609">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1609">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="c1102-1610">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1610">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="c1102-1611">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-1611">Container</span></span>

* <span data-ttu-id="c1102-1612">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1612">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1613">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1613">Network</span></span>

* <span data-ttu-id="c1102-1614">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="c1102-1614">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-1615">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-1615">Resource</span></span>

* <span data-ttu-id="c1102-1616">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1616">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="c1102-1617">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-1617">Role</span></span>

* <span data-ttu-id="c1102-1618">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1618">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-1619">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-1619">SQL</span></span>

* <span data-ttu-id="c1102-1620">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1620">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1621">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1621">Storage</span></span>

* <span data-ttu-id="c1102-1622">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1622">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1623">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1623">VM</span></span>

* <span data-ttu-id="c1102-1624">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1624">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="c1102-1625">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1625">February 13, 2018</span></span>

<span data-ttu-id="c1102-1626">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="c1102-1626">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="c1102-1627">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-1627">Core</span></span>

* <span data-ttu-id="c1102-1628">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1628">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1629">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1629">ACS</span></span>

* <span data-ttu-id="c1102-1630">[破壊的変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1630">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="c1102-1631">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1631">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="c1102-1632">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1632">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="c1102-1633">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1633">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="c1102-1634">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1634">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="c1102-1635">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1635">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="c1102-1636">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1636">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="c1102-1637">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="c1102-1637">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1638">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-1638">Appservice</span></span>

* <span data-ttu-id="c1102-1639">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1639">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="c1102-1640">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1640">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="c1102-1641">CDN</span><span class="sxs-lookup"><span data-stu-id="c1102-1641">CDN</span></span>

* <span data-ttu-id="c1102-1642">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1642">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="c1102-1643">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-1643">Container</span></span>

* <span data-ttu-id="c1102-1644">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1644">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="c1102-1645">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1645">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="c1102-1646">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="c1102-1646">CosmosDB</span></span>

* <span data-ttu-id="c1102-1647">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1647">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="c1102-1648">拡張機能</span><span class="sxs-lookup"><span data-stu-id="c1102-1648">Extension</span></span>

* <span data-ttu-id="c1102-1649">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1649">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="c1102-1650">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1650">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="c1102-1651">フィードバック</span><span class="sxs-lookup"><span data-stu-id="c1102-1651">Feedback</span></span>

* <span data-ttu-id="c1102-1652">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1652">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="c1102-1653">Interactive</span><span class="sxs-lookup"><span data-stu-id="c1102-1653">Interactive</span></span>

* <span data-ttu-id="c1102-1654">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1654">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="c1102-1655">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1655">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="c1102-1656">IoT</span><span class="sxs-lookup"><span data-stu-id="c1102-1656">IoT</span></span>

* <span data-ttu-id="c1102-1657">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1657">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="c1102-1658">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1658">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="c1102-1659">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1659">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="c1102-1660">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1660">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-1661">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-1661">Monitor</span></span>

* <span data-ttu-id="c1102-1662">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1662">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1663">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1663">Network</span></span>

* <span data-ttu-id="c1102-1664">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1664">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="c1102-1665">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c1102-1665">Profile</span></span>

* <span data-ttu-id="c1102-1666">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1666">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-1667">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-1667">Resource</span></span>

* <span data-ttu-id="c1102-1668">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1668">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="c1102-1669">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-1669">Role</span></span>

* <span data-ttu-id="c1102-1670">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1670">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-1671">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-1671">SQL</span></span>

* <span data-ttu-id="c1102-1672">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1672">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="c1102-1673">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1673">Added `sql db rename`</span></span>
* <span data-ttu-id="c1102-1674">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1674">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1675">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1675">Storage</span></span>

* <span data-ttu-id="c1102-1676">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1676">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1677">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1677">VM</span></span>

* <span data-ttu-id="c1102-1678">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1678">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="c1102-1679">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1679">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="c1102-1680">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="c1102-1680">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="c1102-1681">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1681">January 31, 2018</span></span>

<span data-ttu-id="c1102-1682">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="c1102-1682">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="c1102-1683">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-1683">Core</span></span>

* <span data-ttu-id="c1102-1684">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1684">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="c1102-1685">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1685">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="c1102-1686">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1686">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="c1102-1687">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="c1102-1687">Use `--verbose` to see</span></span>
* <span data-ttu-id="c1102-1688">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="c1102-1688">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1689">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1689">ACS</span></span>

* <span data-ttu-id="c1102-1690">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1690">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="c1102-1691">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1691">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1692">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-1692">Appservice</span></span>

* <span data-ttu-id="c1102-1693">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="c1102-1693">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="c1102-1694">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1694">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="c1102-1695">CDN</span><span class="sxs-lookup"><span data-stu-id="c1102-1695">CDN</span></span>

* <span data-ttu-id="c1102-1696">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1696">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="c1102-1697">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="c1102-1697">CosmosDB</span></span>

* <span data-ttu-id="c1102-1698">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1698">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="c1102-1699">Interactive</span><span class="sxs-lookup"><span data-stu-id="c1102-1699">Interactive</span></span>

* <span data-ttu-id="c1102-1700">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1700">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1701">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1701">Network</span></span>

* <span data-ttu-id="c1102-1702">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1702">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="c1102-1703">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1703">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="c1102-1704">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1704">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="c1102-1705">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1705">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="c1102-1706">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1706">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="c1102-1707">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1707">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="c1102-1708">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1708">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="c1102-1709">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1709">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="c1102-1710">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1710">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="c1102-1711">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1711">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="c1102-1712">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c1102-1712">Profile</span></span>

* <span data-ttu-id="c1102-1713">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1713">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-1714">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-1714">Resource</span></span>

* <span data-ttu-id="c1102-1715">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1715">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1716">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1716">Storage</span></span>

* <span data-ttu-id="c1102-1717">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1717">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="c1102-1718">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1718">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="c1102-1719">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1719">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="c1102-1720">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1720">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="c1102-1721">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1721">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1722">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1722">VM</span></span>

* <span data-ttu-id="c1102-1723">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1723">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="c1102-1724">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1724">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="c1102-1725">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1725">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="c1102-1726">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1726">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="c1102-1727">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1727">January 17, 2018</span></span>

<span data-ttu-id="c1102-1728">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="c1102-1728">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-1729">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-1729">ACR</span></span>

* <span data-ttu-id="c1102-1730">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1730">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="c1102-1731">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1731">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1732">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1732">ACS</span></span>

* <span data-ttu-id="c1102-1733">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1733">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="c1102-1734">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1734">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1735">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-1735">Appservice</span></span>

* <span data-ttu-id="c1102-1736">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1736">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="c1102-1737">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1737">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="c1102-1738">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1738">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="c1102-1739">バックアップ</span><span class="sxs-lookup"><span data-stu-id="c1102-1739">Backup</span></span>

* <span data-ttu-id="c1102-1740">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1740">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="c1102-1741">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1741">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="c1102-1742">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1742">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="c1102-1743">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1743">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="c1102-1744">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1744">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="c1102-1745">Batch</span><span class="sxs-lookup"><span data-stu-id="c1102-1745">Batch</span></span>

* <span data-ttu-id="c1102-1746">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1746">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="c1102-1747">クラウド</span><span class="sxs-lookup"><span data-stu-id="c1102-1747">Cloud</span></span>

* <span data-ttu-id="c1102-1748">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1748">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="c1102-1749">消費</span><span class="sxs-lookup"><span data-stu-id="c1102-1749">Consumption</span></span>

* <span data-ttu-id="c1102-1750">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1750">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="c1102-1751">Event Grid</span><span class="sxs-lookup"><span data-stu-id="c1102-1751">Event Grid</span></span>

* <span data-ttu-id="c1102-1752">[破壊的変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1752">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="c1102-1753">[破壊的変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1753">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="c1102-1754">[破壊的変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1754">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="c1102-1755">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="c1102-1755">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="c1102-1756">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1756">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="c1102-1757">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1757">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="c1102-1758">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1758">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="c1102-1759">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1759">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="c1102-1760">Interactive</span><span class="sxs-lookup"><span data-stu-id="c1102-1760">Interactive</span></span>

* <span data-ttu-id="c1102-1761">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1761">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="c1102-1762">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1762">Fixed errors on startup</span></span>
* <span data-ttu-id="c1102-1763">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1763">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="c1102-1764">IoT</span><span class="sxs-lookup"><span data-stu-id="c1102-1764">IoT</span></span>

* <span data-ttu-id="c1102-1765">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1765">Added support for device provisioning service</span></span>
* <span data-ttu-id="c1102-1766">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1766">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="c1102-1767">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1767">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-1768">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-1768">Monitor</span></span>

* <span data-ttu-id="c1102-1769">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1769">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="c1102-1770">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="c1102-1770">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="c1102-1771">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1771">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1772">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1772">Network</span></span>

* <span data-ttu-id="c1102-1773">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1773">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="c1102-1774">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1774">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="c1102-1775">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c1102-1775">Profile</span></span>

* <span data-ttu-id="c1102-1776">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1776">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="c1102-1777">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-1777">Role</span></span>

* <span data-ttu-id="c1102-1778">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1778">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="c1102-1779">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="c1102-1779">Service Fabric</span></span>

* <span data-ttu-id="c1102-1780">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1780">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="c1102-1781">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1781">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1782">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1782">VM</span></span>

* <span data-ttu-id="c1102-1783">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="c1102-1783">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="c1102-1784">[破壊的変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1784">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="c1102-1785">[破壊的変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1785">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="c1102-1786">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1786">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="c1102-1787">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1787">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="c1102-1788">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1788">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="c1102-1789">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1789">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="c1102-1790">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1790">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="c1102-1791">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1791">December 19, 2017</span></span>

<span data-ttu-id="c1102-1792">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="c1102-1792">Version 2.0.23</span></span>

* <span data-ttu-id="c1102-1793">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1793">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="c1102-1794">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-1794">Container</span></span>

* <span data-ttu-id="c1102-1795">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1795">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1796">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1796">Network</span></span>

* <span data-ttu-id="c1102-1797">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1797">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="c1102-1798">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1798">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1799">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1799">Storage</span></span>

* <span data-ttu-id="c1102-1800">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1800">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1801">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1801">VM</span></span>

* <span data-ttu-id="c1102-1802">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1802">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="c1102-1803">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1803">December 5, 2017</span></span>

<span data-ttu-id="c1102-1804">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="c1102-1804">Version 2.0.22</span></span>

* <span data-ttu-id="c1102-1805">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1805">Removed `az component` commands.</span></span> <span data-ttu-id="c1102-1806">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="c1102-1806">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="c1102-1807">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-1807">Core</span></span>
* <span data-ttu-id="c1102-1808">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1808">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="c1102-1809">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1809">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1810">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1810">ACS</span></span>

* <span data-ttu-id="c1102-1811">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1811">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="c1102-1812">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1812">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="c1102-1813">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1813">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="c1102-1814">Advisor</span><span class="sxs-lookup"><span data-stu-id="c1102-1814">Advisor</span></span>

* <span data-ttu-id="c1102-1815">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c1102-1815">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1816">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-1816">Appservice</span></span>

* <span data-ttu-id="c1102-1817">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1817">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="c1102-1818">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1818">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="c1102-1819">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1819">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="c1102-1820">消費</span><span class="sxs-lookup"><span data-stu-id="c1102-1820">Consumption</span></span>

* <span data-ttu-id="c1102-1821">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1821">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="c1102-1822">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-1822">Container</span></span>

* <span data-ttu-id="c1102-1823">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1823">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-1824">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-1824">Monitor</span></span>

* <span data-ttu-id="c1102-1825">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1825">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-1826">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-1826">Resource</span></span>

* <span data-ttu-id="c1102-1827">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1827">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="c1102-1828">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-1828">Role</span></span>

* <span data-ttu-id="c1102-1829">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1829">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="c1102-1830">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1830">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="c1102-1831">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1831">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-1832">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-1832">SQL</span></span>

* <span data-ttu-id="c1102-1833">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1833">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="c1102-1834">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1834">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1835">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1835">VM</span></span>

* <span data-ttu-id="c1102-1836">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1836">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="c1102-1837">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1837">November 14, 2017</span></span>

<span data-ttu-id="c1102-1838">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="c1102-1838">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-1839">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-1839">ACR</span></span>

* <span data-ttu-id="c1102-1840">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1840">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="c1102-1841">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1841">ACS</span></span>

* <span data-ttu-id="c1102-1842">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1842">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="c1102-1843">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-1843">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="c1102-1844">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1844">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="c1102-1845">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1845">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="c1102-1846">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1846">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1847">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-1847">Appservice</span></span>

* <span data-ttu-id="c1102-1848">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1848">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="c1102-1849">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1849">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="c1102-1850">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1850">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="c1102-1851">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1851">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="c1102-1852">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1852">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="c1102-1853">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="c1102-1853">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="c1102-1854">Batch</span><span class="sxs-lookup"><span data-stu-id="c1102-1854">Batch</span></span>

* <span data-ttu-id="c1102-1855">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1855">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="c1102-1856">Batchai</span><span class="sxs-lookup"><span data-stu-id="c1102-1856">Batchai</span></span>

* <span data-ttu-id="c1102-1857">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1857">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="c1102-1858">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1858">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="c1102-1859">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1859">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="c1102-1860">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1860">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="c1102-1861">クラウド</span><span class="sxs-lookup"><span data-stu-id="c1102-1861">Cloud</span></span>

* <span data-ttu-id="c1102-1862">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1862">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="c1102-1863">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-1863">Container</span></span>

* <span data-ttu-id="c1102-1864">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1864">Added support to open multiple ports</span></span>
* <span data-ttu-id="c1102-1865">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1865">Added container group restart policy</span></span>
* <span data-ttu-id="c1102-1866">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1866">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="c1102-1867">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1867">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="c1102-1868">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="c1102-1868">Data Lake Analytics</span></span>

* <span data-ttu-id="c1102-1869">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1869">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="c1102-1870">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="c1102-1870">Data Lake Store</span></span>

* <span data-ttu-id="c1102-1871">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1871">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="c1102-1872">拡張機能</span><span class="sxs-lookup"><span data-stu-id="c1102-1872">Extension</span></span>

* <span data-ttu-id="c1102-1873">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1873">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="c1102-1874">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1874">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="c1102-1875">IoT</span><span class="sxs-lookup"><span data-stu-id="c1102-1875">IoT</span></span>

* <span data-ttu-id="c1102-1876">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1876">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-1877">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-1877">Monitor</span></span>

* <span data-ttu-id="c1102-1878">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1878">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1879">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1879">Network</span></span>

* <span data-ttu-id="c1102-1880">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1880">Added support for CAA DNS records</span></span>
* <span data-ttu-id="c1102-1881">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1881">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="c1102-1882">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1882">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="c1102-1883">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1883">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="c1102-1884">Reservations</span><span class="sxs-lookup"><span data-stu-id="c1102-1884">Reservations</span></span>

* <span data-ttu-id="c1102-1885">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="c1102-1885">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-1886">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-1886">Resource</span></span>

* <span data-ttu-id="c1102-1887">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1887">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-1888">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-1888">SQL</span></span>

* <span data-ttu-id="c1102-1889">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1889">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1890">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1890">Storage</span></span>

* <span data-ttu-id="c1102-1891">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1891">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="c1102-1892">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1892">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="c1102-1893">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1893">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="c1102-1894">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1894">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="c1102-1895">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1895">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="c1102-1896">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1896">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="c1102-1897">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1897">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1898">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1898">VM</span></span>

* <span data-ttu-id="c1102-1899">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1899">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="c1102-1900">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1900">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="c1102-1901">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1901">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="c1102-1902">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1902">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="c1102-1903">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1903">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="c1102-1904">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1904">October 24, 2017</span></span>

<span data-ttu-id="c1102-1905">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="c1102-1905">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="c1102-1906">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-1906">Core</span></span>

* <span data-ttu-id="c1102-1907">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1907">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-1908">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-1908">ACR</span></span>

* <span data-ttu-id="c1102-1909">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1909">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="c1102-1910">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1910">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="c1102-1911">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1911">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1912">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1912">ACS</span></span>

* <span data-ttu-id="c1102-1913">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1913">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="c1102-1914">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1914">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1915">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-1915">Appservice</span></span>

* <span data-ttu-id="c1102-1916">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1916">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="c1102-1917">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="c1102-1917">Component</span></span>

* <span data-ttu-id="c1102-1918">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1918">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-1919">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-1919">Monitor</span></span>

* <span data-ttu-id="c1102-1920">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1920">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-1921">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-1921">Resource</span></span>

* <span data-ttu-id="c1102-1922">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1922">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="c1102-1923">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1923">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1924">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1924">VM</span></span>

* <span data-ttu-id="c1102-1925">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1925">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="c1102-1926">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1926">October 9, 2017</span></span>

<span data-ttu-id="c1102-1927">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="c1102-1927">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="c1102-1928">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-1928">Core</span></span>

* <span data-ttu-id="c1102-1929">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1929">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1930">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-1930">Appservice</span></span>

* <span data-ttu-id="c1102-1931">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1931">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="c1102-1932">Batch</span><span class="sxs-lookup"><span data-stu-id="c1102-1932">Batch</span></span>

* <span data-ttu-id="c1102-1933">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1933">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="c1102-1934">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1934">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="c1102-1935">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1935">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="c1102-1936">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1936">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="c1102-1937">Batchai</span><span class="sxs-lookup"><span data-stu-id="c1102-1937">Batchai</span></span>

* <span data-ttu-id="c1102-1938">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c1102-1938">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="c1102-1939">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1102-1939">Keyvault</span></span>

* <span data-ttu-id="c1102-1940">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1940">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="c1102-1941">(#4448)</span><span class="sxs-lookup"><span data-stu-id="c1102-1941">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="c1102-1942">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1942">Network</span></span>

* <span data-ttu-id="c1102-1943">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1943">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="c1102-1944">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1944">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-1945">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-1945">Resource</span></span>

* <span data-ttu-id="c1102-1946">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1946">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="c1102-1947">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1947">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="c1102-1948">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1948">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="c1102-1949">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1949">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-1950">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-1950">Sql</span></span>

* <span data-ttu-id="c1102-1951">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1951">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="c1102-1952">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1952">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="c1102-1953">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1953">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1954">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1954">Storage</span></span>

* <span data-ttu-id="c1102-1955">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1955">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1956">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1956">Vm</span></span>

* <span data-ttu-id="c1102-1957">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1957">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="c1102-1958">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1958">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="c1102-1959">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1959">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="c1102-1960">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1960">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="c1102-1961">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1961">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="c1102-1962">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="c1102-1962">September 22, 2017</span></span>

<span data-ttu-id="c1102-1963">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="c1102-1963">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-1964">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-1964">Resource</span></span>

* <span data-ttu-id="c1102-1965">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1965">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="c1102-1966">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1966">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="c1102-1967">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1967">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="c1102-1968">[破壊的変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1968">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="c1102-1969">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-1969">Network</span></span>

* <span data-ttu-id="c1102-1970">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1970">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="c1102-1971">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1971">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="c1102-1972">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1972">Added `asg` application security group commands</span></span>
* <span data-ttu-id="c1102-1973">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1973">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="c1102-1974">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1974">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="c1102-1975">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1975">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="c1102-1976">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1976">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-1977">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-1977">Storage</span></span>

* <span data-ttu-id="c1102-1978">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1978">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="c1102-1979">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="c1102-1979">Eventgrid</span></span>

* <span data-ttu-id="c1102-1980">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1980">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-1981">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-1981">SQL</span></span>

* <span data-ttu-id="c1102-1982">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-1982">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="c1102-1983">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="c1102-1983">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="c1102-1984">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1984">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="c1102-1985">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1102-1985">Keyvault</span></span>

* <span data-ttu-id="c1102-1986">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1986">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-1987">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-1987">VM</span></span>

* <span data-ttu-id="c1102-1988">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1988">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="c1102-1989">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1989">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="c1102-1990">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1990">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="c1102-1991">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1991">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="c1102-1992">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1992">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="c1102-1993">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1993">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-1994">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-1994">ACS</span></span>

* <span data-ttu-id="c1102-1995">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1995">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-1996">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-1996">Appservice</span></span>

* <span data-ttu-id="c1102-1997">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-1997">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="c1102-1998">バックアップ</span><span class="sxs-lookup"><span data-stu-id="c1102-1998">Backup</span></span>

* <span data-ttu-id="c1102-1999">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="c1102-1999">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="c1102-2000">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="c1102-2000">September 11, 2017</span></span>

<span data-ttu-id="c1102-2001">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="c1102-2001">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="c1102-2002">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-2002">Core</span></span>

* <span data-ttu-id="c1102-2003">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-2003">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="c1102-2004">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2004">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-2005">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-2005">Acs</span></span>

* <span data-ttu-id="c1102-2006">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2006">Added `acs list-locations` command</span></span>
* <span data-ttu-id="c1102-2007">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="c1102-2007">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-2008">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-2008">Appservice</span></span>

* <span data-ttu-id="c1102-2009">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2009">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="c1102-2010">CDN</span><span class="sxs-lookup"><span data-stu-id="c1102-2010">CDN</span></span>

* <span data-ttu-id="c1102-2011">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2011">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="c1102-2012">拡張機能</span><span class="sxs-lookup"><span data-stu-id="c1102-2012">Extension</span></span>

* <span data-ttu-id="c1102-2013">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c1102-2013">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="c1102-2014">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1102-2014">Keyvault</span></span>

* <span data-ttu-id="c1102-2015">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2015">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="c1102-2016">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-2016">Network</span></span>

* <span data-ttu-id="c1102-2017">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2017">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="c1102-2018">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2018">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="c1102-2019">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2019">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="c1102-2020">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2020">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="c1102-2021">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2021">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-2022">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-2022">Resource</span></span>

* <span data-ttu-id="c1102-2023">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="c1102-2023">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="c1102-2024">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="c1102-2024">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="c1102-2025">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="c1102-2025">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="c1102-2026">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="c1102-2026">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-2027">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-2027">SQL</span></span>

* <span data-ttu-id="c1102-2028">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2028">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-2029">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-2029">VM</span></span>

* <span data-ttu-id="c1102-2030">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="c1102-2030">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="c1102-2031">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="c1102-2031">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="c1102-2032">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2032">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="c1102-2033">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="c1102-2033">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="c1102-2034">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="c1102-2034">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="c1102-2035">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c1102-2035">August 31, 2017</span></span>

<span data-ttu-id="c1102-2036">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="c1102-2036">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="c1102-2037">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1102-2037">Keyvault</span></span>

* <span data-ttu-id="c1102-2038">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2038">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="c1102-2039">SF</span><span class="sxs-lookup"><span data-stu-id="c1102-2039">Sf</span></span>

* <span data-ttu-id="c1102-2040">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="c1102-2040">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-2041">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-2041">Storage</span></span>

* <span data-ttu-id="c1102-2042">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2042">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="c1102-2043">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="c1102-2043">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="c1102-2044">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="c1102-2044">August 28, 2017</span></span>

<span data-ttu-id="c1102-2045">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="c1102-2045">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="c1102-2046">CLI</span><span class="sxs-lookup"><span data-stu-id="c1102-2046">CLI</span></span>

* <span data-ttu-id="c1102-2047">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2047">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-2048">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-2048">ACS</span></span>

* <span data-ttu-id="c1102-2049">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2049">Corrected preview regions</span></span>
* <span data-ttu-id="c1102-2050">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-2050">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="c1102-2051">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2051">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-2052">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-2052">Appservice</span></span>

* <span data-ttu-id="c1102-2053">[破壊的変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2053">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="c1102-2054">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2054">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="c1102-2055">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2055">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="c1102-2056">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2056">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="c1102-2057">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="c1102-2057">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="c1102-2058">IoT</span><span class="sxs-lookup"><span data-stu-id="c1102-2058">IoT</span></span>

* <span data-ttu-id="c1102-2059">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2059">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="c1102-2060">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-2060">Network</span></span>

* <span data-ttu-id="c1102-2061">[破壊的変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2061">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="c1102-2062">[破壊的変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2062">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="c1102-2063">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2063">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="c1102-2064">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2064">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="c1102-2065">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2065">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="c1102-2066">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c1102-2066">Profile</span></span>

* <span data-ttu-id="c1102-2067">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2067">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="c1102-2068">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="c1102-2068">Service Fabric</span></span>

* <span data-ttu-id="c1102-2069">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="c1102-2069">Preview release</span></span>
* <span data-ttu-id="c1102-2070">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2070">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="c1102-2071">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2071">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="c1102-2072">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2072">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-2073">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-2073">Storage</span></span>

* <span data-ttu-id="c1102-2074">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-2074">Enabled setting blob tier</span></span>
* <span data-ttu-id="c1102-2075">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2075">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="c1102-2076">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2076">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="c1102-2077">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-2077">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="c1102-2078">[破壊的変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2078">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="c1102-2079">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="c1102-2079">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-2080">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-2080">VM</span></span>

* <span data-ttu-id="c1102-2081">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2081">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="c1102-2082">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-2082">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="c1102-2083">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2083">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="c1102-2084">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2084">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="c1102-2085">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2085">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="c1102-2086">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2086">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="c1102-2087">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="c1102-2087">August 15, 2017</span></span>

<span data-ttu-id="c1102-2088">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="c1102-2088">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-2089">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-2089">ACS</span></span>

* <span data-ttu-id="c1102-2090">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2090">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-2091">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-2091">Appservice</span></span>

* <span data-ttu-id="c1102-2092">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2092">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="c1102-2093">Event Grid</span><span class="sxs-lookup"><span data-stu-id="c1102-2093">Event Grid</span></span>

* <span data-ttu-id="c1102-2094">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2094">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="c1102-2095">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="c1102-2095">August 11, 2017</span></span>

<span data-ttu-id="c1102-2096">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="c1102-2096">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-2097">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-2097">ACS</span></span>

* <span data-ttu-id="c1102-2098">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2098">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="c1102-2099">Batch</span><span class="sxs-lookup"><span data-stu-id="c1102-2099">Batch</span></span>

* <span data-ttu-id="c1102-2100">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2100">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="c1102-2101">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2101">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="c1102-2102">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2102">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="c1102-2103">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2103">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="c1102-2104">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2104">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="c1102-2105">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2105">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="c1102-2106">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="c1102-2106">Component</span></span>

* <span data-ttu-id="c1102-2107">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2107">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="c1102-2108">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c1102-2108">Container</span></span>

* <span data-ttu-id="c1102-2109">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2109">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="c1102-2110">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="c1102-2110">Data Lake Store</span></span>

* <span data-ttu-id="c1102-2111">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-2111">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="c1102-2112">Event Grid</span><span class="sxs-lookup"><span data-stu-id="c1102-2112">Event Grid</span></span>

* <span data-ttu-id="c1102-2113">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c1102-2113">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="c1102-2114">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-2114">Network</span></span>

* <span data-ttu-id="c1102-2115">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2115">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="c1102-2116">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2116">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="c1102-2117">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2117">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="c1102-2118">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2118">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="c1102-2119">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c1102-2119">Profile</span></span>

* <span data-ttu-id="c1102-2120">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2120">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-2121">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-2121">Storage</span></span>

* <span data-ttu-id="c1102-2122">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="c1102-2122">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-2123">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-2123">VM</span></span>

* <span data-ttu-id="c1102-2124">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2124">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="c1102-2125">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2125">Exposed `list-skus` command</span></span>
* <span data-ttu-id="c1102-2126">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2126">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="c1102-2127">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="c1102-2127">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="c1102-2128">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2128">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="c1102-2129">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="c1102-2129">July 28, 2017</span></span>

<span data-ttu-id="c1102-2130">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="c1102-2130">Version 2.0.12</span></span>

* <span data-ttu-id="c1102-2131">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2131">Added container commands</span></span>
* <span data-ttu-id="c1102-2132">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2132">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="c1102-2133">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-2133">Core</span></span>

* <span data-ttu-id="c1102-2134">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="c1102-2134">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="c1102-2135">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2135">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="c1102-2136">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="c1102-2136">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="c1102-2137">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="c1102-2137">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="c1102-2138">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="c1102-2138">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="c1102-2139">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="c1102-2139">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="c1102-2140">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="c1102-2140">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="c1102-2141">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="c1102-2141">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="c1102-2142">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="c1102-2142">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="c1102-2143">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="c1102-2143">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="c1102-2144">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="c1102-2144">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="c1102-2145">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="c1102-2145">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="c1102-2146">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2146">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="c1102-2147">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2147">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="c1102-2148">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2148">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="c1102-2149">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="c1102-2149">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="c1102-2150">ACR</span><span class="sxs-lookup"><span data-stu-id="c1102-2150">ACR</span></span>

* <span data-ttu-id="c1102-2151">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2151">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="c1102-2152">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2152">Support SKU update for managed registries</span></span>
* <span data-ttu-id="c1102-2153">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2153">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="c1102-2154">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2154">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="c1102-2155">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2155">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="c1102-2156">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2156">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-2157">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-2157">ACS</span></span>

* <span data-ttu-id="c1102-2158">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2158">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-2159">Appservice</span><span class="sxs-lookup"><span data-stu-id="c1102-2159">Appservice</span></span>

* <span data-ttu-id="c1102-2160">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2160">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="c1102-2161">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2161">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="c1102-2162">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="c1102-2162">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="c1102-2163">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="c1102-2163">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="c1102-2164">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="c1102-2164">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="c1102-2165">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="c1102-2165">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="c1102-2166">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="c1102-2166">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="c1102-2167">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="c1102-2167">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="c1102-2168">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-2168">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="c1102-2169">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="c1102-2169">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="c1102-2170">Batch</span><span class="sxs-lookup"><span data-stu-id="c1102-2170">Batch</span></span>

* <span data-ttu-id="c1102-2171">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="c1102-2171">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="c1102-2172">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2172">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="c1102-2173">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2173">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="c1102-2174">CDN</span><span class="sxs-lookup"><span data-stu-id="c1102-2174">CDN</span></span>

* <span data-ttu-id="c1102-2175">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2175">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="c1102-2176">クラウド</span><span class="sxs-lookup"><span data-stu-id="c1102-2176">Cloud</span></span>

* <span data-ttu-id="c1102-2177">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2177">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="c1102-2178">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="c1102-2178">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="c1102-2179">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2179">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="c1102-2180">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2180">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="c1102-2181">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2181">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="c1102-2182">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="c1102-2182">CosmosDB</span></span>

* <span data-ttu-id="c1102-2183">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2183">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="c1102-2184">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2184">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="c1102-2185">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="c1102-2185">Data Lake Analytics</span></span>

* <span data-ttu-id="c1102-2186">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2186">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="c1102-2187">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2187">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="c1102-2188">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2188">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="c1102-2189">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="c1102-2189">Data Lake Store</span></span>

* <span data-ttu-id="c1102-2190">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2190">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="c1102-2191">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2191">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="c1102-2192">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-2192">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="c1102-2193">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="c1102-2193">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="c1102-2194">対話</span><span class="sxs-lookup"><span data-stu-id="c1102-2194">Interactive</span></span>

* <span data-ttu-id="c1102-2195">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2195">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="c1102-2196">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="c1102-2196">Increased test coverage</span></span>
* <span data-ttu-id="c1102-2197">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2197">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="c1102-2198">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="c1102-2198">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="c1102-2199">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="c1102-2199">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="c1102-2200">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="c1102-2200">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="c1102-2201">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="c1102-2201">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="c1102-2202">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2202">Added `--progress` flag</span></span>
* <span data-ttu-id="c1102-2203">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2203">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="c1102-2204">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="c1102-2204">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="c1102-2205">IoT</span><span class="sxs-lookup"><span data-stu-id="c1102-2205">IoT</span></span>

* <span data-ttu-id="c1102-2206">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-2206">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="c1102-2207">(#3934)</span><span class="sxs-lookup"><span data-stu-id="c1102-2207">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="c1102-2208">Key Vault</span><span class="sxs-lookup"><span data-stu-id="c1102-2208">Key vault</span></span>

* <span data-ttu-id="c1102-2209">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-2209">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="c1102-2210">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="c1102-2210">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="c1102-2211">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="c1102-2211">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="c1102-2212">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="c1102-2212">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="c1102-2213">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="c1102-2213">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="c1102-2214">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="c1102-2214">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="c1102-2215">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-2215">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="c1102-2216">(#3307)</span><span class="sxs-lookup"><span data-stu-id="c1102-2216">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="c1102-2217">ラボ</span><span class="sxs-lookup"><span data-stu-id="c1102-2217">Lab</span></span>

* <span data-ttu-id="c1102-2218">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2218">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="c1102-2219">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2219">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-2220">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-2220">Monitor</span></span>

* <span data-ttu-id="c1102-2221">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="c1102-2221">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="c1102-2222">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2222">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="c1102-2223">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2223">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="c1102-2224">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2224">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="c1102-2225">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2225">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="c1102-2226">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="c1102-2226">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="c1102-2227">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2227">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="c1102-2228">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="c1102-2228">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="c1102-2229">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2229">`location` no longer required</span></span>
  * <span data-ttu-id="c1102-2230">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="c1102-2230">Add name and ID support for target</span></span>
  * <span data-ttu-id="c1102-2231">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="c1102-2231">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="c1102-2232">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-2232">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="c1102-2233">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2233">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="c1102-2234">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="c1102-2234">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="c1102-2235">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2235">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="c1102-2236">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2236">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="c1102-2237">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-2237">Network</span></span>

* <span data-ttu-id="c1102-2238">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2238">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="c1102-2239">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2239">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="c1102-2240">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2240">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="c1102-2241">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2241">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="c1102-2242">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2242">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="c1102-2243">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2243">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="c1102-2244">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2244">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="c1102-2245">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2245">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="c1102-2246">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2246">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="c1102-2247">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2247">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="c1102-2248">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2248">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="c1102-2249">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2249">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="c1102-2250">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2250">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="c1102-2251">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2251">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="c1102-2252">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2252">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="c1102-2253">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2253">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="c1102-2254">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2254">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="c1102-2255">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2255">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="c1102-2256">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2256">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="c1102-2257">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2257">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="c1102-2258">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2258">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="c1102-2259">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2259">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="c1102-2260">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2260">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="c1102-2261">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="c1102-2261">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="c1102-2262">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="c1102-2262">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="c1102-2263">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="c1102-2263">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="c1102-2264">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="c1102-2264">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="c1102-2265">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c1102-2265">Profile</span></span>

* <span data-ttu-id="c1102-2266">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2266">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="c1102-2267">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2267">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="c1102-2268">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="c1102-2268">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="c1102-2269">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2269">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="c1102-2270">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2270">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="c1102-2271">RDBMS</span><span class="sxs-lookup"><span data-stu-id="c1102-2271">RDBMS</span></span>

* <span data-ttu-id="c1102-2272">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="c1102-2272">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="c1102-2273">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="c1102-2273">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="c1102-2274">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="c1102-2274">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="c1102-2275">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="c1102-2275">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-2276">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-2276">Resource</span></span>

* <span data-ttu-id="c1102-2277">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2277">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="c1102-2278">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2278">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="c1102-2279">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2279">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="c1102-2280">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2280">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="c1102-2281">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="c1102-2281">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="c1102-2282">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2282">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="c1102-2283">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="c1102-2283">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="c1102-2284">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2284">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="c1102-2285">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-2285">Role</span></span>

* <span data-ttu-id="c1102-2286">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2286">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="c1102-2287">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="c1102-2287">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="c1102-2288">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="c1102-2288">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="c1102-2289">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="c1102-2289">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="c1102-2290">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2290">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="c1102-2291">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="c1102-2291">Service Fabric</span></span>
* <span data-ttu-id="c1102-2292">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="c1102-2292">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="c1102-2293">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="c1102-2293">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="c1102-2294">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="c1102-2294">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-2295">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-2295">SQL</span></span>

* <span data-ttu-id="c1102-2296">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2296">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="c1102-2297">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2297">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="c1102-2298">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2298">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-2299">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-2299">Storage</span></span>

* <span data-ttu-id="c1102-2300">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="c1102-2300">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="c1102-2301">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-2301">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="c1102-2302">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="c1102-2302">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="c1102-2303">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="c1102-2303">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="c1102-2304">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="c1102-2304">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="c1102-2305">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="c1102-2305">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-2306">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-2306">VM</span></span>

* <span data-ttu-id="c1102-2307">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2307">Support configuring nsg</span></span>
* <span data-ttu-id="c1102-2308">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2308">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="c1102-2309">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="c1102-2309">Support managed service identities</span></span>
* <span data-ttu-id="c1102-2310">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2310">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="c1102-2311">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="c1102-2311">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="c1102-2312">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="c1102-2312">May 10, 2017</span></span>

<span data-ttu-id="c1102-2313">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="c1102-2313">Version 2.0.6</span></span>

* <span data-ttu-id="c1102-2314">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2314">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="c1102-2315">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2315">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="c1102-2316">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2316">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="c1102-2317">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2317">Include Cognitive Services module</span></span>
* <span data-ttu-id="c1102-2318">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2318">Include Service Fabric module</span></span>
* <span data-ttu-id="c1102-2319">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="c1102-2319">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="c1102-2320">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2320">Add support for CDN commands</span></span>
* <span data-ttu-id="c1102-2321">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2321">Remove Container module</span></span>
* <span data-ttu-id="c1102-2322">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="c1102-2322">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="c1102-2323">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="c1102-2323">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="c1102-2324">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-2324">Core</span></span>

* <span data-ttu-id="c1102-2325">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="c1102-2325">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="c1102-2326">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="c1102-2326">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="c1102-2327">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="c1102-2327">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="c1102-2328">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="c1102-2328">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="c1102-2329">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="c1102-2329">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="c1102-2330">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="c1102-2330">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="c1102-2331">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="c1102-2331">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="c1102-2332">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="c1102-2332">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="c1102-2333">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="c1102-2333">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="c1102-2334">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="c1102-2334">core: Improved performance</span></span>
* <span data-ttu-id="c1102-2335">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="c1102-2335">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="c1102-2336">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="c1102-2336">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-2337">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-2337">ACS</span></span>

* <span data-ttu-id="c1102-2338">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2338">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="c1102-2339">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2339">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="c1102-2340">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2340">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="c1102-2341">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="c1102-2341">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-2342">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-2342">AppService</span></span>

* <span data-ttu-id="c1102-2343">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2343">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="c1102-2344">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2344">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="c1102-2345">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="c1102-2345">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="c1102-2346">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2346">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="c1102-2347">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2347">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="c1102-2348">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="c1102-2348">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="c1102-2349">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="c1102-2349">support slot swap with preview</span></span>
* <span data-ttu-id="c1102-2350">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="c1102-2350">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="c1102-2351">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="c1102-2351">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="c1102-2352">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="c1102-2352">CosmosDB</span></span>

* <span data-ttu-id="c1102-2353">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2353">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="c1102-2354">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2354">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="c1102-2355">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2355">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="c1102-2356">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2356">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="c1102-2357">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="c1102-2357">Data Lake Analytics</span></span>

* <span data-ttu-id="c1102-2358">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2358">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="c1102-2359">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="c1102-2359">Add support for new catalog item type: package.</span></span> <span data-ttu-id="c1102-2360">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="c1102-2360">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="c1102-2361">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="c1102-2361">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="c1102-2362">テーブル</span><span class="sxs-lookup"><span data-stu-id="c1102-2362">Table</span></span>
  * <span data-ttu-id="c1102-2363">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="c1102-2363">Table valued function</span></span>
  * <span data-ttu-id="c1102-2364">表示</span><span class="sxs-lookup"><span data-stu-id="c1102-2364">View</span></span>
  * <span data-ttu-id="c1102-2365">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="c1102-2365">Table Statistics.</span></span> <span data-ttu-id="c1102-2366">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="c1102-2366">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="c1102-2367">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="c1102-2367">Data Lake Store</span></span>

* <span data-ttu-id="c1102-2368">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2368">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="c1102-2369">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="c1102-2369">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="c1102-2370">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="c1102-2370">missed help for access show.</span></span> <span data-ttu-id="c1102-2371">追加しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2371">adding it.</span></span> <span data-ttu-id="c1102-2372">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="c1102-2372">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="c1102-2373">検索</span><span class="sxs-lookup"><span data-stu-id="c1102-2373">Find</span></span>

* <span data-ttu-id="c1102-2374">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="c1102-2374">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="c1102-2375">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c1102-2375">KeyVault</span></span>

* <span data-ttu-id="c1102-2376">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2376">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="c1102-2377">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2377">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="c1102-2378">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="c1102-2378">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="c1102-2379">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2379">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="c1102-2380">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="c1102-2380">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="c1102-2381">ラボ</span><span class="sxs-lookup"><span data-stu-id="c1102-2381">Lab</span></span>

* <span data-ttu-id="c1102-2382">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2382">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="c1102-2383">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2383">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="c1102-2384">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2384">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="c1102-2385">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2385">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="c1102-2386">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2386">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="c1102-2387">監視</span><span class="sxs-lookup"><span data-stu-id="c1102-2387">Monitor</span></span>

* <span data-ttu-id="c1102-2388">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="c1102-2388">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="c1102-2389">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="c1102-2389">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="c1102-2390">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-2390">Network</span></span>

* <span data-ttu-id="c1102-2391">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2391">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="c1102-2392">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2392">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="c1102-2393">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2393">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="c1102-2394">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2394">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="c1102-2395">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2395">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="c1102-2396">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2396">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="c1102-2397">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2397">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="c1102-2398">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2398">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="c1102-2399">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2399">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="c1102-2400">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2400">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="c1102-2401">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2401">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="c1102-2402">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2402">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="c1102-2403">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2403">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="c1102-2404">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2404">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="c1102-2405">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="c1102-2405">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="c1102-2406">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2406">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="c1102-2407">プロファイル</span><span class="sxs-lookup"><span data-stu-id="c1102-2407">Profile</span></span>

* <span data-ttu-id="c1102-2408">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="c1102-2408">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="c1102-2409">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="c1102-2409">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="c1102-2410">Redis</span><span class="sxs-lookup"><span data-stu-id="c1102-2410">Redis</span></span>

* <span data-ttu-id="c1102-2411">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2411">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="c1102-2412">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2412">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="c1102-2413">Resource</span><span class="sxs-lookup"><span data-stu-id="c1102-2413">Resource</span></span>

* <span data-ttu-id="c1102-2414">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="c1102-2414">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="c1102-2415">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="c1102-2415">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="c1102-2416">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="c1102-2416">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="c1102-2417">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2417">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="c1102-2418">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="c1102-2418">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="c1102-2419">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2419">Add docs for az lock update.</span></span> <span data-ttu-id="c1102-2420">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="c1102-2420">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="c1102-2421">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="c1102-2421">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="c1102-2422">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="c1102-2422">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="c1102-2423">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="c1102-2423">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="c1102-2424">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="c1102-2424">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="c1102-2425">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="c1102-2425">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="c1102-2426">Role</span><span class="sxs-lookup"><span data-stu-id="c1102-2426">Role</span></span>

* <span data-ttu-id="c1102-2427">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="c1102-2427">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="c1102-2428">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="c1102-2428">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="c1102-2429">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="c1102-2429">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="c1102-2430">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="c1102-2430">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="c1102-2431">SQL</span><span class="sxs-lookup"><span data-stu-id="c1102-2431">SQL</span></span>

* <span data-ttu-id="c1102-2432">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="c1102-2432">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="c1102-2433">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="c1102-2433">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="c1102-2434">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-2434">Storage</span></span>

* <span data-ttu-id="c1102-2435">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="c1102-2435">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="c1102-2436">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2436">Add support for incremental blob copy</span></span>
* <span data-ttu-id="c1102-2437">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2437">Add support for large block blob upload</span></span>
* <span data-ttu-id="c1102-2438">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="c1102-2438">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-2439">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-2439">VM</span></span>

* <span data-ttu-id="c1102-2440">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="c1102-2440">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="c1102-2441">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="c1102-2441">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="c1102-2442">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="c1102-2442">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="c1102-2443">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="c1102-2443">az vm/vmss disk</span></span>
  3. <span data-ttu-id="c1102-2444">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="c1102-2444">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="c1102-2445">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="c1102-2445">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="c1102-2446">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="c1102-2446">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="c1102-2447">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="c1102-2447">April 3, 2017</span></span>

<span data-ttu-id="c1102-2448">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="c1102-2448">Version 2.0.2</span></span>

<span data-ttu-id="c1102-2449">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="c1102-2449">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="c1102-2450">コア</span><span class="sxs-lookup"><span data-stu-id="c1102-2450">Core</span></span>

* <span data-ttu-id="c1102-2451">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="c1102-2451">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="c1102-2452">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="c1102-2452">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="c1102-2453">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="c1102-2453">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="c1102-2454">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="c1102-2454">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="c1102-2455">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="c1102-2455">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="c1102-2456">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="c1102-2456">Add prompting for missing template parameters.</span></span> <span data-ttu-id="c1102-2457">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="c1102-2457">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="c1102-2458">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="c1102-2458">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="c1102-2459">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="c1102-2459">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="c1102-2460">ACS</span><span class="sxs-lookup"><span data-stu-id="c1102-2460">ACS</span></span>

* <span data-ttu-id="c1102-2461">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="c1102-2461">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="c1102-2462">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="c1102-2462">Add support for ssh key password prompting.</span></span> <span data-ttu-id="c1102-2463">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="c1102-2463">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="c1102-2464">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="c1102-2464">Add support for windows clusters.</span></span> <span data-ttu-id="c1102-2465">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="c1102-2465">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="c1102-2466">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="c1102-2466">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="c1102-2467">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="c1102-2467">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="c1102-2468">AppService</span><span class="sxs-lookup"><span data-stu-id="c1102-2468">AppService</span></span>

* <span data-ttu-id="c1102-2469">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="c1102-2469">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="c1102-2470">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="c1102-2470">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="c1102-2471">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="c1102-2471">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="c1102-2472">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="c1102-2472">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="c1102-2473">DataLake</span><span class="sxs-lookup"><span data-stu-id="c1102-2473">DataLake</span></span>

* <span data-ttu-id="c1102-2474">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c1102-2474">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="c1102-2475">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="c1102-2475">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="c1102-2476">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="c1102-2476">DocuemntDB</span></span>

* <span data-ttu-id="c1102-2477">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="c1102-2477">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="c1102-2478">VM</span><span class="sxs-lookup"><span data-stu-id="c1102-2478">VM</span></span>

* <span data-ttu-id="c1102-2479">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="c1102-2479">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="c1102-2480">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="c1102-2480">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="c1102-2481">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="c1102-2481">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="c1102-2482">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="c1102-2482">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="c1102-2483">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="c1102-2483">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="c1102-2484">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="c1102-2484">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="c1102-2485">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="c1102-2485">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="c1102-2486">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="c1102-2486">February 27, 2017</span></span>

<span data-ttu-id="c1102-2487">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="c1102-2487">Version 2.0.0</span></span>

<span data-ttu-id="c1102-2488">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="c1102-2488">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="c1102-2489">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="c1102-2489">Container Service (acs)</span></span>
- <span data-ttu-id="c1102-2490">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="c1102-2490">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="c1102-2491">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="c1102-2491">Networking</span></span>
- <span data-ttu-id="c1102-2492">Storage</span><span class="sxs-lookup"><span data-stu-id="c1102-2492">Storage</span></span>

<span data-ttu-id="c1102-2493">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="c1102-2493">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="c1102-2494">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="c1102-2494">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="c1102-2495">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="c1102-2495">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="c1102-2496">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="c1102-2496">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="c1102-2497">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="c1102-2497">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="c1102-2498">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="c1102-2498">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="c1102-2499">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="c1102-2499">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="c1102-2500">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="c1102-2500">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="c1102-2501">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="c1102-2501">Provide feedback from the command line with the `az feedback` command</span></span>

