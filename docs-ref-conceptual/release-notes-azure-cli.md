---
title: "Azure CLI 2.0 リリース ノート"
description: "Azure CLI 2.0 の最新情報について説明します"
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 02/27/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 01078b7a3665f563f0a6b1d809c9a41f18d136d6
ms.sourcegitcommit: f3ab5da6019083ef2482b62c7355817e6170dcfb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2018
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="0a195-103">Azure CLI 2.0 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="0a195-103">Azure CLI 2.0 release notes</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="0a195-104">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="0a195-104">February 27, 2018</span></span>

<span data-ttu-id="0a195-105">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="0a195-105">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="0a195-106">コア</span><span class="sxs-lookup"><span data-stu-id="0a195-106">Core</span></span>

* <span data-ttu-id="0a195-107">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正: Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="0a195-107">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="0a195-108">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-108">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="0a195-109">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-109">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="0a195-110">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-110">ACS</span></span>

* <span data-ttu-id="0a195-111">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-111">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="0a195-112">修正された問題: ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="0a195-112">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="0a195-113">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-113">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="0a195-114">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="0a195-114">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-115">Appservice</span><span class="sxs-lookup"><span data-stu-id="0a195-115">Appservice</span></span>

* <span data-ttu-id="0a195-116">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="0a195-116">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="0a195-117">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="0a195-117">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="0a195-118">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="0a195-118">Cognitive Services</span></span>

* <span data-ttu-id="0a195-119">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="0a195-119">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="0a195-120">消費</span><span class="sxs-lookup"><span data-stu-id="0a195-120">Consumption</span></span>

* <span data-ttu-id="0a195-121">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-121">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="0a195-122">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="0a195-122">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="0a195-123">コンテナー</span><span class="sxs-lookup"><span data-stu-id="0a195-123">Container</span></span>

* <span data-ttu-id="0a195-124">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-124">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="0a195-125">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="0a195-125">Network</span></span>

* <span data-ttu-id="0a195-126">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正: `network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="0a195-126">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="0a195-127">リソース</span><span class="sxs-lookup"><span data-stu-id="0a195-127">Resource</span></span>

* <span data-ttu-id="0a195-128">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-128">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="0a195-129">役割</span><span class="sxs-lookup"><span data-stu-id="0a195-129">Role</span></span>

* <span data-ttu-id="0a195-130">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-130">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="0a195-131">SQL</span><span class="sxs-lookup"><span data-stu-id="0a195-131">SQL</span></span>

* <span data-ttu-id="0a195-132">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-132">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="0a195-133">Storage</span><span class="sxs-lookup"><span data-stu-id="0a195-133">Storage</span></span>

* <span data-ttu-id="0a195-134">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="0a195-134">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-135">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-135">VM</span></span>

* <span data-ttu-id="0a195-136">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-136">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="0a195-137">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="0a195-137">February 13, 2018</span></span>

<span data-ttu-id="0a195-138">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="0a195-138">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="0a195-139">コア</span><span class="sxs-lookup"><span data-stu-id="0a195-139">Core</span></span>

* <span data-ttu-id="0a195-140">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-140">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="0a195-141">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-141">ACS</span></span>

* <span data-ttu-id="0a195-142">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-142">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="0a195-143">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-143">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="0a195-144">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-144">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="0a195-145">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="0a195-145">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="0a195-146">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-146">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="0a195-147">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="0a195-147">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="0a195-148">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-148">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="0a195-149">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="0a195-149">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-150">Appservice</span><span class="sxs-lookup"><span data-stu-id="0a195-150">Appservice</span></span>

* <span data-ttu-id="0a195-151">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-151">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="0a195-152">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-152">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="0a195-153">CDN</span><span class="sxs-lookup"><span data-stu-id="0a195-153">CDN</span></span>

* <span data-ttu-id="0a195-154">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-154">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="0a195-155">コンテナー</span><span class="sxs-lookup"><span data-stu-id="0a195-155">Container</span></span>

* <span data-ttu-id="0a195-156">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-156">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="0a195-157">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-157">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="0a195-158">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="0a195-158">CosmosDB</span></span>

* <span data-ttu-id="0a195-159">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-159">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="0a195-160">内線番号</span><span class="sxs-lookup"><span data-stu-id="0a195-160">Extension</span></span>

* <span data-ttu-id="0a195-161">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-161">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="0a195-162">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-162">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="0a195-163">フィードバック</span><span class="sxs-lookup"><span data-stu-id="0a195-163">Feedback</span></span>

* <span data-ttu-id="0a195-164">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-164">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="0a195-165">対話</span><span class="sxs-lookup"><span data-stu-id="0a195-165">Interactive</span></span>

* <span data-ttu-id="0a195-166">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-166">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="0a195-167">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-167">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="0a195-168">IoT</span><span class="sxs-lookup"><span data-stu-id="0a195-168">IoT</span></span>

* <span data-ttu-id="0a195-169">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-169">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success.</span></span>
* <span data-ttu-id="0a195-170">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-170">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success.</span></span>
* <span data-ttu-id="0a195-171">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-171">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="0a195-172">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-172">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="0a195-173">監視</span><span class="sxs-lookup"><span data-stu-id="0a195-173">Monitor</span></span>

* <span data-ttu-id="0a195-174">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-174">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="0a195-175">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="0a195-175">Network</span></span>

* <span data-ttu-id="0a195-176">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-176">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="0a195-177">プロファイル</span><span class="sxs-lookup"><span data-stu-id="0a195-177">Profile</span></span>

* <span data-ttu-id="0a195-178">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="0a195-178">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="0a195-179">リソース</span><span class="sxs-lookup"><span data-stu-id="0a195-179">Resource</span></span>

* <span data-ttu-id="0a195-180">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-180">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="0a195-181">役割</span><span class="sxs-lookup"><span data-stu-id="0a195-181">Role</span></span>

* <span data-ttu-id="0a195-182">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-182">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="0a195-183">SQL</span><span class="sxs-lookup"><span data-stu-id="0a195-183">SQL</span></span>

* <span data-ttu-id="0a195-184">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-184">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="0a195-185">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-185">Added `sql db rename`</span></span>
* <span data-ttu-id="0a195-186">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-186">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="0a195-187">Storage</span><span class="sxs-lookup"><span data-stu-id="0a195-187">Storage</span></span>

* <span data-ttu-id="0a195-188">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-188">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-189">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-189">VM</span></span>

* <span data-ttu-id="0a195-190">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-190">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="0a195-191">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-191">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="0a195-192">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="0a195-192">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="0a195-193">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0a195-193">January 31, 2018</span></span>

<span data-ttu-id="0a195-194">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="0a195-194">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="0a195-195">コア</span><span class="sxs-lookup"><span data-stu-id="0a195-195">Core</span></span>

* <span data-ttu-id="0a195-196">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-196">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="0a195-197">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="0a195-197">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="0a195-198">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-198">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="0a195-199">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="0a195-199">Use `--verbose` to see</span></span>
* <span data-ttu-id="0a195-200">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="0a195-200">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="0a195-201">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-201">ACS</span></span>

* <span data-ttu-id="0a195-202">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="0a195-202">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="0a195-203">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="0a195-203">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-204">Appservice</span><span class="sxs-lookup"><span data-stu-id="0a195-204">Appservice</span></span>

* <span data-ttu-id="0a195-205">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="0a195-205">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="0a195-206">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="0a195-206">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="0a195-207">CDN</span><span class="sxs-lookup"><span data-stu-id="0a195-207">CDN</span></span>

* <span data-ttu-id="0a195-208">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-208">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="0a195-209">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="0a195-209">CosmosDB</span></span>

* <span data-ttu-id="0a195-210">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-210">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="0a195-211">対話</span><span class="sxs-lookup"><span data-stu-id="0a195-211">Interactive</span></span>

* <span data-ttu-id="0a195-212">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-212">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="0a195-213">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="0a195-213">Network</span></span>

* <span data-ttu-id="0a195-214">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-214">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="0a195-215">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-215">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="0a195-216">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-216">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="0a195-217">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-217">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="0a195-218">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-218">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="0a195-219">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-219">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="0a195-220">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-220">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="0a195-221">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-221">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="0a195-222">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-222">Fixed issue where certain records were imported twice with `dns zone import`</span></span> 
* <span data-ttu-id="0a195-223">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="0a195-223">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="0a195-224">プロファイル</span><span class="sxs-lookup"><span data-stu-id="0a195-224">Profile</span></span>

* <span data-ttu-id="0a195-225">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-225">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="0a195-226">リソース</span><span class="sxs-lookup"><span data-stu-id="0a195-226">Resource</span></span>

* <span data-ttu-id="0a195-227">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-227">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="0a195-228">Storage</span><span class="sxs-lookup"><span data-stu-id="0a195-228">Storage</span></span>

* <span data-ttu-id="0a195-229">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-229">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="0a195-230">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-230">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="0a195-231">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-231">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>  
* <span data-ttu-id="0a195-232">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-232">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="0a195-233">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-233">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-234">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-234">VM</span></span>

* <span data-ttu-id="0a195-235">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-235">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="0a195-236">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-236">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="0a195-237">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-237">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="0a195-238">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-238">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="0a195-239">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="0a195-239">January 17, 2018</span></span>

<span data-ttu-id="0a195-240">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="0a195-240">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="0a195-241">ACR</span><span class="sxs-lookup"><span data-stu-id="0a195-241">ACR</span></span>

* <span data-ttu-id="0a195-242">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-242">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="0a195-243">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="0a195-243">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="0a195-244">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-244">ACS</span></span>

* <span data-ttu-id="0a195-245">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-245">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="0a195-246">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="0a195-246">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-247">Appservice</span><span class="sxs-lookup"><span data-stu-id="0a195-247">Appservice</span></span>

* <span data-ttu-id="0a195-248">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-248">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="0a195-249">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-249">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="0a195-250">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-250">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="0a195-251">Backup</span><span class="sxs-lookup"><span data-stu-id="0a195-251">Backup</span></span>

* <span data-ttu-id="0a195-252">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-252">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="0a195-253">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-253">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="0a195-254">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-254">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="0a195-255">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-255">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="0a195-256">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-256">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="0a195-257">Batch</span><span class="sxs-lookup"><span data-stu-id="0a195-257">Batch</span></span>

* <span data-ttu-id="0a195-258">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-258">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="0a195-259">クラウド</span><span class="sxs-lookup"><span data-stu-id="0a195-259">Cloud</span></span>

* <span data-ttu-id="0a195-260">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-260">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="0a195-261">消費</span><span class="sxs-lookup"><span data-stu-id="0a195-261">Consumption</span></span>

* <span data-ttu-id="0a195-262">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-262">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="0a195-263">Event Grid</span><span class="sxs-lookup"><span data-stu-id="0a195-263">Event Grid</span></span>

* <span data-ttu-id="0a195-264">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="0a195-264">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="0a195-265">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="0a195-265">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="0a195-266">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="0a195-266">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="0a195-267">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="0a195-267">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="0a195-268">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-268">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="0a195-269">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-269">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="0a195-270">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-270">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="0a195-271">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-271">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="0a195-272">対話</span><span class="sxs-lookup"><span data-stu-id="0a195-272">Interactive</span></span>

* <span data-ttu-id="0a195-273">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="0a195-273">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="0a195-274">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-274">Fixed errors on startup</span></span>
* <span data-ttu-id="0a195-275">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-275">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="0a195-276">IoT</span><span class="sxs-lookup"><span data-stu-id="0a195-276">IoT</span></span>

* <span data-ttu-id="0a195-277">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-277">Added support for device provisioning service</span></span>
* <span data-ttu-id="0a195-278">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-278">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="0a195-279">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-279">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="0a195-280">監視</span><span class="sxs-lookup"><span data-stu-id="0a195-280">Monitor</span></span>

* <span data-ttu-id="0a195-281">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-281">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="0a195-282">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="0a195-282">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="0a195-283">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-283">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="0a195-284">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="0a195-284">Network</span></span>

* <span data-ttu-id="0a195-285">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-285">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="0a195-286">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-286">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="0a195-287">プロファイル</span><span class="sxs-lookup"><span data-stu-id="0a195-287">Profile</span></span>

* <span data-ttu-id="0a195-288">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-288">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="0a195-289">役割</span><span class="sxs-lookup"><span data-stu-id="0a195-289">Role</span></span>

* <span data-ttu-id="0a195-290">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-290">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="0a195-291">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="0a195-291">Service Fabric</span></span>

* <span data-ttu-id="0a195-292">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-292">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="0a195-293">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-293">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-294">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-294">VM</span></span>

* <span data-ttu-id="0a195-295">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="0a195-295">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="0a195-296">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-296">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="0a195-297">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-297">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="0a195-298">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-298">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="0a195-299">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-299">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="0a195-300">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-300">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="0a195-301">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-301">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="0a195-302">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-302">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="0a195-303">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="0a195-303">December 19, 2017</span></span>

<span data-ttu-id="0a195-304">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="0a195-304">Version 2.0.23</span></span>

* <span data-ttu-id="0a195-305">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-305">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="0a195-306">コンテナー</span><span class="sxs-lookup"><span data-stu-id="0a195-306">Container</span></span>

* <span data-ttu-id="0a195-307">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-307">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="0a195-308">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="0a195-308">Network</span></span>

* <span data-ttu-id="0a195-309">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-309">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="0a195-310">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-310">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="0a195-311">Storage</span><span class="sxs-lookup"><span data-stu-id="0a195-311">Storage</span></span>

* <span data-ttu-id="0a195-312">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-312">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-313">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-313">VM</span></span>

* <span data-ttu-id="0a195-314">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-314">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="0a195-315">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="0a195-315">December 5, 2017</span></span>

<span data-ttu-id="0a195-316">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="0a195-316">Version 2.0.22</span></span>

* <span data-ttu-id="0a195-317">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-317">Removed `az component` commands.</span></span> <span data-ttu-id="0a195-318">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="0a195-318">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="0a195-319">コア</span><span class="sxs-lookup"><span data-stu-id="0a195-319">Core</span></span>
* <span data-ttu-id="0a195-320">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-320">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="0a195-321">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-321">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="0a195-322">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-322">ACS</span></span>

* <span data-ttu-id="0a195-323">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-323">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="0a195-324">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="0a195-324">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="0a195-325">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-325">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="0a195-326">Advisor</span><span class="sxs-lookup"><span data-stu-id="0a195-326">Advisor</span></span>

* <span data-ttu-id="0a195-327">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="0a195-327">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-328">Appservice</span><span class="sxs-lookup"><span data-stu-id="0a195-328">Appservice</span></span>

* <span data-ttu-id="0a195-329">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-329">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="0a195-330">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-330">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="0a195-331">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-331">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="0a195-332">消費</span><span class="sxs-lookup"><span data-stu-id="0a195-332">Consumption</span></span>

* <span data-ttu-id="0a195-333">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-333">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="0a195-334">コンテナー</span><span class="sxs-lookup"><span data-stu-id="0a195-334">Container</span></span>

* <span data-ttu-id="0a195-335">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-335">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="0a195-336">監視</span><span class="sxs-lookup"><span data-stu-id="0a195-336">Monitor</span></span>

* <span data-ttu-id="0a195-337">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-337">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="0a195-338">リソース</span><span class="sxs-lookup"><span data-stu-id="0a195-338">Resource</span></span>

* <span data-ttu-id="0a195-339">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-339">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="0a195-340">役割</span><span class="sxs-lookup"><span data-stu-id="0a195-340">Role</span></span>

* <span data-ttu-id="0a195-341">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-341">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="0a195-342">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="0a195-342">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="0a195-343">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="0a195-343">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="0a195-344">SQL</span><span class="sxs-lookup"><span data-stu-id="0a195-344">SQL</span></span>

* <span data-ttu-id="0a195-345">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-345">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="0a195-346">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-346">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-347">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-347">VM</span></span>

* <span data-ttu-id="0a195-348">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-348">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="0a195-349">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="0a195-349">November 14, 2017</span></span>

<span data-ttu-id="0a195-350">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="0a195-350">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="0a195-351">ACR</span><span class="sxs-lookup"><span data-stu-id="0a195-351">ACR</span></span>

* <span data-ttu-id="0a195-352">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-352">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="0a195-353">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-353">ACS</span></span>

* <span data-ttu-id="0a195-354">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-354">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="0a195-355">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="0a195-355">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="0a195-356">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-356">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="0a195-357">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-357">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="0a195-358">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-358">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-359">Appservice</span><span class="sxs-lookup"><span data-stu-id="0a195-359">Appservice</span></span>

* <span data-ttu-id="0a195-360">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-360">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="0a195-361">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-361">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="0a195-362">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="0a195-362">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="0a195-363">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="0a195-363">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="0a195-364">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-364">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="0a195-365">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="0a195-365">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="0a195-366">Batch</span><span class="sxs-lookup"><span data-stu-id="0a195-366">Batch</span></span>

* <span data-ttu-id="0a195-367">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-367">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="0a195-368">Batchai</span><span class="sxs-lookup"><span data-stu-id="0a195-368">Batchai</span></span>

* <span data-ttu-id="0a195-369">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-369">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="0a195-370">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-370">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="0a195-371">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-371">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="0a195-372">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-372">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="0a195-373">クラウド</span><span class="sxs-lookup"><span data-stu-id="0a195-373">Cloud</span></span>

* <span data-ttu-id="0a195-374">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-374">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="0a195-375">コンテナー</span><span class="sxs-lookup"><span data-stu-id="0a195-375">Container</span></span>

* <span data-ttu-id="0a195-376">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-376">Added support to open multiple ports</span></span>
* <span data-ttu-id="0a195-377">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-377">Added container group restart policy</span></span>
* <span data-ttu-id="0a195-378">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-378">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="0a195-379">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="0a195-379">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="0a195-380">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="0a195-380">Data Lake Analytics</span></span>

* <span data-ttu-id="0a195-381">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-381">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="0a195-382">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="0a195-382">Data Lake Store</span></span>

* <span data-ttu-id="0a195-383">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-383">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="0a195-384">内線番号</span><span class="sxs-lookup"><span data-stu-id="0a195-384">Extension</span></span>

* <span data-ttu-id="0a195-385">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-385">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="0a195-386">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-386">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="0a195-387">IoT</span><span class="sxs-lookup"><span data-stu-id="0a195-387">IoT</span></span>

* <span data-ttu-id="0a195-388">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-388">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="0a195-389">監視</span><span class="sxs-lookup"><span data-stu-id="0a195-389">Monitor</span></span>

* <span data-ttu-id="0a195-390">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-390">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="0a195-391">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="0a195-391">Network</span></span>

* <span data-ttu-id="0a195-392">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-392">Added support for CAA DNS records</span></span>
* <span data-ttu-id="0a195-393">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-393">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="0a195-394">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-394">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="0a195-395">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-395">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="0a195-396">Reservations</span><span class="sxs-lookup"><span data-stu-id="0a195-396">Reservations</span></span>

* <span data-ttu-id="0a195-397">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="0a195-397">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="0a195-398">リソース</span><span class="sxs-lookup"><span data-stu-id="0a195-398">Resource</span></span>

* <span data-ttu-id="0a195-399">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-399">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="0a195-400">SQL</span><span class="sxs-lookup"><span data-stu-id="0a195-400">SQL</span></span>

* <span data-ttu-id="0a195-401">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-401">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="0a195-402">Storage</span><span class="sxs-lookup"><span data-stu-id="0a195-402">Storage</span></span>

* <span data-ttu-id="0a195-403">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-403">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="0a195-404">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-404">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="0a195-405">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-405">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="0a195-406">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-406">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="0a195-407">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-407">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="0a195-408">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-408">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="0a195-409">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-409">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-410">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-410">VM</span></span>

* <span data-ttu-id="0a195-411">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-411">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="0a195-412">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-412">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="0a195-413">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-413">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="0a195-414">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-414">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="0a195-415">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-415">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="0a195-416">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="0a195-416">October 24, 2017</span></span>

<span data-ttu-id="0a195-417">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="0a195-417">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="0a195-418">コア</span><span class="sxs-lookup"><span data-stu-id="0a195-418">Core</span></span>

* <span data-ttu-id="0a195-419">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="0a195-419">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="0a195-420">ACR</span><span class="sxs-lookup"><span data-stu-id="0a195-420">ACR</span></span>

* <span data-ttu-id="0a195-421">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="0a195-421">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="0a195-422">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-422">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="0a195-423">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-423">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="0a195-424">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-424">ACS</span></span>

* <span data-ttu-id="0a195-425">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-425">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="0a195-426">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-426">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-427">Appservice</span><span class="sxs-lookup"><span data-stu-id="0a195-427">Appservice</span></span>

* <span data-ttu-id="0a195-428">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-428">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="0a195-429">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0a195-429">Component</span></span>

* <span data-ttu-id="0a195-430">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-430">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="0a195-431">監視</span><span class="sxs-lookup"><span data-stu-id="0a195-431">Monitor</span></span>

* <span data-ttu-id="0a195-432">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-432">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="0a195-433">リソース</span><span class="sxs-lookup"><span data-stu-id="0a195-433">Resource</span></span>

* <span data-ttu-id="0a195-434">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-434">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="0a195-435">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-435">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-436">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-436">VM</span></span>

* <span data-ttu-id="0a195-437">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-437">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="0a195-438">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="0a195-438">October 9, 2017</span></span>

<span data-ttu-id="0a195-439">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="0a195-439">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="0a195-440">コア</span><span class="sxs-lookup"><span data-stu-id="0a195-440">Core</span></span>

* <span data-ttu-id="0a195-441">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-441">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-442">Appservice</span><span class="sxs-lookup"><span data-stu-id="0a195-442">Appservice</span></span>

* <span data-ttu-id="0a195-443">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-443">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="0a195-444">Batch</span><span class="sxs-lookup"><span data-stu-id="0a195-444">Batch</span></span>

* <span data-ttu-id="0a195-445">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="0a195-445">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="0a195-446">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="0a195-446">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="0a195-447">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-447">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="0a195-448">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="0a195-448">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="0a195-449">Batchai</span><span class="sxs-lookup"><span data-stu-id="0a195-449">Batchai</span></span>

* <span data-ttu-id="0a195-450">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="0a195-450">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="0a195-451">KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a195-451">Keyvault</span></span>

* <span data-ttu-id="0a195-452">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-452">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="0a195-453">(#4448)</span><span class="sxs-lookup"><span data-stu-id="0a195-453">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="0a195-454">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="0a195-454">Network</span></span>

* <span data-ttu-id="0a195-455">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-455">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="0a195-456">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="0a195-456">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="0a195-457">リソース</span><span class="sxs-lookup"><span data-stu-id="0a195-457">Resource</span></span>

* <span data-ttu-id="0a195-458">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-458">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="0a195-459">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-459">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="0a195-460">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-460">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="0a195-461">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-461">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="0a195-462">SQL</span><span class="sxs-lookup"><span data-stu-id="0a195-462">Sql</span></span>

* <span data-ttu-id="0a195-463">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-463">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="0a195-464">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="0a195-464">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="0a195-465">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="0a195-465">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="0a195-466">Storage</span><span class="sxs-lookup"><span data-stu-id="0a195-466">Storage</span></span>

* <span data-ttu-id="0a195-467">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-467">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-468">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-468">Vm</span></span>

* <span data-ttu-id="0a195-469">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-469">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="0a195-470">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-470">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="0a195-471">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-471">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="0a195-472">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-472">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="0a195-473">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-473">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="0a195-474">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="0a195-474">September 22, 2017</span></span>

<span data-ttu-id="0a195-475">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="0a195-475">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="0a195-476">リソース</span><span class="sxs-lookup"><span data-stu-id="0a195-476">Resource</span></span>

* <span data-ttu-id="0a195-477">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-477">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="0a195-478">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-478">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="0a195-479">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-479">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="0a195-480">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-480">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="0a195-481">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="0a195-481">Network</span></span>

* <span data-ttu-id="0a195-482">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-482">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="0a195-483">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-483">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="0a195-484">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-484">Added `asg` application security group commands</span></span>
* <span data-ttu-id="0a195-485">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-485">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="0a195-486">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-486">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="0a195-487">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-487">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="0a195-488">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-488">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="0a195-489">Storage</span><span class="sxs-lookup"><span data-stu-id="0a195-489">Storage</span></span>

* <span data-ttu-id="0a195-490">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-490">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="0a195-491">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="0a195-491">Eventgrid</span></span>

* <span data-ttu-id="0a195-492">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="0a195-492">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="0a195-493">SQL</span><span class="sxs-lookup"><span data-stu-id="0a195-493">SQL</span></span>

* <span data-ttu-id="0a195-494">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-494">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="0a195-495">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="0a195-495">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="0a195-496">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-496">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="0a195-497">KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a195-497">Keyvault</span></span>

* <span data-ttu-id="0a195-498">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-498">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-499">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-499">VM</span></span>

* <span data-ttu-id="0a195-500">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-500">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="0a195-501">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-501">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="0a195-502">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-502">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="0a195-503">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-503">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="0a195-504">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-504">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="0a195-505">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-505">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="0a195-506">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-506">ACS</span></span>

* <span data-ttu-id="0a195-507">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-507">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-508">Appservice</span><span class="sxs-lookup"><span data-stu-id="0a195-508">Appservice</span></span>

* <span data-ttu-id="0a195-509">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-509">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="0a195-510">Backup</span><span class="sxs-lookup"><span data-stu-id="0a195-510">Backup</span></span>

* <span data-ttu-id="0a195-511">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="0a195-511">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="0a195-512">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="0a195-512">September 11, 2017</span></span>

<span data-ttu-id="0a195-513">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="0a195-513">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="0a195-514">コア</span><span class="sxs-lookup"><span data-stu-id="0a195-514">Core</span></span>

* <span data-ttu-id="0a195-515">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="0a195-515">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="0a195-516">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-516">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="0a195-517">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-517">Acs</span></span>

* <span data-ttu-id="0a195-518">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-518">Added `acs list-locations` command</span></span>
* <span data-ttu-id="0a195-519">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="0a195-519">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-520">Appservice</span><span class="sxs-lookup"><span data-stu-id="0a195-520">Appservice</span></span>

* <span data-ttu-id="0a195-521">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-521">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="0a195-522">CDN</span><span class="sxs-lookup"><span data-stu-id="0a195-522">CDN</span></span>

* <span data-ttu-id="0a195-523">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-523">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="0a195-524">内線番号</span><span class="sxs-lookup"><span data-stu-id="0a195-524">Extension</span></span>

* <span data-ttu-id="0a195-525">最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="0a195-525">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="0a195-526">KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a195-526">Keyvault</span></span>

* <span data-ttu-id="0a195-527">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-527">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="0a195-528">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="0a195-528">Network</span></span>

* <span data-ttu-id="0a195-529">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-529">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="0a195-530">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-530">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="0a195-531">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-531">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="0a195-532">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-532">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="0a195-533">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-533">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="0a195-534">リソース</span><span class="sxs-lookup"><span data-stu-id="0a195-534">Resource</span></span>

* <span data-ttu-id="0a195-535">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="0a195-535">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="0a195-536">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="0a195-536">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="0a195-537">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="0a195-537">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="0a195-538">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="0a195-538">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="0a195-539">SQL</span><span class="sxs-lookup"><span data-stu-id="0a195-539">SQL</span></span>

* <span data-ttu-id="0a195-540">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-540">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-541">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-541">VM</span></span>

* <span data-ttu-id="0a195-542">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="0a195-542">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="0a195-543">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="0a195-543">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="0a195-544">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="0a195-544">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="0a195-545">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="0a195-545">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="0a195-546">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="0a195-546">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="0a195-547">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0a195-547">August 31, 2017</span></span>

<span data-ttu-id="0a195-548">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="0a195-548">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="0a195-549">KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a195-549">Keyvault</span></span>

* <span data-ttu-id="0a195-550">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-550">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="0a195-551">SF</span><span class="sxs-lookup"><span data-stu-id="0a195-551">Sf</span></span>

* <span data-ttu-id="0a195-552">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="0a195-552">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="0a195-553">Storage</span><span class="sxs-lookup"><span data-stu-id="0a195-553">Storage</span></span>

* <span data-ttu-id="0a195-554">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-554">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="0a195-555">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="0a195-555">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="0a195-556">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="0a195-556">August 28, 2017</span></span>

<span data-ttu-id="0a195-557">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="0a195-557">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="0a195-558">CLI</span><span class="sxs-lookup"><span data-stu-id="0a195-558">CLI</span></span>

* <span data-ttu-id="0a195-559">`--version` に法的事項を追加しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-559">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="0a195-560">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-560">ACS</span></span>

* <span data-ttu-id="0a195-561">プレビュー リージョンを修正しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-561">Corrected preview regions.</span></span>
* <span data-ttu-id="0a195-562">既定の `dns_name_prefix` を正しい形式にしました。</span><span class="sxs-lookup"><span data-stu-id="0a195-562">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="0a195-563">ACS コマンド出力を最適化しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-563">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-564">Appservice</span><span class="sxs-lookup"><span data-stu-id="0a195-564">Appservice</span></span>

* <span data-ttu-id="0a195-565">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-565">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="0a195-566">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-566">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="0a195-567">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="0a195-567">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="0a195-568">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="0a195-568">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="0a195-569">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="0a195-569">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="0a195-570">IoT</span><span class="sxs-lookup"><span data-stu-id="0a195-570">IoT</span></span>

* <span data-ttu-id="0a195-571">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="0a195-571">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="0a195-572">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="0a195-572">Network</span></span>

* <span data-ttu-id="0a195-573">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-573">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="0a195-574">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-574">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="0a195-575">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-575">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="0a195-576">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-576">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="0a195-577">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-577">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="0a195-578">プロファイル</span><span class="sxs-lookup"><span data-stu-id="0a195-578">Profile</span></span>

* <span data-ttu-id="0a195-579">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="0a195-579">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="0a195-580">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="0a195-580">Service Fabric</span></span>

* <span data-ttu-id="0a195-581">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="0a195-581">Preview release</span></span>
* <span data-ttu-id="0a195-582">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="0a195-582">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="0a195-583">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-583">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="0a195-584">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-584">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="0a195-585">Storage</span><span class="sxs-lookup"><span data-stu-id="0a195-585">Storage</span></span>

* <span data-ttu-id="0a195-586">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="0a195-586">Enabled setting blob tier</span></span>
* <span data-ttu-id="0a195-587">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-587">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="0a195-588">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-588">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="0a195-589">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="0a195-589">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="0a195-590">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-590">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="0a195-591">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="0a195-591">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-592">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-592">VM</span></span>

* <span data-ttu-id="0a195-593">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-593">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="0a195-594">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-594">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="0a195-595">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="0a195-595">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="0a195-596">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-596">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="0a195-597">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-597">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="0a195-598">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-598">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="0a195-599">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="0a195-599">August 15, 2017</span></span>

<span data-ttu-id="0a195-600">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="0a195-600">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="0a195-601">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-601">ACS</span></span>

* <span data-ttu-id="0a195-602">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-602">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-603">Appservice</span><span class="sxs-lookup"><span data-stu-id="0a195-603">Appservice</span></span>

* <span data-ttu-id="0a195-604">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-604">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="0a195-605">Event Grid</span><span class="sxs-lookup"><span data-stu-id="0a195-605">Event Grid</span></span>

* <span data-ttu-id="0a195-606">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-606">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="0a195-607">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="0a195-607">August 11, 2017</span></span>

<span data-ttu-id="0a195-608">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="0a195-608">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="0a195-609">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-609">ACS</span></span>

* <span data-ttu-id="0a195-610">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-610">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="0a195-611">Batch</span><span class="sxs-lookup"><span data-stu-id="0a195-611">Batch</span></span>

* <span data-ttu-id="0a195-612">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="0a195-612">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="0a195-613">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-613">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="0a195-614">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-614">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="0a195-615">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="0a195-615">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="0a195-616">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-616">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="0a195-617">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-617">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="0a195-618">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0a195-618">Component</span></span>

* <span data-ttu-id="0a195-619">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-619">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="0a195-620">コンテナー</span><span class="sxs-lookup"><span data-stu-id="0a195-620">Container</span></span>

* <span data-ttu-id="0a195-621">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-621">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="0a195-622">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="0a195-622">Data Lake Store</span></span>

* <span data-ttu-id="0a195-623">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="0a195-623">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="0a195-624">Event Grid</span><span class="sxs-lookup"><span data-stu-id="0a195-624">Event Grid</span></span>

* <span data-ttu-id="0a195-625">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="0a195-625">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="0a195-626">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="0a195-626">Network</span></span>

* <span data-ttu-id="0a195-627">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-627">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="0a195-628">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-628">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="0a195-629">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-629">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="0a195-630">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-630">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="0a195-631">プロファイル</span><span class="sxs-lookup"><span data-stu-id="0a195-631">Profile</span></span>

* <span data-ttu-id="0a195-632">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-632">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="0a195-633">Storage</span><span class="sxs-lookup"><span data-stu-id="0a195-633">Storage</span></span>

* <span data-ttu-id="0a195-634">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="0a195-634">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-635">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-635">VM</span></span>

* <span data-ttu-id="0a195-636">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="0a195-636">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="0a195-637">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="0a195-637">Exposed `list-skus` command</span></span>
* <span data-ttu-id="0a195-638">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-638">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="0a195-639">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="0a195-639">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="0a195-640">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="0a195-640">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="0a195-641">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="0a195-641">July 28, 2017</span></span>

<span data-ttu-id="0a195-642">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="0a195-642">Version 2.0.12</span></span>

* <span data-ttu-id="0a195-643">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-643">Added container commands</span></span>
* <span data-ttu-id="0a195-644">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-644">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="0a195-645">コア</span><span class="sxs-lookup"><span data-stu-id="0a195-645">Core</span></span>

* <span data-ttu-id="0a195-646">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="0a195-646">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="0a195-647">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-647">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="0a195-648">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="0a195-648">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="0a195-649">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="0a195-649">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="0a195-650">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="0a195-650">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="0a195-651">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="0a195-651">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="0a195-652">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="0a195-652">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="0a195-653">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="0a195-653">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="0a195-654">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="0a195-654">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="0a195-655">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="0a195-655">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="0a195-656">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="0a195-656">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="0a195-657">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="0a195-657">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="0a195-658">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="0a195-658">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="0a195-659">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="0a195-659">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="0a195-660">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-660">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="0a195-661">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="0a195-661">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="0a195-662">ACR</span><span class="sxs-lookup"><span data-stu-id="0a195-662">ACR</span></span>

* <span data-ttu-id="0a195-663">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-663">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="0a195-664">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-664">Support SKU update for managed registries</span></span>
* <span data-ttu-id="0a195-665">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-665">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="0a195-666">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-666">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="0a195-667">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-667">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="0a195-668">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-668">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="0a195-669">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-669">ACS</span></span>

* <span data-ttu-id="0a195-670">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-670">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-671">Appservice</span><span class="sxs-lookup"><span data-stu-id="0a195-671">Appservice</span></span>

* <span data-ttu-id="0a195-672">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-672">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="0a195-673">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-673">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="0a195-674">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="0a195-674">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="0a195-675">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="0a195-675">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="0a195-676">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="0a195-676">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="0a195-677">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="0a195-677">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="0a195-678">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="0a195-678">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="0a195-679">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="0a195-679">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="0a195-680">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-680">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="0a195-681">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="0a195-681">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="0a195-682">Batch</span><span class="sxs-lookup"><span data-stu-id="0a195-682">Batch</span></span>

* <span data-ttu-id="0a195-683">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="0a195-683">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="0a195-684">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-684">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="0a195-685">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-685">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="0a195-686">CDN</span><span class="sxs-lookup"><span data-stu-id="0a195-686">CDN</span></span>

* <span data-ttu-id="0a195-687">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-687">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="0a195-688">クラウド</span><span class="sxs-lookup"><span data-stu-id="0a195-688">Cloud</span></span>

* <span data-ttu-id="0a195-689">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-689">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="0a195-690">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="0a195-690">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="0a195-691">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-691">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="0a195-692">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="0a195-692">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="0a195-693">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="0a195-693">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="0a195-694">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="0a195-694">CosmosDB</span></span>

* <span data-ttu-id="0a195-695">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-695">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="0a195-696">既定のコレクション TTL のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-696">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="0a195-697">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="0a195-697">Data Lake Analytics</span></span>

* <span data-ttu-id="0a195-698">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-698">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="0a195-699">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-699">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="0a195-700">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-700">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="0a195-701">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="0a195-701">Data Lake Store</span></span>

* <span data-ttu-id="0a195-702">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-702">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="0a195-703">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="0a195-703">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="0a195-704">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-704">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="0a195-705">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="0a195-705">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="0a195-706">対話</span><span class="sxs-lookup"><span data-stu-id="0a195-706">Interactive</span></span>

* <span data-ttu-id="0a195-707">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="0a195-707">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="0a195-708">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="0a195-708">Increased test coverage</span></span>
* <span data-ttu-id="0a195-709">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="0a195-709">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="0a195-710">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="0a195-710">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="0a195-711">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="0a195-711">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="0a195-712">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="0a195-712">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="0a195-713">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="0a195-713">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="0a195-714">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-714">Added `--progress` flag</span></span>
* <span data-ttu-id="0a195-715">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="0a195-715">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="0a195-716">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="0a195-716">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="0a195-717">IoT</span><span class="sxs-lookup"><span data-stu-id="0a195-717">IoT</span></span>

* <span data-ttu-id="0a195-718">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-718">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="0a195-719">(#3934)</span><span class="sxs-lookup"><span data-stu-id="0a195-719">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="0a195-720">Key Vault</span><span class="sxs-lookup"><span data-stu-id="0a195-720">Key vault</span></span>

* <span data-ttu-id="0a195-721">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-721">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="0a195-722">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="0a195-722">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="0a195-723">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="0a195-723">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="0a195-724">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="0a195-724">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="0a195-725">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="0a195-725">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="0a195-726">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="0a195-726">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="0a195-727">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-727">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="0a195-728">(#3307)</span><span class="sxs-lookup"><span data-stu-id="0a195-728">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="0a195-729">ラボ</span><span class="sxs-lookup"><span data-stu-id="0a195-729">Lab</span></span>

* <span data-ttu-id="0a195-730">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-730">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="0a195-731">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-731">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="0a195-732">監視</span><span class="sxs-lookup"><span data-stu-id="0a195-732">Monitor</span></span>

* <span data-ttu-id="0a195-733">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="0a195-733">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="0a195-734">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-734">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="0a195-735">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-735">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="0a195-736">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-736">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="0a195-737">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="0a195-737">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="0a195-738">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-738">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="0a195-739">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="0a195-739">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="0a195-740">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="0a195-740">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="0a195-741">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="0a195-741">`location` no longer required</span></span>
  * <span data-ttu-id="0a195-742">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="0a195-742">Add name and ID support for target</span></span>
  * <span data-ttu-id="0a195-743">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="0a195-743">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="0a195-744">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="0a195-744">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="0a195-745">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="0a195-745">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="0a195-746">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="0a195-746">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="0a195-747">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-747">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="0a195-748">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-748">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="0a195-749">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="0a195-749">Network</span></span>

* <span data-ttu-id="0a195-750">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-750">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="0a195-751">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-751">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="0a195-752">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-752">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="0a195-753">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-753">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="0a195-754">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-754">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="0a195-755">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-755">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="0a195-756">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-756">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="0a195-757">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-757">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="0a195-758">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-758">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="0a195-759">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-759">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="0a195-760">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-760">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="0a195-761">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-761">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="0a195-762">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-762">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="0a195-763">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-763">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="0a195-764">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-764">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="0a195-765">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="0a195-765">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="0a195-766">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-766">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="0a195-767">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-767">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="0a195-768">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-768">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="0a195-769">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-769">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="0a195-770">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-770">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="0a195-771">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-771">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="0a195-772">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="0a195-772">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="0a195-773">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="0a195-773">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="0a195-774">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="0a195-774">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="0a195-775">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="0a195-775">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="0a195-776">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="0a195-776">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="0a195-777">プロファイル</span><span class="sxs-lookup"><span data-stu-id="0a195-777">Profile</span></span>

* <span data-ttu-id="0a195-778">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-778">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="0a195-779">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-779">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="0a195-780">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="0a195-780">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="0a195-781">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-781">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="0a195-782">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-782">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="0a195-783">RDBMS</span><span class="sxs-lookup"><span data-stu-id="0a195-783">RDBMS</span></span>

* <span data-ttu-id="0a195-784">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="0a195-784">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="0a195-785">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="0a195-785">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="0a195-786">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="0a195-786">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="0a195-787">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="0a195-787">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="0a195-788">リソース</span><span class="sxs-lookup"><span data-stu-id="0a195-788">Resource</span></span>

* <span data-ttu-id="0a195-789">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="0a195-789">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="0a195-790">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="0a195-790">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="0a195-791">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-791">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="0a195-792">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-792">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="0a195-793">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="0a195-793">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="0a195-794">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-794">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="0a195-795">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="0a195-795">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="0a195-796">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-796">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="0a195-797">役割</span><span class="sxs-lookup"><span data-stu-id="0a195-797">Role</span></span>

* <span data-ttu-id="0a195-798">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-798">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="0a195-799">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="0a195-799">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="0a195-800">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="0a195-800">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="0a195-801">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="0a195-801">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="0a195-802">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-802">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="0a195-803">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="0a195-803">Service Fabric</span></span>
* <span data-ttu-id="0a195-804">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="0a195-804">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="0a195-805">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="0a195-805">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="0a195-806">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="0a195-806">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="0a195-807">SQL</span><span class="sxs-lookup"><span data-stu-id="0a195-807">SQL</span></span>

* <span data-ttu-id="0a195-808">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="0a195-808">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="0a195-809">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="0a195-809">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="0a195-810">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="0a195-810">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="0a195-811">Storage</span><span class="sxs-lookup"><span data-stu-id="0a195-811">Storage</span></span>

* <span data-ttu-id="0a195-812">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="0a195-812">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="0a195-813">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="0a195-813">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="0a195-814">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="0a195-814">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="0a195-815">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="0a195-815">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="0a195-816">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="0a195-816">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="0a195-817">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="0a195-817">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-818">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-818">VM</span></span>

* <span data-ttu-id="0a195-819">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-819">Support configuring nsg</span></span>
* <span data-ttu-id="0a195-820">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="0a195-820">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="0a195-821">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="0a195-821">Support managed service identities</span></span>
* <span data-ttu-id="0a195-822">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-822">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="0a195-823">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="0a195-823">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="0a195-824">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="0a195-824">May 10, 2017</span></span>

<span data-ttu-id="0a195-825">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="0a195-825">Version 2.0.6</span></span>

* <span data-ttu-id="0a195-826">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="0a195-826">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="0a195-827">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="0a195-827">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="0a195-828">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-828">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="0a195-829">Cognitive Services モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-829">Include Cognitive Services module.</span></span>
* <span data-ttu-id="0a195-830">Service Fabric モジュールが追加されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-830">Include Service Fabric module.</span></span>
* <span data-ttu-id="0a195-831">対話型モジュールが追加されました (az-shell の名前変更)。</span><span class="sxs-lookup"><span data-stu-id="0a195-831">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="0a195-832">CDN コマンドに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="0a195-832">Add support for CDN commands.</span></span>
* <span data-ttu-id="0a195-833">コンテナー モジュールが削除されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-833">Remove Container module.</span></span>
* <span data-ttu-id="0a195-834">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="0a195-834">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="0a195-835">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="0a195-835">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="0a195-836">コア</span><span class="sxs-lookup"><span data-stu-id="0a195-836">Core</span></span>

* <span data-ttu-id="0a195-837">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="0a195-837">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="0a195-838">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="0a195-838">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="0a195-839">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="0a195-839">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="0a195-840">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="0a195-840">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="0a195-841">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="0a195-841">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="0a195-842">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="0a195-842">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="0a195-843">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="0a195-843">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="0a195-844">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="0a195-844">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="0a195-845">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="0a195-845">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="0a195-846">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="0a195-846">core: Improved performance</span></span>
* <span data-ttu-id="0a195-847">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="0a195-847">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="0a195-848">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="0a195-848">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="0a195-849">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-849">ACS</span></span>

* <span data-ttu-id="0a195-850">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="0a195-850">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="0a195-851">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="0a195-851">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="0a195-852">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="0a195-852">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="0a195-853">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="0a195-853">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-854">AppService</span><span class="sxs-lookup"><span data-stu-id="0a195-854">AppService</span></span>

* <span data-ttu-id="0a195-855">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="0a195-855">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="0a195-856">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="0a195-856">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="0a195-857">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="0a195-857">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="0a195-858">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="0a195-858">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="0a195-859">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="0a195-859">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="0a195-860">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="0a195-860">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="0a195-861">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="0a195-861">support slot swap with preview</span></span>
* <span data-ttu-id="0a195-862">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="0a195-862">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="0a195-863">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="0a195-863">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="0a195-864">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0a195-864">CosmosDB</span></span>

* <span data-ttu-id="0a195-865">documentdb モジュールから cosmosdb に名前が変更されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-865">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="0a195-866">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="0a195-866">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="0a195-867">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="0a195-867">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="0a195-868">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="0a195-868">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="0a195-869">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="0a195-869">Data Lake Analytics</span></span>

* <span data-ttu-id="0a195-870">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-870">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="0a195-871">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="0a195-871">Add support for new catalog item type: package.</span></span> <span data-ttu-id="0a195-872">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="0a195-872">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="0a195-873">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="0a195-873">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="0a195-874">テーブル</span><span class="sxs-lookup"><span data-stu-id="0a195-874">Table</span></span>
  * <span data-ttu-id="0a195-875">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="0a195-875">Table valued function</span></span>
  * <span data-ttu-id="0a195-876">表示</span><span class="sxs-lookup"><span data-stu-id="0a195-876">View</span></span>
  * <span data-ttu-id="0a195-877">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="0a195-877">Table Statistics.</span></span> <span data-ttu-id="0a195-878">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0a195-878">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="0a195-879">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="0a195-879">Data Lake Store</span></span>

* <span data-ttu-id="0a195-880">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-880">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="0a195-881">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="0a195-881">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="0a195-882">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="0a195-882">missed help for access show.</span></span> <span data-ttu-id="0a195-883">追加しました </span><span class="sxs-lookup"><span data-stu-id="0a195-883">adding it.</span></span> <span data-ttu-id="0a195-884">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="0a195-884">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="0a195-885">検索</span><span class="sxs-lookup"><span data-stu-id="0a195-885">Find</span></span>

* <span data-ttu-id="0a195-886">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="0a195-886">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="0a195-887">KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a195-887">KeyVault</span></span>

* <span data-ttu-id="0a195-888">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="0a195-888">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="0a195-889">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-889">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="0a195-890">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的に上書きされます</span><span class="sxs-lookup"><span data-stu-id="0a195-890">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="0a195-891">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-891">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="0a195-892">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="0a195-892">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="0a195-893">ラボ</span><span class="sxs-lookup"><span data-stu-id="0a195-893">Lab</span></span>

* <span data-ttu-id="0a195-894">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-894">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="0a195-895">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-895">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="0a195-896">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-896">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="0a195-897">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-897">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="0a195-898">ラボ内でシークレットを管理するためのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-898">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="0a195-899">監視</span><span class="sxs-lookup"><span data-stu-id="0a195-899">Monitor</span></span>

* <span data-ttu-id="0a195-900">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="0a195-900">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="0a195-901">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="0a195-901">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="0a195-902">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="0a195-902">Network</span></span>

* <span data-ttu-id="0a195-903">`network watcher test-connectivity` コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-903">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="0a195-904">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="0a195-904">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="0a195-905">Application Gateway 接続のドレインに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="0a195-905">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="0a195-906">Application Gateway WAF 規則セットの構成に対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="0a195-906">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="0a195-907">ExpressRoute ルート フィルターとルールに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="0a195-907">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="0a195-908">TrafficManager の地理的なルーティングに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="0a195-908">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="0a195-909">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="0a195-909">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="0a195-910">VPN 接続 IPSec ポリシーに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="0a195-910">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="0a195-911">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-911">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="0a195-912">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="0a195-912">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="0a195-913">`network vpn-connection list/show` コマンドの出力から null 値が削除されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-913">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="0a195-914">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="0a195-914">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="0a195-915">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-915">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="0a195-916">`dns zone import` でレコードが適切にインポートされないバグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-916">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="0a195-917">`traffic-manager endpoint update` が動作しないバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="0a195-917">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="0a195-918">"Network Watcher" プレビューのコマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-918">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="0a195-919">プロファイル</span><span class="sxs-lookup"><span data-stu-id="0a195-919">Profile</span></span>

* <span data-ttu-id="0a195-920">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="0a195-920">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="0a195-921">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="0a195-921">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="0a195-922">Redis</span><span class="sxs-lookup"><span data-stu-id="0a195-922">Redis</span></span>

* <span data-ttu-id="0a195-923">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="0a195-923">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="0a195-924">"update-settings" コマンドが廃止されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-924">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="0a195-925">リソース</span><span class="sxs-lookup"><span data-stu-id="0a195-925">Resource</span></span>

* <span data-ttu-id="0a195-926">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="0a195-926">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="0a195-927">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="0a195-927">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="0a195-928">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="0a195-928">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="0a195-929">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="0a195-929">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="0a195-930">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="0a195-930">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="0a195-931">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="0a195-931">Add docs for az lock update.</span></span> <span data-ttu-id="0a195-932">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="0a195-932">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="0a195-933">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="0a195-933">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="0a195-934">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="0a195-934">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="0a195-935">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-935">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="0a195-936">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="0a195-936">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="0a195-937">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="0a195-937">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="0a195-938">役割</span><span class="sxs-lookup"><span data-stu-id="0a195-938">Role</span></span>

* <span data-ttu-id="0a195-939">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="0a195-939">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="0a195-940">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="0a195-940">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="0a195-941">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="0a195-941">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="0a195-942">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="0a195-942">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="0a195-943">SQL</span><span class="sxs-lookup"><span data-stu-id="0a195-943">SQL</span></span>

* <span data-ttu-id="0a195-944">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="0a195-944">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="0a195-945">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="0a195-945">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="0a195-946">Storage</span><span class="sxs-lookup"><span data-stu-id="0a195-946">Storage</span></span>

* <span data-ttu-id="0a195-947">`storage account create` のリソース グループの場所に対する既定の場所。</span><span class="sxs-lookup"><span data-stu-id="0a195-947">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="0a195-948">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="0a195-948">Add support for incremental blob copy</span></span>
* <span data-ttu-id="0a195-949">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="0a195-949">Add support for large block blob upload</span></span>
* <span data-ttu-id="0a195-950">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="0a195-950">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-951">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-951">VM</span></span>

* <span data-ttu-id="0a195-952">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="0a195-952">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="0a195-953">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="0a195-953">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="0a195-954">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="0a195-954">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="0a195-955">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="0a195-955">az vm/vmss disk</span></span>
  3. <span data-ttu-id="0a195-956">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="0a195-956">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="0a195-957">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="0a195-957">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="0a195-958">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="0a195-958">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="0a195-959">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="0a195-959">April 3, 2017</span></span>

<span data-ttu-id="0a195-960">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="0a195-960">Version 2.0.2</span></span>

<span data-ttu-id="0a195-961">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました。</span><span class="sxs-lookup"><span data-stu-id="0a195-961">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="0a195-962">コア</span><span class="sxs-lookup"><span data-stu-id="0a195-962">Core</span></span>

* <span data-ttu-id="0a195-963">既定の一覧に acr、lab、monitor、find モジュールを追加。</span><span class="sxs-lookup"><span data-stu-id="0a195-963">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="0a195-964">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="0a195-964">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="0a195-965">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="0a195-965">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="0a195-966">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="0a195-966">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="0a195-967">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="0a195-967">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="0a195-968">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="0a195-968">Add prompting for missing template parameters.</span></span> <span data-ttu-id="0a195-969">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="0a195-969">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="0a195-970">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="0a195-970">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="0a195-971">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="0a195-971">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="0a195-972">ACS</span><span class="sxs-lookup"><span data-stu-id="0a195-972">ACS</span></span>

* <span data-ttu-id="0a195-973">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="0a195-973">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="0a195-974">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="0a195-974">Add support for ssh key password prompting.</span></span> <span data-ttu-id="0a195-975">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="0a195-975">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="0a195-976">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="0a195-976">Add support for windows clusters.</span></span> <span data-ttu-id="0a195-977">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="0a195-977">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="0a195-978">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="0a195-978">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="0a195-979">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="0a195-979">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="0a195-980">AppService</span><span class="sxs-lookup"><span data-stu-id="0a195-980">AppService</span></span>

* <span data-ttu-id="0a195-981">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="0a195-981">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="0a195-982">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="0a195-982">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="0a195-983">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="0a195-983">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="0a195-984">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="0a195-984">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="0a195-985">DataLake</span><span class="sxs-lookup"><span data-stu-id="0a195-985">DataLake</span></span>

* <span data-ttu-id="0a195-986">Data Lake Analytics モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="0a195-986">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="0a195-987">Data Lake Store モジュールの最初のリリース。</span><span class="sxs-lookup"><span data-stu-id="0a195-987">Initial release of Data Lake Store module.</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="0a195-988">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="0a195-988">DocuemntDB</span></span>

* <span data-ttu-id="0a195-989">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="0a195-989">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="0a195-990">VM</span><span class="sxs-lookup"><span data-stu-id="0a195-990">VM</span></span>

* <span data-ttu-id="0a195-991">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="0a195-991">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="0a195-992">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="0a195-992">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="0a195-993">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="0a195-993">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="0a195-994">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="0a195-994">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="0a195-995">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="0a195-995">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="0a195-996">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="0a195-996">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="0a195-997">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="0a195-997">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="0a195-998">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="0a195-998">February 27, 2017</span></span>

<span data-ttu-id="0a195-999">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="0a195-999">Version 2.0.0</span></span>

<span data-ttu-id="0a195-1000">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。</span><span class="sxs-lookup"><span data-stu-id="0a195-1000">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="0a195-1001">一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="0a195-1001">General availability applies to these command modules:</span></span>
- <span data-ttu-id="0a195-1002">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="0a195-1002">Container Service (acs)</span></span>
- <span data-ttu-id="0a195-1003">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="0a195-1003">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="0a195-1004">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="0a195-1004">Networking</span></span>
- <span data-ttu-id="0a195-1005">Storage</span><span class="sxs-lookup"><span data-stu-id="0a195-1005">Storage</span></span>

<span data-ttu-id="0a195-1006">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="0a195-1006">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="0a195-1007">問題は、Microsoft サポートで直接開くことも、[github の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="0a195-1007">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="0a195-1008">[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="0a195-1008">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="0a195-1009">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません。</span><span class="sxs-lookup"><span data-stu-id="0a195-1009">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="0a195-1010">CLI のバージョンを確認するには、`az --version` を使用します。</span><span class="sxs-lookup"><span data-stu-id="0a195-1010">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="0a195-1011">出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="0a195-1011">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="0a195-1012">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。</span><span class="sxs-lookup"><span data-stu-id="0a195-1012">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="0a195-1013">これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です。</span><span class="sxs-lookup"><span data-stu-id="0a195-1013">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="0a195-1014">CLI のナイトリー プレビュー ビルドもあります。</span><span class="sxs-lookup"><span data-stu-id="0a195-1014">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="0a195-1015">詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0a195-1015">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="0a195-1016">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="0a195-1016">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="0a195-1017">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="0a195-1017">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="0a195-1018">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる。</span><span class="sxs-lookup"><span data-stu-id="0a195-1018">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="0a195-1019">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る。</span><span class="sxs-lookup"><span data-stu-id="0a195-1019">Provide feedback from the command line with the `az feedback` command.</span></span>

