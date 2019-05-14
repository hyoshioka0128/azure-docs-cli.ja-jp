---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/06/2019
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: ce11abccc23ee1f150916ef2f91dc895d4664d31
ms.sourcegitcommit: 65bf8561a6e047e4eab52186e066a2e8c21f1d40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "65240507"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="95764-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="95764-103">Azure CLI release notes</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="95764-104">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="95764-104">May 6, 2019</span></span>

<span data-ttu-id="95764-105">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="95764-105">Version 2.0.64</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-106">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-106">Appservice</span></span>
* <span data-ttu-id="95764-107">`functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-107">Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="95764-108">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-108">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="95764-109">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="95764-109">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="95764-110">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-110">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="95764-111">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-111">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="95764-112">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-112">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="95764-113">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-113">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="95764-114">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-114">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="95764-115">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-115">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="95764-116">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-116">Added `create-remote-connection` command</span></span>

### <a name="role"></a><span data-ttu-id="95764-117">Role</span><span class="sxs-lookup"><span data-stu-id="95764-117">Role</span></span>
* <span data-ttu-id="95764-118">[非推奨] `create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="95764-118">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="95764-119">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="95764-119">April 23, 2019</span></span>

<span data-ttu-id="95764-120">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="95764-120">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="95764-121">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-121">ACS</span></span>
* <span data-ttu-id="95764-122">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-122">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="95764-123">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-123">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="95764-124">AMS</span><span class="sxs-lookup"><span data-stu-id="95764-124">AMS</span></span>
* <span data-ttu-id="95764-125">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-125">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-126">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-126">AppService</span></span>
* <span data-ttu-id="95764-127">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-127">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="95764-128">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-128">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="95764-129">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-129">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="95764-130">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-130">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="95764-131">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-131">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="95764-132">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-132">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="95764-133">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-133">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="95764-134">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-134">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="95764-135">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-135">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="95764-136">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="95764-136">Deployment Manager</span></span>
* <span data-ttu-id="95764-137">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="95764-137">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="95764-138">ラボ</span><span class="sxs-lookup"><span data-stu-id="95764-138">Lab</span></span>
* <span data-ttu-id="95764-139">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-139">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="95764-140">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-140">Network</span></span>
* <span data-ttu-id="95764-141">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-141">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="95764-142">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-142">Resource</span></span>
* <span data-ttu-id="95764-143">[非推奨] `resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="95764-143">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="95764-144">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="95764-144">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="95764-145">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-145">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="95764-146">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-146">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="95764-147">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-147">SQL</span></span>
* <span data-ttu-id="95764-148">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-148">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="95764-149">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-149">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="95764-150">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-150">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="95764-151">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-151">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="95764-152">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-152">Storage</span></span>
* <span data-ttu-id="95764-153">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-153">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="95764-154">VM</span><span class="sxs-lookup"><span data-stu-id="95764-154">VM</span></span>
* <span data-ttu-id="95764-155">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-155">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="95764-156">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-156">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="95764-157">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-157">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="95764-158">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="95764-158">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="95764-159">コア</span><span class="sxs-lookup"><span data-stu-id="95764-159">Core</span></span>
* <span data-ttu-id="95764-160">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-160">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="95764-161">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-161">ACR</span></span>
* <span data-ttu-id="95764-162">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-162">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="95764-163">AMS</span><span class="sxs-lookup"><span data-stu-id="95764-163">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="95764-166">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-166">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="95764-167">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-167">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-168">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-168">AppService</span></span>
* <span data-ttu-id="95764-169">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-169">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="95764-170">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-170">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="95764-171">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-171">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="95764-172">[破壊的変更] `devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="95764-172">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="95764-173">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-173">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="95764-174">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-174">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="95764-175">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-175">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="95764-176">CDN</span><span class="sxs-lookup"><span data-stu-id="95764-176">CDN</span></span>
* <span data-ttu-id="95764-177">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-177">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="95764-178">フィードバック</span><span class="sxs-lookup"><span data-stu-id="95764-178">Feedback</span></span>
* <span data-ttu-id="95764-179">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-179">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="95764-180">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-180">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="95764-181">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-181">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-182">監視</span><span class="sxs-lookup"><span data-stu-id="95764-182">Monitor</span></span>
* <span data-ttu-id="95764-183">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-183">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="95764-184">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-184">Network</span></span>
* <span data-ttu-id="95764-185">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-185">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="95764-186">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-186">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="95764-187">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-187">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="95764-188">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-188">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="95764-189">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="95764-189">PrivateDNS</span></span>
* <span data-ttu-id="95764-190">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-190">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="95764-191">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-191">Resource</span></span>
* <span data-ttu-id="95764-192">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-192">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="95764-193">Role</span><span class="sxs-lookup"><span data-stu-id="95764-193">Role</span></span>
* <span data-ttu-id="95764-194">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-194">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="95764-195">[破壊的変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-195">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="95764-196">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-196">SQL</span></span>
* <span data-ttu-id="95764-197">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-197">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="95764-198">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-198">Storage</span></span>
* <span data-ttu-id="95764-199">[破壊的変更] `storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-199">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="95764-200">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-200">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="95764-201">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-201">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="95764-202">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-202">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="95764-203">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="95764-203">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="95764-204">コア</span><span class="sxs-lookup"><span data-stu-id="95764-204">Core</span></span>
* <span data-ttu-id="95764-205">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-205">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="95764-206">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-206">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="95764-207">クラウド</span><span class="sxs-lookup"><span data-stu-id="95764-207">Cloud</span></span>
* <span data-ttu-id="95764-208">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-208">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="95764-209">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-209">ACR</span></span>
* <span data-ttu-id="95764-210">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-210">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="95764-211">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-211">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="95764-212">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-212">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="95764-213">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-213">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-214">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-214">AppService</span></span>
* <span data-ttu-id="95764-215">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-215">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="95764-216">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-216">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="95764-217">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="95764-217">BOT Service</span></span>
* <span data-ttu-id="95764-218">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-218">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="95764-219">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-219">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="95764-220">[破壊的変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-220">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="95764-221">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-221">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="95764-222">CDN</span><span class="sxs-lookup"><span data-stu-id="95764-222">CDN</span></span>
* <span data-ttu-id="95764-223">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-223">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [破壊的変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="95764-225">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="95764-225">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="95764-226">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-226">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="95764-227">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="95764-227">Cosmosdb</span></span>
* <span data-ttu-id="95764-228">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-228">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="95764-229">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-229">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="95764-230">Interactive</span><span class="sxs-lookup"><span data-stu-id="95764-230">Interactive</span></span>
* <span data-ttu-id="95764-231">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-231">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-232">監視</span><span class="sxs-lookup"><span data-stu-id="95764-232">Monitor</span></span>
* <span data-ttu-id="95764-233">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-233">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="95764-234">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-234">Network</span></span>
* <span data-ttu-id="95764-235">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-235">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="95764-236">プロファイル</span><span class="sxs-lookup"><span data-stu-id="95764-236">Profile</span></span>
* <span data-ttu-id="95764-237">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-237">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="95764-238">Postgres</span><span class="sxs-lookup"><span data-stu-id="95764-238">Postgres</span></span> 
* <span data-ttu-id="95764-239">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-239">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="95764-240">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="95764-240">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="95764-241">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-241">Resource</span></span>
* <span data-ttu-id="95764-242">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="95764-242">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="95764-243">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-243">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="95764-244">Graph</span><span class="sxs-lookup"><span data-stu-id="95764-244">Graph</span></span>
* <span data-ttu-id="95764-245">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-245">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="95764-246">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-246">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="95764-247">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-247">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="95764-248">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-248">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="95764-249">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-249">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="95764-250">storage</span><span class="sxs-lookup"><span data-stu-id="95764-250">storage</span></span>
* <span data-ttu-id="95764-251">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-251">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="95764-252">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-252">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="95764-253">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-253">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="95764-254">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-254">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="95764-255">VM</span><span class="sxs-lookup"><span data-stu-id="95764-255">VM</span></span>
* <span data-ttu-id="95764-256">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-256">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="95764-257">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="95764-257">March 12, 2019</span></span>

<span data-ttu-id="95764-258">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="95764-258">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="95764-259">コア</span><span class="sxs-lookup"><span data-stu-id="95764-259">Core</span></span>

* <span data-ttu-id="95764-260">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-260">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="95764-261">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-261">ACR</span></span>

* <span data-ttu-id="95764-262">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-262">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="95764-263">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-263">ACS</span></span>

* <span data-ttu-id="95764-264">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-264">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="95764-265">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-265">AppService</span></span>

* <span data-ttu-id="95764-266">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-266">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="95764-267">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-267">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="95764-268">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-268">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="95764-269">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-269">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="95764-270">Botservice</span><span class="sxs-lookup"><span data-stu-id="95764-270">Botservice</span></span>

* <span data-ttu-id="95764-271">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-271">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="95764-272">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-272">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="95764-273">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-273">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="95764-274">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-274">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="95764-275">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-275">Container</span></span>

* <span data-ttu-id="95764-276">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-276">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="95764-277">EventHub</span><span class="sxs-lookup"><span data-stu-id="95764-277">EventHub</span></span>

* <span data-ttu-id="95764-278">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-278">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="95764-279">Find</span><span class="sxs-lookup"><span data-stu-id="95764-279">Find</span></span>

* <span data-ttu-id="95764-280">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="95764-280">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="95764-281">HDInsight</span><span class="sxs-lookup"><span data-stu-id="95764-281">HDInsight</span></span>

* <span data-ttu-id="95764-282">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-282">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="95764-283">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-283">Network</span></span>

* <span data-ttu-id="95764-284">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-284">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="95764-285">Rdbms</span><span class="sxs-lookup"><span data-stu-id="95764-285">Rdbms</span></span>

* <span data-ttu-id="95764-286">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="95764-286">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="95764-287">Role</span><span class="sxs-lookup"><span data-stu-id="95764-287">Role</span></span>

* <span data-ttu-id="95764-288">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-288">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="95764-289">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-289">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="95764-290">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="95764-290">Service Fabric</span></span>

* <span data-ttu-id="95764-291">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-291">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="95764-292">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="95764-292">February 26, 2019</span></span>

<span data-ttu-id="95764-293">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="95764-293">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="95764-294">コア</span><span class="sxs-lookup"><span data-stu-id="95764-294">Core</span></span>

* <span data-ttu-id="95764-295">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-295">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="95764-296">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-296">ACR</span></span>

* <span data-ttu-id="95764-297">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-297">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="95764-298">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-298">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="95764-299">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-299">ACS</span></span>

* <span data-ttu-id="95764-300">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-300">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-301">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-301">AppService</span></span>

* <span data-ttu-id="95764-302">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-302">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="95764-303">Batch</span><span class="sxs-lookup"><span data-stu-id="95764-303">Batch</span></span>
* <span data-ttu-id="95764-304">[破壊的変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-304">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="95764-305">[破壊的変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-305">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="95764-306">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-306">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="95764-307">[破壊的変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-307">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="95764-308">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-308">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="95764-309">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="95764-309">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="95764-310">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="95764-310">CosmosDB</span></span>

* <span data-ttu-id="95764-311">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-311">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="95764-312">Kusto</span><span class="sxs-lookup"><span data-stu-id="95764-312">Kusto</span></span>

* <span data-ttu-id="95764-313">[破壊的変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-313">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="95764-314">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-314">Network</span></span>

* <span data-ttu-id="95764-315">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-315">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="95764-316">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-316">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="95764-317">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-317">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="95764-318">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-318">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="95764-319">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-319">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="95764-320">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-320">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="95764-321">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-321">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="95764-322">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-322">Resource</span></span>

* <span data-ttu-id="95764-323">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-323">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="95764-324">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-324">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="95764-325">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-325">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="95764-326">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-326">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="95764-327">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-327">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="95764-328">Role</span><span class="sxs-lookup"><span data-stu-id="95764-328">Role</span></span>

* <span data-ttu-id="95764-329">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-329">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="95764-330">VM</span><span class="sxs-lookup"><span data-stu-id="95764-330">VM</span></span>

* <span data-ttu-id="95764-331">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-331">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="95764-332">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="95764-332">February 12, 2019</span></span>

<span data-ttu-id="95764-333">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="95764-333">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="95764-334">コア</span><span class="sxs-lookup"><span data-stu-id="95764-334">Core</span></span>

* <span data-ttu-id="95764-335">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-335">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="95764-336">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-336">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="95764-337">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-337">ACR</span></span>
* <span data-ttu-id="95764-338">[破壊的変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-338">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="95764-339">[破壊的変更] `acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-339">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="95764-340">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-340">ACS</span></span>
* <span data-ttu-id="95764-341">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-341">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="95764-342">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-342">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="95764-343">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-343">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="95764-344">AMS</span><span class="sxs-lookup"><span data-stu-id="95764-344">AMS</span></span>
* <span data-ttu-id="95764-345">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-345">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="95764-346">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-346">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-347">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-347">Appservice</span></span>
* <span data-ttu-id="95764-348">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-348">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="95764-349">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-349">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="95764-350">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="95764-350">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="95764-351">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-351">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="95764-352">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-352">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="95764-353">Botservice</span><span class="sxs-lookup"><span data-stu-id="95764-353">Botservice</span></span>
* <span data-ttu-id="95764-354">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="95764-354">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="95764-355">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-355">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="95764-356">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-356">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="95764-357">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-357">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="95764-358">[非推奨] `--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-358">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="95764-359">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-359">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="95764-360">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-360">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="95764-361">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-361">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="95764-362">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="95764-362">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="95764-363">8.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-363">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="95764-364">Key Vault</span><span class="sxs-lookup"><span data-stu-id="95764-364">Key Vault</span></span>
* <span data-ttu-id="95764-365">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-365">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-366">監視</span><span class="sxs-lookup"><span data-stu-id="95764-366">Monitor</span></span>
* <span data-ttu-id="95764-367">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-367">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="95764-368">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-368">Network</span></span>
* <span data-ttu-id="95764-369">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-369">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="95764-370">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-370">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="95764-371">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-371">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="95764-372">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-372">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="95764-373">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="95764-373">Policy Insights</span></span>
* <span data-ttu-id="95764-374">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-374">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="95764-375">RDBMS</span><span class="sxs-lookup"><span data-stu-id="95764-375">RDBMS</span></span>
* <span data-ttu-id="95764-376">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="95764-376">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="95764-377">Redis</span><span class="sxs-lookup"><span data-stu-id="95764-377">Redis</span></span>
* <span data-ttu-id="95764-378">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-378">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="95764-379">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-379">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="95764-380">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-380">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="95764-381">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-381">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="95764-382">[破壊的変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-382">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="95764-383">[破壊的変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="95764-383">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="95764-384">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-384">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="95764-385">Role</span><span class="sxs-lookup"><span data-stu-id="95764-385">Role</span></span>
* <span data-ttu-id="95764-386">[破壊的変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="95764-386">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="95764-387">SQL VM</span><span class="sxs-lookup"><span data-stu-id="95764-387">SQL VM</span></span>
* <span data-ttu-id="95764-388">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-388">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="95764-389">VM</span><span class="sxs-lookup"><span data-stu-id="95764-389">VM</span></span>
* <span data-ttu-id="95764-390">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-390">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="95764-391">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-391">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="95764-392">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-392">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="95764-393">[破壊的変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="95764-393">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="95764-394">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="95764-394">January 31, 2019</span></span>

<span data-ttu-id="95764-395">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="95764-395">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="95764-396">コア</span><span class="sxs-lookup"><span data-stu-id="95764-396">Core</span></span>

* <span data-ttu-id="95764-397">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="95764-397">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="95764-398">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="95764-398">January 28, 2019</span></span>

<span data-ttu-id="95764-399">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="95764-399">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="95764-400">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-400">ACR</span></span>
* <span data-ttu-id="95764-401">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-401">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="95764-402">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-402">ACS</span></span>
* <span data-ttu-id="95764-403">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-403">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="95764-404">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-404">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="95764-405">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-405">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="95764-406">AMS</span><span class="sxs-lookup"><span data-stu-id="95764-406">AMS</span></span>
* <span data-ttu-id="95764-407">[破壊的変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-407">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="95764-408">[破壊的変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-408">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-409">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-409">Appservice</span></span>
* <span data-ttu-id="95764-410">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-410">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="95764-411">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-411">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="95764-412">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-412">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="95764-413">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-413">Container</span></span>
* <span data-ttu-id="95764-414">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-414">Added `container start` command</span></span>
* <span data-ttu-id="95764-415">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-415">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="95764-416">EventGrid</span><span class="sxs-lookup"><span data-stu-id="95764-416">EventGrid</span></span>
* <span data-ttu-id="95764-417">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-417">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="95764-418">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-418">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="95764-419">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-419">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="95764-420">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-420">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="95764-421">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="95764-421">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="95764-422">HDInsight</span><span class="sxs-lookup"><span data-stu-id="95764-422">HDInsight</span></span>
* <span data-ttu-id="95764-423">[破壊的変更] `hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-423">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="95764-424">[破壊的変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-424">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="95764-425">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-425">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="95764-426">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-426">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="95764-427">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-427">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="95764-428">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-428">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="95764-429">IoT</span><span class="sxs-lookup"><span data-stu-id="95764-429">IoT</span></span>
* <span data-ttu-id="95764-430">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-430">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="95764-431">Kusto</span><span class="sxs-lookup"><span data-stu-id="95764-431">Kusto</span></span>
* <span data-ttu-id="95764-432">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="95764-432">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-433">監視</span><span class="sxs-lookup"><span data-stu-id="95764-433">Monitor</span></span>
* <span data-ttu-id="95764-434">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-434">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="95764-435">プロファイル</span><span class="sxs-lookup"><span data-stu-id="95764-435">Profile</span></span>
* <span data-ttu-id="95764-436">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="95764-436">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="95764-437">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-437">Network</span></span>
* <span data-ttu-id="95764-438">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-438">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="95764-439">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-439">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="95764-440">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-440">Resource</span></span>
* <span data-ttu-id="95764-441">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-441">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="95764-442">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-442">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="95764-443">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="95764-443">SQL Virtual Machine</span></span>
* <span data-ttu-id="95764-444">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="95764-444">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="95764-445">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-445">Storage</span></span>
* <span data-ttu-id="95764-446">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-446">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="95764-447">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="95764-447">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="95764-448">VM</span><span class="sxs-lookup"><span data-stu-id="95764-448">VM</span></span>
* <span data-ttu-id="95764-449">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-449">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="95764-450">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-450">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="95764-451">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="95764-451">January 15, 2019</span></span>

<span data-ttu-id="95764-452">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="95764-452">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="95764-453">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-453">ACR</span></span>
* <span data-ttu-id="95764-454">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-454">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="95764-455">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-455">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="95764-456">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-456">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="95764-457">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-457">ACS</span></span>
* <span data-ttu-id="95764-458">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-458">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-459">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-459">Appservice</span></span>
* <span data-ttu-id="95764-460">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-460">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="95764-461">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-461">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="95764-462">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-462">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="95764-463">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-463">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="95764-464">Botservice</span><span class="sxs-lookup"><span data-stu-id="95764-464">Botservice</span></span>
* <span data-ttu-id="95764-465">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-465">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="95764-466">構成</span><span class="sxs-lookup"><span data-stu-id="95764-466">Configure</span></span>
* <span data-ttu-id="95764-467">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-467">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="95764-468">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="95764-468">CosmosDB</span></span>
* <span data-ttu-id="95764-469">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-469">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="95764-470">HDInsight</span><span class="sxs-lookup"><span data-stu-id="95764-470">HDInsight</span></span>
* <span data-ttu-id="95764-471">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-471">Added commands for managing applications</span></span>
* <span data-ttu-id="95764-472">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-472">Added commands for managing script actions</span></span>
* <span data-ttu-id="95764-473">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-473">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="95764-474">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-474">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="95764-475">[破壊的変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-475">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="95764-476">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-476">Network</span></span>
* <span data-ttu-id="95764-477">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-477">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="95764-478">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-478">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="95764-479">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-479">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="95764-480">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-480">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="95764-481">Role</span><span class="sxs-lookup"><span data-stu-id="95764-481">Role</span></span>
* <span data-ttu-id="95764-482">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="95764-482">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="95764-483">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="95764-483">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="95764-484">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="95764-484">Security</span></span>
* <span data-ttu-id="95764-485">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="95764-485">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="95764-486">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-486">Storage</span></span>
* <span data-ttu-id="95764-487">[破壊的変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="95764-487">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="95764-488">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="95764-488">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="95764-489">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-489">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="95764-490">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-490">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="95764-491">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-491">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="95764-492">VM</span><span class="sxs-lookup"><span data-stu-id="95764-492">VM</span></span>
* <span data-ttu-id="95764-493">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-493">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="95764-494">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-494">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="95764-495">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-495">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="95764-496">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-496">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="95764-497">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-497">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="95764-498">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-498">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="95764-499">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="95764-499">December 20, 2018</span></span>

<span data-ttu-id="95764-500">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="95764-500">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="95764-501">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-501">Appservice</span></span>
* <span data-ttu-id="95764-502">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-502">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="95764-503">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-503">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="95764-504">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-504">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="95764-505">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="95764-505">IoTCentral</span></span>
* <span data-ttu-id="95764-506">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-506">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="95764-507">Role</span><span class="sxs-lookup"><span data-stu-id="95764-507">Role</span></span>
* <span data-ttu-id="95764-508">[破壊的変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-508">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="95764-509">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-509">SQL</span></span>
* <span data-ttu-id="95764-510">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-510">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="95764-511">VM</span><span class="sxs-lookup"><span data-stu-id="95764-511">VM</span></span>
* <span data-ttu-id="95764-512">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-512">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="95764-513">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="95764-513">December 18, 2018</span></span>

<span data-ttu-id="95764-514">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="95764-514">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="95764-515">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-515">ACR</span></span>
* <span data-ttu-id="95764-516">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-516">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="95764-517">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="95764-517">Condensed the table layout for task list</span></span>
* <span data-ttu-id="95764-518">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-518">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="95764-519">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-519">ACS</span></span>
* <span data-ttu-id="95764-520">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-520">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="95764-521">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-521">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="95764-522">[非推奨] `az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="95764-522">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="95764-523">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="95764-523">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="95764-524">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-524">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="95764-525">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-525">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-526">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-526">Appservice</span></span>
* <span data-ttu-id="95764-527">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-527">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="95764-528">Botservice</span><span class="sxs-lookup"><span data-stu-id="95764-528">Botservice</span></span>
* <span data-ttu-id="95764-529">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-529">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="95764-530">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-530">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="95764-531">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-531">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="95764-532">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="95764-532">Reduced Kudu network calls</span></span>
* <span data-ttu-id="95764-533">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-533">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="95764-534">消費</span><span class="sxs-lookup"><span data-stu-id="95764-534">Consumption</span></span>
* <span data-ttu-id="95764-535">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-535">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="95764-536">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="95764-536">CosmosDB</span></span>
* <span data-ttu-id="95764-537">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-537">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="95764-538">マップ</span><span class="sxs-lookup"><span data-stu-id="95764-538">Maps</span></span>
* <span data-ttu-id="95764-539">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-539">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="95764-540">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-540">Network</span></span>
* <span data-ttu-id="95764-541">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-541">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="95764-542">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-542">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="95764-543">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-543">Resource</span></span>
* <span data-ttu-id="95764-544">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-544">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="95764-545">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-545">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="95764-546">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-546">Storage</span></span>
*  <span data-ttu-id="95764-547">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-547">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="95764-548">VM</span><span class="sxs-lookup"><span data-stu-id="95764-548">VM</span></span>
* <span data-ttu-id="95764-549">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-549">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="95764-550">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="95764-550">December 4, 2018</span></span>

<span data-ttu-id="95764-551">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="95764-551">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="95764-552">コア</span><span class="sxs-lookup"><span data-stu-id="95764-552">Core</span></span>
* <span data-ttu-id="95764-553">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-553">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="95764-554">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-554">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-555">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-555">Appservice</span></span>
* <span data-ttu-id="95764-556">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-556">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="95764-557">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-557">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="95764-558">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-558">Network</span></span>
* <span data-ttu-id="95764-559">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-559">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="95764-560">Role</span><span class="sxs-lookup"><span data-stu-id="95764-560">Role</span></span>
* <span data-ttu-id="95764-561">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-561">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="95764-562">VM</span><span class="sxs-lookup"><span data-stu-id="95764-562">VM</span></span>
* <span data-ttu-id="95764-563">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-563">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="95764-564">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-564">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="95764-565">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-565">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="95764-566">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-566">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="95764-567">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="95764-567">November 20, 2018</span></span>

<span data-ttu-id="95764-568">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="95764-568">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="95764-569">コア</span><span class="sxs-lookup"><span data-stu-id="95764-569">Core</span></span>
* <span data-ttu-id="95764-570">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-570">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="95764-571">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-571">ACR</span></span>
* <span data-ttu-id="95764-572">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-572">Added context token to task step</span></span>
* <span data-ttu-id="95764-573">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-573">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="95764-574">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-574">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-575">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-575">Appservice</span></span>
* <span data-ttu-id="95764-576">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-576">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="95764-577">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="95764-577">Updated the default `node_version`.</span></span> <span data-ttu-id="95764-578">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="95764-578">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="95764-579">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-579">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="95764-580">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-580">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="95764-581">IotCentral</span><span class="sxs-lookup"><span data-stu-id="95764-581">IotCentral</span></span>
* <span data-ttu-id="95764-582">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-582">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="95764-583">KeyVault</span><span class="sxs-lookup"><span data-stu-id="95764-583">KeyVault</span></span>
* <span data-ttu-id="95764-584">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-584">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="95764-585">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-585">Network</span></span>
* <span data-ttu-id="95764-586">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-586">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="95764-587">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-587">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="95764-588">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-588">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="95764-589">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-589">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="95764-590">Rdbms</span><span class="sxs-lookup"><span data-stu-id="95764-590">Rdbms</span></span>
* <span data-ttu-id="95764-591">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-591">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="95764-592">Rbac</span><span class="sxs-lookup"><span data-stu-id="95764-592">Rbac</span></span>
* <span data-ttu-id="95764-593">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-593">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="95764-594">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-594">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="95764-595">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-595">Storage</span></span>
* <span data-ttu-id="95764-596">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-596">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="95764-597">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-597">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="95764-598">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-598">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="95764-599">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="95764-599">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="95764-600">VM</span><span class="sxs-lookup"><span data-stu-id="95764-600">VM</span></span>
* <span data-ttu-id="95764-601">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-601">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="95764-602">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-602">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="95764-603">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="95764-603">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="95764-604">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-604">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="95764-605">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-605">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="95764-606">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-606">Added `snapshot wait` command</span></span>
* <span data-ttu-id="95764-607">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-607">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="95764-608">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="95764-608">November 6, 2018</span></span>

<span data-ttu-id="95764-609">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="95764-609">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="95764-610">コア</span><span class="sxs-lookup"><span data-stu-id="95764-610">Core</span></span>
* <span data-ttu-id="95764-611">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-611">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="95764-612">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-612">ACR</span></span>
* <span data-ttu-id="95764-613">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-613">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="95764-614">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-614">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="95764-615">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-615">ACS</span></span>
* <span data-ttu-id="95764-616">[破壊的変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-616">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="95764-617">Advisor</span><span class="sxs-lookup"><span data-stu-id="95764-617">Advisor</span></span>
* <span data-ttu-id="95764-618">GA リリース</span><span class="sxs-lookup"><span data-stu-id="95764-618">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="95764-619">AMS</span><span class="sxs-lookup"><span data-stu-id="95764-619">AMS</span></span>
* <span data-ttu-id="95764-620">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-620">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="95764-621">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-621">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="95764-622">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-622">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="95764-623">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-623">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="95764-624">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-624">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="95764-625">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-625">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="95764-626">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-626">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="95764-627">[破壊的変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="95764-627">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="95764-628">[破壊的変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-628">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="95764-629">[破壊的変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-629">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="95764-630">[破壊的変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="95764-630">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="95764-631">[破壊的変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="95764-631">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="95764-632">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="95764-632">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="95764-633">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="95764-633">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="95764-634">[破壊的変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="95764-634">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="95764-635">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="95764-635">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="95764-636">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="95764-636">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-637">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-637">AppService</span></span>
* <span data-ttu-id="95764-638">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-638">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="95764-639">構成</span><span class="sxs-lookup"><span data-stu-id="95764-639">Configure</span></span>
* <span data-ttu-id="95764-640">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-640">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="95764-641">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-641">Container</span></span>
* <span data-ttu-id="95764-642">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-642">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="95764-643">EventHub</span><span class="sxs-lookup"><span data-stu-id="95764-643">EventHub</span></span>
* <span data-ttu-id="95764-644">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-644">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="95764-645">Interactive</span><span class="sxs-lookup"><span data-stu-id="95764-645">Interactive</span></span>
* <span data-ttu-id="95764-646">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="95764-646">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-647">監視</span><span class="sxs-lookup"><span data-stu-id="95764-647">Monitor</span></span>
* <span data-ttu-id="95764-648">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-648">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="95764-649">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-649">Network</span></span>
* <span data-ttu-id="95764-650">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-650">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="95764-651">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-651">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="95764-652">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-652">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="95764-653">プロファイル</span><span class="sxs-lookup"><span data-stu-id="95764-653">Profile</span></span>
* <span data-ttu-id="95764-654">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-654">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="95764-655">RDBMS</span><span class="sxs-lookup"><span data-stu-id="95764-655">RDBMS</span></span>
* <span data-ttu-id="95764-656">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-656">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="95764-657">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-657">Resource</span></span>
* <span data-ttu-id="95764-658">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-658">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="95764-659">Role</span><span class="sxs-lookup"><span data-stu-id="95764-659">Role</span></span>
* <span data-ttu-id="95764-660">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-660">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="95764-661">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-661">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="95764-662">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-662">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="95764-663">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-663">Storage</span></span>
* <span data-ttu-id="95764-664">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="95764-664">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="95764-665">VM</span><span class="sxs-lookup"><span data-stu-id="95764-665">VM</span></span>
* <span data-ttu-id="95764-666">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-666">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="95764-667">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-667">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="95764-668">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-668">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="95764-669">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="95764-669">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="95764-670">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="95764-670">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="95764-671">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-671">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="95764-672">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="95764-672">October 23, 2018</span></span>

<span data-ttu-id="95764-673">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="95764-673">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="95764-674">コア</span><span class="sxs-lookup"><span data-stu-id="95764-674">Core</span></span>
* <span data-ttu-id="95764-675">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-675">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="95764-676">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-676">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="95764-677">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-677">ACR</span></span>
* <span data-ttu-id="95764-678">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-678">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="95764-679">CDN</span><span class="sxs-lookup"><span data-stu-id="95764-679">CDN</span></span>
* <span data-ttu-id="95764-680">[破壊的変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="95764-680">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="95764-681">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-681">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="95764-682">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-682">Container</span></span>
* <span data-ttu-id="95764-683">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-683">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="95764-684">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-684">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="95764-685">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-685">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="95764-686">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-686">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="95764-687">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-687">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="95764-688">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-688">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="95764-689">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-689">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="95764-690">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="95764-690">CosmosDB</span></span>
* <span data-ttu-id="95764-691">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-691">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="95764-692">Interactive</span><span class="sxs-lookup"><span data-stu-id="95764-692">Interactive</span></span>
* <span data-ttu-id="95764-693">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-693">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="95764-694">IoT Central</span><span class="sxs-lookup"><span data-stu-id="95764-694">IoT Central</span></span>
* <span data-ttu-id="95764-695">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-695">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="95764-696">[破壊的変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="95764-696">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-697">監視</span><span class="sxs-lookup"><span data-stu-id="95764-697">Monitor</span></span>
* <span data-ttu-id="95764-698">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="95764-698">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="95764-699">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-699">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="95764-700">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-700">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="95764-701">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-701">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="95764-702">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-702">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="95764-703">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-703">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="95764-704">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="95764-704">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="95764-705">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-705">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="95764-706">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-706">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="95764-707">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-707">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="95764-708">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-708">Network</span></span>
* <span data-ttu-id="95764-709">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-709">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="95764-710">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-710">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="95764-711">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="95764-711">ServiceBus</span></span>
* <span data-ttu-id="95764-712">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-712">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="95764-713">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-713">SQL</span></span>
* <span data-ttu-id="95764-714">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-714">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="95764-715">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-715">Storage</span></span>
* <span data-ttu-id="95764-716">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-716">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="95764-717">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-717">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="95764-718">VM</span><span class="sxs-lookup"><span data-stu-id="95764-718">VM</span></span>
* <span data-ttu-id="95764-719">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="95764-719">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="95764-720">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-720">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="95764-721">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-721">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="95764-722">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="95764-722">October 16, 2018</span></span>

<span data-ttu-id="95764-723">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="95764-723">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="95764-724">VM</span><span class="sxs-lookup"><span data-stu-id="95764-724">VM</span></span>
* <span data-ttu-id="95764-725">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-725">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="95764-726">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="95764-726">October 9, 2018</span></span>

<span data-ttu-id="95764-727">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="95764-727">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="95764-728">コア</span><span class="sxs-lookup"><span data-stu-id="95764-728">Core</span></span>
* <span data-ttu-id="95764-729">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-729">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="95764-730">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-730">ACR</span></span>
* <span data-ttu-id="95764-731">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-731">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="95764-732">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-732">ACS</span></span>
* <span data-ttu-id="95764-733">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="95764-733">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="95764-734">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-734">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="95764-735">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-735">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="95764-736">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-736">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="95764-737">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-737">Container</span></span>
* <span data-ttu-id="95764-738">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-738">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="95764-739">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-739">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="95764-740">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="95764-740">Event Hub</span></span>
* <span data-ttu-id="95764-741">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-741">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="95764-742">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-742">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="95764-743">Extensions</span><span class="sxs-lookup"><span data-stu-id="95764-743">Extensions</span></span>
* <span data-ttu-id="95764-744">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-744">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="95764-745">HDInsight</span><span class="sxs-lookup"><span data-stu-id="95764-745">HDInsight</span></span>
* <span data-ttu-id="95764-746">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="95764-746">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="95764-747">IoT</span><span class="sxs-lookup"><span data-stu-id="95764-747">IoT</span></span>
* <span data-ttu-id="95764-748">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-748">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="95764-749">KeyVault</span><span class="sxs-lookup"><span data-stu-id="95764-749">KeyVault</span></span>
* <span data-ttu-id="95764-750">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-750">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="95764-751">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-751">Network</span></span>
* <span data-ttu-id="95764-752">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="95764-752">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="95764-753">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="95764-753">See #6052</span></span>
* <span data-ttu-id="95764-754">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-754">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="95764-755">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="95764-755">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="95764-756">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-756">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="95764-757">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-757">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="95764-758">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-758">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="95764-759">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-759">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="95764-760">Role</span><span class="sxs-lookup"><span data-stu-id="95764-760">Role</span></span>
* <span data-ttu-id="95764-761">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-761">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="95764-762">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-762">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="95764-763">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-763">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="95764-764">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-764">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="95764-765">Service Bus</span><span class="sxs-lookup"><span data-stu-id="95764-765">Service Bus</span></span>
* <span data-ttu-id="95764-766">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-766">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="95764-767">VM</span><span class="sxs-lookup"><span data-stu-id="95764-767">VM</span></span>
* <span data-ttu-id="95764-768">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-768">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="95764-769">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-769">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="95764-770">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-770">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="95764-771">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-771">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="95764-772">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-772">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="95764-773">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-773">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="95764-774">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="95764-774">September 21, 2018</span></span>

<span data-ttu-id="95764-775">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="95764-775">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="95764-776">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-776">ACR</span></span>
* <span data-ttu-id="95764-777">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-777">Added ACR Task commands</span></span>
* <span data-ttu-id="95764-778">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-778">Added quick run command</span></span>
* <span data-ttu-id="95764-779">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-779">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="95764-780">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-780">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="95764-781">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-781">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="95764-782">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-782">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="95764-783">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-783">ACS</span></span>
* <span data-ttu-id="95764-784">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-784">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="95764-785">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-785">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-786">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-786">AppService</span></span>

* <span data-ttu-id="95764-787">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-787">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="95764-788">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-788">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="95764-789">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-789">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="95764-790">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-790">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="95764-791">Batch</span><span class="sxs-lookup"><span data-stu-id="95764-791">Batch</span></span>
* <span data-ttu-id="95764-792">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-792">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="95764-793">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-793">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="95764-794">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-794">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="95764-795">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-795">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="95764-796">Batch AI</span><span class="sxs-lookup"><span data-stu-id="95764-796">Batch AI</span></span> 
* <span data-ttu-id="95764-797">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-797">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="95764-798">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="95764-798">Cognitive Services</span></span>
* <span data-ttu-id="95764-799">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-799">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="95764-800">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-800">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="95764-801">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-801">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="95764-802">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-802">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="95764-803">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-803">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="95764-804">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-804">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="95764-805">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-805">Container</span></span>
* <span data-ttu-id="95764-806">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-806">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="95764-807">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-807">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="95764-808">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-808">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="95764-809">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-809">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="95764-810">DataLake</span><span class="sxs-lookup"><span data-stu-id="95764-810">Datalake</span></span>
* <span data-ttu-id="95764-811">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-811">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="95764-812">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="95764-812">Interactive Shell</span></span>
* <span data-ttu-id="95764-813">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-813">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="95764-814">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-814">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="95764-815">IoT</span><span class="sxs-lookup"><span data-stu-id="95764-815">IoT</span></span>
* <span data-ttu-id="95764-816">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-816">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="95764-817">Key Vault</span><span class="sxs-lookup"><span data-stu-id="95764-817">Key Vault</span></span>
* <span data-ttu-id="95764-818">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-818">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="95764-819">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-819">Network</span></span>
* <span data-ttu-id="95764-820">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-820">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="95764-821">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-821">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="95764-822">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-822">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="95764-823">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-823">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="95764-824">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-824">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="95764-825">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-825">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="95764-826">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="95764-826">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="95764-827">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-827">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="95764-828">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-828">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="95764-829">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-829">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="95764-830">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-830">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="95764-831">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-831">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="95764-832">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-832">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="95764-833">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="95764-833">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="95764-834">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-834">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="95764-835">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-835">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="95764-836">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-836">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="95764-837">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-837">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="95764-838">RDBMS</span><span class="sxs-lookup"><span data-stu-id="95764-838">RDBMS</span></span>
* <span data-ttu-id="95764-839">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-839">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="95764-840">予約</span><span class="sxs-lookup"><span data-stu-id="95764-840">Reservation</span></span>
* <span data-ttu-id="95764-841">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-841">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="95764-842">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-842">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="95764-843">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="95764-843">Manage App</span></span>
* <span data-ttu-id="95764-844">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-844">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="95764-845">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-845">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="95764-846">Role</span><span class="sxs-lookup"><span data-stu-id="95764-846">Role</span></span>
* <span data-ttu-id="95764-847">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-847">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="95764-848">SignalR</span><span class="sxs-lookup"><span data-stu-id="95764-848">SignalR</span></span>
* <span data-ttu-id="95764-849">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="95764-849">First release</span></span>

### <a name="storage"></a><span data-ttu-id="95764-850">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-850">Storage</span></span>
* <span data-ttu-id="95764-851">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-851">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="95764-852">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-852">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="95764-853">VM</span><span class="sxs-lookup"><span data-stu-id="95764-853">VM</span></span>
* <span data-ttu-id="95764-854">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="95764-854">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="95764-855">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-855">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="95764-856">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="95764-856">August 28, 2018</span></span>

<span data-ttu-id="95764-857">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="95764-857">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="95764-858">コア</span><span class="sxs-lookup"><span data-stu-id="95764-858">Core</span></span>

* <span data-ttu-id="95764-859">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-859">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="95764-860">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-860">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="95764-861">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-861">ACR</span></span>

* <span data-ttu-id="95764-862">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-862">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="95764-863">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-863">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="95764-864">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-864">ACS</span></span>

* <span data-ttu-id="95764-865">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-865">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="95764-866">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-866">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-867">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-867">AppService</span></span>

* <span data-ttu-id="95764-868">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-868">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="95764-869">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-869">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="95764-870">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-870">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="95764-871">バックアップ</span><span class="sxs-lookup"><span data-stu-id="95764-871">Backup</span></span>

* <span data-ttu-id="95764-872">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-872">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="95764-873">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="95764-873">Bot Service</span></span>

* <span data-ttu-id="95764-874">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="95764-874">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="95764-875">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="95764-875">Cognitive Services</span></span>

* <span data-ttu-id="95764-876">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-876">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="95764-877">IoT</span><span class="sxs-lookup"><span data-stu-id="95764-877">IoT</span></span>

* <span data-ttu-id="95764-878">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-878">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-879">監視</span><span class="sxs-lookup"><span data-stu-id="95764-879">Monitor</span></span>

* <span data-ttu-id="95764-880">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-880">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="95764-881">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-881">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="95764-882">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-882">Network</span></span>

* <span data-ttu-id="95764-883">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-883">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="95764-884">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-884">Resource</span></span>

* <span data-ttu-id="95764-885">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-885">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="95764-886">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-886">Storage</span></span>

* <span data-ttu-id="95764-887">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-887">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="95764-888">VM</span><span class="sxs-lookup"><span data-stu-id="95764-888">VM</span></span>

* <span data-ttu-id="95764-889">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-889">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="95764-890">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-890">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="95764-891">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="95764-891">Auguest 14, 2018</span></span>

<span data-ttu-id="95764-892">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="95764-892">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="95764-893">コア</span><span class="sxs-lookup"><span data-stu-id="95764-893">Core</span></span>

* <span data-ttu-id="95764-894">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-894">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="95764-895">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-895">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="95764-896">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="95764-896">Telemetry</span></span>

* <span data-ttu-id="95764-897">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-897">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="95764-898">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-898">ACR</span></span>

* <span data-ttu-id="95764-899">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-899">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="95764-900">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-900">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="95764-901">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-901">ACS</span></span>

* <span data-ttu-id="95764-902">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-902">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="95764-903">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-903">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="95764-904">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-904">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="95764-905">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-905">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="95764-906">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-906">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="95764-907">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-907">AppService</span></span>

* <span data-ttu-id="95764-908">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-908">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="95764-909">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-909">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="95764-910">BatchAI</span><span class="sxs-lookup"><span data-stu-id="95764-910">BatchAI</span></span>

* <span data-ttu-id="95764-911">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="95764-911">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="95764-912">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-912">Container</span></span>

* <span data-ttu-id="95764-913">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-913">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="95764-914">IoT</span><span class="sxs-lookup"><span data-stu-id="95764-914">IoT</span></span>

* <span data-ttu-id="95764-915">[破壊的変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-915">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="95764-916">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-916">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="95764-917">Iot Central</span><span class="sxs-lookup"><span data-stu-id="95764-917">Iot Central</span></span>

* <span data-ttu-id="95764-918">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="95764-918">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="95764-919">KeyVault</span><span class="sxs-lookup"><span data-stu-id="95764-919">KeyVault</span></span>


* <span data-ttu-id="95764-920">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-920">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="95764-921">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-921">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="95764-922">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-922">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="95764-923">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-923">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="95764-924">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-924">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="95764-925">リレー</span><span class="sxs-lookup"><span data-stu-id="95764-925">Relay</span></span>

* <span data-ttu-id="95764-926">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="95764-926">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="95764-927">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-927">Sql</span></span>

* <span data-ttu-id="95764-928">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-928">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="95764-929">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-929">Storage</span></span>

* <span data-ttu-id="95764-930">[破壊的変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="95764-930">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="95764-931">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-931">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="95764-932">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="95764-932">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="95764-933">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-933">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="95764-934">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-934">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="95764-935">VM</span><span class="sxs-lookup"><span data-stu-id="95764-935">VM</span></span>

* <span data-ttu-id="95764-936">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-936">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="95764-937">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="95764-937">July 31, 2018</span></span>

<span data-ttu-id="95764-938">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="95764-938">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="95764-939">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-939">ACR</span></span>

* <span data-ttu-id="95764-940">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-940">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="95764-941">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-941">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="95764-942">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-942">ACS</span></span>

* <span data-ttu-id="95764-943">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-943">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="95764-944">Batch</span><span class="sxs-lookup"><span data-stu-id="95764-944">Batch</span></span>

* <span data-ttu-id="95764-945">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-945">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="95764-946">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-946">Container</span></span>

* <span data-ttu-id="95764-947">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-947">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="95764-948">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-948">Network</span></span>

* <span data-ttu-id="95764-949">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-949">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="95764-950">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-950">Resource</span></span>

* <span data-ttu-id="95764-951">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-951">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="95764-952">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-952">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="95764-953">Role</span><span class="sxs-lookup"><span data-stu-id="95764-953">Role</span></span>

* <span data-ttu-id="95764-954">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-954">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="95764-955">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-955">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="95764-956">Search</span><span class="sxs-lookup"><span data-stu-id="95764-956">Search</span></span>

* <span data-ttu-id="95764-957">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-957">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="95764-958">Service Bus</span><span class="sxs-lookup"><span data-stu-id="95764-958">Service Bus</span></span>

* <span data-ttu-id="95764-959">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-959">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="95764-960">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-960">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="95764-961">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="95764-961">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="95764-962">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="95764-962">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="95764-963">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-963">Storage</span></span>

* <span data-ttu-id="95764-964">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-964">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="95764-965">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="95764-965">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="95764-966">VM</span><span class="sxs-lookup"><span data-stu-id="95764-966">VM</span></span>

* <span data-ttu-id="95764-967">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-967">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="95764-968">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-968">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="95764-969">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-969">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="95764-970">[破壊的変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-970">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="95764-971">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="95764-971">July 18, 2018</span></span>

<span data-ttu-id="95764-972">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="95764-972">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="95764-973">コア</span><span class="sxs-lookup"><span data-stu-id="95764-973">Core</span></span>

* <span data-ttu-id="95764-974">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-974">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="95764-975">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-975">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="95764-976">[破壊的変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-976">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="95764-977">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-977">ACR</span></span>

* <span data-ttu-id="95764-978">[破壊的変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-978">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="95764-979">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-979">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="95764-980">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-980">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="95764-981">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-981">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="95764-982">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-982">ACS</span></span>

* <span data-ttu-id="95764-983">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-983">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-984">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-984">AppService</span></span>

* <span data-ttu-id="95764-985">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-985">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="95764-986">Batch</span><span class="sxs-lookup"><span data-stu-id="95764-986">Batch</span></span>

* <span data-ttu-id="95764-987">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-987">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="95764-988">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-988">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="95764-989">Batch AI</span><span class="sxs-lookup"><span data-stu-id="95764-989">Batch AI</span></span>

* <span data-ttu-id="95764-990">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-990">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="95764-991">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-991">Container</span></span>

* <span data-ttu-id="95764-992">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-992">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="95764-993">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-993">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="95764-994">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-994">Network</span></span>

* <span data-ttu-id="95764-995">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-995">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="95764-996">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-996">Added `network nic wait`</span></span>
* <span data-ttu-id="95764-997">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-997">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="95764-998">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-998">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="95764-999">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-999">Resource</span></span>

* <span data-ttu-id="95764-1000">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1000">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="95764-1001">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1001">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="95764-1002">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1002">Added `deployment wait` command</span></span>
* <span data-ttu-id="95764-1003">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1003">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="95764-1004">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-1004">SQL</span></span>

* <span data-ttu-id="95764-1005">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1005">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="95764-1006">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-1006">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="95764-1007">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="95764-1007">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1008">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1008">Storage</span></span>

* <span data-ttu-id="95764-1009">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1009">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1010">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1010">VM</span></span>

* <span data-ttu-id="95764-1011">[破壊的変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1011">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="95764-1012">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1012">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="95764-1013">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1013">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="95764-1014">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="95764-1014">July 3, 2018</span></span>

<span data-ttu-id="95764-1015">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="95764-1015">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="95764-1016">AKS</span><span class="sxs-lookup"><span data-stu-id="95764-1016">AKS</span></span>

* <span data-ttu-id="95764-1017">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1017">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="95764-1018">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="95764-1018">July 3, 2018</span></span>

<span data-ttu-id="95764-1019">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="95764-1019">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="95764-1020">コア</span><span class="sxs-lookup"><span data-stu-id="95764-1020">Core</span></span>

* <span data-ttu-id="95764-1021">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1021">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="95764-1022">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-1022">ACR</span></span>

* <span data-ttu-id="95764-1023">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1023">Added polling build status</span></span>
* <span data-ttu-id="95764-1024">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1024">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="95764-1025">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1025">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1026">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1026">ACS</span></span>

* <span data-ttu-id="95764-1027">[破壊的変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1027">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="95764-1028">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1028">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="95764-1029">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1029">Updated options for `aks browse` command.</span></span> <span data-ttu-id="95764-1030">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1030">Added `--listen-port` support</span></span>
* <span data-ttu-id="95764-1031">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1031">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="95764-1032">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="95764-1032">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="95764-1033">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1033">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1034">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-1034">AppService</span></span>

* <span data-ttu-id="95764-1035">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-1035">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="95764-1036">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1036">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="95764-1037">バックアップ</span><span class="sxs-lookup"><span data-stu-id="95764-1037">Backup</span></span>

* <span data-ttu-id="95764-1038">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-1038">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="95764-1039">BatchAI</span><span class="sxs-lookup"><span data-stu-id="95764-1039">BatchAI</span></span>

* <span data-ttu-id="95764-1040">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1040">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="95764-1041">クラウド</span><span class="sxs-lookup"><span data-stu-id="95764-1041">Cloud</span></span>

* <span data-ttu-id="95764-1042">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1042">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="95764-1043">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-1043">Container</span></span>

* <span data-ttu-id="95764-1044">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1044">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="95764-1045">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1045">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="95764-1046">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1046">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="95764-1047">拡張機能</span><span class="sxs-lookup"><span data-stu-id="95764-1047">Extension</span></span>

* <span data-ttu-id="95764-1048">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1048">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="95764-1049">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1049">Network</span></span>

* <span data-ttu-id="95764-1050">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1050">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="95764-1051">Rdbms</span><span class="sxs-lookup"><span data-stu-id="95764-1051">Rdbms</span></span>

* <span data-ttu-id="95764-1052">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1052">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="95764-1053">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-1053">Resource</span></span>

* <span data-ttu-id="95764-1054">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1054">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1055">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1055">VM</span></span>

* <span data-ttu-id="95764-1056">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-1056">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="95764-1057">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="95764-1057">June 25, 2018</span></span>

<span data-ttu-id="95764-1058">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="95764-1058">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="95764-1059">CLI</span><span class="sxs-lookup"><span data-stu-id="95764-1059">CLI</span></span>

* <span data-ttu-id="95764-1060">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-1060">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="95764-1061">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="95764-1061">June 19, 2018</span></span>

<span data-ttu-id="95764-1062">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="95764-1062">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="95764-1063">コア</span><span class="sxs-lookup"><span data-stu-id="95764-1063">Core</span></span>

* <span data-ttu-id="95764-1064">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1064">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="95764-1065">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-1065">ACR</span></span>

* <span data-ttu-id="95764-1066">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1066">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="95764-1067">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1067">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1068">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1068">ACS</span></span>

* <span data-ttu-id="95764-1069">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1069">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="95764-1070">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1070">Added `--update` support</span></span>
* <span data-ttu-id="95764-1071">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1071">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="95764-1072">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="95764-1072">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="95764-1073">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1073">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="95764-1074">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1074">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="95764-1075">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1075">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="95764-1076">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1076">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1077">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-1077">AppService</span></span>

* <span data-ttu-id="95764-1078">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1078">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="95764-1079">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1079">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="95764-1080">Batch</span><span class="sxs-lookup"><span data-stu-id="95764-1080">Batch</span></span>

* <span data-ttu-id="95764-1081">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1081">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="95764-1082">Batch AI</span><span class="sxs-lookup"><span data-stu-id="95764-1082">Batch AI</span></span>

* <span data-ttu-id="95764-1083">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1083">Added support for workspaces.</span></span> <span data-ttu-id="95764-1084">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="95764-1084">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="95764-1085">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1085">Added support for experiments.</span></span> <span data-ttu-id="95764-1086">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="95764-1086">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="95764-1087">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1087">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="95764-1088">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1088">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="95764-1089">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="95764-1089">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="95764-1090">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1090">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="95764-1091">[破壊的変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="95764-1091">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="95764-1092">[破壊的変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="95764-1092">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="95764-1093">[破壊的変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1093">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="95764-1094">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="95764-1094">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="95764-1095">[破壊的変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1095">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="95764-1096">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="95764-1096">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="95764-1097">[破壊的変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1097">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="95764-1098">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="95764-1098">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="95764-1099">[破壊的変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1099">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="95764-1100">[破壊的変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1100">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="95764-1101">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1101">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="95764-1102">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1102">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="95764-1103">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1103">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="95764-1104">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1104">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="95764-1105">マップ</span><span class="sxs-lookup"><span data-stu-id="95764-1105">Maps</span></span>

* <span data-ttu-id="95764-1106">[破壊的変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1106">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="95764-1107">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1107">Network</span></span>

* <span data-ttu-id="95764-1108">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="95764-1108">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="95764-1109">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1109">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="95764-1110">#6502</span><span class="sxs-lookup"><span data-stu-id="95764-1110">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="95764-1111">Reservations</span><span class="sxs-lookup"><span data-stu-id="95764-1111">Reservations</span></span>

* <span data-ttu-id="95764-1112">[破壊的変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1112">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="95764-1113">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1113">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="95764-1114">[破壊的変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1114">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="95764-1115">[破壊的変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1115">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="95764-1116">[破壊的変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1116">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="95764-1117">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1117">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="95764-1118">Role</span><span class="sxs-lookup"><span data-stu-id="95764-1118">Role</span></span>

* <span data-ttu-id="95764-1119">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1119">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="95764-1120">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-1120">SQL</span></span>

* <span data-ttu-id="95764-1121">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1121">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1122">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1122">Storage</span></span>

* <span data-ttu-id="95764-1123">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="95764-1123">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1124">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1124">VM</span></span>

* <span data-ttu-id="95764-1125">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1125">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="95764-1126">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1126">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="95764-1127">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1127">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="95764-1128">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="95764-1128">June 13, 2018</span></span>

<span data-ttu-id="95764-1129">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="95764-1129">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="95764-1130">コア</span><span class="sxs-lookup"><span data-stu-id="95764-1130">Core</span></span>

* <span data-ttu-id="95764-1131">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1131">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="95764-1132">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="95764-1132">June 13, 2018</span></span>

<span data-ttu-id="95764-1133">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="95764-1133">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="95764-1134">AKS</span><span class="sxs-lookup"><span data-stu-id="95764-1134">AKS</span></span>

* <span data-ttu-id="95764-1135">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1135">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="95764-1136">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1136">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="95764-1137">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1137">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="95764-1138">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1138">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="95764-1139">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1139">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1140">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-1140">AppService</span></span>

* <span data-ttu-id="95764-1141">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1141">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="95764-1142">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="95764-1142">June 5, 2018</span></span>

<span data-ttu-id="95764-1143">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="95764-1143">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="95764-1144">Interactive</span><span class="sxs-lookup"><span data-stu-id="95764-1144">Interactive</span></span>

* <span data-ttu-id="95764-1145">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1145">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="95764-1146">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="95764-1146">June 5, 2018</span></span>

<span data-ttu-id="95764-1147">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="95764-1147">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="95764-1148">コア</span><span class="sxs-lookup"><span data-stu-id="95764-1148">Core</span></span>

* <span data-ttu-id="95764-1149">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1149">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="95764-1150">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="95764-1150">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="95764-1151">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-1151">ACR</span></span>

* <span data-ttu-id="95764-1152">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1152">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="95764-1153">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1153">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="95764-1154">AKS</span><span class="sxs-lookup"><span data-stu-id="95764-1154">AKS</span></span>

* <span data-ttu-id="95764-1155">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1155">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="95764-1156">Batch</span><span class="sxs-lookup"><span data-stu-id="95764-1156">Batch</span></span>

* <span data-ttu-id="95764-1157">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1157">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="95764-1158">IoT</span><span class="sxs-lookup"><span data-stu-id="95764-1158">IOT</span></span>

* <span data-ttu-id="95764-1159">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1159">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="95764-1160">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1160">Network</span></span>

* <span data-ttu-id="95764-1161">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="95764-1161">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="95764-1162">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="95764-1162">Policy Insights</span></span>

* <span data-ttu-id="95764-1163">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="95764-1163">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="95764-1164">ARM</span><span class="sxs-lookup"><span data-stu-id="95764-1164">ARM</span></span>

* <span data-ttu-id="95764-1165">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1165">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="95764-1166">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-1166">SQL</span></span>

* <span data-ttu-id="95764-1167">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1167">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="95764-1168">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1168">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="95764-1169">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1169">Storage</span></span>

* <span data-ttu-id="95764-1170">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1170">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1171">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1171">VM</span></span>

* <span data-ttu-id="95764-1172">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1172">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="95764-1173">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1173">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="95764-1174">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1174">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="95764-1175">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="95764-1175">May 22, 2018</span></span>

<span data-ttu-id="95764-1176">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="95764-1176">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="95764-1177">コア</span><span class="sxs-lookup"><span data-stu-id="95764-1177">Core</span></span>

* <span data-ttu-id="95764-1178">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1178">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1179">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1179">ACS</span></span>

* <span data-ttu-id="95764-1180">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1180">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="95764-1181">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1181">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1182">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-1182">AppService</span></span>

* <span data-ttu-id="95764-1183">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="95764-1183">Improved generic update commands</span></span>
* <span data-ttu-id="95764-1184">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1184">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="95764-1185">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-1185">Container</span></span>

* <span data-ttu-id="95764-1186">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1186">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="95764-1187">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1187">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="95764-1188">拡張機能</span><span class="sxs-lookup"><span data-stu-id="95764-1188">Extension</span></span>

* <span data-ttu-id="95764-1189">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="95764-1189">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="95764-1190">Interactive</span><span class="sxs-lookup"><span data-stu-id="95764-1190">Interactive</span></span>

* <span data-ttu-id="95764-1191">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1191">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="95764-1192">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="95764-1192">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="95764-1193">KeyVault</span><span class="sxs-lookup"><span data-stu-id="95764-1193">KeyVault</span></span>

* <span data-ttu-id="95764-1194">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1194">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="95764-1195">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1195">Network</span></span>

* <span data-ttu-id="95764-1196">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1196">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="95764-1197">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1197">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="95764-1198">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-1198">SQL</span></span>

* <span data-ttu-id="95764-1199">[破壊的変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1199">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="95764-1200">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1200">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="95764-1201">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1201">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="95764-1202">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1202">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="95764-1203">[破壊的変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1203">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="95764-1204">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="95764-1204">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="95764-1205">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="95764-1205">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="95764-1206">`edition`</span><span class="sxs-lookup"><span data-stu-id="95764-1206">`edition`.</span></span> <span data-ttu-id="95764-1207">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="95764-1207">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="95764-1208">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="95764-1208">`elasticPoolName`.</span></span> <span data-ttu-id="95764-1209">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="95764-1209">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="95764-1210">[破壊的変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1210">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="95764-1211">`edition`</span><span class="sxs-lookup"><span data-stu-id="95764-1211">`edition`.</span></span> <span data-ttu-id="95764-1212">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="95764-1212">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="95764-1213">`dtu`</span><span class="sxs-lookup"><span data-stu-id="95764-1213">`dtu`.</span></span> <span data-ttu-id="95764-1214">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="95764-1214">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="95764-1215">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="95764-1215">`databaseDtuMin`.</span></span> <span data-ttu-id="95764-1216">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="95764-1216">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="95764-1217">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="95764-1217">`databaseDtuMax`.</span></span> <span data-ttu-id="95764-1218">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="95764-1218">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="95764-1219">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1219">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="95764-1220">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1220">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1221">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1221">Storage</span></span>

* <span data-ttu-id="95764-1222">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1222">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="95764-1223">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1223">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1224">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1224">VM</span></span>

* <span data-ttu-id="95764-1225">[破壊的変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1225">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="95764-1226">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="95764-1226">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="95764-1227">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1227">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="95764-1228">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1228">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="95764-1229">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1229">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="95764-1230">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="95764-1230">May 7, 2018</span></span>

<span data-ttu-id="95764-1231">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="95764-1231">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="95764-1232">コア</span><span class="sxs-lookup"><span data-stu-id="95764-1232">Core</span></span>

* <span data-ttu-id="95764-1233">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1233">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="95764-1234">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1234">Added limited support for positional arguments</span></span>
* <span data-ttu-id="95764-1235">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1235">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="95764-1236">#5591</span><span class="sxs-lookup"><span data-stu-id="95764-1236">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="95764-1237">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1237">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="95764-1238">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="95764-1238">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="95764-1239">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1239">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="95764-1240">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1240">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="95764-1241">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1241">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="95764-1242">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-1242">ACR</span></span>

* <span data-ttu-id="95764-1243">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1243">Added ACR Build commands</span></span>
* <span data-ttu-id="95764-1244">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1244">Improved resource not found error messages</span></span>
* <span data-ttu-id="95764-1245">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1245">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="95764-1246">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1246">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="95764-1247">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1247">Improved repository commands error messages</span></span>
* <span data-ttu-id="95764-1248">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-1248">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1249">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1249">ACS</span></span>

* <span data-ttu-id="95764-1250">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1250">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="95764-1251">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1251">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="95764-1252">AMS</span><span class="sxs-lookup"><span data-stu-id="95764-1252">AMS</span></span>

* <span data-ttu-id="95764-1253">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="95764-1253">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1254">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1254">Appservice</span></span>

* <span data-ttu-id="95764-1255">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1255">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="95764-1256">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1256">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="95764-1257">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1257">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="95764-1258">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1258">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="95764-1259">Batch AI</span><span class="sxs-lookup"><span data-stu-id="95764-1259">Batch AI</span></span>

* <span data-ttu-id="95764-1260">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1260">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="95764-1261">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="95764-1261">Cognitive Services</span></span>

* <span data-ttu-id="95764-1262">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1262">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="95764-1263">消費</span><span class="sxs-lookup"><span data-stu-id="95764-1263">Consumption</span></span>

* <span data-ttu-id="95764-1264">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1264">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="95764-1265">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-1265">Container</span></span>

* <span data-ttu-id="95764-1266">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1266">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="95764-1267">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="95764-1267">Cosmos DB</span></span>

* <span data-ttu-id="95764-1268">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="95764-1268">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="95764-1269">DMS</span><span class="sxs-lookup"><span data-stu-id="95764-1269">DMS</span></span>

* <span data-ttu-id="95764-1270">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1270">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="95764-1271">拡張機能</span><span class="sxs-lookup"><span data-stu-id="95764-1271">Extension</span></span>

* <span data-ttu-id="95764-1272">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1272">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="95764-1273">Interactive</span><span class="sxs-lookup"><span data-stu-id="95764-1273">Interactive</span></span>

* <span data-ttu-id="95764-1274">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-1274">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="95764-1275">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="95764-1275">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="95764-1276">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1276">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="95764-1277">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1277">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="95764-1278">ラボ</span><span class="sxs-lookup"><span data-stu-id="95764-1278">Lab</span></span>

* <span data-ttu-id="95764-1279">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1279">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="95764-1280">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1280">Network</span></span>

* <span data-ttu-id="95764-1281">[破壊的変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1281">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="95764-1282">プロファイル</span><span class="sxs-lookup"><span data-stu-id="95764-1282">Profile</span></span>

* <span data-ttu-id="95764-1283">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1283">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="95764-1284">[破壊的変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1284">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="95764-1285">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1285">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="95764-1286">Redis</span><span class="sxs-lookup"><span data-stu-id="95764-1286">Redis</span></span>

* <span data-ttu-id="95764-1287">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1287">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="95764-1288">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="95764-1288">Deprecated `redis list-all`.</span></span> <span data-ttu-id="95764-1289">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="95764-1289">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="95764-1290">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1290">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="95764-1291">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1291">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="95764-1292">Role</span><span class="sxs-lookup"><span data-stu-id="95764-1292">Role</span></span>

* <span data-ttu-id="95764-1293">[破壊的変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1293">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1294">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1294">Storage</span></span>

* <span data-ttu-id="95764-1295">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="95764-1295">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="95764-1296">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="95764-1296">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="95764-1297">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="95764-1297">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="95764-1298">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="95764-1298">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="95764-1299">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1299">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1300">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1300">VM</span></span>

* <span data-ttu-id="95764-1301">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1301">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="95764-1302">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1302">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="95764-1303">[破壊的変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="95764-1303">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="95764-1304">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1304">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="95764-1305">[破壊的変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1305">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="95764-1306">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1306">Added write accelerator support</span></span>
* <span data-ttu-id="95764-1307">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1307">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="95764-1308">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1308">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="95764-1309">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1309">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="95764-1310">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="95764-1310">April 10, 2018</span></span>

<span data-ttu-id="95764-1311">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="95764-1311">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="95764-1312">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-1312">ACR</span></span>

* <span data-ttu-id="95764-1313">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1313">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1314">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1314">ACS</span></span>

* <span data-ttu-id="95764-1315">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1315">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1316">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1316">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="95764-1318">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1318">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="95764-1319">BatchAI</span><span class="sxs-lookup"><span data-stu-id="95764-1319">BatchAI</span></span>

* <span data-ttu-id="95764-1320">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1320">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="95764-1321">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="95764-1321">Job level mounting</span></span>
  - <span data-ttu-id="95764-1322">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="95764-1322">Environment variables with secret values</span></span>
  - <span data-ttu-id="95764-1323">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="95764-1323">Performance counters settings</span></span>
  - <span data-ttu-id="95764-1324">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="95764-1324">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="95764-1325">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="95764-1325">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="95764-1326">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="95764-1326">Usage and limits reporting</span></span>
  - <span data-ttu-id="95764-1327">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="95764-1327">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="95764-1328">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="95764-1328">Support for custom images</span></span>
  - <span data-ttu-id="95764-1329">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1329">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="95764-1330">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="95764-1330">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="95764-1331">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="95764-1331">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="95764-1332">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="95764-1332">National clouds are supported</span></span>
* <span data-ttu-id="95764-1333">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1333">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="95764-1334">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1334">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="95764-1335">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1335">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="95764-1336">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1336">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="95764-1337">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="95764-1337">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="95764-1338">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="95764-1338">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="95764-1339">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1339">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="95764-1340">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1340">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="95764-1341">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="95764-1341">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="95764-1342">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1342">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="95764-1343">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="95764-1343">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="95764-1344">[破壊的変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="95764-1344">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="95764-1345">[破壊的変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1345">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="95764-1346">課金</span><span class="sxs-lookup"><span data-stu-id="95764-1346">Billing</span></span>

* <span data-ttu-id="95764-1347">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1347">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="95764-1348">消費</span><span class="sxs-lookup"><span data-stu-id="95764-1348">Consumption</span></span>

* <span data-ttu-id="95764-1349">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1349">Added `marketplace` commands</span></span>
* <span data-ttu-id="95764-1350">[破壊的変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1350">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="95764-1351">[破壊的変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1351">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="95764-1352">[破壊的変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1352">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="95764-1353">[破壊的変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1353">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="95764-1354">[破壊的変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1354">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="95764-1355">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-1355">Container</span></span>

* <span data-ttu-id="95764-1356">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1356">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="95764-1357">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1357">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="95764-1358">拡張機能</span><span class="sxs-lookup"><span data-stu-id="95764-1358">Extension</span></span>

* <span data-ttu-id="95764-1359">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1359">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="95764-1360">Interactive</span><span class="sxs-lookup"><span data-stu-id="95764-1360">Interactive</span></span>

* <span data-ttu-id="95764-1361">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1361">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="95764-1362">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1362">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="95764-1363">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1363">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="95764-1364">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1364">Network</span></span>

* <span data-ttu-id="95764-1365">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1365">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="95764-1366">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1366">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="95764-1367">#4910</span><span class="sxs-lookup"><span data-stu-id="95764-1367">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="95764-1368">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1368">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="95764-1369">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="95764-1369">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="95764-1370">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1370">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="95764-1371">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1371">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="95764-1372">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1372">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="95764-1373">プロファイル</span><span class="sxs-lookup"><span data-stu-id="95764-1373">Profile</span></span>

* <span data-ttu-id="95764-1374">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1374">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="95764-1375">[破壊的変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1375">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="95764-1376">RDBMS</span><span class="sxs-lookup"><span data-stu-id="95764-1376">RDBMS</span></span>

* <span data-ttu-id="95764-1377">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1377">Added `georestore` command</span></span>
* <span data-ttu-id="95764-1378">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1378">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="95764-1379">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-1379">Resource</span></span>

* <span data-ttu-id="95764-1380">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1380">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="95764-1381">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1381">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="95764-1382">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-1382">SQL</span></span>

* <span data-ttu-id="95764-1383">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1383">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1384">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1384">Storage</span></span>

* <span data-ttu-id="95764-1385">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1385">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1386">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1386">VM</span></span>

* <span data-ttu-id="95764-1387">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1387">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="95764-1388">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1388">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="95764-1390">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1390">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="95764-1391">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1391">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="95764-1392">#5718</span><span class="sxs-lookup"><span data-stu-id="95764-1392">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="95764-1393">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1393">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="95764-1394">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="95764-1394">March 27, 2018</span></span>

<span data-ttu-id="95764-1395">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="95764-1395">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="95764-1396">コア</span><span class="sxs-lookup"><span data-stu-id="95764-1396">Core</span></span>

* <span data-ttu-id="95764-1397">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="95764-1397">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1398">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1398">ACS</span></span>

* <span data-ttu-id="95764-1399">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1399">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1400">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1400">Appservice</span></span>

* <span data-ttu-id="95764-1401">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1401">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="95764-1402">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1402">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="95764-1403">バックアップ</span><span class="sxs-lookup"><span data-stu-id="95764-1403">Backup</span></span>

* <span data-ttu-id="95764-1404">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1404">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="95764-1405">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="95764-1405">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="95764-1406">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1406">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="95764-1407">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1407">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="95764-1408">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-1408">Container</span></span>

* <span data-ttu-id="95764-1409">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1409">Added `container exec` command.</span></span> <span data-ttu-id="95764-1410">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="95764-1410">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="95764-1411">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="95764-1411">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="95764-1412">拡張機能</span><span class="sxs-lookup"><span data-stu-id="95764-1412">Extension</span></span>

* <span data-ttu-id="95764-1413">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1413">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="95764-1414">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1414">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="95764-1415">[破壊的変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1415">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="95764-1416">Interactive</span><span class="sxs-lookup"><span data-stu-id="95764-1416">Interactive</span></span>

* <span data-ttu-id="95764-1417">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1417">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="95764-1418">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1418">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="95764-1419">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="95764-1419">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="95764-1420">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="95764-1420">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="95764-1421">ラボ</span><span class="sxs-lookup"><span data-stu-id="95764-1421">Lab</span></span>

* <span data-ttu-id="95764-1422">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1422">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-1423">監視</span><span class="sxs-lookup"><span data-stu-id="95764-1423">Monitor</span></span>

* <span data-ttu-id="95764-1424">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="95764-1424">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="95764-1425">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="95764-1425">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="95764-1426">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="95764-1426">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="95764-1427">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1427">Network</span></span>

* <span data-ttu-id="95764-1428">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1428">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="95764-1429">プロファイル</span><span class="sxs-lookup"><span data-stu-id="95764-1429">Profile</span></span>

* <span data-ttu-id="95764-1430">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1430">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="95764-1431">RDBMS</span><span class="sxs-lookup"><span data-stu-id="95764-1431">RDBMS</span></span>

* <span data-ttu-id="95764-1432">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1432">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="95764-1433">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-1433">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="95764-1435">Role</span><span class="sxs-lookup"><span data-stu-id="95764-1435">Role</span></span>

* <span data-ttu-id="95764-1436">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1436">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="95764-1437">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1437">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="95764-1438">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1438">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="95764-1439">[破壊的変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1439">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="95764-1440">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1440">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1441">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1441">Storage</span></span>

* <span data-ttu-id="95764-1442">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1442">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="95764-1443">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="95764-1443">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1444">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1444">VM</span></span>

* <span data-ttu-id="95764-1445">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1445">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="95764-1446">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1446">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="95764-1447">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1447">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="95764-1448">[破壊的変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1448">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="95764-1449">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="95764-1449">March 13, 2018</span></span>

<span data-ttu-id="95764-1450">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="95764-1450">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="95764-1451">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-1451">ACR</span></span>

* <span data-ttu-id="95764-1452">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1452">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="95764-1453">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1453">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="95764-1454">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1454">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1455">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1455">ACS</span></span>

* <span data-ttu-id="95764-1456">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1456">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="95764-1457">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1457">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="95764-1458">Advisor</span><span class="sxs-lookup"><span data-stu-id="95764-1458">Advisor</span></span>

* <span data-ttu-id="95764-1459">[破壊的変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1459">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="95764-1460">[破壊的変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1460">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="95764-1461">[破壊的変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1461">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="95764-1462">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1462">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="95764-1463">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1463">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1464">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1464">Appservice</span></span>

* <span data-ttu-id="95764-1465">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1465">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="95764-1466">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1466">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="95764-1467">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="95764-1467">Eventhubs</span></span>

* <span data-ttu-id="95764-1468">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="95764-1468">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="95764-1469">拡張機能</span><span class="sxs-lookup"><span data-stu-id="95764-1469">Extension</span></span>

* <span data-ttu-id="95764-1470">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1470">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="95764-1471">Interactive</span><span class="sxs-lookup"><span data-stu-id="95764-1471">Interactive</span></span>

* <span data-ttu-id="95764-1472">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="95764-1472">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="95764-1473">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="95764-1473">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="95764-1474">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="95764-1474">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="95764-1475">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1475">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-1476">監視</span><span class="sxs-lookup"><span data-stu-id="95764-1476">Monitor</span></span>

* <span data-ttu-id="95764-1477">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1477">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="95764-1478">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1478">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="95764-1479">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1479">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="95764-1480">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1480">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="95764-1481">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1481">Network</span></span>

* <span data-ttu-id="95764-1482">[破壊的変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1482">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="95764-1483">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1483">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="95764-1484">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1484">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="95764-1485">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1485">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="95764-1486">プロファイル</span><span class="sxs-lookup"><span data-stu-id="95764-1486">Profile</span></span>

* <span data-ttu-id="95764-1487">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1487">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="95764-1488">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1488">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="95764-1489">RDBMS</span><span class="sxs-lookup"><span data-stu-id="95764-1489">RDBMS</span></span>

* <span data-ttu-id="95764-1490">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1490">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="95764-1491">Service Bus</span><span class="sxs-lookup"><span data-stu-id="95764-1491">Service Bus</span></span>

* <span data-ttu-id="95764-1492">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="95764-1492">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1493">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1493">Storage</span></span>

* <span data-ttu-id="95764-1494">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-1494">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="95764-1495">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="95764-1495">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1496">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1496">VM</span></span>

* <span data-ttu-id="95764-1497">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1497">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="95764-1498">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1498">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="95764-1499">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1499">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="95764-1500">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1500">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="95764-1501">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="95764-1501">February 27, 2018</span></span>

<span data-ttu-id="95764-1502">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="95764-1502">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="95764-1503">コア</span><span class="sxs-lookup"><span data-stu-id="95764-1503">Core</span></span>

* <span data-ttu-id="95764-1504">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="95764-1504">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="95764-1505">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1505">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="95764-1506">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1506">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1507">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1507">ACS</span></span>

* <span data-ttu-id="95764-1508">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1508">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="95764-1509">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="95764-1509">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="95764-1510">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1510">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="95764-1511">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1511">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1512">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1512">Appservice</span></span>

* <span data-ttu-id="95764-1513">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="95764-1513">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="95764-1514">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="95764-1514">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="95764-1515">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="95764-1515">Cognitive Services</span></span>

* <span data-ttu-id="95764-1516">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-1516">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="95764-1517">消費</span><span class="sxs-lookup"><span data-stu-id="95764-1517">Consumption</span></span>

* <span data-ttu-id="95764-1518">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1518">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="95764-1519">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-1519">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="95764-1520">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-1520">Container</span></span>

* <span data-ttu-id="95764-1521">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1521">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="95764-1522">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1522">Network</span></span>

* <span data-ttu-id="95764-1523">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="95764-1523">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="95764-1524">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-1524">Resource</span></span>

* <span data-ttu-id="95764-1525">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1525">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="95764-1526">Role</span><span class="sxs-lookup"><span data-stu-id="95764-1526">Role</span></span>

* <span data-ttu-id="95764-1527">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1527">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="95764-1528">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-1528">SQL</span></span>

* <span data-ttu-id="95764-1529">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1529">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1530">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1530">Storage</span></span>

* <span data-ttu-id="95764-1531">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1531">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1532">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1532">VM</span></span>

* <span data-ttu-id="95764-1533">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1533">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="95764-1534">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="95764-1534">February 13, 2018</span></span>

<span data-ttu-id="95764-1535">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="95764-1535">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="95764-1536">コア</span><span class="sxs-lookup"><span data-stu-id="95764-1536">Core</span></span>

* <span data-ttu-id="95764-1537">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1537">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1538">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1538">ACS</span></span>

* <span data-ttu-id="95764-1539">[破壊的変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1539">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="95764-1540">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1540">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="95764-1541">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1541">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="95764-1542">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-1542">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="95764-1543">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1543">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="95764-1544">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="95764-1544">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="95764-1545">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1545">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="95764-1546">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="95764-1546">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1547">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1547">Appservice</span></span>

* <span data-ttu-id="95764-1548">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1548">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="95764-1549">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1549">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="95764-1550">CDN</span><span class="sxs-lookup"><span data-stu-id="95764-1550">CDN</span></span>

* <span data-ttu-id="95764-1551">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1551">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="95764-1552">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-1552">Container</span></span>

* <span data-ttu-id="95764-1553">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1553">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="95764-1554">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1554">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="95764-1555">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="95764-1555">CosmosDB</span></span>

* <span data-ttu-id="95764-1556">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1556">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="95764-1557">拡張機能</span><span class="sxs-lookup"><span data-stu-id="95764-1557">Extension</span></span>

* <span data-ttu-id="95764-1558">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1558">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="95764-1559">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1559">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="95764-1560">フィードバック</span><span class="sxs-lookup"><span data-stu-id="95764-1560">Feedback</span></span>

* <span data-ttu-id="95764-1561">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1561">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="95764-1562">Interactive</span><span class="sxs-lookup"><span data-stu-id="95764-1562">Interactive</span></span>

* <span data-ttu-id="95764-1563">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1563">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="95764-1564">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1564">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="95764-1565">IoT</span><span class="sxs-lookup"><span data-stu-id="95764-1565">IoT</span></span>

* <span data-ttu-id="95764-1566">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1566">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="95764-1567">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1567">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="95764-1568">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1568">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="95764-1569">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1569">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-1570">監視</span><span class="sxs-lookup"><span data-stu-id="95764-1570">Monitor</span></span>

* <span data-ttu-id="95764-1571">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1571">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="95764-1572">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1572">Network</span></span>

* <span data-ttu-id="95764-1573">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1573">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="95764-1574">プロファイル</span><span class="sxs-lookup"><span data-stu-id="95764-1574">Profile</span></span>

* <span data-ttu-id="95764-1575">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1575">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="95764-1576">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-1576">Resource</span></span>

* <span data-ttu-id="95764-1577">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1577">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="95764-1578">Role</span><span class="sxs-lookup"><span data-stu-id="95764-1578">Role</span></span>

* <span data-ttu-id="95764-1579">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1579">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="95764-1580">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-1580">SQL</span></span>

* <span data-ttu-id="95764-1581">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1581">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="95764-1582">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1582">Added `sql db rename`</span></span>
* <span data-ttu-id="95764-1583">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1583">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1584">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1584">Storage</span></span>

* <span data-ttu-id="95764-1585">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1585">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1586">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1586">VM</span></span>

* <span data-ttu-id="95764-1587">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1587">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="95764-1588">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1588">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="95764-1589">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="95764-1589">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="95764-1590">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="95764-1590">January 31, 2018</span></span>

<span data-ttu-id="95764-1591">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="95764-1591">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="95764-1592">コア</span><span class="sxs-lookup"><span data-stu-id="95764-1592">Core</span></span>

* <span data-ttu-id="95764-1593">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1593">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="95764-1594">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1594">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="95764-1595">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1595">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="95764-1596">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="95764-1596">Use `--verbose` to see</span></span>
* <span data-ttu-id="95764-1597">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="95764-1597">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1598">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1598">ACS</span></span>

* <span data-ttu-id="95764-1599">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="95764-1599">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="95764-1600">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="95764-1600">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1601">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1601">Appservice</span></span>

* <span data-ttu-id="95764-1602">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="95764-1602">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="95764-1603">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1603">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="95764-1604">CDN</span><span class="sxs-lookup"><span data-stu-id="95764-1604">CDN</span></span>

* <span data-ttu-id="95764-1605">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1605">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="95764-1606">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="95764-1606">CosmosDB</span></span>

* <span data-ttu-id="95764-1607">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1607">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="95764-1608">Interactive</span><span class="sxs-lookup"><span data-stu-id="95764-1608">Interactive</span></span>

* <span data-ttu-id="95764-1609">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1609">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="95764-1610">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1610">Network</span></span>

* <span data-ttu-id="95764-1611">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1611">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="95764-1612">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1612">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="95764-1613">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1613">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="95764-1614">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1614">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="95764-1615">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1615">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="95764-1616">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1616">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="95764-1617">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1617">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="95764-1618">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1618">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="95764-1619">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1619">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="95764-1620">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="95764-1620">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="95764-1621">プロファイル</span><span class="sxs-lookup"><span data-stu-id="95764-1621">Profile</span></span>

* <span data-ttu-id="95764-1622">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1622">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="95764-1623">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-1623">Resource</span></span>

* <span data-ttu-id="95764-1624">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1624">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1625">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1625">Storage</span></span>

* <span data-ttu-id="95764-1626">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1626">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="95764-1627">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1627">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="95764-1628">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1628">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="95764-1629">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1629">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="95764-1630">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1630">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1631">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1631">VM</span></span>

* <span data-ttu-id="95764-1632">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1632">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="95764-1633">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1633">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="95764-1634">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1634">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="95764-1635">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1635">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="95764-1636">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="95764-1636">January 17, 2018</span></span>

<span data-ttu-id="95764-1637">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="95764-1637">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="95764-1638">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-1638">ACR</span></span>

* <span data-ttu-id="95764-1639">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1639">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="95764-1640">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1640">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1641">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1641">ACS</span></span>

* <span data-ttu-id="95764-1642">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1642">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="95764-1643">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1643">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1644">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1644">Appservice</span></span>

* <span data-ttu-id="95764-1645">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1645">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="95764-1646">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1646">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="95764-1647">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1647">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="95764-1648">バックアップ</span><span class="sxs-lookup"><span data-stu-id="95764-1648">Backup</span></span>

* <span data-ttu-id="95764-1649">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1649">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="95764-1650">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1650">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="95764-1651">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1651">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="95764-1652">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1652">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="95764-1653">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1653">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="95764-1654">Batch</span><span class="sxs-lookup"><span data-stu-id="95764-1654">Batch</span></span>

* <span data-ttu-id="95764-1655">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1655">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="95764-1656">クラウド</span><span class="sxs-lookup"><span data-stu-id="95764-1656">Cloud</span></span>

* <span data-ttu-id="95764-1657">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1657">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="95764-1658">消費</span><span class="sxs-lookup"><span data-stu-id="95764-1658">Consumption</span></span>

* <span data-ttu-id="95764-1659">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1659">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="95764-1660">Event Grid</span><span class="sxs-lookup"><span data-stu-id="95764-1660">Event Grid</span></span>

* <span data-ttu-id="95764-1661">[破壊的変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="95764-1661">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="95764-1662">[破壊的変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="95764-1662">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="95764-1663">[破壊的変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1663">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="95764-1664">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="95764-1664">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="95764-1665">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1665">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="95764-1666">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1666">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="95764-1667">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1667">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="95764-1668">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1668">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="95764-1669">Interactive</span><span class="sxs-lookup"><span data-stu-id="95764-1669">Interactive</span></span>

* <span data-ttu-id="95764-1670">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="95764-1670">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="95764-1671">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1671">Fixed errors on startup</span></span>
* <span data-ttu-id="95764-1672">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1672">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="95764-1673">IoT</span><span class="sxs-lookup"><span data-stu-id="95764-1673">IoT</span></span>

* <span data-ttu-id="95764-1674">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1674">Added support for device provisioning service</span></span>
* <span data-ttu-id="95764-1675">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1675">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="95764-1676">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1676">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-1677">監視</span><span class="sxs-lookup"><span data-stu-id="95764-1677">Monitor</span></span>

* <span data-ttu-id="95764-1678">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1678">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="95764-1679">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="95764-1679">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="95764-1680">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1680">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="95764-1681">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1681">Network</span></span>

* <span data-ttu-id="95764-1682">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1682">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="95764-1683">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1683">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="95764-1684">プロファイル</span><span class="sxs-lookup"><span data-stu-id="95764-1684">Profile</span></span>

* <span data-ttu-id="95764-1685">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1685">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="95764-1686">Role</span><span class="sxs-lookup"><span data-stu-id="95764-1686">Role</span></span>

* <span data-ttu-id="95764-1687">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1687">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="95764-1688">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="95764-1688">Service Fabric</span></span>

* <span data-ttu-id="95764-1689">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1689">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="95764-1690">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1690">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1691">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1691">VM</span></span>

* <span data-ttu-id="95764-1692">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="95764-1692">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="95764-1693">[破壊的変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1693">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="95764-1694">[破壊的変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1694">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="95764-1695">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1695">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="95764-1696">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1696">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="95764-1697">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1697">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="95764-1698">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1698">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="95764-1699">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1699">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="95764-1700">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="95764-1700">December 19, 2017</span></span>

<span data-ttu-id="95764-1701">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="95764-1701">Version 2.0.23</span></span>

* <span data-ttu-id="95764-1702">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1702">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="95764-1703">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-1703">Container</span></span>

* <span data-ttu-id="95764-1704">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1704">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="95764-1705">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1705">Network</span></span>

* <span data-ttu-id="95764-1706">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1706">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="95764-1707">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1707">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1708">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1708">Storage</span></span>

* <span data-ttu-id="95764-1709">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1709">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1710">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1710">VM</span></span>

* <span data-ttu-id="95764-1711">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1711">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="95764-1712">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="95764-1712">December 5, 2017</span></span>

<span data-ttu-id="95764-1713">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="95764-1713">Version 2.0.22</span></span>

* <span data-ttu-id="95764-1714">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1714">Removed `az component` commands.</span></span> <span data-ttu-id="95764-1715">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="95764-1715">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="95764-1716">コア</span><span class="sxs-lookup"><span data-stu-id="95764-1716">Core</span></span>
* <span data-ttu-id="95764-1717">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1717">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="95764-1718">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1718">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1719">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1719">ACS</span></span>

* <span data-ttu-id="95764-1720">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1720">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="95764-1721">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1721">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="95764-1722">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1722">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="95764-1723">Advisor</span><span class="sxs-lookup"><span data-stu-id="95764-1723">Advisor</span></span>

* <span data-ttu-id="95764-1724">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="95764-1724">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1725">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1725">Appservice</span></span>

* <span data-ttu-id="95764-1726">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1726">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="95764-1727">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1727">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="95764-1728">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1728">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="95764-1729">消費</span><span class="sxs-lookup"><span data-stu-id="95764-1729">Consumption</span></span>

* <span data-ttu-id="95764-1730">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1730">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="95764-1731">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-1731">Container</span></span>

* <span data-ttu-id="95764-1732">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1732">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-1733">監視</span><span class="sxs-lookup"><span data-stu-id="95764-1733">Monitor</span></span>

* <span data-ttu-id="95764-1734">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1734">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="95764-1735">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-1735">Resource</span></span>

* <span data-ttu-id="95764-1736">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1736">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="95764-1737">Role</span><span class="sxs-lookup"><span data-stu-id="95764-1737">Role</span></span>

* <span data-ttu-id="95764-1738">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1738">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="95764-1739">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="95764-1739">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="95764-1740">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1740">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="95764-1741">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-1741">SQL</span></span>

* <span data-ttu-id="95764-1742">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1742">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="95764-1743">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1743">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1744">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1744">VM</span></span>

* <span data-ttu-id="95764-1745">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1745">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="95764-1746">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="95764-1746">November 14, 2017</span></span>

<span data-ttu-id="95764-1747">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="95764-1747">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="95764-1748">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-1748">ACR</span></span>

* <span data-ttu-id="95764-1749">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1749">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="95764-1750">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1750">ACS</span></span>

* <span data-ttu-id="95764-1751">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1751">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="95764-1752">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1752">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="95764-1753">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1753">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="95764-1754">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1754">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="95764-1755">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1755">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1756">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1756">Appservice</span></span>

* <span data-ttu-id="95764-1757">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1757">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="95764-1758">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1758">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="95764-1759">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1759">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="95764-1760">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-1760">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="95764-1761">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1761">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="95764-1762">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="95764-1762">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="95764-1763">Batch</span><span class="sxs-lookup"><span data-stu-id="95764-1763">Batch</span></span>

* <span data-ttu-id="95764-1764">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1764">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="95764-1765">Batchai</span><span class="sxs-lookup"><span data-stu-id="95764-1765">Batchai</span></span>

* <span data-ttu-id="95764-1766">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1766">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="95764-1767">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1767">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="95764-1768">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1768">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="95764-1769">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1769">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="95764-1770">クラウド</span><span class="sxs-lookup"><span data-stu-id="95764-1770">Cloud</span></span>

* <span data-ttu-id="95764-1771">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1771">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="95764-1772">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-1772">Container</span></span>

* <span data-ttu-id="95764-1773">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1773">Added support to open multiple ports</span></span>
* <span data-ttu-id="95764-1774">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1774">Added container group restart policy</span></span>
* <span data-ttu-id="95764-1775">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1775">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="95764-1776">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-1776">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="95764-1777">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="95764-1777">Data Lake Analytics</span></span>

* <span data-ttu-id="95764-1778">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1778">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="95764-1779">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="95764-1779">Data Lake Store</span></span>

* <span data-ttu-id="95764-1780">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1780">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="95764-1781">拡張機能</span><span class="sxs-lookup"><span data-stu-id="95764-1781">Extension</span></span>

* <span data-ttu-id="95764-1782">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1782">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="95764-1783">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1783">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="95764-1784">IoT</span><span class="sxs-lookup"><span data-stu-id="95764-1784">IoT</span></span>

* <span data-ttu-id="95764-1785">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1785">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-1786">監視</span><span class="sxs-lookup"><span data-stu-id="95764-1786">Monitor</span></span>

* <span data-ttu-id="95764-1787">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1787">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="95764-1788">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1788">Network</span></span>

* <span data-ttu-id="95764-1789">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1789">Added support for CAA DNS records</span></span>
* <span data-ttu-id="95764-1790">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1790">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="95764-1791">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1791">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="95764-1792">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1792">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="95764-1793">Reservations</span><span class="sxs-lookup"><span data-stu-id="95764-1793">Reservations</span></span>

* <span data-ttu-id="95764-1794">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="95764-1794">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="95764-1795">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-1795">Resource</span></span>

* <span data-ttu-id="95764-1796">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1796">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="95764-1797">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-1797">SQL</span></span>

* <span data-ttu-id="95764-1798">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1798">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1799">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1799">Storage</span></span>

* <span data-ttu-id="95764-1800">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1800">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="95764-1801">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1801">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="95764-1802">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1802">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="95764-1803">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1803">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="95764-1804">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1804">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="95764-1805">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1805">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="95764-1806">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1806">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1807">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1807">VM</span></span>

* <span data-ttu-id="95764-1808">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1808">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="95764-1809">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1809">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="95764-1810">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1810">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="95764-1811">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1811">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="95764-1812">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1812">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="95764-1813">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="95764-1813">October 24, 2017</span></span>

<span data-ttu-id="95764-1814">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="95764-1814">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="95764-1815">コア</span><span class="sxs-lookup"><span data-stu-id="95764-1815">Core</span></span>

* <span data-ttu-id="95764-1816">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-1816">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="95764-1817">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-1817">ACR</span></span>

* <span data-ttu-id="95764-1818">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-1818">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="95764-1819">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1819">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="95764-1820">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1820">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1821">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1821">ACS</span></span>

* <span data-ttu-id="95764-1822">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1822">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="95764-1823">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1823">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1824">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1824">Appservice</span></span>

* <span data-ttu-id="95764-1825">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1825">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="95764-1826">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="95764-1826">Component</span></span>

* <span data-ttu-id="95764-1827">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1827">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-1828">監視</span><span class="sxs-lookup"><span data-stu-id="95764-1828">Monitor</span></span>

* <span data-ttu-id="95764-1829">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1829">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="95764-1830">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-1830">Resource</span></span>

* <span data-ttu-id="95764-1831">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1831">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="95764-1832">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1832">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1833">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1833">VM</span></span>

* <span data-ttu-id="95764-1834">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1834">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="95764-1835">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="95764-1835">October 9, 2017</span></span>

<span data-ttu-id="95764-1836">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="95764-1836">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="95764-1837">コア</span><span class="sxs-lookup"><span data-stu-id="95764-1837">Core</span></span>

* <span data-ttu-id="95764-1838">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1838">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1839">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1839">Appservice</span></span>

* <span data-ttu-id="95764-1840">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1840">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="95764-1841">Batch</span><span class="sxs-lookup"><span data-stu-id="95764-1841">Batch</span></span>

* <span data-ttu-id="95764-1842">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-1842">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="95764-1843">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-1843">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="95764-1844">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1844">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="95764-1845">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1845">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="95764-1846">Batchai</span><span class="sxs-lookup"><span data-stu-id="95764-1846">Batchai</span></span>

* <span data-ttu-id="95764-1847">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="95764-1847">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="95764-1848">KeyVault</span><span class="sxs-lookup"><span data-stu-id="95764-1848">Keyvault</span></span>

* <span data-ttu-id="95764-1849">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1849">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="95764-1850">(#4448)</span><span class="sxs-lookup"><span data-stu-id="95764-1850">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="95764-1851">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1851">Network</span></span>

* <span data-ttu-id="95764-1852">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1852">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="95764-1853">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-1853">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="95764-1854">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-1854">Resource</span></span>

* <span data-ttu-id="95764-1855">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1855">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="95764-1856">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1856">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="95764-1857">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1857">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="95764-1858">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1858">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="95764-1859">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-1859">Sql</span></span>

* <span data-ttu-id="95764-1860">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1860">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="95764-1861">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="95764-1861">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="95764-1862">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="95764-1862">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1863">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1863">Storage</span></span>

* <span data-ttu-id="95764-1864">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1864">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1865">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1865">Vm</span></span>

* <span data-ttu-id="95764-1866">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1866">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="95764-1867">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1867">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="95764-1868">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1868">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="95764-1869">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1869">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="95764-1870">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1870">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="95764-1871">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="95764-1871">September 22, 2017</span></span>

<span data-ttu-id="95764-1872">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="95764-1872">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="95764-1873">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-1873">Resource</span></span>

* <span data-ttu-id="95764-1874">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1874">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="95764-1875">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1875">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="95764-1876">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1876">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="95764-1877">[破壊的変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1877">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="95764-1878">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1878">Network</span></span>

* <span data-ttu-id="95764-1879">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1879">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="95764-1880">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1880">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="95764-1881">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1881">Added `asg` application security group commands</span></span>
* <span data-ttu-id="95764-1882">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1882">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="95764-1883">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1883">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="95764-1884">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1884">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="95764-1885">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1885">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1886">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1886">Storage</span></span>

* <span data-ttu-id="95764-1887">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1887">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="95764-1888">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="95764-1888">Eventgrid</span></span>

* <span data-ttu-id="95764-1889">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-1889">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="95764-1890">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-1890">SQL</span></span>

* <span data-ttu-id="95764-1891">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1891">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="95764-1892">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="95764-1892">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="95764-1893">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1893">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="95764-1894">KeyVault</span><span class="sxs-lookup"><span data-stu-id="95764-1894">Keyvault</span></span>

* <span data-ttu-id="95764-1895">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1895">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1896">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1896">VM</span></span>

* <span data-ttu-id="95764-1897">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1897">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="95764-1898">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1898">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="95764-1899">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1899">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="95764-1900">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1900">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="95764-1901">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1901">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="95764-1902">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1902">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1903">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1903">ACS</span></span>

* <span data-ttu-id="95764-1904">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1904">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1905">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1905">Appservice</span></span>

* <span data-ttu-id="95764-1906">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1906">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="95764-1907">バックアップ</span><span class="sxs-lookup"><span data-stu-id="95764-1907">Backup</span></span>

* <span data-ttu-id="95764-1908">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="95764-1908">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="95764-1909">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="95764-1909">September 11, 2017</span></span>

<span data-ttu-id="95764-1910">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="95764-1910">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="95764-1911">コア</span><span class="sxs-lookup"><span data-stu-id="95764-1911">Core</span></span>

* <span data-ttu-id="95764-1912">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1912">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="95764-1913">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1913">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1914">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1914">Acs</span></span>

* <span data-ttu-id="95764-1915">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1915">Added `acs list-locations` command</span></span>
* <span data-ttu-id="95764-1916">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="95764-1916">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1917">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1917">Appservice</span></span>

* <span data-ttu-id="95764-1918">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1918">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="95764-1919">CDN</span><span class="sxs-lookup"><span data-stu-id="95764-1919">CDN</span></span>

* <span data-ttu-id="95764-1920">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1920">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="95764-1921">拡張機能</span><span class="sxs-lookup"><span data-stu-id="95764-1921">Extension</span></span>

* <span data-ttu-id="95764-1922">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="95764-1922">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="95764-1923">KeyVault</span><span class="sxs-lookup"><span data-stu-id="95764-1923">Keyvault</span></span>

* <span data-ttu-id="95764-1924">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1924">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="95764-1925">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1925">Network</span></span>

* <span data-ttu-id="95764-1926">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1926">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="95764-1927">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1927">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="95764-1928">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1928">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="95764-1929">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1929">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="95764-1930">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1930">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="95764-1931">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-1931">Resource</span></span>

* <span data-ttu-id="95764-1932">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="95764-1932">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="95764-1933">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="95764-1933">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="95764-1934">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="95764-1934">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="95764-1935">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="95764-1935">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="95764-1936">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-1936">SQL</span></span>

* <span data-ttu-id="95764-1937">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1937">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1938">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1938">VM</span></span>

* <span data-ttu-id="95764-1939">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="95764-1939">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="95764-1940">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="95764-1940">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="95764-1941">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1941">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="95764-1942">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="95764-1942">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="95764-1943">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="95764-1943">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="95764-1944">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="95764-1944">August 31, 2017</span></span>

<span data-ttu-id="95764-1945">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="95764-1945">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="95764-1946">KeyVault</span><span class="sxs-lookup"><span data-stu-id="95764-1946">Keyvault</span></span>

* <span data-ttu-id="95764-1947">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1947">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="95764-1948">SF</span><span class="sxs-lookup"><span data-stu-id="95764-1948">Sf</span></span>

* <span data-ttu-id="95764-1949">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="95764-1949">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1950">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1950">Storage</span></span>

* <span data-ttu-id="95764-1951">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1951">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="95764-1952">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="95764-1952">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="95764-1953">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="95764-1953">August 28, 2017</span></span>

<span data-ttu-id="95764-1954">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="95764-1954">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="95764-1955">CLI</span><span class="sxs-lookup"><span data-stu-id="95764-1955">CLI</span></span>

* <span data-ttu-id="95764-1956">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1956">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1957">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1957">ACS</span></span>

* <span data-ttu-id="95764-1958">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1958">Corrected preview regions</span></span>
* <span data-ttu-id="95764-1959">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1959">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="95764-1960">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="95764-1960">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-1961">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-1961">Appservice</span></span>

* <span data-ttu-id="95764-1962">[破壊的変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1962">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="95764-1963">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1963">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="95764-1964">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="95764-1964">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="95764-1965">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="95764-1965">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="95764-1966">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="95764-1966">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="95764-1967">IoT</span><span class="sxs-lookup"><span data-stu-id="95764-1967">IoT</span></span>

* <span data-ttu-id="95764-1968">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="95764-1968">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="95764-1969">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-1969">Network</span></span>

* <span data-ttu-id="95764-1970">[破壊的変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1970">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="95764-1971">[破壊的変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1971">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="95764-1972">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1972">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="95764-1973">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1973">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="95764-1974">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1974">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="95764-1975">プロファイル</span><span class="sxs-lookup"><span data-stu-id="95764-1975">Profile</span></span>

* <span data-ttu-id="95764-1976">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="95764-1976">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="95764-1977">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="95764-1977">Service Fabric</span></span>

* <span data-ttu-id="95764-1978">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="95764-1978">Preview release</span></span>
* <span data-ttu-id="95764-1979">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="95764-1979">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="95764-1980">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1980">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="95764-1981">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1981">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="95764-1982">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-1982">Storage</span></span>

* <span data-ttu-id="95764-1983">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1983">Enabled setting blob tier</span></span>
* <span data-ttu-id="95764-1984">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1984">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="95764-1985">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-1985">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="95764-1986">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="95764-1986">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="95764-1987">[破壊的変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-1987">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="95764-1988">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="95764-1988">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="95764-1989">VM</span><span class="sxs-lookup"><span data-stu-id="95764-1989">VM</span></span>

* <span data-ttu-id="95764-1990">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1990">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="95764-1991">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-1991">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="95764-1992">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-1992">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="95764-1993">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1993">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="95764-1994">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1994">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="95764-1995">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1995">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="95764-1996">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="95764-1996">August 15, 2017</span></span>

<span data-ttu-id="95764-1997">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="95764-1997">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="95764-1998">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-1998">ACS</span></span>

* <span data-ttu-id="95764-1999">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-1999">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-2000">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-2000">Appservice</span></span>

* <span data-ttu-id="95764-2001">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2001">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="95764-2002">Event Grid</span><span class="sxs-lookup"><span data-stu-id="95764-2002">Event Grid</span></span>

* <span data-ttu-id="95764-2003">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2003">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="95764-2004">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="95764-2004">August 11, 2017</span></span>

<span data-ttu-id="95764-2005">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="95764-2005">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="95764-2006">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-2006">ACS</span></span>

* <span data-ttu-id="95764-2007">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2007">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="95764-2008">Batch</span><span class="sxs-lookup"><span data-stu-id="95764-2008">Batch</span></span>

* <span data-ttu-id="95764-2009">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="95764-2009">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="95764-2010">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2010">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="95764-2011">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2011">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="95764-2012">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2012">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="95764-2013">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2013">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="95764-2014">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2014">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="95764-2015">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="95764-2015">Component</span></span>

* <span data-ttu-id="95764-2016">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2016">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="95764-2017">コンテナー</span><span class="sxs-lookup"><span data-stu-id="95764-2017">Container</span></span>

* <span data-ttu-id="95764-2018">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2018">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="95764-2019">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="95764-2019">Data Lake Store</span></span>

* <span data-ttu-id="95764-2020">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="95764-2020">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="95764-2021">Event Grid</span><span class="sxs-lookup"><span data-stu-id="95764-2021">Event Grid</span></span>

* <span data-ttu-id="95764-2022">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="95764-2022">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="95764-2023">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-2023">Network</span></span>

* <span data-ttu-id="95764-2024">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2024">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="95764-2025">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2025">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="95764-2026">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2026">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="95764-2027">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2027">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="95764-2028">プロファイル</span><span class="sxs-lookup"><span data-stu-id="95764-2028">Profile</span></span>

* <span data-ttu-id="95764-2029">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2029">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="95764-2030">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-2030">Storage</span></span>

* <span data-ttu-id="95764-2031">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="95764-2031">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="95764-2032">VM</span><span class="sxs-lookup"><span data-stu-id="95764-2032">VM</span></span>

* <span data-ttu-id="95764-2033">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="95764-2033">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="95764-2034">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="95764-2034">Exposed `list-skus` command</span></span>
* <span data-ttu-id="95764-2035">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2035">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="95764-2036">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="95764-2036">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="95764-2037">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-2037">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="95764-2038">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="95764-2038">July 28, 2017</span></span>

<span data-ttu-id="95764-2039">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="95764-2039">Version 2.0.12</span></span>

* <span data-ttu-id="95764-2040">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2040">Added container commands</span></span>
* <span data-ttu-id="95764-2041">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2041">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="95764-2042">コア</span><span class="sxs-lookup"><span data-stu-id="95764-2042">Core</span></span>

* <span data-ttu-id="95764-2043">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="95764-2043">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="95764-2044">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2044">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="95764-2045">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="95764-2045">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="95764-2046">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="95764-2046">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="95764-2047">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="95764-2047">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="95764-2048">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="95764-2048">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="95764-2049">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="95764-2049">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="95764-2050">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="95764-2050">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="95764-2051">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="95764-2051">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="95764-2052">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="95764-2052">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="95764-2053">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="95764-2053">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="95764-2054">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="95764-2054">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="95764-2055">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="95764-2055">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="95764-2056">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="95764-2056">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="95764-2057">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2057">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="95764-2058">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="95764-2058">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="95764-2059">ACR</span><span class="sxs-lookup"><span data-stu-id="95764-2059">ACR</span></span>

* <span data-ttu-id="95764-2060">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2060">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="95764-2061">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2061">Support SKU update for managed registries</span></span>
* <span data-ttu-id="95764-2062">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2062">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="95764-2063">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2063">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="95764-2064">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2064">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="95764-2065">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2065">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="95764-2066">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-2066">ACS</span></span>

* <span data-ttu-id="95764-2067">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2067">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-2068">Appservice</span><span class="sxs-lookup"><span data-stu-id="95764-2068">Appservice</span></span>

* <span data-ttu-id="95764-2069">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2069">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="95764-2070">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2070">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="95764-2071">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="95764-2071">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="95764-2072">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="95764-2072">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="95764-2073">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="95764-2073">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="95764-2074">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="95764-2074">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="95764-2075">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="95764-2075">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="95764-2076">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="95764-2076">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="95764-2077">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="95764-2077">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="95764-2078">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="95764-2078">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="95764-2079">Batch</span><span class="sxs-lookup"><span data-stu-id="95764-2079">Batch</span></span>

* <span data-ttu-id="95764-2080">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="95764-2080">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="95764-2081">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-2081">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="95764-2082">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2082">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="95764-2083">CDN</span><span class="sxs-lookup"><span data-stu-id="95764-2083">CDN</span></span>

* <span data-ttu-id="95764-2084">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-2084">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="95764-2085">クラウド</span><span class="sxs-lookup"><span data-stu-id="95764-2085">Cloud</span></span>

* <span data-ttu-id="95764-2086">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-2086">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="95764-2087">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="95764-2087">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="95764-2088">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2088">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="95764-2089">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="95764-2089">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="95764-2090">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="95764-2090">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="95764-2091">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="95764-2091">CosmosDB</span></span>

* <span data-ttu-id="95764-2092">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2092">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="95764-2093">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2093">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="95764-2094">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="95764-2094">Data Lake Analytics</span></span>

* <span data-ttu-id="95764-2095">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2095">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="95764-2096">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2096">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="95764-2097">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2097">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="95764-2098">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="95764-2098">Data Lake Store</span></span>

* <span data-ttu-id="95764-2099">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2099">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="95764-2100">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="95764-2100">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="95764-2101">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-2101">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="95764-2102">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="95764-2102">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="95764-2103">対話</span><span class="sxs-lookup"><span data-stu-id="95764-2103">Interactive</span></span>

* <span data-ttu-id="95764-2104">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="95764-2104">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="95764-2105">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="95764-2105">Increased test coverage</span></span>
* <span data-ttu-id="95764-2106">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="95764-2106">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="95764-2107">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="95764-2107">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="95764-2108">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="95764-2108">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="95764-2109">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="95764-2109">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="95764-2110">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="95764-2110">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="95764-2111">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2111">Added `--progress` flag</span></span>
* <span data-ttu-id="95764-2112">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-2112">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="95764-2113">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="95764-2113">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="95764-2114">IoT</span><span class="sxs-lookup"><span data-stu-id="95764-2114">IoT</span></span>

* <span data-ttu-id="95764-2115">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="95764-2115">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="95764-2116">(#3934)</span><span class="sxs-lookup"><span data-stu-id="95764-2116">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="95764-2117">Key Vault</span><span class="sxs-lookup"><span data-stu-id="95764-2117">Key vault</span></span>

* <span data-ttu-id="95764-2118">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="95764-2118">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="95764-2119">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="95764-2119">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="95764-2120">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="95764-2120">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="95764-2121">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="95764-2121">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="95764-2122">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="95764-2122">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="95764-2123">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="95764-2123">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="95764-2124">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="95764-2124">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="95764-2125">(#3307)</span><span class="sxs-lookup"><span data-stu-id="95764-2125">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="95764-2126">ラボ</span><span class="sxs-lookup"><span data-stu-id="95764-2126">Lab</span></span>

* <span data-ttu-id="95764-2127">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2127">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="95764-2128">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2128">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-2129">監視</span><span class="sxs-lookup"><span data-stu-id="95764-2129">Monitor</span></span>

* <span data-ttu-id="95764-2130">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="95764-2130">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="95764-2131">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-2131">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="95764-2132">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-2132">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="95764-2133">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-2133">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="95764-2134">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="95764-2134">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="95764-2135">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="95764-2135">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="95764-2136">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="95764-2136">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="95764-2137">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="95764-2137">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="95764-2138">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="95764-2138">`location` no longer required</span></span>
  * <span data-ttu-id="95764-2139">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="95764-2139">Add name and ID support for target</span></span>
  * <span data-ttu-id="95764-2140">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="95764-2140">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="95764-2141">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="95764-2141">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="95764-2142">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2142">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="95764-2143">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="95764-2143">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="95764-2144">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2144">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="95764-2145">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2145">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="95764-2146">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-2146">Network</span></span>

* <span data-ttu-id="95764-2147">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2147">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="95764-2148">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2148">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="95764-2149">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2149">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="95764-2150">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2150">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="95764-2151">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2151">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="95764-2152">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2152">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="95764-2153">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2153">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="95764-2154">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2154">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="95764-2155">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2155">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="95764-2156">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2156">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="95764-2157">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2157">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="95764-2158">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2158">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="95764-2159">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2159">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="95764-2160">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2160">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="95764-2161">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2161">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="95764-2162">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-2162">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="95764-2163">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2163">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="95764-2164">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2164">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="95764-2165">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2165">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="95764-2166">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2166">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="95764-2167">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2167">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="95764-2168">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2168">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="95764-2169">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-2169">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="95764-2170">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="95764-2170">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="95764-2171">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="95764-2171">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="95764-2172">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="95764-2172">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="95764-2173">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="95764-2173">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="95764-2174">プロファイル</span><span class="sxs-lookup"><span data-stu-id="95764-2174">Profile</span></span>

* <span data-ttu-id="95764-2175">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2175">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="95764-2176">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2176">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="95764-2177">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="95764-2177">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="95764-2178">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2178">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="95764-2179">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2179">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="95764-2180">RDBMS</span><span class="sxs-lookup"><span data-stu-id="95764-2180">RDBMS</span></span>

* <span data-ttu-id="95764-2181">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="95764-2181">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="95764-2182">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="95764-2182">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="95764-2183">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="95764-2183">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="95764-2184">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="95764-2184">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="95764-2185">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-2185">Resource</span></span>

* <span data-ttu-id="95764-2186">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-2186">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="95764-2187">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="95764-2187">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="95764-2188">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2188">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="95764-2189">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2189">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="95764-2190">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="95764-2190">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="95764-2191">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2191">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="95764-2192">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="95764-2192">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="95764-2193">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2193">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="95764-2194">Role</span><span class="sxs-lookup"><span data-stu-id="95764-2194">Role</span></span>

* <span data-ttu-id="95764-2195">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2195">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="95764-2196">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="95764-2196">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="95764-2197">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="95764-2197">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="95764-2198">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="95764-2198">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="95764-2199">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2199">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="95764-2200">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="95764-2200">Service Fabric</span></span>
* <span data-ttu-id="95764-2201">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="95764-2201">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="95764-2202">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="95764-2202">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="95764-2203">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="95764-2203">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="95764-2204">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-2204">SQL</span></span>

* <span data-ttu-id="95764-2205">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-2205">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="95764-2206">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="95764-2206">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="95764-2207">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="95764-2207">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="95764-2208">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-2208">Storage</span></span>

* <span data-ttu-id="95764-2209">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="95764-2209">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="95764-2210">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="95764-2210">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="95764-2211">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="95764-2211">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="95764-2212">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="95764-2212">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="95764-2213">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="95764-2213">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="95764-2214">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="95764-2214">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="95764-2215">VM</span><span class="sxs-lookup"><span data-stu-id="95764-2215">VM</span></span>

* <span data-ttu-id="95764-2216">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2216">Support configuring nsg</span></span>
* <span data-ttu-id="95764-2217">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2217">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="95764-2218">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="95764-2218">Support managed service identities</span></span>
* <span data-ttu-id="95764-2219">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2219">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="95764-2220">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="95764-2220">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="95764-2221">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="95764-2221">May 10, 2017</span></span>

<span data-ttu-id="95764-2222">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="95764-2222">Version 2.0.6</span></span>

* <span data-ttu-id="95764-2223">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="95764-2223">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="95764-2224">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-2224">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="95764-2225">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-2225">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="95764-2226">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-2226">Include Cognitive Services module</span></span>
* <span data-ttu-id="95764-2227">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-2227">Include Service Fabric module</span></span>
* <span data-ttu-id="95764-2228">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="95764-2228">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="95764-2229">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2229">Add support for CDN commands</span></span>
* <span data-ttu-id="95764-2230">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="95764-2230">Remove Container module</span></span>
* <span data-ttu-id="95764-2231">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="95764-2231">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="95764-2232">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="95764-2232">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="95764-2233">コア</span><span class="sxs-lookup"><span data-stu-id="95764-2233">Core</span></span>

* <span data-ttu-id="95764-2234">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="95764-2234">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="95764-2235">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="95764-2235">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="95764-2236">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="95764-2236">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="95764-2237">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="95764-2237">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="95764-2238">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="95764-2238">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="95764-2239">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="95764-2239">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="95764-2240">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="95764-2240">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="95764-2241">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="95764-2241">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="95764-2242">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="95764-2242">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="95764-2243">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="95764-2243">core: Improved performance</span></span>
* <span data-ttu-id="95764-2244">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="95764-2244">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="95764-2245">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="95764-2245">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="95764-2246">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-2246">ACS</span></span>

* <span data-ttu-id="95764-2247">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="95764-2247">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="95764-2248">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="95764-2248">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="95764-2249">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="95764-2249">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="95764-2250">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="95764-2250">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-2251">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-2251">AppService</span></span>

* <span data-ttu-id="95764-2252">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2252">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="95764-2253">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-2253">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="95764-2254">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="95764-2254">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="95764-2255">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="95764-2255">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="95764-2256">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="95764-2256">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="95764-2257">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="95764-2257">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="95764-2258">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="95764-2258">support slot swap with preview</span></span>
* <span data-ttu-id="95764-2259">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="95764-2259">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="95764-2260">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="95764-2260">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="95764-2261">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="95764-2261">CosmosDB</span></span>

* <span data-ttu-id="95764-2262">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="95764-2262">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="95764-2263">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2263">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="95764-2264">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2264">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="95764-2265">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2265">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="95764-2266">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="95764-2266">Data Lake Analytics</span></span>

* <span data-ttu-id="95764-2267">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="95764-2267">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="95764-2268">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="95764-2268">Add support for new catalog item type: package.</span></span> <span data-ttu-id="95764-2269">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="95764-2269">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="95764-2270">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="95764-2270">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="95764-2271">テーブル</span><span class="sxs-lookup"><span data-stu-id="95764-2271">Table</span></span>
  * <span data-ttu-id="95764-2272">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="95764-2272">Table valued function</span></span>
  * <span data-ttu-id="95764-2273">表示</span><span class="sxs-lookup"><span data-stu-id="95764-2273">View</span></span>
  * <span data-ttu-id="95764-2274">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="95764-2274">Table Statistics.</span></span> <span data-ttu-id="95764-2275">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="95764-2275">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="95764-2276">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="95764-2276">Data Lake Store</span></span>

* <span data-ttu-id="95764-2277">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="95764-2277">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="95764-2278">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="95764-2278">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="95764-2279">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="95764-2279">missed help for access show.</span></span> <span data-ttu-id="95764-2280">追加しました </span><span class="sxs-lookup"><span data-stu-id="95764-2280">adding it.</span></span> <span data-ttu-id="95764-2281">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="95764-2281">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="95764-2282">検索</span><span class="sxs-lookup"><span data-stu-id="95764-2282">Find</span></span>

* <span data-ttu-id="95764-2283">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="95764-2283">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="95764-2284">KeyVault</span><span class="sxs-lookup"><span data-stu-id="95764-2284">KeyVault</span></span>

* <span data-ttu-id="95764-2285">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="95764-2285">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="95764-2286">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="95764-2286">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="95764-2287">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="95764-2287">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="95764-2288">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="95764-2288">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="95764-2289">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="95764-2289">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="95764-2290">ラボ</span><span class="sxs-lookup"><span data-stu-id="95764-2290">Lab</span></span>

* <span data-ttu-id="95764-2291">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-2291">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="95764-2292">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-2292">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="95764-2293">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-2293">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="95764-2294">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-2294">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="95764-2295">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-2295">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="95764-2296">監視</span><span class="sxs-lookup"><span data-stu-id="95764-2296">Monitor</span></span>

* <span data-ttu-id="95764-2297">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="95764-2297">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="95764-2298">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="95764-2298">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="95764-2299">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-2299">Network</span></span>

* <span data-ttu-id="95764-2300">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-2300">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="95764-2301">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2301">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="95764-2302">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2302">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="95764-2303">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2303">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="95764-2304">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2304">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="95764-2305">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2305">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="95764-2306">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2306">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="95764-2307">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2307">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="95764-2308">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="95764-2308">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="95764-2309">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2309">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="95764-2310">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="95764-2310">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="95764-2311">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="95764-2311">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="95764-2312">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="95764-2312">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="95764-2313">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="95764-2313">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="95764-2314">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="95764-2314">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="95764-2315">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-2315">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="95764-2316">プロファイル</span><span class="sxs-lookup"><span data-stu-id="95764-2316">Profile</span></span>

* <span data-ttu-id="95764-2317">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="95764-2317">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="95764-2318">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="95764-2318">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="95764-2319">Redis</span><span class="sxs-lookup"><span data-stu-id="95764-2319">Redis</span></span>

* <span data-ttu-id="95764-2320">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-2320">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="95764-2321">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="95764-2321">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="95764-2322">Resource</span><span class="sxs-lookup"><span data-stu-id="95764-2322">Resource</span></span>

* <span data-ttu-id="95764-2323">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="95764-2323">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="95764-2324">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="95764-2324">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="95764-2325">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="95764-2325">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="95764-2326">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="95764-2326">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="95764-2327">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="95764-2327">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="95764-2328">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="95764-2328">Add docs for az lock update.</span></span> <span data-ttu-id="95764-2329">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="95764-2329">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="95764-2330">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="95764-2330">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="95764-2331">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="95764-2331">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="95764-2332">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="95764-2332">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="95764-2333">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="95764-2333">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="95764-2334">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="95764-2334">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="95764-2335">Role</span><span class="sxs-lookup"><span data-stu-id="95764-2335">Role</span></span>

* <span data-ttu-id="95764-2336">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="95764-2336">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="95764-2337">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="95764-2337">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="95764-2338">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="95764-2338">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="95764-2339">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="95764-2339">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="95764-2340">SQL</span><span class="sxs-lookup"><span data-stu-id="95764-2340">SQL</span></span>

* <span data-ttu-id="95764-2341">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="95764-2341">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="95764-2342">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="95764-2342">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="95764-2343">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-2343">Storage</span></span>

* <span data-ttu-id="95764-2344">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="95764-2344">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="95764-2345">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2345">Add support for incremental blob copy</span></span>
* <span data-ttu-id="95764-2346">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="95764-2346">Add support for large block blob upload</span></span>
* <span data-ttu-id="95764-2347">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="95764-2347">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="95764-2348">VM</span><span class="sxs-lookup"><span data-stu-id="95764-2348">VM</span></span>

* <span data-ttu-id="95764-2349">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="95764-2349">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="95764-2350">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="95764-2350">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="95764-2351">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="95764-2351">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="95764-2352">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="95764-2352">az vm/vmss disk</span></span>
  3. <span data-ttu-id="95764-2353">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="95764-2353">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="95764-2354">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="95764-2354">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="95764-2355">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="95764-2355">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="95764-2356">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="95764-2356">April 3, 2017</span></span>

<span data-ttu-id="95764-2357">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="95764-2357">Version 2.0.2</span></span>

<span data-ttu-id="95764-2358">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="95764-2358">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="95764-2359">コア</span><span class="sxs-lookup"><span data-stu-id="95764-2359">Core</span></span>

* <span data-ttu-id="95764-2360">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="95764-2360">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="95764-2361">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="95764-2361">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="95764-2362">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="95764-2362">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="95764-2363">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="95764-2363">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="95764-2364">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="95764-2364">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="95764-2365">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="95764-2365">Add prompting for missing template parameters.</span></span> <span data-ttu-id="95764-2366">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="95764-2366">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="95764-2367">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="95764-2367">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="95764-2368">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="95764-2368">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="95764-2369">ACS</span><span class="sxs-lookup"><span data-stu-id="95764-2369">ACS</span></span>

* <span data-ttu-id="95764-2370">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="95764-2370">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="95764-2371">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="95764-2371">Add support for ssh key password prompting.</span></span> <span data-ttu-id="95764-2372">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="95764-2372">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="95764-2373">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="95764-2373">Add support for windows clusters.</span></span> <span data-ttu-id="95764-2374">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="95764-2374">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="95764-2375">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="95764-2375">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="95764-2376">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="95764-2376">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="95764-2377">AppService</span><span class="sxs-lookup"><span data-stu-id="95764-2377">AppService</span></span>

* <span data-ttu-id="95764-2378">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="95764-2378">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="95764-2379">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="95764-2379">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="95764-2380">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="95764-2380">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="95764-2381">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="95764-2381">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="95764-2382">DataLake</span><span class="sxs-lookup"><span data-stu-id="95764-2382">DataLake</span></span>

* <span data-ttu-id="95764-2383">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="95764-2383">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="95764-2384">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="95764-2384">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="95764-2385">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="95764-2385">DocuemntDB</span></span>

* <span data-ttu-id="95764-2386">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="95764-2386">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="95764-2387">VM</span><span class="sxs-lookup"><span data-stu-id="95764-2387">VM</span></span>

* <span data-ttu-id="95764-2388">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="95764-2388">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="95764-2389">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="95764-2389">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="95764-2390">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="95764-2390">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="95764-2391">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="95764-2391">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="95764-2392">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="95764-2392">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="95764-2393">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="95764-2393">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="95764-2394">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="95764-2394">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="95764-2395">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="95764-2395">February 27, 2017</span></span>

<span data-ttu-id="95764-2396">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="95764-2396">Version 2.0.0</span></span>

<span data-ttu-id="95764-2397">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="95764-2397">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="95764-2398">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="95764-2398">Container Service (acs)</span></span>
- <span data-ttu-id="95764-2399">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="95764-2399">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="95764-2400">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="95764-2400">Networking</span></span>
- <span data-ttu-id="95764-2401">Storage</span><span class="sxs-lookup"><span data-stu-id="95764-2401">Storage</span></span>

<span data-ttu-id="95764-2402">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="95764-2402">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="95764-2403">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="95764-2403">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="95764-2404">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="95764-2404">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="95764-2405">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="95764-2405">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="95764-2406">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="95764-2406">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="95764-2407">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="95764-2407">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="95764-2408">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="95764-2408">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="95764-2409">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="95764-2409">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="95764-2410">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="95764-2410">Provide feedback from the command line with the `az feedback` command</span></span>

