---
title: "Azure CLI 2.0 リリース ノート"
description: "Azure CLI 2.0 の最新情報について説明します"
keywords: "Azure CLI 2.0, リリース ノート"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/17/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 86babea3030ea932de1858a391014e5d0bba7f73
ms.sourcegitcommit: cae66f994cb7b7f829f75ac528093fdb6851f64e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2018
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="8790a-104">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="8790a-104">Azure CLI 2.0 release notes</span></span>

## <a name="january-17-2018"></a><span data-ttu-id="8790a-105">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="8790a-105">January 17, 2018</span></span>

<span data-ttu-id="8790a-106">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="8790a-106">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="8790a-107">ACR</span><span class="sxs-lookup"><span data-stu-id="8790a-107">ACR</span></span>

* <span data-ttu-id="8790a-108">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-108">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="8790a-109">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="8790a-109">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="8790a-110">ACS</span><span class="sxs-lookup"><span data-stu-id="8790a-110">ACS</span></span>

* <span data-ttu-id="8790a-111">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-111">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="8790a-112">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="8790a-112">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="8790a-113">Appservice</span><span class="sxs-lookup"><span data-stu-id="8790a-113">Appservice</span></span>

* <span data-ttu-id="8790a-114">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-114">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="8790a-115">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-115">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="8790a-116">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-116">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="8790a-117">Backup</span><span class="sxs-lookup"><span data-stu-id="8790a-117">Backup</span></span>

* <span data-ttu-id="8790a-118">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-118">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="8790a-119">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-119">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="8790a-120">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-120">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="8790a-121">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-121">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="8790a-122">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-122">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="8790a-123">Batch</span><span class="sxs-lookup"><span data-stu-id="8790a-123">Batch</span></span>

* <span data-ttu-id="8790a-124">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-124">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="8790a-125">クラウド</span><span class="sxs-lookup"><span data-stu-id="8790a-125">Cloud</span></span>

* <span data-ttu-id="8790a-126">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-126">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="8790a-127">消費</span><span class="sxs-lookup"><span data-stu-id="8790a-127">Consumption</span></span>

* <span data-ttu-id="8790a-128">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-128">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="8790a-129">Event Grid</span><span class="sxs-lookup"><span data-stu-id="8790a-129">Event Grid</span></span>

* <span data-ttu-id="8790a-130">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="8790a-130">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="8790a-131">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="8790a-131">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="8790a-132">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="8790a-132">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="8790a-133">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="8790a-133">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="8790a-134">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-134">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="8790a-135">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-135">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="8790a-136">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-136">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="8790a-137">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-137">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="8790a-138">対話</span><span class="sxs-lookup"><span data-stu-id="8790a-138">Interactive</span></span>

* <span data-ttu-id="8790a-139">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="8790a-139">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="8790a-140">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-140">Fixed errors on startup</span></span>
* <span data-ttu-id="8790a-141">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-141">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="8790a-142">IoT</span><span class="sxs-lookup"><span data-stu-id="8790a-142">IoT</span></span>

* <span data-ttu-id="8790a-143">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-143">Added support for device provisioning service</span></span>
* <span data-ttu-id="8790a-144">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-144">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="8790a-145">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-145">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="8790a-146">監視</span><span class="sxs-lookup"><span data-stu-id="8790a-146">Monitor</span></span>

* <span data-ttu-id="8790a-147">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-147">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="8790a-148">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="8790a-148">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="8790a-149">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-149">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span> 

### <a name="network"></a><span data-ttu-id="8790a-150">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8790a-150">Network</span></span>

* <span data-ttu-id="8790a-151">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-151">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="8790a-152">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-152">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="8790a-153">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8790a-153">Profile</span></span>

* <span data-ttu-id="8790a-154">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-154">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="8790a-155">役割</span><span class="sxs-lookup"><span data-stu-id="8790a-155">Role</span></span>

* <span data-ttu-id="8790a-156">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-156">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="8790a-157">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8790a-157">Service Fabric</span></span>

* <span data-ttu-id="8790a-158">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-158">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="8790a-159">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-159">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="8790a-160">VM</span><span class="sxs-lookup"><span data-stu-id="8790a-160">VM</span></span>

* <span data-ttu-id="8790a-161">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="8790a-161">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="8790a-162">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-162">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="8790a-163">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-163">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="8790a-164">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-164">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="8790a-165">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-165">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="8790a-166">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-166">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="8790a-167">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-167">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="8790a-168">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-168">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="8790a-169">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="8790a-169">December 19, 2017</span></span>

<span data-ttu-id="8790a-170">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="8790a-170">Version 2.0.23</span></span>

* <span data-ttu-id="8790a-171">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-171">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="8790a-172">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8790a-172">Container</span></span>

* <span data-ttu-id="8790a-173">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-173">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="8790a-174">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8790a-174">Network</span></span>

* <span data-ttu-id="8790a-175">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-175">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="8790a-176">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-176">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="8790a-177">ストレージ</span><span class="sxs-lookup"><span data-stu-id="8790a-177">Storage</span></span>

* <span data-ttu-id="8790a-178">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-178">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="8790a-179">VM</span><span class="sxs-lookup"><span data-stu-id="8790a-179">VM</span></span>

* <span data-ttu-id="8790a-180">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-180">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="8790a-181">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="8790a-181">December 5, 2017</span></span>

<span data-ttu-id="8790a-182">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="8790a-182">Version 2.0.22</span></span>

* <span data-ttu-id="8790a-183">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-183">Removed `az component` commands.</span></span> <span data-ttu-id="8790a-184">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="8790a-184">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="8790a-185">コア</span><span class="sxs-lookup"><span data-stu-id="8790a-185">Core</span></span>
* <span data-ttu-id="8790a-186">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-186">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="8790a-187">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-187">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="8790a-188">ACS</span><span class="sxs-lookup"><span data-stu-id="8790a-188">ACS</span></span>

* <span data-ttu-id="8790a-189">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-189">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="8790a-190">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="8790a-190">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="8790a-191">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-191">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="8790a-192">Advisor</span><span class="sxs-lookup"><span data-stu-id="8790a-192">Advisor</span></span>

* <span data-ttu-id="8790a-193">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8790a-193">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="8790a-194">Appservice</span><span class="sxs-lookup"><span data-stu-id="8790a-194">Appservice</span></span>

* <span data-ttu-id="8790a-195">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-195">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="8790a-196">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-196">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="8790a-197">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-197">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="8790a-198">消費</span><span class="sxs-lookup"><span data-stu-id="8790a-198">Consumption</span></span>

* <span data-ttu-id="8790a-199">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-199">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="8790a-200">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8790a-200">Container</span></span>

* <span data-ttu-id="8790a-201">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-201">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="8790a-202">監視</span><span class="sxs-lookup"><span data-stu-id="8790a-202">Monitor</span></span>

* <span data-ttu-id="8790a-203">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-203">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="8790a-204">リソース</span><span class="sxs-lookup"><span data-stu-id="8790a-204">Resource</span></span>

* <span data-ttu-id="8790a-205">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-205">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="8790a-206">役割</span><span class="sxs-lookup"><span data-stu-id="8790a-206">Role</span></span>

* <span data-ttu-id="8790a-207">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-207">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="8790a-208">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="8790a-208">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="8790a-209">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="8790a-209">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="8790a-210">SQL</span><span class="sxs-lookup"><span data-stu-id="8790a-210">SQL</span></span>

* <span data-ttu-id="8790a-211">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-211">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="8790a-212">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-212">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="8790a-213">VM</span><span class="sxs-lookup"><span data-stu-id="8790a-213">VM</span></span>

* <span data-ttu-id="8790a-214">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-214">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="8790a-215">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="8790a-215">November 14, 2017</span></span>

<span data-ttu-id="8790a-216">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="8790a-216">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="8790a-217">ACR</span><span class="sxs-lookup"><span data-stu-id="8790a-217">ACR</span></span>

* <span data-ttu-id="8790a-218">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-218">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="8790a-219">ACS</span><span class="sxs-lookup"><span data-stu-id="8790a-219">ACS</span></span>

* <span data-ttu-id="8790a-220">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-220">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="8790a-221">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8790a-221">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="8790a-222">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-222">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="8790a-223">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-223">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="8790a-224">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-224">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="8790a-225">Appservice</span><span class="sxs-lookup"><span data-stu-id="8790a-225">Appservice</span></span>

* <span data-ttu-id="8790a-226">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-226">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="8790a-227">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-227">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="8790a-228">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="8790a-228">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="8790a-229">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="8790a-229">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="8790a-230">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-230">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="8790a-231">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="8790a-231">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="8790a-232">Batch</span><span class="sxs-lookup"><span data-stu-id="8790a-232">Batch</span></span>

* <span data-ttu-id="8790a-233">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-233">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="8790a-234">Batchai</span><span class="sxs-lookup"><span data-stu-id="8790a-234">Batchai</span></span>

* <span data-ttu-id="8790a-235">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-235">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="8790a-236">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-236">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="8790a-237">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-237">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="8790a-238">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-238">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="8790a-239">クラウド</span><span class="sxs-lookup"><span data-stu-id="8790a-239">Cloud</span></span>

* <span data-ttu-id="8790a-240">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-240">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="8790a-241">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8790a-241">Container</span></span>

* <span data-ttu-id="8790a-242">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-242">Added support to open multiple ports</span></span>
* <span data-ttu-id="8790a-243">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-243">Added container group restart policy</span></span>
* <span data-ttu-id="8790a-244">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-244">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="8790a-245">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="8790a-245">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="8790a-246">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="8790a-246">Data Lake Analytics</span></span>

* <span data-ttu-id="8790a-247">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-247">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="8790a-248">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8790a-248">Data Lake Store</span></span>

* <span data-ttu-id="8790a-249">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-249">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="8790a-250">内線番号</span><span class="sxs-lookup"><span data-stu-id="8790a-250">Extension</span></span>

* <span data-ttu-id="8790a-251">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-251">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="8790a-252">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-252">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="8790a-253">IoT</span><span class="sxs-lookup"><span data-stu-id="8790a-253">IoT</span></span>

* <span data-ttu-id="8790a-254">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-254">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="8790a-255">監視</span><span class="sxs-lookup"><span data-stu-id="8790a-255">Monitor</span></span>

* <span data-ttu-id="8790a-256">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-256">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="8790a-257">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8790a-257">Network</span></span>

* <span data-ttu-id="8790a-258">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-258">Added support for CAA DNS records</span></span>
* <span data-ttu-id="8790a-259">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-259">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="8790a-260">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-260">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="8790a-261">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-261">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="8790a-262">Reservations</span><span class="sxs-lookup"><span data-stu-id="8790a-262">Reservations</span></span>

* <span data-ttu-id="8790a-263">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="8790a-263">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="8790a-264">リソース</span><span class="sxs-lookup"><span data-stu-id="8790a-264">Resource</span></span>

* <span data-ttu-id="8790a-265">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-265">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="8790a-266">SQL</span><span class="sxs-lookup"><span data-stu-id="8790a-266">SQL</span></span>

* <span data-ttu-id="8790a-267">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-267">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="8790a-268">ストレージ</span><span class="sxs-lookup"><span data-stu-id="8790a-268">Storage</span></span>

* <span data-ttu-id="8790a-269">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-269">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="8790a-270">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-270">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="8790a-271">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-271">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="8790a-272">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-272">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="8790a-273">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-273">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="8790a-274">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-274">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="8790a-275">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-275">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="8790a-276">VM</span><span class="sxs-lookup"><span data-stu-id="8790a-276">VM</span></span>

* <span data-ttu-id="8790a-277">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-277">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="8790a-278">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-278">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="8790a-279">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-279">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="8790a-280">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-280">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="8790a-281">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-281">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="8790a-282">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="8790a-282">October 24, 2017</span></span>

<span data-ttu-id="8790a-283">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="8790a-283">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="8790a-284">コア</span><span class="sxs-lookup"><span data-stu-id="8790a-284">Core</span></span>

* <span data-ttu-id="8790a-285">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="8790a-285">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="8790a-286">ACR</span><span class="sxs-lookup"><span data-stu-id="8790a-286">ACR</span></span>

* <span data-ttu-id="8790a-287">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="8790a-287">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="8790a-288">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-288">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="8790a-289">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-289">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="8790a-290">ACS</span><span class="sxs-lookup"><span data-stu-id="8790a-290">ACS</span></span>

* <span data-ttu-id="8790a-291">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-291">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="8790a-292">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-292">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="8790a-293">Appservice</span><span class="sxs-lookup"><span data-stu-id="8790a-293">Appservice</span></span>

* <span data-ttu-id="8790a-294">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-294">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="8790a-295">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8790a-295">Component</span></span>

* <span data-ttu-id="8790a-296">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-296">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="8790a-297">監視</span><span class="sxs-lookup"><span data-stu-id="8790a-297">Monitor</span></span>

* <span data-ttu-id="8790a-298">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-298">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="8790a-299">リソース</span><span class="sxs-lookup"><span data-stu-id="8790a-299">Resource</span></span>

* <span data-ttu-id="8790a-300">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-300">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="8790a-301">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-301">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="8790a-302">VM</span><span class="sxs-lookup"><span data-stu-id="8790a-302">VM</span></span>

* <span data-ttu-id="8790a-303">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-303">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="8790a-304">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="8790a-304">October 9, 2017</span></span>

<span data-ttu-id="8790a-305">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="8790a-305">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="8790a-306">コア</span><span class="sxs-lookup"><span data-stu-id="8790a-306">Core</span></span>

* <span data-ttu-id="8790a-307">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-307">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="8790a-308">Appservice</span><span class="sxs-lookup"><span data-stu-id="8790a-308">Appservice</span></span>

* <span data-ttu-id="8790a-309">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-309">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="8790a-310">Batch</span><span class="sxs-lookup"><span data-stu-id="8790a-310">Batch</span></span>

* <span data-ttu-id="8790a-311">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="8790a-311">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="8790a-312">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="8790a-312">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="8790a-313">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-313">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="8790a-314">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="8790a-314">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="8790a-315">Batchai</span><span class="sxs-lookup"><span data-stu-id="8790a-315">Batchai</span></span>

* <span data-ttu-id="8790a-316">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8790a-316">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="8790a-317">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8790a-317">Keyvault</span></span>

* <span data-ttu-id="8790a-318">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-318">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="8790a-319">(#4448)</span><span class="sxs-lookup"><span data-stu-id="8790a-319">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="8790a-320">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8790a-320">Network</span></span>

* <span data-ttu-id="8790a-321">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-321">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="8790a-322">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="8790a-322">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="8790a-323">リソース</span><span class="sxs-lookup"><span data-stu-id="8790a-323">Resource</span></span>

* <span data-ttu-id="8790a-324">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-324">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="8790a-325">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-325">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="8790a-326">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-326">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="8790a-327">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-327">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="8790a-328">SQL</span><span class="sxs-lookup"><span data-stu-id="8790a-328">Sql</span></span>

* <span data-ttu-id="8790a-329">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-329">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="8790a-330">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="8790a-330">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="8790a-331">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="8790a-331">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="8790a-332">ストレージ</span><span class="sxs-lookup"><span data-stu-id="8790a-332">Storage</span></span>

* <span data-ttu-id="8790a-333">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-333">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="8790a-334">VM</span><span class="sxs-lookup"><span data-stu-id="8790a-334">Vm</span></span>

* <span data-ttu-id="8790a-335">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-335">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="8790a-336">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-336">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="8790a-337">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-337">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="8790a-338">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-338">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="8790a-339">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-339">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="8790a-340">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="8790a-340">September 22, 2017</span></span>

<span data-ttu-id="8790a-341">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="8790a-341">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="8790a-342">リソース</span><span class="sxs-lookup"><span data-stu-id="8790a-342">Resource</span></span>

* <span data-ttu-id="8790a-343">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-343">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="8790a-344">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-344">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="8790a-345">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-345">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="8790a-346">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-346">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="8790a-347">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8790a-347">Network</span></span>

* <span data-ttu-id="8790a-348">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-348">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="8790a-349">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-349">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="8790a-350">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-350">Added `asg` application security group commands</span></span>
* <span data-ttu-id="8790a-351">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-351">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="8790a-352">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-352">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="8790a-353">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-353">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="8790a-354">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-354">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="8790a-355">ストレージ</span><span class="sxs-lookup"><span data-stu-id="8790a-355">Storage</span></span>

* <span data-ttu-id="8790a-356">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-356">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="8790a-357">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="8790a-357">Eventgrid</span></span>

* <span data-ttu-id="8790a-358">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="8790a-358">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="8790a-359">SQL</span><span class="sxs-lookup"><span data-stu-id="8790a-359">SQL</span></span>

* <span data-ttu-id="8790a-360">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-360">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="8790a-361">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="8790a-361">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="8790a-362">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-362">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="8790a-363">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8790a-363">Keyvault</span></span>

* <span data-ttu-id="8790a-364">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-364">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="8790a-365">VM</span><span class="sxs-lookup"><span data-stu-id="8790a-365">VM</span></span>

* <span data-ttu-id="8790a-366">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-366">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="8790a-367">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-367">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="8790a-368">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-368">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="8790a-369">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-369">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="8790a-370">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-370">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="8790a-371">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-371">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="8790a-372">ACS</span><span class="sxs-lookup"><span data-stu-id="8790a-372">ACS</span></span>

* <span data-ttu-id="8790a-373">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-373">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="8790a-374">Appservice</span><span class="sxs-lookup"><span data-stu-id="8790a-374">Appservice</span></span>

* <span data-ttu-id="8790a-375">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-375">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="8790a-376">Backup</span><span class="sxs-lookup"><span data-stu-id="8790a-376">Backup</span></span>

* <span data-ttu-id="8790a-377">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="8790a-377">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="8790a-378">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="8790a-378">September 11, 2017</span></span>

<span data-ttu-id="8790a-379">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="8790a-379">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="8790a-380">コア</span><span class="sxs-lookup"><span data-stu-id="8790a-380">Core</span></span>

* <span data-ttu-id="8790a-381">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="8790a-381">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="8790a-382">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-382">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="8790a-383">ACS</span><span class="sxs-lookup"><span data-stu-id="8790a-383">Acs</span></span>

* <span data-ttu-id="8790a-384">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-384">Added `acs list-locations` command</span></span>
* <span data-ttu-id="8790a-385">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="8790a-385">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="8790a-386">Appservice</span><span class="sxs-lookup"><span data-stu-id="8790a-386">Appservice</span></span>

* <span data-ttu-id="8790a-387">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-387">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="8790a-388">CDN</span><span class="sxs-lookup"><span data-stu-id="8790a-388">CDN</span></span>

* <span data-ttu-id="8790a-389">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-389">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="8790a-390">内線番号</span><span class="sxs-lookup"><span data-stu-id="8790a-390">Extension</span></span>

* <span data-ttu-id="8790a-391">最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="8790a-391">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="8790a-392">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8790a-392">Keyvault</span></span>

* <span data-ttu-id="8790a-393">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-393">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="8790a-394">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8790a-394">Network</span></span>

* <span data-ttu-id="8790a-395">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-395">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="8790a-396">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-396">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="8790a-397">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-397">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="8790a-398">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-398">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="8790a-399">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-399">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="8790a-400">リソース</span><span class="sxs-lookup"><span data-stu-id="8790a-400">Resource</span></span>

* <span data-ttu-id="8790a-401">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="8790a-401">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="8790a-402">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="8790a-402">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="8790a-403">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="8790a-403">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="8790a-404">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="8790a-404">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="8790a-405">SQL</span><span class="sxs-lookup"><span data-stu-id="8790a-405">SQL</span></span>

* <span data-ttu-id="8790a-406">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-406">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="8790a-407">VM</span><span class="sxs-lookup"><span data-stu-id="8790a-407">VM</span></span>

* <span data-ttu-id="8790a-408">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="8790a-408">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="8790a-409">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="8790a-409">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="8790a-410">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8790a-410">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="8790a-411">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="8790a-411">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="8790a-412">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="8790a-412">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="8790a-413">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="8790a-413">August 31, 2017</span></span>

<span data-ttu-id="8790a-414">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="8790a-414">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="8790a-415">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8790a-415">Keyvault</span></span>

* <span data-ttu-id="8790a-416">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-416">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="8790a-417">SF</span><span class="sxs-lookup"><span data-stu-id="8790a-417">Sf</span></span>

* <span data-ttu-id="8790a-418">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="8790a-418">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="8790a-419">ストレージ</span><span class="sxs-lookup"><span data-stu-id="8790a-419">Storage</span></span>

* <span data-ttu-id="8790a-420">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-420">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="8790a-421">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="8790a-421">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="8790a-422">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="8790a-422">August 28, 2017</span></span>

<span data-ttu-id="8790a-423">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="8790a-423">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="8790a-424">CLI</span><span class="sxs-lookup"><span data-stu-id="8790a-424">CLI</span></span>

* <span data-ttu-id="8790a-425">`--version` に法的事項を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-425">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="8790a-426">ACS</span><span class="sxs-lookup"><span data-stu-id="8790a-426">ACS</span></span>

* <span data-ttu-id="8790a-427">プレビュー リージョンを修正しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-427">Corrected preview regions.</span></span>
* <span data-ttu-id="8790a-428">既定の `dns_name_prefix` を正しい形式にしました。</span><span class="sxs-lookup"><span data-stu-id="8790a-428">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="8790a-429">ACS コマンド出力を最適化しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-429">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="8790a-430">Appservice</span><span class="sxs-lookup"><span data-stu-id="8790a-430">Appservice</span></span>

* <span data-ttu-id="8790a-431">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-431">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="8790a-432">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-432">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="8790a-433">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="8790a-433">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="8790a-434">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="8790a-434">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="8790a-435">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="8790a-435">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="8790a-436">IoT</span><span class="sxs-lookup"><span data-stu-id="8790a-436">IoT</span></span>

* <span data-ttu-id="8790a-437">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="8790a-437">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="8790a-438">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8790a-438">Network</span></span>

* <span data-ttu-id="8790a-439">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-439">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="8790a-440">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-440">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="8790a-441">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-441">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="8790a-442">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-442">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="8790a-443">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-443">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="8790a-444">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8790a-444">Profile</span></span>

* <span data-ttu-id="8790a-445">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="8790a-445">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="8790a-446">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8790a-446">Service Fabric</span></span>

* <span data-ttu-id="8790a-447">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="8790a-447">Preview release</span></span>
* <span data-ttu-id="8790a-448">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="8790a-448">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="8790a-449">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-449">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="8790a-450">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-450">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="8790a-451">ストレージ</span><span class="sxs-lookup"><span data-stu-id="8790a-451">Storage</span></span>

* <span data-ttu-id="8790a-452">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8790a-452">Enabled setting blob tier</span></span>
* <span data-ttu-id="8790a-453">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-453">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="8790a-454">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-454">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="8790a-455">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8790a-455">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="8790a-456">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-456">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="8790a-457">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="8790a-457">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="8790a-458">VM</span><span class="sxs-lookup"><span data-stu-id="8790a-458">VM</span></span>

* <span data-ttu-id="8790a-459">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-459">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="8790a-460">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-460">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="8790a-461">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="8790a-461">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="8790a-462">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-462">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="8790a-463">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-463">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="8790a-464">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-464">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="8790a-465">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="8790a-465">August 15, 2017</span></span>

<span data-ttu-id="8790a-466">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="8790a-466">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="8790a-467">ACS</span><span class="sxs-lookup"><span data-stu-id="8790a-467">ACS</span></span>

* <span data-ttu-id="8790a-468">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-468">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="8790a-469">Appservice</span><span class="sxs-lookup"><span data-stu-id="8790a-469">Appservice</span></span>

* <span data-ttu-id="8790a-470">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-470">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="8790a-471">Event Grid</span><span class="sxs-lookup"><span data-stu-id="8790a-471">Event Grid</span></span>

* <span data-ttu-id="8790a-472">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-472">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="8790a-473">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="8790a-473">August 11, 2017</span></span>

<span data-ttu-id="8790a-474">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="8790a-474">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="8790a-475">ACS</span><span class="sxs-lookup"><span data-stu-id="8790a-475">ACS</span></span>

* <span data-ttu-id="8790a-476">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-476">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="8790a-477">Batch</span><span class="sxs-lookup"><span data-stu-id="8790a-477">Batch</span></span>

* <span data-ttu-id="8790a-478">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="8790a-478">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="8790a-479">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-479">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="8790a-480">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-480">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="8790a-481">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="8790a-481">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="8790a-482">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-482">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="8790a-483">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-483">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="8790a-484">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8790a-484">Component</span></span>

* <span data-ttu-id="8790a-485">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-485">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="8790a-486">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8790a-486">Container</span></span>

* <span data-ttu-id="8790a-487">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-487">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="8790a-488">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8790a-488">Data Lake Store</span></span>

* <span data-ttu-id="8790a-489">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="8790a-489">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="8790a-490">Event Grid</span><span class="sxs-lookup"><span data-stu-id="8790a-490">Event Grid</span></span>

* <span data-ttu-id="8790a-491">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8790a-491">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="8790a-492">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8790a-492">Network</span></span>

* <span data-ttu-id="8790a-493">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-493">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="8790a-494">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-494">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="8790a-495">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-495">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="8790a-496">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-496">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="8790a-497">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8790a-497">Profile</span></span>

* <span data-ttu-id="8790a-498">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-498">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="8790a-499">ストレージ</span><span class="sxs-lookup"><span data-stu-id="8790a-499">Storage</span></span>

* <span data-ttu-id="8790a-500">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="8790a-500">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="8790a-501">VM</span><span class="sxs-lookup"><span data-stu-id="8790a-501">VM</span></span>

* <span data-ttu-id="8790a-502">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="8790a-502">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="8790a-503">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="8790a-503">Exposed `list-skus` command</span></span>
* <span data-ttu-id="8790a-504">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-504">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="8790a-505">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="8790a-505">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="8790a-506">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="8790a-506">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="8790a-507">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="8790a-507">July 28, 2017</span></span>

<span data-ttu-id="8790a-508">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="8790a-508">Version 2.0.12</span></span>

* <span data-ttu-id="8790a-509">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-509">Added container commands</span></span>
* <span data-ttu-id="8790a-510">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-510">Added billing and consumption modules</span></span>

```
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

### <a name="core"></a><span data-ttu-id="8790a-511">コア</span><span class="sxs-lookup"><span data-stu-id="8790a-511">Core</span></span>

* <span data-ttu-id="8790a-512">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="8790a-512">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="8790a-513">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-513">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="8790a-514">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="8790a-514">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="8790a-515">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="8790a-515">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="8790a-516">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="8790a-516">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="8790a-517">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="8790a-517">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="8790a-518">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="8790a-518">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="8790a-519">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="8790a-519">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="8790a-520">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="8790a-520">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="8790a-521">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="8790a-521">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="8790a-522">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="8790a-522">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="8790a-523">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="8790a-523">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="8790a-524">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="8790a-524">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="8790a-525">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="8790a-525">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="8790a-526">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-526">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="8790a-527">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="8790a-527">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="8790a-528">ACR</span><span class="sxs-lookup"><span data-stu-id="8790a-528">ACR</span></span>

* <span data-ttu-id="8790a-529">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-529">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="8790a-530">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-530">Support SKU update for managed registries</span></span>
* <span data-ttu-id="8790a-531">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-531">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="8790a-532">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-532">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="8790a-533">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-533">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="8790a-534">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-534">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="8790a-535">ACS</span><span class="sxs-lookup"><span data-stu-id="8790a-535">ACS</span></span>

* <span data-ttu-id="8790a-536">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-536">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="8790a-537">Appservice</span><span class="sxs-lookup"><span data-stu-id="8790a-537">Appservice</span></span>

* <span data-ttu-id="8790a-538">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-538">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="8790a-539">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-539">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="8790a-540">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="8790a-540">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="8790a-541">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="8790a-541">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="8790a-542">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="8790a-542">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="8790a-543">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="8790a-543">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="8790a-544">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="8790a-544">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="8790a-545">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="8790a-545">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="8790a-546">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-546">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="8790a-547">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="8790a-547">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="8790a-548">Batch</span><span class="sxs-lookup"><span data-stu-id="8790a-548">Batch</span></span>

* <span data-ttu-id="8790a-549">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="8790a-549">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="8790a-550">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-550">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="8790a-551">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-551">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="8790a-552">CDN</span><span class="sxs-lookup"><span data-stu-id="8790a-552">CDN</span></span>

* <span data-ttu-id="8790a-553">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-553">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="8790a-554">クラウド</span><span class="sxs-lookup"><span data-stu-id="8790a-554">Cloud</span></span>

* <span data-ttu-id="8790a-555">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-555">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="8790a-556">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="8790a-556">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="8790a-557">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-557">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="8790a-558">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="8790a-558">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="8790a-559">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="8790a-559">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8790a-560">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8790a-560">CosmosDB</span></span>

* <span data-ttu-id="8790a-561">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-561">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="8790a-562">既定のコレクション TTL のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-562">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="8790a-563">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="8790a-563">Data Lake Analytics</span></span>

* <span data-ttu-id="8790a-564">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-564">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="8790a-565">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-565">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="8790a-566">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-566">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="8790a-567">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8790a-567">Data Lake Store</span></span>

* <span data-ttu-id="8790a-568">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-568">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="8790a-569">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="8790a-569">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="8790a-570">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-570">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="8790a-571">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="8790a-571">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="8790a-572">対話</span><span class="sxs-lookup"><span data-stu-id="8790a-572">Interactive</span></span>

* <span data-ttu-id="8790a-573">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="8790a-573">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="8790a-574">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="8790a-574">Increased test coverage</span></span>
* <span data-ttu-id="8790a-575">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="8790a-575">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="8790a-576">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="8790a-576">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="8790a-577">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="8790a-577">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="8790a-578">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="8790a-578">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="8790a-579">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="8790a-579">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="8790a-580">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-580">Added `--progress` flag</span></span>
* <span data-ttu-id="8790a-581">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8790a-581">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="8790a-582">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="8790a-582">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="8790a-583">IoT</span><span class="sxs-lookup"><span data-stu-id="8790a-583">IoT</span></span>

* <span data-ttu-id="8790a-584">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-584">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="8790a-585">(#3934)</span><span class="sxs-lookup"><span data-stu-id="8790a-585">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="8790a-586">Key Vault</span><span class="sxs-lookup"><span data-stu-id="8790a-586">Key vault</span></span>

* <span data-ttu-id="8790a-587">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-587">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="8790a-588">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8790a-588">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="8790a-589">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8790a-589">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="8790a-590">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8790a-590">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="8790a-591">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8790a-591">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="8790a-592">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="8790a-592">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="8790a-593">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-593">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="8790a-594">(#3307)</span><span class="sxs-lookup"><span data-stu-id="8790a-594">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="8790a-595">ラボ</span><span class="sxs-lookup"><span data-stu-id="8790a-595">Lab</span></span>

* <span data-ttu-id="8790a-596">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-596">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="8790a-597">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-597">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="8790a-598">監視</span><span class="sxs-lookup"><span data-stu-id="8790a-598">Monitor</span></span>

* <span data-ttu-id="8790a-599">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="8790a-599">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="8790a-600">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-600">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="8790a-601">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-601">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="8790a-602">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-602">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="8790a-603">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8790a-603">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="8790a-604">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-604">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="8790a-605">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="8790a-605">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="8790a-606">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="8790a-606">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="8790a-607">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="8790a-607">`location` no longer required</span></span>
  * <span data-ttu-id="8790a-608">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="8790a-608">Add name and ID support for target</span></span>
  * <span data-ttu-id="8790a-609">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="8790a-609">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="8790a-610">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="8790a-610">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="8790a-611">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="8790a-611">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="8790a-612">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="8790a-612">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="8790a-613">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-613">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="8790a-614">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-614">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="8790a-615">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8790a-615">Network</span></span>

* <span data-ttu-id="8790a-616">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-616">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="8790a-617">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-617">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="8790a-618">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-618">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="8790a-619">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-619">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="8790a-620">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-620">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="8790a-621">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-621">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="8790a-622">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-622">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="8790a-623">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-623">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="8790a-624">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-624">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="8790a-625">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-625">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="8790a-626">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-626">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="8790a-627">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-627">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="8790a-628">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-628">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="8790a-629">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-629">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="8790a-630">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-630">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="8790a-631">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="8790a-631">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="8790a-632">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-632">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="8790a-633">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-633">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="8790a-634">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-634">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="8790a-635">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-635">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="8790a-636">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-636">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="8790a-637">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-637">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="8790a-638">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="8790a-638">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="8790a-639">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="8790a-639">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="8790a-640">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="8790a-640">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="8790a-641">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="8790a-641">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="8790a-642">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="8790a-642">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="8790a-643">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8790a-643">Profile</span></span>

* <span data-ttu-id="8790a-644">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-644">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="8790a-645">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-645">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="8790a-646">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="8790a-646">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="8790a-647">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-647">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="8790a-648">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-648">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="8790a-649">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8790a-649">RDBMS</span></span>

* <span data-ttu-id="8790a-650">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="8790a-650">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="8790a-651">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="8790a-651">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="8790a-652">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="8790a-652">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="8790a-653">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="8790a-653">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="8790a-654">リソース</span><span class="sxs-lookup"><span data-stu-id="8790a-654">Resource</span></span>

* <span data-ttu-id="8790a-655">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="8790a-655">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="8790a-656">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="8790a-656">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="8790a-657">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-657">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="8790a-658">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-658">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="8790a-659">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="8790a-659">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="8790a-660">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-660">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="8790a-661">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="8790a-661">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="8790a-662">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-662">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="8790a-663">役割</span><span class="sxs-lookup"><span data-stu-id="8790a-663">Role</span></span>

* <span data-ttu-id="8790a-664">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-664">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="8790a-665">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="8790a-665">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="8790a-666">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="8790a-666">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="8790a-667">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="8790a-667">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="8790a-668">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-668">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="8790a-669">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8790a-669">Service Fabric</span></span>
* <span data-ttu-id="8790a-670">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="8790a-670">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="8790a-671">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="8790a-671">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="8790a-672">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="8790a-672">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="8790a-673">SQL</span><span class="sxs-lookup"><span data-stu-id="8790a-673">SQL</span></span>

* <span data-ttu-id="8790a-674">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="8790a-674">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="8790a-675">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="8790a-675">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="8790a-676">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8790a-676">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="8790a-677">ストレージ</span><span class="sxs-lookup"><span data-stu-id="8790a-677">Storage</span></span>

* <span data-ttu-id="8790a-678">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="8790a-678">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="8790a-679">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8790a-679">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="8790a-680">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="8790a-680">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="8790a-681">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="8790a-681">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="8790a-682">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="8790a-682">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="8790a-683">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="8790a-683">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="8790a-684">VM</span><span class="sxs-lookup"><span data-stu-id="8790a-684">VM</span></span>

* <span data-ttu-id="8790a-685">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-685">Support configuring nsg</span></span>
* <span data-ttu-id="8790a-686">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8790a-686">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="8790a-687">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="8790a-687">Support managed service identities</span></span>
* <span data-ttu-id="8790a-688">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-688">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="8790a-689">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="8790a-689">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="8790a-690">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="8790a-690">May 10, 2017</span></span>

<span data-ttu-id="8790a-691">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="8790a-691">Version 2.0.6</span></span>

* <span data-ttu-id="8790a-692">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="8790a-692">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="8790a-693">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="8790a-693">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="8790a-694">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-694">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="8790a-695">Cognitive Services モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-695">Include Cognitive Services module.</span></span>
* <span data-ttu-id="8790a-696">Service Fabric モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-696">Include Service Fabric module.</span></span>
* <span data-ttu-id="8790a-697">対話型モジュールが追加されました (az-shell の名前変更)。</span><span class="sxs-lookup"><span data-stu-id="8790a-697">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="8790a-698">CDN コマンドに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="8790a-698">Add support for CDN commands.</span></span>
* <span data-ttu-id="8790a-699">コンテナー モジュールが削除されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-699">Remove Container module.</span></span>
* <span data-ttu-id="8790a-700">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="8790a-700">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="8790a-701">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="8790a-701">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

```
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

### <a name="core"></a><span data-ttu-id="8790a-702">コア</span><span class="sxs-lookup"><span data-stu-id="8790a-702">Core</span></span>

* <span data-ttu-id="8790a-703">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="8790a-703">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="8790a-704">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="8790a-704">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="8790a-705">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="8790a-705">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="8790a-706">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="8790a-706">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="8790a-707">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="8790a-707">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="8790a-708">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="8790a-708">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="8790a-709">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="8790a-709">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="8790a-710">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="8790a-710">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="8790a-711">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="8790a-711">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="8790a-712">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="8790a-712">core: Improved performance</span></span>
* <span data-ttu-id="8790a-713">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="8790a-713">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="8790a-714">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="8790a-714">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="8790a-715">ACS</span><span class="sxs-lookup"><span data-stu-id="8790a-715">ACS</span></span>

* <span data-ttu-id="8790a-716">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="8790a-716">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="8790a-717">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="8790a-717">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="8790a-718">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="8790a-718">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="8790a-719">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="8790a-719">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="8790a-720">AppService</span><span class="sxs-lookup"><span data-stu-id="8790a-720">AppService</span></span>

* <span data-ttu-id="8790a-721">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8790a-721">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="8790a-722">Team Services (VSTS) が継続的な配信オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="8790a-722">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="8790a-723">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="8790a-723">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="8790a-724">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="8790a-724">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="8790a-725">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="8790a-725">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="8790a-726">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="8790a-726">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="8790a-727">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="8790a-727">support slot swap with preview</span></span>
* <span data-ttu-id="8790a-728">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="8790a-728">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="8790a-729">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="8790a-729">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8790a-730">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8790a-730">CosmosDB</span></span>

* <span data-ttu-id="8790a-731">documentdb モジュールから cosmosdb に名前が変更されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-731">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="8790a-732">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8790a-732">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="8790a-733">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8790a-733">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="8790a-734">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8790a-734">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="8790a-735">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="8790a-735">Data Lake Analytics</span></span>

* <span data-ttu-id="8790a-736">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-736">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="8790a-737">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="8790a-737">Add support for new catalog item type: package.</span></span> <span data-ttu-id="8790a-738">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="8790a-738">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="8790a-739">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="8790a-739">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="8790a-740">テーブル</span><span class="sxs-lookup"><span data-stu-id="8790a-740">Table</span></span>
  * <span data-ttu-id="8790a-741">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="8790a-741">Table valued function</span></span>
  * <span data-ttu-id="8790a-742">表示</span><span class="sxs-lookup"><span data-stu-id="8790a-742">View</span></span>
  * <span data-ttu-id="8790a-743">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="8790a-743">Table Statistics.</span></span> <span data-ttu-id="8790a-744">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8790a-744">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="8790a-745">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8790a-745">Data Lake Store</span></span>

* <span data-ttu-id="8790a-746">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-746">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="8790a-747">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="8790a-747">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="8790a-748">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="8790a-748">missed help for access show.</span></span> <span data-ttu-id="8790a-749">追加しました </span><span class="sxs-lookup"><span data-stu-id="8790a-749">adding it.</span></span> <span data-ttu-id="8790a-750">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="8790a-750">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="8790a-751">検索</span><span class="sxs-lookup"><span data-stu-id="8790a-751">Find</span></span>

* <span data-ttu-id="8790a-752">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="8790a-752">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="8790a-753">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8790a-753">KeyVault</span></span>

* <span data-ttu-id="8790a-754">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="8790a-754">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="8790a-755">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-755">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="8790a-756">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的に上書きされます</span><span class="sxs-lookup"><span data-stu-id="8790a-756">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="8790a-757">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-757">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="8790a-758">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="8790a-758">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="8790a-759">ラボ</span><span class="sxs-lookup"><span data-stu-id="8790a-759">Lab</span></span>

* <span data-ttu-id="8790a-760">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-760">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="8790a-761">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-761">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="8790a-762">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-762">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="8790a-763">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-763">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="8790a-764">ラボ内でシークレットを管理するためのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-764">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="8790a-765">監視</span><span class="sxs-lookup"><span data-stu-id="8790a-765">Monitor</span></span>

* <span data-ttu-id="8790a-766">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="8790a-766">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="8790a-767">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="8790a-767">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="8790a-768">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8790a-768">Network</span></span>

* <span data-ttu-id="8790a-769">`network watcher test-connectivity` コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-769">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="8790a-770">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="8790a-770">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="8790a-771">Application Gateway 接続のドレインに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="8790a-771">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="8790a-772">Application Gateway WAF 規則セットの構成に対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="8790a-772">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="8790a-773">ExpressRoute ルート フィルターとルールに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="8790a-773">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="8790a-774">TrafficManager の地理的なルーティングに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="8790a-774">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="8790a-775">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="8790a-775">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="8790a-776">VPN 接続 IPSec ポリシーに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="8790a-776">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="8790a-777">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-777">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="8790a-778">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8790a-778">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="8790a-779">`network vpn-connection list/show` コマンドの出力から null 値が削除されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-779">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="8790a-780">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="8790a-780">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="8790a-781">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-781">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="8790a-782">`dns zone import` でレコードが適切にインポートされないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-782">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="8790a-783">`traffic-manager endpoint update` が動作しないバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="8790a-783">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="8790a-784">"Network Watcher" プレビューのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-784">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="8790a-785">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8790a-785">Profile</span></span>

* <span data-ttu-id="8790a-786">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="8790a-786">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="8790a-787">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="8790a-787">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="8790a-788">Redis</span><span class="sxs-lookup"><span data-stu-id="8790a-788">Redis</span></span>

* <span data-ttu-id="8790a-789">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8790a-789">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="8790a-790">"update-settings" コマンドが廃止されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-790">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="8790a-791">リソース</span><span class="sxs-lookup"><span data-stu-id="8790a-791">Resource</span></span>

* <span data-ttu-id="8790a-792">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="8790a-792">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="8790a-793">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="8790a-793">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="8790a-794">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="8790a-794">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="8790a-795">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="8790a-795">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="8790a-796">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="8790a-796">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="8790a-797">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="8790a-797">Add docs for az lock update.</span></span> <span data-ttu-id="8790a-798">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="8790a-798">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="8790a-799">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="8790a-799">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="8790a-800">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="8790a-800">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="8790a-801">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-801">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="8790a-802">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="8790a-802">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="8790a-803">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="8790a-803">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="8790a-804">役割</span><span class="sxs-lookup"><span data-stu-id="8790a-804">Role</span></span>

* <span data-ttu-id="8790a-805">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="8790a-805">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="8790a-806">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="8790a-806">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="8790a-807">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="8790a-807">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="8790a-808">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="8790a-808">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="8790a-809">SQL</span><span class="sxs-lookup"><span data-stu-id="8790a-809">SQL</span></span>

* <span data-ttu-id="8790a-810">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="8790a-810">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="8790a-811">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="8790a-811">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="8790a-812">ストレージ</span><span class="sxs-lookup"><span data-stu-id="8790a-812">Storage</span></span>

* <span data-ttu-id="8790a-813">`storage account create` のリソース グループの場所に対する既定の場所。</span><span class="sxs-lookup"><span data-stu-id="8790a-813">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="8790a-814">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8790a-814">Add support for incremental blob copy</span></span>
* <span data-ttu-id="8790a-815">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8790a-815">Add support for large block blob upload</span></span>
* <span data-ttu-id="8790a-816">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="8790a-816">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="8790a-817">VM</span><span class="sxs-lookup"><span data-stu-id="8790a-817">VM</span></span>

* <span data-ttu-id="8790a-818">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="8790a-818">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="8790a-819">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="8790a-819">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="8790a-820">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="8790a-820">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="8790a-821">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="8790a-821">az vm/vmss disk</span></span>
  3. <span data-ttu-id="8790a-822">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="8790a-822">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="8790a-823">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="8790a-823">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="8790a-824">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="8790a-824">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="8790a-825">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="8790a-825">April 3, 2017</span></span>

<span data-ttu-id="8790a-826">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="8790a-826">Version 2.0.2</span></span>

<span data-ttu-id="8790a-827">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました。</span><span class="sxs-lookup"><span data-stu-id="8790a-827">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

```
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

### <a name="core"></a><span data-ttu-id="8790a-828">コア</span><span class="sxs-lookup"><span data-stu-id="8790a-828">Core</span></span>

* <span data-ttu-id="8790a-829">既定の一覧に acr、lab、monitor、find モジュールを追加。</span><span class="sxs-lookup"><span data-stu-id="8790a-829">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="8790a-830">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="8790a-830">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="8790a-831">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="8790a-831">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="8790a-832">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="8790a-832">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="8790a-833">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="8790a-833">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="8790a-834">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="8790a-834">Add prompting for missing template parameters.</span></span> <span data-ttu-id="8790a-835">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="8790a-835">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="8790a-836">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="8790a-836">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="8790a-837">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="8790a-837">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="8790a-838">ACS</span><span class="sxs-lookup"><span data-stu-id="8790a-838">ACS</span></span>

* <span data-ttu-id="8790a-839">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="8790a-839">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="8790a-840">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="8790a-840">Add support for ssh key password prompting.</span></span> <span data-ttu-id="8790a-841">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="8790a-841">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="8790a-842">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="8790a-842">Add support for windows clusters.</span></span> <span data-ttu-id="8790a-843">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="8790a-843">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="8790a-844">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="8790a-844">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="8790a-845">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="8790a-845">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="8790a-846">AppService</span><span class="sxs-lookup"><span data-stu-id="8790a-846">AppService</span></span>

* <span data-ttu-id="8790a-847">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="8790a-847">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="8790a-848">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="8790a-848">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="8790a-849">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="8790a-849">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="8790a-850">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="8790a-850">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="8790a-851">DataLake</span><span class="sxs-lookup"><span data-stu-id="8790a-851">DataLake</span></span>

* <span data-ttu-id="8790a-852">Data Lake Analytics モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="8790a-852">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="8790a-853">Data Lake Store モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="8790a-853">Initial release of Data Lake Store module.</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="8790a-854">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="8790a-854">DocuemntDB</span></span>

* <span data-ttu-id="8790a-855">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="8790a-855">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="8790a-856">VM</span><span class="sxs-lookup"><span data-stu-id="8790a-856">VM</span></span>

* <span data-ttu-id="8790a-857">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="8790a-857">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="8790a-858">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="8790a-858">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="8790a-859">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="8790a-859">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="8790a-860">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="8790a-860">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="8790a-861">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="8790a-861">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="8790a-862">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="8790a-862">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="8790a-863">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="8790a-863">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="8790a-864">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="8790a-864">February 27, 2017</span></span>

<span data-ttu-id="8790a-865">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="8790a-865">Version 2.0.0</span></span>

<span data-ttu-id="8790a-866">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。</span><span class="sxs-lookup"><span data-stu-id="8790a-866">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="8790a-867">一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="8790a-867">General availability applies to these command modules:</span></span>
- <span data-ttu-id="8790a-868">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="8790a-868">Container Service (acs)</span></span>
- <span data-ttu-id="8790a-869">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="8790a-869">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="8790a-870">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8790a-870">Networking</span></span>
- <span data-ttu-id="8790a-871">ストレージ</span><span class="sxs-lookup"><span data-stu-id="8790a-871">Storage</span></span>

<span data-ttu-id="8790a-872">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8790a-872">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="8790a-873">問題は、Microsoft サポートで直接開くことも、[github の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="8790a-873">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="8790a-874">[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="8790a-874">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="8790a-875">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません。</span><span class="sxs-lookup"><span data-stu-id="8790a-875">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="8790a-876">CLI のバージョンを確認するには、`az --version` を使用します。</span><span class="sxs-lookup"><span data-stu-id="8790a-876">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="8790a-877">出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="8790a-877">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

```
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
> <span data-ttu-id="8790a-878">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。</span><span class="sxs-lookup"><span data-stu-id="8790a-878">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="8790a-879">これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です。</span><span class="sxs-lookup"><span data-stu-id="8790a-879">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="8790a-880">CLI のナイトリー プレビュー ビルドもあります。</span><span class="sxs-lookup"><span data-stu-id="8790a-880">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="8790a-881">詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8790a-881">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="8790a-882">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="8790a-882">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="8790a-883">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="8790a-883">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="8790a-884">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる。</span><span class="sxs-lookup"><span data-stu-id="8790a-884">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="8790a-885">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る。</span><span class="sxs-lookup"><span data-stu-id="8790a-885">Provide feedback from the command line with the `az feedback` command.</span></span>

