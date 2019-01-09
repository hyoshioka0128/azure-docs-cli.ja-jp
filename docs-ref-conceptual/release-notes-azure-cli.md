---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 12/18/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 10663ad8e85a15b8fedb5ac12c5d17256d07e523
ms.sourcegitcommit: 614811ea63ceb0e71bd99323846dc1b754e15255
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/28/2018
ms.locfileid: "53805960"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="29c35-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="29c35-103">Azure CLI release notes</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="29c35-104">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="29c35-104">December 20, 2018</span></span>

<span data-ttu-id="29c35-105">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="29c35-105">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="29c35-106">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-106">Appservice</span></span>
* <span data-ttu-id="29c35-107">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-107">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="29c35-108">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-108">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="29c35-109">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-109">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="29c35-110">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="29c35-110">IoTCentral</span></span>
* <span data-ttu-id="29c35-111">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-111">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="29c35-112">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-112">Role</span></span>
* <span data-ttu-id="29c35-113">[重大な変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-113">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-114">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-114">SQL</span></span>
* <span data-ttu-id="29c35-115">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-115">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-116">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-116">VM</span></span>
* <span data-ttu-id="29c35-117">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-117">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="29c35-118">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="29c35-118">December 18, 2018</span></span>

<span data-ttu-id="29c35-119">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="29c35-119">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="29c35-120">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-120">ACR</span></span>
* <span data-ttu-id="29c35-121">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-121">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="29c35-122">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="29c35-122">Condensed the table layout for task list</span></span>
* <span data-ttu-id="29c35-123">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-123">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-124">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-124">ACS</span></span>
* <span data-ttu-id="29c35-125">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-125">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="29c35-126">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-126">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="29c35-127">[非推奨] `az acs` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-127">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="29c35-128">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="29c35-128">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="29c35-129">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-129">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="29c35-130">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-130">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-131">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-131">Appservice</span></span>
* <span data-ttu-id="29c35-132">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-132">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="29c35-133">Botservice</span><span class="sxs-lookup"><span data-stu-id="29c35-133">Botservice</span></span>
* <span data-ttu-id="29c35-134">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-134">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="29c35-135">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-135">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="29c35-136">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-136">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="29c35-137">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="29c35-137">Reduced Kudu network calls</span></span>
* <span data-ttu-id="29c35-138">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-138">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="29c35-139">消費</span><span class="sxs-lookup"><span data-stu-id="29c35-139">Consumption</span></span>
* <span data-ttu-id="29c35-140">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-140">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="29c35-141">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="29c35-141">CosmosDB</span></span>
* <span data-ttu-id="29c35-142">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-142">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="29c35-143">マップ</span><span class="sxs-lookup"><span data-stu-id="29c35-143">Maps</span></span>
* <span data-ttu-id="29c35-144">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-144">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="29c35-145">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-145">Network</span></span>
* <span data-ttu-id="29c35-146">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-146">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="29c35-147">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-147">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-148">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-148">Resource</span></span>
* <span data-ttu-id="29c35-149">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-149">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="29c35-150">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-150">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-151">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-151">Storage</span></span>
*  <span data-ttu-id="29c35-152">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-152">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-153">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-153">VM</span></span>
* <span data-ttu-id="29c35-154">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-154">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="29c35-155">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="29c35-155">December 4, 2018</span></span>

<span data-ttu-id="29c35-156">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="29c35-156">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="29c35-157">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-157">Core</span></span>
* <span data-ttu-id="29c35-158">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-158">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="29c35-159">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-159">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-160">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-160">Appservice</span></span>
* <span data-ttu-id="29c35-161">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-161">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="29c35-162">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-162">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="29c35-163">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-163">Network</span></span>
* <span data-ttu-id="29c35-164">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-164">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="29c35-165">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-165">Role</span></span>
* <span data-ttu-id="29c35-166">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-166">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="29c35-167">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-167">VM</span></span>
* <span data-ttu-id="29c35-168">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-168">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="29c35-169">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-169">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="29c35-170">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-170">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="29c35-171">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-171">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="29c35-172">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="29c35-172">November 20, 2018</span></span>

<span data-ttu-id="29c35-173">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="29c35-173">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="29c35-174">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-174">Core</span></span>
* <span data-ttu-id="29c35-175">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-175">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-176">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-176">ACR</span></span>
* <span data-ttu-id="29c35-177">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-177">Added context token to task step</span></span>
* <span data-ttu-id="29c35-178">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-178">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="29c35-179">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-179">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-180">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-180">Appservice</span></span>
* <span data-ttu-id="29c35-181">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-181">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="29c35-182">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-182">Updated the default `node_version`.</span></span> <span data-ttu-id="29c35-183">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="29c35-183">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="29c35-184">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-184">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="29c35-185">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-185">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="29c35-186">IotCentral</span><span class="sxs-lookup"><span data-stu-id="29c35-186">IotCentral</span></span>
* <span data-ttu-id="29c35-187">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-187">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="29c35-188">KeyVault</span><span class="sxs-lookup"><span data-stu-id="29c35-188">KeyVault</span></span>
* <span data-ttu-id="29c35-189">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-189">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="29c35-190">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-190">Network</span></span>
* <span data-ttu-id="29c35-191">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-191">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="29c35-192">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-192">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="29c35-193">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-193">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="29c35-194">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-194">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="29c35-195">Rdbms</span><span class="sxs-lookup"><span data-stu-id="29c35-195">Rdbms</span></span>
* <span data-ttu-id="29c35-196">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-196">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="29c35-197">Rbac</span><span class="sxs-lookup"><span data-stu-id="29c35-197">Rbac</span></span>
* <span data-ttu-id="29c35-198">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-198">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="29c35-199">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-199">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="29c35-200">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-200">Storage</span></span>
* <span data-ttu-id="29c35-201">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-201">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="29c35-202">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-202">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="29c35-203">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-203">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="29c35-204">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="29c35-204">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-205">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-205">VM</span></span>
* <span data-ttu-id="29c35-206">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-206">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="29c35-207">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-207">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="29c35-208">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="29c35-208">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="29c35-209">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-209">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="29c35-210">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-210">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="29c35-211">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-211">Added `snapshot wait` command</span></span>
* <span data-ttu-id="29c35-212">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-212">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="29c35-213">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="29c35-213">November 6, 2018</span></span>

<span data-ttu-id="29c35-214">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="29c35-214">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="29c35-215">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-215">Core</span></span>
* <span data-ttu-id="29c35-216">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-216">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-217">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-217">ACR</span></span>
* <span data-ttu-id="29c35-218">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-218">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="29c35-219">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-219">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-220">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-220">ACS</span></span>
* <span data-ttu-id="29c35-221">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-221">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="29c35-222">Advisor</span><span class="sxs-lookup"><span data-stu-id="29c35-222">Advisor</span></span>
* <span data-ttu-id="29c35-223">GA リリース</span><span class="sxs-lookup"><span data-stu-id="29c35-223">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="29c35-224">AMS</span><span class="sxs-lookup"><span data-stu-id="29c35-224">AMS</span></span>
* <span data-ttu-id="29c35-225">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-225">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="29c35-226">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-226">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="29c35-227">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-227">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="29c35-228">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-228">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="29c35-229">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-229">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="29c35-230">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-230">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="29c35-231">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-231">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="29c35-232">[重大な変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="29c35-232">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="29c35-233">[重大な変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-233">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="29c35-234">[重大な変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-234">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="29c35-235">[重大な変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="29c35-235">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="29c35-236">[重大な変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="29c35-236">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="29c35-237">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="29c35-237">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="29c35-238">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="29c35-238">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="29c35-239">[重大な変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-239">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="29c35-240">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="29c35-240">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="29c35-241">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="29c35-241">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-242">AppService</span><span class="sxs-lookup"><span data-stu-id="29c35-242">AppService</span></span>
* <span data-ttu-id="29c35-243">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-243">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="29c35-244">構成</span><span class="sxs-lookup"><span data-stu-id="29c35-244">Configure</span></span>
* <span data-ttu-id="29c35-245">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-245">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="29c35-246">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-246">Container</span></span>
* <span data-ttu-id="29c35-247">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-247">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="29c35-248">EventHub</span><span class="sxs-lookup"><span data-stu-id="29c35-248">EventHub</span></span>
* <span data-ttu-id="29c35-249">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-249">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="29c35-250">Interactive</span><span class="sxs-lookup"><span data-stu-id="29c35-250">Interactive</span></span>
* <span data-ttu-id="29c35-251">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="29c35-251">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="29c35-252">監視</span><span class="sxs-lookup"><span data-stu-id="29c35-252">Monitor</span></span>
* <span data-ttu-id="29c35-253">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-253">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="29c35-254">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-254">Network</span></span>
* <span data-ttu-id="29c35-255">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-255">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="29c35-256">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-256">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="29c35-257">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-257">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="29c35-258">プロファイル</span><span class="sxs-lookup"><span data-stu-id="29c35-258">Profile</span></span>
* <span data-ttu-id="29c35-259">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-259">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="29c35-260">RDBMS</span><span class="sxs-lookup"><span data-stu-id="29c35-260">RDBMS</span></span>
* <span data-ttu-id="29c35-261">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-261">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-262">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-262">Resource</span></span>
* <span data-ttu-id="29c35-263">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-263">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="29c35-264">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-264">Role</span></span>
* <span data-ttu-id="29c35-265">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-265">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="29c35-266">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-266">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="29c35-267">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-267">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-268">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-268">Storage</span></span>
* <span data-ttu-id="29c35-269">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="29c35-269">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-270">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-270">VM</span></span>
* <span data-ttu-id="29c35-271">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-271">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="29c35-272">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-272">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="29c35-273">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-273">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="29c35-274">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-274">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="29c35-275">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="29c35-275">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="29c35-276">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-276">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="29c35-277">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="29c35-277">October 23, 2018</span></span>

<span data-ttu-id="29c35-278">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="29c35-278">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="29c35-279">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-279">Core</span></span>
* <span data-ttu-id="29c35-280">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-280">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="29c35-281">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-281">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-282">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-282">ACR</span></span>
* <span data-ttu-id="29c35-283">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-283">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="29c35-284">CDN</span><span class="sxs-lookup"><span data-stu-id="29c35-284">CDN</span></span>
* <span data-ttu-id="29c35-285">[重大な変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="29c35-285">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="29c35-286">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-286">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="29c35-287">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-287">Container</span></span>
* <span data-ttu-id="29c35-288">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-288">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="29c35-289">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-289">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="29c35-290">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-290">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="29c35-291">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-291">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="29c35-292">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-292">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="29c35-293">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-293">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="29c35-294">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-294">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="29c35-295">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="29c35-295">CosmosDB</span></span>
* <span data-ttu-id="29c35-296">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-296">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="29c35-297">Interactive</span><span class="sxs-lookup"><span data-stu-id="29c35-297">Interactive</span></span>
* <span data-ttu-id="29c35-298">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-298">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="29c35-299">IoT Central</span><span class="sxs-lookup"><span data-stu-id="29c35-299">IoT Central</span></span>
* <span data-ttu-id="29c35-300">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-300">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="29c35-301">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="29c35-301">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="29c35-302">監視</span><span class="sxs-lookup"><span data-stu-id="29c35-302">Monitor</span></span>
* <span data-ttu-id="29c35-303">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="29c35-303">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="29c35-304">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-304">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="29c35-305">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-305">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="29c35-306">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-306">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="29c35-307">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-307">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="29c35-308">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-308">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="29c35-309">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="29c35-309">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="29c35-310">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-310">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="29c35-311">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-311">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="29c35-312">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-312">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="29c35-313">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-313">Network</span></span>
* <span data-ttu-id="29c35-314">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-314">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="29c35-315">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-315">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="29c35-316">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="29c35-316">ServiceBus</span></span>
* <span data-ttu-id="29c35-317">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-317">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-318">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-318">SQL</span></span>
* <span data-ttu-id="29c35-319">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-319">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-320">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-320">Storage</span></span>
* <span data-ttu-id="29c35-321">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-321">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="29c35-322">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-322">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-323">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-323">VM</span></span>
* <span data-ttu-id="29c35-324">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="29c35-324">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="29c35-325">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-325">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="29c35-326">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-326">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="29c35-327">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="29c35-327">October 16, 2018</span></span>

<span data-ttu-id="29c35-328">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="29c35-328">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-329">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-329">VM</span></span>
* <span data-ttu-id="29c35-330">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-330">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="29c35-331">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="29c35-331">October 9, 2018</span></span>

<span data-ttu-id="29c35-332">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="29c35-332">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="29c35-333">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-333">Core</span></span>
* <span data-ttu-id="29c35-334">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-334">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-335">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-335">ACR</span></span>
* <span data-ttu-id="29c35-336">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-336">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-337">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-337">ACS</span></span>
* <span data-ttu-id="29c35-338">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="29c35-338">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="29c35-339">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-339">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="29c35-340">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-340">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="29c35-341">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-341">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="29c35-342">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-342">Container</span></span>
* <span data-ttu-id="29c35-343">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-343">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="29c35-344">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-344">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="29c35-345">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="29c35-345">Event Hub</span></span>
* <span data-ttu-id="29c35-346">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-346">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="29c35-347">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-347">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="29c35-348">Extensions</span><span class="sxs-lookup"><span data-stu-id="29c35-348">Extensions</span></span>
* <span data-ttu-id="29c35-349">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-349">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="29c35-350">HDInsight</span><span class="sxs-lookup"><span data-stu-id="29c35-350">HDInsight</span></span>
* <span data-ttu-id="29c35-351">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="29c35-351">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="29c35-352">IoT</span><span class="sxs-lookup"><span data-stu-id="29c35-352">IoT</span></span>
* <span data-ttu-id="29c35-353">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-353">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="29c35-354">KeyVault</span><span class="sxs-lookup"><span data-stu-id="29c35-354">KeyVault</span></span>
* <span data-ttu-id="29c35-355">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-355">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="29c35-356">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-356">Network</span></span>
* <span data-ttu-id="29c35-357">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="29c35-357">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="29c35-358">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="29c35-358">See #6052</span></span>
* <span data-ttu-id="29c35-359">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-359">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="29c35-360">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="29c35-360">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="29c35-361">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-361">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="29c35-362">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-362">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="29c35-363">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-363">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="29c35-364">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-364">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="29c35-365">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-365">Role</span></span>
* <span data-ttu-id="29c35-366">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-366">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="29c35-367">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-367">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="29c35-368">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-368">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="29c35-369">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-369">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="29c35-370">Service Bus</span><span class="sxs-lookup"><span data-stu-id="29c35-370">Service Bus</span></span>
* <span data-ttu-id="29c35-371">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-371">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-372">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-372">VM</span></span>
* <span data-ttu-id="29c35-373">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-373">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="29c35-374">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-374">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="29c35-375">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-375">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="29c35-376">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-376">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="29c35-377">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-377">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="29c35-378">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-378">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="29c35-379">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="29c35-379">September 21, 2018</span></span>

<span data-ttu-id="29c35-380">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="29c35-380">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-381">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-381">ACR</span></span>
* <span data-ttu-id="29c35-382">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-382">Added ACR Task commands</span></span>
* <span data-ttu-id="29c35-383">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-383">Added quick run command</span></span>
* <span data-ttu-id="29c35-384">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-384">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="29c35-385">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-385">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="29c35-386">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-386">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="29c35-387">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-387">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-388">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-388">ACS</span></span>
* <span data-ttu-id="29c35-389">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-389">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="29c35-390">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-390">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-391">AppService</span><span class="sxs-lookup"><span data-stu-id="29c35-391">AppService</span></span>

* <span data-ttu-id="29c35-392">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-392">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="29c35-393">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-393">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="29c35-394">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-394">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="29c35-395">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-395">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="29c35-396">Batch</span><span class="sxs-lookup"><span data-stu-id="29c35-396">Batch</span></span>
* <span data-ttu-id="29c35-397">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-397">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="29c35-398">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-398">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="29c35-399">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-399">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="29c35-400">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-400">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="29c35-401">Batch AI</span><span class="sxs-lookup"><span data-stu-id="29c35-401">Batch AI</span></span> 
* <span data-ttu-id="29c35-402">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-402">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="29c35-403">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="29c35-403">Cognitive Services</span></span>
* <span data-ttu-id="29c35-404">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-404">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="29c35-405">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-405">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="29c35-406">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-406">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="29c35-407">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-407">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="29c35-408">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-408">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="29c35-409">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-409">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="29c35-410">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-410">Container</span></span>
* <span data-ttu-id="29c35-411">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-411">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="29c35-412">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-412">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="29c35-413">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-413">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="29c35-414">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-414">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="29c35-415">DataLake</span><span class="sxs-lookup"><span data-stu-id="29c35-415">Datalake</span></span>
* <span data-ttu-id="29c35-416">仮想ネットワーク ルール用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-416">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="29c35-417">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="29c35-417">Interactive Shell</span></span>
* <span data-ttu-id="29c35-418">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-418">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="29c35-419">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-419">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="29c35-420">IoT</span><span class="sxs-lookup"><span data-stu-id="29c35-420">IoT</span></span>
* <span data-ttu-id="29c35-421">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-421">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="29c35-422">Key Vault</span><span class="sxs-lookup"><span data-stu-id="29c35-422">Key Vault</span></span>
* <span data-ttu-id="29c35-423">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-423">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="29c35-424">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-424">Network</span></span>
* <span data-ttu-id="29c35-425">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-425">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="29c35-426">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-426">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="29c35-427">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-427">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="29c35-428">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-428">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="29c35-429">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-429">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="29c35-430">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-430">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="29c35-431">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="29c35-431">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="29c35-432">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-432">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="29c35-433">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-433">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="29c35-434">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-434">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="29c35-435">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-435">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="29c35-436">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-436">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="29c35-437">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-437">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="29c35-438">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="29c35-438">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="29c35-439">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-439">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="29c35-440">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-440">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="29c35-441">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-441">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="29c35-442">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-442">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="29c35-443">RDBMS</span><span class="sxs-lookup"><span data-stu-id="29c35-443">RDBMS</span></span>
* <span data-ttu-id="29c35-444">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-444">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="29c35-445">予約</span><span class="sxs-lookup"><span data-stu-id="29c35-445">Reservation</span></span>
* <span data-ttu-id="29c35-446">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-446">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="29c35-447">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-447">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="29c35-448">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="29c35-448">Manage App</span></span>
* <span data-ttu-id="29c35-449">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-449">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="29c35-450">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-450">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="29c35-451">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-451">Role</span></span>
* <span data-ttu-id="29c35-452">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-452">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="29c35-453">SignalR</span><span class="sxs-lookup"><span data-stu-id="29c35-453">SignalR</span></span>
* <span data-ttu-id="29c35-454">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="29c35-454">First release</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-455">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-455">Storage</span></span>
* <span data-ttu-id="29c35-456">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-456">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="29c35-457">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-457">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-458">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-458">VM</span></span>
* <span data-ttu-id="29c35-459">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="29c35-459">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="29c35-460">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-460">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="29c35-461">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="29c35-461">August 28, 2018</span></span>

<span data-ttu-id="29c35-462">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="29c35-462">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="29c35-463">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-463">Core</span></span>

* <span data-ttu-id="29c35-464">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-464">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="29c35-465">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-465">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-466">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-466">ACR</span></span>

* <span data-ttu-id="29c35-467">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-467">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="29c35-468">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-468">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-469">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-469">ACS</span></span>

* <span data-ttu-id="29c35-470">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-470">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="29c35-471">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-471">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-472">AppService</span><span class="sxs-lookup"><span data-stu-id="29c35-472">AppService</span></span>

* <span data-ttu-id="29c35-473">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-473">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="29c35-474">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-474">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="29c35-475">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-475">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="29c35-476">バックアップ</span><span class="sxs-lookup"><span data-stu-id="29c35-476">Backup</span></span>

* <span data-ttu-id="29c35-477">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-477">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="29c35-478">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="29c35-478">Bot Service</span></span>

* <span data-ttu-id="29c35-479">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="29c35-479">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="29c35-480">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="29c35-480">Cognitive Services</span></span>

* <span data-ttu-id="29c35-481">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-481">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="29c35-482">IoT</span><span class="sxs-lookup"><span data-stu-id="29c35-482">IoT</span></span>

* <span data-ttu-id="29c35-483">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-483">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="29c35-484">監視</span><span class="sxs-lookup"><span data-stu-id="29c35-484">Monitor</span></span>

* <span data-ttu-id="29c35-485">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-485">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="29c35-486">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-486">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="29c35-487">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-487">Network</span></span>

* <span data-ttu-id="29c35-488">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-488">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-489">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-489">Resource</span></span>

* <span data-ttu-id="29c35-490">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-490">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-491">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-491">Storage</span></span>

* <span data-ttu-id="29c35-492">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-492">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-493">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-493">VM</span></span>

* <span data-ttu-id="29c35-494">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-494">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="29c35-495">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-495">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="29c35-496">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="29c35-496">Auguest 14, 2018</span></span>

<span data-ttu-id="29c35-497">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="29c35-497">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="29c35-498">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-498">Core</span></span>

* <span data-ttu-id="29c35-499">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-499">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="29c35-500">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-500">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="29c35-501">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="29c35-501">Telemetry</span></span>

* <span data-ttu-id="29c35-502">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-502">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-503">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-503">ACR</span></span>

* <span data-ttu-id="29c35-504">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-504">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="29c35-505">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-505">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-506">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-506">ACS</span></span>

* <span data-ttu-id="29c35-507">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-507">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="29c35-508">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-508">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="29c35-509">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-509">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="29c35-510">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-510">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="29c35-511">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-511">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="29c35-512">AppService</span><span class="sxs-lookup"><span data-stu-id="29c35-512">AppService</span></span>

* <span data-ttu-id="29c35-513">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-513">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="29c35-514">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-514">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="29c35-515">BatchAI</span><span class="sxs-lookup"><span data-stu-id="29c35-515">BatchAI</span></span>

* <span data-ttu-id="29c35-516">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-516">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="29c35-517">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-517">Container</span></span>

* <span data-ttu-id="29c35-518">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-518">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="29c35-519">IoT</span><span class="sxs-lookup"><span data-stu-id="29c35-519">IoT</span></span>

* <span data-ttu-id="29c35-520">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-520">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="29c35-521">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-521">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="29c35-522">Iot Central</span><span class="sxs-lookup"><span data-stu-id="29c35-522">Iot Central</span></span>

* <span data-ttu-id="29c35-523">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="29c35-523">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="29c35-524">KeyVault</span><span class="sxs-lookup"><span data-stu-id="29c35-524">KeyVault</span></span>


* <span data-ttu-id="29c35-525">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-525">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="29c35-526">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-526">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="29c35-527">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-527">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="29c35-528">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-528">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="29c35-529">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-529">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="29c35-530">リレー</span><span class="sxs-lookup"><span data-stu-id="29c35-530">Relay</span></span>

* <span data-ttu-id="29c35-531">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="29c35-531">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-532">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-532">Sql</span></span>

* <span data-ttu-id="29c35-533">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-533">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-534">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-534">Storage</span></span>

* <span data-ttu-id="29c35-535">[重大な変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="29c35-535">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="29c35-536">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-536">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="29c35-537">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="29c35-537">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="29c35-538">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-538">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="29c35-539">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-539">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-540">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-540">VM</span></span>

* <span data-ttu-id="29c35-541">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-541">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="29c35-542">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="29c35-542">July 31, 2018</span></span>

<span data-ttu-id="29c35-543">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="29c35-543">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-544">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-544">ACR</span></span>

* <span data-ttu-id="29c35-545">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-545">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="29c35-546">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-546">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-547">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-547">ACS</span></span>

* <span data-ttu-id="29c35-548">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-548">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="29c35-549">Batch</span><span class="sxs-lookup"><span data-stu-id="29c35-549">Batch</span></span>

* <span data-ttu-id="29c35-550">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-550">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="29c35-551">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-551">Container</span></span>

* <span data-ttu-id="29c35-552">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-552">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="29c35-553">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-553">Network</span></span>

* <span data-ttu-id="29c35-554">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-554">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="29c35-555">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-555">Resource</span></span>

* <span data-ttu-id="29c35-556">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-556">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="29c35-557">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-557">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="29c35-558">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-558">Role</span></span>

* <span data-ttu-id="29c35-559">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-559">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="29c35-560">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-560">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="29c35-561">Search</span><span class="sxs-lookup"><span data-stu-id="29c35-561">Search</span></span>

* <span data-ttu-id="29c35-562">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-562">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="29c35-563">Service Bus</span><span class="sxs-lookup"><span data-stu-id="29c35-563">Service Bus</span></span>

* <span data-ttu-id="29c35-564">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-564">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="29c35-565">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-565">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="29c35-566">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="29c35-566">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="29c35-567">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="29c35-567">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-568">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-568">Storage</span></span>

* <span data-ttu-id="29c35-569">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-569">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="29c35-570">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="29c35-570">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-571">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-571">VM</span></span>

* <span data-ttu-id="29c35-572">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-572">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="29c35-573">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-573">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="29c35-574">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-574">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="29c35-575">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-575">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="29c35-576">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="29c35-576">July 18, 2018</span></span>

<span data-ttu-id="29c35-577">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="29c35-577">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="29c35-578">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-578">Core</span></span>

* <span data-ttu-id="29c35-579">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-579">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="29c35-580">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-580">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="29c35-581">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-581">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-582">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-582">ACR</span></span>

* <span data-ttu-id="29c35-583">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-583">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="29c35-584">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-584">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="29c35-585">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-585">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="29c35-586">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-586">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-587">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-587">ACS</span></span>

* <span data-ttu-id="29c35-588">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-588">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-589">AppService</span><span class="sxs-lookup"><span data-stu-id="29c35-589">AppService</span></span>

* <span data-ttu-id="29c35-590">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-590">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="29c35-591">Batch</span><span class="sxs-lookup"><span data-stu-id="29c35-591">Batch</span></span>

* <span data-ttu-id="29c35-592">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-592">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="29c35-593">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-593">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="29c35-594">Batch AI</span><span class="sxs-lookup"><span data-stu-id="29c35-594">Batch AI</span></span>

* <span data-ttu-id="29c35-595">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-595">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="29c35-596">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-596">Container</span></span>

* <span data-ttu-id="29c35-597">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-597">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="29c35-598">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-598">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="29c35-599">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-599">Network</span></span>

* <span data-ttu-id="29c35-600">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-600">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="29c35-601">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-601">Added `network nic wait`</span></span>
* <span data-ttu-id="29c35-602">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-602">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="29c35-603">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-603">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="29c35-604">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-604">Resource</span></span>

* <span data-ttu-id="29c35-605">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-605">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="29c35-606">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-606">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="29c35-607">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-607">Added `deployment wait` command</span></span>
* <span data-ttu-id="29c35-608">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-608">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-609">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-609">SQL</span></span>

* <span data-ttu-id="29c35-610">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-610">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="29c35-611">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-611">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="29c35-612">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="29c35-612">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-613">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-613">Storage</span></span>

* <span data-ttu-id="29c35-614">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-614">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-615">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-615">VM</span></span>

* <span data-ttu-id="29c35-616">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-616">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="29c35-617">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-617">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="29c35-618">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-618">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="29c35-619">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="29c35-619">July 3, 2018</span></span>

<span data-ttu-id="29c35-620">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="29c35-620">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="29c35-621">AKS</span><span class="sxs-lookup"><span data-stu-id="29c35-621">AKS</span></span>

* <span data-ttu-id="29c35-622">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-622">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="29c35-623">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="29c35-623">July 3, 2018</span></span>

<span data-ttu-id="29c35-624">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="29c35-624">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="29c35-625">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-625">Core</span></span>

* <span data-ttu-id="29c35-626">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-626">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-627">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-627">ACR</span></span>

* <span data-ttu-id="29c35-628">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-628">Added polling build status</span></span>
* <span data-ttu-id="29c35-629">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-629">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="29c35-630">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-630">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-631">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-631">ACS</span></span>

* <span data-ttu-id="29c35-632">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-632">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="29c35-633">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-633">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="29c35-634">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-634">Updated options for `aks browse` command.</span></span> <span data-ttu-id="29c35-635">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-635">Added `--listen-port` support</span></span>
* <span data-ttu-id="29c35-636">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-636">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="29c35-637">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="29c35-637">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="29c35-638">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-638">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-639">AppService</span><span class="sxs-lookup"><span data-stu-id="29c35-639">AppService</span></span>

* <span data-ttu-id="29c35-640">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-640">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="29c35-641">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-641">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="29c35-642">バックアップ</span><span class="sxs-lookup"><span data-stu-id="29c35-642">Backup</span></span>

* <span data-ttu-id="29c35-643">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-643">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="29c35-644">BatchAI</span><span class="sxs-lookup"><span data-stu-id="29c35-644">BatchAI</span></span>

* <span data-ttu-id="29c35-645">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-645">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="29c35-646">クラウド</span><span class="sxs-lookup"><span data-stu-id="29c35-646">Cloud</span></span>

* <span data-ttu-id="29c35-647">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-647">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="29c35-648">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-648">Container</span></span>

* <span data-ttu-id="29c35-649">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-649">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="29c35-650">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-650">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="29c35-651">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-651">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="29c35-652">拡張機能</span><span class="sxs-lookup"><span data-stu-id="29c35-652">Extension</span></span>

* <span data-ttu-id="29c35-653">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-653">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="29c35-654">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-654">Network</span></span>

* <span data-ttu-id="29c35-655">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-655">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="29c35-656">Rdbms</span><span class="sxs-lookup"><span data-stu-id="29c35-656">Rdbms</span></span>

* <span data-ttu-id="29c35-657">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-657">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-658">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-658">Resource</span></span>

* <span data-ttu-id="29c35-659">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-659">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-660">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-660">VM</span></span>

* <span data-ttu-id="29c35-661">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-661">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="29c35-662">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="29c35-662">June 25, 2018</span></span>

<span data-ttu-id="29c35-663">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="29c35-663">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="29c35-664">CLI</span><span class="sxs-lookup"><span data-stu-id="29c35-664">CLI</span></span>

* <span data-ttu-id="29c35-665">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-665">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="29c35-666">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="29c35-666">June 19, 2018</span></span>

<span data-ttu-id="29c35-667">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="29c35-667">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="29c35-668">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-668">Core</span></span>

* <span data-ttu-id="29c35-669">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-669">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-670">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-670">ACR</span></span>

* <span data-ttu-id="29c35-671">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-671">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="29c35-672">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-672">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-673">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-673">ACS</span></span>

* <span data-ttu-id="29c35-674">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-674">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="29c35-675">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-675">Added `--update` support</span></span>
* <span data-ttu-id="29c35-676">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-676">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="29c35-677">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="29c35-677">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="29c35-678">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-678">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="29c35-679">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-679">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="29c35-680">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-680">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="29c35-681">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-681">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-682">AppService</span><span class="sxs-lookup"><span data-stu-id="29c35-682">AppService</span></span>

* <span data-ttu-id="29c35-683">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-683">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="29c35-684">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-684">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="29c35-685">Batch</span><span class="sxs-lookup"><span data-stu-id="29c35-685">Batch</span></span>

* <span data-ttu-id="29c35-686">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-686">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="29c35-687">Batch AI</span><span class="sxs-lookup"><span data-stu-id="29c35-687">Batch AI</span></span>

* <span data-ttu-id="29c35-688">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-688">Added support for workspaces.</span></span> <span data-ttu-id="29c35-689">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="29c35-689">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="29c35-690">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-690">Added support for experiments.</span></span> <span data-ttu-id="29c35-691">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="29c35-691">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="29c35-692">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-692">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="29c35-693">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-693">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="29c35-694">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="29c35-694">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="29c35-695">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-695">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="29c35-696">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="29c35-696">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="29c35-697">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="29c35-697">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="29c35-698">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-698">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="29c35-699">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="29c35-699">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="29c35-700">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-700">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="29c35-701">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="29c35-701">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="29c35-702">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-702">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="29c35-703">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="29c35-703">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="29c35-704">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-704">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="29c35-705">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-705">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="29c35-706">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-706">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="29c35-707">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-707">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="29c35-708">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-708">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="29c35-709">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-709">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="29c35-710">マップ</span><span class="sxs-lookup"><span data-stu-id="29c35-710">Maps</span></span>

* <span data-ttu-id="29c35-711">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-711">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="29c35-712">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-712">Network</span></span>

* <span data-ttu-id="29c35-713">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="29c35-713">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="29c35-714">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-714">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="29c35-715">#6502</span><span class="sxs-lookup"><span data-stu-id="29c35-715">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="29c35-716">Reservations</span><span class="sxs-lookup"><span data-stu-id="29c35-716">Reservations</span></span>

* <span data-ttu-id="29c35-717">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-717">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="29c35-718">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-718">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="29c35-719">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-719">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="29c35-720">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-720">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="29c35-721">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-721">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="29c35-722">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-722">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="29c35-723">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-723">Role</span></span>

* <span data-ttu-id="29c35-724">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-724">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-725">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-725">SQL</span></span>

* <span data-ttu-id="29c35-726">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-726">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-727">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-727">Storage</span></span>

* <span data-ttu-id="29c35-728">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="29c35-728">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-729">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-729">VM</span></span>

* <span data-ttu-id="29c35-730">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-730">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="29c35-731">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-731">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="29c35-732">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-732">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="29c35-733">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="29c35-733">June 13, 2018</span></span>

<span data-ttu-id="29c35-734">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="29c35-734">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="29c35-735">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-735">Core</span></span>

* <span data-ttu-id="29c35-736">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-736">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="29c35-737">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="29c35-737">June 13, 2018</span></span>

<span data-ttu-id="29c35-738">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="29c35-738">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="29c35-739">AKS</span><span class="sxs-lookup"><span data-stu-id="29c35-739">AKS</span></span>

* <span data-ttu-id="29c35-740">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-740">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="29c35-741">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-741">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="29c35-742">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-742">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="29c35-743">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-743">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="29c35-744">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-744">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-745">AppService</span><span class="sxs-lookup"><span data-stu-id="29c35-745">AppService</span></span>

* <span data-ttu-id="29c35-746">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-746">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="29c35-747">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="29c35-747">June 5, 2018</span></span>

<span data-ttu-id="29c35-748">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="29c35-748">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="29c35-749">Interactive</span><span class="sxs-lookup"><span data-stu-id="29c35-749">Interactive</span></span>

* <span data-ttu-id="29c35-750">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-750">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="29c35-751">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="29c35-751">June 5, 2018</span></span>

<span data-ttu-id="29c35-752">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="29c35-752">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="29c35-753">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-753">Core</span></span>

* <span data-ttu-id="29c35-754">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-754">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="29c35-755">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="29c35-755">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-756">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-756">ACR</span></span>

* <span data-ttu-id="29c35-757">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-757">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="29c35-758">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-758">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="29c35-759">AKS</span><span class="sxs-lookup"><span data-stu-id="29c35-759">AKS</span></span>

* <span data-ttu-id="29c35-760">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-760">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="29c35-761">Batch</span><span class="sxs-lookup"><span data-stu-id="29c35-761">Batch</span></span>

* <span data-ttu-id="29c35-762">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-762">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="29c35-763">IoT</span><span class="sxs-lookup"><span data-stu-id="29c35-763">IOT</span></span>

* <span data-ttu-id="29c35-764">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-764">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="29c35-765">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-765">Network</span></span>

* <span data-ttu-id="29c35-766">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="29c35-766">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="29c35-767">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="29c35-767">Policy Insights</span></span>

* <span data-ttu-id="29c35-768">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="29c35-768">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="29c35-769">ARM</span><span class="sxs-lookup"><span data-stu-id="29c35-769">ARM</span></span>

* <span data-ttu-id="29c35-770">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-770">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-771">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-771">SQL</span></span>

* <span data-ttu-id="29c35-772">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-772">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="29c35-773">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-773">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="29c35-774">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-774">Storage</span></span>

* <span data-ttu-id="29c35-775">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-775">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-776">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-776">VM</span></span>

* <span data-ttu-id="29c35-777">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-777">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="29c35-778">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-778">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="29c35-779">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-779">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="29c35-780">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="29c35-780">May 22, 2018</span></span>

<span data-ttu-id="29c35-781">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="29c35-781">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="29c35-782">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-782">Core</span></span>

* <span data-ttu-id="29c35-783">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-783">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-784">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-784">ACS</span></span>

* <span data-ttu-id="29c35-785">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-785">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="29c35-786">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-786">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-787">AppService</span><span class="sxs-lookup"><span data-stu-id="29c35-787">AppService</span></span>

* <span data-ttu-id="29c35-788">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="29c35-788">Improved generic update commands</span></span>
* <span data-ttu-id="29c35-789">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-789">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="29c35-790">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-790">Container</span></span>

* <span data-ttu-id="29c35-791">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-791">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="29c35-792">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-792">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="29c35-793">拡張機能</span><span class="sxs-lookup"><span data-stu-id="29c35-793">Extension</span></span>

* <span data-ttu-id="29c35-794">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="29c35-794">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="29c35-795">Interactive</span><span class="sxs-lookup"><span data-stu-id="29c35-795">Interactive</span></span>

* <span data-ttu-id="29c35-796">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-796">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="29c35-797">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="29c35-797">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="29c35-798">KeyVault</span><span class="sxs-lookup"><span data-stu-id="29c35-798">KeyVault</span></span>

* <span data-ttu-id="29c35-799">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-799">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="29c35-800">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-800">Network</span></span>

* <span data-ttu-id="29c35-801">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-801">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="29c35-802">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-802">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-803">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-803">SQL</span></span>

* <span data-ttu-id="29c35-804">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-804">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="29c35-805">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-805">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="29c35-806">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-806">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="29c35-807">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-807">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="29c35-808">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-808">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="29c35-809">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="29c35-809">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="29c35-810">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="29c35-810">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="29c35-811">`edition`</span><span class="sxs-lookup"><span data-stu-id="29c35-811">`edition`.</span></span> <span data-ttu-id="29c35-812">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="29c35-812">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="29c35-813">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="29c35-813">`elasticPoolName`.</span></span> <span data-ttu-id="29c35-814">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="29c35-814">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="29c35-815">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-815">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="29c35-816">`edition`</span><span class="sxs-lookup"><span data-stu-id="29c35-816">`edition`.</span></span> <span data-ttu-id="29c35-817">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="29c35-817">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="29c35-818">`dtu`</span><span class="sxs-lookup"><span data-stu-id="29c35-818">`dtu`.</span></span> <span data-ttu-id="29c35-819">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="29c35-819">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="29c35-820">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="29c35-820">`databaseDtuMin`.</span></span> <span data-ttu-id="29c35-821">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="29c35-821">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="29c35-822">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="29c35-822">`databaseDtuMax`.</span></span> <span data-ttu-id="29c35-823">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="29c35-823">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="29c35-824">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-824">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="29c35-825">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-825">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-826">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-826">Storage</span></span>

* <span data-ttu-id="29c35-827">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-827">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="29c35-828">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-828">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-829">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-829">VM</span></span>

* <span data-ttu-id="29c35-830">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-830">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="29c35-831">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="29c35-831">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="29c35-832">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-832">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="29c35-833">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-833">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="29c35-834">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-834">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="29c35-835">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="29c35-835">May 7, 2018</span></span>

<span data-ttu-id="29c35-836">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="29c35-836">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="29c35-837">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-837">Core</span></span>

* <span data-ttu-id="29c35-838">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-838">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="29c35-839">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-839">Added limited support for positional arguments</span></span>
* <span data-ttu-id="29c35-840">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-840">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="29c35-841">#5591</span><span class="sxs-lookup"><span data-stu-id="29c35-841">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="29c35-842">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-842">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="29c35-843">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="29c35-843">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="29c35-844">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-844">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="29c35-845">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-845">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="29c35-846">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-846">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-847">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-847">ACR</span></span>

* <span data-ttu-id="29c35-848">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-848">Added ACR Build commands</span></span>
* <span data-ttu-id="29c35-849">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-849">Improved resource not found error messages</span></span>
* <span data-ttu-id="29c35-850">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-850">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="29c35-851">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-851">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="29c35-852">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-852">Improved repository commands error messages</span></span>
* <span data-ttu-id="29c35-853">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-853">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-854">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-854">ACS</span></span>

* <span data-ttu-id="29c35-855">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-855">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="29c35-856">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-856">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="29c35-857">AMS</span><span class="sxs-lookup"><span data-stu-id="29c35-857">AMS</span></span>

* <span data-ttu-id="29c35-858">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="29c35-858">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-859">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-859">Appservice</span></span>

* <span data-ttu-id="29c35-860">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-860">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="29c35-861">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-861">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="29c35-862">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-862">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="29c35-863">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-863">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="29c35-864">Batch AI</span><span class="sxs-lookup"><span data-stu-id="29c35-864">Batch AI</span></span>

* <span data-ttu-id="29c35-865">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-865">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="29c35-866">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="29c35-866">Cognitive Services</span></span>

* <span data-ttu-id="29c35-867">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-867">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="29c35-868">消費</span><span class="sxs-lookup"><span data-stu-id="29c35-868">Consumption</span></span>

* <span data-ttu-id="29c35-869">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-869">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="29c35-870">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-870">Container</span></span>

* <span data-ttu-id="29c35-871">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-871">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="29c35-872">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="29c35-872">Cosmos DB</span></span>

* <span data-ttu-id="29c35-873">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="29c35-873">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="29c35-874">DMS</span><span class="sxs-lookup"><span data-stu-id="29c35-874">DMS</span></span>

* <span data-ttu-id="29c35-875">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-875">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="29c35-876">拡張機能</span><span class="sxs-lookup"><span data-stu-id="29c35-876">Extension</span></span>

* <span data-ttu-id="29c35-877">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-877">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="29c35-878">Interactive</span><span class="sxs-lookup"><span data-stu-id="29c35-878">Interactive</span></span>

* <span data-ttu-id="29c35-879">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-879">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="29c35-880">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="29c35-880">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="29c35-881">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-881">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="29c35-882">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-882">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="29c35-883">ラボ</span><span class="sxs-lookup"><span data-stu-id="29c35-883">Lab</span></span>

* <span data-ttu-id="29c35-884">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-884">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="29c35-885">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-885">Network</span></span>

* <span data-ttu-id="29c35-886">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-886">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="29c35-887">プロファイル</span><span class="sxs-lookup"><span data-stu-id="29c35-887">Profile</span></span>

* <span data-ttu-id="29c35-888">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-888">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="29c35-889">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-889">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="29c35-890">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-890">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="29c35-891">Redis</span><span class="sxs-lookup"><span data-stu-id="29c35-891">Redis</span></span>

* <span data-ttu-id="29c35-892">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-892">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="29c35-893">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="29c35-893">Deprecated `redis list-all`.</span></span> <span data-ttu-id="29c35-894">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="29c35-894">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="29c35-895">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-895">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="29c35-896">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-896">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="29c35-897">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-897">Role</span></span>

* <span data-ttu-id="29c35-898">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-898">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-899">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-899">Storage</span></span>

* <span data-ttu-id="29c35-900">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="29c35-900">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="29c35-901">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="29c35-901">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="29c35-902">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="29c35-902">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="29c35-903">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="29c35-903">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="29c35-904">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-904">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-905">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-905">VM</span></span>

* <span data-ttu-id="29c35-906">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-906">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="29c35-907">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-907">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="29c35-908">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="29c35-908">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="29c35-909">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-909">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="29c35-910">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-910">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="29c35-911">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-911">Added write accelerator support</span></span>
* <span data-ttu-id="29c35-912">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-912">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="29c35-913">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-913">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="29c35-914">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-914">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="29c35-915">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="29c35-915">April 10, 2018</span></span>

<span data-ttu-id="29c35-916">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="29c35-916">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-917">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-917">ACR</span></span>

* <span data-ttu-id="29c35-918">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-918">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-919">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-919">ACS</span></span>

* <span data-ttu-id="29c35-920">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-920">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-921">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-921">Appservice</span></span>

* [重大な変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="29c35-923">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-923">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="29c35-924">BatchAI</span><span class="sxs-lookup"><span data-stu-id="29c35-924">BatchAI</span></span>

* <span data-ttu-id="29c35-925">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-925">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="29c35-926">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="29c35-926">Job level mounting</span></span>
  - <span data-ttu-id="29c35-927">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="29c35-927">Environment variables with secret values</span></span>
  - <span data-ttu-id="29c35-928">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="29c35-928">Performance counters settings</span></span>
  - <span data-ttu-id="29c35-929">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="29c35-929">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="29c35-930">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="29c35-930">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="29c35-931">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="29c35-931">Usage and limits reporting</span></span>
  - <span data-ttu-id="29c35-932">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="29c35-932">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="29c35-933">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="29c35-933">Support for custom images</span></span>
  - <span data-ttu-id="29c35-934">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-934">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="29c35-935">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-935">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="29c35-936">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="29c35-936">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="29c35-937">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="29c35-937">National clouds are supported</span></span>
* <span data-ttu-id="29c35-938">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-938">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="29c35-939">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-939">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="29c35-940">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-940">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="29c35-941">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-941">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="29c35-942">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="29c35-942">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="29c35-943">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="29c35-943">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="29c35-944">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-944">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="29c35-945">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-945">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="29c35-946">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="29c35-946">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="29c35-947">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-947">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="29c35-948">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="29c35-948">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="29c35-949">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="29c35-949">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="29c35-950">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-950">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="29c35-951">課金</span><span class="sxs-lookup"><span data-stu-id="29c35-951">Billing</span></span>

* <span data-ttu-id="29c35-952">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-952">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="29c35-953">消費</span><span class="sxs-lookup"><span data-stu-id="29c35-953">Consumption</span></span>

* <span data-ttu-id="29c35-954">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-954">Added `marketplace` commands</span></span>
* <span data-ttu-id="29c35-955">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-955">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="29c35-956">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-956">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="29c35-957">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-957">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="29c35-958">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-958">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="29c35-959">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-959">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="29c35-960">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-960">Container</span></span>

* <span data-ttu-id="29c35-961">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-961">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="29c35-962">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-962">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="29c35-963">拡張機能</span><span class="sxs-lookup"><span data-stu-id="29c35-963">Extension</span></span>

* <span data-ttu-id="29c35-964">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-964">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="29c35-965">Interactive</span><span class="sxs-lookup"><span data-stu-id="29c35-965">Interactive</span></span>

* <span data-ttu-id="29c35-966">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-966">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="29c35-967">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-967">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="29c35-968">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-968">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="29c35-969">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-969">Network</span></span>

* <span data-ttu-id="29c35-970">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-970">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="29c35-971">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-971">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="29c35-972">#4910</span><span class="sxs-lookup"><span data-stu-id="29c35-972">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="29c35-973">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-973">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="29c35-974">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="29c35-974">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="29c35-975">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-975">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="29c35-976">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-976">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="29c35-977">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-977">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="29c35-978">プロファイル</span><span class="sxs-lookup"><span data-stu-id="29c35-978">Profile</span></span>

* <span data-ttu-id="29c35-979">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-979">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="29c35-980">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-980">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="29c35-981">RDBMS</span><span class="sxs-lookup"><span data-stu-id="29c35-981">RDBMS</span></span>

* <span data-ttu-id="29c35-982">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-982">Added `georestore` command</span></span>
* <span data-ttu-id="29c35-983">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-983">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-984">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-984">Resource</span></span>

* <span data-ttu-id="29c35-985">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-985">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="29c35-986">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-986">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-987">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-987">SQL</span></span>

* <span data-ttu-id="29c35-988">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-988">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-989">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-989">Storage</span></span>

* <span data-ttu-id="29c35-990">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-990">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-991">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-991">VM</span></span>

* <span data-ttu-id="29c35-992">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-992">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="29c35-993">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-993">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="29c35-995">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-995">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="29c35-996">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-996">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="29c35-997">#5718</span><span class="sxs-lookup"><span data-stu-id="29c35-997">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="29c35-998">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-998">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="29c35-999">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="29c35-999">March 27, 2018</span></span>

<span data-ttu-id="29c35-1000">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="29c35-1000">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="29c35-1001">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-1001">Core</span></span>

* <span data-ttu-id="29c35-1002">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="29c35-1002">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1003">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1003">ACS</span></span>

* <span data-ttu-id="29c35-1004">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1004">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1005">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1005">Appservice</span></span>

* <span data-ttu-id="29c35-1006">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1006">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="29c35-1007">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1007">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="29c35-1008">バックアップ</span><span class="sxs-lookup"><span data-stu-id="29c35-1008">Backup</span></span>

* <span data-ttu-id="29c35-1009">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1009">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="29c35-1010">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="29c35-1010">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="29c35-1011">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1011">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="29c35-1012">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1012">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="29c35-1013">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-1013">Container</span></span>

* <span data-ttu-id="29c35-1014">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1014">Added `container exec` command.</span></span> <span data-ttu-id="29c35-1015">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="29c35-1015">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="29c35-1016">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="29c35-1016">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="29c35-1017">拡張機能</span><span class="sxs-lookup"><span data-stu-id="29c35-1017">Extension</span></span>

* <span data-ttu-id="29c35-1018">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1018">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="29c35-1019">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1019">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="29c35-1020">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1020">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="29c35-1021">Interactive</span><span class="sxs-lookup"><span data-stu-id="29c35-1021">Interactive</span></span>

* <span data-ttu-id="29c35-1022">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1022">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="29c35-1023">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1023">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="29c35-1024">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1024">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="29c35-1025">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1025">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="29c35-1026">ラボ</span><span class="sxs-lookup"><span data-stu-id="29c35-1026">Lab</span></span>

* <span data-ttu-id="29c35-1027">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1027">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="29c35-1028">監視</span><span class="sxs-lookup"><span data-stu-id="29c35-1028">Monitor</span></span>

* <span data-ttu-id="29c35-1029">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="29c35-1029">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="29c35-1030">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="29c35-1030">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="29c35-1031">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="29c35-1031">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="29c35-1032">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1032">Network</span></span>

* <span data-ttu-id="29c35-1033">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1033">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="29c35-1034">プロファイル</span><span class="sxs-lookup"><span data-stu-id="29c35-1034">Profile</span></span>

* <span data-ttu-id="29c35-1035">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1035">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="29c35-1036">RDBMS</span><span class="sxs-lookup"><span data-stu-id="29c35-1036">RDBMS</span></span>

* <span data-ttu-id="29c35-1037">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1037">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-1038">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-1038">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="29c35-1040">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-1040">Role</span></span>

* <span data-ttu-id="29c35-1041">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1041">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="29c35-1042">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1042">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="29c35-1043">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1043">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="29c35-1044">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1044">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="29c35-1045">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1045">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-1046">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-1046">Storage</span></span>

* <span data-ttu-id="29c35-1047">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1047">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="29c35-1048">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="29c35-1048">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1049">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1049">VM</span></span>

* <span data-ttu-id="29c35-1050">インスタンス数が 100 を超えるセットに対する今後の重大な変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1050">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="29c35-1051">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1051">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="29c35-1052">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1052">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="29c35-1053">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1053">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="29c35-1054">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1054">March 13, 2018</span></span>

<span data-ttu-id="29c35-1055">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="29c35-1055">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-1056">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-1056">ACR</span></span>

* <span data-ttu-id="29c35-1057">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1057">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="29c35-1058">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1058">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="29c35-1059">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1059">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1060">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1060">ACS</span></span>

* <span data-ttu-id="29c35-1061">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1061">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="29c35-1062">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1062">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="29c35-1063">Advisor</span><span class="sxs-lookup"><span data-stu-id="29c35-1063">Advisor</span></span>

* <span data-ttu-id="29c35-1064">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1064">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="29c35-1065">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1065">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="29c35-1066">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1066">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="29c35-1067">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1067">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="29c35-1068">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1068">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1069">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1069">Appservice</span></span>

* <span data-ttu-id="29c35-1070">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1070">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="29c35-1071">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1071">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="29c35-1072">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="29c35-1072">Eventhubs</span></span>

* <span data-ttu-id="29c35-1073">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="29c35-1073">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="29c35-1074">拡張機能</span><span class="sxs-lookup"><span data-stu-id="29c35-1074">Extension</span></span>

* <span data-ttu-id="29c35-1075">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1075">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="29c35-1076">Interactive</span><span class="sxs-lookup"><span data-stu-id="29c35-1076">Interactive</span></span>

* <span data-ttu-id="29c35-1077">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="29c35-1077">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="29c35-1078">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="29c35-1078">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="29c35-1079">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="29c35-1079">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="29c35-1080">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1080">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="29c35-1081">監視</span><span class="sxs-lookup"><span data-stu-id="29c35-1081">Monitor</span></span>

* <span data-ttu-id="29c35-1082">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1082">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="29c35-1083">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1083">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="29c35-1084">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1084">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="29c35-1085">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1085">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="29c35-1086">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1086">Network</span></span>

* <span data-ttu-id="29c35-1087">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1087">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="29c35-1088">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1088">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="29c35-1089">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1089">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="29c35-1090">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1090">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="29c35-1091">プロファイル</span><span class="sxs-lookup"><span data-stu-id="29c35-1091">Profile</span></span>

* <span data-ttu-id="29c35-1092">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1092">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="29c35-1093">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1093">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="29c35-1094">RDBMS</span><span class="sxs-lookup"><span data-stu-id="29c35-1094">RDBMS</span></span>

* <span data-ttu-id="29c35-1095">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1095">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="29c35-1096">Service Bus</span><span class="sxs-lookup"><span data-stu-id="29c35-1096">Service Bus</span></span>

* <span data-ttu-id="29c35-1097">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="29c35-1097">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-1098">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-1098">Storage</span></span>

* <span data-ttu-id="29c35-1099">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1099">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="29c35-1100">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1100">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1101">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1101">VM</span></span>

* <span data-ttu-id="29c35-1102">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1102">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="29c35-1103">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1103">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="29c35-1104">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1104">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="29c35-1105">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1105">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="29c35-1106">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1106">February 27, 2018</span></span>

<span data-ttu-id="29c35-1107">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="29c35-1107">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="29c35-1108">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-1108">Core</span></span>

* <span data-ttu-id="29c35-1109">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="29c35-1109">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="29c35-1110">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1110">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="29c35-1111">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1111">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1112">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1112">ACS</span></span>

* <span data-ttu-id="29c35-1113">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1113">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="29c35-1114">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="29c35-1114">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="29c35-1115">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1115">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="29c35-1116">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1116">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1117">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1117">Appservice</span></span>

* <span data-ttu-id="29c35-1118">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="29c35-1118">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="29c35-1119">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="29c35-1119">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="29c35-1120">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="29c35-1120">Cognitive Services</span></span>

* <span data-ttu-id="29c35-1121">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1121">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="29c35-1122">消費</span><span class="sxs-lookup"><span data-stu-id="29c35-1122">Consumption</span></span>

* <span data-ttu-id="29c35-1123">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1123">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="29c35-1124">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1124">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="29c35-1125">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-1125">Container</span></span>

* <span data-ttu-id="29c35-1126">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1126">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="29c35-1127">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1127">Network</span></span>

* <span data-ttu-id="29c35-1128">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="29c35-1128">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-1129">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-1129">Resource</span></span>

* <span data-ttu-id="29c35-1130">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1130">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="29c35-1131">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-1131">Role</span></span>

* <span data-ttu-id="29c35-1132">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1132">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-1133">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-1133">SQL</span></span>

* <span data-ttu-id="29c35-1134">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1134">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-1135">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-1135">Storage</span></span>

* <span data-ttu-id="29c35-1136">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1136">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1137">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1137">VM</span></span>

* <span data-ttu-id="29c35-1138">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1138">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="29c35-1139">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1139">February 13, 2018</span></span>

<span data-ttu-id="29c35-1140">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="29c35-1140">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="29c35-1141">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-1141">Core</span></span>

* <span data-ttu-id="29c35-1142">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1142">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1143">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1143">ACS</span></span>

* <span data-ttu-id="29c35-1144">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1144">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="29c35-1145">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1145">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="29c35-1146">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1146">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="29c35-1147">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1147">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="29c35-1148">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1148">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="29c35-1149">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1149">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="29c35-1150">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1150">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="29c35-1151">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="29c35-1151">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1152">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1152">Appservice</span></span>

* <span data-ttu-id="29c35-1153">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1153">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="29c35-1154">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1154">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="29c35-1155">CDN</span><span class="sxs-lookup"><span data-stu-id="29c35-1155">CDN</span></span>

* <span data-ttu-id="29c35-1156">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1156">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="29c35-1157">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-1157">Container</span></span>

* <span data-ttu-id="29c35-1158">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1158">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="29c35-1159">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1159">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="29c35-1160">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="29c35-1160">CosmosDB</span></span>

* <span data-ttu-id="29c35-1161">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1161">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="29c35-1162">拡張機能</span><span class="sxs-lookup"><span data-stu-id="29c35-1162">Extension</span></span>

* <span data-ttu-id="29c35-1163">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1163">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="29c35-1164">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1164">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="29c35-1165">フィードバック</span><span class="sxs-lookup"><span data-stu-id="29c35-1165">Feedback</span></span>

* <span data-ttu-id="29c35-1166">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1166">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="29c35-1167">Interactive</span><span class="sxs-lookup"><span data-stu-id="29c35-1167">Interactive</span></span>

* <span data-ttu-id="29c35-1168">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1168">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="29c35-1169">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1169">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="29c35-1170">IoT</span><span class="sxs-lookup"><span data-stu-id="29c35-1170">IoT</span></span>

* <span data-ttu-id="29c35-1171">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1171">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="29c35-1172">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1172">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="29c35-1173">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1173">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="29c35-1174">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1174">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="29c35-1175">監視</span><span class="sxs-lookup"><span data-stu-id="29c35-1175">Monitor</span></span>

* <span data-ttu-id="29c35-1176">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1176">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="29c35-1177">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1177">Network</span></span>

* <span data-ttu-id="29c35-1178">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1178">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="29c35-1179">プロファイル</span><span class="sxs-lookup"><span data-stu-id="29c35-1179">Profile</span></span>

* <span data-ttu-id="29c35-1180">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1180">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-1181">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-1181">Resource</span></span>

* <span data-ttu-id="29c35-1182">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1182">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="29c35-1183">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-1183">Role</span></span>

* <span data-ttu-id="29c35-1184">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1184">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-1185">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-1185">SQL</span></span>

* <span data-ttu-id="29c35-1186">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1186">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="29c35-1187">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1187">Added `sql db rename`</span></span>
* <span data-ttu-id="29c35-1188">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1188">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-1189">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-1189">Storage</span></span>

* <span data-ttu-id="29c35-1190">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1190">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1191">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1191">VM</span></span>

* <span data-ttu-id="29c35-1192">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1192">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="29c35-1193">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1193">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="29c35-1194">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="29c35-1194">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="29c35-1195">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1195">January 31, 2018</span></span>

<span data-ttu-id="29c35-1196">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="29c35-1196">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="29c35-1197">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-1197">Core</span></span>

* <span data-ttu-id="29c35-1198">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1198">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="29c35-1199">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1199">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="29c35-1200">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1200">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="29c35-1201">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="29c35-1201">Use `--verbose` to see</span></span>
* <span data-ttu-id="29c35-1202">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="29c35-1202">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1203">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1203">ACS</span></span>

* <span data-ttu-id="29c35-1204">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1204">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="29c35-1205">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1205">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1206">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1206">Appservice</span></span>

* <span data-ttu-id="29c35-1207">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="29c35-1207">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="29c35-1208">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1208">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="29c35-1209">CDN</span><span class="sxs-lookup"><span data-stu-id="29c35-1209">CDN</span></span>

* <span data-ttu-id="29c35-1210">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1210">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="29c35-1211">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="29c35-1211">CosmosDB</span></span>

* <span data-ttu-id="29c35-1212">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1212">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="29c35-1213">Interactive</span><span class="sxs-lookup"><span data-stu-id="29c35-1213">Interactive</span></span>

* <span data-ttu-id="29c35-1214">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1214">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="29c35-1215">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1215">Network</span></span>

* <span data-ttu-id="29c35-1216">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1216">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="29c35-1217">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1217">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="29c35-1218">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1218">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="29c35-1219">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1219">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="29c35-1220">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1220">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="29c35-1221">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1221">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="29c35-1222">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1222">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="29c35-1223">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1223">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="29c35-1224">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1224">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="29c35-1225">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1225">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="29c35-1226">プロファイル</span><span class="sxs-lookup"><span data-stu-id="29c35-1226">Profile</span></span>

* <span data-ttu-id="29c35-1227">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1227">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-1228">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-1228">Resource</span></span>

* <span data-ttu-id="29c35-1229">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1229">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-1230">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-1230">Storage</span></span>

* <span data-ttu-id="29c35-1231">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1231">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="29c35-1232">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1232">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="29c35-1233">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1233">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="29c35-1234">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1234">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="29c35-1235">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1235">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1236">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1236">VM</span></span>

* <span data-ttu-id="29c35-1237">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1237">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="29c35-1238">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1238">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="29c35-1239">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1239">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="29c35-1240">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1240">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="29c35-1241">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1241">January 17, 2018</span></span>

<span data-ttu-id="29c35-1242">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="29c35-1242">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-1243">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-1243">ACR</span></span>

* <span data-ttu-id="29c35-1244">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1244">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="29c35-1245">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1245">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1246">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1246">ACS</span></span>

* <span data-ttu-id="29c35-1247">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1247">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="29c35-1248">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1248">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1249">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1249">Appservice</span></span>

* <span data-ttu-id="29c35-1250">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1250">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="29c35-1251">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1251">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="29c35-1252">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1252">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="29c35-1253">バックアップ</span><span class="sxs-lookup"><span data-stu-id="29c35-1253">Backup</span></span>

* <span data-ttu-id="29c35-1254">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1254">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="29c35-1255">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1255">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="29c35-1256">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1256">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="29c35-1257">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1257">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="29c35-1258">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1258">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="29c35-1259">Batch</span><span class="sxs-lookup"><span data-stu-id="29c35-1259">Batch</span></span>

* <span data-ttu-id="29c35-1260">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1260">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="29c35-1261">クラウド</span><span class="sxs-lookup"><span data-stu-id="29c35-1261">Cloud</span></span>

* <span data-ttu-id="29c35-1262">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1262">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="29c35-1263">消費</span><span class="sxs-lookup"><span data-stu-id="29c35-1263">Consumption</span></span>

* <span data-ttu-id="29c35-1264">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1264">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="29c35-1265">Event Grid</span><span class="sxs-lookup"><span data-stu-id="29c35-1265">Event Grid</span></span>

* <span data-ttu-id="29c35-1266">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1266">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="29c35-1267">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1267">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="29c35-1268">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1268">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="29c35-1269">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="29c35-1269">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="29c35-1270">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1270">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="29c35-1271">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1271">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="29c35-1272">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1272">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="29c35-1273">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1273">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="29c35-1274">Interactive</span><span class="sxs-lookup"><span data-stu-id="29c35-1274">Interactive</span></span>

* <span data-ttu-id="29c35-1275">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1275">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="29c35-1276">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1276">Fixed errors on startup</span></span>
* <span data-ttu-id="29c35-1277">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1277">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="29c35-1278">IoT</span><span class="sxs-lookup"><span data-stu-id="29c35-1278">IoT</span></span>

* <span data-ttu-id="29c35-1279">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1279">Added support for device provisioning service</span></span>
* <span data-ttu-id="29c35-1280">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1280">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="29c35-1281">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1281">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="29c35-1282">監視</span><span class="sxs-lookup"><span data-stu-id="29c35-1282">Monitor</span></span>

* <span data-ttu-id="29c35-1283">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1283">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="29c35-1284">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1284">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="29c35-1285">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1285">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="29c35-1286">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1286">Network</span></span>

* <span data-ttu-id="29c35-1287">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1287">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="29c35-1288">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1288">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="29c35-1289">プロファイル</span><span class="sxs-lookup"><span data-stu-id="29c35-1289">Profile</span></span>

* <span data-ttu-id="29c35-1290">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1290">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="29c35-1291">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-1291">Role</span></span>

* <span data-ttu-id="29c35-1292">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1292">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="29c35-1293">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="29c35-1293">Service Fabric</span></span>

* <span data-ttu-id="29c35-1294">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1294">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="29c35-1295">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1295">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1296">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1296">VM</span></span>

* <span data-ttu-id="29c35-1297">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="29c35-1297">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="29c35-1298">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1298">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="29c35-1299">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1299">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="29c35-1300">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1300">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="29c35-1301">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1301">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="29c35-1302">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1302">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="29c35-1303">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1303">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="29c35-1304">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1304">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="29c35-1305">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1305">December 19, 2017</span></span>

<span data-ttu-id="29c35-1306">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="29c35-1306">Version 2.0.23</span></span>

* <span data-ttu-id="29c35-1307">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1307">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="29c35-1308">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-1308">Container</span></span>

* <span data-ttu-id="29c35-1309">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1309">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="29c35-1310">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1310">Network</span></span>

* <span data-ttu-id="29c35-1311">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1311">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="29c35-1312">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1312">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-1313">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-1313">Storage</span></span>

* <span data-ttu-id="29c35-1314">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1314">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1315">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1315">VM</span></span>

* <span data-ttu-id="29c35-1316">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1316">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="29c35-1317">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1317">December 5, 2017</span></span>

<span data-ttu-id="29c35-1318">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="29c35-1318">Version 2.0.22</span></span>

* <span data-ttu-id="29c35-1319">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1319">Removed `az component` commands.</span></span> <span data-ttu-id="29c35-1320">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="29c35-1320">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="29c35-1321">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-1321">Core</span></span>
* <span data-ttu-id="29c35-1322">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1322">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="29c35-1323">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1323">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1324">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1324">ACS</span></span>

* <span data-ttu-id="29c35-1325">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1325">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="29c35-1326">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1326">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="29c35-1327">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1327">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="29c35-1328">Advisor</span><span class="sxs-lookup"><span data-stu-id="29c35-1328">Advisor</span></span>

* <span data-ttu-id="29c35-1329">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="29c35-1329">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1330">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1330">Appservice</span></span>

* <span data-ttu-id="29c35-1331">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1331">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="29c35-1332">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1332">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="29c35-1333">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1333">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="29c35-1334">消費</span><span class="sxs-lookup"><span data-stu-id="29c35-1334">Consumption</span></span>

* <span data-ttu-id="29c35-1335">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1335">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="29c35-1336">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-1336">Container</span></span>

* <span data-ttu-id="29c35-1337">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1337">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="29c35-1338">監視</span><span class="sxs-lookup"><span data-stu-id="29c35-1338">Monitor</span></span>

* <span data-ttu-id="29c35-1339">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1339">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-1340">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-1340">Resource</span></span>

* <span data-ttu-id="29c35-1341">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1341">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="29c35-1342">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-1342">Role</span></span>

* <span data-ttu-id="29c35-1343">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1343">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="29c35-1344">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1344">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="29c35-1345">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1345">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-1346">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-1346">SQL</span></span>

* <span data-ttu-id="29c35-1347">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1347">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="29c35-1348">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1348">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1349">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1349">VM</span></span>

* <span data-ttu-id="29c35-1350">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1350">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="29c35-1351">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1351">November 14, 2017</span></span>

<span data-ttu-id="29c35-1352">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="29c35-1352">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-1353">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-1353">ACR</span></span>

* <span data-ttu-id="29c35-1354">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1354">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="29c35-1355">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1355">ACS</span></span>

* <span data-ttu-id="29c35-1356">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1356">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="29c35-1357">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1357">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="29c35-1358">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1358">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="29c35-1359">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1359">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="29c35-1360">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1360">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1361">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1361">Appservice</span></span>

* <span data-ttu-id="29c35-1362">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1362">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="29c35-1363">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1363">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="29c35-1364">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1364">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="29c35-1365">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1365">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="29c35-1366">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1366">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="29c35-1367">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="29c35-1367">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="29c35-1368">Batch</span><span class="sxs-lookup"><span data-stu-id="29c35-1368">Batch</span></span>

* <span data-ttu-id="29c35-1369">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1369">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="29c35-1370">Batchai</span><span class="sxs-lookup"><span data-stu-id="29c35-1370">Batchai</span></span>

* <span data-ttu-id="29c35-1371">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1371">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="29c35-1372">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1372">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="29c35-1373">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1373">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="29c35-1374">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1374">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="29c35-1375">クラウド</span><span class="sxs-lookup"><span data-stu-id="29c35-1375">Cloud</span></span>

* <span data-ttu-id="29c35-1376">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1376">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="29c35-1377">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-1377">Container</span></span>

* <span data-ttu-id="29c35-1378">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1378">Added support to open multiple ports</span></span>
* <span data-ttu-id="29c35-1379">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1379">Added container group restart policy</span></span>
* <span data-ttu-id="29c35-1380">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1380">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="29c35-1381">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1381">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="29c35-1382">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="29c35-1382">Data Lake Analytics</span></span>

* <span data-ttu-id="29c35-1383">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1383">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="29c35-1384">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="29c35-1384">Data Lake Store</span></span>

* <span data-ttu-id="29c35-1385">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1385">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="29c35-1386">拡張機能</span><span class="sxs-lookup"><span data-stu-id="29c35-1386">Extension</span></span>

* <span data-ttu-id="29c35-1387">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1387">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="29c35-1388">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1388">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="29c35-1389">IoT</span><span class="sxs-lookup"><span data-stu-id="29c35-1389">IoT</span></span>

* <span data-ttu-id="29c35-1390">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1390">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="29c35-1391">監視</span><span class="sxs-lookup"><span data-stu-id="29c35-1391">Monitor</span></span>

* <span data-ttu-id="29c35-1392">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1392">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="29c35-1393">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1393">Network</span></span>

* <span data-ttu-id="29c35-1394">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1394">Added support for CAA DNS records</span></span>
* <span data-ttu-id="29c35-1395">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1395">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="29c35-1396">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1396">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="29c35-1397">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1397">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="29c35-1398">Reservations</span><span class="sxs-lookup"><span data-stu-id="29c35-1398">Reservations</span></span>

* <span data-ttu-id="29c35-1399">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="29c35-1399">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-1400">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-1400">Resource</span></span>

* <span data-ttu-id="29c35-1401">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1401">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-1402">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-1402">SQL</span></span>

* <span data-ttu-id="29c35-1403">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1403">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-1404">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-1404">Storage</span></span>

* <span data-ttu-id="29c35-1405">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1405">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="29c35-1406">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1406">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="29c35-1407">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1407">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="29c35-1408">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1408">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="29c35-1409">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1409">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="29c35-1410">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1410">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="29c35-1411">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1411">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1412">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1412">VM</span></span>

* <span data-ttu-id="29c35-1413">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1413">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="29c35-1414">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1414">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="29c35-1415">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1415">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="29c35-1416">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1416">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="29c35-1417">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1417">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="29c35-1418">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1418">October 24, 2017</span></span>

<span data-ttu-id="29c35-1419">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="29c35-1419">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="29c35-1420">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-1420">Core</span></span>

* <span data-ttu-id="29c35-1421">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1421">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-1422">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-1422">ACR</span></span>

* <span data-ttu-id="29c35-1423">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1423">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="29c35-1424">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1424">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="29c35-1425">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1425">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1426">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1426">ACS</span></span>

* <span data-ttu-id="29c35-1427">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1427">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="29c35-1428">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1428">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1429">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1429">Appservice</span></span>

* <span data-ttu-id="29c35-1430">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1430">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="29c35-1431">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="29c35-1431">Component</span></span>

* <span data-ttu-id="29c35-1432">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1432">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="29c35-1433">監視</span><span class="sxs-lookup"><span data-stu-id="29c35-1433">Monitor</span></span>

* <span data-ttu-id="29c35-1434">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1434">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-1435">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-1435">Resource</span></span>

* <span data-ttu-id="29c35-1436">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1436">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="29c35-1437">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1437">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1438">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1438">VM</span></span>

* <span data-ttu-id="29c35-1439">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1439">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="29c35-1440">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1440">October 9, 2017</span></span>

<span data-ttu-id="29c35-1441">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="29c35-1441">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="29c35-1442">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-1442">Core</span></span>

* <span data-ttu-id="29c35-1443">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1443">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1444">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1444">Appservice</span></span>

* <span data-ttu-id="29c35-1445">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1445">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="29c35-1446">Batch</span><span class="sxs-lookup"><span data-stu-id="29c35-1446">Batch</span></span>

* <span data-ttu-id="29c35-1447">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1447">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="29c35-1448">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1448">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="29c35-1449">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1449">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="29c35-1450">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1450">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="29c35-1451">Batchai</span><span class="sxs-lookup"><span data-stu-id="29c35-1451">Batchai</span></span>

* <span data-ttu-id="29c35-1452">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="29c35-1452">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="29c35-1453">KeyVault</span><span class="sxs-lookup"><span data-stu-id="29c35-1453">Keyvault</span></span>

* <span data-ttu-id="29c35-1454">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1454">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="29c35-1455">(#4448)</span><span class="sxs-lookup"><span data-stu-id="29c35-1455">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="29c35-1456">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1456">Network</span></span>

* <span data-ttu-id="29c35-1457">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1457">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="29c35-1458">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1458">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-1459">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-1459">Resource</span></span>

* <span data-ttu-id="29c35-1460">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1460">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="29c35-1461">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1461">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="29c35-1462">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1462">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="29c35-1463">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1463">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-1464">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-1464">Sql</span></span>

* <span data-ttu-id="29c35-1465">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1465">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="29c35-1466">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1466">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="29c35-1467">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1467">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-1468">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-1468">Storage</span></span>

* <span data-ttu-id="29c35-1469">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1469">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1470">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1470">Vm</span></span>

* <span data-ttu-id="29c35-1471">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1471">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="29c35-1472">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1472">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="29c35-1473">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1473">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="29c35-1474">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1474">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="29c35-1475">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1475">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="29c35-1476">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1476">September 22, 2017</span></span>

<span data-ttu-id="29c35-1477">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="29c35-1477">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-1478">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-1478">Resource</span></span>

* <span data-ttu-id="29c35-1479">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1479">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="29c35-1480">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1480">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="29c35-1481">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1481">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="29c35-1482">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1482">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="29c35-1483">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1483">Network</span></span>

* <span data-ttu-id="29c35-1484">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1484">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="29c35-1485">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1485">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="29c35-1486">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1486">Added `asg` application security group commands</span></span>
* <span data-ttu-id="29c35-1487">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1487">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="29c35-1488">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1488">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="29c35-1489">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1489">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="29c35-1490">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1490">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-1491">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-1491">Storage</span></span>

* <span data-ttu-id="29c35-1492">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1492">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="29c35-1493">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="29c35-1493">Eventgrid</span></span>

* <span data-ttu-id="29c35-1494">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1494">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-1495">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-1495">SQL</span></span>

* <span data-ttu-id="29c35-1496">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1496">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="29c35-1497">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="29c35-1497">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="29c35-1498">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1498">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="29c35-1499">KeyVault</span><span class="sxs-lookup"><span data-stu-id="29c35-1499">Keyvault</span></span>

* <span data-ttu-id="29c35-1500">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1500">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1501">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1501">VM</span></span>

* <span data-ttu-id="29c35-1502">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1502">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="29c35-1503">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1503">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="29c35-1504">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1504">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="29c35-1505">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1505">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="29c35-1506">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1506">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="29c35-1507">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1507">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1508">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1508">ACS</span></span>

* <span data-ttu-id="29c35-1509">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1509">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1510">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1510">Appservice</span></span>

* <span data-ttu-id="29c35-1511">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1511">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="29c35-1512">バックアップ</span><span class="sxs-lookup"><span data-stu-id="29c35-1512">Backup</span></span>

* <span data-ttu-id="29c35-1513">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="29c35-1513">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="29c35-1514">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1514">September 11, 2017</span></span>

<span data-ttu-id="29c35-1515">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="29c35-1515">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="29c35-1516">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-1516">Core</span></span>

* <span data-ttu-id="29c35-1517">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1517">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="29c35-1518">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1518">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1519">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1519">Acs</span></span>

* <span data-ttu-id="29c35-1520">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1520">Added `acs list-locations` command</span></span>
* <span data-ttu-id="29c35-1521">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1521">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1522">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1522">Appservice</span></span>

* <span data-ttu-id="29c35-1523">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1523">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="29c35-1524">CDN</span><span class="sxs-lookup"><span data-stu-id="29c35-1524">CDN</span></span>

* <span data-ttu-id="29c35-1525">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1525">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="29c35-1526">拡張機能</span><span class="sxs-lookup"><span data-stu-id="29c35-1526">Extension</span></span>

* <span data-ttu-id="29c35-1527">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="29c35-1527">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="29c35-1528">KeyVault</span><span class="sxs-lookup"><span data-stu-id="29c35-1528">Keyvault</span></span>

* <span data-ttu-id="29c35-1529">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1529">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="29c35-1530">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1530">Network</span></span>

* <span data-ttu-id="29c35-1531">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1531">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="29c35-1532">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1532">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="29c35-1533">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1533">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="29c35-1534">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1534">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="29c35-1535">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1535">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-1536">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-1536">Resource</span></span>

* <span data-ttu-id="29c35-1537">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="29c35-1537">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="29c35-1538">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="29c35-1538">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="29c35-1539">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="29c35-1539">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="29c35-1540">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1540">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-1541">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-1541">SQL</span></span>

* <span data-ttu-id="29c35-1542">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1542">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1543">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1543">VM</span></span>

* <span data-ttu-id="29c35-1544">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="29c35-1544">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="29c35-1545">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="29c35-1545">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="29c35-1546">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1546">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="29c35-1547">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="29c35-1547">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="29c35-1548">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="29c35-1548">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="29c35-1549">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1549">August 31, 2017</span></span>

<span data-ttu-id="29c35-1550">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="29c35-1550">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="29c35-1551">KeyVault</span><span class="sxs-lookup"><span data-stu-id="29c35-1551">Keyvault</span></span>

* <span data-ttu-id="29c35-1552">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1552">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="29c35-1553">SF</span><span class="sxs-lookup"><span data-stu-id="29c35-1553">Sf</span></span>

* <span data-ttu-id="29c35-1554">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="29c35-1554">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-1555">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-1555">Storage</span></span>

* <span data-ttu-id="29c35-1556">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1556">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="29c35-1557">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="29c35-1557">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="29c35-1558">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1558">August 28, 2017</span></span>

<span data-ttu-id="29c35-1559">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="29c35-1559">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="29c35-1560">CLI</span><span class="sxs-lookup"><span data-stu-id="29c35-1560">CLI</span></span>

* <span data-ttu-id="29c35-1561">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1561">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1562">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1562">ACS</span></span>

* <span data-ttu-id="29c35-1563">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1563">Corrected preview regions</span></span>
* <span data-ttu-id="29c35-1564">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1564">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="29c35-1565">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1565">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1566">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1566">Appservice</span></span>

* <span data-ttu-id="29c35-1567">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1567">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="29c35-1568">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1568">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="29c35-1569">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1569">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="29c35-1570">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1570">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="29c35-1571">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="29c35-1571">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="29c35-1572">IoT</span><span class="sxs-lookup"><span data-stu-id="29c35-1572">IoT</span></span>

* <span data-ttu-id="29c35-1573">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1573">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="29c35-1574">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1574">Network</span></span>

* <span data-ttu-id="29c35-1575">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1575">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="29c35-1576">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1576">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="29c35-1577">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1577">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="29c35-1578">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1578">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="29c35-1579">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1579">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="29c35-1580">プロファイル</span><span class="sxs-lookup"><span data-stu-id="29c35-1580">Profile</span></span>

* <span data-ttu-id="29c35-1581">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1581">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="29c35-1582">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="29c35-1582">Service Fabric</span></span>

* <span data-ttu-id="29c35-1583">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="29c35-1583">Preview release</span></span>
* <span data-ttu-id="29c35-1584">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1584">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="29c35-1585">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1585">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="29c35-1586">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1586">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-1587">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-1587">Storage</span></span>

* <span data-ttu-id="29c35-1588">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1588">Enabled setting blob tier</span></span>
* <span data-ttu-id="29c35-1589">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1589">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="29c35-1590">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1590">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="29c35-1591">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1591">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="29c35-1592">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1592">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="29c35-1593">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="29c35-1593">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1594">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1594">VM</span></span>

* <span data-ttu-id="29c35-1595">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1595">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="29c35-1596">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1596">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="29c35-1597">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1597">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="29c35-1598">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1598">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="29c35-1599">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1599">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="29c35-1600">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1600">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="29c35-1601">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1601">August 15, 2017</span></span>

<span data-ttu-id="29c35-1602">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="29c35-1602">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1603">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1603">ACS</span></span>

* <span data-ttu-id="29c35-1604">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1604">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1605">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1605">Appservice</span></span>

* <span data-ttu-id="29c35-1606">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1606">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="29c35-1607">Event Grid</span><span class="sxs-lookup"><span data-stu-id="29c35-1607">Event Grid</span></span>

* <span data-ttu-id="29c35-1608">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1608">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="29c35-1609">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1609">August 11, 2017</span></span>

<span data-ttu-id="29c35-1610">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="29c35-1610">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1611">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1611">ACS</span></span>

* <span data-ttu-id="29c35-1612">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1612">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="29c35-1613">Batch</span><span class="sxs-lookup"><span data-stu-id="29c35-1613">Batch</span></span>

* <span data-ttu-id="29c35-1614">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1614">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="29c35-1615">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1615">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="29c35-1616">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1616">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="29c35-1617">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1617">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="29c35-1618">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1618">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="29c35-1619">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1619">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="29c35-1620">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="29c35-1620">Component</span></span>

* <span data-ttu-id="29c35-1621">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1621">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="29c35-1622">コンテナー</span><span class="sxs-lookup"><span data-stu-id="29c35-1622">Container</span></span>

* <span data-ttu-id="29c35-1623">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1623">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="29c35-1624">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="29c35-1624">Data Lake Store</span></span>

* <span data-ttu-id="29c35-1625">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1625">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="29c35-1626">Event Grid</span><span class="sxs-lookup"><span data-stu-id="29c35-1626">Event Grid</span></span>

* <span data-ttu-id="29c35-1627">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="29c35-1627">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="29c35-1628">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1628">Network</span></span>

* <span data-ttu-id="29c35-1629">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1629">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="29c35-1630">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1630">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="29c35-1631">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1631">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="29c35-1632">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1632">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="29c35-1633">プロファイル</span><span class="sxs-lookup"><span data-stu-id="29c35-1633">Profile</span></span>

* <span data-ttu-id="29c35-1634">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1634">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-1635">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-1635">Storage</span></span>

* <span data-ttu-id="29c35-1636">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="29c35-1636">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1637">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1637">VM</span></span>

* <span data-ttu-id="29c35-1638">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1638">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="29c35-1639">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1639">Exposed `list-skus` command</span></span>
* <span data-ttu-id="29c35-1640">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1640">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="29c35-1641">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="29c35-1641">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="29c35-1642">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1642">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="29c35-1643">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1643">July 28, 2017</span></span>

<span data-ttu-id="29c35-1644">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="29c35-1644">Version 2.0.12</span></span>

* <span data-ttu-id="29c35-1645">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1645">Added container commands</span></span>
* <span data-ttu-id="29c35-1646">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1646">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="29c35-1647">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-1647">Core</span></span>

* <span data-ttu-id="29c35-1648">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="29c35-1648">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="29c35-1649">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1649">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="29c35-1650">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="29c35-1650">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="29c35-1651">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="29c35-1651">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="29c35-1652">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="29c35-1652">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="29c35-1653">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="29c35-1653">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="29c35-1654">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="29c35-1654">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="29c35-1655">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="29c35-1655">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="29c35-1656">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="29c35-1656">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="29c35-1657">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="29c35-1657">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="29c35-1658">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="29c35-1658">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="29c35-1659">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="29c35-1659">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="29c35-1660">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1660">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="29c35-1661">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1661">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="29c35-1662">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1662">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="29c35-1663">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="29c35-1663">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="29c35-1664">ACR</span><span class="sxs-lookup"><span data-stu-id="29c35-1664">ACR</span></span>

* <span data-ttu-id="29c35-1665">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1665">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="29c35-1666">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1666">Support SKU update for managed registries</span></span>
* <span data-ttu-id="29c35-1667">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1667">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="29c35-1668">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1668">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="29c35-1669">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1669">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="29c35-1670">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1670">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1671">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1671">ACS</span></span>

* <span data-ttu-id="29c35-1672">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1672">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1673">Appservice</span><span class="sxs-lookup"><span data-stu-id="29c35-1673">Appservice</span></span>

* <span data-ttu-id="29c35-1674">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1674">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="29c35-1675">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1675">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="29c35-1676">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="29c35-1676">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="29c35-1677">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="29c35-1677">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="29c35-1678">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="29c35-1678">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="29c35-1679">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="29c35-1679">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="29c35-1680">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="29c35-1680">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="29c35-1681">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="29c35-1681">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="29c35-1682">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1682">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="29c35-1683">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="29c35-1683">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="29c35-1684">Batch</span><span class="sxs-lookup"><span data-stu-id="29c35-1684">Batch</span></span>

* <span data-ttu-id="29c35-1685">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1685">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="29c35-1686">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1686">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="29c35-1687">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1687">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="29c35-1688">CDN</span><span class="sxs-lookup"><span data-stu-id="29c35-1688">CDN</span></span>

* <span data-ttu-id="29c35-1689">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1689">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="29c35-1690">クラウド</span><span class="sxs-lookup"><span data-stu-id="29c35-1690">Cloud</span></span>

* <span data-ttu-id="29c35-1691">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1691">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="29c35-1692">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="29c35-1692">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="29c35-1693">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1693">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="29c35-1694">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1694">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="29c35-1695">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1695">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="29c35-1696">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="29c35-1696">CosmosDB</span></span>

* <span data-ttu-id="29c35-1697">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1697">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="29c35-1698">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1698">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="29c35-1699">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="29c35-1699">Data Lake Analytics</span></span>

* <span data-ttu-id="29c35-1700">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1700">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="29c35-1701">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1701">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="29c35-1702">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1702">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="29c35-1703">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="29c35-1703">Data Lake Store</span></span>

* <span data-ttu-id="29c35-1704">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1704">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="29c35-1705">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1705">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="29c35-1706">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1706">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="29c35-1707">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="29c35-1707">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="29c35-1708">対話</span><span class="sxs-lookup"><span data-stu-id="29c35-1708">Interactive</span></span>

* <span data-ttu-id="29c35-1709">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1709">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="29c35-1710">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="29c35-1710">Increased test coverage</span></span>
* <span data-ttu-id="29c35-1711">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1711">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="29c35-1712">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="29c35-1712">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="29c35-1713">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="29c35-1713">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="29c35-1714">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="29c35-1714">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="29c35-1715">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="29c35-1715">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="29c35-1716">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1716">Added `--progress` flag</span></span>
* <span data-ttu-id="29c35-1717">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1717">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="29c35-1718">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="29c35-1718">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="29c35-1719">IoT</span><span class="sxs-lookup"><span data-stu-id="29c35-1719">IoT</span></span>

* <span data-ttu-id="29c35-1720">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1720">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="29c35-1721">(#3934)</span><span class="sxs-lookup"><span data-stu-id="29c35-1721">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="29c35-1722">Key Vault</span><span class="sxs-lookup"><span data-stu-id="29c35-1722">Key vault</span></span>

* <span data-ttu-id="29c35-1723">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1723">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="29c35-1724">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="29c35-1724">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="29c35-1725">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="29c35-1725">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="29c35-1726">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="29c35-1726">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="29c35-1727">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="29c35-1727">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="29c35-1728">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="29c35-1728">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="29c35-1729">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1729">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="29c35-1730">(#3307)</span><span class="sxs-lookup"><span data-stu-id="29c35-1730">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="29c35-1731">ラボ</span><span class="sxs-lookup"><span data-stu-id="29c35-1731">Lab</span></span>

* <span data-ttu-id="29c35-1732">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1732">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="29c35-1733">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1733">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="29c35-1734">監視</span><span class="sxs-lookup"><span data-stu-id="29c35-1734">Monitor</span></span>

* <span data-ttu-id="29c35-1735">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="29c35-1735">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="29c35-1736">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1736">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="29c35-1737">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1737">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="29c35-1738">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1738">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="29c35-1739">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1739">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="29c35-1740">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1740">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="29c35-1741">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1741">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="29c35-1742">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="29c35-1742">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="29c35-1743">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1743">`location` no longer required</span></span>
  * <span data-ttu-id="29c35-1744">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="29c35-1744">Add name and ID support for target</span></span>
  * <span data-ttu-id="29c35-1745">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="29c35-1745">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="29c35-1746">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1746">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="29c35-1747">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1747">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="29c35-1748">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="29c35-1748">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="29c35-1749">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1749">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="29c35-1750">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1750">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="29c35-1751">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1751">Network</span></span>

* <span data-ttu-id="29c35-1752">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1752">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="29c35-1753">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1753">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="29c35-1754">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1754">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="29c35-1755">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1755">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="29c35-1756">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1756">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="29c35-1757">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1757">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="29c35-1758">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1758">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="29c35-1759">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1759">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="29c35-1760">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1760">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="29c35-1761">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1761">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="29c35-1762">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1762">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="29c35-1763">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1763">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="29c35-1764">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1764">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="29c35-1765">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1765">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="29c35-1766">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1766">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="29c35-1767">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1767">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="29c35-1768">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1768">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="29c35-1769">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1769">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="29c35-1770">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1770">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="29c35-1771">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1771">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="29c35-1772">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1772">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="29c35-1773">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1773">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="29c35-1774">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1774">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="29c35-1775">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="29c35-1775">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="29c35-1776">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="29c35-1776">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="29c35-1777">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="29c35-1777">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="29c35-1778">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="29c35-1778">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="29c35-1779">プロファイル</span><span class="sxs-lookup"><span data-stu-id="29c35-1779">Profile</span></span>

* <span data-ttu-id="29c35-1780">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1780">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="29c35-1781">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1781">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="29c35-1782">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="29c35-1782">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="29c35-1783">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1783">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="29c35-1784">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1784">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="29c35-1785">RDBMS</span><span class="sxs-lookup"><span data-stu-id="29c35-1785">RDBMS</span></span>

* <span data-ttu-id="29c35-1786">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="29c35-1786">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="29c35-1787">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="29c35-1787">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="29c35-1788">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="29c35-1788">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="29c35-1789">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="29c35-1789">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-1790">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-1790">Resource</span></span>

* <span data-ttu-id="29c35-1791">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1791">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="29c35-1792">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1792">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="29c35-1793">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1793">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="29c35-1794">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1794">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="29c35-1795">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="29c35-1795">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="29c35-1796">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1796">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="29c35-1797">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="29c35-1797">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="29c35-1798">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1798">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="29c35-1799">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-1799">Role</span></span>

* <span data-ttu-id="29c35-1800">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1800">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="29c35-1801">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="29c35-1801">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="29c35-1802">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="29c35-1802">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="29c35-1803">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="29c35-1803">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="29c35-1804">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1804">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="29c35-1805">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="29c35-1805">Service Fabric</span></span>
* <span data-ttu-id="29c35-1806">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="29c35-1806">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="29c35-1807">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="29c35-1807">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="29c35-1808">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="29c35-1808">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-1809">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-1809">SQL</span></span>

* <span data-ttu-id="29c35-1810">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1810">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="29c35-1811">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1811">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="29c35-1812">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1812">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-1813">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-1813">Storage</span></span>

* <span data-ttu-id="29c35-1814">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="29c35-1814">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="29c35-1815">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1815">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="29c35-1816">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="29c35-1816">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="29c35-1817">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="29c35-1817">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="29c35-1818">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="29c35-1818">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="29c35-1819">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="29c35-1819">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1820">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1820">VM</span></span>

* <span data-ttu-id="29c35-1821">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1821">Support configuring nsg</span></span>
* <span data-ttu-id="29c35-1822">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1822">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="29c35-1823">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="29c35-1823">Support managed service identities</span></span>
* <span data-ttu-id="29c35-1824">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1824">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="29c35-1825">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="29c35-1825">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="29c35-1826">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1826">May 10, 2017</span></span>

<span data-ttu-id="29c35-1827">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="29c35-1827">Version 2.0.6</span></span>

* <span data-ttu-id="29c35-1828">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1828">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="29c35-1829">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1829">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="29c35-1830">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1830">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="29c35-1831">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1831">Include Cognitive Services module</span></span>
* <span data-ttu-id="29c35-1832">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1832">Include Service Fabric module</span></span>
* <span data-ttu-id="29c35-1833">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="29c35-1833">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="29c35-1834">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1834">Add support for CDN commands</span></span>
* <span data-ttu-id="29c35-1835">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1835">Remove Container module</span></span>
* <span data-ttu-id="29c35-1836">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="29c35-1836">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="29c35-1837">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="29c35-1837">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="29c35-1838">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-1838">Core</span></span>

* <span data-ttu-id="29c35-1839">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="29c35-1839">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="29c35-1840">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="29c35-1840">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="29c35-1841">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="29c35-1841">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="29c35-1842">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="29c35-1842">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="29c35-1843">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="29c35-1843">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="29c35-1844">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="29c35-1844">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="29c35-1845">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="29c35-1845">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="29c35-1846">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="29c35-1846">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="29c35-1847">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="29c35-1847">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="29c35-1848">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="29c35-1848">core: Improved performance</span></span>
* <span data-ttu-id="29c35-1849">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="29c35-1849">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="29c35-1850">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="29c35-1850">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1851">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1851">ACS</span></span>

* <span data-ttu-id="29c35-1852">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1852">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="29c35-1853">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1853">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="29c35-1854">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1854">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="29c35-1855">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="29c35-1855">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1856">AppService</span><span class="sxs-lookup"><span data-stu-id="29c35-1856">AppService</span></span>

* <span data-ttu-id="29c35-1857">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1857">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="29c35-1858">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1858">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="29c35-1859">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="29c35-1859">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="29c35-1860">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1860">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="29c35-1861">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1861">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="29c35-1862">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="29c35-1862">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="29c35-1863">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="29c35-1863">support slot swap with preview</span></span>
* <span data-ttu-id="29c35-1864">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="29c35-1864">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="29c35-1865">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="29c35-1865">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="29c35-1866">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="29c35-1866">CosmosDB</span></span>

* <span data-ttu-id="29c35-1867">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1867">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="29c35-1868">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1868">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="29c35-1869">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1869">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="29c35-1870">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1870">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="29c35-1871">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="29c35-1871">Data Lake Analytics</span></span>

* <span data-ttu-id="29c35-1872">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1872">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="29c35-1873">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1873">Add support for new catalog item type: package.</span></span> <span data-ttu-id="29c35-1874">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="29c35-1874">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="29c35-1875">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="29c35-1875">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="29c35-1876">テーブル</span><span class="sxs-lookup"><span data-stu-id="29c35-1876">Table</span></span>
  * <span data-ttu-id="29c35-1877">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="29c35-1877">Table valued function</span></span>
  * <span data-ttu-id="29c35-1878">表示</span><span class="sxs-lookup"><span data-stu-id="29c35-1878">View</span></span>
  * <span data-ttu-id="29c35-1879">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="29c35-1879">Table Statistics.</span></span> <span data-ttu-id="29c35-1880">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="29c35-1880">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="29c35-1881">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="29c35-1881">Data Lake Store</span></span>

* <span data-ttu-id="29c35-1882">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1882">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="29c35-1883">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="29c35-1883">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="29c35-1884">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="29c35-1884">missed help for access show.</span></span> <span data-ttu-id="29c35-1885">追加しました </span><span class="sxs-lookup"><span data-stu-id="29c35-1885">adding it.</span></span> <span data-ttu-id="29c35-1886">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="29c35-1886">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="29c35-1887">検索</span><span class="sxs-lookup"><span data-stu-id="29c35-1887">Find</span></span>

* <span data-ttu-id="29c35-1888">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1888">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="29c35-1889">KeyVault</span><span class="sxs-lookup"><span data-stu-id="29c35-1889">KeyVault</span></span>

* <span data-ttu-id="29c35-1890">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1890">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="29c35-1891">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1891">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="29c35-1892">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="29c35-1892">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="29c35-1893">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1893">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="29c35-1894">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="29c35-1894">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="29c35-1895">ラボ</span><span class="sxs-lookup"><span data-stu-id="29c35-1895">Lab</span></span>

* <span data-ttu-id="29c35-1896">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1896">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="29c35-1897">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1897">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="29c35-1898">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1898">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="29c35-1899">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1899">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="29c35-1900">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1900">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="29c35-1901">監視</span><span class="sxs-lookup"><span data-stu-id="29c35-1901">Monitor</span></span>

* <span data-ttu-id="29c35-1902">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="29c35-1902">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="29c35-1903">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="29c35-1903">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="29c35-1904">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-1904">Network</span></span>

* <span data-ttu-id="29c35-1905">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1905">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="29c35-1906">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1906">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="29c35-1907">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1907">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="29c35-1908">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1908">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="29c35-1909">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1909">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="29c35-1910">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1910">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="29c35-1911">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1911">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="29c35-1912">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1912">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="29c35-1913">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1913">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="29c35-1914">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1914">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="29c35-1915">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1915">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="29c35-1916">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1916">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="29c35-1917">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1917">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="29c35-1918">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1918">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="29c35-1919">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="29c35-1919">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="29c35-1920">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1920">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="29c35-1921">プロファイル</span><span class="sxs-lookup"><span data-stu-id="29c35-1921">Profile</span></span>

* <span data-ttu-id="29c35-1922">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="29c35-1922">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="29c35-1923">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="29c35-1923">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="29c35-1924">Redis</span><span class="sxs-lookup"><span data-stu-id="29c35-1924">Redis</span></span>

* <span data-ttu-id="29c35-1925">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1925">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="29c35-1926">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1926">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="29c35-1927">リソース</span><span class="sxs-lookup"><span data-stu-id="29c35-1927">Resource</span></span>

* <span data-ttu-id="29c35-1928">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="29c35-1928">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="29c35-1929">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="29c35-1929">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="29c35-1930">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="29c35-1930">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="29c35-1931">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="29c35-1931">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="29c35-1932">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="29c35-1932">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="29c35-1933">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="29c35-1933">Add docs for az lock update.</span></span> <span data-ttu-id="29c35-1934">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="29c35-1934">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="29c35-1935">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="29c35-1935">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="29c35-1936">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="29c35-1936">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="29c35-1937">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="29c35-1937">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="29c35-1938">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="29c35-1938">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="29c35-1939">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="29c35-1939">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="29c35-1940">Role</span><span class="sxs-lookup"><span data-stu-id="29c35-1940">Role</span></span>

* <span data-ttu-id="29c35-1941">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="29c35-1941">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="29c35-1942">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="29c35-1942">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="29c35-1943">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="29c35-1943">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="29c35-1944">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="29c35-1944">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="29c35-1945">SQL</span><span class="sxs-lookup"><span data-stu-id="29c35-1945">SQL</span></span>

* <span data-ttu-id="29c35-1946">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="29c35-1946">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="29c35-1947">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="29c35-1947">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="29c35-1948">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-1948">Storage</span></span>

* <span data-ttu-id="29c35-1949">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="29c35-1949">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="29c35-1950">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1950">Add support for incremental blob copy</span></span>
* <span data-ttu-id="29c35-1951">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1951">Add support for large block blob upload</span></span>
* <span data-ttu-id="29c35-1952">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="29c35-1952">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1953">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1953">VM</span></span>

* <span data-ttu-id="29c35-1954">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="29c35-1954">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="29c35-1955">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="29c35-1955">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="29c35-1956">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="29c35-1956">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="29c35-1957">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="29c35-1957">az vm/vmss disk</span></span>
  3. <span data-ttu-id="29c35-1958">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="29c35-1958">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="29c35-1959">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="29c35-1959">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="29c35-1960">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="29c35-1960">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="29c35-1961">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="29c35-1961">April 3, 2017</span></span>

<span data-ttu-id="29c35-1962">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="29c35-1962">Version 2.0.2</span></span>

<span data-ttu-id="29c35-1963">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="29c35-1963">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="29c35-1964">コア</span><span class="sxs-lookup"><span data-stu-id="29c35-1964">Core</span></span>

* <span data-ttu-id="29c35-1965">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="29c35-1965">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="29c35-1966">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="29c35-1966">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="29c35-1967">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="29c35-1967">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="29c35-1968">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="29c35-1968">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="29c35-1969">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="29c35-1969">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="29c35-1970">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="29c35-1970">Add prompting for missing template parameters.</span></span> <span data-ttu-id="29c35-1971">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="29c35-1971">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="29c35-1972">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="29c35-1972">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="29c35-1973">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="29c35-1973">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="29c35-1974">ACS</span><span class="sxs-lookup"><span data-stu-id="29c35-1974">ACS</span></span>

* <span data-ttu-id="29c35-1975">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="29c35-1975">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="29c35-1976">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="29c35-1976">Add support for ssh key password prompting.</span></span> <span data-ttu-id="29c35-1977">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="29c35-1977">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="29c35-1978">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="29c35-1978">Add support for windows clusters.</span></span> <span data-ttu-id="29c35-1979">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="29c35-1979">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="29c35-1980">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="29c35-1980">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="29c35-1981">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="29c35-1981">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="29c35-1982">AppService</span><span class="sxs-lookup"><span data-stu-id="29c35-1982">AppService</span></span>

* <span data-ttu-id="29c35-1983">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="29c35-1983">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="29c35-1984">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="29c35-1984">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="29c35-1985">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="29c35-1985">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="29c35-1986">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="29c35-1986">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="29c35-1987">DataLake</span><span class="sxs-lookup"><span data-stu-id="29c35-1987">DataLake</span></span>

* <span data-ttu-id="29c35-1988">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="29c35-1988">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="29c35-1989">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="29c35-1989">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="29c35-1990">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="29c35-1990">DocuemntDB</span></span>

* <span data-ttu-id="29c35-1991">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="29c35-1991">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="29c35-1992">VM</span><span class="sxs-lookup"><span data-stu-id="29c35-1992">VM</span></span>

* <span data-ttu-id="29c35-1993">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="29c35-1993">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="29c35-1994">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="29c35-1994">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="29c35-1995">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="29c35-1995">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="29c35-1996">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="29c35-1996">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="29c35-1997">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="29c35-1997">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="29c35-1998">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="29c35-1998">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="29c35-1999">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="29c35-1999">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="29c35-2000">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="29c35-2000">February 27, 2017</span></span>

<span data-ttu-id="29c35-2001">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="29c35-2001">Version 2.0.0</span></span>

<span data-ttu-id="29c35-2002">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="29c35-2002">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="29c35-2003">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="29c35-2003">Container Service (acs)</span></span>
- <span data-ttu-id="29c35-2004">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="29c35-2004">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="29c35-2005">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="29c35-2005">Networking</span></span>
- <span data-ttu-id="29c35-2006">Storage</span><span class="sxs-lookup"><span data-stu-id="29c35-2006">Storage</span></span>

<span data-ttu-id="29c35-2007">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="29c35-2007">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="29c35-2008">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="29c35-2008">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="29c35-2009">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="29c35-2009">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="29c35-2010">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="29c35-2010">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="29c35-2011">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="29c35-2011">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="29c35-2012">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="29c35-2012">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="29c35-2013">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="29c35-2013">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="29c35-2014">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="29c35-2014">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="29c35-2015">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="29c35-2015">Provide feedback from the command line with the `az feedback` command</span></span>

