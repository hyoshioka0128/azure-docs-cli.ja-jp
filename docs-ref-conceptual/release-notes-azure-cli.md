---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 04/09/2019
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: df665565130322504c4794462098980b1064a6c7
ms.sourcegitcommit: c6dff58438d256647d4aa29a53eef4bf93a0cd24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/11/2019
ms.locfileid: "59479999"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="a3b3e-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="a3b3e-103">Azure CLI release notes</span></span>
## <a name="april-9-2019"></a><span data-ttu-id="a3b3e-104">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-104">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-105">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-105">Core</span></span>
* <span data-ttu-id="a3b3e-106">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-106">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-107">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-107">ACR</span></span>
* <span data-ttu-id="a3b3e-108">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-108">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="a3b3e-109">AMS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-109">AMS</span></span>
* [<span data-ttu-id="a3b3e-110">非推奨</span><span class="sxs-lookup"><span data-stu-id="a3b3e-110">DEPRECATED</span></span>]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [<span data-ttu-id="a3b3e-111">破壊的変更</span><span class="sxs-lookup"><span data-stu-id="a3b3e-111">BREAKING CHANGE</span></span>]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="a3b3e-112">新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-112">Added new encryption parameters support in</span></span> `ams streaming-policy create`
* <span data-ttu-id="a3b3e-113">新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-113">Added new paramter `--filters` to</span></span> `ams streaming-locator create`

### <a name="appservice"></a><span data-ttu-id="a3b3e-114">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-114">AppService</span></span>
* <span data-ttu-id="a3b3e-115">`--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-115">Added `--logs` support to</span></span> `webapp up`
* <span data-ttu-id="a3b3e-116">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-116">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="a3b3e-117">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-117">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="a3b3e-118">[破壊的変更] `devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-118">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="a3b3e-119">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-119">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="a3b3e-120">関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-120">Added ability to switch a plan underneath a function app using</span></span> `functionapp update --plan`
* <span data-ttu-id="a3b3e-121">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-121">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="a3b3e-122">CDN</span><span class="sxs-lookup"><span data-stu-id="a3b3e-122">CDN</span></span>
* <span data-ttu-id="a3b3e-123">`Microsoft_Standard` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-123">Added support for `Microsoft_Standard` and</span></span> `Standard_ChinaCdn`

### <a name="feedback"></a><span data-ttu-id="a3b3e-124">フィードバック</span><span class="sxs-lookup"><span data-stu-id="a3b3e-124">Feedback</span></span>
* <span data-ttu-id="a3b3e-125">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-125">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="a3b3e-126">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-126">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="a3b3e-127">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-127">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="a3b3e-128">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-128">Monitor</span></span>
* <span data-ttu-id="a3b3e-129">"Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-129">Fixed issue where "count" was not a permitted value with</span></span> `metrics alert [create|update]` 

### <a name="network"></a><span data-ttu-id="a3b3e-130">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-130">Network</span></span>
* <span data-ttu-id="a3b3e-131">表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-131">Fixed table format not displaying with</span></span> `vnet-gateway list-bgp-peer-status`
* <span data-ttu-id="a3b3e-132">`list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-132">Added `list-request-headers` and `list-response-headers` commands to</span></span> `application-gateway rewrite-rule`
* <span data-ttu-id="a3b3e-133">`list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-133">Added `list-server-variables` command to</span></span> `application-gateway rewrite-rule condition`
* <span data-ttu-id="a3b3e-134">ExpressRoute Port のリンク状態を更新すると、属性不明例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-134">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception</span></span> `express-route port update`

### <a name="privatedns"></a><span data-ttu-id="a3b3e-135">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-135">PrivateDNS</span></span>
* <span data-ttu-id="a3b3e-136">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-136">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-137">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-137">Resource</span></span>
* <span data-ttu-id="a3b3e-138">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-138">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-139">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-139">Role</span></span>
* <span data-ttu-id="a3b3e-140">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-140">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="a3b3e-141">[破壊的変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-141">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-142">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-142">SQL</span></span>
* <span data-ttu-id="a3b3e-143">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-143">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-144">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-144">Storage</span></span>
* <span data-ttu-id="a3b3e-145">[破壊的変更] 結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-145">[BREAKING CHANGE] Removed result of</span></span> `storage blob delete`
* <span data-ttu-id="a3b3e-146">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-146">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="a3b3e-147">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-147">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="a3b3e-148">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-148">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="a3b3e-149">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-149">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="a3b3e-150">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-150">Core</span></span>
* <span data-ttu-id="a3b3e-151">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-151">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="a3b3e-152">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-152">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="a3b3e-153">クラウド</span><span class="sxs-lookup"><span data-stu-id="a3b3e-153">Cloud</span></span>
* <span data-ttu-id="a3b3e-154">"サブスクリプションが見つかりません" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-154">Fixed a 'subscription not found' error in</span></span> `cloud set`

### <a name="acr"></a><span data-ttu-id="a3b3e-155">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-155">ACR</span></span>
* <span data-ttu-id="a3b3e-156">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-156">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="a3b3e-157">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-157">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="a3b3e-158">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-158">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="a3b3e-159">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-159">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-160">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-160">AppService</span></span>
* <span data-ttu-id="a3b3e-161">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-161">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="a3b3e-162">スロットが機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-162">Fixed bug where slots didn't work for</span></span> `[webapp|functionapp] config ssl bind`

### <a name="bot-service"></a><span data-ttu-id="a3b3e-163">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="a3b3e-163">BOT Service</span></span>
* <span data-ttu-id="a3b3e-164">ボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-164">Added `bot prepare-deploy` to prepare for deploying bots via</span></span> `webapp`
* <span data-ttu-id="a3b3e-165">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-165">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="a3b3e-166">[破壊的変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-166">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="a3b3e-167">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-167">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="a3b3e-168">CDN</span><span class="sxs-lookup"><span data-stu-id="a3b3e-168">CDN</span></span>
* <span data-ttu-id="a3b3e-169">`--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-169">Added support for `--no-wait` to</span></span> `cdn endpoint [create|update|start|stop|delete|load|purge]`  
* [破壊的変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="a3b3e-171">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-171">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="a3b3e-172">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-172">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="a3b3e-173">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="a3b3e-173">Cosmosdb</span></span>
* <span data-ttu-id="a3b3e-174">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-174">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="a3b3e-175">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-175">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="a3b3e-176">Interactive</span><span class="sxs-lookup"><span data-stu-id="a3b3e-176">Interactive</span></span>
* <span data-ttu-id="a3b3e-177">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-177">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="a3b3e-178">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-178">Monitor</span></span>
* <span data-ttu-id="a3b3e-179">ディメンション値 `*` を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-179">Changed to allow dimension value `*` for</span></span> `monitor metrics alert [create|update]`

### <a name="network"></a><span data-ttu-id="a3b3e-180">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-180">Network</span></span>
* <span data-ttu-id="a3b3e-181">`rewrite-rule` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-181">Added `rewrite-rule` command group to</span></span> `application-gateway`

### <a name="profile"></a><span data-ttu-id="a3b3e-182">プロファイル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-182">Profile</span></span>
* <span data-ttu-id="a3b3e-183">マネージド サービス ID に対応するテナント レベル アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-183">Added tenant level account support for managed service identity to</span></span> `login`

### <a name="postgres"></a><span data-ttu-id="a3b3e-184">Postgres</span><span class="sxs-lookup"><span data-stu-id="a3b3e-184">Postgres</span></span> 
* <span data-ttu-id="a3b3e-185">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-185">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="a3b3e-186">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-186">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-187">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-187">Resource</span></span>
* <span data-ttu-id="a3b3e-188">テーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-188">Improved table output for</span></span> `deployment [create|list|show]`
* <span data-ttu-id="a3b3e-189">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-189">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="a3b3e-190">Graph</span><span class="sxs-lookup"><span data-stu-id="a3b3e-190">Graph</span></span>
* <span data-ttu-id="a3b3e-191">`--end-date` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-191">Added support for `--end-date` to</span></span> `ad [app|sp] credential reset`
* <span data-ttu-id="a3b3e-192">追加アクセス許可のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-192">Added support to add permissions with</span></span> `ad app permission add`
* <span data-ttu-id="a3b3e-193">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-193">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="a3b3e-194">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-194">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="a3b3e-195">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-195">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-196">storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-196">storage</span></span>
* <span data-ttu-id="a3b3e-197">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-197">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="a3b3e-198">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-198">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="a3b3e-199">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-199">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="a3b3e-200">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-200">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-201">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-201">VM</span></span>
* <span data-ttu-id="a3b3e-202">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-202">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="a3b3e-203">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-203">March 12, 2019</span></span>

<span data-ttu-id="a3b3e-204">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="a3b3e-204">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-205">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-205">Core</span></span>

* <span data-ttu-id="a3b3e-206">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-206">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-207">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-207">ACR</span></span>

* <span data-ttu-id="a3b3e-208">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-208">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-209">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-209">ACS</span></span>

* <span data-ttu-id="a3b3e-210">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-210">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="a3b3e-211">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-211">AppService</span></span>

* <span data-ttu-id="a3b3e-212">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-212">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="a3b3e-213">誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-213">Removed erroneous print statement for</span></span> `webapp auth update`
* <span data-ttu-id="a3b3e-214">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-214">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="a3b3e-215">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-215">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="a3b3e-216">Botservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-216">Botservice</span></span>

* <span data-ttu-id="a3b3e-217">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-217">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="a3b3e-218">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-218">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="a3b3e-219">最後の `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-219">Removed single quotes from `bot publish` command output at end of</span></span> `bot create`
* <span data-ttu-id="a3b3e-220">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-220">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-221">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-221">Container</span></span>

* <span data-ttu-id="a3b3e-222">`--no-wait` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-222">Added `--no-wait` argument to</span></span> `container [start|restart]`

### <a name="eventhub"></a><span data-ttu-id="a3b3e-223">EventHub</span><span class="sxs-lookup"><span data-stu-id="a3b3e-223">EventHub</span></span>

* <span data-ttu-id="a3b3e-224">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-224">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="a3b3e-225">Find</span><span class="sxs-lookup"><span data-stu-id="a3b3e-225">Find</span></span>

* <span data-ttu-id="a3b3e-226">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="a3b3e-226">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="a3b3e-227">HDInsight</span><span class="sxs-lookup"><span data-stu-id="a3b3e-227">HDInsight</span></span>

* <span data-ttu-id="a3b3e-228">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-228">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-229">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-229">Network</span></span>

* <span data-ttu-id="a3b3e-230">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-230">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="a3b3e-231">Rdbms</span><span class="sxs-lookup"><span data-stu-id="a3b3e-231">Rdbms</span></span>

* <span data-ttu-id="a3b3e-232">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-232">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-233">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-233">Role</span></span>

* <span data-ttu-id="a3b3e-234">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-234">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="a3b3e-235">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-235">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="a3b3e-236">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="a3b3e-236">Service Fabric</span></span>

* <span data-ttu-id="a3b3e-237">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-237">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="a3b3e-238">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-238">February 26, 2019</span></span>

<span data-ttu-id="a3b3e-239">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="a3b3e-239">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-240">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-240">Core</span></span>

* <span data-ttu-id="a3b3e-241">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-241">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-242">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-242">ACR</span></span>

* <span data-ttu-id="a3b3e-243">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-243">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="a3b3e-244">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-244">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-245">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-245">ACS</span></span>

* <span data-ttu-id="a3b3e-246">`--listen-address` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-246">Added `--listen-address` option to</span></span> `aks port-forward`

### <a name="appservice"></a><span data-ttu-id="a3b3e-247">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-247">AppService</span></span>

* <span data-ttu-id="a3b3e-248">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-248">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="a3b3e-249">Batch</span><span class="sxs-lookup"><span data-stu-id="a3b3e-249">Batch</span></span>
* <span data-ttu-id="a3b3e-250">[破壊的変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-250">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="a3b3e-251">[破壊的変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-251">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="a3b3e-252">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-252">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="a3b3e-253">[破壊的変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-253">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="a3b3e-254">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-254">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="a3b3e-255">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-255">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="a3b3e-256">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="a3b3e-256">CosmosDB</span></span>

* <span data-ttu-id="a3b3e-257">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-257">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="a3b3e-258">Kusto</span><span class="sxs-lookup"><span data-stu-id="a3b3e-258">Kusto</span></span>

* <span data-ttu-id="a3b3e-259">[破壊的変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-259">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-260">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-260">Network</span></span>

* <span data-ttu-id="a3b3e-261">`--express-route-gateway-bypass` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-261">Added `--express-route-gateway-bypass` argument to</span></span> `vpn-connection [create|update]`
* <span data-ttu-id="a3b3e-262">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-262">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="a3b3e-263">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-263">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="a3b3e-264">`--legacy-mode` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-264">Added argument `--legacy-mode` to</span></span> `express-route peering [create|update]` 
* <span data-ttu-id="a3b3e-265">`--allow-classic-operations` 引数と `--express-route-port` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-265">Added arguments `--allow-classic-operations` and `--express-route-port` to</span></span> `express-route [create|update]`
* <span data-ttu-id="a3b3e-266">`--gateway-default-site` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-266">Added `--gateway-default-site` argument to</span></span> `vnet-gateway [create|update]`
* <span data-ttu-id="a3b3e-267">`ipsec-policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-267">Added `ipsec-policy` commands to</span></span> `vnet-gateway`

### <a name="resource"></a><span data-ttu-id="a3b3e-268">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-268">Resource</span></span>

* <span data-ttu-id="a3b3e-269">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-269">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="a3b3e-270">URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-270">Added support for URI-based parameters file to</span></span> `policy assignment create`
* <span data-ttu-id="a3b3e-271">URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-271">Added support for URI-based parameters and definitions to</span></span> `policy set-definition update`
* <span data-ttu-id="a3b3e-272">パラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-272">Fixed handling of parameters and rules for</span></span> `policy definition update`
* <span data-ttu-id="a3b3e-273">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-273">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-274">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-274">Role</span></span>

* <span data-ttu-id="a3b3e-275">アプリ ロールのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-275">Added support for app roles to</span></span> `ad app [create|update]`

### <a name="vm"></a><span data-ttu-id="a3b3e-276">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-276">VM</span></span>

* <span data-ttu-id="a3b3e-277">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-277">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="a3b3e-278">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-278">February 12, 2019</span></span>

<span data-ttu-id="a3b3e-279">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="a3b3e-279">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-280">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-280">Core</span></span>

* `az --version` <span data-ttu-id="a3b3e-281">更新可能なパッケージがある場合、通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-281">now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="a3b3e-282">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-282">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-283">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-283">ACR</span></span>
* <span data-ttu-id="a3b3e-284">[破壊的変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-284">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="a3b3e-285">[破壊的変更] `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-285">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from</span></span> `acr repository delete`

### <a name="acs"></a><span data-ttu-id="a3b3e-286">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-286">ACS</span></span>
* <span data-ttu-id="a3b3e-287">大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-287">Added support for case-insensitive names to</span></span> `aks [enable-addons|disable-addons]`
* <span data-ttu-id="a3b3e-288">Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-288">Added support for Azure Active Directory updating operation using</span></span> `aks update-credentials --reset-aad`
* <span data-ttu-id="a3b3e-289">`--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-289">Added clarification that `--output` is ignored for</span></span> `aks get-credentials`

### <a name="ams"></a><span data-ttu-id="a3b3e-290">AMS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-290">AMS</span></span>
* <span data-ttu-id="a3b3e-291">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-291">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="a3b3e-292">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-292">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-293">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-293">Appservice</span></span>
* <span data-ttu-id="a3b3e-294">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-294">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="a3b3e-295">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-295">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="a3b3e-296">ヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-296">Improved help for</span></span> `appservice-plan-update`
* <span data-ttu-id="a3b3e-297">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-297">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="a3b3e-298">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-298">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="a3b3e-299">Botservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-299">Botservice</span></span>
* <span data-ttu-id="a3b3e-300">UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-300">Improved UX for</span></span> `bot publish`
* <span data-ttu-id="a3b3e-301">`npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-301">Added warning for timeouts when running `npm install` during</span></span> `az bot publish`
* <span data-ttu-id="a3b3e-302">`--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-302">Removed invalid char `.` from `--name`  in</span></span> `az bot create`
* <span data-ttu-id="a3b3e-303">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-303">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="a3b3e-304">[非推奨] `--proj-name` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-304">[DEPRECATED] Deprecated `--proj-name` argument in favor of</span></span> `--proj-file-path`
* <span data-ttu-id="a3b3e-305">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-305">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="a3b3e-306">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-306">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="a3b3e-307">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-307">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="a3b3e-308">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="a3b3e-308">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="a3b3e-309">8.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-309">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="a3b3e-310">Key Vault</span><span class="sxs-lookup"><span data-stu-id="a3b3e-310">Key Vault</span></span>
* <span data-ttu-id="a3b3e-311">一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-311">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using</span></span> `--id`

### <a name="monitor"></a><span data-ttu-id="a3b3e-312">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-312">Monitor</span></span>
* <span data-ttu-id="a3b3e-313">ディメンション値を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-313">Changed `monitor metrics alert [create|update]` to allow dimension value</span></span> `*`

### <a name="network"></a><span data-ttu-id="a3b3e-314">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-314">Network</span></span>
* <span data-ttu-id="a3b3e-315">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-315">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="a3b3e-316">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-316">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="a3b3e-317">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-317">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="a3b3e-318">`--idle-timeout` と `--floating-ip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-318">Added `--idle-timeout` and `--floating-ip` to</span></span> `lb inbound-nat-pool [create|update]`

### <a name="policy-insights"></a><span data-ttu-id="a3b3e-319">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="a3b3e-319">Policy Insights</span></span>
* <span data-ttu-id="a3b3e-320">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-320">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="a3b3e-321">RDBMS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-321">RDBMS</span></span>
* <span data-ttu-id="a3b3e-322">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-322">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="a3b3e-323">Redis</span><span class="sxs-lookup"><span data-stu-id="a3b3e-323">Redis</span></span>
* <span data-ttu-id="a3b3e-324">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-324">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="a3b3e-325">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-325">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="a3b3e-326">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-326">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="a3b3e-327">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-327">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="a3b3e-328">[破壊的変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-328">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="a3b3e-329">[破壊的変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-329">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="a3b3e-330">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-330">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-331">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-331">Role</span></span>
* <span data-ttu-id="a3b3e-332">[破壊的変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-332">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="a3b3e-333">SQL VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-333">SQL VM</span></span>
* <span data-ttu-id="a3b3e-334">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-334">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-335">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-335">VM</span></span>
* <span data-ttu-id="a3b3e-336">`--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-336">Changed `vm list-skus` to allow use of `--all` in place of</span></span> `--all true`
* <span data-ttu-id="a3b3e-337">追加済み</span><span class="sxs-lookup"><span data-stu-id="a3b3e-337">Added</span></span> `vmss run-command [invoke | list | show]`
* <span data-ttu-id="a3b3e-338">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-338">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="a3b3e-339">[破壊的変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-339">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="a3b3e-340">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-340">January 31, 2019</span></span>

<span data-ttu-id="a3b3e-341">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="a3b3e-341">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-342">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-342">Core</span></span>

* <span data-ttu-id="a3b3e-343">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-343">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="a3b3e-344">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-344">January 28, 2019</span></span>

<span data-ttu-id="a3b3e-345">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="a3b3e-345">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-346">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-346">ACR</span></span>
* <span data-ttu-id="a3b3e-347">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-347">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-348">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-348">ACS</span></span>
* <span data-ttu-id="a3b3e-349">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-349">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="a3b3e-350">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-350">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="a3b3e-351">サービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-351">Added support for service principal updates operation with</span></span> `aks update-credentials -reset-service-principal`

### <a name="ams"></a><span data-ttu-id="a3b3e-352">AMS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-352">AMS</span></span>
* <span data-ttu-id="a3b3e-353">[破壊的変更] 名前を `ams asset get-streaming-locators` から変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-353">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to</span></span> `ams asset list-streaming-locators`
* <span data-ttu-id="a3b3e-354">[破壊的変更] 名前を `ams streaming-locator get-content-keys` から変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-354">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to</span></span> `ams streaming-locator list-content-keys`

### <a name="appservice"></a><span data-ttu-id="a3b3e-355">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-355">Appservice</span></span>
* <span data-ttu-id="a3b3e-356">App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-356">Added support for app insights on</span></span> `functionapp create`
* <span data-ttu-id="a3b3e-357">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-357">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="a3b3e-358">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-358">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-359">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-359">Container</span></span>
* <span data-ttu-id="a3b3e-360">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-360">Added `container start` command</span></span>
* <span data-ttu-id="a3b3e-361">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-361">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="a3b3e-362">EventGrid</span><span class="sxs-lookup"><span data-stu-id="a3b3e-362">EventGrid</span></span>
* <span data-ttu-id="a3b3e-363">`--deadletter-endpoint` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-363">Added `--deadletter-endpoint` parameter to</span></span> `event-subscription [create|update]`
* <span data-ttu-id="a3b3e-364">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-364">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="a3b3e-365">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-365">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="a3b3e-366">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-366">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="a3b3e-367">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-367">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="a3b3e-368">HDInsight</span><span class="sxs-lookup"><span data-stu-id="a3b3e-368">HDInsight</span></span>
* <span data-ttu-id="a3b3e-369">[破壊的変更] `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-369">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from</span></span> `hdinsight [application] create`
* <span data-ttu-id="a3b3e-370">[破壊的変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-370">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="a3b3e-371">`--vnet-name` パラメーターと `--subnet-name` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-371">Added `--vnet-name` and `--subnet-name` parameters to</span></span> `hdinsight create`
* <span data-ttu-id="a3b3e-372">Enterprise セキュリティ パッケージとディスク暗号化のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-372">Added support for Enterprise Security Package and disk encryption to</span></span> `hdinsight create` 
* <span data-ttu-id="a3b3e-373">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-373">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="a3b3e-374">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-374">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="a3b3e-375">IoT</span><span class="sxs-lookup"><span data-stu-id="a3b3e-375">IoT</span></span>
* <span data-ttu-id="a3b3e-376">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-376">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="a3b3e-377">Kusto</span><span class="sxs-lookup"><span data-stu-id="a3b3e-377">Kusto</span></span>
* <span data-ttu-id="a3b3e-378">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-378">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="a3b3e-379">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-379">Monitor</span></span>
* <span data-ttu-id="a3b3e-380">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-380">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="a3b3e-381">プロファイル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-381">Profile</span></span>
* <span data-ttu-id="a3b3e-382">マネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-382">Enable tenant level account for managed service identity for</span></span> `login`

### <a name="network"></a><span data-ttu-id="a3b3e-383">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-383">Network</span></span>
* <span data-ttu-id="a3b3e-384">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-384">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="a3b3e-385">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-385">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-386">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-386">Resource</span></span>
* <span data-ttu-id="a3b3e-387">URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-387">Added support for URI parameters file to</span></span> `group deployment create`
* <span data-ttu-id="a3b3e-388">マネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-388">Added support for managed identity to</span></span> `policy assignment [create|list|show]`

### <a name="sql-virtual-machine"></a><span data-ttu-id="a3b3e-389">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="a3b3e-389">SQL Virtual Machine</span></span>
* <span data-ttu-id="a3b3e-390">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-390">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-391">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-391">Storage</span></span>
* <span data-ttu-id="a3b3e-392">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-392">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="a3b3e-393">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-393">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-394">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-394">VM</span></span>
* <span data-ttu-id="a3b3e-395">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-395">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="a3b3e-396">`--force` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-396">Added `--force` flag to</span></span> `vm encryption enable`

## <a name="january-15-2019"></a><span data-ttu-id="a3b3e-397">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-397">January 15, 2019</span></span>

<span data-ttu-id="a3b3e-398">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="a3b3e-398">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-399">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-399">ACR</span></span>
* <span data-ttu-id="a3b3e-400">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-400">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="a3b3e-401">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-401">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="a3b3e-402">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-402">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="a3b3e-403">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-403">ACS</span></span>
* <span data-ttu-id="a3b3e-404">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-404">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-405">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-405">Appservice</span></span>
* <span data-ttu-id="a3b3e-406">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-406">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="a3b3e-407">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-407">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="a3b3e-408">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-408">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="a3b3e-409">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-409">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="a3b3e-410">Botservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-410">Botservice</span></span>
* <span data-ttu-id="a3b3e-411">デプロイ状態の更新プログラムを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-411">Added deployment status updates to</span></span> `bot create`

### <a name="configure"></a><span data-ttu-id="a3b3e-412">構成</span><span class="sxs-lookup"><span data-stu-id="a3b3e-412">Configure</span></span>
* <span data-ttu-id="a3b3e-413">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-413">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="a3b3e-414">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="a3b3e-414">CosmosDB</span></span>
* <span data-ttu-id="a3b3e-415">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-415">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="a3b3e-416">HDInsight</span><span class="sxs-lookup"><span data-stu-id="a3b3e-416">HDInsight</span></span>
* <span data-ttu-id="a3b3e-417">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-417">Added commands for managing applications</span></span>
* <span data-ttu-id="a3b3e-418">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-418">Added commands for managing script actions</span></span>
* <span data-ttu-id="a3b3e-419">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-419">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="a3b3e-420">リージョンの使用状況を一覧表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-420">Added support to list regional usage to</span></span> `hdinsight list-usage`
* <span data-ttu-id="a3b3e-421">[破壊的変更] 既定のクラスターの種類を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-421">[BREAKING CHANGE] Removed default cluster type from</span></span> `hdinsight create`

### <a name="network"></a><span data-ttu-id="a3b3e-422">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-422">Network</span></span>
* <span data-ttu-id="a3b3e-423">`--custom-headers` 引数と `--status-code-ranges` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-423">Added `--custom-headers` and `--status-code-ranges` arguments to</span></span> `traffic-manager profile [create|update]`
* <span data-ttu-id="a3b3e-424">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-424">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="a3b3e-425">`--custom-headers` 引数と `--subnets` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-425">Added `--custom-headers` and `--subnets` arguments to</span></span> `traffic-manager endpoint [create|update]`  
* <span data-ttu-id="a3b3e-426">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-426">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-427">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-427">Role</span></span>
* <span data-ttu-id="a3b3e-428">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-428">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="a3b3e-429">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="a3b3e-429">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="a3b3e-430">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-430">Security</span></span>
* <span data-ttu-id="a3b3e-431">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-431">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-432">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-432">Storage</span></span>
* <span data-ttu-id="a3b3e-433">[破壊的変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-433">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="a3b3e-434">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="a3b3e-434">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="a3b3e-435">`--marker` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-435">Added `--marker` parameter to</span></span> `storage [blob|file|container|share] list`
* <span data-ttu-id="a3b3e-436">次のページを表すログ マーカーを STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-436">Added log marker for next page to STDERR for</span></span> `storage [blob|file|container|share] list` 
* <span data-ttu-id="a3b3e-437">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-437">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-438">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-438">VM</span></span>
* <span data-ttu-id="a3b3e-439">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-439">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="a3b3e-440">テナント イメージ相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-440">Added support for cross tenant image referencing to</span></span> `[vm|vmss] create`
* <span data-ttu-id="a3b3e-441">既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-441">Fixed bug with default configuration in</span></span> `vm diagnostics get-default-config --windows-os`
* <span data-ttu-id="a3b3e-442">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-442">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="a3b3e-443">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-443">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="a3b3e-444">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-444">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="a3b3e-445">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-445">December 20, 2018</span></span>

<span data-ttu-id="a3b3e-446">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="a3b3e-446">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="a3b3e-447">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-447">Appservice</span></span>
* <span data-ttu-id="a3b3e-448">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-448">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="a3b3e-449">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-449">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="a3b3e-450">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-450">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="a3b3e-451">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="a3b3e-451">IoTCentral</span></span>
* <span data-ttu-id="a3b3e-452">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-452">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-453">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-453">Role</span></span>
* <span data-ttu-id="a3b3e-454">[破壊的変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-454">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-455">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-455">SQL</span></span>
* <span data-ttu-id="a3b3e-456">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-456">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-457">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-457">VM</span></span>
* <span data-ttu-id="a3b3e-458">`---os-type` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-458">Added `---os-type` parameter to</span></span> `disk create`

## <a name="december-18-2018"></a><span data-ttu-id="a3b3e-459">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-459">December 18, 2018</span></span>

<span data-ttu-id="a3b3e-460">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="a3b3e-460">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="a3b3e-461">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-461">ACR</span></span>
* <span data-ttu-id="a3b3e-462">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-462">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="a3b3e-463">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-463">Condensed the table layout for task list</span></span>
* <span data-ttu-id="a3b3e-464">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-464">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-465">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-465">ACS</span></span>
* <span data-ttu-id="a3b3e-466">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-466">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="a3b3e-467">AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-467">Removed "(PREVIEW)" from AAD arguments to</span></span> `aks create`
* <span data-ttu-id="a3b3e-468">[非推奨] `az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-468">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="a3b3e-469">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="a3b3e-469">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="a3b3e-470">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-470">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="a3b3e-471">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-471">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-472">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-472">Appservice</span></span>
* <span data-ttu-id="a3b3e-473">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-473">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="a3b3e-474">Botservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-474">Botservice</span></span>
* <span data-ttu-id="a3b3e-475">呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-475">Added support for `.bot` file parsing when calling</span></span> `bot show`
* <span data-ttu-id="a3b3e-476">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-476">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="a3b3e-477">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-477">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="a3b3e-478">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-478">Reduced Kudu network calls</span></span>
* <span data-ttu-id="a3b3e-479">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-479">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="a3b3e-480">消費</span><span class="sxs-lookup"><span data-stu-id="a3b3e-480">Consumption</span></span>
* <span data-ttu-id="a3b3e-481">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-481">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="a3b3e-482">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="a3b3e-482">CosmosDB</span></span>
* <span data-ttu-id="a3b3e-483">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-483">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="a3b3e-484">マップ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-484">Maps</span></span>
* <span data-ttu-id="a3b3e-485">S1 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-485">Added support for the S1 SKU to</span></span> `maps account [create|update]`

### <a name="network"></a><span data-ttu-id="a3b3e-486">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-486">Network</span></span>
* <span data-ttu-id="a3b3e-487">`--format` と `--log-version` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-487">Added support for `--format` and `--log-version` to</span></span> `watcher flow-log configure`
* <span data-ttu-id="a3b3e-488">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-488">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-489">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-489">Resource</span></span>
* <span data-ttu-id="a3b3e-490">管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-490">Fixed handling of scope parameter for management groups in</span></span> `policy assignment [create|list|delete|show|update]` 
* <span data-ttu-id="a3b3e-491">新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-491">Added new command</span></span> `resource wait`

### <a name="storage"></a><span data-ttu-id="a3b3e-492">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-492">Storage</span></span>
*  <span data-ttu-id="a3b3e-493">ストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-493">Added ability to update log schema version for storage services in</span></span> `storage logging update`

### <a name="vm"></a><span data-ttu-id="a3b3e-494">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-494">VM</span></span>
* <span data-ttu-id="a3b3e-495">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-495">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="a3b3e-496">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-496">December 4, 2018</span></span>

<span data-ttu-id="a3b3e-497">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="a3b3e-497">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="a3b3e-498">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-498">Core</span></span>
* <span data-ttu-id="a3b3e-499">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-499">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="a3b3e-500">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-500">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-501">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-501">Appservice</span></span>
* <span data-ttu-id="a3b3e-502">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-502">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="a3b3e-503">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-503">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-504">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-504">Network</span></span>
* <span data-ttu-id="a3b3e-505">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-505">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-506">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-506">Role</span></span>
* <span data-ttu-id="a3b3e-507">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-507">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="a3b3e-508">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-508">VM</span></span>
* <span data-ttu-id="a3b3e-509">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-509">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="a3b3e-510">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-510">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="a3b3e-511">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-511">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="a3b3e-512">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-512">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="a3b3e-513">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-513">November 20, 2018</span></span>

<span data-ttu-id="a3b3e-514">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="a3b3e-514">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="a3b3e-515">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-515">Core</span></span>
* <span data-ttu-id="a3b3e-516">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-516">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-517">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-517">ACR</span></span>
* <span data-ttu-id="a3b3e-518">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-518">Added context token to task step</span></span>
* <span data-ttu-id="a3b3e-519">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-519">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="a3b3e-520">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-520">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-521">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-521">Appservice</span></span>
* <span data-ttu-id="a3b3e-522">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-522">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="a3b3e-523">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-523">Updated the default `node_version`.</span></span> <span data-ttu-id="a3b3e-524">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-524">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="a3b3e-525">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-525">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="a3b3e-526">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-526">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="a3b3e-527">IotCentral</span><span class="sxs-lookup"><span data-stu-id="a3b3e-527">IotCentral</span></span>
* <span data-ttu-id="a3b3e-528">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-528">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="a3b3e-529">KeyVault</span><span class="sxs-lookup"><span data-stu-id="a3b3e-529">KeyVault</span></span>
* <span data-ttu-id="a3b3e-530">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-530">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-531">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-531">Network</span></span>
* <span data-ttu-id="a3b3e-532">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-532">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="a3b3e-533">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-533">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="a3b3e-534">可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-534">Added `--zones` for availability zone support to</span></span> `application-gateway create` 
* <span data-ttu-id="a3b3e-535">`--file-upload-limit`、`--max-request-body-size`、および `--request-body-check` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-535">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to</span></span> `application-gateway waf-config set`

### <a name="rdbms"></a><span data-ttu-id="a3b3e-536">Rdbms</span><span class="sxs-lookup"><span data-stu-id="a3b3e-536">Rdbms</span></span>
* <span data-ttu-id="a3b3e-537">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-537">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="a3b3e-538">Rbac</span><span class="sxs-lookup"><span data-stu-id="a3b3e-538">Rbac</span></span>
* <span data-ttu-id="a3b3e-539">変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-539">Fixed an issue with attempting to update immutable credentials in</span></span> `ad app update`
* <span data-ttu-id="a3b3e-540">近い将来の破壊的変更を伝える、出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-540">Added output warnings to communicate breaking changes in the near future for</span></span> `ad [app|sp] list` 

### <a name="storage"></a><span data-ttu-id="a3b3e-541">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-541">Storage</span></span>
* <span data-ttu-id="a3b3e-542">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-542">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="a3b3e-543">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-543">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="a3b3e-544">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-544">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="a3b3e-545">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-545">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-546">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-546">VM</span></span>
* <span data-ttu-id="a3b3e-547">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-547">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="a3b3e-548">`sig image-version` のバージョン名パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-548">Changed version name parameters to `sig image-version` to be</span></span> `--image-version -e`
* <span data-ttu-id="a3b3e-549">`sig image-version` の引数 `--image-version-name` が非推奨になり、置き換えられました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-549">Deprecated `sig image-version` argument `--image-version-name`, replaced by</span></span> `--image-version`
* <span data-ttu-id="a3b3e-550">ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-550">Added support to use local OS disk to</span></span> `[vm|vmss] create --ephemeral-os-disk`
* <span data-ttu-id="a3b3e-551">`--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-551">Added support for `--no-wait` to</span></span> `snapshot create/update`
* <span data-ttu-id="a3b3e-552">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-552">Added `snapshot wait` command</span></span>
* <span data-ttu-id="a3b3e-553">インスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-553">Added support for using instance name with</span></span> `[vm|vmss] extension set --extension-instance-name`

## <a name="november-6-2018"></a><span data-ttu-id="a3b3e-554">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-554">November 6, 2018</span></span>

<span data-ttu-id="a3b3e-555">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="a3b3e-555">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-556">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-556">Core</span></span>
* <span data-ttu-id="a3b3e-557">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-557">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-558">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-558">ACR</span></span>
* <span data-ttu-id="a3b3e-559">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-559">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="a3b3e-560">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-560">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-561">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-561">ACS</span></span>
* <span data-ttu-id="a3b3e-562">[破壊的変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-562">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="a3b3e-563">Advisor</span><span class="sxs-lookup"><span data-stu-id="a3b3e-563">Advisor</span></span>
* <span data-ttu-id="a3b3e-564">GA リリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-564">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="a3b3e-565">AMS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-565">AMS</span></span>
* <span data-ttu-id="a3b3e-566">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-566">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="a3b3e-567">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-567">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="a3b3e-568">暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-568">Added encryption parameters support to</span></span> `ams streaming-policy create`
* <span data-ttu-id="a3b3e-569">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-569">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="a3b3e-570">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-570">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="a3b3e-571">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-571">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="a3b3e-572">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-572">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="a3b3e-573">[破壊的変更] `ams streaming locator` コマンドを置き換えました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-573">[BREAKING CHANGE] Replaced `ams streaming locator` command with</span></span> `ams streaming-locator`
* <span data-ttu-id="a3b3e-574">[破壊的変更] `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-574">[BREAKING CHANGE] Updated `--content-keys` argument of</span></span> `ams streaming locator`
* <span data-ttu-id="a3b3e-575">[破壊的変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-575">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="a3b3e-576">[破壊的変更] `ams streaming policy` コマンドを置き換えました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-576">[BREAKING CHANGE] Replaced `ams streaming policy` command with</span></span> `ams streaming-policy`
* <span data-ttu-id="a3b3e-577">[破壊的変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-577">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="a3b3e-578">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-578">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="a3b3e-579">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-579">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="a3b3e-580">[破壊的変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-580">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="a3b3e-581">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-581">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="a3b3e-582">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-582">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-583">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-583">AppService</span></span>
* <span data-ttu-id="a3b3e-584">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-584">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="a3b3e-585">構成</span><span class="sxs-lookup"><span data-stu-id="a3b3e-585">Configure</span></span>
* <span data-ttu-id="a3b3e-586">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-586">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-587">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-587">Container</span></span>
* <span data-ttu-id="a3b3e-588">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-588">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="a3b3e-589">EventHub</span><span class="sxs-lookup"><span data-stu-id="a3b3e-589">EventHub</span></span>
* <span data-ttu-id="a3b3e-590">Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-590">Added `--enable-kafka` flag to support Kafka in</span></span> `eventhub namespace [create|update]`

### <a name="interactive"></a><span data-ttu-id="a3b3e-591">Interactive</span><span class="sxs-lookup"><span data-stu-id="a3b3e-591">Interactive</span></span>
* <span data-ttu-id="a3b3e-592">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="a3b3e-592">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="a3b3e-593">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-593">Monitor</span></span>
* <span data-ttu-id="a3b3e-594">`--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-594">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in</span></span> `monitor metrics alert [create|update]`

### <a name="network"></a><span data-ttu-id="a3b3e-595">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-595">Network</span></span>
* <span data-ttu-id="a3b3e-596">を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-596">Deprecated `network interface-endpoint` command names in favor of</span></span> `network private-endpoint`
* <span data-ttu-id="a3b3e-597">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-597">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="a3b3e-598">`--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-598">Fixed issue where `--ip-tags` did not work correctly with</span></span> `public-ip create` 

### <a name="profile"></a><span data-ttu-id="a3b3e-599">プロファイル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-599">Profile</span></span>
* <span data-ttu-id="a3b3e-600">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-600">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="a3b3e-601">RDBMS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-601">RDBMS</span></span>
* <span data-ttu-id="a3b3e-602">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-602">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-603">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-603">Resource</span></span>
* <span data-ttu-id="a3b3e-604">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-604">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-605">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-605">Role</span></span>
* <span data-ttu-id="a3b3e-606">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-606">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="a3b3e-607">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-607">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="a3b3e-608">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-608">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-609">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-609">Storage</span></span>
* <span data-ttu-id="a3b3e-610">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-610">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-611">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-611">VM</span></span>
* <span data-ttu-id="a3b3e-612">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-612">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="a3b3e-613">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-613">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="a3b3e-614">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-614">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="a3b3e-615">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-615">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="a3b3e-616">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="a3b3e-616">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="a3b3e-617">引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-617">Improved argument validation for</span></span> `vm create --image`

## <a name="october-23-2018"></a><span data-ttu-id="a3b3e-618">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-618">October 23, 2018</span></span>

<span data-ttu-id="a3b3e-619">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="a3b3e-619">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-620">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-620">Core</span></span>
* <span data-ttu-id="a3b3e-621">`--subscription` がサブスクリプションよりも優先される `--ids` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-621">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in</span></span> `--ids`
* <span data-ttu-id="a3b3e-622">パラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-622">Added explicit warnings when parameters would be ignored by use of</span></span> `--ids`

### <a name="acr"></a><span data-ttu-id="a3b3e-623">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-623">ACR</span></span>
* <span data-ttu-id="a3b3e-624">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-624">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="a3b3e-625">CDN</span><span class="sxs-lookup"><span data-stu-id="a3b3e-625">CDN</span></span>
* <span data-ttu-id="a3b3e-626">[破壊的変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-626">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="a3b3e-627">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-627">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-628">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-628">Container</span></span>
* <span data-ttu-id="a3b3e-629">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-629">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="a3b3e-630">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-630">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="a3b3e-631">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-631">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="a3b3e-632">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-632">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="a3b3e-633">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-633">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="a3b3e-634">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-634">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="a3b3e-635">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-635">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="a3b3e-636">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="a3b3e-636">CosmosDB</span></span>
* <span data-ttu-id="a3b3e-637">`--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-637">Added `--enable-multiple-write-locations` support to</span></span> `cosmosdb create`

### <a name="interactive"></a><span data-ttu-id="a3b3e-638">Interactive</span><span class="sxs-lookup"><span data-stu-id="a3b3e-638">Interactive</span></span>
* <span data-ttu-id="a3b3e-639">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-639">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="a3b3e-640">IoT Central</span><span class="sxs-lookup"><span data-stu-id="a3b3e-640">IoT Central</span></span>
* <span data-ttu-id="a3b3e-641">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-641">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="a3b3e-642">[破壊的変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-642">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="a3b3e-643">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-643">Monitor</span></span>
* <span data-ttu-id="a3b3e-644">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="a3b3e-644">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="a3b3e-645">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-645">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="a3b3e-646">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-646">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="a3b3e-647">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-647">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="a3b3e-648">非推奨のオプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-648">Added `--namespace` as alias for deprecated option</span></span> `--resource-provider`
  * <span data-ttu-id="a3b3e-649">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-649">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="a3b3e-650">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="a3b3e-650">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="a3b3e-651">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-651">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="a3b3e-652">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-652">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="a3b3e-653">`--event-hub` 引数と `--event-hub-rule` 引数の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-653">Improved validation for `--event-hub` and `--event-hub-rule` arguments to</span></span> `monitor diagnostic-settings create`

### <a name="network"></a><span data-ttu-id="a3b3e-654">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-654">Network</span></span>
* <span data-ttu-id="a3b3e-655">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-655">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="a3b3e-656">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-656">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="a3b3e-657">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a3b3e-657">ServiceBus</span></span>
* <span data-ttu-id="a3b3e-658">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-658">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-659">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-659">SQL</span></span>
* <span data-ttu-id="a3b3e-660">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-660">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-661">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-661">Storage</span></span>
* <span data-ttu-id="a3b3e-662">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-662">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="a3b3e-663">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-663">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-664">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-664">VM</span></span>
* <span data-ttu-id="a3b3e-665">Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-665">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in</span></span> `[vm|vmss] create`
* <span data-ttu-id="a3b3e-666">ネットワーク アクセラレータをサポートする、サポートされているサイズの一覧を更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-666">Updated supported size list supporting networking accelerator for</span></span> `vm create`
* <span data-ttu-id="a3b3e-667">ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-667">Added strong typed arguments for ultrassd iops and mbps configs for</span></span> `disk create`

## <a name="october-16-2018"></a><span data-ttu-id="a3b3e-668">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-668">October 16, 2018</span></span>

<span data-ttu-id="a3b3e-669">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="a3b3e-669">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-670">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-670">VM</span></span>
* <span data-ttu-id="a3b3e-671">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-671">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="a3b3e-672">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-672">October 9, 2018</span></span>

<span data-ttu-id="a3b3e-673">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="a3b3e-673">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-674">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-674">Core</span></span>
* <span data-ttu-id="a3b3e-675">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-675">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-676">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-676">ACR</span></span>
* <span data-ttu-id="a3b3e-677">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-677">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-678">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-678">ACS</span></span>
* <span data-ttu-id="a3b3e-679">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="a3b3e-679">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="a3b3e-680">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-680">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="a3b3e-681">省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-681">Changed `aks create` to no longer require</span></span> `--aad-tenant-id`
* <span data-ttu-id="a3b3e-682">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-682">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-683">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-683">Container</span></span>
* <span data-ttu-id="a3b3e-684">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-684">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="a3b3e-685">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-685">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="a3b3e-686">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-686">Event Hub</span></span>
* <span data-ttu-id="a3b3e-687">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-687">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="a3b3e-688">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-688">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="a3b3e-689">Extensions</span><span class="sxs-lookup"><span data-stu-id="a3b3e-689">Extensions</span></span>
* <span data-ttu-id="a3b3e-690">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-690">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="a3b3e-691">HDInsight</span><span class="sxs-lookup"><span data-stu-id="a3b3e-691">HDInsight</span></span>
* <span data-ttu-id="a3b3e-692">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-692">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="a3b3e-693">IoT</span><span class="sxs-lookup"><span data-stu-id="a3b3e-693">IoT</span></span>
* <span data-ttu-id="a3b3e-694">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-694">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="a3b3e-695">KeyVault</span><span class="sxs-lookup"><span data-stu-id="a3b3e-695">KeyVault</span></span>
* <span data-ttu-id="a3b3e-696">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-696">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-697">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-697">Network</span></span>
* <span data-ttu-id="a3b3e-698">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-698">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="a3b3e-699">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="a3b3e-699">See #6052</span></span>
* <span data-ttu-id="a3b3e-700">`--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-700">Deprecated `--remote-vnet-id` for</span></span> `network vnet peering create`
* <span data-ttu-id="a3b3e-701">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-701">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="a3b3e-702">`network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-702">Added support for multiple subnet prefixes to `network vnet create` with</span></span> `--subnet-prefixes`
* <span data-ttu-id="a3b3e-703">`network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-703">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with</span></span> `--address-prefixes`
* <span data-ttu-id="a3b3e-704">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-704">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="a3b3e-705">`--service-endpoint-policy` の利便性の引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-705">Added `--service-endpoint-policy` convenience argument to</span></span> `network vnet subnet update`

### <a name="role"></a><span data-ttu-id="a3b3e-706">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-706">Role</span></span>
* <span data-ttu-id="a3b3e-707">Azure AD アプリ所有者を一覧表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-707">Added support for listing Azure AD app owners to</span></span> `ad app owner`
* <span data-ttu-id="a3b3e-708">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-708">Added support for listing Azure AD service principal owners to</span></span> `ad sp owner`
* <span data-ttu-id="a3b3e-709">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-709">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="a3b3e-710">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-710">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="a3b3e-711">Service Bus</span><span class="sxs-lookup"><span data-stu-id="a3b3e-711">Service Bus</span></span>
* <span data-ttu-id="a3b3e-712">[破壊的変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-712">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-713">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-713">VM</span></span>
* <span data-ttu-id="a3b3e-714">空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-714">Fixed empty `accessSas` field in</span></span> `disk grant-access`
* <span data-ttu-id="a3b3e-715">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-715">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="a3b3e-716">更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-716">Fixed update commands for</span></span> `sig`
* <span data-ttu-id="a3b3e-717">イメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-717">Added `--no-wait` support for managing image versions in</span></span> `sig`
* <span data-ttu-id="a3b3e-718">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-718">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="a3b3e-719">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-719">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="a3b3e-720">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-720">September 21, 2018</span></span>

<span data-ttu-id="a3b3e-721">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="a3b3e-721">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-722">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-722">ACR</span></span>
* <span data-ttu-id="a3b3e-723">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-723">Added ACR Task commands</span></span>
* <span data-ttu-id="a3b3e-724">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-724">Added quick run command</span></span>
* <span data-ttu-id="a3b3e-725">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-725">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="a3b3e-726">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-726">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="a3b3e-727">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-727">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="a3b3e-728">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-728">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-729">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-729">ACS</span></span>
* <span data-ttu-id="a3b3e-730">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-730">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="a3b3e-731">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-731">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-732">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-732">AppService</span></span>

* <span data-ttu-id="a3b3e-733">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-733">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="a3b3e-734">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-734">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="a3b3e-735">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-735">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="a3b3e-736">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-736">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="a3b3e-737">Batch</span><span class="sxs-lookup"><span data-stu-id="a3b3e-737">Batch</span></span>
* <span data-ttu-id="a3b3e-738">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-738">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="a3b3e-739">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-739">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="a3b3e-740">`--max-tasks-per-node-option` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-740">Added `--max-tasks-per-node-option` to</span></span> `batch pool create`
* <span data-ttu-id="a3b3e-741">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-741">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="a3b3e-742">Batch AI</span><span class="sxs-lookup"><span data-stu-id="a3b3e-742">Batch AI</span></span> 
* <span data-ttu-id="a3b3e-743">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-743">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="a3b3e-744">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="a3b3e-744">Cognitive Services</span></span>
* <span data-ttu-id="a3b3e-745">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-745">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="a3b3e-746">コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-746">Added command</span></span> `cognitiveservices account list-usage`
* <span data-ttu-id="a3b3e-747">コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-747">Added command</span></span> `cognitiveservices account list-kinds`
* <span data-ttu-id="a3b3e-748">コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-748">Added command</span></span> `cognitiveservices account list`
* <span data-ttu-id="a3b3e-749">非推奨</span><span class="sxs-lookup"><span data-stu-id="a3b3e-749">Deprecated</span></span> `cognitiveservices list`
* <span data-ttu-id="a3b3e-750">`--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-750">Changed `--name` to be optional for</span></span> `cognitiveservices account list-skus`

### <a name="container"></a><span data-ttu-id="a3b3e-751">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-751">Container</span></span>
* <span data-ttu-id="a3b3e-752">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-752">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="a3b3e-753">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-753">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="a3b3e-754">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-754">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="a3b3e-755">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-755">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="a3b3e-756">DataLake</span><span class="sxs-lookup"><span data-stu-id="a3b3e-756">Datalake</span></span>
* <span data-ttu-id="a3b3e-757">仮想ネットワーク ルール用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-757">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="a3b3e-758">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-758">Interactive Shell</span></span>
* <span data-ttu-id="a3b3e-759">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-759">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="a3b3e-760">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-760">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="a3b3e-761">IoT</span><span class="sxs-lookup"><span data-stu-id="a3b3e-761">IoT</span></span>
* <span data-ttu-id="a3b3e-762">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-762">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="a3b3e-763">Key Vault</span><span class="sxs-lookup"><span data-stu-id="a3b3e-763">Key Vault</span></span>
* <span data-ttu-id="a3b3e-764">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-764">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-765">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-765">Network</span></span>
* <span data-ttu-id="a3b3e-766">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-766">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="a3b3e-767">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-767">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="a3b3e-768">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-768">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="a3b3e-769">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-769">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="a3b3e-770">`--enable-tcp-reset` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-770">Add `--enable-tcp-reset` to</span></span> `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`
* <span data-ttu-id="a3b3e-771">`--disable-outbound-snat` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-771">Add `--disable-outbound-snat` to</span></span> `network lb rule create/update`
* <span data-ttu-id="a3b3e-772">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-772">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="a3b3e-773">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-773">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="a3b3e-774">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-774">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* `network express-route create/update`<span data-ttu-id="a3b3e-775">:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-775">: Add `--allow-global-reach` flag</span></span>
* `network vnet subnet create/update`<span data-ttu-id="a3b3e-776">:サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-776">: Add support for</span></span> `--delegation`
* <span data-ttu-id="a3b3e-777">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-777">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="a3b3e-778">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-778">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="a3b3e-779">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-779">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* `dns record-set * create/update`<span data-ttu-id="a3b3e-780">:サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-780">: Add support for</span></span> `--target-resource`
* <span data-ttu-id="a3b3e-781">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-781">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="a3b3e-782">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-782">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="a3b3e-783">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-783">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="a3b3e-784">RDBMS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-784">RDBMS</span></span>
* <span data-ttu-id="a3b3e-785">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-785">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="a3b3e-786">予約</span><span class="sxs-lookup"><span data-stu-id="a3b3e-786">Reservation</span></span>
* <span data-ttu-id="a3b3e-787">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-787">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="a3b3e-788">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-788">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="a3b3e-789">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="a3b3e-789">Manage App</span></span>
* <span data-ttu-id="a3b3e-790">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-790">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="a3b3e-791">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-791">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-792">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-792">Role</span></span>
* <span data-ttu-id="a3b3e-793">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-793">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="a3b3e-794">SignalR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-794">SignalR</span></span>
* <span data-ttu-id="a3b3e-795">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-795">First release</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-796">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-796">Storage</span></span>
* <span data-ttu-id="a3b3e-797">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-797">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="a3b3e-798">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-798">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-799">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-799">VM</span></span>
* <span data-ttu-id="a3b3e-800">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-800">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="a3b3e-801">共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-801">Added support for shared image gallery through</span></span> `az sig`

## <a name="august-28-2018"></a><span data-ttu-id="a3b3e-802">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-802">August 28, 2018</span></span>

<span data-ttu-id="a3b3e-803">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="a3b3e-803">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-804">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-804">Core</span></span>

* <span data-ttu-id="a3b3e-805">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-805">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="a3b3e-806">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-806">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-807">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-807">ACR</span></span>

* <span data-ttu-id="a3b3e-808">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-808">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="a3b3e-809">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-809">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-810">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-810">ACS</span></span>

* <span data-ttu-id="a3b3e-811">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-811">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="a3b3e-812">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-812">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-813">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-813">AppService</span></span>

* <span data-ttu-id="a3b3e-814">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-814">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="a3b3e-815">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-815">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="a3b3e-816">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-816">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="a3b3e-817">バックアップ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-817">Backup</span></span>

* <span data-ttu-id="a3b3e-818">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-818">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="a3b3e-819">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="a3b3e-819">Bot Service</span></span>

* <span data-ttu-id="a3b3e-820">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-820">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="a3b3e-821">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="a3b3e-821">Cognitive Services</span></span>

* <span data-ttu-id="a3b3e-822">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-822">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="a3b3e-823">IoT</span><span class="sxs-lookup"><span data-stu-id="a3b3e-823">IoT</span></span>

* <span data-ttu-id="a3b3e-824">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-824">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="a3b3e-825">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-825">Monitor</span></span>

* <span data-ttu-id="a3b3e-826">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-826">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="a3b3e-827">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-827">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-828">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-828">Network</span></span>

* <span data-ttu-id="a3b3e-829">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-829">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-830">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-830">Resource</span></span>

* <span data-ttu-id="a3b3e-831">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-831">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-832">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-832">Storage</span></span>

* <span data-ttu-id="a3b3e-833">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-833">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-834">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-834">VM</span></span>

* <span data-ttu-id="a3b3e-835">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-835">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="a3b3e-836">`--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-836">Deprecated `--storage-caching` for</span></span> `vm create`

## <a name="auguest-14-2018"></a><span data-ttu-id="a3b3e-837">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-837">Auguest 14, 2018</span></span>

<span data-ttu-id="a3b3e-838">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="a3b3e-838">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-839">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-839">Core</span></span>

* <span data-ttu-id="a3b3e-840">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-840">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="a3b3e-841">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-841">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="a3b3e-842">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-842">Telemetry</span></span>

* <span data-ttu-id="a3b3e-843">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-843">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-844">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-844">ACR</span></span>

* <span data-ttu-id="a3b3e-845">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-845">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="a3b3e-846">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-846">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-847">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-847">ACS</span></span>

* <span data-ttu-id="a3b3e-848">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-848">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="a3b3e-849">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-849">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="a3b3e-850">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-850">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="a3b3e-851">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-851">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="a3b3e-852">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-852">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="a3b3e-853">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-853">AppService</span></span>

* <span data-ttu-id="a3b3e-854">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-854">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="a3b3e-855">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-855">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="a3b3e-856">BatchAI</span><span class="sxs-lookup"><span data-stu-id="a3b3e-856">BatchAI</span></span>

* <span data-ttu-id="a3b3e-857">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-857">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="a3b3e-858">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-858">Container</span></span>

* <span data-ttu-id="a3b3e-859">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-859">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="a3b3e-860">IoT</span><span class="sxs-lookup"><span data-stu-id="a3b3e-860">IoT</span></span>

* <span data-ttu-id="a3b3e-861">[破壊的変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-861">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="a3b3e-862">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-862">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="a3b3e-863">Iot Central</span><span class="sxs-lookup"><span data-stu-id="a3b3e-863">Iot Central</span></span>

* <span data-ttu-id="a3b3e-864">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-864">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="a3b3e-865">KeyVault</span><span class="sxs-lookup"><span data-stu-id="a3b3e-865">KeyVault</span></span>


* <span data-ttu-id="a3b3e-866">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-866">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="a3b3e-867">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-867">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="a3b3e-868">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-868">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="a3b3e-869">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-869">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="a3b3e-870">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-870">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="a3b3e-871">リレー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-871">Relay</span></span>

* <span data-ttu-id="a3b3e-872">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-872">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-873">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-873">Sql</span></span>

* <span data-ttu-id="a3b3e-874">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-874">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-875">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-875">Storage</span></span>

* <span data-ttu-id="a3b3e-876">[破壊的変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-876">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="a3b3e-877">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-877">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="a3b3e-878">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-878">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="a3b3e-879">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-879">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="a3b3e-880">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-880">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-881">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-881">VM</span></span>

* <span data-ttu-id="a3b3e-882">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-882">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="a3b3e-883">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-883">July 31, 2018</span></span>

<span data-ttu-id="a3b3e-884">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="a3b3e-884">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-885">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-885">ACR</span></span>

* <span data-ttu-id="a3b3e-886">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-886">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="a3b3e-887">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-887">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-888">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-888">ACS</span></span>

* <span data-ttu-id="a3b3e-889">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-889">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="a3b3e-890">Batch</span><span class="sxs-lookup"><span data-stu-id="a3b3e-890">Batch</span></span>

* <span data-ttu-id="a3b3e-891">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-891">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-892">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-892">Container</span></span>

* <span data-ttu-id="a3b3e-893">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-893">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-894">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-894">Network</span></span>

* <span data-ttu-id="a3b3e-895">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-895">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="a3b3e-896">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-896">Resource</span></span>

* <span data-ttu-id="a3b3e-897">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-897">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="a3b3e-898">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-898">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-899">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-899">Role</span></span>

* <span data-ttu-id="a3b3e-900">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-900">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="a3b3e-901">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-901">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="a3b3e-902">Search</span><span class="sxs-lookup"><span data-stu-id="a3b3e-902">Search</span></span>

* <span data-ttu-id="a3b3e-903">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-903">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="a3b3e-904">Service Bus</span><span class="sxs-lookup"><span data-stu-id="a3b3e-904">Service Bus</span></span>

* <span data-ttu-id="a3b3e-905">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-905">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="a3b3e-906">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-906">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  `--enable-batched-operations` <span data-ttu-id="a3b3e-907">および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="a3b3e-907">and `--enable-dead-lettering-on-message-expiration` in</span></span> `queue`
  *  `--dead-letter-on-filter-exceptions` <span data-ttu-id="a3b3e-908">in</span><span class="sxs-lookup"><span data-stu-id="a3b3e-908">in</span></span> `subscriptions`

### <a name="storage"></a><span data-ttu-id="a3b3e-909">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-909">Storage</span></span>

* <span data-ttu-id="a3b3e-910">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-910">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="a3b3e-911">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-911">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-912">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-912">VM</span></span>

* <span data-ttu-id="a3b3e-913">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-913">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="a3b3e-914">サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-914">Added support for</span></span> `StandardSSD_LRS`
* <span data-ttu-id="a3b3e-915">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-915">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="a3b3e-916">[破壊的変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-916">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="a3b3e-917">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-917">July 18, 2018</span></span>

<span data-ttu-id="a3b3e-918">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="a3b3e-918">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-919">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-919">Core</span></span>

* <span data-ttu-id="a3b3e-920">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-920">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="a3b3e-921">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-921">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="a3b3e-922">[破壊的変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-922">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-923">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-923">ACR</span></span>

* <span data-ttu-id="a3b3e-924">[破壊的変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-924">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="a3b3e-925">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-925">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="a3b3e-926">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-926">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="a3b3e-927">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-927">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-928">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-928">ACS</span></span>

* <span data-ttu-id="a3b3e-929">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-929">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-930">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-930">AppService</span></span>

* <span data-ttu-id="a3b3e-931">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-931">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="a3b3e-932">Batch</span><span class="sxs-lookup"><span data-stu-id="a3b3e-932">Batch</span></span>

* <span data-ttu-id="a3b3e-933">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-933">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="a3b3e-934">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-934">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="a3b3e-935">Batch AI</span><span class="sxs-lookup"><span data-stu-id="a3b3e-935">Batch AI</span></span>

* <span data-ttu-id="a3b3e-936">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-936">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-937">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-937">Container</span></span>

* <span data-ttu-id="a3b3e-938">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-938">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="a3b3e-939">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-939">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-940">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-940">Network</span></span>

* <span data-ttu-id="a3b3e-941">`--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-941">Added `--no-wait` support to</span></span> `network nic [create|update|delete]` 
* <span data-ttu-id="a3b3e-942">追加済み</span><span class="sxs-lookup"><span data-stu-id="a3b3e-942">Added</span></span> `network nic wait`
* <span data-ttu-id="a3b3e-943">`--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-943">Deprecated `--ids` argument for</span></span> `network vnet [subnet|peering] list`
* <span data-ttu-id="a3b3e-944">出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-944">Added `--include-default` flag to include default security rules in the output of</span></span> `network nsg rule list`  

### <a name="resource"></a><span data-ttu-id="a3b3e-945">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-945">Resource</span></span>

* <span data-ttu-id="a3b3e-946">`--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-946">Added `--no-wait` support to</span></span> `group deployment delete`
* <span data-ttu-id="a3b3e-947">`--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-947">Added `--no-wait` support to</span></span> `deployment delete`
* <span data-ttu-id="a3b3e-948">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-948">Added `deployment wait` command</span></span>
* <span data-ttu-id="a3b3e-949">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-949">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-950">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-950">SQL</span></span>

* <span data-ttu-id="a3b3e-951">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-951">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="a3b3e-952">実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-952">Allow configuring default sql server by executing</span></span> `az configure --defaults sql-server=<name>`
* <span data-ttu-id="a3b3e-953">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-953">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-954">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-954">Storage</span></span>

* <span data-ttu-id="a3b3e-955">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-955">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-956">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-956">VM</span></span>

* <span data-ttu-id="a3b3e-957">[破壊的変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-957">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="a3b3e-958">`--no-wait` のサポートを `vm extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-958">Added `--no-wait` support to `vm extension [set|delete]` and</span></span> `vmss extension [set|delete]`
* <span data-ttu-id="a3b3e-959">追加済み</span><span class="sxs-lookup"><span data-stu-id="a3b3e-959">Added</span></span> `vm extension wait`

## <a name="july-3-2018"></a><span data-ttu-id="a3b3e-960">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-960">July 3, 2018</span></span>

<span data-ttu-id="a3b3e-961">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="a3b3e-961">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="a3b3e-962">AKS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-962">AKS</span></span>

* <span data-ttu-id="a3b3e-963">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-963">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="a3b3e-964">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-964">July 3, 2018</span></span>

<span data-ttu-id="a3b3e-965">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="a3b3e-965">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-966">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-966">Core</span></span>

* <span data-ttu-id="a3b3e-967">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-967">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-968">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-968">ACR</span></span>

* <span data-ttu-id="a3b3e-969">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-969">Added polling build status</span></span>
* <span data-ttu-id="a3b3e-970">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-970">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="a3b3e-971">`--top` パラメーターと `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-971">Added `--top` and `--orderby` parameters for</span></span> `show-manifests`

### <a name="acs"></a><span data-ttu-id="a3b3e-972">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-972">ACS</span></span>

* <span data-ttu-id="a3b3e-973">[破壊的変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-973">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="a3b3e-974">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-974">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="a3b3e-975">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-975">Updated options for `aks browse` command.</span></span> <span data-ttu-id="a3b3e-976">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-976">Added `--listen-port` support</span></span>
* <span data-ttu-id="a3b3e-977">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-977">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="a3b3e-978">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-978">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="a3b3e-979">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-979">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-980">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-980">AppService</span></span>

* <span data-ttu-id="a3b3e-981">ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-981">Added support for disabling identity via</span></span> `webapp identity remove`
* <span data-ttu-id="a3b3e-982">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-982">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="a3b3e-983">バックアップ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-983">Backup</span></span>

* <span data-ttu-id="a3b3e-984">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-984">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="a3b3e-985">BatchAI</span><span class="sxs-lookup"><span data-stu-id="a3b3e-985">BatchAI</span></span>

* <span data-ttu-id="a3b3e-986">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-986">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="a3b3e-987">クラウド</span><span class="sxs-lookup"><span data-stu-id="a3b3e-987">Cloud</span></span>

* <span data-ttu-id="a3b3e-988">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-988">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-989">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-989">Container</span></span>

* <span data-ttu-id="a3b3e-990">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-990">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="a3b3e-991">Log Analytics の `--log-analytics-workspace` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-991">Added Log Analytics parameters `--log-analytics-workspace` and</span></span> `--log-analytics-workspace-key`
* <span data-ttu-id="a3b3e-992">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-992">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="a3b3e-993">拡張機能</span><span class="sxs-lookup"><span data-stu-id="a3b3e-993">Extension</span></span>

* <span data-ttu-id="a3b3e-994">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-994">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-995">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-995">Network</span></span>

* <span data-ttu-id="a3b3e-996">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-996">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="a3b3e-997">Rdbms</span><span class="sxs-lookup"><span data-stu-id="a3b3e-997">Rdbms</span></span>

* <span data-ttu-id="a3b3e-998">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-998">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-999">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-999">Resource</span></span>

* <span data-ttu-id="a3b3e-1000">新しい操作グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1000">Added new operation group</span></span> `deployment`

### <a name="vm"></a><span data-ttu-id="a3b3e-1001">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1001">VM</span></span>

* <span data-ttu-id="a3b3e-1002">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1002">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="a3b3e-1003">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1003">June 25, 2018</span></span>

<span data-ttu-id="a3b3e-1004">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1004">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="a3b3e-1005">CLI</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1005">CLI</span></span>

* <span data-ttu-id="a3b3e-1006">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1006">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="a3b3e-1007">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1007">June 19, 2018</span></span>

<span data-ttu-id="a3b3e-1008">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1008">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-1009">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1009">Core</span></span>

* <span data-ttu-id="a3b3e-1010">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1010">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-1011">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1011">ACR</span></span>

* <span data-ttu-id="a3b3e-1012">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1012">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="a3b3e-1013">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1013">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-1014">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1014">ACS</span></span>

* <span data-ttu-id="a3b3e-1015">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1015">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="a3b3e-1016">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1016">Added `--update` support</span></span>
* <span data-ttu-id="a3b3e-1017">ユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1017">Changed `aks get-credentials --admin` to not eplace the user context in</span></span> `$HOME/.kube/config`
* <span data-ttu-id="a3b3e-1018">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1018">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="a3b3e-1019">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1019">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="a3b3e-1020">`aks install-connector` および `aks upgrade-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1020">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and</span></span> `aks remove-connector`
* <span data-ttu-id="a3b3e-1021">新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1021">Added new Azure Container Instance regions for</span></span> `aks install-connector`
* <span data-ttu-id="a3b3e-1022">Helm のリリース名とノード名への正規化された場所を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1022">Added the normalized location into the helm release name and node name to</span></span> `aks install-connector`

### <a name="appservice"></a><span data-ttu-id="a3b3e-1023">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1023">AppService</span></span>

* <span data-ttu-id="a3b3e-1024">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1024">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="a3b3e-1025">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1025">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="a3b3e-1026">Batch</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1026">Batch</span></span>

* <span data-ttu-id="a3b3e-1027">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1027">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="a3b3e-1028">Batch AI</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1028">Batch AI</span></span>

* <span data-ttu-id="a3b3e-1029">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1029">Added support for workspaces.</span></span> <span data-ttu-id="a3b3e-1030">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1030">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="a3b3e-1031">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1031">Added support for experiments.</span></span> <span data-ttu-id="a3b3e-1032">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1032">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="a3b3e-1033">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1033">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="a3b3e-1034">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1034">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="a3b3e-1035">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1035">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="a3b3e-1036">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1036">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="a3b3e-1037">[破壊的変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1037">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="a3b3e-1038">[破壊的変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1038">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="a3b3e-1039">[破壊的変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1039">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="a3b3e-1040">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1040">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="a3b3e-1041">[破壊的変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1041">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="a3b3e-1042">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1042">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="a3b3e-1043">[破壊的変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1043">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="a3b3e-1044">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1044">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="a3b3e-1045">[破壊的変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1045">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="a3b3e-1046">[破壊的変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1046">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="a3b3e-1047">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1047">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="a3b3e-1048">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1048">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="a3b3e-1049">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1049">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="a3b3e-1050">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1050">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="a3b3e-1051">マップ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1051">Maps</span></span>

* <span data-ttu-id="a3b3e-1052">[破壊的変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1052">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1053">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1053">Network</span></span>

* <span data-ttu-id="a3b3e-1054">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1054">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="a3b3e-1055">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1055">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="a3b3e-1056">#6502</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1056">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="a3b3e-1057">Reservations</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1057">Reservations</span></span>

* <span data-ttu-id="a3b3e-1058">[破壊的変更] 必須パラメーター `ReservedResourceType` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1058">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to</span></span> `reservations catalog show`
* <span data-ttu-id="a3b3e-1059">`Location` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1059">Added parameter `Location`to</span></span> `reservations catalog show`
* <span data-ttu-id="a3b3e-1060">[破壊的変更] `kind` を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1060">[BREAKING CHANGE] Removed `kind` from</span></span> `ReservationProperties`
* <span data-ttu-id="a3b3e-1061">[破壊的変更] `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1061">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in</span></span> `Catalog`
* <span data-ttu-id="a3b3e-1062">[破壊的変更] `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1062">[BREAKING CHANGE] Removed `size` and `tier` properties from</span></span> `Catalog`
* <span data-ttu-id="a3b3e-1063">`InstanceFlexibility` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1063">Added parameter `InstanceFlexibility` to</span></span> `reservations reservation update`

### <a name="role"></a><span data-ttu-id="a3b3e-1064">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1064">Role</span></span>

* <span data-ttu-id="a3b3e-1065">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1065">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-1066">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1066">SQL</span></span>

* <span data-ttu-id="a3b3e-1067">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1067">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-1068">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1068">Storage</span></span>

* <span data-ttu-id="a3b3e-1069">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1069">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1070">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1070">VM</span></span>

* <span data-ttu-id="a3b3e-1071">高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1071">Improved refine vm size check for accelerated networking support in</span></span> `vm create`
* <span data-ttu-id="a3b3e-1072">既定の VM サイズが `Standard_D1_v2` から切り替わるという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1072">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to</span></span> `Standard_DS1_v2`
* <span data-ttu-id="a3b3e-1073">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1073">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="a3b3e-1074">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1074">June 13, 2018</span></span>

<span data-ttu-id="a3b3e-1075">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1075">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-1076">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1076">Core</span></span>

* <span data-ttu-id="a3b3e-1077">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1077">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="a3b3e-1078">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1078">June 13, 2018</span></span>

<span data-ttu-id="a3b3e-1079">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1079">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="a3b3e-1080">AKS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1080">AKS</span></span>

* <span data-ttu-id="a3b3e-1081">高度なネットワーク オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1081">Added advanced networking options to</span></span> `aks create`
* <span data-ttu-id="a3b3e-1082">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1082">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="a3b3e-1083">`--no-ssh-key` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1083">Added `--no-ssh-key` argument to</span></span> `aks create`
* <span data-ttu-id="a3b3e-1084">`--enable-rbac` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1084">Added `--enable-rbac` argument to</span></span> `aks create`
* <span data-ttu-id="a3b3e-1085">[プレビュー] Azure Active Directory 認証のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1085">[PREVIEW] Added support for Azure Active Directory authentication to</span></span> `aks create`

### <a name="appservice"></a><span data-ttu-id="a3b3e-1086">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1086">AppService</span></span>

* <span data-ttu-id="a3b3e-1087">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1087">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="a3b3e-1088">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1088">June 5, 2018</span></span>

<span data-ttu-id="a3b3e-1089">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1089">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="a3b3e-1090">Interactive</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1090">Interactive</span></span>

* <span data-ttu-id="a3b3e-1091">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1091">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="a3b3e-1092">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1092">June 5, 2018</span></span>

<span data-ttu-id="a3b3e-1093">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1093">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-1094">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1094">Core</span></span>

* <span data-ttu-id="a3b3e-1095">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1095">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="a3b3e-1096">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1096">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-1097">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1097">ACR</span></span>

* <span data-ttu-id="a3b3e-1098">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1098">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="a3b3e-1099">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1099">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="a3b3e-1100">AKS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1100">AKS</span></span>

* <span data-ttu-id="a3b3e-1101">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1101">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="a3b3e-1102">Batch</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1102">Batch</span></span>

* <span data-ttu-id="a3b3e-1103">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1103">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="a3b3e-1104">IoT</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1104">IOT</span></span>

* <span data-ttu-id="a3b3e-1105">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1105">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1106">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1106">Network</span></span>

* <span data-ttu-id="a3b3e-1107">強化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1107">Improved</span></span> `network vnet peering`

### <a name="policy-insights"></a><span data-ttu-id="a3b3e-1108">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1108">Policy Insights</span></span>

* <span data-ttu-id="a3b3e-1109">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1109">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="a3b3e-1110">ARM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1110">ARM</span></span>

* <span data-ttu-id="a3b3e-1111">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1111">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-1112">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1112">SQL</span></span>

* <span data-ttu-id="a3b3e-1113">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1113">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="a3b3e-1114">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1114">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="a3b3e-1115">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1115">Storage</span></span>

* <span data-ttu-id="a3b3e-1116">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1116">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1117">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1117">VM</span></span>

* <span data-ttu-id="a3b3e-1118">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1118">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="a3b3e-1119">`--accelerated-networking` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1119">Added `--accelerated-networking` option to</span></span> `vm create`
* <span data-ttu-id="a3b3e-1120">`--tags` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1120">Added `--tags` to</span></span> `identity create`

## <a name="may-22-2018"></a><span data-ttu-id="a3b3e-1121">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1121">May 22, 2018</span></span>

<span data-ttu-id="a3b3e-1122">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1122">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-1123">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1123">Core</span></span>

* <span data-ttu-id="a3b3e-1124">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1124">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-1125">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1125">ACS</span></span>

* <span data-ttu-id="a3b3e-1126">新しい Dev Space コマンド `aks use-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1126">Added new Dev-Spaces commands `aks use-dev-spaces` and</span></span> `aks remove-dev-spaces`
* <span data-ttu-id="a3b3e-1127">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1127">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-1128">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1128">AppService</span></span>

* <span data-ttu-id="a3b3e-1129">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1129">Improved generic update commands</span></span>
* <span data-ttu-id="a3b3e-1130">非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1130">Added async support for</span></span> `webapp deployment source config-zip`

### <a name="container"></a><span data-ttu-id="a3b3e-1131">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1131">Container</span></span>

* <span data-ttu-id="a3b3e-1132">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1132">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="a3b3e-1133">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1133">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="a3b3e-1134">拡張機能</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1134">Extension</span></span>

* <span data-ttu-id="a3b3e-1135">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1135">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="a3b3e-1136">Interactive</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1136">Interactive</span></span>

* <span data-ttu-id="a3b3e-1137">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1137">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="a3b3e-1138">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1138">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="a3b3e-1139">KeyVault</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1139">KeyVault</span></span>

* <span data-ttu-id="a3b3e-1140">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1140">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1141">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1141">Network</span></span>

* <span data-ttu-id="a3b3e-1142">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1142">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="a3b3e-1143">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1143">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-1144">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1144">SQL</span></span>

* <span data-ttu-id="a3b3e-1145">[破壊的変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1145">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="a3b3e-1146">`serviceLevelObjective` プロパティの名前を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1146">Renamed `serviceLevelObjective` property to</span></span> `currentServiceObjectiveName`
    * <span data-ttu-id="a3b3e-1147">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1147">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="a3b3e-1148">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1148">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="a3b3e-1149">[破壊的変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1149">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * `requestedServiceObjectiveName`<span data-ttu-id="a3b3e-1150">。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1150">.</span></span>  <span data-ttu-id="a3b3e-1151">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1151">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * `edition`<span data-ttu-id="a3b3e-1152">。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1152">.</span></span> <span data-ttu-id="a3b3e-1153">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1153">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * `elasticPoolName`<span data-ttu-id="a3b3e-1154">。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1154">.</span></span> <span data-ttu-id="a3b3e-1155">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1155">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="a3b3e-1156">[破壊的変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1156">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * `edition`<span data-ttu-id="a3b3e-1157">。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1157">.</span></span> <span data-ttu-id="a3b3e-1158">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1158">To update, use the `--edition` parameter</span></span>
    * `dtu`<span data-ttu-id="a3b3e-1159">。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1159">.</span></span> <span data-ttu-id="a3b3e-1160">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1160">To update, use the `--capacity` parameter</span></span>
    *  `databaseDtuMin`<span data-ttu-id="a3b3e-1161">。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1161">.</span></span> <span data-ttu-id="a3b3e-1162">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1162">To update, use the `--db-min-capacity` parameter</span></span>
    *  `databaseDtuMax`<span data-ttu-id="a3b3e-1163">。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1163">.</span></span> <span data-ttu-id="a3b3e-1164">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1164">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="a3b3e-1165">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1165">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="a3b3e-1166">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1166">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-1167">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1167">Storage</span></span>

* <span data-ttu-id="a3b3e-1168">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1168">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="a3b3e-1169">問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1169">Fixed problem with</span></span> `storage entity query`

### <a name="vm"></a><span data-ttu-id="a3b3e-1170">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1170">VM</span></span>

* <span data-ttu-id="a3b3e-1171">[破壊的変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1171">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="a3b3e-1172">同じサポートに、`vm update` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1172">The same support can be accessed through `vm update` or</span></span> `vm disk attach`
* <span data-ttu-id="a3b3e-1173">一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1173">Fixed extension image matching in</span></span> `[vm|vmss] extension`
* <span data-ttu-id="a3b3e-1174">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1174">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="a3b3e-1175">`--license-type` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1175">Added `--license-type` to</span></span> `[vm|vmss] update`

## <a name="may-7-2018"></a><span data-ttu-id="a3b3e-1176">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1176">May 7, 2018</span></span>

<span data-ttu-id="a3b3e-1177">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1177">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-1178">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1178">Core</span></span>

* <span data-ttu-id="a3b3e-1179">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1179">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="a3b3e-1180">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1180">Added limited support for positional arguments</span></span>
* <span data-ttu-id="a3b3e-1181">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1181">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="a3b3e-1182">#5591</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1182">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="a3b3e-1183">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1183">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="a3b3e-1184">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1184">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="a3b3e-1185">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1185">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="a3b3e-1186">ユーザーが入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1186">Improved error when users type</span></span> `az ''`
* <span data-ttu-id="a3b3e-1187">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1187">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-1188">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1188">ACR</span></span>

* <span data-ttu-id="a3b3e-1189">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1189">Added ACR Build commands</span></span>
* <span data-ttu-id="a3b3e-1190">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1190">Improved resource not found error messages</span></span>
* <span data-ttu-id="a3b3e-1191">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1191">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="a3b3e-1192">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1192">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="a3b3e-1193">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1193">Improved repository commands error messages</span></span>
* <span data-ttu-id="a3b3e-1194">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1194">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-1195">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1195">ACS</span></span>

* <span data-ttu-id="a3b3e-1196">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1196">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="a3b3e-1197">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1197">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="a3b3e-1198">AMS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1198">AMS</span></span>

* <span data-ttu-id="a3b3e-1199">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1199">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-1200">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1200">Appservice</span></span>

* <span data-ttu-id="a3b3e-1201">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1201">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="a3b3e-1202">`--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1202">Removed `--runtime-version` from</span></span> `webapp auth update`
* <span data-ttu-id="a3b3e-1203">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1203">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="a3b3e-1204">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1204">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="a3b3e-1205">Batch AI</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1205">Batch AI</span></span>

* <span data-ttu-id="a3b3e-1206">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1206">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="a3b3e-1207">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1207">Cognitive Services</span></span>

* <span data-ttu-id="a3b3e-1208">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1208">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="a3b3e-1209">消費</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1209">Consumption</span></span>

* <span data-ttu-id="a3b3e-1210">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1210">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-1211">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1211">Container</span></span>

* <span data-ttu-id="a3b3e-1212">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1212">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="a3b3e-1213">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1213">Cosmos DB</span></span>

* <span data-ttu-id="a3b3e-1214">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1214">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="a3b3e-1215">DMS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1215">DMS</span></span>

* <span data-ttu-id="a3b3e-1216">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1216">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="a3b3e-1217">拡張機能</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1217">Extension</span></span>

* <span data-ttu-id="a3b3e-1218">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1218">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="a3b3e-1219">Interactive</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1219">Interactive</span></span>

* <span data-ttu-id="a3b3e-1220">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1220">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="a3b3e-1221">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1221">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="a3b3e-1222">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1222">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="a3b3e-1223">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1223">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="a3b3e-1224">ラボ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1224">Lab</span></span>

* <span data-ttu-id="a3b3e-1225">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1225">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1226">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1226">Network</span></span>

* <span data-ttu-id="a3b3e-1227">[破壊的変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1227">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="a3b3e-1228">プロファイル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1228">Profile</span></span>

* <span data-ttu-id="a3b3e-1229">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1229">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="a3b3e-1230">[破壊的変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1230">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="a3b3e-1231">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1231">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="a3b3e-1232">Redis</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1232">Redis</span></span>

* <span data-ttu-id="a3b3e-1233">`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1233">Deprecated `redis patch-schedule patch-schedule show` in favor of</span></span> `redis patch-schedule show`
* <span data-ttu-id="a3b3e-1234">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1234">Deprecated `redis list-all`.</span></span> <span data-ttu-id="a3b3e-1235">この機能は組み込まれました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1235">This functionality has been folded into</span></span> `redis list`
* <span data-ttu-id="a3b3e-1236">`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1236">Deprecated `redis import-method` in favor of</span></span> `redis import`
* <span data-ttu-id="a3b3e-1237">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1237">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-1238">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1238">Role</span></span>

* <span data-ttu-id="a3b3e-1239">[破壊的変更] 非推奨を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1239">[BREAKING CHANGE] Removed deprecated</span></span> `ad sp reset-credentials`

### <a name="storage"></a><span data-ttu-id="a3b3e-1240">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1240">Storage</span></span>

* <span data-ttu-id="a3b3e-1241">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1241">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="a3b3e-1242">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1242">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="a3b3e-1243">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1243">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="a3b3e-1244">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1244">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="a3b3e-1245">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1245">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1246">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1246">VM</span></span>

* <span data-ttu-id="a3b3e-1247">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1247">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="a3b3e-1248">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1248">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="a3b3e-1249">[破壊的変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1249">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="a3b3e-1250">削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1250">Added support for eviction policy to</span></span> `vmss`
* <span data-ttu-id="a3b3e-1251">[破壊的変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1251">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="a3b3e-1252">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1252">Added write accelerator support</span></span>
* <span data-ttu-id="a3b3e-1253">追加済み</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1253">Added</span></span> `vmss perform-maintenance`
* <span data-ttu-id="a3b3e-1254">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1254">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="a3b3e-1255">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1255">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="a3b3e-1256">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1256">April 10, 2018</span></span>

<span data-ttu-id="a3b3e-1257">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1257">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-1258">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1258">ACR</span></span>

* <span data-ttu-id="a3b3e-1259">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1259">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-1260">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1260">ACS</span></span>

* <span data-ttu-id="a3b3e-1261">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1261">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-1262">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1262">Appservice</span></span>

* [<span data-ttu-id="a3b3e-1263">破壊的変更</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1263">BREAKING CHANGE</span></span>]: Removed `assign-identity`
* <span data-ttu-id="a3b3e-1264">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1264">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="a3b3e-1265">BatchAI</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1265">BatchAI</span></span>

* <span data-ttu-id="a3b3e-1266">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1266">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="a3b3e-1267">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1267">Job level mounting</span></span>
  - <span data-ttu-id="a3b3e-1268">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1268">Environment variables with secret values</span></span>
  - <span data-ttu-id="a3b3e-1269">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1269">Performance counters settings</span></span>
  - <span data-ttu-id="a3b3e-1270">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1270">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="a3b3e-1271">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1271">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="a3b3e-1272">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1272">Usage and limits reporting</span></span>
  - <span data-ttu-id="a3b3e-1273">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1273">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="a3b3e-1274">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1274">Support for custom images</span></span>
  - <span data-ttu-id="a3b3e-1275">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1275">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="a3b3e-1276">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1276">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="a3b3e-1277">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1277">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="a3b3e-1278">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1278">National clouds are supported</span></span>
* <span data-ttu-id="a3b3e-1279">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1279">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="a3b3e-1280">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1280">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="a3b3e-1281">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1281">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="a3b3e-1282">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1282">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="a3b3e-1283">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1283">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="a3b3e-1284">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1284">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="a3b3e-1285">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1285">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="a3b3e-1286">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1286">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="a3b3e-1287">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1287">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="a3b3e-1288">`--generate-ssh-keys` オプションを `cluster create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1288">Added `--generate-ssh-keys` option to `cluster create` and</span></span> `file-server create`
* <span data-ttu-id="a3b3e-1289">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1289">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="a3b3e-1290">[破壊的変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1290">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="a3b3e-1291">[破壊的変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1291">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="a3b3e-1292">課金</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1292">Billing</span></span>

* <span data-ttu-id="a3b3e-1293">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1293">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="a3b3e-1294">消費</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1294">Consumption</span></span>

* <span data-ttu-id="a3b3e-1295">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1295">Added `marketplace` commands</span></span>
* <span data-ttu-id="a3b3e-1296">[破壊的変更] 名前を `reservations summaries` から変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1296">[BREAKING CHANGE] Renamed `reservations summaries` to</span></span> `reservation summary`
* <span data-ttu-id="a3b3e-1297">[破壊的変更] 名前を `reservations details` から変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1297">[BREAKING CHANGE] Renamed `reservations details` to</span></span> `reservation detail`
* <span data-ttu-id="a3b3e-1298">[破壊的変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1298">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="a3b3e-1299">[破壊的変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1299">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="a3b3e-1300">[破壊的変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1300">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-1301">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1301">Container</span></span>

* <span data-ttu-id="a3b3e-1302">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、および `--gitrepo-revision` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1302">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and</span></span> `--gitrepo-mount-path`
* <span data-ttu-id="a3b3e-1303">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1303">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="a3b3e-1304">拡張機能</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1304">Extension</span></span>

* <span data-ttu-id="a3b3e-1305">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1305">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="a3b3e-1306">Interactive</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1306">Interactive</span></span>

* <span data-ttu-id="a3b3e-1307">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1307">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="a3b3e-1308">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1308">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="a3b3e-1309">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1309">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1310">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1310">Network</span></span>

* <span data-ttu-id="a3b3e-1311">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1311">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="a3b3e-1312">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1312">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="a3b3e-1313">#4910</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1313">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="a3b3e-1314">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1314">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="a3b3e-1315">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1315">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="a3b3e-1316">`--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1316">Fixed issue with `--disable-bgp-route-propagation` flag in</span></span> `network route-table [create|update]`
* <span data-ttu-id="a3b3e-1317">ダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1317">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for</span></span> `network lb [create|update]`
* <span data-ttu-id="a3b3e-1318">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1318">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and</span></span> `network dns record-set txt add-record`

### <a name="profile"></a><span data-ttu-id="a3b3e-1319">プロファイル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1319">Profile</span></span>

* <span data-ttu-id="a3b3e-1320">Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1320">Added support for Azure Classic accounts in</span></span> `account list`
* <span data-ttu-id="a3b3e-1321">[破壊的変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1321">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="a3b3e-1322">RDBMS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1322">RDBMS</span></span>

* <span data-ttu-id="a3b3e-1323">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1323">Added `georestore` command</span></span>
* <span data-ttu-id="a3b3e-1324">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1324">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-1325">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1325">Resource</span></span>

* <span data-ttu-id="a3b3e-1326">`--metadata` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1326">Added support for `--metadata` to</span></span> `policy definition create`
* <span data-ttu-id="a3b3e-1327">`--metadata`、`--set`、`--add`、`--remove` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1327">Added support for `--metadata`, `--set`, `--add`, `--remove` to</span></span> `policy definition update`

### <a name="sql"></a><span data-ttu-id="a3b3e-1328">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1328">SQL</span></span>

* <span data-ttu-id="a3b3e-1329">`sql elastic-pool op list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1329">Added `sql elastic-pool op list` and</span></span> `sql elastic-pool op cancel`

### <a name="storage"></a><span data-ttu-id="a3b3e-1330">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1330">Storage</span></span>

* <span data-ttu-id="a3b3e-1331">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1331">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1332">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1332">VM</span></span>

* <span data-ttu-id="a3b3e-1333">プラットフォーム障害ドメイン数の構成サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1333">Added support to configure platform fault domain count to</span></span> `vmss create`
* <span data-ttu-id="a3b3e-1334">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1334">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [<span data-ttu-id="a3b3e-1335">破壊的変更</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1335">BREAKING CHANGE</span></span>]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret`
* <span data-ttu-id="a3b3e-1336">Public-IP SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1336">Added support for Public-IP SKU to</span></span> `vm create`
* <span data-ttu-id="a3b3e-1337">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1337">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="a3b3e-1338">#5718</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1338">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="a3b3e-1339">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1339">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="a3b3e-1340">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1340">March 27, 2018</span></span>

<span data-ttu-id="a3b3e-1341">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1341">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-1342">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1342">Core</span></span>

* <span data-ttu-id="a3b3e-1343">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1343">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-1344">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1344">ACS</span></span>

* <span data-ttu-id="a3b3e-1345">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1345">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-1346">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1346">Appservice</span></span>

* <span data-ttu-id="a3b3e-1347">HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1347">Added HTTPS-only support to</span></span> `webapp update`
* <span data-ttu-id="a3b3e-1348">`az webapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1348">Added support for slots to `az webapp identity [assign|show]` and</span></span> `az functionapp identity [assign|show]`

### <a name="backup"></a><span data-ttu-id="a3b3e-1349">バックアップ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1349">Backup</span></span>

* <span data-ttu-id="a3b3e-1350">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1350">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="a3b3e-1351">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1351">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="a3b3e-1352">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1352">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="a3b3e-1353">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1353">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-1354">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1354">Container</span></span>

* <span data-ttu-id="a3b3e-1355">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1355">Added `container exec` command.</span></span> <span data-ttu-id="a3b3e-1356">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1356">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="a3b3e-1357">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1357">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="a3b3e-1358">拡張機能</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1358">Extension</span></span>

* <span data-ttu-id="a3b3e-1359">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1359">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="a3b3e-1360">完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1360">Changed `extension list-available` to show full extension data with</span></span> `--show-details`
* <span data-ttu-id="a3b3e-1361">[破壊的変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1361">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="a3b3e-1362">Interactive</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1362">Interactive</span></span>

* <span data-ttu-id="a3b3e-1363">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1363">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="a3b3e-1364">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1364">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="a3b3e-1365">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1365">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="a3b3e-1366">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1366">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="a3b3e-1367">ラボ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1367">Lab</span></span>

* <span data-ttu-id="a3b3e-1368">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1368">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="a3b3e-1369">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1369">Monitor</span></span>

* <span data-ttu-id="a3b3e-1370">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1370">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="a3b3e-1371">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1371">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="a3b3e-1372">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1372">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1373">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1373">Network</span></span>

* <span data-ttu-id="a3b3e-1374">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1374">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="a3b3e-1375">プロファイル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1375">Profile</span></span>

* <span data-ttu-id="a3b3e-1376">`--identity-port` と `--msi-port` の警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1376">Added warning for `--identity-port` and `--msi-port` to</span></span> `login`

### <a name="rdbms"></a><span data-ttu-id="a3b3e-1377">RDBMS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1377">RDBMS</span></span>

* <span data-ttu-id="a3b3e-1378">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1378">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-1379">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1379">Resource</span></span>

* [<span data-ttu-id="a3b3e-1380">破壊的変更</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1380">BREAKING CHANGE</span></span>]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="a3b3e-1381">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1381">Role</span></span>

* <span data-ttu-id="a3b3e-1382">必要なアクセス権の構成とネイティブ クライアントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1382">Added support for required access configurations and native clients to</span></span> `az ad app create`
* <span data-ttu-id="a3b3e-1383">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1383">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="a3b3e-1384">資格情報管理コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1384">Added credential management commands</span></span> `ad sp credential [reset|list|delete]`
* <span data-ttu-id="a3b3e-1385">[破壊的変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1385">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="a3b3e-1386">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1386">Added support for `dataActions` and `notDataActions` permissions to</span></span> `role definition`

### <a name="storage"></a><span data-ttu-id="a3b3e-1387">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1387">Storage</span></span>

* <span data-ttu-id="a3b3e-1388">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1388">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="a3b3e-1389">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1389">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1390">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1390">VM</span></span>

* <span data-ttu-id="a3b3e-1391">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1391">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="a3b3e-1392">ゾーン回復性のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1392">Added zone resilient support to</span></span> `vm [snapshot|image]`
* <span data-ttu-id="a3b3e-1393">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1393">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="a3b3e-1394">[破壊的変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1394">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="a3b3e-1395">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1395">March 13, 2018</span></span>

<span data-ttu-id="a3b3e-1396">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1396">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-1397">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1397">ACR</span></span>

* <span data-ttu-id="a3b3e-1398">`--image` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1398">Added support for `--image` parameter to</span></span> `repository delete`
* <span data-ttu-id="a3b3e-1399">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1399">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="a3b3e-1400">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1400">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-1401">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1401">ACS</span></span>

* <span data-ttu-id="a3b3e-1402">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1402">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="a3b3e-1403">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1403">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="a3b3e-1404">Advisor</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1404">Advisor</span></span>

* <span data-ttu-id="a3b3e-1405">[破壊的変更] 名前を `advisor configuration get` から変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1405">[BREAKING CHANGE] Renamed `advisor configuration get` to</span></span> `advisor configuration list`
* <span data-ttu-id="a3b3e-1406">[破壊的変更] 名前を `advisor configuration set` から変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1406">[BREAKING CHANGE] Renamed `advisor configuration set` to</span></span> `advisor configuration update`
* <span data-ttu-id="a3b3e-1407">[破壊的変更] 削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1407">[BREAKING CHANGE] Removed</span></span> `advisor recommendation generate`
* <span data-ttu-id="a3b3e-1408">`--refresh` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1408">Added `--refresh` parameter to</span></span> `advisor recommendation list`
* <span data-ttu-id="a3b3e-1409">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1409">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-1410">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1410">Appservice</span></span>

* <span data-ttu-id="a3b3e-1411">非推奨</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1411">Deprecated</span></span> `[webapp|functionapp] assign-identity`
* <span data-ttu-id="a3b3e-1412">マネージド ID コマンド `webapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1412">Added managed identity commands `webapp identity [assign|show]` and</span></span> `functionapp identity [assign|show]`

### <a name="eventhubs"></a><span data-ttu-id="a3b3e-1413">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1413">Eventhubs</span></span>

* <span data-ttu-id="a3b3e-1414">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1414">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="a3b3e-1415">拡張機能</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1415">Extension</span></span>

* <span data-ttu-id="a3b3e-1416">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1416">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="a3b3e-1417">Interactive</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1417">Interactive</span></span>

* <span data-ttu-id="a3b3e-1418">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1418">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="a3b3e-1419">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1419">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="a3b3e-1420">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1420">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="a3b3e-1421">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1421">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="a3b3e-1422">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1422">Monitor</span></span>

* <span data-ttu-id="a3b3e-1423">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1423">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="a3b3e-1424">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1424">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="a3b3e-1425">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1425">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="a3b3e-1426">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1426">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1427">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1427">Network</span></span>

* <span data-ttu-id="a3b3e-1428">[破壊的変更] `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1428">[BREAKING CHANGE] Removed `--tags` parameter from</span></span>  `route-filter rule create`
* <span data-ttu-id="a3b3e-1429">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1429">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="a3b3e-1430">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1430">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="a3b3e-1431">`--vnet` および `--subnet` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1431">Added `--vnet` and `--subnet` parameters to</span></span> `network watcher show-topology`

### <a name="profile"></a><span data-ttu-id="a3b3e-1432">プロファイル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1432">Profile</span></span>

* <span data-ttu-id="a3b3e-1433">`--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1433">Deprecated `--msi` parameter for</span></span> `az login`
* <span data-ttu-id="a3b3e-1434">`az login` の `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1434">Added `--identity` parameter for `az login` to replace</span></span> `--msi`

### <a name="rdbms"></a><span data-ttu-id="a3b3e-1435">RDBMS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1435">RDBMS</span></span>

* <span data-ttu-id="a3b3e-1436">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1436">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="a3b3e-1437">Service Bus</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1437">Service Bus</span></span>

* <span data-ttu-id="a3b3e-1438">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1438">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-1439">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1439">Storage</span></span>

* <span data-ttu-id="a3b3e-1440">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1440">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="a3b3e-1441">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1441">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1442">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1442">VM</span></span>

* <span data-ttu-id="a3b3e-1443">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1443">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="a3b3e-1444">`[vm|vmss] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1444">Deprecated `[vm|vmss] assign-identity` and</span></span> `[vm|vmss] remove-identity`
* <span data-ttu-id="a3b3e-1445">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1445">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="a3b3e-1446">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1446">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="a3b3e-1447">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1447">February 27, 2018</span></span>

<span data-ttu-id="a3b3e-1448">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1448">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-1449">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1449">Core</span></span>

* <span data-ttu-id="a3b3e-1450">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1450">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="a3b3e-1451">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1451">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="a3b3e-1452">HTTP ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1452">Added HTTP logging to</span></span> `--debug`

### <a name="acs"></a><span data-ttu-id="a3b3e-1453">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1453">ACS</span></span>

* <span data-ttu-id="a3b3e-1454">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1454">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="a3b3e-1455">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1455">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="a3b3e-1456">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1456">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to</span></span> `aks install-connector`
* <span data-ttu-id="a3b3e-1457">非推奨に関する通知を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1457">Removed deprecation notice from</span></span> `aks get-versions`

### <a name="appservice"></a><span data-ttu-id="a3b3e-1458">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1458">Appservice</span></span>

* <span data-ttu-id="a3b3e-1459">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1459">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="a3b3e-1460">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1460">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="a3b3e-1461">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1461">Cognitive Services</span></span>

* <span data-ttu-id="a3b3e-1462">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1462">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="a3b3e-1463">消費</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1463">Consumption</span></span>

* <span data-ttu-id="a3b3e-1464">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1464">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="a3b3e-1465">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1465">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-1466">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1466">Container</span></span>

* <span data-ttu-id="a3b3e-1467">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1467">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1468">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1468">Network</span></span>

* <span data-ttu-id="a3b3e-1469">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:クライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1469">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in</span></span> `network vnet-gateway vpn-client generate`

### <a name="resource"></a><span data-ttu-id="a3b3e-1470">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1470">Resource</span></span>

* <span data-ttu-id="a3b3e-1471">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1471">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-1472">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1472">Role</span></span>

* <span data-ttu-id="a3b3e-1473">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1473">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-1474">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1474">SQL</span></span>

* <span data-ttu-id="a3b3e-1475">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1475">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-1476">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1476">Storage</span></span>

* <span data-ttu-id="a3b3e-1477">ターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1477">Enabled specifying destination-path/prefix for</span></span> `storage blob [upload-batch|download-batch]`

### <a name="vm"></a><span data-ttu-id="a3b3e-1478">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1478">VM</span></span>

* <span data-ttu-id="a3b3e-1479">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1479">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="a3b3e-1480">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1480">February 13, 2018</span></span>

<span data-ttu-id="a3b3e-1481">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1481">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-1482">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1482">Core</span></span>

* <span data-ttu-id="a3b3e-1483">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1483">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-1484">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1484">ACS</span></span>

* <span data-ttu-id="a3b3e-1485">[破壊的変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1485">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="a3b3e-1486">使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1486">Changed `aks get-versions` to show Kubernetes versions available for</span></span> `aks create`
* <span data-ttu-id="a3b3e-1487">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1487">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="a3b3e-1488">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1488">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="a3b3e-1489">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1489">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="a3b3e-1490">ダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1490">Improved reliability when locating the dashboard pod for</span></span> `az aks browse`
* <span data-ttu-id="a3b3e-1491">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1491">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="a3b3e-1492">メッセージを `az aks install-cli` に追加しました。これは `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1492">Added a message to `az aks install-cli` to help get `kubectl` in</span></span> `$PATH`

### <a name="appservice"></a><span data-ttu-id="a3b3e-1493">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1493">Appservice</span></span>

* <span data-ttu-id="a3b3e-1494">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1494">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="a3b3e-1495">既定の App Service プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1495">Added support for default app service plans through</span></span> `az configure --defaults appserviceplan=my-asp`

### <a name="cdn"></a><span data-ttu-id="a3b3e-1496">CDN</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1496">CDN</span></span>

* <span data-ttu-id="a3b3e-1497">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1497">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-1498">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1498">Container</span></span>

* <span data-ttu-id="a3b3e-1499">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1499">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="a3b3e-1500">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1500">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="a3b3e-1501">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1501">CosmosDB</span></span>

* <span data-ttu-id="a3b3e-1502">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1502">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="a3b3e-1503">拡張機能</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1503">Extension</span></span>

* <span data-ttu-id="a3b3e-1504">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1504">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="a3b3e-1505">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1505">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="a3b3e-1506">フィードバック</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1506">Feedback</span></span>

* <span data-ttu-id="a3b3e-1507">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1507">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="a3b3e-1508">Interactive</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1508">Interactive</span></span>

* <span data-ttu-id="a3b3e-1509">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1509">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="a3b3e-1510">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1510">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="a3b3e-1511">IoT</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1511">IoT</span></span>

* <span data-ttu-id="a3b3e-1512">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1512">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="a3b3e-1513">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1513">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="a3b3e-1514">`--no-wait` のサポートを `iot dps access policy [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1514">Added `--no-wait` support to `iot dps access policy [create|update]` and</span></span> `iot dps linked-hub [create|update]`
* <span data-ttu-id="a3b3e-1515">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1515">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="a3b3e-1516">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1516">Monitor</span></span>

* <span data-ttu-id="a3b3e-1517">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1517">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1518">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1518">Network</span></span>

* <span data-ttu-id="a3b3e-1519">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1519">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="a3b3e-1520">プロファイル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1520">Profile</span></span>

* <span data-ttu-id="a3b3e-1521">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1521">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-1522">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1522">Resource</span></span>

* <span data-ttu-id="a3b3e-1523">再び追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1523">Added back</span></span> `feature show`

### <a name="role"></a><span data-ttu-id="a3b3e-1524">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1524">Role</span></span>

* <span data-ttu-id="a3b3e-1525">`--available-to-other-tenants` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1525">Added `--available-to-other-tenants` argument to</span></span> `ad app update`

### <a name="sql"></a><span data-ttu-id="a3b3e-1526">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1526">SQL</span></span>

* <span data-ttu-id="a3b3e-1527">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1527">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="a3b3e-1528">追加済み</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1528">Added</span></span> `sql db rename`
* <span data-ttu-id="a3b3e-1529">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1529">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-1530">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1530">Storage</span></span>

* <span data-ttu-id="a3b3e-1531">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1531">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1532">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1532">VM</span></span>

* <span data-ttu-id="a3b3e-1533">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1533">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="a3b3e-1534">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1534">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="a3b3e-1535">固定</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1535">Fixed</span></span> `vm boot-diagnostics get-boot-log`


## <a name="january-31-2018"></a><span data-ttu-id="a3b3e-1536">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1536">January 31, 2018</span></span>

<span data-ttu-id="a3b3e-1537">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1537">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-1538">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1538">Core</span></span>

* <span data-ttu-id="a3b3e-1539">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1539">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="a3b3e-1540">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1540">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="a3b3e-1541">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1541">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="a3b3e-1542">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1542">Use `--verbose` to see</span></span>
* <span data-ttu-id="a3b3e-1543">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1543">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-1544">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1544">ACS</span></span>

* <span data-ttu-id="a3b3e-1545">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1545">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="a3b3e-1546">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1546">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-1547">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1547">Appservice</span></span>

* <span data-ttu-id="a3b3e-1548">固定</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1548">Fixed</span></span> `webapp log [tail|download]`
* <span data-ttu-id="a3b3e-1549">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1549">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="a3b3e-1550">CDN</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1550">CDN</span></span>

* <span data-ttu-id="a3b3e-1551">クライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1551">Fixed missing client issue with</span></span> `cdn custom-domain create`

### <a name="cosmosdb"></a><span data-ttu-id="a3b3e-1552">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1552">CosmosDB</span></span>

* <span data-ttu-id="a3b3e-1553">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1553">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="a3b3e-1554">Interactive</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1554">Interactive</span></span>

* <span data-ttu-id="a3b3e-1555">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1555">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1556">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1556">Network</span></span>

* <span data-ttu-id="a3b3e-1557">`--cert-password` の保護を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1557">Added protection for `--cert-password` to</span></span> `application-gateway create`
* <span data-ttu-id="a3b3e-1558">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1558">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="a3b3e-1559">`--shared-key` と `--authorization-key` の保護を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1559">Added protection for `--shared-key` and `--authorization-key` to</span></span> `vpn-connection create`
* <span data-ttu-id="a3b3e-1560">クライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1560">Fixed missing client issue with</span></span> `asg create`
* <span data-ttu-id="a3b3e-1561">エクスポートされた名前の `--file-name / -f` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1561">Added `--file-name / -f` parameter for exported names to</span></span> `dns zone export`
* <span data-ttu-id="a3b3e-1562">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1562">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="a3b3e-1563">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1563">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="a3b3e-1564">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1564">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="a3b3e-1565">特定のレコードが 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1565">Fixed issue where certain records were imported twice with</span></span> `dns zone import`
* <span data-ttu-id="a3b3e-1566">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1566">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="a3b3e-1567">プロファイル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1567">Profile</span></span>

* <span data-ttu-id="a3b3e-1568">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1568">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-1569">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1569">Resource</span></span>

* <span data-ttu-id="a3b3e-1570">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1570">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-1571">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1571">Storage</span></span>

* <span data-ttu-id="a3b3e-1572">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1572">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="a3b3e-1573">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1573">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="a3b3e-1574">"-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1574">Fixed bug preventing "-n" arg option with</span></span> `storage account check-name`
* <span data-ttu-id="a3b3e-1575">"snapshot" 列をテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1575">Added 'snapshot' column to table output for</span></span> `blob [list|show]`
* <span data-ttu-id="a3b3e-1576">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1576">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1577">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1577">VM</span></span>

* <span data-ttu-id="a3b3e-1578">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1578">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="a3b3e-1579">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1579">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="a3b3e-1580">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1580">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="a3b3e-1581">`--admin-password` の保護を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1581">Added protection for `--admin-password` to</span></span> `[vm|vmss] create`


## <a name="january-17-2018"></a><span data-ttu-id="a3b3e-1582">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1582">January 17, 2018</span></span>

<span data-ttu-id="a3b3e-1583">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1583">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-1584">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1584">ACR</span></span>

* <span data-ttu-id="a3b3e-1585">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1585">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="a3b3e-1586">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1586">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-1587">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1587">ACS</span></span>

* <span data-ttu-id="a3b3e-1588">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1588">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="a3b3e-1589">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1589">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-1590">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1590">Appservice</span></span>

* <span data-ttu-id="a3b3e-1591">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1591">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="a3b3e-1592">カスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1592">Added support for custom URLs to</span></span> `browse`
* <span data-ttu-id="a3b3e-1593">スロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1593">Fixed slot support for</span></span> `log tail`

### <a name="backup"></a><span data-ttu-id="a3b3e-1594">バックアップ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1594">Backup</span></span>

* <span data-ttu-id="a3b3e-1595">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1595">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="a3b3e-1596">ストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1596">Added storage account options to</span></span> `backup restore restore-disks`
* <span data-ttu-id="a3b3e-1597">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1597">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="a3b3e-1598">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1598">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="a3b3e-1599">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1599">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="a3b3e-1600">Batch</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1600">Batch</span></span>

* <span data-ttu-id="a3b3e-1601">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1601">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="a3b3e-1602">クラウド</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1602">Cloud</span></span>

* <span data-ttu-id="a3b3e-1603">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1603">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="a3b3e-1604">消費</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1604">Consumption</span></span>

* <span data-ttu-id="a3b3e-1605">予約の新しいコマンドとして、`consumption reservations summaries` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1605">Added new commands for reservations: `consumption reservations summaries` and</span></span> `consumption reservations details`

### <a name="event-grid"></a><span data-ttu-id="a3b3e-1606">Event Grid</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1606">Event Grid</span></span>

* <span data-ttu-id="a3b3e-1607">[破壊的変更] `az eventgrid topic event-subscription` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1607">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to</span></span> `eventgrid event-subscription`
* <span data-ttu-id="a3b3e-1608">[破壊的変更] `az eventgrid resource event-subscription` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1608">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to</span></span> `eventgrid event-subscription`
* <span data-ttu-id="a3b3e-1609">[破壊的変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1609">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="a3b3e-1610">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1610">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="a3b3e-1611">コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1611">Added command</span></span> `eventgrid topic update`
* <span data-ttu-id="a3b3e-1612">コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1612">Added command</span></span> `eventgrid event-subscription update`
* <span data-ttu-id="a3b3e-1613">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1613">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="a3b3e-1614">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1614">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="a3b3e-1615">Interactive</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1615">Interactive</span></span>

* <span data-ttu-id="a3b3e-1616">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1616">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="a3b3e-1617">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1617">Fixed errors on startup</span></span>
* <span data-ttu-id="a3b3e-1618">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1618">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="a3b3e-1619">IoT</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1619">IoT</span></span>

* <span data-ttu-id="a3b3e-1620">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1620">Added support for device provisioning service</span></span>
* <span data-ttu-id="a3b3e-1621">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1621">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="a3b3e-1622">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1622">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="a3b3e-1623">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1623">Monitor</span></span>

* <span data-ttu-id="a3b3e-1624">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1624">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="a3b3e-1625">`--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1625">The `--name` parameter is now required for</span></span> `az monitor diagnostic-settings create`
* <span data-ttu-id="a3b3e-1626">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1626">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1627">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1627">Network</span></span>

* <span data-ttu-id="a3b3e-1628">アクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1628">Fixed issue when trying to change to/from active-standby mode with</span></span> `vnet-gateway update`
* <span data-ttu-id="a3b3e-1629">HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1629">Added support for HTTP2 to</span></span> `application-gateway [create|update]`

### <a name="profile"></a><span data-ttu-id="a3b3e-1630">プロファイル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1630">Profile</span></span>

* <span data-ttu-id="a3b3e-1631">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1631">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-1632">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1632">Role</span></span>

* <span data-ttu-id="a3b3e-1633">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1633">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="a3b3e-1634">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1634">Service Fabric</span></span>

* <span data-ttu-id="a3b3e-1635">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1635">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="a3b3e-1636">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1636">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1637">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1637">VM</span></span>

* <span data-ttu-id="a3b3e-1638">[プレビュー] クロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1638">[PREVIEW] Cross-zone support for</span></span> `vmss`
* <span data-ttu-id="a3b3e-1639">[破壊的変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1639">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="a3b3e-1640">[破壊的変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1640">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="a3b3e-1641">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1641">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="a3b3e-1642">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1642">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="a3b3e-1643">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1643">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to</span></span> `[vm|vmss] create`
* <span data-ttu-id="a3b3e-1644">エラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1644">Fixed error issues with</span></span> `[vm|vmss] create`
* <span data-ttu-id="a3b3e-1645">リソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1645">Fixed excessive resource usage caused by</span></span> `vm image list --all`

## <a name="december-19-2017"></a><span data-ttu-id="a3b3e-1646">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1646">December 19, 2017</span></span>

<span data-ttu-id="a3b3e-1647">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1647">Version 2.0.23</span></span>

* <span data-ttu-id="a3b3e-1648">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1648">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-1649">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1649">Container</span></span>

* <span data-ttu-id="a3b3e-1650">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1650">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1651">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1651">Network</span></span>

* <span data-ttu-id="a3b3e-1652">`--disable-bgp-route-propagation` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1652">Added `--disable-bgp-route-propagation` argument to</span></span> `route-table [create|update]`
* <span data-ttu-id="a3b3e-1653">`--ip-tags` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1653">Added `--ip-tags` argument to</span></span> `public-ip [create|update]`

### <a name="storage"></a><span data-ttu-id="a3b3e-1654">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1654">Storage</span></span>

* <span data-ttu-id="a3b3e-1655">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1655">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1656">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1656">VM</span></span>

* <span data-ttu-id="a3b3e-1657">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1657">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="a3b3e-1658">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1658">December 5, 2017</span></span>

<span data-ttu-id="a3b3e-1659">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1659">Version 2.0.22</span></span>

* <span data-ttu-id="a3b3e-1660">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1660">Removed `az component` commands.</span></span> <span data-ttu-id="a3b3e-1661">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1661">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-1662">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1662">Core</span></span>
* <span data-ttu-id="a3b3e-1663">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1663">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="a3b3e-1664">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1664">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-1665">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1665">ACS</span></span>

* <span data-ttu-id="a3b3e-1666">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1666">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="a3b3e-1667">エラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1667">Improved error reporting for</span></span> `acs create`
* <span data-ttu-id="a3b3e-1668">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1668">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="a3b3e-1669">Advisor</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1669">Advisor</span></span>

* <span data-ttu-id="a3b3e-1670">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1670">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-1671">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1671">Appservice</span></span>

* <span data-ttu-id="a3b3e-1672">証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1672">Fixed cert name generation with</span></span> `webapp config ssl upload`
* <span data-ttu-id="a3b3e-1673">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1673">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="a3b3e-1674">既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1674">Added default value for</span></span> `WEBSITE_NODE_DEFAULT_VERSION`

### <a name="consumption"></a><span data-ttu-id="a3b3e-1675">消費</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1675">Consumption</span></span>

* <span data-ttu-id="a3b3e-1676">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1676">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-1677">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1677">Container</span></span>

* <span data-ttu-id="a3b3e-1678">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1678">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="a3b3e-1679">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1679">Monitor</span></span>

* <span data-ttu-id="a3b3e-1680">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1680">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-1681">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1681">Resource</span></span>

* <span data-ttu-id="a3b3e-1682">`--include-response-body` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1682">Added `--include-response-body` argument to</span></span> `resource show`

### <a name="role"></a><span data-ttu-id="a3b3e-1683">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1683">Role</span></span>

* <span data-ttu-id="a3b3e-1684">"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1684">Added display of default assignments for "classic" administraors to</span></span> `role assignment list`
* <span data-ttu-id="a3b3e-1685">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1685">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="a3b3e-1686">エラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1686">Improved error reporting for</span></span> `ad sp create-for-rbac`

### <a name="sql"></a><span data-ttu-id="a3b3e-1687">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1687">SQL</span></span>

* <span data-ttu-id="a3b3e-1688">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1688">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="a3b3e-1689">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1689">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1690">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1690">VM</span></span>

* <span data-ttu-id="a3b3e-1691">ゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1691">Added zone information to</span></span> `az vm list-skus`


## <a name="november-14-2017"></a><span data-ttu-id="a3b3e-1692">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1692">November 14, 2017</span></span>

<span data-ttu-id="a3b3e-1693">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1693">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-1694">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1694">ACR</span></span>

* <span data-ttu-id="a3b3e-1695">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1695">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="a3b3e-1696">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1696">ACS</span></span>

* <span data-ttu-id="a3b3e-1697">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1697">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="a3b3e-1698">`--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1698">Deprecated `--orchestrator-release` option for</span></span> `acs create`
* <span data-ttu-id="a3b3e-1699">AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1699">Changed default VM size for AKS to</span></span> `Standard_D1_v2`
* <span data-ttu-id="a3b3e-1700">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1700">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="a3b3e-1701">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1701">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-1702">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1702">Appservice</span></span>

* <span data-ttu-id="a3b3e-1703">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1703">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="a3b3e-1704">`--docker-container-logging` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1704">Added `--docker-container-logging` option to</span></span> `az webapp log config`
* <span data-ttu-id="a3b3e-1705">`storage` オプションを `--web-server-logging` パラメーターから削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1705">Removed the `storage` option from the parameter `--web-server-logging` of</span></span> `az webapp log config`
* <span data-ttu-id="a3b3e-1706">エラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1706">Improved error messages for</span></span> `deployment user set`
* <span data-ttu-id="a3b3e-1707">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1707">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="a3b3e-1708">固定</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1708">Fixed</span></span> `list-locations`

### <a name="batch"></a><span data-ttu-id="a3b3e-1709">Batch</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1709">Batch</span></span>

* <span data-ttu-id="a3b3e-1710">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1710">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="a3b3e-1711">Batchai</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1711">Batchai</span></span>

* <span data-ttu-id="a3b3e-1712">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1712">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="a3b3e-1713">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1713">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="a3b3e-1714">`job list-files` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1714">Fixed documentation for `job list-files` and</span></span> `job stream-file`
* <span data-ttu-id="a3b3e-1715">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1715">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="a3b3e-1716">クラウド</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1716">Cloud</span></span>

* <span data-ttu-id="a3b3e-1717">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1717">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-1718">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1718">Container</span></span>

* <span data-ttu-id="a3b3e-1719">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1719">Added support to open multiple ports</span></span>
* <span data-ttu-id="a3b3e-1720">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1720">Added container group restart policy</span></span>
* <span data-ttu-id="a3b3e-1721">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1721">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="a3b3e-1722">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1722">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="a3b3e-1723">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1723">Data Lake Analytics</span></span>

* <span data-ttu-id="a3b3e-1724">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1724">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="a3b3e-1725">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1725">Data Lake Store</span></span>

* <span data-ttu-id="a3b3e-1726">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1726">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="a3b3e-1727">拡張機能</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1727">Extension</span></span>

* <span data-ttu-id="a3b3e-1728">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1728">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="a3b3e-1729">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1729">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="a3b3e-1730">IoT</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1730">IoT</span></span>

* <span data-ttu-id="a3b3e-1731">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1731">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="a3b3e-1732">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1732">Monitor</span></span>

* <span data-ttu-id="a3b3e-1733">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1733">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1734">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1734">Network</span></span>

* <span data-ttu-id="a3b3e-1735">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1735">Added support for CAA DNS records</span></span>
* <span data-ttu-id="a3b3e-1736">エンドポイントを更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1736">Fixed issue where endpoints could not be updated with</span></span> `traffic-manager profile update`
* <span data-ttu-id="a3b3e-1737">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1737">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="a3b3e-1738">相対 DNS 名が正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1738">Fixed issue where relative DNS names were incorrectly imported by</span></span> `dns zone import`

### <a name="reservations"></a><span data-ttu-id="a3b3e-1739">Reservations</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1739">Reservations</span></span>

* <span data-ttu-id="a3b3e-1740">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1740">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-1741">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1741">Resource</span></span>

* <span data-ttu-id="a3b3e-1742">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1742">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-1743">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1743">SQL</span></span>

* <span data-ttu-id="a3b3e-1744">`--ignore-missing-vnet-service-endpoint` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1744">Added `--ignore-missing-vnet-service-endpoint` parameter to</span></span> `sql server vnet-rule [create|update]`

### <a name="storage"></a><span data-ttu-id="a3b3e-1745">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1745">Storage</span></span>

* <span data-ttu-id="a3b3e-1746">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1746">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="a3b3e-1747">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1747">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="a3b3e-1748">`--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1748">Fixed bug that prevented using `--source-uri` with</span></span> `storage [blob|file] copy start-batch`
* <span data-ttu-id="a3b3e-1749">複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1749">Added commands to glob and delete multiple objects with</span></span> `storage [blob|file] delete-batch`
* <span data-ttu-id="a3b3e-1750">メトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1750">Fixed issue when enabling metrics with</span></span> `storage metrics update`
* <span data-ttu-id="a3b3e-1751">使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1751">Fixed issue with files over 200GB when using</span></span> `storage blob upload-batch`
* <span data-ttu-id="a3b3e-1752">`--bypass` と `--default-action` が無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1752">Fixed issue where `--bypass` and `--default-action` were ignored by</span></span> `storage account [create|update]`

### <a name="vm"></a><span data-ttu-id="a3b3e-1753">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1753">VM</span></span>

* <span data-ttu-id="a3b3e-1754">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1754">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="a3b3e-1755">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1755">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="a3b3e-1756">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1756">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="a3b3e-1757">`vm format-secret` の名前を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1757">Renamed `vm format-secret` to</span></span> `vm secret format`
* <span data-ttu-id="a3b3e-1758">`--encrypt format` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1758">Added `--encrypt format` argument to</span></span> `vm encryption enable`

## <a name="october-24-2017"></a><span data-ttu-id="a3b3e-1759">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1759">October 24, 2017</span></span>

<span data-ttu-id="a3b3e-1760">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1760">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-1761">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1761">Core</span></span>

* <span data-ttu-id="a3b3e-1762">`MGMT_STORAGE` API バージョンを使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1762">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version</span></span> `2016-01-01`

### <a name="acr"></a><span data-ttu-id="a3b3e-1763">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1763">ACR</span></span>

* <span data-ttu-id="a3b3e-1764">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1764">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="a3b3e-1765">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1765">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="a3b3e-1766">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1766">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-1767">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1767">ACS</span></span>

* <span data-ttu-id="a3b3e-1768">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1768">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="a3b3e-1769">Kubernetes を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1769">Fixed kubernetes</span></span> `get-credentials`

### <a name="appservice"></a><span data-ttu-id="a3b3e-1770">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1770">Appservice</span></span>

* <span data-ttu-id="a3b3e-1771">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1771">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="a3b3e-1772">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1772">Component</span></span>

* <span data-ttu-id="a3b3e-1773">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1773">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="a3b3e-1774">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1774">Monitor</span></span>

* <span data-ttu-id="a3b3e-1775">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1775">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-1776">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1776">Resource</span></span>

* <span data-ttu-id="a3b3e-1777">msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1777">Fixed incompatibility with most recent version of msrest dependency in</span></span> `group export`
* <span data-ttu-id="a3b3e-1778">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1778">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1779">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1779">VM</span></span>

* <span data-ttu-id="a3b3e-1780">`--accelerated-networking` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1780">Added `--accelerated-networking` argument to</span></span> `vmss create`


## <a name="october-9-2017"></a><span data-ttu-id="a3b3e-1781">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1781">October 9, 2017</span></span>

<span data-ttu-id="a3b3e-1782">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1782">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-1783">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1783">Core</span></span>

* <span data-ttu-id="a3b3e-1784">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1784">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-1785">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1785">Appservice</span></span>

* <span data-ttu-id="a3b3e-1786">新しいコマンドによる汎用的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1786">Added generic update with new command</span></span> `webapp update`

### <a name="batch"></a><span data-ttu-id="a3b3e-1787">Batch</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1787">Batch</span></span>

* <span data-ttu-id="a3b3e-1788">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1788">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="a3b3e-1789">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1789">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="a3b3e-1790">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1790">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="a3b3e-1791">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1791">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="a3b3e-1792">Batchai</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1792">Batchai</span></span>

* <span data-ttu-id="a3b3e-1793">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1793">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="a3b3e-1794">KeyVault</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1794">Keyvault</span></span>

* <span data-ttu-id="a3b3e-1795">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1795">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="a3b3e-1796">(#4448)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1796">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="a3b3e-1797">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1797">Network</span></span>

* <span data-ttu-id="a3b3e-1798">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1798">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="a3b3e-1799">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1799">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-1800">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1800">Resource</span></span>

* <span data-ttu-id="a3b3e-1801">リソース グループ名に関する `--resource-group/-g` オプションのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1801">Added support for `--resource-group/-g` options for resource group name to</span></span> `group`
* <span data-ttu-id="a3b3e-1802">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1802">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="a3b3e-1803">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1803">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="a3b3e-1804">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1804">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-1805">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1805">Sql</span></span>

* <span data-ttu-id="a3b3e-1806">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1806">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="a3b3e-1807">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1807">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="a3b3e-1808">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1808">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-1809">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1809">Storage</span></span>

* <span data-ttu-id="a3b3e-1810">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1810">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1811">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1811">Vm</span></span>

* <span data-ttu-id="a3b3e-1812">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1812">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="a3b3e-1813">[プレビュー] ローリング アップグレードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1813">[PREVIEW] Added support for rolling upgrade to</span></span> `vmss create`
* <span data-ttu-id="a3b3e-1814">暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1814">Added support for updating encryption settings with</span></span> `vm encryption enable`
* <span data-ttu-id="a3b3e-1815">`--os-disk-size-gb` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1815">Added `--os-disk-size-gb` parameter to</span></span> `vm create`
* <span data-ttu-id="a3b3e-1816">Windows 用の `--license-type` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1816">Added `--license-type` parameter for Windows to</span></span> `vmss create`


## <a name="september-22-2017"></a><span data-ttu-id="a3b3e-1817">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1817">September 22, 2017</span></span>

<span data-ttu-id="a3b3e-1818">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1818">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-1819">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1819">Resource</span></span>

* <span data-ttu-id="a3b3e-1820">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1820">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="a3b3e-1821">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1821">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="a3b3e-1822">UI の定義とテンプレートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1822">Added support for UI definitions and templates to</span></span> `managedapp definition create`
* <span data-ttu-id="a3b3e-1823">[破壊的変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` からに変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1823">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to</span></span> `applicationDefinitions`

### <a name="network"></a><span data-ttu-id="a3b3e-1824">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1824">Network</span></span>

* <span data-ttu-id="a3b3e-1825">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1825">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="a3b3e-1826">IPv6 Microsoft ピアリングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1826">Added support for IPv6 Microsoft Peering to</span></span> `express-route`
* <span data-ttu-id="a3b3e-1827">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1827">Added `asg` application security group commands</span></span>
* <span data-ttu-id="a3b3e-1828">`--application-security-groups` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1828">Added `--application-security-groups` argument to</span></span> `nic [create|ip-config create|ip-config update]`
* <span data-ttu-id="a3b3e-1829">`--source-asgs` 引数と `--destination-asgs` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1829">Added `--source-asgs` and `--destination-asgs` arguments to</span></span> `nsg rule [create|update]`
* <span data-ttu-id="a3b3e-1830">`--ddos-protection` 引数と `--vm-protection` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1830">Added `--ddos-protection` and `--vm-protection` arguments to</span></span> `vnet [create|update]`
* <span data-ttu-id="a3b3e-1831">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1831">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-1832">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1832">Storage</span></span>

* <span data-ttu-id="a3b3e-1833">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1833">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="a3b3e-1834">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1834">Eventgrid</span></span>

* <span data-ttu-id="a3b3e-1835">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1835">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-1836">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1836">SQL</span></span>

* <span data-ttu-id="a3b3e-1837">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1837">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="a3b3e-1838">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1838">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="a3b3e-1839">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1839">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and</span></span> `dw [create|update]`

### <a name="keyvault"></a><span data-ttu-id="a3b3e-1840">KeyVault</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1840">Keyvault</span></span>

* <span data-ttu-id="a3b3e-1841">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1841">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1842">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1842">VM</span></span>

* <span data-ttu-id="a3b3e-1843">可用性ゾーンに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1843">Added for support to availability zone to</span></span> `[vm|vmss|disk] create`
* <span data-ttu-id="a3b3e-1844">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1844">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="a3b3e-1845">`--asgs` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1845">Added `--asgs` argument to</span></span> `vm create`
* <span data-ttu-id="a3b3e-1846">VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1846">Added support for running commands on VMs with</span></span> `vm run-command`
* <span data-ttu-id="a3b3e-1847">[プレビュー] VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1847">[PREVIEW] Added support for VMSS disk encryption with</span></span> `vmss encryption`
* <span data-ttu-id="a3b3e-1848">VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1848">Added support for performing maintenance on VMs with</span></span> `vm perform-maintenance`

### <a name="acs"></a><span data-ttu-id="a3b3e-1849">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1849">ACS</span></span>

* <span data-ttu-id="a3b3e-1850">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1850">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-1851">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1851">Appservice</span></span>

* <span data-ttu-id="a3b3e-1852">認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1852">Added ability to update and show authentication settings with</span></span> `webapp auth [update|show]`

### <a name="backup"></a><span data-ttu-id="a3b3e-1853">バックアップ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1853">Backup</span></span>

* <span data-ttu-id="a3b3e-1854">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1854">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="a3b3e-1855">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1855">September 11, 2017</span></span>

<span data-ttu-id="a3b3e-1856">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1856">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="a3b3e-1857">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1857">Core</span></span>

* <span data-ttu-id="a3b3e-1858">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1858">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="a3b3e-1859">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1859">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-1860">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1860">Acs</span></span>

* <span data-ttu-id="a3b3e-1861">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1861">Added `acs list-locations` command</span></span>
* <span data-ttu-id="a3b3e-1862">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1862">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-1863">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1863">Appservice</span></span>

* <span data-ttu-id="a3b3e-1864">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1864">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="a3b3e-1865">CDN</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1865">CDN</span></span>

* <span data-ttu-id="a3b3e-1866">"CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1866">Fixed 'CustomDomain is not interable' bug for</span></span> `cdn custom-domain create`

### <a name="extension"></a><span data-ttu-id="a3b3e-1867">拡張機能</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1867">Extension</span></span>

* <span data-ttu-id="a3b3e-1868">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1868">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="a3b3e-1869">KeyVault</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1869">Keyvault</span></span>

* <span data-ttu-id="a3b3e-1870">アクセス許可で大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1870">Fixed issue where permissions were case sensitive for</span></span> `keyvault set-policy`

### <a name="network"></a><span data-ttu-id="a3b3e-1871">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1871">Network</span></span>

* <span data-ttu-id="a3b3e-1872">`vnet list-private-access-services` の名前を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1872">Renamed `vnet list-private-access-services` to</span></span> `vnet list-endpoint-services`
* <span data-ttu-id="a3b3e-1873">`--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1873">Renamed `--private-access-services` argument to `--service-endpoints` for</span></span> `vnet subnet create/update`
* <span data-ttu-id="a3b3e-1874">複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1874">Added support for multiple IP ranges and port ranges to</span></span> `nsg rule create/update`
* <span data-ttu-id="a3b3e-1875">SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1875">Added support for SKU to</span></span> `lb create`
* <span data-ttu-id="a3b3e-1876">SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1876">Added support for SKU to</span></span> `public-ip create`

### <a name="resource"></a><span data-ttu-id="a3b3e-1877">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1877">Resource</span></span>

* <span data-ttu-id="a3b3e-1878">`policy definition create` でリソース ポリシーのパラメーター定義を渡せるようにしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1878">Allow passing in resource policy parameter definitions in `policy definition create`, and</span></span> `policy definition update`
* <span data-ttu-id="a3b3e-1879">パラメーター値を渡せるようにしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1879">Allow passing in parameter values for</span></span> `policy assignment create`
* <span data-ttu-id="a3b3e-1880">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1880">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="a3b3e-1881">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1881">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-1882">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1882">SQL</span></span>

* <span data-ttu-id="a3b3e-1883">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1883">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1884">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1884">VM</span></span>

* <span data-ttu-id="a3b3e-1885">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1885">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="a3b3e-1886">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1886">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="a3b3e-1887">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1887">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="a3b3e-1888">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1888">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="a3b3e-1889">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1889">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="a3b3e-1890">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1890">August 31, 2017</span></span>

<span data-ttu-id="a3b3e-1891">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1891">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="a3b3e-1892">KeyVault</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1892">Keyvault</span></span>

* <span data-ttu-id="a3b3e-1893">シークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1893">Fixed bug when trying to automatically resolve secret encoding with</span></span> `secret download`

### <a name="sf"></a><span data-ttu-id="a3b3e-1894">SF</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1894">Sf</span></span>

* <span data-ttu-id="a3b3e-1895">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1895">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-1896">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1896">Storage</span></span>

* <span data-ttu-id="a3b3e-1897">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1897">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="a3b3e-1898">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1898">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="a3b3e-1899">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1899">August 28, 2017</span></span>

<span data-ttu-id="a3b3e-1900">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1900">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="a3b3e-1901">CLI</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1901">CLI</span></span>

* <span data-ttu-id="a3b3e-1902">法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1902">Added legal note to</span></span> `--version`

### <a name="acs"></a><span data-ttu-id="a3b3e-1903">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1903">ACS</span></span>

* <span data-ttu-id="a3b3e-1904">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1904">Corrected preview regions</span></span>
* <span data-ttu-id="a3b3e-1905">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1905">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="a3b3e-1906">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1906">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-1907">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1907">Appservice</span></span>

* <span data-ttu-id="a3b3e-1908">[破壊的変更] 出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1908">[BREAKING CHANGE] Fixed inconsistencies in the output of</span></span> `az webapp config appsettings [delete|set]`
* <span data-ttu-id="a3b3e-1909">`-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1909">Added a new alias of `-i` for</span></span> `az webapp config container set --docker-custom-image-name`
* <span data-ttu-id="a3b3e-1910">公開しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1910">Exposed</span></span> `az webapp log show`
* <span data-ttu-id="a3b3e-1911">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1911">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="a3b3e-1912">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1912">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="a3b3e-1913">IoT</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1913">IoT</span></span>

* <span data-ttu-id="a3b3e-1914">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1914">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1915">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1915">Network</span></span>

* <span data-ttu-id="a3b3e-1916">[破壊的変更] 名前を `vnet list-private-access-services` から変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1916">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to</span></span> `vnet list-endpoint-services`
* <span data-ttu-id="a3b3e-1917">[破壊的変更] オプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1917">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for</span></span> `vnet subnet [create|update]`
* <span data-ttu-id="a3b3e-1918">複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1918">Added support for multiple IP and port ranges to</span></span> `nsg rule [create|update]`
* <span data-ttu-id="a3b3e-1919">SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1919">Added support for SKU to</span></span> `lb create`
* <span data-ttu-id="a3b3e-1920">SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1920">Added support for SKU to</span></span> `public-ip create`

### <a name="profile"></a><span data-ttu-id="a3b3e-1921">プロファイル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1921">Profile</span></span>

* <span data-ttu-id="a3b3e-1922">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1922">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="a3b3e-1923">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1923">Service Fabric</span></span>

* <span data-ttu-id="a3b3e-1924">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1924">Preview release</span></span>
* <span data-ttu-id="a3b3e-1925">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1925">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="a3b3e-1926">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1926">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="a3b3e-1927">空のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1927">Added support for empty</span></span> `registry_cred`

### <a name="storage"></a><span data-ttu-id="a3b3e-1928">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1928">Storage</span></span>

* <span data-ttu-id="a3b3e-1929">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1929">Enabled setting blob tier</span></span>
* <span data-ttu-id="a3b3e-1930">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1930">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="a3b3e-1931">VNET ルールと IP ベースのルールを追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1931">Added commands to add VNET rules and IP based rules to</span></span> `storage account network-rule`
* <span data-ttu-id="a3b3e-1932">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1932">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="a3b3e-1933">[破壊的変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1933">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="a3b3e-1934">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1934">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1935">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1935">VM</span></span>

* <span data-ttu-id="a3b3e-1936">`vmss get-instance-view` で余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1936">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using</span></span> `--instance-id *`
* <span data-ttu-id="a3b3e-1937">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1937">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="a3b3e-1938">管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1938">Removed human names from the admin name blacklist for</span></span> `[vm|vmss] create`
* <span data-ttu-id="a3b3e-1939">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1939">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="a3b3e-1940">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1940">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="a3b3e-1941">`--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1941">Fixed issue where `--no-wait` argument did not work wth</span></span> `vm availability-set create`


## <a name="august-15-2017"></a><span data-ttu-id="a3b3e-1942">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1942">August 15, 2017</span></span>

<span data-ttu-id="a3b3e-1943">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1943">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-1944">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1944">ACS</span></span>

* <span data-ttu-id="a3b3e-1945">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1945">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-1946">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1946">Appservice</span></span>

* <span data-ttu-id="a3b3e-1947">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1947">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="a3b3e-1948">Event Grid</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1948">Event Grid</span></span>

* <span data-ttu-id="a3b3e-1949">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1949">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="a3b3e-1950">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1950">August 11, 2017</span></span>

<span data-ttu-id="a3b3e-1951">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1951">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-1952">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1952">ACS</span></span>

* <span data-ttu-id="a3b3e-1953">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1953">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="a3b3e-1954">Batch</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1954">Batch</span></span>

* <span data-ttu-id="a3b3e-1955">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1955">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="a3b3e-1956">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1956">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="a3b3e-1957">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1957">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="a3b3e-1958">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1958">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="a3b3e-1959">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1959">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="a3b3e-1960">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1960">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="a3b3e-1961">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1961">Component</span></span>

* <span data-ttu-id="a3b3e-1962">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1962">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="a3b3e-1963">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1963">Container</span></span>

* `create`<span data-ttu-id="a3b3e-1964">:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1964">: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="a3b3e-1965">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1965">Data Lake Store</span></span>

* <span data-ttu-id="a3b3e-1966">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1966">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="a3b3e-1967">Event Grid</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1967">Event Grid</span></span>

* <span data-ttu-id="a3b3e-1968">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1968">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-1969">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1969">Network</span></span>

* `lb`<span data-ttu-id="a3b3e-1970">:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1970">: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* `application-gateway {subresource} delete`<span data-ttu-id="a3b3e-1971">:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1971">: Fixed issue where `--no-wait` was not honored</span></span>
* `application-gateway http-settings update`<span data-ttu-id="a3b3e-1972">:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1972">: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="a3b3e-1973">予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1973">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with</span></span> `az network vpn-connection ipsec-policy add`

### <a name="profile"></a><span data-ttu-id="a3b3e-1974">プロファイル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1974">Profile</span></span>

* `account list`<span data-ttu-id="a3b3e-1975">:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1975">: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-1976">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1976">Storage</span></span>

* <span data-ttu-id="a3b3e-1977">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1977">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-1978">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1978">VM</span></span>

* `availability-set`<span data-ttu-id="a3b3e-1979">:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1979">: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="a3b3e-1980">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1980">Exposed `list-skus` command</span></span>
* <span data-ttu-id="a3b3e-1981">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1981">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="a3b3e-1982">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1982">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="a3b3e-1983">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1983">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="a3b3e-1984">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1984">July 28, 2017</span></span>

<span data-ttu-id="a3b3e-1985">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1985">Version 2.0.12</span></span>

* <span data-ttu-id="a3b3e-1986">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1986">Added container commands</span></span>
* <span data-ttu-id="a3b3e-1987">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1987">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="a3b3e-1988">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1988">Core</span></span>

* <span data-ttu-id="a3b3e-1989">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1989">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="a3b3e-1990">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1990">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="a3b3e-1991">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1991">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="a3b3e-1992">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1992">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="a3b3e-1993">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1993">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="a3b3e-1994">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1994">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="a3b3e-1995">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1995">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="a3b3e-1996">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1996">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="a3b3e-1997">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1997">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="a3b3e-1998">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1998">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="a3b3e-1999">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-1999">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="a3b3e-2000">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2000">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="a3b3e-2001">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2001">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="a3b3e-2002">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2002">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="a3b3e-2003">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2003">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="a3b3e-2004">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2004">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="a3b3e-2005">ACR</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2005">ACR</span></span>

* <span data-ttu-id="a3b3e-2006">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2006">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="a3b3e-2007">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2007">Support SKU update for managed registries</span></span>
* <span data-ttu-id="a3b3e-2008">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2008">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="a3b3e-2009">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2009">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="a3b3e-2010">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2010">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="a3b3e-2011">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2011">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-2012">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2012">ACS</span></span>

* <span data-ttu-id="a3b3e-2013">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2013">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-2014">Appservice</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2014">Appservice</span></span>

* <span data-ttu-id="a3b3e-2015">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2015">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="a3b3e-2016">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2016">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="a3b3e-2017">すべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2017">Remove all commands under</span></span> `appservice web`
* <span data-ttu-id="a3b3e-2018">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2018">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="a3b3e-2019">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2019">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="a3b3e-2020">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2020">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="a3b3e-2021">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2021">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="a3b3e-2022">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2022">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="a3b3e-2023">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2023">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="a3b3e-2024">代わりに使用してください</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2024">Instead use</span></span> `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`

### <a name="batch"></a><span data-ttu-id="a3b3e-2025">Batch</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2025">Batch</span></span>

* <span data-ttu-id="a3b3e-2026">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2026">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="a3b3e-2027">`pool create` のオプション `--target-dedicated` の名前を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2027">Renamed `pool create` option `--target-dedicated` to</span></span> `--target-dedicated-nodes`
* <span data-ttu-id="a3b3e-2028">`pool create` のオプションの `--target-low-priority-nodes` を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2028">Added `pool create` options `--target-low-priority-nodes` and</span></span> `--application-licenses`

### <a name="cdn"></a><span data-ttu-id="a3b3e-2029">CDN</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2029">CDN</span></span>

* <span data-ttu-id="a3b3e-2030">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2030">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="a3b3e-2031">クラウド</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2031">Cloud</span></span>

* <span data-ttu-id="a3b3e-2032">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2032">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="a3b3e-2033">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2033">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="a3b3e-2034">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2034">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="a3b3e-2035">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2035">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="a3b3e-2036">公開しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2036">Exposed</span></span> `endpoint_vm_image_alias_doc`

### <a name="cosmosdb"></a><span data-ttu-id="a3b3e-2037">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2037">CosmosDB</span></span>

* <span data-ttu-id="a3b3e-2038">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2038">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="a3b3e-2039">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2039">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="a3b3e-2040">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2040">Data Lake Analytics</span></span>

* <span data-ttu-id="a3b3e-2041">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2041">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="a3b3e-2042">追加済み</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2042">Added</span></span> `dla job pipeline show`
* <span data-ttu-id="a3b3e-2043">追加済み</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2043">Added</span></span> `dla job recurrence list`

### <a name="data-lake-store"></a><span data-ttu-id="a3b3e-2044">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2044">Data Lake Store</span></span>

* <span data-ttu-id="a3b3e-2045">ユーザー管理のキー コンテナーのキー ローテーションのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2045">Added support for user managed key vault key rotation in</span></span> `dls account update`
* <span data-ttu-id="a3b3e-2046">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2046">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="a3b3e-2047">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2047">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="a3b3e-2048">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2048">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="a3b3e-2049">対話</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2049">Interactive</span></span>

* <span data-ttu-id="a3b3e-2050">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2050">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="a3b3e-2051">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2051">Increased test coverage</span></span>
* <span data-ttu-id="a3b3e-2052">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2052">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="a3b3e-2053">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2053">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="a3b3e-2054">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2054">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="a3b3e-2055">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2055">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="a3b3e-2056">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2056">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="a3b3e-2057">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2057">Added `--progress` flag</span></span>
* <span data-ttu-id="a3b3e-2058">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2058">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="a3b3e-2059">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2059">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="a3b3e-2060">IoT</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2060">IoT</span></span>

* <span data-ttu-id="a3b3e-2061">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2061">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="a3b3e-2062">(#3934)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2062">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="a3b3e-2063">Key Vault</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2063">Key vault</span></span>

* <span data-ttu-id="a3b3e-2064">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2064">Added commands for key vault recovery features:</span></span>
  * `keyvault` <span data-ttu-id="a3b3e-2065">サブコマンド `purge`、`recover`</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2065">subcommands `purge`, `recover`,</span></span> `keyvault list-deleted`
  * `keyvault secret` <span data-ttu-id="a3b3e-2066">サブコマンド `backup`、`restore`、`purge`、`recover`</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2066">subcommands `backup`, `restore`, `purge`, `recover`,</span></span> `list-deleted`
  * `keyvault certificate` <span data-ttu-id="a3b3e-2067">サブコマンド `purge`、`recover`</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2067">subcommands `purge`, `recover`,</span></span> `list-deleted`
  * `keyvault key` <span data-ttu-id="a3b3e-2068">サブコマンド `purge`、`recover`</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2068">subcommands `purge`, `recover`,</span></span> `list-deleted`
* <span data-ttu-id="a3b3e-2069">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2069">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="a3b3e-2070">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2070">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="a3b3e-2071">(#3307)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2071">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="a3b3e-2072">ラボ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2072">Lab</span></span>

* <span data-ttu-id="a3b3e-2073">ラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2073">Added support for claiming any vm in the lab through</span></span> `az lab vm claim`
* <span data-ttu-id="a3b3e-2074">`az lab vm list` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2074">Added table output formatter for `az lab vm list` and</span></span> `az lab vm show`

### <a name="monitor"></a><span data-ttu-id="a3b3e-2075">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2075">Monitor</span></span>

* <span data-ttu-id="a3b3e-2076">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2076">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="a3b3e-2077">`monitor alert-rule-incidents list` の名前を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2077">Renamed `monitor alert-rule-incidents list` to</span></span> `monitor alert list-incidents`
* <span data-ttu-id="a3b3e-2078">`monitor alert-rule-incidents show` の名前を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2078">Renamed `monitor alert-rule-incidents show` to</span></span> `monitor alert show-incident`
* <span data-ttu-id="a3b3e-2079">`monitor metric-defintions list` の名前を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2079">Renamed `monitor metric-defintions list` to</span></span> `monitor metrics list-definitions`
* <span data-ttu-id="a3b3e-2080">`monitor alert-rules` の名前を変更しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2080">Renamed `monitor alert-rules` to</span></span> `monitor alert`
* <span data-ttu-id="a3b3e-2081">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2081">Changed `monitor alert create`:</span></span>
  * `condition` <span data-ttu-id="a3b3e-2082">`action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2082">and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="a3b3e-2083">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2083">Add numerous parameters to simplify the rule creation process</span></span>
  * `location` <span data-ttu-id="a3b3e-2084">必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2084">no longer required</span></span>
  * <span data-ttu-id="a3b3e-2085">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2085">Add name and ID support for target</span></span>
  * <span data-ttu-id="a3b3e-2086">Remove</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2086">Remove</span></span> `--alert-rule-resource-name`
  * <span data-ttu-id="a3b3e-2087">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2087">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * `description` <span data-ttu-id="a3b3e-2088">既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2088">defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="a3b3e-2089">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2089">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="a3b3e-2090">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2090">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="a3b3e-2091">便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2091">Added convenience arguments and examples to</span></span> `monitor alert rule update`

### <a name="network"></a><span data-ttu-id="a3b3e-2092">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2092">Network</span></span>

* <span data-ttu-id="a3b3e-2093">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2093">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="a3b3e-2094">`--private-access-services` 引数を `vnet subnet create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2094">Added `--private-access-services` argument to `vnet subnet create` and</span></span> `vnet subnet update`
* <span data-ttu-id="a3b3e-2095">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2095">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="a3b3e-2096">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2096">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="a3b3e-2097">`application-gateway address-pool create` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2097">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and</span></span> `application-gateway address-pool update`
* <span data-ttu-id="a3b3e-2098">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2098">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="a3b3e-2099">`list-options`、`predefined list` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2099">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`,</span></span> `predefined show`
* <span data-ttu-id="a3b3e-2100">`--name`、`--cipher-suites` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2100">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`,</span></span> `--min-protocol-version`
* <span data-ttu-id="a3b3e-2101">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2101">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="a3b3e-2102">`--default-redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2102">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`,</span></span> `--redirect-config`
* <span data-ttu-id="a3b3e-2103">`--redirect-config` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2103">Added argument `--redirect-config` to</span></span> `application-gateway url-path-map rule create`
* <span data-ttu-id="a3b3e-2104">`--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2104">Added support for `--no-wait` to</span></span> `application-gateway url-path-map rule delete`
* <span data-ttu-id="a3b3e-2105">`--host-name-from-http-settings`、`--min-servers`、`--match-body` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2105">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`,</span></span> `--match-status-codes`
* <span data-ttu-id="a3b3e-2106">`--redirect-config` 引数を `application-gateway rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2106">Added argument `--redirect-config` to `application-gateway rule create` and</span></span> `application-gateway rule update`
* <span data-ttu-id="a3b3e-2107">`--accelerated-networking` のサポートを `nic create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2107">Added support for `--accelerated-networking` to `nic create` and</span></span> `nic update`
* <span data-ttu-id="a3b3e-2108">`--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2108">Removed `--internal-dns-name-suffix` argument from</span></span> `nic create`
* <span data-ttu-id="a3b3e-2109">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2109">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="a3b3e-2110">`local-gateway create` で無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2110">Fixed bug where `local-gateway create` ignored</span></span> `--local-address-prefixes`
* <span data-ttu-id="a3b3e-2111">`--dns-servers` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2111">Added support for `--dns-servers` to</span></span> `vnet update`
* <span data-ttu-id="a3b3e-2112">ルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2112">Fixed bug when creating a peering without route filtering with</span></span> `express-route peering create`
* <span data-ttu-id="a3b3e-2113">`--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2113">Fixed bug where `--provider` and `--bandwidth` arguments did not work with</span></span> `express-route update`
* <span data-ttu-id="a3b3e-2114">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2114">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="a3b3e-2115">出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2115">Improved output formatting for</span></span> `network list-usages`
* <span data-ttu-id="a3b3e-2116">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2116">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="a3b3e-2117">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2117">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="a3b3e-2118">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2118">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="a3b3e-2119">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2119">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="a3b3e-2120">プロファイル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2120">Profile</span></span>

* <span data-ttu-id="a3b3e-2121">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2121">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="a3b3e-2122">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2122">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="a3b3e-2123">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2123">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="a3b3e-2124">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2124">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="a3b3e-2125">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2125">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="a3b3e-2126">RDBMS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2126">RDBMS</span></span>

* <span data-ttu-id="a3b3e-2127">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2127">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="a3b3e-2128">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2128">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="a3b3e-2129">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2129">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="a3b3e-2130">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2130">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-2131">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2131">Resource</span></span>

* <span data-ttu-id="a3b3e-2132">不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2132">Improved prompts for missing parameters for</span></span> `group deployment create`
* <span data-ttu-id="a3b3e-2133">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2133">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="a3b3e-2134">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2134">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="a3b3e-2135">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2135">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="a3b3e-2136">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2136">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="a3b3e-2137">`<resource-namespace>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2137">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and</span></span> `<resource-type>`
* <span data-ttu-id="a3b3e-2138">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2138">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="a3b3e-2139">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2139">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-2140">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2140">Role</span></span>

* <span data-ttu-id="a3b3e-2141">SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2141">Support output in SDK auth file format for</span></span> `create-for-rbac`
* <span data-ttu-id="a3b3e-2142">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2142">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="a3b3e-2143">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2143">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="a3b3e-2144">非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2144">Show deprecation warnings when using</span></span> `--expanded-view`
* <span data-ttu-id="a3b3e-2145">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2145">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="a3b3e-2146">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2146">Service Fabric</span></span>
* <span data-ttu-id="a3b3e-2147">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2147">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="a3b3e-2148">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2148">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="a3b3e-2149">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2149">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-2150">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2150">SQL</span></span>

* <span data-ttu-id="a3b3e-2151">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2151">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="a3b3e-2152">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2152">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="a3b3e-2153">`sql db list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2153">Added commands `sql db list-editions` and</span></span> `sql elastic-pool list-editions`

### <a name="storage"></a><span data-ttu-id="a3b3e-2154">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2154">Storage</span></span>

* <span data-ttu-id="a3b3e-2155">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2155">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="a3b3e-2156">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2156">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="a3b3e-2157">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2157">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="a3b3e-2158">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2158">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="a3b3e-2159">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2159">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="a3b3e-2160">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2160">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-2161">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2161">VM</span></span>

* <span data-ttu-id="a3b3e-2162">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2162">Support configuring nsg</span></span>
* <span data-ttu-id="a3b3e-2163">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2163">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="a3b3e-2164">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2164">Support managed service identities</span></span>
* <span data-ttu-id="a3b3e-2165">既存のロード バランサーを使用する `cmss create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2165">Fixed issue where `cmss create` with an existing load balancer required</span></span> `--backend-pool-name`
* <span data-ttu-id="a3b3e-2166">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2166">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="a3b3e-2167">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2167">May 10, 2017</span></span>

<span data-ttu-id="a3b3e-2168">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2168">Version 2.0.6</span></span>

* <span data-ttu-id="a3b3e-2169">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2169">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="a3b3e-2170">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2170">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="a3b3e-2171">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2171">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="a3b3e-2172">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2172">Include Cognitive Services module</span></span>
* <span data-ttu-id="a3b3e-2173">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2173">Include Service Fabric module</span></span>
* <span data-ttu-id="a3b3e-2174">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2174">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="a3b3e-2175">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2175">Add support for CDN commands</span></span>
* <span data-ttu-id="a3b3e-2176">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2176">Remove Container module</span></span>
* <span data-ttu-id="a3b3e-2177">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2177">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="a3b3e-2178">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2178">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="a3b3e-2179">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2179">Core</span></span>

* <span data-ttu-id="a3b3e-2180">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2180">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="a3b3e-2181">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2181">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="a3b3e-2182">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2182">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="a3b3e-2183">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2183">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="a3b3e-2184">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2184">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="a3b3e-2185">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2185">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="a3b3e-2186">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2186">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="a3b3e-2187">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2187">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="a3b3e-2188">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2188">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="a3b3e-2189">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2189">core: Improved performance</span></span>
* <span data-ttu-id="a3b3e-2190">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2190">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="a3b3e-2191">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2191">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-2192">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2192">ACS</span></span>

* <span data-ttu-id="a3b3e-2193">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2193">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="a3b3e-2194">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2194">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="a3b3e-2195">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2195">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="a3b3e-2196">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2196">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-2197">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2197">AppService</span></span>

* <span data-ttu-id="a3b3e-2198">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2198">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="a3b3e-2199">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2199">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="a3b3e-2200">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2200">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="a3b3e-2201">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2201">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="a3b3e-2202">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2202">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="a3b3e-2203">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2203">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="a3b3e-2204">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2204">support slot swap with preview</span></span>
* <span data-ttu-id="a3b3e-2205">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2205">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="a3b3e-2206">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2206">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="a3b3e-2207">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2207">CosmosDB</span></span>

* <span data-ttu-id="a3b3e-2208">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2208">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="a3b3e-2209">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2209">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="a3b3e-2210">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2210">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="a3b3e-2211">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2211">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="a3b3e-2212">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2212">Data Lake Analytics</span></span>

* <span data-ttu-id="a3b3e-2213">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2213">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="a3b3e-2214">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2214">Add support for new catalog item type: package.</span></span> <span data-ttu-id="a3b3e-2215">介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2215">accessed through:</span></span> `az dla catalog package`
* <span data-ttu-id="a3b3e-2216">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2216">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="a3b3e-2217">テーブル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2217">Table</span></span>
  * <span data-ttu-id="a3b3e-2218">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2218">Table valued function</span></span>
  * <span data-ttu-id="a3b3e-2219">表示</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2219">View</span></span>
  * <span data-ttu-id="a3b3e-2220">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2220">Table Statistics.</span></span> <span data-ttu-id="a3b3e-2221">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2221">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="a3b3e-2222">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2222">Data Lake Store</span></span>

* <span data-ttu-id="a3b3e-2223">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2223">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="a3b3e-2224">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2224">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="a3b3e-2225">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2225">missed help for access show.</span></span> <span data-ttu-id="a3b3e-2226">追加しました </span><span class="sxs-lookup"><span data-stu-id="a3b3e-2226">adding it.</span></span> <span data-ttu-id="a3b3e-2227">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2227">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="a3b3e-2228">検索</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2228">Find</span></span>

* <span data-ttu-id="a3b3e-2229">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2229">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="a3b3e-2230">KeyVault</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2230">KeyVault</span></span>

* <span data-ttu-id="a3b3e-2231">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2231">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="a3b3e-2232">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2232">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="a3b3e-2233">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2233">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="a3b3e-2234">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2234">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="a3b3e-2235">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2235">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="a3b3e-2236">ラボ</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2236">Lab</span></span>

* <span data-ttu-id="a3b3e-2237">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2237">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="a3b3e-2238">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2238">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="a3b3e-2239">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2239">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="a3b3e-2240">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2240">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="a3b3e-2241">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2241">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="a3b3e-2242">監視</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2242">Monitor</span></span>

* <span data-ttu-id="a3b3e-2243">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2243">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="a3b3e-2244">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2244">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="a3b3e-2245">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2245">Network</span></span>

* <span data-ttu-id="a3b3e-2246">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2246">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="a3b3e-2247">`--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2247">Add support for `--filters` parameter for</span></span> `network watcher packet-capture create`
* <span data-ttu-id="a3b3e-2248">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2248">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="a3b3e-2249">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2249">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="a3b3e-2250">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2250">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="a3b3e-2251">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2251">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="a3b3e-2252">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2252">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="a3b3e-2253">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2253">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="a3b3e-2254">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2254">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="a3b3e-2255">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2255">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="a3b3e-2256">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2256">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="a3b3e-2257">BC:出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2257">BC: Fix bug in the output of</span></span> `vpn-connection create`
* <span data-ttu-id="a3b3e-2258">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2258">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="a3b3e-2259">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2259">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="a3b3e-2260">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2260">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="a3b3e-2261">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2261">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="a3b3e-2262">プロファイル</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2262">Profile</span></span>

* <span data-ttu-id="a3b3e-2263">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2263">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="a3b3e-2264">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2264">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="a3b3e-2265">Redis</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2265">Redis</span></span>

* <span data-ttu-id="a3b3e-2266">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2266">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="a3b3e-2267">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2267">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="a3b3e-2268">Resource</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2268">Resource</span></span>

* <span data-ttu-id="a3b3e-2269">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2269">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="a3b3e-2270">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2270">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="a3b3e-2271">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2271">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="a3b3e-2272">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="a3b3e-2272">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="a3b3e-2273">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2273">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="a3b3e-2274">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="a3b3e-2274">Add docs for az lock update.</span></span> <span data-ttu-id="a3b3e-2275">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2275">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="a3b3e-2276">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="a3b3e-2276">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="a3b3e-2277">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2277">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="a3b3e-2278">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2278">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="a3b3e-2279">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2279">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="a3b3e-2280">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2280">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="a3b3e-2281">Role</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2281">Role</span></span>

* <span data-ttu-id="a3b3e-2282">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2282">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="a3b3e-2283">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2283">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="a3b3e-2284">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2284">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="a3b3e-2285">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2285">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="a3b3e-2286">SQL</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2286">SQL</span></span>

* <span data-ttu-id="a3b3e-2287">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2287">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="a3b3e-2288">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2288">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="a3b3e-2289">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2289">Storage</span></span>

* <span data-ttu-id="a3b3e-2290">リソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2290">Default location to resource group location for</span></span> `storage account create`
* <span data-ttu-id="a3b3e-2291">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2291">Add support for incremental blob copy</span></span>
* <span data-ttu-id="a3b3e-2292">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2292">Add support for large block blob upload</span></span>
* <span data-ttu-id="a3b3e-2293">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2293">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-2294">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2294">VM</span></span>

* <span data-ttu-id="a3b3e-2295">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2295">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="a3b3e-2296">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2296">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="a3b3e-2297">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2297">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="a3b3e-2298">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2298">az vm/vmss disk</span></span>
  3. <span data-ttu-id="a3b3e-2299">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2299">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="a3b3e-2300">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2300">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="a3b3e-2301">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2301">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="a3b3e-2302">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2302">April 3, 2017</span></span>

<span data-ttu-id="a3b3e-2303">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2303">Version 2.0.2</span></span>

<span data-ttu-id="a3b3e-2304">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2304">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="a3b3e-2305">コア</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2305">Core</span></span>

* <span data-ttu-id="a3b3e-2306">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2306">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="a3b3e-2307">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2307">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="a3b3e-2308">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2308">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="a3b3e-2309">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2309">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="a3b3e-2310">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2310">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="a3b3e-2311">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="a3b3e-2311">Add prompting for missing template parameters.</span></span> <span data-ttu-id="a3b3e-2312">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2312">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="a3b3e-2313">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2313">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="a3b3e-2314">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2314">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="a3b3e-2315">ACS</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2315">ACS</span></span>

* <span data-ttu-id="a3b3e-2316">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2316">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="a3b3e-2317">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="a3b3e-2317">Add support for ssh key password prompting.</span></span> <span data-ttu-id="a3b3e-2318">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2318">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="a3b3e-2319">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="a3b3e-2319">Add support for windows clusters.</span></span> <span data-ttu-id="a3b3e-2320">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2320">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="a3b3e-2321">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="a3b3e-2321">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="a3b3e-2322">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2322">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="a3b3e-2323">AppService</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2323">AppService</span></span>

* <span data-ttu-id="a3b3e-2324">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2324">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="a3b3e-2325">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2325">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="a3b3e-2326">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2326">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="a3b3e-2327">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2327">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="a3b3e-2328">DataLake</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2328">DataLake</span></span>

* <span data-ttu-id="a3b3e-2329">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2329">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="a3b3e-2330">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2330">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="a3b3e-2331">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2331">DocuemntDB</span></span>

* <span data-ttu-id="a3b3e-2332">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2332">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="a3b3e-2333">VM</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2333">VM</span></span>

* <span data-ttu-id="a3b3e-2334">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2334">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="a3b3e-2335">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2335">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="a3b3e-2336">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2336">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="a3b3e-2337">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2337">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="a3b3e-2338">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2338">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="a3b3e-2339">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2339">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="a3b3e-2340">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2340">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="a3b3e-2341">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2341">February 27, 2017</span></span>

<span data-ttu-id="a3b3e-2342">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2342">Version 2.0.0</span></span>

<span data-ttu-id="a3b3e-2343">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2343">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="a3b3e-2344">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2344">Container Service (acs)</span></span>
- <span data-ttu-id="a3b3e-2345">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2345">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="a3b3e-2346">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2346">Networking</span></span>
- <span data-ttu-id="a3b3e-2347">Storage</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2347">Storage</span></span>

<span data-ttu-id="a3b3e-2348">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2348">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="a3b3e-2349">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2349">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="a3b3e-2350">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2350">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="a3b3e-2351">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2351">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="a3b3e-2352">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2352">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="a3b3e-2353">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2353">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="a3b3e-2354">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2354">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="a3b3e-2355">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2355">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="a3b3e-2356">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="a3b3e-2356">Provide feedback from the command line with the `az feedback` command</span></span>

